# Findings and Recommendations  
**Internal Security Audit – Botium Toys**

---

## Purpose of This Section
This document summarizes the key findings identified during the internal security audit and provides actionable recommendations to improve Botium Toys’ overall security posture. The findings are based on the audit scope, risk assessment, and controls and compliance checklist, and are aligned with the NIST Cybersecurity Framework (CSF).

---

## Summary of Risk Levels
- **High Risk:** Immediate attention required due to potential regulatory, financial, or data exposure impact
- **Medium Risk:** Should be addressed to strengthen security maturity and reduce operational risk
- **Low Risk:** Currently acceptable but should be maintained and periodically reviewed

---

## High-Risk Findings
These issues present the greatest risk to Botium Toys and require immediate remediation.

- Customer credit card data and personally identifiable information (PII/SPII) are not encrypted
- All employees have broad access to internally stored sensitive data
- Least privilege and separation of duties have not been implemented
- No intrusion detection system (IDS) is in place
- No backups or disaster recovery plans exist for critical systems and data

---

## Medium-Risk Findings
These issues increase the likelihood of future security incidents and operational disruption.

- Password policy exists but does not meet current complexity standards
- No centralized password management system is enforced
- Legacy systems are monitored manually without a defined schedule or documented procedures

---

## Low-Risk Findings
These controls are currently effective but should continue to be reviewed regularly.

- Firewall is configured with appropriate security rules
- Antivirus software is installed and actively monitored
- Physical security controls (locks, CCTV, fire detection and prevention systems) are sufficient

---

## Recommendations

### Immediate Actions (High Priority)
The following actions should be implemented as soon as possible to reduce critical risk:

- Implement encryption for all customer credit card data and PII/SPII
- Enforce role-based access control using the principle of least privilege
- Deploy an intrusion detection system (IDS) to monitor for malicious activity
- Establish regular data backups and a documented disaster recovery plan

---

### Short-Term Actions (Medium Priority)
These improvements will enhance security operations and reduce operational risk:

- Update password policies to meet minimum complexity requirements
- Deploy a centralized password management system
- Create and document a regular monitoring and maintenance schedule for legacy systems

---

### Long-Term Actions (Low Priority)
These actions support continuous improvement and security maturity:

- Conduct regular internal security audits
- Align security controls with NIST CSF maturity levels
- Provide ongoing security awareness training for employees

---

## Expected Impact
If implemented, these recommendations will:

- Reduce the risk of data breaches and regulatory fines
- Improve compliance with PCI DSS and GDPR requirements
- Strengthen confidentiality, integrity, and availability (CIA triad)
- Improve overall organizational security posture and resilience

---

## Conclusion
This internal security audit identified several critical gaps in Botium Toys’ security controls and compliance posture. Addressing the identified risks through the recommended actions will significantly improve the organization’s ability to protect sensitive data, maintain compliance, and support secure business growth.
