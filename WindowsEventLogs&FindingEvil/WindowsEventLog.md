## Windows Event Logging Basics

- Windows event logging offers comprehensive logging capabilities for application errors, security events, and diagnostic information. As cybersecurity professionals, we leverage these logs extensively for analysis and intrusion detection.

- The default Windows event logs consist of Application, Security, Setup, System, and Forwarded Events. While the first four logs cover application errors, security events, system setup activities, and general system information, the "Forwarded Events" section is unique, showcasing event log data forwarded from other machines.

- It should be noted, that the Windows Event Viewer has the ability to open and display previously saved .evtx files, which can be then found in the "Saved Logs" section.

### The Anatomy of an Event Log

- When examining Application logs, we encounter two distinct levels of events: information and error.

- 4624(S): An account was successfully logged on. (https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/event-4624)

### Leveraging Custom XML Queries

- To streamline our analysis, we can create custom XML queries to identify related events using the "Logon ID" as a starting point. By navigating to "Filter Current Log" -> "XML" -> "Edit Query Manually," we gain access to a custom XML query language that enables more granular log searches.

- Advanced XML filtering in the Windows Event Viewer (https://techcommunity.microsoft.com/blog/askds/advanced-xml-filtering-in-the-windows-event-viewer/399761)

- 4907(S): Auditing settings on object were changed. (https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/event-4907)

- DACLs and SACLs (https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists)

- Audit Generation (https://learn.microsoft.com/en-us/windows/win32/secauthz/audit-generation)

- SACL Access Right (https://learn.microsoft.com/en-us/windows/win32/secauthz/sacl-access-right)

- ACE Strings (https://learn.microsoft.com/en-us/windows/win32/secauthz/ace-strings?redirectedfrom=MSDN)

- Understanding SDDL Syntax (https://uwconnect.uw.edu/it?id=kb_article_view&sysparm_article=KB0034194)

- Privilege Constants (Authorization) - (https://learn.microsoft.com/en-us/windows/win32/secauthz/privilege-constants)

### Useful Windows Event Logs

#### Windows System Logs

 - Event ID 1074 (System Shutdown/Restart)
 - Event ID 6005 (The Event log service was started)
 - Event ID 6006 (The Event log service was stopped)
 - Event ID 6013 (Windows uptime)
 - Event ID 7040 (Service status change)

#### Windows Security Logs

- Event ID 1102 (The audit log was cleared)
- Event ID 1116 (Antivirus malware detection)
- Event ID 1118 (Antivirus remediation activity has started)
- Event ID 1119 (Antivirus remediation activity has succeeded)
- Event ID 1120 (Antivirus remediation activity has failed)
- Event ID 4624 (Successful Logon)
- Event ID 4625 (Failed Logon)
- Event ID 4648 (A logon was attempted using explicit credentials)
- Event ID 4656 (A handle to an object was requested)
- Event ID 4672 (Special Privileges Assigned to a New Logon)
- Event ID 4698 (A scheduled task was created)
- Event ID 4700 & Event ID 4701 (A scheduled task was enabled/disabled)
- Event ID 4702 (A scheduled task was updated)
- Event ID 4719 (System audit policy was changed)
- Event ID 4738 (A user account was changed)
- Event ID 4771 (Kerberos pre-authentication failed)
- Event ID 4776 (The domain controller attempted to validate the credentials for an account)
- Event ID 5001 (Antivirus real-time protection configuration has changed)
- Event ID 5140 (A network share object was accessed)
- Event ID 5142 (A network share object was added)
- Event ID 5145 (A network share object was checked to see whether client can be granted desired access)
- Event ID 5157 (The Windows Filtering Platform has blocked a connection)
- Event ID 7045 (A service was installed in the system)
