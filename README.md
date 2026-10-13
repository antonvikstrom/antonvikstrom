# Hello, I'm Anton 👋

I build and defend a home lab where I run attacks, write detections, and automate the response. I like turning logs and network traffic into answers.

Below is the layout of my home lab, built on Proxmox to safely run attacks, study malware, and practice defensive monitoring.

<img width="782" height="763" alt="Screenshot 2026-07-06 at 21 13 20" src="https://github.com/user-attachments/assets/c8d68bf6-2eeb-4d28-b810-e6231c506adf" />

*A 5-zone network behind pfSense, with lab traffic kept separate from my home network.*

## Featured Projects

#### [Detection-as-Code Pipeline with CI-Tested Sigma, YARA & SPL Rules](https://github.com/antonvikstrom/detection-as-code)
Detections from my other projects in one version-controlled repo. GitHub Actions checks every rule and runs it against test data, so a rule has to fire on what it should and stay quiet on what it shouldn't. Includes a live abuse.ch watchlist and a behavioral DNS exfiltration rule.

**Tech:** Sigma, pySigma, YARA, Splunk SPL, Python, GitHub Actions, MITRE ATT&CK

#### [AI-Assisted SOAR Engine with Human Approval](https://github.com/antonvikstrom/soar-automation-pipeline)
Splunk alerts go to n8n, where a sandboxed Python step filters out benign events before Claude triages the rest. High-severity alerts wait for approval in Discord, and only then does the pipeline block the IP in pfSense. Every decision is written back to Splunk as an audit trail.

**Tech:** Splunk (SPL, HEC), n8n, Docker, Python, Claude API, Discord API, pfSense REST API

#### [Building a Secure Home Cyber Lab (pfSense, Active Directory & Splunk)](https://github.com/antonvikstrom/building-secure-home-lab)
A 5-zone lab on Proxmox behind pfSense, with WireGuard for remote access. Active Directory, vulnerable endpoints and an isolated REMnux clean room, with Sysmon and Splunk collecting the telemetry.

**Tech:** Proxmox VE, pfSense, Active Directory, Splunk, Sysmon, Docker, WireGuard

#### [Ansible: Splunk Forwarder Automation](https://github.com/antonvikstrom/ansible-splunk-forwarder)
Ansible playbooks that take a Linux machine from a clean snapshot to sending logs to Splunk, with secrets in Ansible Vault and ansible-lint in CI. A second run changes nothing.

**Tech:** Ansible, Ansible Vault, Splunk Universal Forwarder, GitHub Actions, Linux

#### [Live Linux Malware Analysis & SIEM Telemetry Engineering](https://github.com/antonvikstrom/dfir-malware-analysis-lab)
Detonated a small Linux ELF stager in an isolated REMnux clean room, pulled out its C2 address with strace and Cutter, and wrote a YARA rule for it. Also fixed a pfSense syslog problem that was silently dropping logs before they reached Splunk.

**Tech:** REMnux, Cutter, strace, YARA, tcpdump, pfSense, Splunk

#### [Automated Adversary Emulation & SIEM Detections](https://github.com/antonvikstrom/automated-threat-detection-pipeline)
Python scripts on Kali that simulate LFI and DNS exfiltration attacks, then check through Splunk's REST API that the detections fired. Includes AbuseIPDB enrichment and SPL rules with regex field extraction.

**Tech:** Python, Splunk (SPL, REST API), Kali Linux, pfSense, Docker, AbuseIPDB API

## Technical Toolkit

### Security Monitoring & Traffic Analysis
<p align="left">
    <img src="https://img.shields.io/badge/-Splunk-000000?&style=for-the-badge&logo=Splunk&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Wireshark-1679A7?&style=for-the-badge&logo=Wireshark&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Sigma-4B0082?&style=for-the-badge" />
    <img src="https://img.shields.io/badge/-YARA-4B0082?&style=for-the-badge" />
</p>

### Endpoint, OS & Hypervisors
<p align="left">
    <img src="https://img.shields.io/badge/-Proxmox-E57000?&style=for-the-badge&logo=Proxmox&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Docker-2496ED?&style=for-the-badge&logo=Docker&logoColor=white" />
    <img src="https://img.shields.io/badge/-Windows%20Server-0078D4?&style=for-the-badge&logo=Windows&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Sysmon-001A57?&style=for-the-badge&logo=Windows&logoColor=white" />
    <img src="https://img.shields.io/badge/-Linux-FCC624?&style=for-the-badge&logo=Linux&logoColor=black" />
    <img src="https://img.shields.io/badge/-Kali_Linux-557C94?&style=for-the-badge&logo=kalilinux&logoColor=white" />
</p>

### Networking & Infrastructure
<p align="left">
    <img src="https://img.shields.io/badge/-pfSense-DA3E25?&style=for-the-badge&logo=pfSense&logoColor=white" />
    <img src="https://img.shields.io/badge/-WireGuard_VPN-88171A?style=for-the-badge&logo=wireguard&logoColor=white" />
</p>

### Scripting & Automation
<p align="left">
    <img src="https://img.shields.io/badge/-Python-3776AB?&style=for-the-badge&logo=Python&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Bash-4EAA25?&style=for-the-badge&logo=GNU-Bash&logoColor=white" />
    <img src="https://img.shields.io/badge/-PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" />
    <img src="https://img.shields.io/badge/-GitHub_Actions-2088FF?&style=for-the-badge&logo=githubactions&logoColor=white" />
    <img src="https://img.shields.io/badge/-n8n-EA4B71?&style=for-the-badge&logo=n8n&logoColor=white" />
    <img src="https://img.shields.io/badge/-Ansible-EE0000?&style=for-the-badge&logo=ansible&logoColor=white" />
</p>

## Certifications
<div>
    <img src="https://img.shields.io/badge/-Google%20Cybersecurity-4285F4?&style=for-the-badge&logo=Google&logoColor=white" />
    <img src="https://img.shields.io/badge/-Security%2B-FF0000?&style=for-the-badge&logo=CompTIA&logoColor=white" />
</div>
