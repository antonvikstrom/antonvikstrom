# Hello, I'm Anton 👋

I am a cybersecurity professional transitioning from a career in education. I love building secure infrastructure, analyzing network traffic, and analyzing logs to solve complex security puzzles.

Below is the layout of my home lab, which I engineered on a bare-metal hypervisor to safely run attacks, study malware, and learn defensive monitoring.

<img width="782" height="763" alt="Screenshot 2026-07-06 at 21 13 20" src="https://github.com/user-attachments/assets/c8d68bf6-2eeb-4d28-b810-e6231c506adf" />

**Note:** This diagram shows the complete 6-zone enterprise network I am building. I use virtual switches in Proxmox to keep my lab traffic entirely isolated from my home network.

## Featured Projects

#### 1. [Building a Secure Home Cyber Lab: pfSense, Active Directory & Splunk](LINK_TO_REPO_1)
* **What I did:** I set up a bare-metal Proxmox hypervisor, built five isolated networks, and configured a pfSense firewall to enforce strict isolation. I stood up a Windows Server AD core, set up an unprivileged WireGuard remote-access gateway, and built a centralized telemetry pipeline feeding client logs into Splunk.
* **Core Tech:** Proxmox VE, pfSense, Active Directory, Splunk, WireGuard VPN.

#### 2. [Adversary Emulation & Log Hunting: Sliver C2 & Splunk](LINK_TO_REPO_2) *(In Progress)*
* **What I did:** I simulated a network compromise using a Sliver HTTP payload on a Windows 10 target. I ran common discovery techniques using Atomic Red Team and used Splunk to trace the attacker's footprint—analyzing process executions, Registry-based execution artifacts (BAM), and active network sockets.
* **Core Tech:** Sliver C2, Atomic Red Team (T1033), Windows Sysmon, Splunk SPL.

#### 3. [Malware Sandbox & Forensic Analysis Clean Room](LINK_TO_REPOR_3_OR_PLACEHOLDER) *(In Progress)*
* **What I did:** Designing an air-gapped forensic segment (OPT4) on the firewall to safely execute real malware, analyze system changes, and write detection rules.
* **Core Tech:** REMnux, Yara, Dynamic Malware Analysis.

## Technical Toolkit

### Security Monitoring & Traffic Analysis
<p align="left">
    <img src="https://img.shields.io/badge/-Splunk-000000?&style=for-the-badge&logo=Splunk&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Wireshark-1679A7?&style=for-the-badge&logo=Wireshark&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Zeek-777BB4?&style=for-the-badge&logo=zeek&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Snort-FF0000?&style=for-the-badge&logo=snort&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-MISP-000000?&style=for-the-badge&logo=misp&logoColor=white" />
    <img src="https://img.shields.io/badge/-Elastic_Stack-005571?&style=for-the-badge&logo=elasticstack&logoColor=white" />
</p>

### Endpoint, OS & Hypervisors
<p align="left">
    <img src="https://img.shields.io/badge/-Proxmox-E57000?&style=for-the-badge&logo=Proxmox&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Windows%20Server-0078D4?&style=for-the-badge&logo=Windows&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Sysmon-001A57?&style=for-the-badge&logo=Windows&logoColor=white" />
    <img src="https://img.shields.io/badge/-Linux-FCC624?&style=for-the-badge&logo=Linux&logoColor=black" />
</p>

### Networking & Infrastructure
<p align="left">
    <img src="https://img.shields.io/badge/-pfSense-DA3E25?&style=for-the-badge&logo=pfSense&logoColor=white" />
    <img src="https://img.shields.io/badge/-VMware-607078?&style=for-the-badge&logo=VMware&logoColor=white" />
    <img src="https://img.shields.io/badge/-WireGuard_VPN-88171A?style=for-the-badge&logo=wireguard&logoColor=white" />
    <img src="https://img.shields.io/badge/-Nmap-2B3E50?style=for-the-badge&logoColor=white" />
</p>

### Scripting
<p align="left">
    <img src="https://img.shields.io/badge/-Python-3776AB?&style=for-the-badge&logo=Python&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Bash-4EAA25?&style=for-the-badge&logo=GNU-Bash&logoColor=white" />
    <img src="https://img.shields.io/badge/-PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" />
</p>

## Certifications
<div>
    <img src="https://img.shields.io/badge/-Google%20Cybersecurity-4285F4?&style=for-the-badge&logo=Google&logoColor=white" />
    <img src="https://img.shields.io/badge/-Security%2B-FF0000?&style=for-the-badge&logo=CompTIA&logoColor=white" />
</div>
