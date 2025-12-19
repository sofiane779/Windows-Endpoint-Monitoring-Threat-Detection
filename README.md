# Windows Endpoint Monitoring & Threat Detection

## Executive Summary
This project demonstrates the deployment of **Sysmon** to achieve high-fidelity telemetry on a Windows 10 endpoint. By simulating common attack vectors (C2 communication and system discovery), I validated the effectiveness of custom XML filtering in capturing critical Indicators of Compromise (IoCs).

## Quick Results
* **Detection Coverage:** Process Creation (ID 1), Network Connections (ID 3).
* **Lab Setup:** Isolated VirtualBox environment (Kali Linux / Windows 10).
* **Key Finding:** Successfully traced a reverse shell simulation back to the parent PowerShell process.

## Detection Highlights
| Event Type | Artifact Captured | Evidence |
| :--- | :--- | :--- |
| **Process** | `whoami.exe` spawned by `powershell.exe` | [View Image](screenshots/ID_1.jpg) |
| **Network** | Outbound TCP/4444 to `192.168.56.10` | [View Image](screenshots/ID_3.png) |


## Repository Structure

```
├── config/
│   └── sysmonconfig-export.xml       
├── screenshots/
│   ├── network_test.png        
│   ├── ID_1.jpg                
│   └── ID_3.png                
├── analysis_report.md          
├── LICENSE                     
└── README.md                   
```
---
👉 **For a deep dive into the methodology, network troubleshooting, and full log correlation, see the [Full Analysis Report](docs/analysis_report.md).**
