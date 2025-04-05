# Identity Auditing, Governance, and Lifecycle Management Notes (SC-300)

This document outlines key concepts related to **auditing**, **governance**, and **identity lifecycle management** in Microsoft Entra ID (formerly Azure AD), aligned with SC-300 exam objectives.

---

## 🔍 Auditing in Identity Solutions

### ✅ Why Auditing Matters
- Detect attacks (in progress or past).
- Ensure regulatory **compliance**.
- Provide **accountability** (who did what and when).
- Help **developers debug** access issues.

### 📝 What Can Be Audited?
- Sign-ins  
- Password changes  
- MFA configurations and usage  
- Admin operations  
- Role assignments  
- App access attempts

### 🧾 Types of Logs in Microsoft Entra ID
| Log Type | Description |
|----------|-------------|
| **Audit Logs** | Track changes to resources (e.g., user creation, group updates). |
| **Sign-in Logs** | Track login attempts, locations, devices, and outcomes. |
| **Provisioning Logs** | Show sync activity from systems like HRIS to Entra ID. |
| **Activity Logs** | Broader operational logs from the identity platform. |

### 🔧 Monitoring Tools
- Azure Monitor  
- Microsoft Sentinel  
- Log Analytics  
- Workbooks  
- Azure Alerts

---

## 🛡️ Governance in Identity Solutions

### 📘 Definition
> Governance is the act of overseeing and controlling systems to ensure they function securely and efficiently.

### 🧠 Scenario: Juan the App Developer
- Juan’s account wasn’t deactivated after he left.
- He reused passwords across personal/work accounts.
- After a phishing attack, his old work account was compromised.
- A **lack of governance** allowed access from a dormant identity.

### 📋 Governance Best Practices
- Regular HR sync to detect stale accounts.
- Audit last login times.
- Review and limit user privileges.
- Enforce password changes and MFA.
- Automate access reviews and cleanup.

---

## 🔄 Identity Lifecycle Management (ILM)

### 🧱 Overview
ILM is the foundation of Identity Governance. It automates the **Join → Move → Leave** process for user identities.

### 🧍 Join-Move-Leave Model

| Stage | Description |
|-------|-------------|
| **Join** | A new user joins and gets an identity. |
| **Move** | The user moves roles/departments; access is adjusted. |
| **Leave** | The user leaves; access is revoked, account possibly deleted. |

### 📌 Key Concepts
- **System of Record (SoR):** Authoritative source like an HR database.
- **Visitor Strategy:** Special rules needed for temporary identities.
- **Automation:** Required for scalable and secure identity management.

---

## 🔎 Monitoring Tools for Identity Governance

| Tool | Description |
|------|-------------|
| **Azure Monitor** | Logs and metrics collection platform. |
| **Application Insights** | Monitors application health and user interaction. |
| **Azure Service Health** | Alerts you to Azure outages and issues. |
| **Azure Resource Health** | Provides current and historical health data. |
| **Azure Resource Manager** | Orchestration tool for deploying/configuring Azure resources. |
| **Azure Policy** | Enforces governance across subscriptions (e.g., require MFA). |

---

## 🧠 Zero Trust Principles

Always design with these in mind:

- 🔒 **Verify Explicitly** – Never assume trust.
- 🎯 **Use Least Privilege Access** – Limit access to just what’s needed.
- 🧯 **Assume Breach** – Monitor and act as if attackers are already inside.

---

> 📘 This README is intended for learners preparing for the SC-300 certification and IT pros managing identity in Microsoft Entra.
