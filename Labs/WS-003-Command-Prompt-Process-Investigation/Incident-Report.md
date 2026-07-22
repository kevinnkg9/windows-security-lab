# Incident Report

## Alert Information

**Alert Name:** Process Creation

**Event ID:** 4688

**Severity:** Informational

**Status:** Closed

**Date Investigated:** *(Enter the date you completed the lab)*

---

# Incident Summary

A Windows Security Event ID 4688 was generated after manually launching Command Prompt (`cmd.exe`). The objective of the investigation was to determine whether the newly created process represented legitimate user activity or suspicious behavior.

The investigation focused on verifying the process location, parent process, user account, and command-line arguments to determine if any indicators of compromise were present.

---

# Evidence Collected

| Evidence | Value |
|----------|-------|
| Event ID | 4688 |
| Process Name | cmd.exe |
| Full Process Path | C:\Windows\System32\cmd.exe |
| Parent Process | C:\Windows\explorer.exe |
| User Account | KEVS-LAPTOP\Kevin |
| Command Line | "C:\Windows\System32\cmd.exe" |
| Investigation Tool | Windows Event Viewer |

---

# Investigation Process

## Step 1 – Verify the Process

The newly created process was identified as **cmd.exe**, the Windows Command Prompt executable.

The executable was launched from the legitimate Windows System32 directory, which is the expected location for Command Prompt.

**Finding:** Legitimate Windows executable.

---

## Step 2 – Analyze the Parent Process

The parent process was identified as **explorer.exe**.

Explorer.exe is responsible for the Windows desktop, taskbar, Start menu, and File Explorer. It commonly launches applications that users open through the graphical interface.

Because Command Prompt was launched manually from the Windows desktop, the parent-child relationship was expected.

**Finding:** Parent process is consistent with normal user activity.

---

## Step 3 – Verify the User Account

The Security ID showed that the process executed under the logged-in user account:

**KEVS-LAPTOP\Kevin**

This confirmed the process was started interactively by the current user rather than automatically by a Windows service or the SYSTEM account.

**Finding:** Expected user context.

---

## Step 4 – Review the Command Line

The command line contained only the executable path:

```text
"C:\Windows\System32\cmd.exe"
```

No suspicious arguments, encoded commands, scripts, or additional parameters were observed.

**Finding:** Normal Command Prompt execution.

---

# Analysis

Multiple pieces of evidence were reviewed before reaching a conclusion.

The executable originated from the expected Windows directory.

The parent process matched how Windows normally launches applications through the graphical interface.

The process executed under the logged-in user account and contained no suspicious command-line arguments.

No abnormal behavior or indicators of malicious activity were identified during the investigation.

---

# Conclusion

Based on the collected evidence, the process creation event was determined to be legitimate user activity.

No indicators of compromise were identified.

**Final Disposition:** Closed

---

# Analyst Notes

This investigation demonstrated the importance of reviewing multiple pieces of evidence before making a security decision. Rather than relying solely on the process name, the investigation considered the executable path, parent-child relationship, user account, and command-line arguments to determine whether the activity was expected.

This lab also reinforced the value of Process Creation auditing (Event ID 4688) for monitoring application execution on Windows systems.