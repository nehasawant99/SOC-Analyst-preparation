# Mini Exercise 1 – Review

### Scenario

* **08:45 AM:** User: Alice — Event ID: 4624
* **Context:** Alice logs into her office computer before work starts.

---

### Questions & Answers

**1. What happened?**

* **Your Answer:** Alice successfully logged into her office computer before work started.
* **Status:**  Correct

**2. Is this normal or suspicious?**

* **Your Answer:** It could be suspicious, but I cannot conclude that from this event alone. I need more information to determine whether the login is expected or unusual.
* **Status:**  Good answer.

> **Why?**
> This is the key lesson: Just because someone logs in before work starts doesn't automatically make it suspicious.
> **Possible normal reasons:**
> * Alice starts work early.
> * She has a flexible schedule.
> * She is working overtime.
> * She is preparing for a meeting.
> * She is working remotely.
> 
> 
> **Or...** Someone else is using her account. We don't know yet.

**3. Would you investigate further?**

* **Your Answer:** Yes. I would collect more evidence, such as whether Alice was the person who logged in, the source IP address, the computer used, and whether this login matches her normal activity.
* **Status:**  Excellent.

**4. Why?**

* **Your Answer:** Because the login happened before work started. I would investigate whether this is normal for Alice or if it is unusual. I need to gather more data and evidence before concluding.
* **Status:**  Correct.

---

# Mini Exercise 2 – Review

### Scenario

```
02:15 AM ──> User: Administrator ──> Event ID: 4624 (Successful Login)
                 │
                 ▼
02:20 AM ──> A new local administrator account is created.

```

---

### Questions & Answers

**1. What happened?**

* **Answer:** The Administrator account successfully logged in at 2:15 AM. A few minutes later, a new local administrator account was created.
* **Status:**  Correct

**2. Is this enough to conclude it is an attack?**

* **Answer:** No. The activity appears suspicious because the login happened at 2:15 AM and was followed by the creation of a new administrator account. However, I cannot conclude it is an attack without collecting more evidence. I would first check whether this is normal activity for the Administrator account.
* **Status:**  Excellent

**3. What would you investigate next?**

* **Answer:** I would investigate:
* The activity performed by the Administrator account after login.
* The newly created administrator account.
* The source IP address.
* The computer used for the login.
* Whether this activity matches the user's normal work pattern.


* **Status:**  Very good investigation plan.

**4. Why is the timeline important?**

* **Answer:** The timeline helps me understand the sequence of events. A login at 2:15 AM may be unusual unless the user works night shifts or has scheduled maintenance. The creation of a new administrator account shortly after the login makes the activity more suspicious. I would collect more evidence before reaching a conclusion.
* **Status:**  Excellent
