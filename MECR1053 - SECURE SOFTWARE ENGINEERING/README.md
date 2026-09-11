# MECR2323 – Secure Software Engineering 

**Semester:** 2 | **Year:** 2025/2026 | **Instructor:** Ts Dr. Mohd Zamri bin Osman

---

## 🔍 Executive Summary

This repository showcases my hands-on experience in **Secure Software Engineering**, covering the full Secure Software Development Life Cycle (SSDLC)—from **formal security requirements engineering** (Protection Profiles and Security Targets) to **automated vulnerability assessment** using SAST, DAST, and SCA tools. Through a formal security evaluation of an online banking system, a comparative analysis of open-source security testing tools, and a dual-tool assessment of a real-world PHP application, I developed the practical skills required for roles in **Application Security, DevSecOps, and Security Engineering**.

---

## 🎯 Core Learning Objectives

- Apply **Common Criteria (ISO/IEC 15408)** concepts—Protection Profiles (PP) and Security Targets (ST)—to formalise security requirements for web applications.
- Define **Security Objectives**, **Functional Security Requirements (FSRs)**, and **Non-Functional Security Requirements (NFSRs)** with measurable targets.
- Map regulatory frameworks (PDPA, BNM RMiT, PCI DSS, ISO 27001, OWASP ASVS) to security objectives.
- Select appropriate **technology stacks** with security justifications (React, Spring Boot, Auth0, PostgreSQL, AWS).
- Design **security testing plans** using SAST, DAST, SCA, penetration testing, and threat modelling (STRIDE).
- Execute **SAST (Semgrep)**, **DAST (OWASP ZAP)**, and **SCA (OWASP Dependency-Check / Trivy)** tools against real applications.
- Perform **manual verification** of tool findings (true positives vs. false positives vs. false negatives).
- Analyse **CVSS v3.1 metrics** to prioritise vulnerabilities by severity and business impact.
- Build **combined attack chains** that chain SAST + SCA vulnerabilities for maximum impact.
- Evaluate **PDPA 2024 compliance implications** and design a **Vulnerability Risk Register** for management.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Security Requirements** | Common Criteria (ISO/IEC 15408), Protection Profiles, Security Targets |
| **Standards & Frameworks** | OWASP Top 10 (2021/2025), OWASP ASVS v4.0, ISO/IEC 27001:2022, PCI DSS v4.0, BNM RMiT, PDPA 2010/2024 |
| **SAST (Static Analysis)** | Semgrep (`p/owasp-top-ten`, `p/security-audit`, `p/secrets`) |
| **DAST (Dynamic Analysis)** | OWASP ZAP (Baseline scan, Fuzzer, Automation Framework) |
| **SCA (Dependency Scanning)** | OWASP Dependency-Check v12.2.2, Trivy (filesystem, secret scanning) |
| **CVE Databases** | National Vulnerability Database (NVD), CVE Details |
| **Threat Modelling** | STRIDE |
| **Vulnerable Targets** | OWASP Juice Shop v16.0.0, DVWA, QuickDeliver PHP App |
| **Containerisation** | Docker, Docker Desktop |
| **CI/CD** | GitHub Actions, GitHub Codespaces |
| **Technology Stack** | React.js, Spring Boot, Auth0, PostgreSQL, AWS, HashiCorp Vault, ELK Stack, Snyk |

---

## 📚 Key Skills Developed

### 📋 Security Requirements Engineering (Common Criteria)
- Developed a complete **Protection Profile (PP)** for a fictional online banking system (SentinelWeb Digital Banking Portal v2.0).
- Defined **8 Security Objectives** (O.CONF, O.INTEG, O.AVAIL, O.AUTH, O.AUDIT, O.PRIV, O.NONREP, O.SESSMGMT) mapped to security principles.
- Wrote **15 Functional Security Requirements (FSRs)** with traceability to objectives (FIA_UID.1, FIA_UAU.1, FDP_ACC.1, etc.).
- Specified **8 Non-Functional Security Requirements (NFSRs)** with measurable criteria (session timeout, uptime, RTO/RPO, TLS enforcement).
- Produced a **Security Target (ST)** with PP-to-ST traceability and implemented security features.

### 🛡️ Regulatory & Framework Compliance
- Mapped **PDPA 2010** (Malaysia) to privacy objectives and data encryption requirements.
- Applied **BNM RMiT** for technology risk governance and incident response.
- Aligned **PCI DSS v4.0** for payment card data encryption and audit logging.
- Used **ISO/IEC 27001:2022** as the overarching ISMS framework.
- Applied **OWASP ASVS v4.0** for web application verification standards.

