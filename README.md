# ServiceNow SOC Incident Triage & ITIL Lifecycle Portfolio

## Overview
This portfolio demonstrates hands-on experience as a **Tier 1 SOC Analyst** performing security incident triage, classification, and workflow management within an enterprise **ServiceNow ITIL environment**. 

Across **18 distinct security incidents** (`INC0010001`–`INC0010018`), I simulated the end-to-end incident response lifecycle—from initial threat detection and Level 1 containment to cross-functional escalations, dependency holds, and mandatory ITIL resolution logging.

---

## Key Skills & Competencies
* **Security Incident Analysis:** Triage of Phishing, SQL Injection, Credential Dumping (LSASS), Living-off-the-Land (LotL) PowerShell, Ransomware Indicators, Rogue Access Points, and Insider Exfiltration.
* **ServiceNow & ITIL Lifecycle Management:** Execution of standard ITIL ticket states—`New`, `In Progress`, `On Hold` (Awaiting Caller / Vendor), `Resolved`, `Closed`, and `Canceled`.
* **Standardized Documentation:** Structured Level 1 SOC Triage Summaries inside internal **Work Notes**, customer-facing communications via **Additional Comments**, and audit-compliant resolution entries.
* **Escalation & Routing:** Category classification and routing across enterprise assignment groups (**Software**, **Hardware**, **Network**, **Database**).

---

## 📸 Portfolio Evidence
<img width="1876" height="961" alt="image" src="https://github.com/user-attachments/assets/33c3adcc-c493-4c21-bfc3-44af36acf376" />



1. **Incident Queue Overview:** Showing tickets `INC0010001` through `INC0010018` with active state transitions and assignment groups.
2. **Detailed Incident View:** Example showing populated **Work Notes**, **Category/Assignment**, and **Resolution Information**.

---

## 📊 Incident Triage Matrix

| Incident ID | Threat / Alert Type | Category | State | Assignment Group | Core Action Taken |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **INC0010001** | EICAR Test File Detection | Software | Resolved | Software | True Positive (Test). File quarantined by AV agent; endpoint clean. |
| **INC0010002** | Credential Harvesting Phishing | Security | Resolved | Network | Blocked phishing URL on Perimeter Gateway; purged email from mailboxes. |
| **INC0010003** | Suspicious PowerShell Execution | Software | In Progress | Software | Initiated host isolation; dumped memory via EDR for Tier 2 analysis. |
| **INC0010004** | Unauthorized Admin Password Reset | Software | On Hold | Software | On Hold (Awaiting Caller). Validated identity before closing ticket. |
| **INC0010005** | Unauthorized Port Scan | Network | Resolved | Network | Internal IP identified as security scanner; closed as authorized activity. |
| **INC0010006** | Authorized Vulnerability Test | Network | Canceled | Network | Canceled. Verified ticket was created during pre-approved penetration test. |
| **INC0010007** | WAF Blocked SQL Injection | Software | Resolved | Software | Source IP added to perimeter blocklist; payload blocked by WAF. |
| **INC0010008** | Cobalt Strike Beaconing | Network | In Progress | Network | Isolated workstation; revoked Kerberos ticket granting tokens (TGT). |
| **INC0010009** | Impossible Travel Anomaly | Security | On Hold | Network | On Hold (Awaiting Caller). Flagged concurrent logins; MFA re-challenge issued. |
| **INC0010010** | Database Privilege Escalation | Database | Resolved | Database | Revoked unauthorized DBA privileges; patched MySQL service account. |
| **INC0010011** | Credential Dumping (LSASS) | Hardware | In Progress | Hardware | Suspended malicious process tree; isolated host via EDR. |
| **INC0010012** | Phishing Payload / Macro Execution | Software | Resolved | Software | Weaponized document purged; host reimaged per SOC playbook. |
| **INC0010013** | Mass Ransomware File Renaming | Hardware | In Progress | Hardware | Disconnected network share; terminated unauthorized encryption process. |
| **INC0010014** | Scheduled Backup Task | Inquiry / Help | New | (empty) | New alert logged; pending initial SOC assignment and review. |
| **INC0010015** | Rogue Wireless Access Point | Network | Resolved | Network | Unsanctioned travel router physically removed; switch port disabled. |
| **INC0010016** | Zero-Day SaaS API Exploit | Software | On Hold | Software | On Hold (Awaiting Vendor). Disabled API integration; logged vendor ticket. |
| **INC0010017** | SSH Brute-Force / Password Spray | Database | Resolved | Database | Attacking IP blocked at firewall; forced SSH key authentication across cluster. |
| **INC0010018** | Mass Cloud Data Exfiltration | Network | Closed | Network | Revoked Okta tokens; blocked transfer at Web Gateway; escalated to HR/Legal. |

---

## 📋 Standardized Level 1 SOC Triage Template

All incidents in this repository were documented using the following structured Level 1 Work Note framework:

```text
[SOC Triage Summary - Level 1 Analysis]
* Alert Type: [Specific Alert / Event]
* Finding: [Brief description of anomalous activity observed]
* Context Check: [Historical analysis, user activity context, change tickets]
* Verdict: [True Positive / False Positive / Authorized Test]
* Immediate Action Taken: [Containment, block, escalation, or hold reason]
