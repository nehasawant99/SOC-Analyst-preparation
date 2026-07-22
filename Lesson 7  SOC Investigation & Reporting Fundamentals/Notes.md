# Module 1: SOC Investigation & Reporting Fundamentals

## Overview

This module ties together event analysis, user behavioural baselining, scenario-based investigation priorities, reporting, and standard operational workflows for Security Operations Centre (SOC) analysts.

> **Sample Analyst Statement**
> *"Three failed login attempts were followed by a successful login. Shortly afterwards, PowerShell was executed. This sequence requires further investigation to determine whether it represents normal user activity or suspicious behavior."*

---

## Lesson 2: User Behaviour & Baselining

Establishing a baseline means understanding what **"normal"** looks like for a user. Key questions to ask:

* [ ] **New User?** Is this user new to the environment?
* [ ] **Login Time:** Does the login time match their normal working pattern?
* [ ] **Workstation:** Is this their usual computer or device?
* [ ] **Source IP:** Is the source IP expected (e.g., corporate VPN vs. foreign IP)?
* [ ] **Privilege Level:** Is this a privileged or administrative account?
* [ ] **Historical Context:** Has this sequence of events happened before?

---

## Lesson 3: Authentication Scenarios

### Scenario A: Low Priority / Likely Benign

* **Event Sequence:** `Event 4625 (Failed)` ➔ `Event 4624 (Success)` ➔ `No further activity`
* **Likely Explanation:** Normal password mistype followed by successful login.

---

### Scenario B: High Priority / Investigation Required

* **Event Sequence:** `Event 4625` ➔ `Event 4625` ➔ `Event 4624` ➔ `New Admin Created` ➔ `PowerShell Executed`
* **Context:** Potential credential access followed by privilege escalation and command execution.

---

### Scenario C: Critical Priority / Highly Suspicious

* **Event Sequence:** `Event 4624` ➔ `Logon Type 10 (RDP)` ➔ `Scheduled Task Created` ➔ `Encoded PowerShell`
* **Context:** Potential lateral movement followed by a persistence mechanism and obfuscated payload execution.

---

## Lesson 4: Report Writing

### Example Incident Summary

> **Incident Summary:** Multiple failed login attempts were observed for the Administrator account, followed by a successful authentication. A new administrator account was created shortly afterward. Additional investigation is required to determine whether this activity was authorized.

---

## Lesson 5: Investigation Workflow

| Step | Phase | Action Details |
| --- | --- | --- |
| **1** | **Alert Generation** | Receive and trigger initial triage on SIEM / EDR alert. |
| **2** | **Review Event** | Analyse Event ID, status code, and basic metadata. |
| **3** | **Identify User** | Determine account involved and check privilege level. |
| **4** | **Check Logon Type** | Verify access vector (e.g., Type 2 Interactive, Type 3 Network, Type 10 RDP). |
| **5** | **Review Timeline** | Map actions before and after the event to build chronology. |
| **6** | **Check Related Events** | Correlate secondary logs (process creation, group changes, network connections). |
| **7** | **Collect Evidence** | Gather IPs, process paths, hashes, and user baseline data. |
| **8** | **Determine Root Cause** | Assess whether activity is True Positive (Malicious) or False Positive (Benign). |
| **9** | **Write Report** | Document summary, technical findings, and mitigation recommendations. |
