# SOC Home Lab & Security Monitoring Environment

##  Project Overview

This project demonstrates the setup of a personal Security Operations Center (SOC) lab using Splunk SIEM, Sysmon endpoint logging, and Kali Linux attack simulation.

The lab simulates real-world cyber attacks such as brute-force authentication attempts and analyzes security logs for detection and investigation.

##  Lab Architecture

* Splunk SIEM Server (Kali Linux)
* Windows Endpoint with Sysmon
* Kali Linux Attacker Machine

Logs from Windows are forwarded to Splunk using Splunk Universal Forwarder for centralized monitoring.

##  Tools & Technologies Used

* Splunk Enterprise
* Sysmon (Microsoft Sysinternals)
* Kali Linux
* Hydra / xfreerdp / Nmap
* Windows Security Event Logs

##  Attack Simulations Performed

* RDP Brute Force Attack Simulation
* Account Lockout Scenario
* Authentication Failure Monitoring

##  Detection Use Cases

* Detection of multiple failed login attempts (EventCode 4625)
* Source IP correlation of attacker machine
* Timeline-based incident investigation

##  Key Learning Outcomes

* SIEM deployment and log ingestion
* Endpoint telemetry analysis
* Security alert triage workflow
* MITRE ATT&CK mapping
* Incident documentation
