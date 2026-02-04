# Threat Hunting: Living-off-the-Land Attacks on Windows

This project demonstrates a SOC lab using **Wazuh** and **Sysmon** to detect:

- T1059 – PowerShell execution
- T1047 – WMI remote execution
- T1053 – Scheduled Task persistence

## Lab Setup

- Windows 10 victim VM (Wazuh agent + Sysmon)
- Windows Server Domain Controller
- Kali Linux attacker VM
- Wazuh Manager on Ubuntu

## Screenshots

All attacks are documented with Sysmon events and Wazuh alerts in the `/screenshots` folder.

## Commands

PowerShell and Evil-WinRM commands used are in the `/commands` folder.

## Report

Final SOC report is available in `/report/README.md`.

---

## Notes

- This lab is safe and simulated.  
- For educational purposes only.
