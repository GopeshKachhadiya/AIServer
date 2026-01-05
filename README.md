# AIServer

# AI Server for LLM Security & Penetration Testing

---

## Project Overview

This project represents a self-hosted AI Server built on Windows 10 Pro, designed specifically for AI security researchers and penetration testers who want to analyze, test, and secure Large Language Models (LLMs) in a controlled environment.

The server uses Ollama to host and run multiple LLMs locally, enabling realistic testing scenarios without relying on cloud-based AI services.

This lab is intentionally created to simulate a real-world AI deployment that can be assessed for misconfigurations, insecure APIs, model abuse, prompt injection, data leakage, and other LLM-specific security risks.

---

## Objectives of the AI Server

- Provide a local AI infrastructure for hands-on LLM security testing
- Enable safe experimentation without exposing public APIs
- Support AI penetration testing methodologies
- Help researchers understand attack surfaces of self-hosted LLMs
- Bridge the gap between traditional penetration testing and AI security

---

## Intended Audience

This lab is suitable for:

- AI Penetration Testers
- Cybersecurity Students
- Red Team Operators
- AI Security Researchers
- Blue Team Engineers securing LLM deployments
- SOC Analysts learning AI threat models

---

## Key Features

- Windows-based AI server deployment
- Local LLM hosting using Ollama
- Offline model execution
- Multiple AI models supported
- Realistic AI service exposure for testing
- Safe environment for offensive and defensive research

---

## Technologies Used

- Operating System:
  - Windows 10 Pro (64-bit)

- AI Model Runtime:
  - Ollama

- AI Models:
  - Open-source LLMs (LLaMA-based, Mistral, Gemma, etc.)

- Virtualization (Optional):
  - VMware Workstation
  - VirtualBox

---

## Use Cases for AI Pentesting

- Prompt injection testing
- Model jailbreak attempts
- Unauthorized model access testing
- API abuse simulation
- Data leakage assessment
- Model misconfiguration detection
- AI supply chain risk analysis
- Secure deployment validation

---

## Lab Architecture Overview

- Attacker Machine:
  - Kali Linux or equivalent penetration testing OS
  - Used for interacting with and testing the AI server

- Target Machine:
  - Windows 10 Pro
  - Ollama installed and running
  - LLMs hosted locally

---

## Minimum System Requirements

### AI Server (Target Machine)

- CPU:
  - Quad-core processor or higher
- RAM:
  - Minimum 8 GB (16 GB recommended)
- Storage:
  - 50 GB free disk space
- OS:
  - Windows 10 Pro (64-bit)
- GPU (Optional):
  - Dedicated GPU for faster inference

### Attacker Machine

- CPU:
  - Dual-core processor or higher
- RAM:
  - 4 GB minimum
- OS:
  - Kali Linux / Parrot OS / Ubuntu

---

## Recreate This AI Server Lab

### Step 1: Install Windows 10 Pro

- Download Windows 10 Pro ISO from the official Microsoft website
- Install it on:
  - A physical machine, or
  - A virtual machine using VMware or VirtualBox
- Complete initial OS setup and updates

---

### Step 2: System Preparation

- Disable unnecessary background services
- Ensure sufficient disk space
- Configure network settings (NAT or Bridged)
- Assign a static IP address if required for testing

---

### Step 3: Install Ollama

- Download Ollama for Windows from the official Ollama website
- Install using default installation settings
- Verify installation using Command Prompt:

```powershell
ollama --version
```

Step 4: Download AI Models
```
Pull required LLM models using Ollama:

ollama pull llama2
ollama pull mistral
ollama pull gemma
```
- Verify installed models:
 ```
 ollama list
 ```
Step 5: Run the AI Server

- Start a model to verify functionality:
  ```
  ollama run llama2
  ```

- Confirm the model responds to prompts

- Ensure Ollama service remains running

Step 6: Network Exposure (For Testing Purposes)

- Identify listening ports used by Ollama

- Configure Windows Firewall rules if required

- Monitor network activity using:

- netstat

- Wireshark

- Confirm reachability from the attacker machine

Step 7: Pentesting Setup

- Configure attacker machine (Kali Linux)

- Perform:

  - Network enumeration

  - Service discovery

  - API interaction testing

  - Prompt injection attempts

  - Authorization and access control testing

## Security Focus Areas

- Authentication and authorization
- Model access control
- Prompt validation and sanitization
- Data retention and leakage risks
- Logging and monitoring
- Resource abuse and rate limiting

---

## Ethical Notice

This lab is created strictly for educational and defensive security research purposes.

- All testing must be performed only on systems you own
- Explicit authorization is required before testing any environment

---

## Project Structure

- AI Server Virtual Machine
- Ollama Configuration
- README.md
- Testing Notes (Optional)
- Future Enhancements Documentation

---

## Future Enhancements

- API-based LLM exposure
- Integration with OpenWebUI
- Role-based access control
- Centralized logging and alerting
- Secure deployment hardening guide

---

## Created By

- Name: Gopesh Kachhadiya
- Role: Junior Penetration Tester / AI Security Enthusiast
- Purpose: Internship Project and Skill Demonstration
- Domain: Offensive Security and AI Penetration Testing



