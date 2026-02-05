> **Note:** This audit was performed as part of the Google Cybersecurity Professional Certificate.
> *(Nota: Esta auditoría fue realizada como parte del Certificado Profesional de Ciberseguridad de Google. El reporte técnico se mantiene en inglés para respetar los estándares internacionales NIST).*

---
# 🛡️ Security Audit Report: Botium Toys

## 📋 Project Description
Internal security audit for "Botium Toys", a fictional toy retailer. The goal was to assess the company's security posture, identify vulnerabilities, and recommend controls based on the **NIST Cybersecurity Framework (CSF)**.

---

## 🔍 Audit Scope & Goals
* **Scope:** Employee devices, internal network, data storage, and legacy systems.
* **Goals:** Ensure compliance with **PCI DSS** (Payment Card Industry Data Security Standard) and **GDPR** (General Data Protection Regulation).
* **Risk Assessment:** High risk due to lack of encryption and access controls.

---

## 🚩 Critical Findings (Hallazgos Críticos)
Based on the internal review and compliance checklist:

| Category | Control / Issue | Status |
| :--- | :--- | :---: |
| **Access Control** | Least Privilege Implementation | ❌ **NO** |
| **Network Security** | Firewall configured | ✅ **YES** |
| **Data Safety** | Encryption (At rest & In transit) | ❌ **NO** |
| **Compliance** | Password Policies (Complexity) | ❌ **NO** |
| **Resilience** | Disaster Recovery Plan | ❌ **NO** |
| **Physical Sec** | CCTV & Locks | ✅ **YES** |

---

## 🚀 Recommendations for Remediation
*Technical recommendations to improve security posture and achieve compliance.*

### 1. Implement Least Privilege (NIST PR.AC)
**Observation:** Currently, all employees have access to sensitive customer data and card information.
**Recommendation:** Restrict access to sensitive data (PII/SPII) to authorized personnel only. Implement **Role-Based Access Control (RBAC)** to ensure employees only access data necessary for their specific job functions.

### 2. Enable Data Encryption (PCI DSS Req 3 & 4)
**Observation:** Credit card data is stored and transmitted without encryption.
**Recommendation:** Implement **AES-256 encryption** for all sensitive data both at rest (stored) and in transit (network). This is mandatory for PCI DSS compliance.

### 3. Strengthen Password Management (NIST PR.AC)
**Observation:** Password policies are weak and not enforced centrally.
**Recommendation:** Enforce a strong password policy requiring complexity (symbols, numbers) and rotation. Implement **Multi-Factor Authentication (MFA)** for all internal systems.

### 4. Disaster Recovery Planning (NIST ID.BE)
**Observation:** No backups or recovery plans exist.
**Recommendation:** Establish a **Disaster Recovery Plan (DRP)** and schedule automated, regular **backups** of critical data. Test backups monthly to ensure integrity.

---

### 🛠️ Tools & Skills Used
* **Frameworks:** NIST CSF, PCI DSS, GDPR.
* **Methodology:** Risk Assessment, Gap Analysis, Controls Audit.
* **Author:** Jonny Lobo (IT Technician & Cybersecurity Student).
