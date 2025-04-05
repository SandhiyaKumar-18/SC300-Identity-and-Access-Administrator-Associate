# 📘 Authorization Overview - SC-300 Study Notes

## 🧾 What is Authorization?

**Authorization (AuthZ)** is the process of determining:
- **What resources a verified identity can access**
- **What actions they are allowed to perform**

🔑 It differs from **Authentication (AuthN)**, which only verifies the identity.

---

## 🎯 Key Benefits of Authorization

- ✅ Secure entitlement assignment
- ✅ Centralized access policy management
- ✅ Simplified enforcement through standardized models

---

## 🧩 Core Concepts

| Concept             | Description |
|---------------------|-------------|
| **Entitlement Type** | Determines if access has been granted. Managed via groups, RBAC, ABAC, or PBAC. |
| **Access Policies** | Define who can access what, and what they can do. Based on least privilege principle. |
| **Enforcement** | Enforcement usually happens in the app layer via APIs or externally using reverse proxies (e.g., UAG) or policy engines like XACML. |

---

## 🔐 Common Authorization Models

### 1. Access Control Lists (ACLs)
- Explicit lists of entities with or without access.
- ⚠️ Hard to scale, but provides fine-grained control.

### 2. Role-Based Access Control (RBAC)
- Access is granted based on roles.
- Most commonly used method.
- Roles are assigned to users; roles determine access permissions.

### 3. Attribute-Based Access Control (ABAC)
- Access decisions are based on:
  - User attributes (e.g., role = manager)
  - Resource attributes (e.g., tag = confidential)
  - Environment attributes (e.g., time = business hours)

### 4. Policy-Based Access Control (PBAC)
- Access is determined by combining **business roles** and **policy rules**.
- More dynamic and scalable than traditional role-based systems.

---

## 🧱 Authentication Context (Microsoft Entra ID)

- A **preview feature** used to apply stronger access control within applications.
- Can be enforced for:
  - Custom apps
  - SharePoint
  - Microsoft Defender for Cloud Apps

📌 **Example:**
- Everyone can view a general SharePoint site.
- Only users on managed devices can access sensitive content like proprietary recipes or documents.

---

## 📚 Summary

- **AuthZ** ensures only the right identities access the right resources.
- Use **RBAC**, **ABAC**, or **PBAC** based on complexity and scale.
- Use **Authentication Context** for advanced protection within Microsoft Entra environments.

---

> 🧠 Part of SC-300 Certification Learning - "Implement an identity management solution"  
> Source: Microsoft Learn – Discuss Authorization Module  
> XP Earned: 100  
