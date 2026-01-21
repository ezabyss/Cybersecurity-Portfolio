# Linux Cryptography Lab – Decrypting an Encrypted Message

## Overview
This project documents a hands-on cryptography lab completed using Linux command-line tools. The objective was to explore an encrypted directory, break a Caesar cipher, and decrypt an encrypted file using OpenSSL. The lab demonstrates how encryption and decryption are used to protect data confidentiality and how analysts can recover data when authorized.

## Scenario
All files in a Linux home directory were encrypted. As a security analyst, I explored the file system, identified hidden files, decrypted a Caesar cipher to obtain recovery instructions, and used a modern symmetric encryption algorithm to recover protected data and reveal a hidden message.

---

## Task 1: Reading the Contents of a File
The lab started in the `/home/analyst` directory. I listed the directory contents and read the README file to obtain further instructions.

### Commands Used

    ls
    cat README.txt

The README file indicated that additional instructions were hidden within a subdirectory.

---

## Task 2: Finding and Decrypting a Hidden File
I navigated into the `caesar` subdirectory and listed all files, including hidden ones. A hidden file was discovered that contained text encrypted with a Caesar cipher.

### Commands Used

    cd caesar
    ls -a
    cat .leftShift3

The file contents were scrambled because each character was shifted three positions to the left.

### Caesar Cipher Decryption
To decrypt the message, I used the `tr` command to translate characters back to their original positions.

    cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"

This revealed the command required to decrypt the encrypted data file.

After completing this step, I returned to the home directory.

    cd ~

---

## Task 3: Decrypting the Encrypted File
Using the recovered command, I decrypted the encrypted file with OpenSSL using the AES-256-CBC algorithm and password-based key derivation.

### Decryption Command

    openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute

I then verified the decrypted file and displayed its contents.

### Verification Commands

    ls
    cat Q1.recovered

The decrypted file contained the hidden message, confirming successful data recovery.

---

## Security Significance
This lab highlights the importance of strong encryption for protecting sensitive data. Classical ciphers such as the Caesar cipher provide minimal security and are easily broken, while modern algorithms like AES-256 provide strong confidentiality when implemented correctly. The exercise also demonstrates how Linux tools can be used responsibly to decrypt data when proper authorization is available.

---

## Short Reflection
This lab strengthened my understanding of cryptography and Linux command-line operations. I learned how weak historical ciphers differ from modern encryption and how encryption protects data confidentiality in real-world systems. The activity reinforced the importance of strong cryptographic standards and proper key management in cybersecurity practice.
