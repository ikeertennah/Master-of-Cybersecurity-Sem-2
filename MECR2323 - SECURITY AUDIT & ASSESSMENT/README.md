# MECR2123 – Security Audit & Assessment 

**Semester:** 2 | **Year:** 2025/2026 | **Instructor:** Assoc. Prof. Ts. Dr. Siti Hajar Othman

---

## 🔍 Executive Summary

This repository showcases my hands-on experience in **Security Audit & Assessment**, covering the full audit lifecycle—from **research trend analysis** and **audit planning** to **ISO/IEC 27001 compliance assessment**, **risk rating**, and **external security auditing**. Through a bibliometric study, two full ISO 27001 internal audits, and a CISA CSET-based ransomware readiness assessment, I developed the practical skills required for roles in **IT Audit, Compliance, GRC, and Security Assessment**.

---

## 🎯 Core Learning Objectives

- Conduct **bibliometric analysis** using VOSviewer to visualise research trends on security audit domains.
- Plan and execute **ISO/IEC 27001 internal audits** aligned with Clauses 4–10 and Annex A controls.
- Identify and classify **Major Non-Conformities (MNC)**, **Minor Non-Conformities (mNC)**, and **Observations/OFIs**.
- Map findings to **ISO 27001 Annex A controls** and produce **corrective + preventive actions**.
- Conduct **external security audits** using ISO/IEC 27001 baseline controls.
- Build **Risk Registers** with likelihood × impact ratings and prioritised remediation.
- Use **CISA CSET** to perform Ransomware Readiness Assessments (RRA) and Cyber Infrastructure Surveys (CIS).
- Evaluate audit quality and apply **audit caveats** where evidence is self-reported.

---

## 🛠️ Tools & Technologies

| Category | Tools |
| :--- | :--- |
| **Bibliometric Analysis** | VOSviewer, Scopus Database (via PSZ), CSV/RIS Export |
| **Audit Standards** | ISO/IEC 27001:2022 (Clauses 4–10, Annex A), BNM RMiT |
| **Assessment Platform** | CISA Cyber Security Evaluation Tool (CSET) |
| **CSET Modules** | Ransomware Readiness Assessment (RRA), Cyber Infrastructure Survey (CIS) |
| **Frameworks** | NIST CSF, Cybersecurity Performance Goals (CPG), MVRA |
| **Audit Artefacts** | Audit Checklist, Risk Register, Executive Summary, Corrective Action Plan |
| **Documentation** | PowerPoint, Word, PDF, Reference Libraries (AWS, S3, Active Directory, IAM) |

---

## 📚 Key Skills Developed

### 📊 Research & Trend Analysis
- Ran Scopus searches using domain keywords (e.g., `data center AND security AND audit`).
- Exported results and imported them into **VOSviewer** for **co-occurrence analysis**.
- Generated **Network Visualisation** and **Density Visualisation** maps.
- Identified mature vs. emerging research clusters (e.g., cybersecurity, network security, AI, blockchain).

### 🔍 Audit Planning & Scoping
- Defined **audit objectives**, **scope**, **in-scope systems**, and **exclusions**.
- Selected risk-based audit domains (Risk Assessment, Access Control, Cloud Security, Supplier Management).
- Assigned **audit team roles** (Lead Auditor, Technical Auditor, Compliance Auditor, Risk Analyst).
- Built **checklists** mapping ISO 27001 baseline requirements to observed practice.

### 🛡️ ISO/IEC 27001 Internal Audit (FinSecure Bank)
- Evaluated compliance against **Clauses 6.1.2, 6.1.3** and **Annex A controls** (A.5.9, A.5.12, A.5.19, A.7.6, A.8.5).
- Classified findings as **Major NC (2)**, **Minor NC (2)**, and **Observation (1)**.
- Produced a **Key Findings Summary Table** with ISO mapping, classification, and risk level.
- Designed a **0–14 / 30 / 60-day remediation roadmap**.

