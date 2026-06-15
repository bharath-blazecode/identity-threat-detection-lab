# Identity Threat Detection Lab

A home lab environment simulating identity-based cyber attacks and 
detecting them using a custom-configured Wazuh SIEM stack with 
MITRE ATT&CK-mapped detection rules.

## Project Status
🔨 In Progress — Phase 1 of 8 complete

## What This Lab Does
Simulates four real-world identity attack patterns against a 
Windows endpoint, detects them using custom Wazuh detection rules, 
and enriches alerts with VirusTotal threat intelligence via a 
Python pipeline that generates structured incident reports.

## Architecture
- **Wazuh SIEM Server** — Ubuntu Server 22.04 LTS (VM)
- **Monitored Endpoint** — Windows 11 Enterprise (VM)
- **Log Collection** — Sysmon 15.x + SwiftOnSecurity config
- **Detection** — 4 custom MITRE ATT&CK-mapped XML rules
- **Enrichment** — Python + VirusTotal API v3
- **Network** — Isolated virtual lab environment

## Tools & Technologies
| Tool | Purpose |
|------|---------|
| Wazuh 4.9.2 | SIEM — log collection, alerting, dashboards |
| Sysmon 15.x | Windows telemetry — process, network, registry |
| MITRE ATT&CK | Framework for mapping detection rules |
| Python 3 | Alert enrichment and incident report generation |
| VirusTotal API | Threat intelligence enrichment |
| VMware Workstation | Hypervisor — lab isolation |

## MITRE ATT&CK Coverage
| Technique | ID | Detection Rule | Status |
|-----------|-----|---------------|--------|
| Brute Force | T1110 | Custom XML rule | 🔨 In progress |
| Pass-the-Hash | T1550.002 | Custom XML rule | 🔨 In progress |
| Token Impersonation | T1134 | Custom XML rule | 🔨 In progress |
| Credential Dumping | T1003 | Custom XML rule | 🔨 In progress |

## Project Phases
- [x] Phase 1: Environment Setup
- [ ] Phase 2: Log Collection & Baseline
- [ ] Phase 3: Attack Simulation
- [ ] Phase 4: Custom Detection Rules
- [ ] Phase 5: Python Alert Enrichment
- [ ] Phase 6: Documentation & GitHub
- [ ] Phase 7: Demo Video & Portfolio Polish
- [ ] Phase 8: Entra ID Integration

## Responsible Use
All attack simulations are performed exclusively on owned virtual 
machines in an isolated lab environment. No external systems are 
tested or targeted.

## Author
Barry Sampath | QUT Bachelor of IT (Cybersecurity & AI)
[LinkedIn](https://linkedin.com/in/barrysampath) | 
[GitHub](https://github.com/bharath-blazecode)