### 🏗️ Secure Architecture Design
- Selected a security-hardened **technology stack** (React.js, Spring Boot, Auth0, PostgreSQL, AWS, HashiCorp Vault, ELK Stack, Snyk, AWS WAF).
- Justified each component's security contribution (e.g., React's virtual DOM prevents XSS; Auth0 provides MFA and centralized identity).
- Designed a **containerised microservices architecture** on AWS with VPC network segregation and multi-AZ redundancy.

### 🧪 Security Testing & Automation
- Designed a **security testing plan** covering SAST, DAST, SCA, penetration testing, regression testing, and threat modelling (STRIDE).
- Executed **Semgrep SAST** scans (`p/owasp-top-ten`, `p/security-audit`) against OWASP Juice Shop (1,003 files, 225 rules, 7 findings).
- Executed **OWASP ZAP baseline scans** (9 alerts, 58 pass indicators).
- Executed **Trivy SCA/secret scans** (3 critical secrets exposed, including an RSA private key).
- Executed **OWASP Dependency-Check SCA** against QuickDeliver (283 dependencies, 38 vulnerable, 305 CVEs).

### 🔬 Manual Verification & False Positive Analysis
- Manually verified findings from Semgrep, ZAP, and Trivy to classify **True Positives vs. False Positives**.
- Identified **False Negatives** for each tool:
  - Semgrep missed SQLi authentication bypass (CWE-89) and business logic flaws.
  - ZAP baseline missed SQLi auth bypass and IDOR (no authenticated context).
  - Trivy missed dependency CVEs (ran filesystem scan, not vuln scan) and IaC misconfigurations.

### 📊 CVSS & Risk Analysis
- Analysed **CVSS v3.1 vectors** for 3 CVEs (PHPMailer CVE-2016-10033 = 9.8; Guzzle CVE-2022-31090 = 7.7; Flysystem CVE-2021-32708 = 8.1).
- Interpreted each metric (AV, AC, PR, UI, S, C, I, A) in the context of the QuickDeliver platform.
- Built a **combined attack chain** chaining SAST (Missing Auth on `adminGetOrders()`) + SCA (PHPMailer RCE) for full server compromise.
- Produced a **Vulnerability Risk Register** with 8 findings (P0–P2 priority), business impact, and remediation lookup table.

### ⚖️ Legal & Compliance Impact
- Evaluated **PDPA 2024 implications** for the QuickDeliver breach (Section 25(2) fines up to RM 1 million; Section 5 notification within 72 hours; RM 300,000 fine for non-compliance).
- Quantified **total financial impact** (~RM 16.8 million including fines, legal costs, customer churn, and remediation).

---

## 📂 Course Breakdown

| Component | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Assignment 1** | Protection Profiles & Security Targets | Developed a full PP and ST for SentinelWeb Digital Banking Portal v2.0 with Security Objectives, FSRs, NFSRs, regulatory mapping, technology stack justification, and testing plan. |
| **Final Project** | SAST & DAST Comparative Analysis | Deployed OWASP Juice Shop via Docker; executed Semgrep (SAST), OWASP ZAP (DAST), and Trivy (SCA); manually verified findings; produced a structured comparative matrix across detection accuracy, OWASP Top 10 coverage, and ease of use. |
| **Final Assessment** | QuickDeliver Security Assessment (SAST + SCA) | Performed dual-tool assessment (Semgrep + OWASP Dependency-Check) against a PHP food delivery app; analysed 5 SAST + 3 SCA findings; built a combined attack chain; evaluated PDPA implications; produced a Vulnerability Risk Register. |

---

## 🏆 Spotlight #1: Protection Profile & Security Target (SentinelWeb Banking)

**Standard:** Common Criteria (ISO/IEC 15408)

| Section | Deliverable |
| :--- | :--- |
| **Security Objectives** | 8 objectives (Confidentiality, Integrity, Availability, Authentication, Audit, Privacy, Non-Repudiation, Session Security) |
| **Functional Security Requirements** | 15 FSRs with traceability (FIA_UID.1, FIA_UAU.1, FDP_ACC.1, FCS_COP.1, etc.) |
| **Non-Functional Security Requirements** | 8 NFSRs with measurable targets (15-min timeout, 99.95% uptime, RTO < 2hr, TLS 1.2+) |
| **Regulatory Mapping** | PDPA 2010, BNM RMiT, PCI DSS v4.0, ISO 27001, OWASP ASVS v4.0 |
| **Technology Stack** | React.js, Spring Boot, Auth0, PostgreSQL, AWS, HashiCorp Vault, ELK, Snyk, AWS WAF |

**Key Insight:** Formally specifying security requirements *before* development ensures that security is a first-class citizen in the SSDLC, not an afterthought.

---

## 🏆 Spotlight #2: SAST vs. DAST vs. SCA (OWASP Juice Shop)

