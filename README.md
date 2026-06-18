# PCI DSS Audit Utilizing SAQ D and Merchant Level 2 Scoping

![Standard](https://img.shields.io/badge/Standard-PCI%20DSS-blue)
![Merchant Level](https://img.shields.io/badge/Merchant%20Level-2-orange)
![Validation](https://img.shields.io/badge/Validation-SAQ%20D-informational)
![Result](https://img.shields.io/badge/Result-Non--Compliant-red)

> A complete PCI DSS compliance audit of SnowBe Online, a fictional e-commerce and retail company preparing to go public. This repository documents the full engagement (planning, scoping, assessment, and final reporting) against the Payment Card Industry Data Security Standard (PCI DSS), following a single audit through its entire lifecycle.

---

## 📋 Overview

SnowBe Online processes roughly **1.2 million card transactions annually** across an AWS-hosted WordPress e-commerce platform, on-premises servers, and physical storefronts in the U.S. and Europe. Because SnowBe stores cardholder data and does not fully outsource payment processing, the environment was scoped as **PCI Merchant Level 2** and assessed against **SAQ D for Merchants**.

The audit evaluated SnowBe's ability to protect cardholder data across its full cardholder data environment (CDE), including access control, data storage and retention, patch management, and firewall configuration.

**Outcome:** Based on the assessment, SnowBe Online was found **non-compliant** with PCI DSS, with five significant findings and corresponding remediation guidance.

---

## 🎯 Objectives

- Determine whether SnowBe is compliant with PCI DSS requirements
- Assess the adequacy and effectiveness of controls protecting cardholder data
- Identify the correct merchant level and validation requirement (SAQ)
- Document findings and provide prioritized remediation guidance

---

## 📁 Repository Contents

This repository is organized by audit phase. Each phase builds on the one before it.

### 📘 01 — Case Study
- [Audit_Case_Study.pdf](./01-Case_Study/Audit_Case_Study.pdf) — the SnowBe scenario and technical environment

### 📗 02 — Audit Plan
- [Audit_Plan.pdf](./02-Audit_Plan/Audit_Plan.pdf) — objectives, scope, interviews, team structure, and tooling

### 📙 03 — Scoping
- [PCI_Audit.pdf](./03-Scoping/PCI_Audit_Scoping.pdf) — merchant level determination and SAQ selection rationale

### 📕 04 — Assessment
- [SAQ_D_v3_Merchant.pdf](./04-Assessment/SAQ_D_v3_Merchant.pdf) — completed Self-Assessment Questionnaire D

### 📒 05 — Audit Report
- [Audit_Report.pdf](./05-Audit_Report/Audit_Report.pdf) — findings, risk analysis, and remediation recommendations

---

## 🔍 Key Findings

The final report identified five areas of non-compliance:

1. **Inadequate cardholder data handling** — CHD stored in internally managed systems without consistent, role-based access restriction.
2. **No formalized patch management process** — critical patches not reliably applied within the required timeframe.
3. **Firewall configuration weaknesses** — configuration standards and network/data-flow documentation incomplete or unenforced.
4. **Weak access control and authentication** — inconsistent role-based access and use of shared credentials.
5. **No data-retention or disposal processes** — no defined policy for retaining or securely disposing of cardholder data.

Each finding includes a root-cause analysis, risk impact, and prioritized remediation guidance in the [audit report](./05-Audit_Report/Audit_Report.pdf).

---

## 🛠️ Methodology

The audit followed a structured planning approach:

- **Define objectives and scope** around all systems that store, process, or transmit cardholder data
- **Conduct role-based interviews** across end users, IT staff, management, and executives
- **Refine scope** toward the highest-risk areas (broad access, indefinite data storage, unpatched systems)
- **Assemble the audit team** by domain (network, systems/application, endpoint, audit lead)
- **Map data flows** for online, in-store, and access-control processes
- **Select tooling** — PCI requirement checklists, internal/external vulnerability scanning, configuration review, SIEM/log monitoring, and encryption/data-discovery tools

---

## 📚 Frameworks Used

- **PCI DSS** — primary audit standard (SAQ D, Merchant Level 2)
- **NIST SP 800-53** — control framework underlying SnowBe's security program
- **NIST Risk Management Framework (RMF)** — risk analysis approach

---

## 👥 Audit Team

This was a group engagement completed by an audit team:

- Kayla Hodge
- Mark VanDike
- Justin VanDrunen
- Jarred Ward
- Jordan Wicks

---

## 👤 Author

**Jarred Ward**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jarredward1)
