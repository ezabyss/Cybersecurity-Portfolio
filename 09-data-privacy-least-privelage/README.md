# Data Privacy Incident Analysis – Least Privilege (AC-6)

## Overview
This project analyzes a data leak incident at an educational technology company where confidential internal documents were unintentionally shared with an external business partner. The analysis focuses on failures in enforcing the principle of least privilege and evaluates improvements using NIST SP 800-53: AC-6.

## Scenario
An educational technology company developed an application that handles sensitive data from students, parents, instructors, and academic institutions. During a sales meeting, a manager shared access to an internal folder containing confidential product plans, customer analytics, and marketing materials. Access was not revoked after the meeting. Later, a sales representative accidentally shared the internal folder link with a business partner, who publicly posted it on social media, resulting in a data leak.

## Objectives
- Analyze how improper access control led to a data leak
- Identify failures in enforcing least privilege
- Review NIST SP 800-53: AC-6 (Least Privilege)
- Recommend control enhancements to improve information privacy
- Justify how these controls reduce future data leak risks

## Framework & Standards
- NIST Cybersecurity Framework (Protect – Data Security)
- NIST SP 800-53: AC-6 (Least Privilege)

## Files
- `data_leak_analysis.md` – Incident analysis, control review, recommendations, justification, and reflection
