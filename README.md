# Hello, I'm Anton 👋

I am a cybersecurity professional transitioning from a career in education. I love building secure infrastructure, analyzing network traffic, and analyzing logs to solve complex security puzzles.

Below is the layout of my home lab, which I engineered on a bare-metal hypervisor to safely run attacks, study malware, and learn defensive monitoring.

<img width="782" height="763" alt="Screenshot 2026-07-06 at 21 13 20" src="https://github.com/user-attachments/assets/c8d68bf6-2eeb-4d28-b810-e6231c506adf" />

**Note:** This diagram shows the complete 6-zone enterprise network I am building. I use virtual switches in Proxmox to keep my lab traffic entirely isolated from my home network.

## Featured Projects

#### [Project 1: Building a Secure Home Cyber Lab (pfSense, Active Directory & Splunk)](https://github.com/antonvikstrom/building-secure-home-lab)
* **What I did:** Built an isolated 6-zone enterprise lab on Proxmox, routed and secured by a pfSense firewall with WireGuard VPN access. Deployed Active Directory, vulnerable endpoints, and an isolated REMnux clean room, then configured Sysmon and Splunk to stream central telemetry.

* **Core Tech:** Proxmox VE, pfSense, Active Directory, Splunk, Sysmon, Docker, WireGuard.

#### [Project 2: Automated Adversary Emulation & SIEM Detections](https://github.com/antonvikstrom/automated-threat-detection-pipeline)
* **What I did:** Built a closed-loop Python automation pipeline on Kali Linux to simulate web (LFI/Path Traversal) and network (Covert DNS Exfiltration) attacks. Programmatically audited SIEM detections via Splunk's REST API, integrated real-time threat intelligence enrichment via AbuseIPDB, and authored custom SPL correlation rules using regex field extraction.

* **Core Tech:** Python (requests, python-dotenv), Splunk (SPL & REST API), Kali Linux, pfSense, Docker, AbuseIPDB API. 

#### [Project 3: Live Linux Malware Analysis & SIEM Telemetry Engineering](https://github.com/antonvikstrom/dfir-malware-analysis-lab)
* **What I did:** Detonated a 194-byte 64-bit Linux ELF stager inside an air-gapped REMnux clean room. Extracted hardcoded C2 socket structures via dynamic tracing (strace) and disassembly (Cutter), authored a custom YARA signature, and remediated a critical pfSense syslog telemetry gap (clog buffer freeze & silent drops) to restore full visibility in Splunk.

* **Core Tech:** REMnux, Cutter, strace, YARA, tcpdump, pfSense, Splunk (SPL & CSV Parsing).

#### [Project 4: Autonomous SOAR Engine with AI Triage & Human-in-the-Loop Response](https://github.com/antonvikstrom/soar-automation-pipeline)

* **What I did:** Built a closed-loop security orchestration pipeline linking Splunk webhook alerts to an n8n
automation engine. Python sandboxed risk scoring filters benign events before they reach Claude for AI triage
(MITRE ATT&CK mapping, severity classification, remediation steps). High-severity threats route through a
Discord approval gate with interactive Approve/Decline buttons, and on human approval, the pipeline
automatically patches a pfSense firewall alias via its REST API to block the attacker IP in real time. All
five decision outcomes (benign suppression, already-blocked skip, human denial, automated block, and low-severity
pass) are written back to Splunk via HTTP Event Collector, closing the audit loop so every SOAR decision
lives alongside its original detection event in the SIEM.

* **Core Tech:** Splunk (SPL, HEC), n8n, Docker, Python, Anthropic Claude API, Discord Bot API, pfSense REST API
(pfrest), MITRE ATT&CK.

#### [Project 5: Detection-as-Code Pipeline with CI-Tested Sigma, YARA & SPL Rules](https://github.com/antonvikstrom/detection-as-code)

* **What I did:** Consolidated detections from the four projects above into a version-controlled detection-as-code repository. GitHub Actions validates every rule's syntax and schema, compiles the YARA rules, and runs the actual detection logic against labeled test fixtures, not just checking that a rule parses, but that it fires on what it should and stays quiet on what it shouldn't. Replaced a hardcoded lab-only IOC with a live threat-intel watchlist pulled daily from abuse.ch, and added a behavioral DNS exfiltration rule (entropy and length scoring) alongside the IOC match to cover domains that haven't been reported anywhere yet.

* **Core Tech:** Sigma, pySigma, YARA, Splunk SPL, Python, GitHub Actions, abuse.ch URLhaus, MITRE ATT&CK.

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
    <img src="https://img.shields.io/badge/-VMware-607078?&style=for-the-badge&logo=VMware&logoColor=white" />
    <img src="https://img.shields.io/badge/-WireGuard_VPN-88171A?style=for-the-badge&logo=wireguard&logoColor=white" />
</p>

### Scripting & Automation
<p align="left">
    <img src="https://img.shields.io/badge/-Python-3776AB?&style=for-the-badge&logo=Python&logoColor=white" /> 
    <img src="https://img.shields.io/badge/-Bash-4EAA25?&style=for-the-badge&logo=GNU-Bash&logoColor=white" />
    <img src="https://img.shields.io/badge/-PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" />
    <img src="https://img.shields.io/badge/-GitHub_Actions-2088FF?&style=for-the-badge&logo=githubactions&logoColor=white" />
    <img src="https://img.shields.io/badge/-n8n-EA4B71?&style=for-the-badge&logo=n8n&logoColor=white" />
</p>

## Certifications
<div>
    <img src="https://img.shields.io/badge/-Google%20Cybersecurity-4285F4?&style=for-the-badge&logo=Google&logoColor=white" />
    <img src="https://img.shields.io/badge/-Security%2B-FF0000?&style=for-the-badge&logo=CompTIA&logoColor=white" />
</div>
