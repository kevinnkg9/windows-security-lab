# Lessons Learned

## Overview

This lab focused on investigating Windows Security Event ID 4720, which records the creation of local user accounts.

The investigation demonstrated how Windows Security Logs can be used to identify who created an account, when the action occurred, and whether the activity was expected or suspicious.

---

## Key Takeaways

- Event ID 4720 records local user account creation.
- The Subject section identifies the account responsible for performing the action.
- The New Account section identifies the account that was created.
- Event timestamps provide an accurate timeline for account management activity.
- Account creation events should always be validated before determining whether the activity is malicious.

---

## Challenges Encountered

Initially, Event ID 4720 was not generated because **User Account Management auditing** was disabled.

After enabling auditing with `auditpol`, Windows successfully recorded account creation events.

This reinforced the importance of verifying audit policy configuration before beginning an investigation.

---

## Skills Developed

- Windows Security Event analysis
- Account management auditing
- Windows Event Viewer investigation
- Incident documentation
- Evidence-based analysis
- MITRE ATT&CK mapping

---

## Future Improvements

Future account management investigations will include:

- User account deletion (Event ID 4726)
- Password reset events
- Group membership changes
- Privilege escalation investigations