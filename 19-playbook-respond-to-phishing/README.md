# Phishing Incident Response – Malicious File Hash

## Overview
This project documents a phishing incident investigated from the perspective of a Level-1 Security Operations Center (SOC) analyst at a financial services organization. The incident involved a phishing email delivering a malicious executable attachment that was confirmed using SHA-256 hash analysis.

The investigation followed an established phishing response playbook to evaluate the alert, assess risk, and determine appropriate escalation.

## Incident Summary
An employee received a phishing email impersonating a job applicant. The email contained a password-protected executable attachment. The file was downloaded and opened, triggering a phishing alert. Prior threat intelligence confirmed the file’s SHA-256 hash as malicious.

Due to the confirmed malware indicator and user interaction, the alert was escalated for containment and remediation.

## Analyst Responsibilities
- Triage phishing alert
- Analyze sender details and email content
- Verify attachment via file hash
- Apply phishing response playbook
- Document findings and escalate appropriately

## Skills Demonstrated
- SOC alert triage
- Phishing analysis
- Malware identification via file hashing
- Playbook-driven incident response
- Professional incident documentation

## Outcome
**Status:** Escalated  
**Reason:** Confirmed malicious attachment with execution risk

