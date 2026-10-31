Day-07-Review-and-Knowledge-Check

Reviewed the Windows Security events investigated during the week.

Key concepts:

Event ID 4624: Successful login.

Event ID 4625: Failed login.

Event ID 4634: Logoff.

Event ID 4722: Account enabled.

Event ID 4723: Password change attempt.

Event ID 4724: Password reset attempt.

Event ID 4725: Account disabled.

Event ID 4740: Account locked out.

Completed a knowledge check and reviewed the importance of distinguishing between missing log records and proof that an activity never occurred.

Lessons Learned

During this lab, I learned how to investigate Windows Security events using Wazuh Threat Hunting. I practiced searching by Windows Event ID, inspecting alert details, and identifying the account involved in an event.

I also learned that successful logins, failed logins, logoffs, and account-management events provide useful information when investigating endpoint activity.

An important lesson was that not finding an event does not prove that the activity never happened. Events may not have been generated, collected, or retained.

Conclusion

Week 11 improved my understanding of Windows authentication and account-management monitoring. I gained practical experience using Wazuh to investigate Windows Server 2022 security events and interpret the information collected from the endpoint.

The investigation also reinforced the importance of documenting actual findings without making conclusions that the available logs cannot support.
