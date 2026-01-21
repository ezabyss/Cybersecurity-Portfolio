# Linux Cryptography Lab – Decrypting Encrypted Messages

## Overview
This project demonstrates practical cryptography skills using Linux command-line tools. It focuses on breaking a classical Caesar cipher, locating hidden files, and decrypting encrypted data using OpenSSL with a modern symmetric encryption algorithm. The lab highlights how encryption protects data confidentiality and how authorized decryption is performed in real-world security workflows.

## Scenario
All files in a Linux home directory were encrypted. Acting as a security analyst, I explored the file system, identified hidden files, decrypted a Caesar cipher to obtain recovery instructions, and used OpenSSL to decrypt an AES-256-CBC encrypted file to recover the protected data.

## Objectives
- Navigate a Linux file system using Bash commands  
- Identify and read hidden files  
- Decrypt a Caesar cipher using character translation  
- Decrypt an encrypted file using OpenSSL (AES-256-CBC)  
- Understand the security implications of weak vs. strong encryption  

## Skills Demonstrated
- Linux command-line navigation  
- File and directory enumeration  
- Cryptography fundamentals  
- Caesar cipher decryption  
- OpenSSL and symmetric encryption  
- Secure handling of encrypted data  

## Tools & Technologies
- Linux Bash shell  
- ls, cat, cd, tr  
- OpenSSL  
- AES-256-CBC encryption  

## Project Files
- **linux_cryptography.md** – Full lab analysis, commands used, security significance, exemplar comparison, and reflection  

## Security Relevance
This project demonstrates why classical ciphers such as the Caesar cipher are insecure and how modern encryption standards like AES-256 provide strong data protection when implemented correctly. It also shows how security analysts can responsibly decrypt data when proper authorization and keys are available.

## Key Takeaway
Strong encryption, combined with proper key management, is essential for protecting sensitive data. This lab reinforces the importance of understanding both historical cryptographic weaknesses and modern encryption practices in cybersecurity.
