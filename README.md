# Splunk SOC Home Lab

A home SIEM lab that collects Windows and Sysmon logs in Splunk Enterprise and detects brute force and suspicious PowerShell activity.

## Lab setup
- Splunk Enterprise 10.x on Ubuntu Server 24.04 (VirtualBox VM)
- Windows 10 host with Sysmon and Splunk Universal Forwarder
- Logs collected: Security, System, Application, Sysmon

## Detections
1. **Brute force (T1110):** 5+ failed logins (Event ID 4625) per account.
2. **Suspicious PowerShell (T1059.001):** hidden-window PowerShell found via Sysmon Event ID 1.
3. **Rare processes:** low-frequency programs for threat hunting.

## Tuning
Excluded the Splunk forwarder's own PowerShell helper to cut false positives.

## Results
- Simulated failed logins with a fake account; the alert flagged it.
- Built a 3-panel SOC dashboard.

## Screenshots
See the screenshots folder.

## Skills shown
SPL, log analysis, Sysmon, alert creation, dashboards, detection tuning, MITRE ATT&CK mapping.

![Dashboard] (SOC%20LAB.png)

![Alert](SOC%20LAB%2ALERT.png)
