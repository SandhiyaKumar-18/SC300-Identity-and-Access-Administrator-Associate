# 🔐 Centralized vs. Decentralized Identity – SC-300 Study Notes

## 🧭 Overview

This document compares **centralized identity systems** (like Microsoft Entra ID) with **decentralized identity models** (DIDs). It highlights structure, benefits, and key differences to help you master identity concepts for the SC-300 certification exam.

---

## 🔐 Centralized Identity Management

A **centralized identity system** is a tool managed by a central authority (admin/admin group), used to provide authentication and authorization to access data, apps, and resources.

### ✅ Key Characteristics

- **Credential Verification**: Verified when stored
- **Authority**: Managed by identity administrator
- **Usage**: Controls access to data, tools, and apps
- **Deployment**: On-premises or cloud-based
- **Example**: Microsoft Entra ID

### 📌 Benefits

- **Secure Adaptive Access**  
  Protects resources with strong authentication and risk-based policies.

- **Seamless User Experience**  
  Fast sign-in, reduced password fatigue, increased productivity.

- **Unified Identity Management**  
  Centralized management of cloud/on-prem identities.

- **Simplified Identity Governance**  
  Automates compliance and ensures only authorized access.

---

## 🌍 Decentralized Identity

A **decentralized identity system** gives individuals, organizations, and devices full control over their digital identities and credentials, enabling transparent and secure interactions.

### ✅ Key Characteristics

- **Self-Owned & User-Controlled**
- **Decentralized Identifiers (DIDs)**
  - Globally unique, self-generated
  - Rooted in decentralized systems (e.g., blockchain)
  - Resistant to tampering and censorship

### 🔐 Identity Data Storage

- **Off-Chain Encrypted Storage**
  - Identity data is stored privately
  - Only non-PII metadata (e.g., keys) is anchored to decentralized networks

---

## 🧩 Components of Decentralized Identity

| Component               | Description |
|-------------------------|-------------|
| **DIDs (W3C Standard)** | Unique, user-owned IDs containing public keys and service endpoints |
| **Decentralized Systems** | Blockchains/ledgers that support DIDs and DPKI |
| **DID User Agents**     | Apps that help users create and manage DIDs, permissions, and authentication |
| **DIF Universal Resolver** | Standard resolver to look up DID Documents across implementations |
| **DIF Identity Hubs**   | Encrypted, replicated data stores on cloud/edge devices (e.g., PC, mobile) |
| **DID Attestations**    | DID-signed, verifiable claims—used to establish trust |
| **Decentralized Apps**  | Apps that access identity hub data with user consent and permissions |

---

## 📌 Key Differences

| Feature            | Centralized Identity         | Decentralized Identity           |
|--------------------|------------------------------|----------------------------------|
| Managed By         | Central Admin or Authority   | User Themselves                  |
| Identity Storage   | Admin-controlled directories | User-controlled encrypted stores |
| Identifier Format  | Assigned by Organization     | Self-generated DIDs              |
| Trust Model        | Organization-based           | Cryptographic Proof              |
| Example            | Microsoft Entra ID           | DID + Wallet + Identity Hub      |

---

## 🎯 Study Tip

Understanding the **contrast between centralized and decentralized identity** is essential for real-world IAM solutions and critical for your SC-300 exam success.

---

> 📘 _This README was generated as part of SC-300 Microsoft Identity & Access Administrator study material._

