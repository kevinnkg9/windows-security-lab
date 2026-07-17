# Lab 02 - Successful Logon Investigation

## Status

Completed

---

## Objective

Investigate Windows Security Event ID 4624 and determine whether the authentication represents expected or suspicious activity.

---

## Tools

- Windows 11
- Windows Event Viewer
- GitHub
- Obsidian

---

## Skills Demonstrated

- Windows Event Log Analysis
- Authentication Investigation
- Logon Type Analysis
- Evidence Collection
- Incident Documentation

---

## Investigation Summary

During this investigation, multiple Event ID 4624 events were analyzed.

The investigation identified several successful authentication types, including:

- Logon Type 5 (Service Logon)
- Logon Type 7 (Workstation Unlock)
- Logon Type 11 (Cached Interactive)

The analysis showed that Event ID 4624 alone does not indicate how a user authenticated. The Logon Type provides important context that allows an analyst to determine whether the authentication was performed by a user, Windows service, or another component.

Based on the evidence collected, the observed events were determined to be expected Windows activity.