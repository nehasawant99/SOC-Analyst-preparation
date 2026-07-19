# Module 1 – Lesson 4: Event ID 4625 (Failed Logon)

# Learning Goal

By the end of this lesson, you will understand:

* What Event ID 4625 is.
* Why Windows generates it.
* Common reasons it occurs.
* How a SOC analyst investigates it.
* How to avoid jumping to conclusions.

# What is Event ID 4625?

Event ID 4625 is generated when a logon attempt fails.

> **In simple words:** Someone tried to log in, but Windows denied access. This does not automatically mean a hacker tried to log in.

---

# Real-Life Examples

### Example 1 – Normal User

```
Neha enters the wrong password.
      │
      ▼
Windows rejects the password.
      │
      ▼
Event ID 4625 is generated.

```

* **Status:**  Normal activity

### Example 2 – Forgotten Password

```
Admin forgets the password.
      │
      ▼
Tries 3 times.
      │
      ▼
Third attempt is still incorrect.
      │
      ▼
Three Event ID 4625 logs are generated.

```

* **Status:**  Normal activity

### Example 3 – Brute-Force Attack

```
Attacker tries: admin123, password123, welcome123, 123456, qwerty...
      │
      ▼
Windows rejects every attempt.
      │
      ▼
Hundreds of Event ID 4625 events are generated.

```

* **Status:**  Suspicious activity

---

> **Important Lesson:** The same Event ID can represent either a normal user mistake or a malicious attack. That's why context matters.

---

# Typical Event 4625 Fields

* **Event ID:** 4625
* **Time:** 09:20 AM
* **User:** Admin
* **Computer:** PC-101
* **Description:** An account failed to log on.

As you progress, you'll also learn fields like:

* Logon Type
* Failure Reason
* Source Network Address
* Workstation Name

These help determine what really happened.

---

# Investigation Process

Suppose you receive this alert: **Event ID: 4625 | User: Admin | Time: 09:20 AM**

A SOC analyst asks:

1. **Check the volume of failures:** Step 1.
How many failed logins occurred? One? Five? One hundred?


2. **Look for subsequent success:** Step 2.
Did a successful login happen afterwards? If yes, was it the same user? Was it from the same computer?


3. **Analyze the source network address:** Step 3.
Was it from the same IP address? An internal IP like `192.168.1.10` vs a public IP from an unexpected location (`203.x.x.x`) dictates the escalation path.


4. **Examine the timestamp patterns:** Step 4.
When did the failures occur? Many failures within a few seconds (e.g., 09:20:01, 09:20:03, 09:20:05) could indicate an automated attack.


5. **Verify account context:** Step 5.
Is this user known? Is this a real employee? Is this an administrator account? Is the account disabled? Has this happened before?


---

# Don't Jump to Conclusions

Suppose you see **Event ID: 4625**.

Don't immediately say:  **"It's a hacker."**

**Instead ask:**

* Was the password typed incorrectly?
* Is the user new?
* Did the keyboard layout change?
* Is the account locked?
* Is someone testing credentials?
* Are there repeated attempts from the same source?

Always gather evidence first.