### 🌐 External Security Audit (MediCare Telehealth)
- Conducted an external audit of a hospital's **telemedicine environment** against ISO 27001.
- Identified **8 key risk areas** (credential sharing, missing MFA, stale accounts, weak log review, untested backups, untested IR plan, weak vendor oversight, low awareness).
- Built a **Compliance Checklist** (Compliant / Partially / Non-Compliant) across 8 Annex A control areas.
- Produced a **Risk Register (R1–R8)** with likelihood, impact, risk rating, and mapped control gap.
- Delivered **8 prioritised recommendations** (Critical → Medium).

### 🧰 CISA CSET Assessment (National Oilwell Varco)
- Completed the **Ransomware Readiness Assessment (RRA)** across 10 goals and 3 tiers (Basic/Intermediate/Advanced).
- Completed the **Cyber Infrastructure Survey (CIS)** across 28 sections and 9 categories (0–100 scoring).
- Identified **priority gaps**: Security & Event Log, Dependencies – Data at Rest, Malicious Code Controls, Cybersecurity Training.
- Produced a **prioritised mitigation strategy** (High/Medium) with target areas.
- Flagged audit caveat that self-reported RRA (100% Yes) required independent verification.

### ⚖️ Compliance & Risk Governance
- Mapped findings to **BNM RMiT** for Malaysian financial institutions.
- Applied **ISO 27001 Annex A controls** for access control, supplier relationships, data classification, asset management, and human resource security.
- Produced **Executive Summaries**, **Conclusions**, and **Certification Readiness Statements** for senior leadership.

---

## 📂 Course Breakdown

| Component | Focus Area | Key Outcomes |
| :--- | :--- | :--- |
| **Assignment 1** | VOSviewer Research Trend Analysis | Used Scopus + VOSviewer to visualise research clusters for "Data Center Security Audit" (183 papers) and "Operating System Security Audit" (313 papers); identified mature vs emerging themes (AI, blockchain, network security). |
| **Audit Lab 1 (Internal Audit)** | FinSecure Bank ISO 27001 Internal Audit | Conducted full internal audit; identified 2 Major NC, 2 Minor NC, 1 Observation; produced Key Findings Summary, 0–60 day remediation roadmap, and executive presentation. |
| **Group Project (External Audit)** | MediCare Telehealth ISO 27001 External Audit | Audited telemedicine services; identified 8 risks; produced Compliance Checklist, Risk Register, 8 prioritised recommendations, and executive summary. |
| **Individual Audit Lab 2** | CISA CSET – RRA & CIS (National Oilwell Varco) | Completed Ransomware Readiness Assessment (100% Yes across 3 tiers) and Cyber Infrastructure Survey (28 sections); identified 4 priority gaps (logging, data-at-rest, malware controls, training) with mitigation plan. |

---

## 🏆 Spotlight #1: FinSecure Bank Internal Audit (ISO 27001)

**Format:** Group Internal Audit | **Role:** Lead Auditor

| ID | Finding | ISO Mapping | Class | Risk |
| :--- | :--- | :--- | :--- | :--- |
| F1 | MFA Failure on Root & Dev Accounts | A.8.5 | Major NC | High |
| F2 | Incomplete Third-Party Supplier Risk Assessment | A.5.19 + Clause 6.1.2 | Major NC | High |
| F3 | Delayed IAM Offboarding (30–45 days) | A.7.6 | Minor NC | Medium |
| F4 | Missing Data Classification Tags on S3 | A.5.12 | Minor NC | Medium |
| F5 | Outdated Asset Register Review (11 months) | A.5.9 | Observation | Low |

**Key Insight:** Discovering **2 Major Non-Conformities** before external certification prevented automatic audit failure—and enabled a structured 0–60 day remediation roadmap.

---

## 🏆 Spotlight #2: MediCare Telehealth External Audit (ISO 27001)

**Format:** Group External Audit | **Role:** Risk Analyst & Documentation Lead

**Top Risks Identified:**

