# Screenshots – Linux Cryptography Lab

This folder contains screenshots that visually document the steps and results of the Linux Cryptography Lab. These screenshots provide evidence of command execution, decryption processes, and successful data recovery.

## Screenshot Descriptions

### 1. Directory Enumeration  
**File:** `step1_ls.png`  
Shows the contents of the `/home/analyst` directory using the `ls` command, including the encrypted file and supporting directories.

---

### 2. Reading Instructions  
**File:** `step2_readme.png`  
Displays the contents of `README.txt`, which provides instructions to locate a hidden file and begin the decryption process.

---

### 3. Hidden File Discovery  
**File:** `step3_hidden_file.png`  
Demonstrates the use of `ls -a` inside the `caesar` directory to reveal the hidden `.leftShift3` file.

---

### 4. Caesar Cipher Decryption  
**File:** `step4_caesar_decrypt.png`  
Shows the execution of the `tr` command used to decrypt the Caesar cipher and reveal the OpenSSL decryption command.

---

### 5. File Decryption with OpenSSL  
**File:** `step5_openssl.png`  
Captures the OpenSSL command used to decrypt the encrypted file using AES-256-CBC and password-based key derivation.

---

### 6. Successful Data Recovery  
**File:** `step6_recovered_message.png`  
Shows the contents of the decrypted file (`Q1.recovered`), confirming successful recovery of the hidden message.

---

## Purpose
These screenshots complement the written analysis by providing visual confirmation of each cryptographic step. Together with the Markdown documentation, they demonstrate practical Linux and cryptography skills in a real-world security scenario.
