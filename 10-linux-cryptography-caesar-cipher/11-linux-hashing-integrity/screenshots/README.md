# Screenshots – Linux Hashing Lab 

This folder contains screenshots documenting each step of the Linux Hashing Lab. The screenshots provide visual evidence of file inspection, hash generation, and hash comparison used to verify file integrity.

---

## Screenshot Descriptions

### 1. Directory Listing  
**File:** `step1_ls_files.png`  
Shows the contents of the `/home/analyst` directory using the `ls` command, displaying `file1.txt` and `file2.txt`.

---

### 2. Viewing File Contents  
**File:** `step2_cat_files.png`  
Displays the contents of both `file1.txt` and `file2.txt` using the `cat` command, showing that the files appear identical when viewed directly.

---

### 3. Hash Generation for File 1  
**File:** `step3_sha256_file1.png`  
Shows the execution of the `sha256sum file1.txt` command and the generated SHA-256 hash value.

---

### 4. Hash Generation for File 2  
**File:** `step4_sha256_file2.png`  
Shows the execution of the `sha256sum file2.txt` command and the generated SHA-256 hash value, which differs from file1.txt.

---

### 5. Writing Hashes to Files  
**File:** `step5_write_hash_files.png`  
Demonstrates saving hash outputs into `file1hash` and `file2hash` files and displaying their contents using the `cat` command.

---

### 6. Comparing Hash Files  
**File:** `step6_compare_hashes.png`  
Shows the use of the `cmp` command to compare the hash files byte by byte, confirming that the files differ.

---

## Purpose
These screenshots visually confirm that cryptographic hashing can detect differences between files that appear identical. Combined with the written analysis, they demonstrate practical integrity verification skills used in cybersecurity operations.
