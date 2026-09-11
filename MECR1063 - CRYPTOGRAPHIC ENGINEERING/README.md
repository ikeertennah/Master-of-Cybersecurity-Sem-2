# MECR1063 – Cryptographic Engineering 

**Semester:** 2 | **Year:** 2025/2026 | **Instructor:** Dr. Muhalim Bin Mohamed Amin

---

## 🔍 Executive Summary

This repository showcases my hands-on experience in **Cryptographic Engineering**, covering the practical implementation and analysis of cryptographic primitives—from **symmetric encryption (AES)** and **key derivation (PBKDF2)** to **integrity mechanisms (CBC-MAC, HMAC)** and **randomness testing (FIPS 140-2 Monobit)**. It also includes a research project on the **impact of quantum computing on Elliptic Curve Cryptography (ECC)**. Through these labs and the project, I developed the skills required for roles in **Cryptography Engineering, Security Architecture, and Post-Quantum Cryptography Migration**.

---

## 🎯 Core Learning Objectives

- Implement symmetric encryption and decryption using **AES-256** in ECB and CBC modes.
- Apply **PBKDF2** for secure password-based key derivation with salt and iteration counts.
- Generate and verify **Message Authentication Codes (MAC)** using CBC-MAC and HMAC-SHA256.
- Evaluate **pseudo-random number generators (PRNGs)** using the **FIPS 140-2 Monobit test**.
- Analyse the **quantum threat** posed by Shor's algorithm to ECC and other public-key cryptosystems.
- Critically review **Post-Quantum Cryptography (PQC)** families (lattice-based, code-based, hash-based, isogeny-based).
- Evaluate **hybrid ECC-PQC** approaches for transitional security.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Cryptographic Libraries** | OpenSSL (AES, HMAC, PBKDF2), Python `secrets`, `hashlib` |
| **Development Environment** | Google Colab, Git Bash (MINGW64), Linux command line |
| **Cryptographic Primitives** | AES-256-ECB, AES-256-CBC, CBC-MAC, HMAC-SHA256, PBKDF2 |
| **Randomness Testing** | FIPS 140-2 Monobit Test |
| **Encoding/Decoding** | `xxd`, `hexdump`, base64 |
| **Research & Analysis** | NIST FIPS standards, NVD, academic papers on PQC |
| **Quantum Computing Concepts** | Shor's Algorithm, ECDLP, Superposition, Entanglement, QFT |

---

## 📚 Key Skills Developed

### 🔐 Symmetric Encryption & Key Derivation
- Generated AES-256 keys from hexadecimal strings using OpenSSL.
- Encrypted and decrypted files using **AES-256-ECB** with and without padding.
- Applied **PBKDF2** for secure key derivation with 1000 iterations.
- Analysed the security benefits of salt and iteration count in PBKDF2.

### 🧾 Integrity Mechanisms (MAC & Hashing)
- Generated **CBC-MAC** for a message using AES-256-CBC.
- Generated **HMAC-SHA256** using OpenSSL with a hexadecimal key.
- Compared CBC-MAC vs. HMAC in terms of security properties and use cases.
- Verified message integrity and authenticity through MAC verification.

### 🎲 Randomness Testing
- Generated 20,000-bit streams using Python's `secrets` library (OS entropy).
- Implemented the **FIPS 140-2 Monobit Test** with strict inequality condition `9725 < x < 10275`.
- Calculated statistical parameters (mean, standard deviation, confidence intervals).
- Iteratively tested streams until three successful acceptances were achieved.

### ⚛️ Post-Quantum Cryptography Research
- Analysed the impact of **Shor's algorithm** on ECC and ECDLP.
- Reviewed NIST-standardised PQC algorithms: **ML-KEM (FIPS 203)**, **ML-DSA (FIPS 204)**, **SLH-DSA (FIPS 205)**.
- Evaluated PQC families: lattice-based, code-based, hash-based, multivariate, isogeny-based.
- Assessed **hybrid ECC-PQC** approaches for transitional security.
- Identified the "Harvest Now, Decrypt Later" threat and migration urgency.

### 📊 Critical Analysis & Literature Review
- Reviewed 5 recent research papers on PQC and quantum threats.
- Synthesised findings into a critical discussion and recommendations.
- Highlighted the SIKE break as a cautionary tale for unproven PQC schemes.
- Proposed actionable insights: cryptographic inventory, NIST-FIPS compliance, hybrid TLS adoption.

---

## 📂 Course Breakdown

| Component | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Lab 1** | AES Encryption & PBKDF2 | Encrypted/decrypted files with AES-256-ECB; applied PBKDF2 key derivation with 1000 iterations; analysed security properties. |
| **Lab 2** | Integrity Mechanisms | Generated CBC-MAC and HMAC-SHA256; compared security properties; verified message integrity. |
| **Lab 3** | Randomness Testing | Implemented FIPS 140-2 Monobit test in Python; generated 20,000-bit streams; achieved 3 acceptances with counts near 10,000. |
| **Project** | Impact of Quantum Computing on ECC | Researched quantum threat to ECC; reviewed PQC families; assessed hybrid ECC-PQC; provided migration recommendations. |

