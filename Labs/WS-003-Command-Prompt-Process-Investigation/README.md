# WS-003: Command Prompt Process Creation Investigation

## Objective

The objective of this lab was to investigate a Windows Security Event ID 4688 (Process Creation) after manually launching Command Prompt. The goal was to determine whether the activity represented expected user behavior or required further investigation by analyzing the process details, parent process, user account, and command-line information.

## Lab Environment

- Operating System: Windows 11 Pro
- Tool: Windows Event Viewer
- Log Source: Windows Security Log
- Event ID: 4688 (A new process has been created)
- Application Investigated: Command Prompt (cmd.exe)

## Skills Demonstrated

- Windows Event Viewer navigation
- Security log analysis
- Process creation investigation
- Parent-child process analysis
- Command-line analysis
- Evidence-based incident investigation
- Basic Windows forensic analysis

## Event Investigated

**Event ID:** 4688

**Event Name:** A new process has been created

## Investigation Summary

A Command Prompt (`cmd.exe`) process was manually launched to generate a Windows Security Event ID 4688. The investigation confirmed that the executable originated from the legitimate Windows System32 directory and was started by `explorer.exe`, indicating that it was launched through the Windows graphical interface.

The process executed under the logged-in user account and contained a normal command line without suspicious arguments or indicators of malicious activity.

After reviewing the available evidence, the activity was determined to be legitimate user behavior and the investigation was closed with no security concerns identified.

## Outcome

**Disposition:** Closed

**Reason:** Legitimate user-initiated process execution. No indicators of malicious activity were identified.