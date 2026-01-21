# Linux Hashing Lab – File Integrity Verification

## Overview
This project demonstrates how cryptographic hash functions are used to verify file integrity using Linux command-line tools. The lab focuses on generating SHA-256 hash values, comparing hashes, and identifying differences between files that appear identical.

Hashing is a critical security control used to detect file tampering, malware, and unauthorized modifications.

---

## Scenario
As a security analyst, I investigated whether two files were identical or different. Although the files appeared the same when viewed directly, cryptographic hashing was used to accurately verify their integrity.

---

## Objectives
- Display and inspect file contents
- Generate SHA-256 hash values
- Compare hashes manually
- Detect file differences using byte-level comparison
- Understand the role of hashing in data integrity

---

## Tools & Commands
- Linux Bash
- `sha256sum`
- `cat`
- `cmp`

---

## Project Files
- `final_hashing_lab.md` – Full lab analysis, commands, and security significance
- `step_by_step_explanation.md` – Beginner-friendly explanation of hashing concepts and commands

---

## Key Takeaway
Hashing allows security teams to detect even the smallest file changes. Files that appear identical can still be different, and cryptographic hashes provide a reliable way to verify integrity and identify tampering.
