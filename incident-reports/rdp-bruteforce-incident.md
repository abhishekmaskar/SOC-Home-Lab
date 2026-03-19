#  Incident Report — RDP Brute Force Attempt

##  Date & Time

19 March 2026
Approx 17:20 – 17:35 IST

##  Affected System

Windows Endpoint
Hostname: DESKTOP-PS0HTLT
IP Address: 192.168.44.130

##  Attacker Details

Source IP Address: 192.168.44.129
Source Machine: Kali Linux Attacker VM

##  Detection Source

Splunk SIEM monitoring Windows Security Logs (EventCode 4625)

##  Incident Description

Multiple failed Remote Desktop login attempts were detected targeting the Administrator account.
The login attempts originated from a Kali Linux attacker machine within the SOC home lab environment.

##  Evidence Observed

* Numerous Windows Security Log events with **EventCode 4625 (Failed Logon)**
* Logon Type observed: Remote Interactive (RDP)
* Source Network Address identified as 192.168.44.129
* Windows account lockout triggered after repeated failed attempts

##  MITRE ATT&CK Mapping

Technique: **T1110 — Brute Force**

##  Potential Impact

If successful, attacker could gain unauthorized remote access to the Windows endpoint.

##  Response / Mitigation

* Account lockout policy prevented further login attempts
* Recommended actions:

  * Block attacker IP at firewall
  * Enforce strong password policy
  * Enable multi-factor authentication
  * Monitor for repeated authentication failures

##  Conclusion

The SOC monitoring setup successfully detected and logged brute force authentication attempts.
This validates the effectiveness of centralized log collection using Splunk and endpoint telemetry via Sysmon.
