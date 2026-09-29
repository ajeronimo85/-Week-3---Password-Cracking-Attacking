# 🔐 Week 3 — Password Cracking & Dictionary Attacks

## 📋 Project Overview

**Week 3** of the NetworkWalks Cybersecurity Program focuses on **Phase 3 of the Ethical Hacking Lifecycle: Gaining Access** through controlled password-cracking and dictionary-attack techniques.

The project involved extracting cryptographic hashes from password-protected PDF documents and performing controlled password-recovery attacks using **John the Ripper (JtR)**, **Johnny GUI**, and **NetworkWalks Online Cracking Tools & Wordlist Generators**.

The exercises demonstrate practical skills in:

* 🔑 Password hash extraction and analysis
* 📚 Dictionary-based password attacks
* 🧬 Custom wordlist generation
* 🔄 Password mutation techniques
* 🛠️ John the Ripper (JtR) and Johnny GUI
* 🧪 Controlled password-recovery testing
* 📄 PDF password-protection analysis
* 📝 Technical documentation and reporting

> **⚠️ Disclaimer:** All activities documented in this project were performed in authorized laboratory/CTF environments for cybersecurity training and educational purposes.

---

## 📦 Project Modules & Status

| Module           | Module Name                               | Category  | Scope                                                                                   | Status        |
| ---------------- | ----------------------------------------- | --------- | --------------------------------------------------------------------------------------- | ------------- |
| **W3-PM1**       | Password Cracking with JtR                | Essential | Cracking authorized password-protected PDF targets using John the Ripper and Johnny GUI | ✅ Completed   |
| **W3-PM2**       | Password Cracking with NetworkWalks Tools | Essential | Hash analysis, dictionary attacks, and custom wordlist generation                       | ✅ Completed   |
| **W3-OPTIONAL1** | AI-Assisted JtR Lab                       | Optional  | Exploring AI-assisted workflows using Claude Desktop and HexStrike MCP                  | 📝 Documented |
| **W3-OPTIONAL2** | Mediroza Hospital Portal Lab              | Optional  | Authorized CTF-style credential attack simulation                                       | 📝 Documented |

---

# 🎯 Lab Targets & Results

The following authorized PDF targets were used to evaluate different password-cracking approaches.

| Target               | Format / Encryption   | Hash Type          | Attack Method                                 | Result             | Verification   |
| -------------------- | --------------------- | ------------------ | --------------------------------------------- | ------------------ | -------------- |
| `My Locked PDF1.pdf` | PDF 1.4 / 128-bit RC4 | `$pdf$4*4*128*...` | JtR Default Dictionary / NetworkWalks Cracker | Password recovered | ✅ PDF unlocked |
| `My Locked PDF2.pdf` | PDF 1.4 / 128-bit RC4 | `$pdf$4*4*128*...` | Custom Generated Wordlist                     | Password recovered | ✅ PDF unlocked |
| `My Locked PDF3.pdf` | PDF 1.4 / 128-bit RC4 | `$pdf$4*4*128*...` | Targeted 1,987-word list                      | Password recovered | ✅ PDF unlocked |

> 🔒 **Credential Note:** Recovered plaintext passwords are intentionally omitted from this public README. Evidence and passwords can be maintained in the private lab report or screenshots where appropriate.

---

# 🔓 W3-PM1 — Password Cracking with John the Ripper & Johnny GUI

## 🛠️ Tools Used

* **John the Ripper v1.9.0 Jumbo**
* **Johnny GUI v2.2**
* **Cygwin 64-bit**
* **x86_64 AVX2**
* PDF hash extraction tools
* Dictionary/wordlist files

  ## 🧪 Task 1: Cracking "My Locked PDF1"
Hash Extraction: Generated the $pdf$ hash string from My Locked PDF1.pdf and saved it to My Locked PDF1-Hash Value.txt.
Johnny Configuration: Loaded JTR engine path and imported the hash into Johnny.
Attack Execution: Launched dictionary attack - JTR cracked the hash in seconds.
Validation: Opened PDF with recovered password good-luck to reveal the secret flag.

![](4-screenshot-curl.png)



