# Module 1 – Lesson 5: Event ID 4624 (Successful Logon)

# Learning Goal

By the end of this lesson, you will understand:

* What Event ID 4624 is.
* When Windows generates it.
* Why it is important.
* Why a successful login is not always normal.
* How a SOC analyst investigates it.

# What is Event ID 4624?

Event ID 4624 is generated when a user successfully logs into Windows.

```
User enters correct credentials
        │
        ▼
Windows verifies the credentials
        │
        ▼
Access is granted
        │
        ▼
Event ID 4624 is generated

```

> **Think of it as:** *"Someone successfully accessed the system."*

---

# Real-Life Examples

### Example 1 – Normal Login

```
09:00 AM ──> Neha enters the correct password.
                 │
                 ▼
             Windows grants access.
                 │
                 ▼
             Event ID 4624

```

* **Status:**  Normal

### Example 2 – Office Employee

```
08:55 AM ──> John arrives at work.
                 │
                 ▼
             Logs into his office PC.
                 │
                 ▼
             Event ID 4624

```

* **Status:**  Expected activity

### Example 3 – Attacker

```
Attacker steals Admin password.
        │
        ▼
Uses the correct password.
        │
        ▼
Windows grants access.
        │
        ▼
Event ID 4624

```

* **Status:**  Also generates Event ID 4624.

> **Key takeaway:** This is why analysts never assume every successful login is legitimate.

---

# 4625 vs 4624

| Event ID | Meaning |
| --- | --- |
| **4625** | Failed logon |
| **4624** | Successful logon |

### Example Timeline

```
09:00 AM ──> Event 4625 (Wrong password)
                 │
                 ▼
09:01 AM ──> Event 4624 (Correct password)

```

* **Context:** This could simply mean the user mistyped the password first.

---

# Important Fields

```text
Event ID: 4624
Time: 09:15 AM
User: Administrator
Computer: SERVER-01
Level: Information
Description: An account was successfully logged on.

```

* **Fields you'll always check:** Event ID, Time, User, Computer, Description
* **Later, you'll learn:** Logon Type, Authentication Package, Source Network Address, Logon Process

---

# Investigation Process

Imagine you receive an alert: **4624 | User: Administrator | Time: 02:30 AM**

Don't immediately say: **"Everything is fine."**

**Instead ask:**

* Is the login time normal?
* Does the Administrator usually log in at 2:30 AM?
* Which computer was accessed?
* Did any failed logins happen before this?
* Was it a local login or a remote login?
* What happened after the login?

---

# Build a Timeline

```
08:58 AM ──> Event 4625 (Failed Login)
                 │
                 ▼
09:00 AM ──> Event 4624 (Successful Login)
                 │
                 ▼
09:02 AM ──> PowerShell Started
                 │
                 ▼
09:05 AM ──> New User Created

```

**Questions:**

* Is this expected?
* Did someone misuse the account?
* Should this be investigated further?

> The answer isn't "yes" or "no" immediately—you collect evidence first.

---

# Investigation Mindset

A successful login becomes suspicious when:

* It happens at an unusual time.
* It comes from an unknown device.
* It comes from an unusual IP.
* It is followed by suspicious activity.
* It involves a privileged account unexpectedly.
