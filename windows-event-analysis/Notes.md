# Module 1 – Windows Event Logs

# Understand:

- What Windows Event Logs are
- Why they exist
- How SOC analysts use them
- How to read an event
- How to investigate suspicious activity

# Lesson 1: What are Windows Event Logs?

* Imagine a company with 1,000 employees using Windows laptops.

Every second, things happen:

- A user logs in.
- Someone enters the wrong password.
- A USB device is connected.
- PowerShell runs.
- An application crashes.
- Windows installs an update.
- A service starts.
- A new user account is created.

Windows records these activities in log files. These records are called Windows Event Logs. Think of them as the operating system's diary.

# Real-world analogy

* Imagine a security guard in an office building.

Every event is written in a register:

09:00 AM
Neha entered the office.

09:10 AM
Printer room door opened.

09:15 AM
An unknown person tried entering the Server Room.

09:20 AM
Server restarted.

09:30 AM
Fire alarm tested.

That register is similar to Windows Event Logs.

A SOC analyst reads this "diary" to understand what happened on a computer.

# Why are Event Logs Important?

Without logs, you only know that "something is wrong."

With logs, you can answer questions like:

- Who logged in?
- When did they log in?
- From which computer?
- Which process started?
- Who created a new user?
- Was PowerShell executed?
- Was a service installed?
- Did someone fail to log in 100 times?

Logs provide evidence for investigations.

# Where are Windows Event Logs Stored?

Windows stores them in .evtx files.

* Common location:

C:\Windows\System32\winevt\Logs\

# Examples:

- Security.evtx
- System.evtx
- Application.evtx
- Microsoft-Windows-PowerShell%4Operational.evtx

Analysts often collect these files from endpoints during investigations.

# How Does a Log Get Created?

Here's a simplified flow:

User Action
     │
     ▼
Windows detects the action
     │
     ▼
Windows Logging Service
     │
     ▼
Event Log (.evtx)
     │
     ▼
Event Viewer / SIEM (Splunk, Microsoft Sentinel, etc.)
     │
     ▼
SOC Analyst

This is why SIEM tools are useful: they collect logs from many machines into one place.

# Types of Windows Logs

For now, focus on these three.

- Log	Purpose	Examples
- Security	Authentication and security events	Logon, logoff, account creation, failed login
- System	Operating system events	Driver issues, startup, shutdown, services
- Application	Application events	Browser crashes, database errors, software logs

We'll spend most of our time on the Security log because it's the primary source for many SOC investigations.

# What Information Does an Event Contain?

* Every event has fields such as:

- Event ID
- Date & Time
- User
- Computer
- Source
- Level
- Description

# Example:

Event ID: 4625

Time:
10:35:21 AM

User:
Administrator

Computer:
DESKTOP-01

Description:
An account failed to log on.

# This tells you:
- What happened? Failed logon.
- Who? Administrator.
- When? 10:35:21 AM.
- Where? DESKTOP-01.
- How SOC Analysts Use These Logs

# When an alert comes in, analysts ask:

- What happened?
- When did it happen?
- Who was involved?
- Which machine was affected?
- Was it successful or blocked?
- Is this normal or suspicious?

The answers usually come from Windows Event Logs.
