# NETWORKWALKS-B083-WK3-PM1-CYBERSECURITY-LAB-SETUP
JOHNNY RIPPER AND HASH CALCULATOR

## 📌 Project Overview

This project focuses on understanding the fundamentals of **password cracking, password security, hashing, and protected-file recovery** in a controlled cybersecurity laboratory environment.

The project contains two practical modules:

1. **Password Cracking with John the Ripper (JTR)**
2. **Password Cracking with Networkwalks Tools**

The exercises use a password-protected PDF file as the test target. The objective is to extract the password hash from the protected PDF and use authorized password-cracking tools to recover the original password.

These activities are performed strictly for **educational and authorized cybersecurity testing purposes**.

---

# 🎯 Objectives

The main objectives of this project are to:

* Understand how password cracking works.
* Understand the difference between **hashing and encryption**.
* Extract a password hash from a protected PDF.
* Use **John the Ripper** to perform password recovery.
* Use **Johnny**, the graphical interface for John the Ripper.
* Use the Networkwalks Hash Calculator.
* Use the Networkwalks Password Cracker.
* Understand how password complexity affects cracking time.
* Practice working with password hashes.
* Document cybersecurity tools and practical procedures.
* Understand why strong passwords are important.

---

# 🧪 Project Modules

| Module      | Project                                   | Tools                             |
| ----------- | ----------------------------------------- | --------------------------------- |
| 🧩 Module 1 | Password Cracking with JTR                | John the Ripper, Johnny           |
| 🧩 Module 2 | Password Cracking with Networkwalks Tools | Hash Calculator, Password Cracker |

---

# 🏗️ Lab Environment

The practical work can be performed on a **Windows PC**. The Networkwalks module can also be performed from Kali Linux because the tools operate through a web browser.

### Environment

| 🧩 Component         | ⚙️ Configuration              |
| -------------------- | ----------------------------- |
| 🖥️ Operating System | Windows                       |
| 🐉 Alternative OS    | Kali Linux                    |
| 🔐 Target            | Password-protected PDF        |
| 🛠️ JTR              | John the Ripper               |
| 🖱️ GUI              | Johnny                        |
| 🌐 Hash Tool         | Networkwalks Hash Calculator  |
| 🔓 Cracking Tool     | Networkwalks Password Cracker |

---

# 🔐 Module 1 – Password Cracking with John the Ripper

## 📖 Background

**John the Ripper (JTR)** is a password-cracking tool used by security professionals to test password strength.

According to the project material, JTR supports multiple password-hash formats and can be used with protected files such as PDF, ZIP, and Office documents. **Johnny** provides a graphical interface for John the Ripper, making the process easier for beginners.

---

## 🛠️ Tools Used

* John the Ripper
* Johnny GUI
* PDF hash extraction tool
* Notepad
* Protected PDF file

---

## ⚙️ JTR Installation

John the Ripper can be downloaded from the official Openwall website.

**Official Website:**

