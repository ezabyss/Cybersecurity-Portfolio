# Controls and Compliance Checklist  
**Internal Security Audit – Botium Toys**

This document evaluates the current state of administrative, technical, and physical security controls at Botium Toys.  
The assessment is based on the audit scope, goals, and risk assessment and aligns with the NIST Cybersecurity Framework (CSF).

---

## 🛂 Administrative Controls

Administrative controls focus on policies, procedures, and how people manage access to assets.

| Control | Implemented | Notes |
|------|------|------|
| Least privilege | ❌ No | All employees can access internally stored data, including sensitive data |
| Separation of duties | ❌ No | No role-based access restrictions are enforced |
| Disaster recovery plan | ❌ No | No disaster recovery plans or backups exist |
| Password policy | ⚠️ Partial | Policy exists but does not meet minimum complexity requirements |
| Centralized password management | ❌ No | No system enforces password policy requirements |
| GDPR breach notification plan | ✅ Yes | Plan exists to notify E.U. customers within 72 hours |
| Privacy policies & procedures | ✅ Yes | Policies are documented and enforced among employees |

---

## 💻 Technical Controls

Technical controls protect systems and data through software and hardware solutions.

| Control | Implemented | Notes |
|------|------|------|
| Firewall | ✅ Yes | Properly configured with defined security rules |
| Antivirus software | ✅ Yes | Installed and regularly monitored by IT |
| Intrusion Detection System (IDS) | ❌ No | No IDS installed to monitor suspicious activity |
| Encryption of sensitive data | ❌ No | Cardholder data and PII are stored and transmitted unencrypted |
| Data backups | ❌ No | No backups of critical data exist |
| Legacy system monitoring | ⚠️ Partial | Legacy systems are monitored, but no defined schedule or procedures |
| Secure password enforcement | ❌ No | No technical controls enforce password policy |

---

## 🏢 Physical Controls

Physical controls protect facilities and tangible assets.

| Control | Implemented | Notes |
|------|------|------|
| Door locks | ✅ Yes | Physical access to facilities is secured |
| CCTV surveillance | ✅ Yes | Surveillance systems are installed and operational |
| Fire detection & prevention | ✅ Yes | Fire alarms and prevention systems are in place |
| Warehouse security | ✅ Yes | Warehouse assets are protected by physical controls |

---

## 📜 Compliance Assessment

### 🔐 PCI DSS (Payment Card Industry Data Security Standard)

Botium Toys processes and stores payment card data.

| Requirement | Compliant | Notes |
|------|------|------|
| Restricted access to cardholder data | ❌ No | Excessive employee access exists |
| Encryption of cardholder data | ❌ No | Card data is not encrypted |
| Secure password requirements | ❌ No | Weak password enforcement |
| Secure data storage environment | ❌ No | Sensitive data stored without proper controls |

**Overall PCI DSS Risk:** 🔴 High

---

### 🌍 GDPR (General Data Protection Regulation)

Botium Toys conducts business in the European Union.

| Requirement | Compliant | Notes |
|------|------|------|
| Protection of EU customer data | ❌ No | Personal data not encrypted |
| Breach notification (72 hours) | ✅ Yes | Notification plan exists |
| Data inventory & classification | ❌ No | Assets not clearly classified |
| Privacy governance | ✅ Yes | Policies and procedures are enforced |

**Overall GDPR Risk:** 🟠 Medium–High

---

## 🧩 CIA Triad Alignment

| CIA Principle | Status | Notes |
|------|------|------|
| Confidentiality | ❌ Weak | Data access and encryption controls insufficient |
| Integrity | ✅ Moderate | Firewall and antivirus support integrity |
| Availability | ❌ Weak | No backups or disaster recovery plan |

---

## ⚠️ Summary of Control Gaps

- Excessive employee access to sensitive data
- No encryption for cardholder or customer data
- No intrusion detection capabilities
- Weak password enforcement
- No backups or disaster recovery planning
- Incomplete monitoring of legacy systems

---

## ✅ Audit Conclusion

Botium Toys has implemented some foundational security controls; however, **critical gaps remain** in access control, encryption, monitoring, and disaster recovery.  
These gaps expose the organization to **high regulatory, financial, and operational risk**.

Immediate remediation is recommended to improve compliance and strengthen the organization’s security posture.
