# Access Control Incident Analysis

## 🧾 Incident Overview
A payroll destination was added to an unknown bank account and stopped before funds were transferred. An investigation was conducted using system event logs and the employee directory to identify the cause and recommend corrective actions.

---

## 📝 Notes (Event Log & Identity Correlation)
- The payroll modification event was initiated by the account **Legal\Administrator**.
- The action originated from IP address **152.207.255.255** at **08:29:57 AM**.
- The IP address directly matches **Robert Taylor Jr.**, listed in the employee directory as a **Legal attorney (Contractor)**.
- The employee record shows an **end date of 12/27/2019**, yet administrative activity occurred in **2023**, indicating access was not revoked after contract termination.

---

## 🌐 IP Address Attribution
The source IP **152.207.255.255** is associated with a former contractor account and not an unknown external entity. This confirms the incident resulted from **internal access misuse due to improper access lifecycle management**, rather than an external network intrusion.

---

## ⚠️ Access Control Issues Identified
- **Failure to revoke access**: Contractor accounts remained active well beyond recorded end dates.
- **Excessive privileges**: A legal contractor retained **admin-level authorization**, including payroll modification capabilities.
- **Lack of segregation of duties**: Payroll functions were accessible to non-finance roles.
- **Insufficient monitoring**: A high-risk payroll change was logged as informational with no alert escalation.

---

## ✅ Recommended Mitigations
1. Enforce **Role-Based Access Control (RBAC)** to restrict payroll and banking actions exclusively to finance roles.
2. Implement **automated access revocation** tied to employee end dates and contract termination.
3. Require **multi-factor authentication (MFA)** for all administrative and financial system actions.
4. Enable **high-severity alerts** for payroll destination changes and external bank account modifications.
5. Conduct **quarterly access reviews** to identify and remove dormant or excessive privileges.

---

## 🧠 Justification
Restricting privileges and enforcing automated offboarding directly reduces the risk of insider misuse and credential abuse. Enhanced monitoring and alerting ensure high-impact financial actions are detected early, preventing fraud and maintaining operational integrity.

---

## 🔍 Root Cause Summary
The incident was caused by **inadequate access lifecycle management**, allowing a former contractor to retain administrative privileges long after their employment ended.

---
## 👥 Access Control Observations

A review of the employee directory revealed that **all listed users**, including part-time staff, seasonal employees, contractors, and non-technical roles, were assigned **admin-level authorization**. This includes roles such as graphic designer, sales associate, marketing, and manufacturer, which do not typically require administrative privileges.

Additionally, multiple users with **employment end dates in the past** retained active administrative access, indicating a lack of periodic access reviews and ineffective offboarding procedures. The widespread use of admin privileges significantly increases the organization’s attack surface and elevates the risk of accidental misuse, insider threat, or credential compromise.


## 🏁 Conclusion
This investigation highlights how weak authorization controls and poor account governance can enable serious financial risk. Strong least-privilege enforcement, timely access revocation, and continuous monitoring are essential to preventing similar incidents.
