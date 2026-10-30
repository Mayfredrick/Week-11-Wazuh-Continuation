# Week 11, Day 4 — Windows Account Management Investigation

## Objective
Investigate Windows account-management activity using Wazuh.

## Lab Environment
- Wazuh Manager: wazuh-server
- Windows Endpoint: WinServ22
- Agent ID: 003

## Event Findings
- Windows Event ID: 4722
- Wazuh Rule ID: 60109
- Rule Description: User account enabled or created
- Subject Username: Adminstrator
- Subject Domain: HOMELAB
- Target Username: ADIT10$
- Target Domain: HOMELAB

## Investigation
I searched Wazuh Threat Hunting for Windows account-management activity and inspected the JSON details of Event ID 4722.

The event showed that the account HOMELAB\ADIT10$ was enabled by an account recorded as HOMELAB\Adminstrator.

The target account ends with a dollar sign, which is consistent with an Active Directory computer account.

I also searched for Windows Event ID 4725, which records account disablement. No matching event was found in the available search results.

## Security Analysis
Event ID 4722 specifically records that a user account was enabled. The event does not establish that the account was newly created.

The absence of a matching Event ID 4725 means the related disablement activity could not be established from the available records.

## Lessons Learned
- Event ID 4722 records account enablement.
- Event ID 4725 records account disablement.
- Subject fields identify the account performing the action.
- Target fields identify the account affected.
- Computer accounts in Active Directory commonly end with a dollar sign.
- Account-management events should be reviewed for unexpected changes.

## Conclusion
I successfully investigated a Windows account-management event using Wazuh. I identified the account performing the action, the affected account, and the associated detection rule. I also checked for a related account-disablement event but found no matching record.

