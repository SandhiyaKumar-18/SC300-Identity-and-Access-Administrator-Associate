# 📌 SC-300 Notes: The Identity Landscape  

## 🔍 Overview  
The **Identity Landscape** is a critical concept in Microsoft’s security framework. It defines how identities are managed, authenticated, authorized, and secured. This document provides an in-depth look at the **Zero Trust model**, identity lifecycle, authentication methods, and security best practices.  

---

## 📌 Key Concepts  

### **1️⃣ Zero Trust Security Model**  
Zero Trust is a **security framework** that requires continuous verification before granting access.  

#### 🔹 Core Principles of Zero Trust:  
- ✅ **Verify Explicitly** – Always authenticate and validate identities before allowing access.  
- ✅ **Use Least Privilege** – Grant users only the **minimum** permissions needed.  
- ✅ **Assume Breach** – Design systems assuming that cyberattacks will happen.  

🔹 **Why Zero Trust?**  
Traditional security relied on perimeter-based defenses (**firewalls & VPNs**), which are ineffective in **cloud and remote work environments**. Zero Trust secures data **everywhere** using identity-based access policies.  

---

### **2️⃣ Identity & Actions**  
Microsoft categorizes identity into different types based on **user interaction and authentication needs**.  

#### 🔹 Identity Types & Actions:  
| **Identity Type** | **Action** | **Description** |
|------------------|------------|----------------|
| **Business to Business (B2B)** | **Authenticate (AuthN)** | Verifies external partners before access. |
| **Business to Consumer (B2C)** | **Authorize (AuthZ)** | Grants permissions to customers logging into services. |
| **Verifiable Credentials** | **Administer & Configure** | Uses decentralized identity verification methods. |
| **Decentralized Providers** | **Audit & Report** | Enables monitoring of authentication activities. |

---

### **3️⃣ Identity Usage**  
Once a user is authenticated, they can access **applications, data, and cloud resources**.  

#### 🔹 Key Aspects of Identity Usage:  
| **Aspect** | **Description** |
|-----------|----------------|
| **Access Applications & Data** | Secure login to apps using identity verification. |
| **Security (Cryptography & MFA)** | Uses encryption & **Multi-Factor Authentication (MFA)** to enhance security. |
| **Licensing Considerations** | Organizations must manage **costs and licensing** for identity services. |

🔹 **Example:**  
An employee logs into **Microsoft Entra ID (Azure AD)** → Identity is verified → Access is granted to Microsoft 365 apps like SharePoint, Teams, and Outlook.  

---

### **4️⃣ Identity Maintenance**  
Identity services must be **continuously protected, monitored, and updated**.  

#### 🔹 Key Maintenance Actions:  
| **Action** | **Purpose** |
|-----------|------------|
| **Protect** | Apply **Conditional Access Policies** for security. |
| **Detect** | Monitor **Azure AD logs** for suspicious activities. |
| **Respond** | Take action on security threats (e.g., disable compromised accounts). |
| **System Updates** | Keep identity systems **up-to-date** with patches and compliance updates. |

🔹 **Why It Matters?**  
Attackers often target **user credentials**. Monitoring authentication logs and enforcing strong security measures **reduces the risk of data breaches**.  

---

### **5️⃣ Classic Identity vs. Zero Trust Identity**  
Microsoft has evolved from **Classic Identity models** (network security) to **Zero Trust Identity** (identity-based security).  

| **Classic Identity** | **Zero Trust Identity** |
|----------------------|----------------------|
| Perimeter-based security (firewalls, VPNs). | Identity-driven security (Conditional Access, MFA). |
| Username & password grant full access. | Continuous verification with **least privilege** access. |
| One-time authentication. | Ongoing risk evaluation for each request. |
| Assets protected behind a corporate firewall. | Secure access **anywhere**, even outside corporate networks. |

🔹 **Example: Why Classic Identity Fails?**  
- If a hacker steals a **password**, they can access everything.  
- **Zero Trust prevents this** by continuously verifying users and limiting access.  

---

## ✅ Summary & Key Takeaways  
- **Zero Trust ensures secure identity verification before granting access.**  
- **Authentication (AuthN) vs. Authorization (AuthZ):**  
  - **AuthN:** Proves identity (e.g., login).  
  - **AuthZ:** Grants permissions based on role.  
- **Identity must be continuously maintained** through **monitoring, security policies, and updates**.  
- **Zero Trust replaces traditional perimeter security** with **continuous access control policies**.  

---

## 📅 Next Steps:  
✅ Learn about **Conditional Access Policies** in Microsoft Entra ID.  
✅ Understand **Multi-Factor Authentication (MFA) & Passwordless Authentication**.  
✅ Explore **Azure AD Identity Protection & Risk-Based Access Controls**.  

---

## 🚀 How to Use This Repository  
1️⃣ Read through the structured **SC-300 notes** to understand the **Identity Landscape**.  
2️⃣ Use the provided tables and examples to grasp **Zero Trust and Identity Governance**.  
3️⃣ Track your progress with the **Next Steps** section.  

📌 **Stay Secure. Stay Updated. Keep Learning! 🚀**
