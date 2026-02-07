# Incident Analysis – Phishing with Malicious File Hash

## Alert Context
A phishing alert was generated after an employee received and interacted with an email containing a suspicious attachment. The message claimed to be a job application and attempted to appear legitimate through impersonation and urgency.

The attachment was identified as an executable file disguised as a resume and protected with a password to bypass email security controls.

## Indicator Analysis
The file attachment (`bfsvc.exe`) was analyzed using its SHA-256 hash. The hash matched a known malicious indicator based on prior threat intelligence. Hash-based validation confirms malicious intent without requiring execution of the file.

Executable attachments delivered via unsolicited email represent a high-risk attack vector commonly used to deploy malware such as loaders or trojans.

## Sender & Content Assessment
Multiple phishing indicators were observed:
- Sender domain unrelated to the organization
- Mismatch between sender display name and email address
- Grammatical errors in subject and message body
- Use of a password-protected executable file

These indicators align with common social engineering techniques used in phishing campaigns.

## 5W Summary
- **Who:** External threat actor impersonating a job applicant
- **What:** Phishing email with malicious executable attachment
- **When:** During business hours
- **Where:** HR mailbox and employee workstation
- **Why:** Attempt to deliver malware via social engineering

## Escalation Rationale
The alert was escalated because:
- The attachment hash is confirmed malicious
- The file type is executable and user interaction occurred
- The email exhibits multiple phishing indicators
- Malware execution could result in system compromise

Escalation enables containment actions such as endpoint isolation, credential review, and organization-wide IOC correlation.
