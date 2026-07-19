# Module 1 – Lesson 3: Understanding Windows Event Structure

# Goal

Learn how to read any Windows event. By the end of this lesson, you should be able to answer:

* What happened?
* When did it happen?
* Who did it?
* Which computer?
* Is it normal or suspicious?

# What is an Event?

An event is a single record created by Windows when an action occurs.

```
User logs in
      │
      ▼
Windows records an event

```

Each event contains information that helps an analyst investigate.

---

# Basic Event Structure

Every Windows event contains fields like these:

| Field | Purpose |
| --- | --- |
| **Event ID** | Identifies the type of event |
| **Date & Time** | When the event happened |
| **Level** | Information, Warning, Error, Critical |
| **Source** | Which Windows component generated the event |
| **Computer** | Computer where the event occurred |
| **User** | User involved (if applicable) |
| **Description** | Details about what happened |

---

# Example Event

* **Event ID:** 4625
* **Date & Time:** 15-Jul-2026 09:15:30
* **Level:** Information
* **Source:** Microsoft-Windows-Security-Auditing
* **Computer:** DESKTOP-01
* **User:** Administrator
* **Description:** An account failed to log on.

---

# Understanding Each Field

### Event ID

* Think of it as the event's identity.
* *Example:* `4625`
* It tells you what type of event occurred.

> **Note:** Don't memorize Event IDs yet. Understand what they represent.

### Date & Time

* *Example:* `09:15:30`
* **Ask:**
* When did it happen?
* Before or after another event?


* Time is used to build an investigation timeline.

### Level

* *Example:* `Information`
* **Important:** A security event can have an Information level and still be very important. Never ignore an event just because its level says "Information."

### Source

* *Example:* `Microsoft-Windows-Security-Auditing`
* This tells you which Windows component generated the event.

### Computer

* *Example:* `DESKTOP-01`
* Useful when investigating multiple systems.

### User

* *Example:* `Administrator`
* **Ask:**
* Which account was involved?
* Is this account expected to perform this action?



### Description

* *Example:* `An account failed to log on.`
* This is the first thing analysts usually read. It gives a quick summary of what happened.

---

# Investigation Example

You see:

* **Event ID:** 4625
* **User:** Administrator
* **Time:** 10:05 AM
* **Description:** An account failed to log on.

Instead of saying: **"It's an attack."**

**Ask:**

* Who is Administrator?
* How many failures occurred?
* Was there a successful login later?
* Is this normal for this user?
* Did the same IP try multiple accounts?

That's investigation.
