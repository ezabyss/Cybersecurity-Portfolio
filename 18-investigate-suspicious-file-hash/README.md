# 🧪 Threat Intelligence Analysis Using VirusTotal & Pyramid of Pain

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/76cd4c42-8cc6-47e4-ba19-b22759d9f311" />


## Overview
This lab focuses on analyzing a malicious artifact using **VirusTotal** and mapping its associated **Indicators of Compromise (IoCs)** to the **Pyramid of Pain** framework.

The activity demonstrates how security analysts leverage shared threat intelligence to evaluate file reputation, identify related indicators, and understand the defensive impact of blocking different IoC types.

---

## Scenario
You are a **Level 1 SOC Analyst** at a financial services company.

An alert was generated after an employee downloaded and opened a **password-protected spreadsheet attachment** received via email. Upon opening the file, a malicious payload executed on the system, resulting in unauthorized executable files being created.

An intrusion detection system detected the activity and alerted the SOC.

---

## Incident Timeline
- **1:11 p.m.** — Employee receives an email with a file attachment  
- **1:13 p.m.** — File is downloaded and opened using the provided password  
- **1:15 p.m.** — Multiple unauthorized executable files are created  
- **1:20 p.m.** — IDS detects suspicious activity and alerts the SOC  

---

## Artifact Details
- **Artifact Type:** File (Spreadsheet attachment)
- **Hash Type:** SHA256
- **SHA256 Hash:** `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`

The SHA256 hash serves as a unique fingerprint for identifying the file across threat intelligence platforms.

---

## Objectives
By completing this lab, I'll be able to:
- Assess whether a file hash is malicious using VirusTotal
- Identify indicators of compromise associated with a malicious file
- Classify IoCs using the Pyramid of Pain framework
- Understand the defensive value of different IoC types

---

## Tools Used
- **VirusTotal**
- **Pyramid of Pain Framework**
- Incident handler’s journal (for investigation notes)

---

## Investigation Summary
The provided SHA256 hash was searched in VirusTotal to determine its reputation and identify related indicators of compromise reported by the cybersecurity community.

The analysis focused on extracting IoCs that could be used to improve detection and response efforts.

---

## Key Findings

### File Reputation
The SHA256 hash was identified as **malicious**, with multiple detections reported by antivirus engines on VirusTotal. This confirms the file was associated with known malicious activity.

---

### Identified Indicators of Compromise (IoCs)

<img width="1600" height="845" alt="image" src="https://github.com/user-attachments/assets/826df6ef-81d4-4460-a19d-7b80c0cf762e" />

The following IoCs were identified and mapped to the Pyramid of Pain:

- **Hash Value (Low Pain)**
  - SHA256 file hash used to uniquely identify the malicious file
  - Easily changed by attackers but useful for quick detection

- **IP Address / Domain (Medium Pain)**
  - Network indicators associated with command-and-control or payload delivery
  - Blocking these disrupts attacker infrastructure but can be replaced

- **Behavioral Indicators (High Pain)**
  - Execution of unauthorized executable files after opening a document
  - Malicious behavior patterns that are harder for attackers to modify

---

## Pyramid of Pain Mapping
This investigation highlights how:
- Hash-based indicators provide fast detection but minimal disruption to attackers
- Network indicators increase attacker effort
- Behavioral indicators cause the greatest operational impact when detected and blocked

---

## Learning Outcome
This lab reinforces the importance of:
- Using threat intelligence platforms responsibly
- Understanding the limitations and strengths of different IoC types
- Applying the Pyramid of Pain to prioritize detection strategies

These skills are critical for SOC analysts performing triage, enrichment, and incident response.

---

**✍️ By Abhishek (Ez Abyss)**
