# Company Branding in Microsoft Entra ID  

## Overview  
Microsoft Entra ID allows organizations to customize their **sign-in pages** with branding elements like a logo, background image, and custom text. This enhances the user experience for applications such as **Microsoft 365** that rely on Microsoft Entra ID for authentication.  

## **Prerequisites**  
To configure company branding, you need one of the following licenses:  
- **Microsoft Entra ID Premium P1 or P2**  
- **Office 365 (for Microsoft 365 apps)**  

## **Steps to Configure Company Branding**  
1. **Open Microsoft Entra ID** in the **Azure portal**.  
2. Navigate to **Manage > Company Branding**. _(This option is only available with a premium license.)_  
3. Customize the following branding settings:  

## **Branding Settings & Descriptions**  

| **Setting** | **Description** |
|------------|---------------|
| **Language** | Default language is set automatically and cannot be changed. |
| **Sign-in page background image** | Upload a **.png** or **.jpg** file (Max: **1920x1080px**, **300 KB**). The image is centered and scales to fit the screen. |
| **Banner logo** | Upload a **.png** or **.jpg** file. This logo appears on the sign-in page and the My Apps portal. |
| **Username hint** | Display a hint message for users who forget their username (**Max: 64 characters**). Cannot contain links or code. |
| **Sign-in page text** | Custom text at the bottom of the sign-in page (**Max: 1,024 characters**). Useful for help desk contact info or legal statements. |

## **Benefits of Custom Branding**  
✔ Creates a **consistent user experience** across all applications.  
✔ Reinforces **corporate identity** with logos and branding elements.  
✔ Provides **helpful instructions** for users with custom sign-in text.  

By configuring company branding in Microsoft Entra ID, organizations can **enhance their authentication experience** while maintaining security and professionalism.  

---

# Configure and Manage Microsoft Entra Roles  

## Overview  
Microsoft Entra ID is a cloud-based identity and access management service that helps organizations secure and manage access to resources. It is used for:  
- **External resources**: Microsoft 365, Azure portal, and SaaS applications.  
- **Internal resources**: Corporate network apps, intranet, and custom cloud applications.  

## **Who Uses Microsoft Entra ID?**  
### **1. IT Administrators**  
- Control access to applications and resources.  
- Enforce security policies like **Multi-Factor Authentication (MFA)**.  
- Automate user provisioning between **Windows Server AD** and cloud apps.  
- Protect user identities and credentials.  

### **2. App Developers**  
- Enable **Single Sign-On (SSO)** for applications.  
- Use APIs to integrate with organizational data.  

### **3. Microsoft 365, Office 365, Azure, and Dynamics CRM Online Subscribers**  
- All tenants automatically use Microsoft Entra ID for access management.  

## **Microsoft Entra Roles**  
Roles in Microsoft Entra ID define what actions a user can perform, such as creating users, managing passwords, and assigning licenses.  

| **Role**                | **Permissions** | **Notes** |
|----------------|--------------|---------|
| **Global Administrator** | Full access to all features in Entra ID | The first admin in a tenant is a Global Administrator. |
| **User Administrator** | Manage users, groups, passwords, and service health | Can reset passwords and manage support tickets. |
| **Billing Administrator** | Manage subscriptions, purchases, and support tickets | Responsible for financial aspects of Microsoft Entra services. |

### **Viewing Roles in Azure**  
- Go to **Azure portal > Microsoft Entra ID > Roles and administrators**.  

## **Azure Roles vs. Microsoft Entra Roles**  

| **Azure Roles** | **Microsoft Entra Roles** |
|----------------|----------------|
| Control **Azure resource access** | Control **Microsoft Entra resource access** |
| Support **custom roles** | Support **custom roles** |
| Assign roles at **multiple levels** (Subscription, Resource Group) | Assign roles at **tenant level** or **Administrative Unit level** |
| Managed via **Azure CLI, PowerShell, REST API** | Managed via **Azure portal, Microsoft Graph, PowerShell** |

### **Role Overlap Between Azure & Microsoft Entra ID**  
- By default, **Azure roles do not grant Microsoft Entra permissions**.  
- **Global Administrators** can enable **Access management for Azure resources** to assign Azure roles.  
- Some roles, like **Global Administrator**, span both **Microsoft Entra ID and Microsoft 365**.  

## **Assigning Microsoft Entra Roles**  
### **Methods to Assign Roles**  
1. **Assign a role to a user or group**:  
   - **Azure portal** > **Microsoft Entra ID** > **Roles and administrators** > Select Role > **+ Add Assignment**.  
2. **Assign a broad-scope role (Subscription, Resource Group, Management Group)**:  
   - Use **Access control (IAM)** settings.  
3. **Assign roles using PowerShell or Microsoft Graph API**.  
4. **Use Privileged Identity Management (PIM) for just-in-time role elevation**.  

## **Example: Assigning a Role Using PIM**  
- If using **Microsoft Entra ID Premium P2**, all role assignments are managed via **Privileged Identity Management (PIM)**.  
- Allows users to **elevate roles temporarily** when required.  

## **Creating Custom Roles in Microsoft Entra ID**  
### **Steps to Create a Custom Role**  
1. Go to **Azure portal > Microsoft Entra ID > Roles and administrators**.  
2. Click **New custom role**.  
3. **Enter a name and description**.  
4. On the **Permissions tab**, add necessary permissions.  
   - Example: `microsoft.directory/applications/credentials/update` for app credential management.  
5. Review and **Create** the role.  

The new role will now be available for assignment.  

## **Conclusion**  
Microsoft Entra roles allow organizations to **manage access securely**. Understanding **the difference between Azure roles and Microsoft Entra roles** ensures proper governance. **Using PIM and custom roles enhances security and minimizes risk.** 🚀  