**Target:** OWASP Juice Shop v16.0.0 (deployed via Docker)

| Tool | Type | Findings | True Positives | False Positives |
| :--- | :--- | :---: | :---: | :---: |
| **Semgrep** | SAST | 7 | 6 | 1 |
| **OWASP ZAP** | DAST | 9 | 7 | 1 |
| **Trivy** | SCA | 3 | 1 | 2 |

**Key Insight:** No single tool provides complete coverage. SAST found hardcoded RSA keys and XSS; DAST found missing security headers; SCA found exposed secrets. **Manual verification is essential** to filter out false positives.

---

## 🏆 Spotlight #3: QuickDeliver Dual-Tool Assessment

**Target:** QuickDeliver PHP Food Delivery Platform (SAST + SCA)

**SAST Findings (Semgrep):**
| # | Vulnerability | OWASP 2025 Category |
| :--- | :--- | :--- |
| 1 | Hardcoded Secrets (DB, API, SMTP) | A02 – Security Misconfiguration |
| 2 | SQL Injection in `searchRestaurants()` | A05 – Injection |
| 3 | Reflected XSS in `searchRestaurants()` | A05 – Injection |
| 4 | Missing CSRF Token in `placeOrder()` | A01 – Broken Access Control |
| 5 | Missing Authentication in `adminGetOrders()` | A01 – Broken Access Control |

**SCA Findings (OWASP Dependency-Check):**
| Library | Version | CVE | CVSS | Severity |
| :--- | :--- | :--- | :---: | :--- |
| phpmailer/phpmailer | 5.2.16 | CVE-2016-10033 | 9.8 | CRITICAL |
| guzzlehttp/guzzle | 6.5.5 | CVE-2022-31090 | 7.7 | HIGH |
| league/flysystem | 1.1.3 | CVE-2021-32708 | 8.1 | HIGH |

**Most Dangerous Attack Chain:**
1. **Reconnaissance (SAST):** Unauthenticated access to `?action=admin` exposes all customer PII.
2. **Exploitation (SCA):** PHPMailer RCE via crafted `sender_name` parameter → PHP web shell.
3. **Impact:** Full server takeover, DB credential theft, ransomware, and regulatory fines.

**Key Insight:** SAST and SCA are **complementary, not alternatives**. One protects custom code; the other protects the software supply chain.

---

## 🎓 Why This Matters

This portfolio demonstrates that I understand **secure software engineering from design to deployment**. I can:

- **Formally specify** security requirements using Common Criteria (PP/ST).
- **Design secure architectures** with justified technology choices.
- **Execute automated security testing** using SAST, DAST, and SCA tools.
- **Manually verify findings** to eliminate false positives and identify false negatives.
- **Prioritise vulnerabilities** using CVSS and business impact.
- **Build attack chains** that combine code-level and library-level weaknesses.
- **Evaluate compliance** with PDPA, PCI DSS, ISO 27001, and OWASP ASVS.
- **Communicate findings** to management via Vulnerability Risk Registers.

These skills transfer directly to roles in **Application Security, DevSecOps, Security Engineering, Penetration Testing, and Compliance**.

---


---

## 🔍 Reflection

This course transformed my understanding of application security from a reactive, testing-only activity into a **proactive, engineering-driven discipline**.

**Security Requirements (Assignment 1):** Writing a formal Protection Profile for a banking system taught me that **clear security requirements are the foundation of a secure system**. The Common Criteria framework forced me to think about security objectives (Confidentiality, Integrity, Availability, etc.) before writing a single line of code. Mapping these to regulatory frameworks (PDPA, BNM RMiT, PCI DSS, ISO 27001) showed me that security and compliance are inseparable.

**Tool Evaluation (Final Project):** Deploying OWASP Juice Shop and running Semgrep, ZAP, and Trivy revealed the **strengths and blind spots of each tool**. Semgrep caught hardcoded RSA keys that no human reviewer would find; ZAP exposed missing security headers; Trivy flagged exposed JWT tokens in test files (false positives). The lesson: **automation amplifies humans, it doesn't replace them**.

**Dual-Tool Assessment (QuickDeliver):** The most valuable lesson came from the QuickDeliver assessment. OWASP Dependency-Check **failed to detect** two CVEs (Guzzle, Flysystem) due to incomplete CPE mappings—a real-world tooling limitation. I had to manually verify these against the NVD database. This taught me that **tool limitations are real**, and security professionals must know when to trust and when to verify.

**Overall:** This course gave me the confidence to conduct a full SSDLC assessment—from formal requirements engineering to automated testing, manual verification, risk prioritisation, and management reporting. I now understand that **secure software engineering is not a phase—it's a mindset**.


