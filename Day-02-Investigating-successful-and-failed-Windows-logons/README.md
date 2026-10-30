# Week 11, Day 2 — Successful vs. Failed Windows Logon Investigation

## Objective
Compare successful and failed Windows authentication events using Wazuh.

## Environment
- Wazuh Manager: wazuh-server
- Windows Endpoint: WinServ22
- Agent ID: 003

## Successful Login Findings
- Windows Event ID: 4624
- Wazuh Rule ID: 60106
- Rule Description: Windows Logon Success
- Target Username: WINSERV22$
- Target Domain: HOMELAB.LOCAL
- Logon Type: 3 (Network)

## Failed Login Findings
- Windows Event ID: 4625
- Wazuh Rule ID: 60122
- Rule Description: Logon Failure - Unknown user or bad password
- Target Username: Administrator
- Target Domain: Homelab

## Analysis
I investigated successful and failed Windows authentication events in Wazuh Threat Hunting.

The successful event involved the computer account WINSERV22$ and used logon type 3, which represents a network logon.

The failed event involved the Homelab Administrator account and was detected by Wazuh rule 60122.

This exercise demonstrated how Wazuh identifies different authentication outcomes and provides information about the accounts involved.

## Lessons Learned
- Event ID 4624 represents a successful logon.
- Event ID 4625 represents a failed logon.
- Active Directory computer accounts commonly end with a dollar sign.
- Logon type 3 represents network authentication.
- Successful authentication still requires context when investigating security activity.

## Conclusion
I successfully investigated and compared Windows authentication events using Wazuh. I identified the accounts, event IDs, logon type, and detection rules associated with each event.

