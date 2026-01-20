# Data Leak Analysis – Least Privilege

## Incident Summary
A manager shared access to an internal folder containing confidential product plans, customer analytics, and marketing materials with their team during a meeting. Access was not revoked afterward. A sales representative later accidentally shared the internal folder link with a business partner, who publicly posted it on social media, resulting in a data leak.

---

## Issue(s): Factors That Led to the Incident
The incident occurred because the principle of least privilege was not enforced. Access to an entire internal folder was granted instead of limiting access to specific files, and permissions were not revoked after the meeting. The absence of technical controls to prevent external sharing allowed human error to cause data exposure.

---

## Review: NIST SP 800-53: AC-6 (Least Privilege)
NIST SP 800-53: AC-6 focuses on granting users only the minimum level of access required to perform their job functions. It emphasizes role-based access control, access revocation, activity logging, and regular privilege audits to reduce the risk of unauthorized access and data leaks.

---

## Recommendations: Control Enhancements
1. **Automatically revoke access** to sensitive folders after meetings or defined time periods.
2. **Restrict access based on user roles**, granting access only to specific files rather than entire directories.

---

## Justification
Automatically revoking access reduces unnecessary exposure to sensitive information after tasks are completed. Role-based access control limits the risk of accidental oversharing by ensuring users can only access what they need. Together, these controls reduce reliance on human memory and significantly lower the likelihood of future data leaks.

---

## Short Reflection
This activity reinforced how data breaches often occur due to access mismanagement rather than malicious intent. I learned that enforcing least privilege must be supported by technical controls, not just policy or user warnings. Applying NIST SP 800-53: AC-6 showed how structured access control and automation can greatly improve information privacy and reduce human error.
