# SOC Evidence Table – Phishing Incident (Malicious Attachment)

## Incident Context
This evidence table documents indicators collected during the investigation of a phishing alert involving a confirmed malicious email attachment. The findings support escalation and further containment actions.

---

## Evidence Summary Table

| # | Evidence Type | Observed Indicator | Why This Is Suspicious | Risk Impact |
|---|--------------|-------------------|------------------------|------------|
| 1 | File Hash (SHA-256) | `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b` | Hash is a **known malicious indicator** verified through threat intelligence | **High** |
| 2 | Attachment Type | `bfsvc.exe` | Executable files are not typical for resumes and are commonly used to deliver malware | **High** |
| 3 | Attachment Protection | Password-protected file (`paradise10789`) | Used to evade email scanning and security controls | **High** |
| 4 | Sender Domain | `76tguyhh6tgftrt7tg.su` | Randomized domain using a TLD frequently abused in phishing campaigns | **High** |
| 5 | Sender Identity | Display name “Def Communications” vs signer “Clyde West” | Identity mismatch indicates impersonation or deception | **Medium–High** |
| 6 | IP Address Usage | `114.114.114.114`, `176.157.125.93` | Direct IP references are uncommon in legitimate corporate email infrastructure | **Medium** |
| 7 | Language Quality | Grammatical errors and misspellings (e.g., “Egnieer”) | Poor grammar is a common phishing indicator | **Medium** |
| 8 | Social Engineering Theme | Job application / resume submission | HR-related themes exploit expected attachment handling | **High** |
| 9 | Targeted Mailbox | `hr@inergy.com` | Role-based inboxes are high-value phishing targets | **High** |

---

## Analyst Assessment
The combination of a **confirmed malicious file hash**, **executable attachment**, **password-protected delivery**, and **multiple impersonation indicators** provides high confidence that this email is a phishing attempt designed to deliver malware. The evidence strongly supports escalation and immediate containment actions.

---

✍️ By Abhishek (Ez Abyss)
