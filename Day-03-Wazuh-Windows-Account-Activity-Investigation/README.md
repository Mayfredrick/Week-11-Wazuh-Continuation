# Week 11, Day 3 — Windows Account Logoff Investigation

## Objective
Investigate Windows account logoff activity using Wazuh Threat Hunting.

## Lab Environment
- Wazuh Manager: wazuh-server
- Windows Endpoint: WinServ22
- Agent ID: 003

## Event Findings
- Windows Event ID: 4634
- Wazuh Rule ID: 60137
- Rule Description: Windows User Logoff
- Target Username: WINSERV22$
- Target Domain: HOMELAB
- Logon Type: 3 (Network)

## Investigation
I searched Wazuh Threat Hunting for Windows Event ID 4634 and inspected the alert details.

The event involved the computer account WINSERV22$ in the HOMELAB domain. The logon type was 3, indicating a network logon session.

Wazuh identified the event using rule 60137, Windows User Logoff.

## Lessons Learned
- Event ID 4634 indicates that a logon session ended.
- Logon type 3 represents a network logon.
- Windows computer accounts commonly end with a dollar sign.
- A normal logoff is not automatically suspicious.
- Wazuh provides useful information for investigating Windows account activity.

## Conclusion
I successfully located and investigated a Windows logoff event using Wazuh. This exercise helped me understand how to monitor account activity and distinguish between successful authentication, failed authentication, and session termination.

