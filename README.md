# SOC Lab 01 – Windows Authentication Investigation using Splunk

## Overview

This project demonstrates the investigation of Windows Authentication events using Splunk Enterprise. The lab focuses on monitoring successful and failed login attempts, identifying suspicious authentication activity, performing threat hunting, and documenting the investigation process following a SOC Analyst workflow.

The objective is to develop practical experience in analyzing Windows Security Event Logs, understanding authentication events, writing Splunk SPL queries, and mapping findings to the MITRE ATT&CK framework.

---

## Objectives

- Investigate Windows authentication events
- Detect successful logon attempts
- Detect failed logon attempts
- Perform authentication threat hunting
- Build Splunk SPL queries
- Create basic detection logic
- Document investigation findings
- Map detections to MITRE ATT&CK

---

## Lab Environment

| Component | Technology |
|-----------|------------|
| SIEM | Splunk Enterprise |
| Operating System | Windows 11 |
| Log Source | Windows Security Event Logs |
| Event Collection | Splunk Universal Forwarder |
| Investigation Tool | Splunk Search & Reporting |

---

## Windows Event IDs Investigated

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4634 | Logoff |
| 4648 | Logon with Explicit Credentials |
| 4672 | Special Privileges Assigned |
| 4720 | User Account Created |
| 4726 | User Account Deleted |

---

## Skills Demonstrated

- Windows Authentication Analysis
- Log Analysis
- Splunk SPL
- Threat Hunting
- Security Monitoring
- Detection Engineering
- Incident Investigation
- Windows Event Log Analysis
- MITRE ATT&CK Mapping

---

## Investigation Workflow

```
User Authentication

↓

Windows Security Logs

↓

Splunk Universal Forwarder

↓

Splunk Index

↓

SPL Queries

↓

Threat Hunting

↓

Detection

↓

Incident Investigation
```

---

## SPL Queries Included

- Failed Login Detection
- Successful Login Detection
- Authentication Investigation
- User Login Statistics
- Failed Login Statistics
- Detection Rule
- Timeline Analysis

---

## Repository Structure

```
SOC-Lab-01-Windows-Authentication/
│
├── README.md
│
├── Queries/
│   ├── failed_logins.spl
│   ├── successful_logins.spl
│   └── detection_rule.spl
│
├── Reports/
│   └── Incident_Report.md
│
├── MITRE/
│   └── Mapping.md
│
└── Notes/
    └── Lessons_Learned.md
```

---

## MITRE ATT&CK Mapping

| Technique | ID | Description |
|------------|-------------|------------------------------|
| Valid Accounts | T1078 | Authentication using valid credentials |
| Brute Force | T1110 | Multiple failed login attempts |
| Account Discovery | T1087 | Enumeration of user accounts |

---

## Key Findings

- Successfully identified Windows authentication events.
- Distinguished successful and failed logins.
- Created reusable Splunk SPL queries.
- Investigated authentication activity using Windows Security logs.
- Mapped authentication events to MITRE ATT&CK techniques.
- Documented findings following a SOC investigation process.

---

## Learning Outcomes

Through this lab, I gained hands-on experience in:

- Understanding Windows authentication events
- Investigating login activity using Splunk
- Writing effective SPL queries
- Detecting suspicious authentication behavior
- Creating SOC-style investigation documentation
- Applying MITRE ATT&CK to authentication events

---

## Future Improvements

- Integrate Sysmon for endpoint visibility
- Configure PowerShell logging
- Create Splunk dashboards
- Build scheduled alerts
- Integrate Wazuh for endpoint detection
- Simulate brute-force attacks for advanced detection

---

## Tools Used

- Splunk Enterprise
- Windows 11
- Windows Event Viewer
- Splunk Universal Forwarder

---

## Author

**GAMPANAPALLI MADHU
Cybersecurity Enthusiast | SOC Analyst Aspirant | Blue Team Learner
