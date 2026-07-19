# Mini Investigation Exercise

### Event

* **Event ID:** 4625
* **Time:** 09:20 AM
* **Computer:** PC-101
* **User:** Admin
* **Level:** Information
* **Description:** An account failed to log on.

---

### Questions & Answers

**1. What happened?**

* **Answer:** An account failed to log on.
* **Status:** Correct

**2. Which user was involved?**

* **Answer:** Admin was the user involved.
* **Status:** Correct

**3. Which computer generated the event?**

* **Answer:** PC-101 generated the event.
* **Status:** Correct

**4. At what time did it happen?**

* **Answer:** 09:20 AM
* **Status:** Correct

**5. Can you conclude this is a cyberattack?**

* **Answer:** We cannot conclude it is a cyberattack. Maybe the Admin mistyped the password. To conclude whether it is an attack, we need more evidence and data from the logs.
* **Status:** Excellent thinking.

---

# Learning

* One failed login does not mean a cyberattack.
* Always collect more evidence before concluding.
* Review additional logs and related events to understand what happened.
* Build a timeline before deciding whether the activity is normal or suspicious.


# Practice Set 1 – Review

## Question 1

### Event

* **Event ID:** 4625
* **Time:** 08:30 AM
* **Computer:** DESKTOP-01
* **User:** John
* **Description:** An account failed to log on.

---

### Questions & Answers

**1. What happened?**

* **Your Answer :** User John attempted to log in to the account, but the logon failed.
* **Status:**  Correct

**2. Which user was involved?**

* **Your Answer :** John was the user involved.
* **Status:**  Correct

**3. Which computer generated the event?**

* **Your Answer :** DESKTOP-01 generated the event.
* **Status:**  Correct

**4. At what time did it happen?**

* **Your Answer:** 08:30 AM
* **Status:**  Correct

**5. Is this enough evidence to conclude it is a cyberattack? Why?**

* **Your Answer :** No. There is not enough evidence to conclude it is a cyberattack. It could simply be a failed login attempt. I would investigate further and check whether the user logged in successfully afterward or if there were multiple failed login attempts.
* **Status:**  Excellent.

> **Mentor Feedback (10/10):** The best sentence was: *"Let see if user login after that."* That is exactly what analysts do. They ask: **What happened next?**

---

## Question 2

### Event

* **Event ID:** 4688
* **Time:** 11:45 AM
* **Computer:** HR-PC
* **User:** Alice
* **Level:** Information
* **Description:** A new process has been created.

---

### Questions & Answers

**1. What happened?**

* **Your Answer :** User Alice created a new process on the system.
* **Status:**  Correct.
* **Improvement Note:** Windows is telling you a process was created, but it doesn't always mean the user manually launched it. For example, opening Chrome, running Windows services, or executing scripts all create processes. It is more accurate to say: *A new process was created under Alice's account.*

**2. Which field tells you who performed the action?**

* **Your Answer:** User field.
* **Status:**  Correct.

**3. Which field tells you when it happened?**

* **Your Answer:** Time field.
* **Status:**  Correct.

**4. Can you determine if this is malicious from this event alone?**

* **Your Answer:** *"Little because the user had create the process..."*
* **Feedback:** Your conclusion is correct, but it is best worded like this: *No. I cannot determine whether it is malicious from this event alone. Creating a new process is normal Windows behavior. I need more evidence before deciding if it is suspicious.*
* **Key Idea:** Process creation is normal. Windows creates thousands of processes every day.

**5. What additional information would you want?**

* **Your Answer:** *maybe the activity of the user after that keep tracking activity*
* **Feedback:** Excellent. This is exactly what analysts do. You could expand it slightly by checking:
* What process was created?
* Was it started by the user or automatically?
* What happened after the process started?
* Did it spawn another process?
* Was it expected for that user?
* Was it signed by a trusted publisher?
