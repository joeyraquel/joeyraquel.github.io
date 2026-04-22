# 🔐 Pentest Lab Trainer — USB Edition

![Offline](https://img.shields.io/badge/Mode-Offline-green)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20Mac-blue)
![Python](https://img.shields.io/badge/Python-3.x-yellow)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

## 🚀 Overview

A **portable, offline penetration testing training platform** that runs directly from a USB drive.

> Real commands. Real methodology. Real lab.

Built as a **local web app + Proxmox lab**, this tool walks you through actual offensive security workflows — not theory.# 🔐 Pentest Lab Trainer — USB Edition

![Offline](https://img.shields.io/badge/Mode-Offline-green)
![Platform](https://img.shields.io/badge/Platform-Windows%7CLinux%7CMac-blue)
![Python](https://img.shields.io/badge/Python-3.x-yellow)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

## 🚀 Overview

A **portable, offline penetration testing training platform** that runs directly from a USB drive.

> Real commands. Real methodology. Real lab.

Built as a **local web app + Proxmox lab**, this tool walks you through actual offensive security workflows — not theory.

## ⚡ Quick Start

```bash
# Windows
START.bat

# Linux / Mac
bash start.sh
```

Then open:

```
http://localhost:8080
```

## 🧠 What Makes This Different

* Not a course
* Not slides
* Not theory

👉 This is a **live operational training system**

You:

* Run real commands in Kali
* Validate real results
* Move forward only when it works

## 🧩 Features

* ✅ Full 8-phase pentest lifecycle
* ✅ Real tools (Nmap, Metasploit, etc.)
* ✅ Step-by-step missions
* ✅ Branching logic based on results
* ✅ Fully offline (no accounts, no cloud)
* ✅ USB-based progress tracking
* ✅ Resume anywhere on any machine

## 🧠 Pentest Methodology

| Phase | Focus             | Tools              |
| ----- | ----------------- | ------------------ |
| 01    | Recon             | Nmap, theHarvester |
| 02    | Enumeration       | Gobuster, WPScan   |
| 03    | Exploitation      | Metasploit, Hydra  |
| 04    | Post-Exploitation | LinPEAS, WinPEAS   |
| 05    | Cover Tracks      | auditd, Wazuh      |
| 06    | Reporting         | CVSS               |
| 07    | C2                | Sliver, MSF        |
| 08    | WiFi              | aircrack-ng        |

## 🧪 Lab Architecture (Proxmox)

```
Attacker (Kali)
     ↓
Targets:
- Metasploitable
- DVWA
- WordPress Vuln
- WebGoat / Juice Shop
- Windows / AD
- SIEM (Wazuh)
- ICS (ScadaBR / OpenPLC)
```

## 🖥️ Home Lab Targets

| System          | IP             | Role     |
| --------------- | -------------- | -------- |
| Kali            | 192.168.1.200  | Attacker |
| Metasploitable2 | 192.168.1.150  | Target   |
| DVWA            | 192.168.1.140  | Web      |
| WP Vuln         | 192.168.1.135  | CMS      |
| Windows 11      | 192.168.1.125  | Endpoint |
| Win Server 2022 | 192.168.1.181  | AD       |
| Wazuh           | 192.168.1.210  | SIEM     |
| REMnux          | 192.168.1.190  | Malware  |
| ICS Lab         | 192.168.1.245+ | SCADA    |

## 📂 Project Structure

```
PentestLab/
├── START.bat
├── start.sh
├── server.py
├── index.html
├── progress.json
└── README.txt
```

## 💾 Persistence System

* Progress saved to:

```
progress.json (USB)
```

* Backup:

```
browser localStorage
```

👉 Your training moves with you.

## 🎯 Example Mission

```
ping -c 4 192.168.1.135
```

**Goal:** Verify target is alive

| Result  | Meaning       |
| ------- | ------------- |
| Replies | Target up     |
| Timeout | VM down       |
| Error   | Network issue |

## 🎓 Certification Alignment

| Cert      | Coverage        |
| --------- | --------------- |
| eJPT      | Recon → Exploit |
| Security+ | Fundamentals    |
| OSCP      | Full lifecycle  |
| GICSP     | ICS focus       |

## 🛣️ Roadmap

* [ ] WordPress exploitation missions
* [ ] OWASP Top 10 (WebGoat + Juice Shop)
* [ ] Active Directory attack paths
* [ ] ICS/SCADA scenarios
* [ ] VPS remote lab access
* [ ] Auto-report generator

## 👤 Author

**Joey Raquel**
Telecom → Cybersecurity Transition

* Satellite / RF / ISP / Cisco
* 17+ years infrastructure experience
* Building offensive security skillset

## ⚖️ Legal

This project is for:

✔ Personal lab environments
✔ Authorized testing only

🚫 Do NOT use on unauthorized systems.

## ⭐ Why This Project Matters

Most people:

* Watch courses
* Take notes
* Forget everything

This forces you to:

* Execute
* Validate
* Think like an attacker


## ⚡ Quick Start

```bash
# Windows
START.bat

# Linux / Mac
bash start.sh
