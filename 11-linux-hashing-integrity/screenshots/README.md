# Screenshots – Linux Hashing Lab

This folder contains screenshots that visually document the key steps of the Linux Hashing Lab. Each screenshot corresponds to a major phase of the hashing and comparison process used to verify file integrity.

---

## Screenshot Descriptions

### 1. Viewing File Contents  
**File:** `step1_view_files.png`  
Shows the directory listing and the contents of `file1.txt` and `file2.txt` using the `ls` and `cat` commands. Although the files appear identical, this step demonstrates why hashing is required for accurate integrity verification.

---

### 2. Generating Hash Values  
**File:** `step2_generate_hashes.png`  
Displays the execution of the `sha256sum` command for both files. The resulting hash values are different, indicating that the files are not identical despite appearing the same.

---

### 3. Saving Hashes to Files  
**File:** `step3_save_hashes.png`  
Shows hash values being written to `file1hash` and `file2hash` and displayed using the `cat` command. This step demonstrates how hashes can be stored for later comparison.

---

### 4. Comparing Hash Files  
**File:** `step4_compare_hashes.png`  
Shows the use of the `cmp` command to compare the hash files byte by byte. The output confirms that the files differ, verifying the integrity check.

---

## Purpose
These screenshots provide visual evidence of how cryptographic hashing can detect differences between files that appear identical. Together with the written analysis, they demonstrate practical file integrity verification techniques used in cybersecurity.
