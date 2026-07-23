# SOC Investigation Reports & Practice Labs

This folder contains hands-on Security Operations Centre (SOC) investigation reports, scenario walkthroughs, and Windows Event Log analysis. The goal of these labs is to practice real-world incident response workflows, user baselining, threat identification, and technical report writing.

---

##  Investigation Framework

Each report in this repository follows a standard SOC reporting template:

1. **Incident Summary:** Brief high-level overview of the activity.
2. **Timeline:** Chronological mapping of logs and alerts with exact timestamps.
3. **Investigation:** Deep-dive analysis into user baseline, logon types, and event sequences.
4. **Findings:** Key technical observations (IP addresses, processes, event IDs).
5. **Conclusion:** Assessment of threat level (True Positive vs. False Positive).
6. **Recommendations:** Prioritised next steps and remediation actions.

---

## 📂 Practice Labs & Case Studies

| Report ID | Topic / Scenario | Primary Focus | Status |
| --- | --- | --- | --- |
| **Project 01** | Authentication & Persistence | Failed Logons (4625), RDP (Type 10), PowerShell Execution, Defender Alert | Completed |
| **Project 02** | *[Next Scenario]* | *[e.g.,..]* | In Progress |

---

##  SOC Analyst Skill Tracking & Improvement Ledger

Use this section to track key investigative skills to master across all practice reports.

### Improvements list: Analysis & Technical Skills

*  **Logon Type Identification:** Quickly map Logon Types (e.g., Type 2 Interactive, Type 3 Network, Type 10 RDP) to access vectors.
*  **Event Correlation:** Link authentication logs (`4625`, `4624`) with process creation (`4688`) and account management (`4720`).
*  **Baselining:** Always compare observed actions against normal working hours, hostnames, and user roles before jumping to conclusions.
*  **Evidence Collection:** Identify missing data points needed for full analysis (Source IP, command-line arguments, file hashes).

### Checklist: SOC Report Writing

*  **Objective Language:** Avoid absolute claims like *"This is a cyberattack."* Use precise language like *"Appears unusual,"* *"Could indicate,"* or *"Requires further investigation."*
*  **Concise Summaries:** Keep Incident Summaries strictly within 2–4 lines.
*  ** Prioritised Actions:** Categorise recommendations clearly based on risk and urgency.

---
### Key takeaways:
> This is for learning and educational purposes to understand, learn and build skills.
