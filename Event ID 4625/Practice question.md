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

# Learning

* One failed login followed by a successful login is often a normal user mistake.
* Do not assume every failed login is a cyberattack.
* Always collect more evidence before concluding.
* Review related events and build a timeline to understand what happened.
