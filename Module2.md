# Microsoft Entra ID - Initial Configuration Notes

## Unit 1: Introduction to Microsoft Entra ID
- Microsoft Entra ID is a cloud-based identity and access management (IAM) solution.
- Provides authentication, authorization, and identity protection.
- Supports Single Sign-On (SSO) and Multi-Factor Authentication (MFA).
- Key features include identity governance, access management, and directory services.

## Unit 2: Setting Up Your Microsoft Entra Tenant
- A tenant is a dedicated Microsoft Entra environment for an organization.
- Steps to create a new tenant:
  - Sign in to the **Microsoft Entra admin center**.
  - Click **Create a new tenant** and choose the **Azure AD** option.
  - Configure organization details (name, region, domain name).
  - Review and create the tenant.

## Unit 3: Adding Custom Domains
- Custom domains provide branding and user-friendly login names.
- Steps to add a domain:
  - Verify domain ownership using **TXT** or **MX** DNS records.
  - Set the custom domain as primary.
  - Ensure users are assigned to the new domain.

## Unit 4: Managing Microsoft Entra Users
- Users can be created manually or synchronized from on-premises Active Directory.
- User attributes include **UPN (User Principal Name), roles, and licenses**.
- Roles:
  - **Global Administrator**: Full control over the tenant.
  - **User Administrator**: Manage users and groups.
  - **Application Administrator**: Manage app registrations.
- Users can be assigned **licenses** for Microsoft 365, Azure services, etc.

## Unit 5: Managing Groups in Microsoft Entra ID
- Groups simplify access management by allowing permissions to be assigned collectively.
- Types of groups:
  - **Security Groups**: Used for role-based access control (RBAC).
  - **Microsoft 365 Groups**: Used for collaboration (Teams, SharePoint, etc.).
- Membership options:
  - **Assigned**: Admin manually adds members.
  - **Dynamic**: Users automatically added based on rules (e.g., department).

## Unit 6: Implementing Password Policies
- Password policies enhance security by enforcing complexity requirements.
- Enforced settings include:
  - Minimum length and complexity.
  - Password expiration policy.
  - Account lockout threshold and duration.
- Self-service password reset (SSPR) can be enabled for users.

## Unit 7: Configuring Multi-Factor Authentication (MFA)
- MFA adds an extra layer of security by requiring multiple authentication factors.
- Available authentication methods:
  - SMS/Phone Call Verification.
  - Microsoft Authenticator App.
  - Hardware Security Keys.
- Can be enforced for all users or based on Conditional Access policies.

## Unit 8: Integrating On-Premises Directories with Microsoft Entra Connect
- **Microsoft Entra Connect** syncs on-premises Active Directory (AD) with Microsoft Entra ID.
- Key components:
  - **Synchronization**: One-way (on-prem to cloud) or two-way sync.
  - **Pass-through Authentication (PTA)**: Uses on-prem credentials for authentication.
  - **Federation**: Uses Active Directory Federation Services (AD FS).
- Configure **filtering** to control which objects sync to Entra ID.

## Unit 9: Configuring Single Sign-On (SSO)
- **SSO** enables users to sign in once and access multiple applications.
- Methods of SSO integration:
  - **Password-based SSO**: Saves credentials securely.
  - **SAML/WS-Federation-based SSO**: Uses identity provider authentication.
  - **OAuth/OpenID Connect (OIDC)**: Used for cloud-native apps.
- Configure **Enterprise Applications** in Microsoft Entra ID for app SSO.

## Unit 10: Monitoring and Auditing in Microsoft Entra ID
- Monitoring ensures security and compliance in identity management.
- **Audit Logs** track administrative activities (e.g., user creation, role changes).
- **Sign-in Logs** provide details on user authentication events.
- **Microsoft Entra Identity Protection** detects and mitigates identity risks.
- Alerts can be configured for suspicious activity.

## Unit 11: Conclusion and Next Steps
- Review key concepts covered in the module.
- Explore advanced topics such as Conditional Access, Privileged Identity Management (PIM), and Identity Governance.
- Practice using the **Microsoft Learn Sandbox** for hands-on exercises.

---
**📌 Additional Resources:**
- [Microsoft Learn: Entra ID Modules](https://learn.microsoft.com/en-us/training/)
- [Microsoft Entra ID Documentation](https://learn.microsoft.com/en-us/entra/identity/)
- [SC-300 Exam Guide](https://learn.microsoft.com/en-us/certifications/exams/sc-300/)