| ID | Risk | Likelihood | Impact | Rating |
| :--- | :--- | :---: | :---: | :---: |
| R1 | Credential sharing | High | High | Critical |
| R2 | No MFA on remote access | High | High | Critical |
| R3 | Stale accounts of resigned staff | Medium | High | High |
| R4 | No formal log review | Medium | High | High |
| R5 | Untested backup restoration | Medium | High | High |
| R6 | Untested Incident Response Plan | Medium | Medium | Medium |
| R7 | Weak vendor oversight | Medium | Medium | Medium |
| R8 | Low cybersecurity awareness | Medium | Medium | Medium |

**Key Insight:** The hospital was **non-compliant in 6 of 8 ISO 27001 control areas**—but the audit provided a clear, prioritised path to full compliance.

---

## 🏆 Spotlight #3: CISA CSET Assessment (National Oilwell Varco)

**Format:** Individual Audit Lab | **Platform:** CISA CSET

**RRA Result:** 100% Yes across Basic, Intermediate, and Advanced tiers — an unusually strong self-reported result.

**CIS Result:** 28 sections scored; 4 priority gaps emerged:

| Priority | Section | Score | Risk |
| :--- | :--- | :---: | :--- |
| High | Security and Event Log | ~25 | Detection & forensics gaps |
| High | Malicious Code Controls | ~40 | Endpoint protection weaknesses |
| Medium | Dependencies – Data at Rest | ~32 | Recovery planning blind spots |
| Medium | Cybersecurity Training | ~50 | Workforce readiness gap |

**Key Insight:** A perfect RRA score can mask weaker foundational capabilities. The CIS revealed the **real investment priorities** — logging, malware controls, and data-dependency visibility.

---

## 🎓 Why This Matters

This portfolio demonstrates I can:

- **Plan and execute** ISO/IEC 27001 internal and external audits.
- **Classify findings** correctly (Major NC, Minor NC, Observation/OFI).
- **Map findings to Annex A controls** with corrective + preventive actions.
- **Build Risk Registers** with likelihood × impact ratings and prioritised remediation.
- **Use CISA CSET** for ransomware readiness and cyber infrastructure assessments.
- **Apply audit caveats** when evidence is self-reported.
- **Communicate findings** to senior leadership via Executive Summaries and remediation roadmaps.
- **Conduct bibliometric research** using VOSviewer to map domain trends.

These skills transfer directly to roles in **IT Audit, Compliance, GRC, Risk Management, Security Assessment, and Consulting**.

---

## 🔍 Reflection

This course transformed my understanding of security from **technical controls** into **governance, assurance, and evidence-based compliance**.

**Bibliometric Analysis (Assignment 1):** Using VOSviewer taught me that security research is not static—it evolves. Visualising clusters on "Data Center Security Audit" and "Operating System Security Audit" revealed that AI, automation, and blockchain are emerging themes, while network security and access control remain foundational. This is valuable context for any auditor assessing technology risk.

**Internal Audit (Lab 1):** Conducting a full ISO 27001 internal audit for FinSecure Bank was a deep dive into how compliance actually works. I learned that **clear classification matters**—calling something a "Major Non-Conformity" has real consequences (automatic audit failure). The 0–60 day remediation roadmap taught me that audits must produce **actionable, time-bound outcomes**, not just findings.

**External Audit (Group Project):** Auditing MediCare's telehealth services showed me how **regulatory context (BNM RMiT, PDPA) shapes audit priorities**. The hospital's gaps—credential sharing, no MFA, stale accounts—are common in fast-growing healthcare organisations where clinical urgency overrides security hygiene.

**CSET Assessment (Lab 2):** The CISA CSET exercise was the most eye-opening. The RRA gave 100% Yes, but the CIS revealed major weaknesses in logging and malware controls. This taught me that **self-assessments can be misleading**—and that audit quality depends on independent verification.

**Overall:** This course gave me the confidence to plan, execute, and report on security audits across industries—from banking to healthcare to oil & gas. I now understand that auditing is not about finding fault; it's about **building trust through evidence**.

