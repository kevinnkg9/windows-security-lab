# WS-004: Local User Account Creation Investigation

## Objective

The objective of this lab was to investigate a Windows Security Event ID 4720 (User Account Creation). The goal was to determine who created the account, when the account was created, and whether the activity represented expected administrative behavior or a potential security concern.

## Lab Environment

- Operating System: Windows 11 Pro
- Tool: Windows Event Viewer
- Log Source: Windows Security Log
- Event ID: 4720 (A user account was created)
- Test Account: soclab

## Skills Demonstrated

- Windows Event Viewer analysis
- Windows Security Log investigation
- User account auditing
- Evidence collection
- Incident documentation
- Event correlation
- Windows account management analysis

## Event Investigated

**Event ID:** 4720

**Event Name:** A user account was created

## Investigation Summary

A local user account named **soclab** was intentionally created to generate a Windows Security Event ID 4720. The investigation confirmed that the account was created by the logged-in user (**kevin**) on the local workstation.

The event timestamp, subject account, and newly created account information were reviewed to determine whether the activity was authorized.

Based on the collected evidence, the account creation was determined to be legitimate administrative activity performed for laboratory testing.

## MITRE ATT&CK Mapping

**Tactic:** Persistence

**Technique:** T1136 – Create Account

Although attackers frequently create local accounts to maintain persistence, this investigation confirmed that the activity was authorized and performed as part of a controlled lab exercise.

## Outcome

**Disposition:** Closed

**Reason:** Authorized user account creation performed for lab testing. No indicators of malicious activity were identified.
---

# Screenshots

## Event Viewer Alert

This screenshot shows the Security log containing Event ID 4720, indicating that a new local user account was created.

![Event Viewer Alert](images/WS004-Event-List.png)

---

## General Event Details

The General tab provides a human-readable summary of the event, including the account that was created, the account that performed the action, and the event timestamp.

![General Tab](images/WS004-General-Tab.png)

---

## Event Details

The Details tab displays the structured event data used by security analysts during investigations and provides additional forensic information beyond the General view.

![Details Tab](images/WS004-Details-Tab.png)

---

## Audit Policy Configuration

Before this investigation, User Account Management auditing was enabled using the Windows `auditpol` utility. This ensured that Windows generated Event ID 4720 when the test account was created.

![Audit Policy](images/WS004-Audit-Policy.png)