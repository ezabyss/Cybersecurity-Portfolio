# Step-by-Step Explanation: Linux Cryptography Lab

This document explains each step of the Linux Cryptography Lab in simple terms, with special focus on understanding the `tr` and `openssl` commands used for decryption.

---

## Step 1: Listing Files in the Home Directory

The first step was to see what files existed in the home directory.

    ls

This command lists all visible files and folders. It helped identify:
- `README.txt` (instructions)
- `Q1.encrypted` (encrypted data)
- `caesar/` (a subdirectory with more clues)

---

## Step 2: Reading the Instructions File

Next, the instructions were read using:

    cat README.txt

The `cat` command displays the contents of a file.  
This revealed that a **hidden file** inside the `caesar` directory contained important information.

---

## Step 3: Finding Hidden Files

Hidden files in Linux start with a dot (`.`).  
To view them, the following command was used:

    cd caesar
    ls -a

- `cd caesar` changes into the directory
- `ls -a` lists **all files**, including hidden ones

This revealed a hidden file named `.leftShift3`.

---

## Step 4: Understanding the Caesar Cipher

The `.leftShift3` file contained scrambled text.  
This happened because it was encrypted using a **Caesar cipher**, which shifts letters in the alphabet.

Example:
- `d` becomes `a`
- `e` becomes `b`

This means every letter was shifted **3 positions to the left**.

---

## Step 5: Decrypting the Caesar Cipher (`tr` command)

The Caesar cipher was decrypted using this command:

    cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"

### Breaking this down:

### `cat .leftShift3`
Reads the encrypted text.

### `|`
This is a **pipe**.  
It sends the output of `cat` directly into the next command.

### `tr`
The `tr` command **translates characters** from one set to another.

### `"d-za-cD-ZA-C"`
This represents the **shifted alphabet**:
- lowercase: `d` through `z`, then `a` through `c`
- uppercase: `D` through `Z`, then `A` through `C`

### `"a-zA-Z"`
This represents the **normal alphabet**.

### What this means
Every shifted letter is mapped back to its original position, effectively **undoing the Caesar cipher**.

The output revealed the **OpenSSL command** needed for the next step.

---

## Step 6: Decrypting the Encrypted File (`openssl` command)

The encrypted data file was decrypted using:

    openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute

### Breaking this down clearly:

### `openssl`
A cryptographic tool used for encryption and decryption.

### `aes-256-cbc`
Specifies the encryption algorithm:
- **AES** = Advanced Encryption Standard
- **256** = key size (very strong)
- **CBC** = Cipher Block Chaining mode

### `-pbkdf2`
Adds extra security by strengthening the password into a cryptographic key.

### `-a`
Specifies Base64 encoding (used to safely store encrypted data).

### `-d`
Means **decrypt** (not encrypt).

### `-in Q1.encrypted`
Specifies the encrypted input file.

### `-out Q1.recovered`
Specifies the output file where decrypted data will be saved.

### `-k ettubrute`
The password used to decrypt the file.

---

## Step 7: Verifying Decryption

To confirm successful decryption:

    ls
    cat Q1.recovered

The presence of `Q1.recovered` and readable output confirmed that the file was successfully decrypted.

---

## Why These Commands Matter in Security

- The `tr` command demonstrates how **weak ciphers** like Caesar can be broken easily.
- The `openssl` command demonstrates how **strong encryption** protects data unless the correct key is used.
- Together, these steps show why modern cryptography is essential for protecting sensitive information.

---

## Final Takeaway

This lab shows the difference between weak historical encryption and modern secure encryption. Understanding both is important for security analysts so they can recognize vulnerabilities and properly secure data systems.
