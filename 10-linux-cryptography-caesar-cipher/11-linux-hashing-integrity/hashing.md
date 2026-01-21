# Linux Hashing Lab – Creating and Comparing Hash Values

## Activity Overview
This lab demonstrates how cryptographic hash functions are used to verify file integrity. Hashing produces a unique, non-reversible value that represents file contents, allowing security analysts to detect changes, tampering, or malicious modifications.

---

## Scenario
Two files were provided that appeared identical when viewed directly. The task was to determine whether the files were truly the same by generating and comparing their SHA-256 hash values.

---

## Task 1: Inspecting File Contents
The lab started in the `/home/analyst` directory, which contained two files: `file1.txt` and `file2.txt`.

### Commands Used

    ls
    cat file1.txt
    cat file2.txt

Both files displayed the same content, demonstrating that visual inspection alone is not sufficient for verifying file integrity.

---

## Task 2: Generating Hash Values
SHA-256 hash values were generated for each file.

### Commands Used

    sha256sum file1.txt
    sha256sum file2.txt

Although the file contents appeared identical, the generated hash values were completely different. This indicates that even a small hidden difference in file data produces a drastically different hash.

---

## Task 3: Writing Hashes to Files
To enable easier comparison, hash outputs were written to separate files.

### Commands Used

    sha256sum file1.txt >> file1hash
    sha256sum file2.txt >> file2hash

The hash files were displayed using:

    cat file1hash
    cat file2hash

---

## Task 4: Comparing Hash Files
The `cmp` command was used to compare the hash files byte by byte.

### Command Used

    cmp file1hash file2hash

The output reported a difference at the first character of the first line, confirming that the files were not identical.

---

## Security Significance
This lab demonstrates why hashing is a critical security control. Cryptographic hashes allow organizations to verify data integrity, detect tampering, and identify malicious changes such as malware infections.

SHA-256 is a one-way function, meaning original data cannot be reconstructed from the hash, making it ideal for integrity validation but unsuitable for encryption or data recovery.

---

## Short Reflection
This lab reinforced the importance of using hashes rather than visual inspection to verify file integrity. I learned how even minimal changes in data can be detected using SHA-256 and how hash comparison is commonly used in malware detection and integrity monitoring.
