# Lessons Learned

## Technical Lessons

- Windows records failed authentication attempts using Event ID 4625.
- Event Viewer provides detailed authentication information useful during investigations.
- Logon Type identifies how authentication was attempted.
- Source Network Address helps determine where authentication originated.
- Multiple event fields should be correlated before reaching conclusions.

---

## Investigation Lessons

A failed logon event alone does not indicate malicious activity.

Evidence should always be reviewed together before making a conclusion.

Analysts should avoid assumptions and instead base findings on observable evidence.

---

## Personal Reflection

This lab helped me better understand how Windows records authentication events and how to investigate them using Event Viewer.

I also learned the importance of documenting investigations clearly and objectively, using evidence to support every conclusion.
