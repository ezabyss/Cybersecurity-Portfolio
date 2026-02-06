# 📝 Incident Handler’s Journal — VirusTotal & Pyramid of Pain Analysis

## Entry Information
- **Date:** Feb 06, 2026  
- **Entry #:** 18
- **Incident Type:** Malicious File Execution via Email Attachment  
- **Role:** Level 1 SOC Analyst  

---

## Description
This journal entry documents the investigation of a malicious file downloaded and executed on an employee workstation. The incident involved a password-protected spreadsheet attachment delivered via email, which executed a malicious payload after being opened.

Threat intelligence analysis was performed using **VirusTotal**, and indicators of compromise (IoCs) were categorized using the **Pyramid of Pain** framework.

---

## Tools Used
- VirusTotal  
- Pyramid of Pain  
- Incident Handler’s Journal  

---

## Incident Timeline
- **1:11 p.m.** — Employee receives an email with a file attachment  
- **1:13 p.m.** — File is downloaded and opened using the provided password  
- **1:15 p.m.** — Unauthorized executable files are created on the system  
- **1:20 p.m.** — Intrusion Detection System (IDS) triggers an alert to the SOC  

---

## Artifact Analyzed
- **Artifact Type:** File (Spreadsheet attachment)  
- **Hash Algorithm:** SHA256  
- **SHA256 Hash:** `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`  

The hash was used to query VirusTotal for reputation and related threat intelligence.

---

## VirusTotal Assessment
The SHA256 hash was identified as **malicious** based on multiple detections from antivirus engines and community reports. This confirms the file is associated with known malicious activity.

---

## The 5 W’s of the Incident

### Who
An unknown threat actor distributing malicious email attachments. The activity aligns with financially motivated attackers.

### What
Execution of a malicious payload delivered via a password-protected spreadsheet attachment.

### Where
Employee workstation within a financial services organization.

### When
The incident occurred between **1:11 p.m. and 1:20 p.m.**, from email delivery to IDS alert.

### Why
The attacker leveraged social engineering and password-protected attachments to bypass basic email security controls. The objective appears to be payload execution and potential system compromise.

---

## Indicators of Compromise (Pyramid of Pain)

### Hash Values (Low Pain)
- SHA256 file hash used to identify the malicious file  
- Easily modified by attackers but useful for detection and correlation

### Network Indicators (Medium Pain)
- IP addresses or domains associated with payload delivery or command-and-control  
- Blocking disrupts attacker infrastructure but can be replaced

### Behavioral Indicators (High Pain)
- Execution of unauthorized executables after opening a document  
- Malicious process creation following user interaction  
- Harder for attackers to modify without changing attack methodology

---

## Additional Notes
- Password-protected attachments increase the likelihood of bypassing automated scanning
- Hash-based detection alone is insufficient for long-term defense
- Behavioral detection provides higher defensive value

---

## Recommendations
- Enhance email security controls and attachment scanning
- Implement behavioral detection rules for document-based payload execution
- Conduct user awareness training on phishing and password-protected attachments
- Correlate VirusTotal intelligence with internal telemetry

---

## Journal Summary
This investigation demonstrates how shared threat intelligence and structured IoC analysis help SOC analysts confirm malicious activity and prioritize detection strategies using the Pyramid of Pain.

---

**✍️ Notes By Abhishek (Ez Abyss)**
