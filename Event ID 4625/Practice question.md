# Mini Exercise

### Scenario

* **09:00 AM:** Admin — Failed Login (Event ID: 4625) — Only one failed attempt
* **Five seconds later:** Admin successfully logs in.

---

### Questions & Answers

**1. What happened?**

* **Answer:** The Admin tried to log in, but the first login attempt failed. Five seconds later, the Admin successfully logged in.
* **Status:**  Correct

**2. Is there enough evidence to call this a cyberattack?**

* **Answer:** No. We cannot conclude it is a cyberattack because there is not enough evidence. We need to investigate further and collect more information before concluding.
* **Status:** Correct

**3. What would you investigate next?**

* **Answer:** I would check the user's activity after the successful login and review related logs to see if there was any suspicious activity.
* **Status:**  Good thinking

**4. What is the most likely explanation?**

* **Answer:** The most likely explanation is that the Admin mistyped the password on the first attempt and then entered the correct password. Based on this event alone, we cannot conclude it is a security incident.
* **Status:**  Excellent

---


# Practice Set 1 – Review

## Question 1

### Scenario

* **09:00 AM:** User: Neha — One failed login — No more events

---

### Questions & Answers

**1. What happened?**

* **Answer:** The user Neha attempted to log in, but the login failed once.
* **Status:** Correct

**2. Is this suspicious?**

* **Answer:** No. I cannot conclude it is suspicious based on a single failed login. I would collect more evidence and investigate further if additional suspicious activity is observed. The login also occurred during normal working hours.
* **Status:** Excellent

**3. What could be the reason?**

* **Answer:** The most likely reason is that the user mistyped the password. However, there could be other reasons, so additional evidence is required before concluding.
* **Status:** Correct

**4. Would you escalate immediately?**

* **Answer:** No. I would not escalate the incident immediately. I would first review the related logs, collect additional evidence, and then decide whether escalation is necessary.
* **Status:** Excellent

---

## Question 2

### Scenario

* **09:00 AM:** User: Admin — 25 failed logins within 1 minute — No successful login

---

### Questions & Answers

**1. What happened?**

* **Answer:** The Admin account had 25 failed login attempts within one minute, and there was no successful login afterwards.
* **Status:** Correct

**2. Is this normal?**

* **Answer:** No. This is unusual because 25 failed login attempts within one minute are not typical user behaviour. It requires further investigation.
* **Status:** Correct
* **Note:** Notice that we still avoid saying "attack" immediately. We say "unusual activity" until we have more evidence.

**3. What type of attack could this indicate?**

* **Answer:** This activity could indicate a brute-force password attack, where someone repeatedly tries different passwords to gain access to an account.
* **Status:** Correct
* **Note:** Notice the wording: *"Could indicate"* instead of *"It is definitely a brute-force attack."* Evidence first, conclusion later.

**4. What evidence would you collect?**

* **Answer:** I would investigate:
* The source IP address.
* The computer from which the login attempts originated.
* The Logon Type.
* Whether the attempts came from the same or different systems.
* Whether similar activity has occurred before.
* Any related events before and after the failed logins.
* I would collect additional evidence before concluding.


* **Status:** Excellent


# Learning

* One failed login followed by a successful login is often a normal user mistake.
* Do not assume every failed login is a cyberattack.
* Always collect more evidence before concluding.
* Review related events and build a timeline to understand what happened.