---

## 🏆 Spotlight #1: AES Encryption & PBKDF2 Key Derivation

**Tools:** OpenSSL, Git Bash

- Encrypted a plaintext file using **AES-256-ECB** with a 256-bit key.
- Decrypted the ciphertext and verified the original message.
- Applied **PBKDF2** with 1000 iterations to derive a key from a password.
- Demonstrated how PBKDF2 mitigates brute-force and rainbow table attacks via salt and iteration count.

**Key Insight:** AES-ECB is not semantically secure for large data, but the lab demonstrated the core mechanics of symmetric encryption and the importance of key derivation functions.

---

## 🏆 Spotlight #2: Integrity Mechanisms (CBC-MAC & HMAC)

**Tools:** OpenSSL

- Generated a **CBC-MAC** for a message using AES-256-CBC.
- Generated an **HMAC-SHA256** using a 128-bit key.
- Compared the two: CBC-MAC relies on block cipher security, while HMAC leverages hash function properties.
- Verified that any modification to the message would invalidate the MAC.

**Key Insight:** HMAC is generally preferred for message authentication due to its provable security and resistance to length-extension attacks.

---

## 🏆 Spotlight #3: Randomness Testing (FIPS 140-2 Monobit)

**Tools:** Python (`secrets`), Google Colab

- Implemented the **Monobit test** with strict inequality `9725 < x < 10275`.
- Generated 20,000-bit streams using OS-provided entropy (`secrets.randbits`).
- Achieved 3 consecutive acceptances on first attempts:
  - Attempt 1: 9948 ones, 10052 zeros — ACCEPTED
  - Attempt 2: 10037 ones, 9963 zeros — ACCEPTED
  - Attempt 3: 9920 ones, 10080 zeros — ACCEPTED
- Calculated standard deviation (≈70.71) and confirmed the range covers ±3.89σ.

**Key Insight:** The `secrets` library produces high-quality randomness suitable for cryptographic use, as confirmed by the FIPS 140-2 Monobit test.

---

## 🏆 Spotlight #4: Quantum Impact on ECC (Group Project)

**Format:** Group Research Project | **Team Size:** 4 | **Role:** Critical Discussion & Conclusion

- Analysed the quantum threat to ECC via **Shor's algorithm**, which solves ECDLP in polynomial time.
- Reviewed NIST-standardised PQC algorithms (ML-KEM, ML-DSA, SLH-DSA).
- Evaluated hybrid ECC-PQC as a transitional strategy.
- Critically examined 5 papers, highlighting:
  - The SIKE break as a warning against unproven PQC.
  - The "Harvest Now, Decrypt Later" threat driving immediate migration.
  - The need for cryptographic dependency inventories before migration.
- Recommended: prioritise inventory, adopt NIST-FIPS standards, use hybrid TLS, and design for crypto-agility.

**Key Insight:** Organisations must begin PQC migration now—not when quantum computers arrive—to protect long-term confidential data.

---

## 🎓 Why This Matters

This portfolio demonstrates that I understand **cryptographic engineering from implementation to strategic migration**. I can:

- **Implement** symmetric encryption, key derivation, and MACs using OpenSSL and Python.
- **Test** randomness quality against FIPS 140-2 standards.
- **Analyse** the quantum threat to public-key cryptography.
- **Evaluate** PQC families and hybrid migration strategies.
- **Conduct** critical literature reviews and synthesise actionable recommendations.
- **Communicate** complex cryptographic concepts to technical and non-technical audiences.

These skills transfer directly to roles in **Cryptography Engineering, Security Architecture, Post-Quantum Migration, and Security Research**.

---


## 🔍 Reflection

This course gave me a deep appreciation for the **mathematical and practical foundations of cryptography**.

**Labs (1–3):** Implementing AES encryption and PBKDF2 taught me that cryptography is easy to misuse. Choosing the wrong mode (e.g., ECB) or weak key derivation can undermine security. Generating MACs showed me how integrity and authenticity are ensured. The randomness lab was particularly eye-opening—seeing how statistical tests validate PRNGs reinforced that cryptographic security depends on high-quality randomness.

**Project:** Researching the quantum threat to ECC was both fascinating and sobering. Shor's algorithm breaks ECDLP in polynomial time, meaning ECC will eventually be obsolete. The SIKE break during the NIST standardisation process showed that even promising PQC schemes can fail. I learned that **crypto-agility** and **early migration** are not optional—they are essential for long-term security.

**Overall:** This course equipped me with the skills to implement, test, and evaluate cryptographic systems, and to think strategically about the quantum transition. I now understand that cryptography is not just about algorithms—it's about the entire lifecycle, from key generation to retirement.


