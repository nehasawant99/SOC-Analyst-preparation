# Mini Exercise 1 – Review

### Scenario

* **09:00 AM:** User: Alice — Event ID: 4624 (Logon Type: 2)

---

### Questions & Answers

**1. What happened?**

* **Answer:** Alice successfully logged into the system using Logon Type 2 (Interactive Logon).
* **Status:** Correct

**2. Is this normal?**

* **Answer:** Yes. This appears to be normal because Alice logged into her computer during normal working hours using an Interactive Logon. However, I would still compare it with her normal login pattern before making a final conclusion.
* **Status:**  Excellent

**3. Would you investigate further?**

* **Answer:** I would investigate further only if there was suspicious activity after the login or if the login did not match Alice's normal behavior.
* *Examples:* Unusual login time, suspicious processes, new administrator account created, or multiple failed logins before the successful login.


* **Status:** Very good thinking.

**4. Why?**

* **Answer:** I cannot directly conclude that every successful login is normal. I need to collect evidence and investigate further if required before making a conclusion.
* **Status:** Perfect.

---

# Mini Exercise 2 – Review

### Scenario

* **02:30 AM:** User: Administrator — Event ID: 4624 (Logon Type: 10 - Remote Desktop)

---

### Questions & Answers

**1. What happened?**

* **Answer:** The Administrator account successfully logged in at 2:30 AM using Logon Type 10 (Remote Desktop).
* **Status:** Correct

**2. What does Logon Type 10 mean?**

* **Answer:** Logon Type 10 means a Remote Interactive (Remote Desktop Protocol - RDP) login. The user accessed the computer remotely from another device instead of logging in directly at the computer.
* **Status:** Correct

**3. Is this automatically malicious?**

* **Answer:** No. I cannot conclude it is malicious based on this event alone. I would first consider whether:
* The Administrator normally works at this time.
* The organisation allows Remote Desktop access.
* This login matches the user's previous activity and work pattern.
* More evidence is required before concluding.


* **Status:** Excellent

**4. What would you investigate next?**

* **Answer:** I would investigate:
* The source IP address.
* The computer used for the remote login.
* The Administrator's activity after the successful login.
* Whether the login matches the user's previous work pattern.
* Any related events before and after the login.
* I would collect additional evidence before deciding whether the activity is suspicious.


* **Status:** Excellent investigation plan.

---

# Mini Exercise 3 – Review

### Scenario

* **11:00 AM:** User: SQLService — Event ID: 4624 (Logon Type: 5)

---

### Questions & Answers

**1. What happened?**

* **Answer:** The SQLService account successfully logged in using Logon Type 5 to start or access the service required by the application.
* **Status:** Correct
* **Note:** A service account usually logs in automatically when the service starts. It is not a person typing a password.

**2. What does Logon Type 5 indicate?**

* **Answer:** Logon Type 5 indicates a Service Logon. Windows starts a service using a service account, such as SQL Server or another application service.
* **Status:** Correct

**3. Would you classify this as suspicious?**

* **Answer:** No. I cannot classify it as suspicious based on this event alone. I would collect more evidence and review the activity if anything unusual occurs after the service starts.
* **Status:** Excellent

**4. Why or why not?**

* **Answer:** Many applications require service accounts to start automatically. This is normal system behavior. However, if the service account is misused or performs unusual actions, I would investigate further before making a conclusion.
* **Status:** Excellent
