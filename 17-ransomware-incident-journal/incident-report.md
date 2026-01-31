# 🛡️ Security Incident Report – Ransomware Attack

## Incident Type
Ransomware / Phishing-Based Malware Infection

## Severity
High

## Status
Contained (Simulated Scenario)

---

## 1. Executive Summary
On Tuesday at approximately 9:00 a.m., a small U.S. healthcare clinic experienced a ransomware attack that resulted in the encryption of critical systems and files. The incident caused a complete disruption of business operations, including loss of access to patient medical records. Initial analysis indicates the attack originated from a targeted phishing email containing a malicious attachment.

---

## 2. Timeline of Events

| Time | Event |
|---|---|
| 9:00 a.m. | Employees report inability to access files and systems |
| 9:05 a.m. | Ransom note appears on affected workstations |
| 9:15 a.m. | IT team shuts down systems to prevent spread |
| 9:30 a.m. | Incident reported to external support organizations |
| Later | Phishing email identified as initial attack vector |

---

## 3. Incident Description
Multiple employees reported being locked out of their computers and unable to access essential applications. A ransom note indicated that files had been encrypted by an organized group of attackers known to target healthcare organizations. The attackers demanded payment in exchange for a decryption key.

---

## 4. Initial Attack Vector
- **Attack Type:** Phishing
- **Delivery Method:** Malicious email attachment
- **User Interaction Required:** Yes (attachment opened)
- **Result:** Malware installation and ransomware deployment

---

## 5. Affected Assets
- Employee workstations
- File servers containing patient records
- Healthcare management software
- Internal network resources

---

## 6. Impact Assessment
- **Confidentiality:** High risk due to potential exposure of patient data
- **Integrity:** Data encrypted and unavailable
- **Availability:** Critical systems rendered inaccessible
- **Operational Impact:** Clinic operations halted

---

## 7. Indicators of Compromise (IOCs)
- Presence of ransom note on infected systems
- Encrypted file extensions
- Suspicious email with malicious attachment
- Unusual system behavior following attachment execution

---

## 8. Containment Actions
- Affected systems powered down
- Network connections isolated
- Incident reported to relevant authorities and technical support
- Users instructed not to open suspicious emails

---

## 9. Root Cause Analysis
The root cause of the incident was insufficient phishing detection and user awareness. A targeted phishing email bypassed defenses and relied on human interaction to execute the malware.

---

## 10. Mitigation & Recommendations
- Implement phishing awareness training
- Enforce email attachment scanning
- Deploy endpoint detection and response (EDR)
- Regularly back up critical data offline
- Implement least privilege access controls
- Conduct regular incident response drills

---

## 11. Lessons Learned
This incident demonstrates how human factors and phishing attacks remain a primary entry point for ransomware. Strong technical controls must be paired with employee awareness to reduce risk. Early detection and rapid containment are critical to minimizing damage.

---

## 12. Analyst Notes
This incident highlights the importance of proper documentation during incident response. Maintaining a detailed incident report supports effective remediation, compliance, and future prevention strategies.

---

## Disclaimer
This report is based on a simulated scenario created for educational and portfolio purposes. No real systems or organizations were involved.

---

**Prepared by:** EzAbyss  
**Role:** Security Analyst (Portfolio Project)
