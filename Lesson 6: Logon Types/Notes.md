# Module 1 – Lesson 6: Logon Types (How Did the User Log In?)

# Learning Goal

By the end of this lesson, you should be able to answer:

* The login was successful... **but how did the user log in?**

A successful login can happen in many ways.

---

# Why Logon Type Matters

Suppose you see:

```text
Event ID: 4624
User: Administrator
Status: Successful Login

```

**Question:** Was it:

* Someone sitting at the computer?
* Someone connecting through Remote Desktop?
* A Windows service?
* A scheduled task?
* A network file access?

> **Key Takeaway:** Without the **Logon Type**, you don't know *how* access was gained.

---

# Most Important Logon Types

You don't need to memorise every logon type. Start with these six:

| Logon Type | Meaning | Common Use |
| --- | --- | --- |
| **2** | **Interactive** | User logs in directly at the keyboard |
| **3** | **Network** | Accessing a shared folder or printer over the network |
| **4** | **Batch** | Scheduled task or automated job |
| **5** | **Service** | Windows service starts using an account |
| **7** | **Unlock** | User unlocks a locked computer |
| **10** | **Remote Interactive** | Remote Desktop (RDP) login |

These are the ones you'll encounter most often in SOC investigations.

---

# Deep Dive: Key Logon Types

### Logon Type 2 – Interactive

```
Neha ──> Sits at office PC ──> Enters password ──> Windows Desktop opens

```

* **Logon Type:** `2`
* **Status:**  Usually normal.

---

### Logon Type 3 – Network

```
Laptop ──> Opens shared folder ──> File Server

```

* **Logon Type:** `3`
* **Context:** The user didn't sit at the server. They simply accessed a network resource over the network.

---

### Logon Type 5 – Service

```
SQL Server Service ──> Starts automatically ──> Logs in using its service account

```

* **Logon Type:** `5`
* **Status:**  This is usually expected system behaviour.

---

### Logon Type 7 – Unlock

```
Lunch Break ──> Computer Locked ──> User Returns ──> Unlocks PC

```

* **Logon Type:** `7`

---

### Logon Type 10 – Remote Desktop (RDP)

```
Home Laptop ──> Remote Desktop Connection ──> Office Computer

```

* **Logon Type:** `10`
* **Context:** Common for remote administration. However, if your organisation doesn't normally use RDP, a Logon Type 10 event may deserve investigation.

---

# Investigation Example

Suppose you see this log entry:

```text
Time: 02:00 AM
User: Administrator
Event ID: 4624
Logon Type: 10

```

**Questions to ask:**

* Does the company allow RDP?
* Does the Administrator normally work at 2:00 AM?
* Which IP address initiated the connection?
* Which computer was accessed?
* What happened after the login?

> Notice we're still collecting evidence—not assuming an attack.

---

# Investigation Mindset

Don't ask only: **"Did someone log in?"**

Also ask: **"How did they log in?"**

That one question can completely change the direction of your investigation.

# There are different account types:

- User Accounts – Alice, John, Neha
- Administrator Accounts – Admin, Administrator
- Service Accounts – SQLService, BackupService, IISService
- Computer Accounts – Used by Windows machines in a domain
* **NOTE**: Confusing between the service logon it handles by the system or certain applications not by the user (Human)
