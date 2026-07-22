````markdown
# Authentication Investigation Report

## Objective

Investigate the authentication events and determine whether the activity appears normal or suspicious.

---

## Investigation Scenario

**Date:** 22-Jul-2026

```text
08:58:30
Event ID: 4625
User: Administrator
Computer: HR-PC-01
Logon Type: 10
Description: Failed logon

↓

08:58:36
Event ID: 4625
User: Administrator
Computer: HR-PC-01
Logon Type: 10
Description: Failed logon

↓

08:58:41
Event ID: 4625
User: Administrator
Computer: HR-PC-01
Logon Type: 10
Description: Failed logon

↓

08:58:48
Event ID: 4624
User: Administrator
Computer: HR-PC-01
Logon Type: 10
Description: Successful logon

↓

08:59:20
Event ID: 4688
User: Administrator
Computer: HR-PC-01
Description:
PowerShell.exe started

↓

09:01:10
Event ID: 4720
User: Administrator
Computer: HR-PC-01
Description:
A new local user account was created.

↓

09:03:45
Windows Defender Alert

Description:
Suspicious PowerShell behaviour detected.
```

---

# Your Task

Write the report in the following format.

---

## 1. Incident Summary

*(2–4 lines)*

What happened overall?

---

## 2. Timeline

List the events in order.

**Example:**

```text
08:58:30 – Failed Login
08:58:36 – Failed Login
...
```

---

## 3. Investigation

Answer questions like:

- What stands out?
- Which events are unusual?
- What would you investigate next?
- Which evidence supports your investigation?

---

## 4. Findings

Write what you observed.

**Examples:**

- Multiple failed logins occurred.
- Successful Remote Desktop login.
- PowerShell executed.
- New user account created.

> **Note:** Don't conclude "attack" yet unless the evidence supports it.

---

## 5. Conclusion

Can you conclude this is malicious?

Or do you need more evidence?

Explain why.

---

## 6. Recommendations

What should the SOC analyst do next?

**Examples:**

- Review PowerShell commands.
- Verify whether the Administrator performed the login.
- Check the source IP address.
- Investigate the newly created user account.
- Review Windows Defender alert details.
````
