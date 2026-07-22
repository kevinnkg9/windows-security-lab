# Lessons Learned

## Overview

This lab provided hands-on experience investigating Windows Security Event ID 4688 (Process Creation) using Windows Event Viewer. The investigation focused on determining whether a newly created Command Prompt process represented normal user activity or potentially suspicious behavior.

---

## Key Takeaways

- Event ID 4688 records newly created processes when Process Creation auditing is enabled.
- A process should never be evaluated based only on its name.
- Verifying the executable path helps determine whether the process is legitimate.
- Parent-child process relationships provide important context during investigations.
- The Security ID identifies which user account launched the process.
- Command-line arguments should always be reviewed for suspicious behavior.
- Multiple pieces of evidence should be analyzed before reaching a conclusion.

---

## Challenges Encountered

One of the biggest challenges during this lab was that Event ID 4688 was not initially being generated. This was caused by Process Creation auditing not being enabled.

After enabling the appropriate audit policy and updating Group Policy, Windows began recording process creation events successfully.

This experience demonstrated that proper logging and auditing configuration is essential before meaningful investigations can take place.

---

## Skills Developed

During this lab I practiced:

- Investigating Windows Security Logs
- Identifying parent-child process relationships
- Reviewing executable paths
- Analyzing command-line arguments
- Documenting an investigation using professional incident response practices

---

## Future Improvements

Future process investigations will include more advanced applications such as PowerShell, Windows Services, scheduled tasks, and other Windows processes to improve familiarity with normal system behavior and strengthen incident investigation skills.