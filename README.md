# Cloud Security Capstone – SWBTL LLC (Azure IaaS Project)

This repository contains documentation, screenshots, and findings from a real-world cloud security lab project designed to secure an enterprise Azure environment for a fictional U.S. government contractor (SWBTL LLC). It was completed as part of the Cybersecurity curriculum at Western Governors University.

---

## 📌 Project Objective

To migrate SWBTL LLC from outdated leased data centers to Microsoft Azure Infrastructure-as-a-Service (IaaS) while ensuring compliance with:

- **FISMA** (Federal Information Security Management Act)  
- **PCI DSS** (Payment Card Industry Data Security Standard)  
- **NIST SP 800-53**

---

## 🔐 Key Security Configurations

### 1. Role-Based Access Control (RBAC)
- Assigned **Contributor** role to only the Marketing group within its scoped resource group.  
- Assigned **Key Vault Contributor** to Accounting users with access restricted to their vaults.  
- Audited and removed **inherited roles** at the subscription level to enforce least privilege.

### 2. Azure Key Vault Encryption
- Configured department-specific Azure Key Vaults for IT, Accounting, and Marketing.  
- Applied role-based permissions: Get, List, Create, Update (no certificate perms).  
- Used **Customer-Managed Keys (CMKs)** for encryption at rest and **TLS** for data in transit.

### 3. Backup Policy Implementation
- Created and deployed an automated backup policy (SWBTL) with:
  - Daily backups at 7:00 PM ET  
  - Retention: 3-day snapshots + 45-day daily recovery points  
- Successfully tested backup deployment on Marketing VMs.

---

## 📁 Folder Structure

/cloud-security-capstone
├── README.md
├── D485-DGN2 Task_TyraAustin.docx
├── D-485 Screenshots-CSL101.docx

---

## 🛠️ Tools & Technologies Used

- **Microsoft Azure** – IaaS, Key Vault, RBAC, Recovery Services Vault  
- **Azure Security Center** (Defender for Cloud)  
- **Windows Admin Center** (via Skillable Lab)  
- **Compliance Frameworks**: FISMA, PCI DSS, NIST SP 800-53

---

## ✅ Learning Outcomes

- Secured cloud infrastructure using Azure-native controls  
- Configured RBAC and encryption for departmental isolation  
- Implemented automated backups to support business continuity  
- Identified and mitigated misconfiguration risks and access violations  
- Applied real-world compliance standards to cloud environments

---

## 📷 Screenshots & Documentation

See the following documents for detailed work:

- `D485-DGN2 Task_TyraAustin.docx`  
- `D-485 Screenshots-CSL101.docx`

Includes:
- Role assignments  
- Key Vault configuration  
- Backup policy deployment  
- Compliance mapping

---

## 📚 References

- Microsoft Azure Docs – Key Vault, IAM, Backup  
- NIST SP 800-53  
- PCI DSS v4.0  
- (ISC)² CCSP Study Guide  
- WGU Skillable Lab environment

---

> 🎓 **Author:** Tyra Austin  
> **Program:** College of Cybersecurity, Western Governors University  
> **Date:** May 2025
