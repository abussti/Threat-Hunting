# Threat Hunting: Living-off-the-Land Attacks on Windows

A hands-on **SOC threat-hunting lab** demonstrating the detection and investigation of Windows living-off-the-land (LotL) activity using **Wazuh, Sysmon, and MITRE ATT&CK**.

The lab simulates attacker activity and follows the workflow of a SOC analyst: **generate activity → collect telemetry → detect → investigate → map to ATT&CK → document findings**.

## Attack Techniques

| Technique | Activity                                 | Detection Focus                                   |
| --------- | ---------------------------------------- | ------------------------------------------------- |
| **T1059** | PowerShell                               | Suspicious command execution and process activity |
| **T1047** | Windows Management Instrumentation (WMI) | Remote execution and process creation             |
| **T1053** | Scheduled Task/Job                       | Persistence through scheduled tasks               |

## Lab Architecture

* **Windows 10 Victim** — Wazuh Agent + Sysmon
* **Windows Server** — Domain Controller
* **Kali Linux** — Attacker VM
* **Ubuntu** — Wazuh Manager

Telemetry generated on the Windows endpoint is collected through **Sysmon and the Wazuh Agent**, allowing the attacks to be investigated through Wazuh alerts and event data.

## Investigation Workflow

1. Simulate attacker activity from the Kali Linux environment
2. Capture process and system activity using Sysmon
3. Forward endpoint telemetry to Wazuh
4. Investigate generated security alerts
5. Identify indicators and relevant execution techniques
6. Map observed behavior to **MITRE ATT&CK**
7. Document findings and recommended defensive actions

## Evidence

All attack simulations and corresponding detections are documented in the [`/screenshots`](./screenshots) directory, including Sysmon events and Wazuh alerts.

Attack commands used during the lab are available in [`/commands`](./commands).

## Report

The complete investigation and findings are available in:

[`/report/Threat Hunting_ Living-off-the-Land Attacks on Windows.pdf`](./report/Threat%20Hunting_%20Living%E2%80%91off%E2%80%91Land%20Attacks%20on%20Windows.pdf)

## Skills Demonstrated

* Threat hunting and SOC investigation
* Windows endpoint telemetry analysis
* Sysmon event analysis
* Wazuh SIEM/EDR-style monitoring
* MITRE ATT&CK mapping
* Living-off-the-land technique detection
* Process and command-line analysis
* Attack timeline reconstruction
* Security reporting and documentation

## Notes

This project was conducted in an **isolated lab environment** using simulated attack activity.

For educational and defensive security research purposes only.
