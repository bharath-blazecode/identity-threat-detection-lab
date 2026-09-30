# Identity Threat Detection Lab

A personal lab for learning how Windows endpoint activity reaches a Wazuh SIEM. I built the virtual environment, enrolled the endpoint and confirmed that its telemetry appeared in the dashboard. Identity-attack simulation and custom detection are the intended next steps.

## Project Status

**Endpoint telemetry collection complete. Development paused.**

Started in June 2026; paused while I focus on university and paid work. There is no scheduled restart date. The completed milestone is a working collection path, not validated attack detection or a continuously operated monitoring service.

## Completed: Environment and Telemetry Collection

- **Wazuh 4.9.2** — all-in-one indexer, server and dashboard on an Ubuntu Server 22.04 LTS VM.
- **Windows 11 Enterprise** — monitored VM with the Wazuh agent enrolled.
- **Sysmon 15.20** — installed with the SwiftOnSecurity configuration; Windows endpoint telemetry reached the Wazuh indexer and appeared in the dashboard.
- **VMware Workstation** — both VMs ran on a single Lenovo ThinkPad. The working milestone used bridged networking on the local network; this was not an isolated attack range.

Getting that path working involved resolving VM file locks, a stale network configuration and an indexer disk-capacity problem. SSH access failed during a NAT attempt; returning to bridged networking restored the working setup. NAT restoration remains unfinished.

The [portfolio case study](https://bharath-blazecode.github.io/work/homelab/) explains those decisions and shows dashboard context. This repository currently contains this README only: runnable lab configuration, collected logs, custom rules, test results and an enrichment pipeline are not published here. The dashboard image does not establish attack-detection accuracy or incident-response performance.

## Illustrative: Detection Walkthrough

The portfolio includes an [illustrative Word-to-PowerShell walkthrough](https://bharath-blazecode.github.io/work/homelab/#example), using a Sysmon process-creation event to explain what an analyst might investigate. Its example rule ID, severity and MITRE ATT&CK mapping are teaching material, not an implemented custom rule, a recorded incident or the result of a simulation run.

## Planned: Simulations, Rules and Enrichment

The following remain planned, not built or validated in this lab:

- **Controlled attack simulations** and incident-response exercises, with test events that can be checked against expected results.
- **Custom Wazuh XML detection rules**, mapped to MITRE ATT&CK and tested against those events.
- **Python 3 and VirusTotal API v3 enrichment**, with structured incident reports.
- **Further baseline analysis**, reproducible configuration, test evidence and fuller documentation.
- **Demo video, further portfolio documentation and Entra ID integration.**

The original detection roadmap listed these targets. They are planned investigation topics, not demonstrated coverage or rules currently in progress:

- Brute Force — **T1110**
- Pass-the-Hash — **T1550.002**
- Access Token Manipulation (including impersonation) — **T1134**
- OS Credential Dumping — **T1003**

## How the Milestones Fit Together

The portfolio calls the completed environment **and endpoint telemetry collection** its **Phase 1** milestone. Its **Phase 2** describes future detection-rule development and incident-response work.

An earlier eight-part roadmap in this README used different boundaries: Phase 1 was environment setup, Phase 2 was log collection and baseline, Phases 3–5 were simulations, rules and enrichment, and Phases 6–8 were documentation, demo/portfolio work and Entra ID integration.

These numbers do not describe equivalent milestones. Environment setup and telemetry collection are complete; broader baseline analysis is not claimed complete. The public README and portfolio case study exist, but the wider documentation and demo work is still planned. The named completion, illustration and planned-work sections above are the current status; the old numbering is context, not a claim that all of an old phase is finished.

## Responsible Use

This is a personal learning environment using my own VMs. No external systems are tested or targeted. Before any future attack simulation, network isolation and safe test conditions need to be established and verified; the completed bridged setup is not evidence of that isolation.

## Author

Barry Sampath | QUT Bachelor of IT (Cybersecurity & AI)

[LinkedIn](https://linkedin.com/in/barrysampath) | [GitHub](https://github.com/bharath-blazecode)
