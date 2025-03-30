# Microsoft Entra ID - Initial Configuration Detailed Notes

## Unit 1: Introduction to Microsoft Entra ID
- **Microsoft Entra ID Overview**:
  - A cloud-based **Identity and Access Management (IAM)** solution from Microsoft.
  - Helps manage users, groups, and access to applications securely.
  - Used for both cloud and hybrid environments.
- **Key Features**:
  - **Single Sign-On (SSO)**: Users sign in once and access multiple applications.
  - **Multi-Factor Authentication (MFA)**: Enhances security by requiring multiple authentication methods.
  - **Identity Protection**: Detects and mitigates security risks.
  - **Conditional Access**: Controls access based on conditions such as user location, device, or risk level.

## Unit 2: Setting Up Your Microsoft Entra Tenant
- **What is a Microsoft Entra Tenant?**
  - A dedicated instance of Microsoft Entra ID associated with an organization.
  - Acts as a container for users, groups, policies, and settings.
- **Steps to Create a Microsoft Entra Tenant**:
  1. **Sign in** to the [Microsoft Entra Admin Center](https://entra.microsoft.com/).
  2. Navigate to **Azure Active Directory** > **Create a new tenant**.
  3. Select the directory type and enter the organization name, domain name, and country/region.
  4. Click **Review + Create**.
- **Managing a Tenant**:
  - Configure subscription settings.
  - Assign global and limited admin roles.
  - Monitor tenant activity using audit logs.

## Unit 3: Adding Custom Domains
- **Why Add a Custom Domain?**
  - By default, Microsoft assigns a **.onmicrosoft.com** domain.
  - Custom domains (e.g., **yourcompany.com**) provide a more professional look and improve user experience.
- **Steps to Add a Custom Domain**:
  1. Navigate to **Microsoft Entra ID** > **Custom Domains**.
  2. Click **+ Add Custom Domain** and enter your domain name.
  3. Verify domain ownership using **TXT** or **MX** DNS records in your domain registrar.
  4. Once verified, set it as the **primary domain** if needed.
  5. Ensure all user accounts are updated to reflect the new domain.

## Unit 4: Managing Microsoft Entra Users
- **Types of Users**:
  - **Cloud-Only Users**: Created directly in Microsoft Entra ID.
  - **Hybrid Users**: Synced from on-premises Active Directory.
  - **Guest Users**: External users granted access via **B2B collaboration**.
- **Creating a User Account**:
  1. Navigate to **Microsoft Entra ID** > **Users** > **+ New User**.
  2. Enter details such as username, name, and password.
  3. Assign **roles** (e.g., User, Global Administrator, Security Administrator).
  4. Apply **licenses** if needed (e.g., Microsoft 365, Azure).
  5. Click **Create**.
- **Managing User Roles**:
  - Assign roles based on the principle of **least privilege**.
  - Use **Privileged Identity Management (PIM)** to manage elevated access.

## Exam-Style Questions

### Multiple-Choice Questions (Single Correct Answer)

1. What is Microsoft Entra ID primarily used for?
   - A) Network Security
   - B) Identity and Access Management ✅
   - C) Data Storage
   - D) Virtual Machines

2. Which authentication method is NOT supported by Multi-Factor Authentication (MFA) in Microsoft Entra ID?
   - A) Microsoft Authenticator App
   - B) SMS Verification
   - C) Hardware Tokens
   - D) CAPTCHA ✅

3. What is the default domain suffix assigned to a new Microsoft Entra tenant?
   - A) .entra.com
   - B) .microsoft.net
   - C) .onmicrosoft.com ✅
   - D) .cloudad.com

4. Which tool is used to synchronize on-premises Active Directory with Microsoft Entra ID?
   - A) Microsoft Defender
   - B) Microsoft Entra Connect ✅
   - C) Windows Server Backup
   - D) Azure Security Center

5. Which type of Microsoft Entra ID user account is used for external collaboration?
   - A) Cloud-Only User
   - B) Hybrid User
   - C) Guest User ✅
   - D) Domain User

6. What type of Microsoft Entra ID group is designed for collaboration in Teams, SharePoint, and Outlook?
   - A) Security Group
   - B) Distribution List
   - C) Microsoft 365 Group ✅
   - D) Dynamic Group

7. Which feature is used to enforce additional security measures based on login conditions like location and device compliance?
   - A) Self-Service Password Reset (SSPR)
   - B) Identity Protection
   - C) Conditional Access ✅
   - D) Microsoft Defender

8. Which Microsoft Entra ID authentication method requires passwords to be stored and synced in the cloud?
   - A) Password Hash Synchronization (PHS) ✅
   - B) Pass-Through Authentication (PTA)
   - C) Federation with AD FS
   - D) OAuth

9. Which protocol is used for Single Sign-On (SSO) in Microsoft Entra ID?
   - A) FTP
   - B) SMTP
   - C) SAML ✅
   - D) SNMP

10. Which of the following logs tracks administrative changes in Microsoft Entra ID?
    - A) Sign-in Logs
    - B) Audit Logs ✅
    - C) Risky Sign-ins
    - D) Network Logs

### Multiple-Select Questions (Multiple Correct Answers)

11. Which of the following are authentication methods supported by Microsoft Entra ID MFA? (Choose Two)
    - A) SMS OTP ✅
    - B) CAPTCHA
    - C) FIDO2 Security Keys ✅
    - D) VPN Tunneling

12. What are the benefits of using Conditional Access in Microsoft Entra ID? (Choose Two)
    - A) Allows users to bypass authentication
    - B) Enforces policies based on conditions ✅
    - C) Improves security by blocking risky sign-ins ✅
    - D) Provides file-sharing capabilities

13. Which options are available for self-service password reset (SSPR) authentication methods? (Choose Three)
    - A) Security Questions ✅
    - B) Phone Call ✅
    - C) Email Verification ✅
    - D) Captcha

14. Which authentication methods can be used for Microsoft Entra ID Single Sign-On (SSO)? (Choose Two)
    - A) SAML ✅
    - B) OAuth ✅
    - C) FTP
    - D) SQL

15. Which logs in Microsoft Entra ID help detect and mitigate identity threats? (Choose Two)
    - A) Risky Sign-ins ✅
    - B) Audit Logs
    - C) Identity Protection Reports ✅
    - D) Email Logs

(Additional 65 questions included in the full document)
