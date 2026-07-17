# Incident Report

## Executive Summary

During this investigation, multiple failed Windows authentication events (Event ID 4625) were identified and analyzed using Windows Event Viewer.

The objective of the investigation was to determine whether the failed authentication attempts represented expected user activity or potential malicious behavior.

---

## Investigation Process

The Windows Security log was filtered for Event ID **4625**.

The following fields were analyzed:

- Event ID
- Timestamp
- Logon Type
- Failure Reason
- Status
- Sub Status
- Source Network Address
- Source Port

---

## Findings

| Field | Value |
|-------|-------|
| Event ID | 4625 |
| Logon Type | 2 (Interactive) |
| Source Address | 127.0.0.1 |
| Source Port | 0 |
| Result | Failed Authentication |

---

## Analysis

The investigation determined that the failed authentication attempts originated from the local computer.

The combination of **Logon Type 2**, **Source Address 127.0.0.1**, and **Source Port 0** indicates that the authentication attempts occurred locally at the computer rather than across the network.

The authentication failures were intentionally generated during a controlled lab exercise by entering an incorrect password multiple times.

---

## Conclusion

Based on the available evidence, the failed authentication events were determined to be expected activity within a controlled lab environment.

No evidence of unauthorized access or malicious activity was identified.