[https://www.openwall.com/john/](https://www.openwall.com/john/)

Johnny is the graphical interface used in this exercise.

**Johnny:**

[https://openwall.info/wiki/john/johnny](https://openwall.info/wiki/john/johnny)

The project instructions also note that **John the Ripper is available directly on Kali Linux**.

---

## 🪜 JTR Procedure

### Step 1 – Download John the Ripper

Download and install John the Ripper on the Windows system.

---

### Step 2 – Install Johnny

Install the Johnny graphical interface.

After installation:

1. Open Johnny.
2. Open **Settings**.
3. Browse to the John executable.
4. Select `john.exe`.

The `john.exe` executable is located inside the JTR `run` directory.

---

### Step 3 – Obtain the PDF Hash

Download the encrypted PDF used for the lab.

The project instructions use a PDF hash extraction tool to extract the password hash.

The extracted hash should begin with:

```text
$pdf$
```

If unnecessary characters such as:

```text
b'
```

appear at the beginning of the extracted value, they should be removed before saving the hash.

---

### Step 4 – Create the Hash File

Open Notepad and paste the extracted hash.

Save the file as:

```text
hash1.txt
```

The hash file is then used as the input for Johnny.

---

### Step 5 – Start the Attack

Open Johnny and:

1. Select **Open password file**.
2. Browse to `hash1.txt`.
3. Open the file.
4. Select **Start new attack**.

Johnny will attempt to recover the password from the supplied hash. The required time depends on system performance and password complexity.

---

### Step 6 – Open the Protected PDF

After the password has been recovered, use it to open the encrypted PDF.

The supplied project material demonstrates the recovered password as:


The PDF can then be opened using the recovered password.

---

# 🌐 Module 2 – Password Cracking with Networkwalks Tools

## 📖 Background

The second module uses two browser-based Networkwalks tools:

* **Hash Calculator**
* **Password Cracker**

The Hash Calculator extracts the password hash from the protected PDF, while the Password Cracker attempts to recover the password from that hash.

No local installation of these two tools is required because they run through a web browser.

---

## 🛠️ Tools Used

### Networkwalks Hash Calculator

[https://networkwalks.com/hash-calculator/](https://networkwalks.com/hash-calculator/)

### Networkwalks Password Cracker

[https://networkwalks.com/password-cracker/](https://networkwalks.com/password-cracker/)

---

## 🪜 Networkwalks Procedure

### Step 1 – Obtain the Protected PDF

Download the encrypted PDF supplied for the laboratory exercise.

The project material identifies the file as:

```text
My Locked PDF1.pdf
```

---

### Step 2 – Open Hash Calculator

Open the Networkwalks Hash Calculator in a web browser.

Upload:

```text
My Locked PDF1.pdf
```

The tool processes the protected PDF and generates a password hash beginning with:

```text
$pdf$
```

---

### Step 3 – Copy the Complete Hash

Copy the complete generated hash.

It is important to copy the entire value beginning with:

```text
$pdf$
```

The project instructions specifically state not to omit any portion of the hash.

---

### Step 4 – Open Password Cracker

Open the Networkwalks Password Cracker:

[https://networkwalks.com/password-cracker/](https://networkwalks.com/password-cracker/)

Paste the extracted hash into the appropriate field.

---

### Step 5 – Start the Password Attack

Start the password-cracking process.

The tool attempts different passwords until it finds a matching value.

The time required depends on the complexity of the password.

---

### Step 6 – Verify the Password

Once the password is recovered, open the protected PDF and enter the recovered password.

The supplied lab demonstrates:

```text
password1
```

as the recovered password.

---

# 🔎 Results

## Module 1 – John the Ripper

| Test                      | Result |
| ------------------------- | ------ |
| PDF hash extracted        | ✅      |
| Hash saved to `hash1.txt` | ✅      |
| Hash loaded into Johnny   | ✅      |
| Password attack started   | ✅      |
| Password recovered        | ✅      |
| Protected PDF opened      | ✅      |

### Recovered Password


```

---

## Module 2 – Networkwalks Tools

| Test                               | Result |
| ---------------------------------- | ------ |
| Protected PDF uploaded             | ✅      |
| PDF hash generated                 | ✅      |
| Complete `$pdf$` hash copied       | ✅      |
| Hash submitted to Password Cracker | ✅      |
| Password recovered                 | ✅      |
| PDF successfully opened            | ✅      |

### Recovered Password

```text
password1
```

---

# 🧠 Hashing vs Encryption

An important concept demonstrated by this project is the difference between **hashing and encryption**.

### 🔐 Encryption

Encryption is designed to protect information so that it can be recovered using the appropriate key.

```text
Plaintext
    ↓
 Encryption + Key
    ↓
Ciphertext
    ↓
Decryption + Key
    ↓
Plaintext
```

### #️⃣ Hashing

Hashing transforms input data into a hash value.

```text
Password
    ↓
 Hash Function
    ↓
Hash Value
```

The project material describes hashing as a one-way function that transforms plaintext into a message digest.

---

# 💡 What I Learned

## 1. Password Hashes

I learned that protected files can contain password-related data in a hashed form and that cracking tools can attempt to recover the original password from that data.

---

## 2. John the Ripper

I learned how John the Ripper can be used to perform password-recovery testing against an extracted hash.

---

## 3. Johnny GUI

I learned how the Johnny graphical interface simplifies interaction with John the Ripper without requiring all operations to be performed through the command line.

---

## 4. Hash Extraction

I learned that a password-protected PDF must first have its relevant hash extracted before it can be supplied to a password-cracking tool.

---

## 5. Password Complexity

The project demonstrated that password complexity affects the amount of time required to recover a password.

Simple passwords can be recovered more easily than complex passwords.

---

## 6. Security Importance

The practical demonstrated why organizations should use strong passwords and avoid predictable or commonly used credentials.

---

# 🛡️ Security & Ethical Use

This project is intended strictly for **education, cybersecurity training, and authorized security testing**.

Password-cracking tools should only be used against:

* Files you own
* Laboratory environments
* Test accounts
* Systems for which you have explicit authorization

Do not attempt to recover passwords from accounts, files, or systems belonging to other people without permission.

---

# 📸 Screenshots

The repository can include screenshots demonstrating each major stage.

Recommended structure:

---

# 📂 Repository Structure

> **Security note:** Do not upload real passwords, private credentials, personal documents, or hashes belonging to systems that are not yours.

---

# 🧰 Technologies & Tools

* 🔐 John the Ripper
* 🖱️ Johnny
* 🌐 Networkwalks Hash Calculator
* 🔓 Networkwalks Password Cracker
* 📝 Notepad
* 🐉 Kali Linux
* 🪟 Windows

---

# 📚 Key Takeaways

This project provided practical experience with:

```text
Protected PDF
      ↓
Hash Extraction
      ↓
Password Hash
      ↓
Password Cracking Tool
      ↓
Recovered Password
      ↓
PDF Verification
```

The exercise demonstrates the importance of password strength and provides hands-on experience with tools commonly used in security testing and cybersecurity education.

---

# 🔗 Resources

* **John the Ripper:** [https://www.openwall.com/john/](https://www.openwall.com/john/)
* **Johnny:** [https://openwall.info/wiki/john/johnny](https://openwall.info/wiki/john/johnny)
* **Networkwalks Hash Calculator:** [https://networkwalks.com/hash-calculator/](https://networkwalks.com/hash-calculator/)
* **Networkwalks Password Cracker:** [https://networkwalks.com/password-cracker/](https://networkwalks.com/password-cracker/)
* **Networkwalks Project Task:** [https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/](https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/)

---

# 👤 Author

**[SHREEYA ZUNJAARAO]**

Cybersecurity Student | Ethical Hacking & Cybersecurity

---

## 📌 Project Information

**Program:** Cybersecurity at Networkwalks
**Week:** 03
**Project:** Password Cracking
**Module 1:** Password Cracking with JTR
**Module 2:** Password Cracking with Networkwalks Tools
**Repository:** GitHub

---

⭐ **Educational cybersecurity project demonstrating password-hash extraction and authorized password-recovery techniques.**

Recovered Password
<CRACKED_PASSWORD>
Module 2 – Networkwalks Tools
Recovered Password
<CRACKED_PASSWORD>
🔐 Security Note

The actual password used during the laboratory exercise has intentionally not been published in this repository.

Sensitive credentials and recovered passwords should not be committed to GitHub, even when they originate from a training exercise.

Use placeholders such as:

<CRACKED_PASSWORD>
<REDACTED>
<LAB_PASSWORD>

when documenting the project publicly.
