# Week 11, Day 1 — Wazuh Failed Login Investigation

## Objective
Investigate a Windows failed-login security event using Wazuh Threat Hunting and inspect the alert's JSON document details.

## Lab Environment
- Wazuh Manager: wazuh-server
- Windows Endpoint: WinServ22
- Agent ID: 003
- Endpoint IP: 192.168.114.12

## Alert Findings
- Windows Event ID: 4625
- Wazuh Rule ID: 60122
- Rule Description: Logon Failure - Unknown user or bad password
- Target Username: Administrator
- Target Domain: Homelab

## Investigation
I searched Wazuh Threat Hunting for rule 60122 and opened the alert using the Inspect Document Details option.

I located the JSON document details and identified the target username and domain. The failed-login event involved the Homelab Administrator account on the WinServ22 endpoint.

## Skills Practiced
- Searching Wazuh security alerts
- Investigating Windows Event ID 4625
- Inspecting alert JSON documents
- Identifying targeted user accounts
- Connecting Windows security events to Wazuh detection rules

## Conclusion
Wazuh successfully detected the failed-login event and provided useful information about the targeted account. This investigation demonstrated how to examine security alerts and collect evidence for a basic SOC investigation.

