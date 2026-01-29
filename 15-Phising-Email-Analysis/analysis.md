# Phishing Email Investigation – Executive Targeting (Spear Phishing)

## 📌 Overview
This project documents the investigation of a suspected spear phishing email received by an executive at **Imaginary Bank**. The email impersonates a trusted internal source and attempts to trick the recipient into installing unauthorized collaboration software. The goal of this analysis is to identify phishing indicators, assess risk, and determine the appropriate security response.

---

## 🎯 Investigation Objective
- Determine whether the email is legitimate or malicious  
- Identify social engineering techniques used by the attacker  
- Evaluate risks posed to the organization  
- Decide whether the email should be **allowed or quarantined**

---

## 🧾 Email Metadata Analysis

| Field | Observed Value | Security Concern |
|-----|---------------|------------------|
| **From** | imaginarybank@gmail.org | Uses a personal domain instead of official corporate domain |
| **To** | cfo@imaginarybank.com | High-value executive target |
| **Sent** | Saturday, Dec 21, 2019 | Unusual timing for board communication |
| **Subject** | “RE: You are been added to an ecsecutiv's groups” | Grammar errors, misleading “RE:” prefix |

### 🔍 Key Red Flags
- Personal email domain used for corporate instructions  
- Spoofed sender name implying internal authority  
- Poor grammar inconsistent with board-level communication  

---

## 🧠 Social Engineering Techniques Identified

The email employs multiple social engineering tactics designed to pressure the recipient:

- **Authority impersonation**: Claims to originate from the board
- **Urgency**: “This invitation will expire in 48 hours”
- **Fear of exclusion**: “Your team needs you!”
- **Trust abuse**: Uses corporate branding and familiar language

These techniques increase the likelihood of user compliance without verification.

---

## ✉️ Message Body Analysis

| Indicator | Evidence |
|---------|---------|
| Spelling & grammar errors | “Conglaturations”, “Downlode”, “You’re team” |
| Unverified software | ExecuTalk not mentioned in any prior meetings |
| Generic signature | No employee name or contact details |
| Broad platform links | Mac, Windows, Android links in same message |

These characteristics strongly indicate a phishing attempt rather than legitimate internal communication.

---

## 🔗 Download & Link Investigation

All three download options redirect to the same external login page:

    my.site.net/pwnexecs/


### 🚨 Security Findings
- Domain is **not owned by Imaginary Bank**
- URL structure suggests malicious intent (`/pwnexecs/`)
- Fake login page designed to harvest credentials
- HTTPS presence alone does **not** imply legitimacy

This is consistent with **credential harvesting phishing attacks**.

---

## ⚠️ Risk Assessment

| Risk Area | Impact |
|---------|--------|
| Credential compromise | Executive account takeover |
| Privilege escalation | Access to sensitive financial data |
| Lateral movement | Further phishing or malware deployment |
| Business impact | Financial fraud, reputational damage |

Because the target is a senior executive, the potential impact is **high**.

---

## ✅ Final Determination

**Decision:** 🚫 **QUARANTINE EMAIL**

### Justification:
- Clear evidence of spear phishing
- Malicious external domain
- Credential harvesting attempt
- Executive-level targeting increases risk severity

---

## 🛡️ Recommended Security Controls

- Enforce **email filtering and domain reputation checks**
- Implement **mandatory security awareness training**
- Require **multi-factor authentication (MFA)** for executives
- Establish a **verified software approval process**
- Encourage **immediate reporting** of suspicious emails

---

## 📚 Key Takeaways
This investigation demonstrates how phishing attacks exploit trust, urgency, and authority rather than technical vulnerabilities alone. Effective defense requires layered controls, user awareness, and strong incident response procedures—especially for high-value targets.

---

## 🔗 References
- Social Engineering & Phishing Detection Best Practices  
- Executive Email Security Controls  
- Credential Harvesting Attack Patterns
