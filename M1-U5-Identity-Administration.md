# Identity Administration

## Define Identity Administration

Identity administration refers to the management of identity objects throughout their lifecycle within an organization. This process can be conducted manually or automated, but it is essential to ensure proper governance and administration of identities.

### Story: The Life of an Identity

Consider a user named Juan. Juan is provided with an account in your company and works for several years. During this period, he is granted administrative access to deploy an application. Eventually, Juan leaves the company on good terms; however, his account is never removed from the system because a manager forgot to submit the necessary paperwork for account closure. Without a governance system in place to detect unused accounts or cross-reference with HR systems, Juan's account remains active. A year later, Juan becomes a victim of a phishing email, leading to his personal username and password being stolen. Like many individuals, Juan used similar passwords for both personal and work accounts. Consequently, your systems are now vulnerable to an attack originating from what appears to be a valid account.

![Diagram of the life of an identity: Start with no access, then job with access and identity creation, followed by leaving the company, and returning to no access.](#)

## Identity Administration Provides

- **Highly Configurable Systems:** Tailored around business processes.
- **Agility:** Ability to scale resources according to demand.
- **Cost Savings:** Achieved through distribution and automation of management.
- **Flexibility:** In synchronization, proliferation, and change control.

## Common Identity Administration Tasks

### Identity Proliferation

Involves the storage of identity objects within the environment. Organizations often have identities in directories like Active Directory, other directory services, and application-specific identity stores.

### Provision and Deprovision

- **Provisioning:** Refers to the creation of identity objects within a system.
- **Deprovisioning:** Focuses on the removal of an identity's access, which may involve deletion, disabling of security principals, or removal of access.

### Identity Updates

Concerns how identity information is updated throughout the environment, aiming to transition from manual efforts to more automated and streamlined approaches.

### Synchronization

Ensures that identity systems within an environment are up-to-date with the latest identity information, which is crucial for determining access. Synchronization can be manual, time-based, or event-driven.

### Password Management

Focuses on where and how passwords are set throughout the identity infrastructure. In many organizations, the Service Desk remains the focal point for forgotten passwords.

### Group Management

Addresses how an organization manages groups (e.g., Active Directory and/or LDAP) within their environment. Groups are a common method for determining access permissions to resources and can be costly to manage and operate.

### Application Entitlement Management

Defines how identities are granted access to applications, focusing on providing coarse-grained application entitlements enforced within the Authorization pillar. Fine-grained entitlements are managed as attributes related to an identity.

### User Interface

Pertains to how end users can request or make updates to their identity information. In many environments, users still contact the Service Desk for any updates to their identity information.

### Change Control

Focuses on how changes flow through the environment, whether manually completed by a Service Desk professional or automated with or without workflow to drive the change process. Some organizations still use emails to complete requests, while others have mature processes to execute changes.

## Identity Management Automation

### PowerShell

- **Platform:** Cross-platform (Windows, macOS, Linux)
- **Requirements:** Requires Windows PowerShell or PowerShell
- **Execution Environments:** Runs in Windows PowerShell, Command Prompt, or Bash and other Unix shells
- **Command Structure:** Follows a verb-noun naming scheme
- **Data Return:** Returns data as objects

#### Example: Create User with Microsoft Graph PowerShell

```powershell
New-MgUser -DisplayName "New User" -PasswordProfile Password -UserPrincipalName "NewUser@contoso.com" -AccountEnabled $true -MailNickName "Newuser"
