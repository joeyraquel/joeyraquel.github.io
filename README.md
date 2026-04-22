🔐 Pentest Lab Trainer — USB Edition

A portable, offline penetration testing training program that runs off a USB drive.
Real commands. Real methodology. Your own Proxmox home lab.


What This Is
A self-contained pentest training program built as a local web app. Plug the USB into any PC, double-click START.bat, and your browser opens a fully guided lab environment — step-by-step missions with real executable commands, branching result confirmation, and progress that saves to the USB itself.
This is not a course. It's an operations guide you run live.

Features

✅ 8-phase pentest methodology — full offensive lifecycle
✅ Real commands — not pseudocode. Copy → paste → run in Kali
✅ Guided missions — do this → here's why → what did you see? → continue
✅ Branching responses — different guidance based on your actual result
✅ Progress saves to USB — plug into any PC, pick up exactly where you left off
✅ Fully offline — no internet required, no account, no subscription
✅ localhost fallback — also saves to browser localStorage as backup


The 8 Phases
#PhaseKey Tools01ReconnaissanceNmap, theHarvester, dig, crt.sh02Scanning & Enumerationenum4linux, Gobuster, WPScan, Nikto03Gaining AccessMetasploit, msfvenom, Hydra, Netcat04Post ExploitationLinPEAS, WinPEAS, GTFOBins, Hashcat05Covering Tracksauditd, Wazuh SIEM review06ReportingCVSS 3.1 scoring, professional finding format07C2 / Command & ControlSliver C2, MSF multi/handler, pivoting08WiFi Hackingaircrack-ng, hashcat, hcxdumptool, Reaver

Home Lab Targets (Proxmox)
VMNameIPPurposeVM200Kali Linux192.168.1.200AttackerVM150Metasploitable2192.168.1.150Primary targetVM140DVWA-Ubuntu192.168.1.140Web app attacksVM135Wp-Vuln192.168.1.135WordPress exploitationVM141Webgoat192.168.1.141OWASP web vulnerabilitiesVM142Juiceshop192.168.1.142Modern web app attacksVM143Badstore192.168.1.143E-commerce vulnerabilitiesVM145Api-Vuln192.168.1.145API security testingVM156Metasploitable3192.168.1.156Windows exploitationVM125Windows 11192.168.1.125Windows attacksVM181Winserver 2022192.168.1.181Active DirectoryVM190REMnux192.168.1.190Malware analysisVM191Flare-VM192.168.1.191Reverse engineeringVM210Wazuh-Rocky192.168.1.210SIEM / detectionVM211Bloodhound192.168.1.211AD attack pathsVM245Scadabr192.168.1.245ICS/SCADA attacksVM246OpenPLC192.168.1.246PLC exploitation

How to Use
Requirements

Python 3 (free — python.org)
Any modern browser (Chrome, Firefox, Edge)

Run It
Windows:
Double-click START.bat
Mac / Linux:
bashbash start.sh
Browser opens automatically to http://localhost:8080.
Progress saves to progress.json on the USB drive.

File Structure
PentestLab/
├── START.bat          ← Windows launcher (double-click)
├── start.sh           ← Mac/Linux launcher
├── server.py          ← Python web server (handles progress save/load)
├── index.html         ← Full training program app
├── progress.json      ← Your saved progress (travels with USB)
└── README.txt         ← Quick start instructions

How Progress Saving Works

App loads → tries to fetch /progress from local Python server
Server reads progress.json from USB directory
On every checkpoint → POST to /progress → server writes to USB
Fallback: always mirrors to browser localStorage as backup

This means your progress follows the USB — not the browser, not the PC.

Sample Mission — Phase 01, Mission 01, Step 02
TITLE:    Ping VM135 — Wp-Vuln
RUN ON:   VM200 Kali Linux (192.168.1.200)
TARGET:   VM135 Wp-Vuln (192.168.1.135)

COMMAND:
  ping -c 4 192.168.1.135

WHY THIS WORKS:
  ping uses ICMP echo requests. A reply = host is up and your
  network path to it works. -c 4 sends exactly 4 packets then stops.

WHAT DID YOU SEE?
  ○ Got replies — 0% packet loss    → VM135 is live, continue
  ○ Request timeout / 100% loss     → Start VM135 in Proxmox, retry
  ○ Network error / unknown host    → Check Kali IP with 'ip a'

Certification Path
This program maps directly to:
CertCoverageeJPTPhases 01–03CompTIA Security+Phases 01, 02, 06OSCPAll phases — especially 03, 04, 07GICSPPhase 08 ICS/SCADA targets

About the Author
Joey Raquel — Telecom infrastructure professional with 17+ years across satellite RF, microwave, GPON/FTTH, HFC/DOCSIS, nuclear facility, and enterprise Cisco environments. Transitioning into offensive cybersecurity targeting penetration testing and security analyst roles at defense and government contracting firms.

🔗 LinkedIn
🌐 Portfolio
📍 Honolulu, HI


Legal Notice
This tool is built for use against systems you own or have explicit written authorization to test. All lab targets are intentionally vulnerable VMs running in a private Proxmox home lab. Never use these techniques against systems you don't own or have permission to test.

Roadmap

 WordPress attack + defense missions
 Webgoat full OWASP Top 10 mission set
 Juiceshop modern web app mission set
 Bloodhound / Active Directory attack path missions
 ICS/SCADA Scadabr + OpenPLC exploitation missions
 VPS deployment with WireGuard-only access + login screen
 Automated report generator from completed missions
