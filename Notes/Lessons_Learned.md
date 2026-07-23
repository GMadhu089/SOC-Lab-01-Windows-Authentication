# Lessons Learned
## Lab Overview

This lab focused on investigating Windows authentication events using Splunk Enterprise.
The objective was to understand how a SOC analyst validates authentication alerts, correlates related events, and determines whether an incident is malicious or benign.

---

# Key Learnings
### 1. Validate SIEM Health First
Before investigating alerts, always verify that logs are being received correctly. Missing logs can lead to incomplete investigations and incorrect conclusions.

---

### 2. Authentication Events Tell a Story
Windows Event IDs 4624 and 4625 provide valuable context when viewed together.
Multiple failed logins followed by a successful login may indicate:

* A user entering the wrong password
* A brute-force attack
* Password spraying
* An attacker successfully guessing credentials

Correlation is essential before drawing conclusions.

---

### 3. Never Investigate a Single Event in Isolation
Every alert should be correlated with:

* Previous authentication events
* Sysmon process activity
* PowerShell execution
* User behavior
* Source IP address
* Host history

Context determines whether activity is malicious.

---

### 4. Evidence-Based Analysis
Analysts should base conclusions on collected evidence rather than assumptions.

During this lab:

* Authentication events were reviewed.
* Source information was verified.
* Related activity was investigated.
* No malicious behavior was identified.

---

### 5. Detection Engineering is Continuous
Even benign activity provides an opportunity to improve monitoring.
Recommended detection:
* Alert when five or more failed logins occur within five minutes.
* Increase severity if a successful login immediately follows repeated failures.

---

### 6. Documentation Matters
A complete incident report should include:
* Executive summary
* Timeline
* Evidence
* Root cause
* Impact
* Recommendations
* Final verdict

Clear documentation ensures other analysts can understand and validate the investigation.

---

# Skills Practiced
* Splunk SPL
* Windows Event Log Analysis
* Authentication Investigation
* Event Correlation
* Threat Hunting
* Detection Engineering
* MITRE ATT&CK Mapping
* Incident Reporting

---

# Improvements for Future Labs
* Simulate a real brute-force attack from another machine.
* Investigate PowerShell-based authentication abuse.
* Detect password spraying across multiple user accounts.
* Create dashboards for authentication monitoring.
* Build correlation searches for automated alerting.

---

# Conclusion
This lab reinforced the importance of validating authentication alerts through evidence-based analysis and event correlation. A disciplined investigation process helps SOC analysts distinguish between normal user behavior and potential attacks, reducing false positives while ensuring genuine threats are escalated appropriately.
