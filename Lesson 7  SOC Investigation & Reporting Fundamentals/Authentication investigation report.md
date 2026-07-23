# Project 1 – Authentication Investigation Report

---

### Investigation Scenario

**Date:** 22-Jul-2026

* **08:58:30**
* **Event ID:** 4625
* **User:** Administrator
* **Computer:** HR-PC-01
* **Logon Type:** 10 (Remote Desktop / RDP)
* **Description:** Failed logon


* **08:58:36**
* **Event ID:** 4625
* **User:** Administrator
* **Computer:** HR-PC-01
* **Logon Type:** 10 (Remote Desktop / RDP)
* **Description:** Failed logon


* **08:58:41**
* **Event ID:** 4625
* **User:** Administrator
* **Computer:** HR-PC-01
* **Logon Type:** 10 (Remote Desktop / RDP)
* **Description:** Failed logon


* **08:58:48**
* **Event ID:** 4624
* **User:** Administrator
* **Computer:** HR-PC-01
* **Logon Type:** 10 (Remote Desktop / RDP)
* **Description:** Successful logon


* **08:59:20**
* **Event ID:** 4688
* **User:** Administrator
* **Computer:** HR-PC-01
* **Description:** PowerShell.exe started


* **09:01:10**
* **Event ID:** 4720
* **User:** Administrator
* **Computer:** HR-PC-01
* **Description:** A new local user account was created.


* **09:03:45**
* **Source:** Windows Defender Alert
* **Computer:** HR-PC-01
* **Description:** Suspicious PowerShell behaviour detected.

---

## 1. Incident Summary

There was login by admin from pc-01-HR but got failed multiples times (3 failed login) after 4 time it got successful login into account and the timestamp where seconds difference that notice and then powershell executed and admin create a local user from pc-01-HR and then window defender alert

---

## 2. Timeline

* **08:58:30** – Failed Login admin from PC-01-HR
* **08:58:36** – Failed Login admin from PC-01-HR
* **08:58:41** – Failed Login admin from PC-01-HR
* **08:58:48** – Successful Login admin from PC-01-HR
* **08:59:20** – Powershell executed admin from PC-01-HR
* **09:01:10** – A new was created by admin from PC-01-HR
* **09:03:45** – Window Defender alert

---

## 3. Investigation

* There were multiple failure to login to account also the timestamp is seconds need investigate by see the log and gather evidence
* Then 4 time there were successful login to account and timestamp the user is same and the pc-01-hr check the pattern of work match previously
* Powershell got executed immediately after login into account if the work pattern that okay but check previously activity to verify cant conclude
* Then new user got created locally from the same pc and admin is that action necessary or work related see to that investigate and gather evidence
* Then the window defender alert the system and then why alert after new user created check the log and activity review carrefully

---

## 4. Findings

* Multiple failed logins occurred.
* Also consecutive failed login there was the successful login into account
* Also the timestamp seem suspicious but cant conclude without investigation and evidence
* The logon type was remote check that the company allow the RDP
* The admin create new user local and then window defender alert was pop then suspicious check the log and previously activity match to work style or to the user

---

## 5. Conclusion

The some factor of the event seem suspicious but cant go to conclusion of mailcoius because:

There is need more investigation and evidence such as work style and the timestamp and the powershell executed is day to day need or the window defender alerted check if was necessary and the new user create local checking the after activity of that user if seem suspicious will take appropriate action

---

## 6. Recommendations

* The Logon type was Remote then check the ip address also the same user use the laptop
* The admin login authentication logs verify
* The local user created by admin check what privilege given and check the after activity
* The window alert pop then check and log activity and commands verify it
* The user admin that normal user behaviour and see that work day to day

---

---

## Improvements list

* Keep timestamps exactly as provided (don't change them).
* Write a concise Incident Summary (2–4 lines), not every event.
* Build the timeline in chronological order.
* Focus on the sequence of events, not individual events.
* Use professional SOC terms:
* Review logs
* Verify source IP
* Analyse PowerShell activity
* Validate user activity
* Collect evidence


* Don't write "This is a cyberattack." Instead use:
* Appears unusual
* Requires further investigation
* Could indicate
* Insufficient evidence to conclude malicious activity


* Explain why each event deserves investigation.
* Mention the significance of Logon Type 10 (RDP) and verify whether remote access is authorised.
* Investigate what happened after the successful login (PowerShell → New User → Defender Alert).
* Ask why Defender generated the alert and review the related PowerShell activity.
* Verify the newly created local account (creator, privileges, and subsequent activity).
* Compare the activity with the Administrator's normal work pattern (baseline).
* Organise recommendations by priority (High, Medium, Low).
