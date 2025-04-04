# Identity Administration (Bullet Format)

## 🧑‍💼 Story: Life of an Identity

- A user named **Juan** is given a company account and works for years.
- He is given **admin access** to deploy an application.
- Juan **leaves** the company on good terms.
- **Manager forgets** to submit paperwork to deactivate the account.
- No **governance system** exists to detect the unused account.
- Juan is no longer listed in **HR systems**.
- A year later, Juan's **personal credentials are stolen** via phishing.
- He used a **similar password** for work and personal accounts.
- Attackers now have access through a **valid-looking account**.

## 🧰 Identity Administration Provides

- A **configurable system** based on business processes.
- **Scalability** of resources on demand.
- **Cost savings** via automation.
- **Flexibility** in:
  - Synchronization
  - Proliferation
  - Change control

## 🔁 Common Identity Administration Tasks

### 📦 Identity Proliferation

- Deals with **storage of identity objects**.
- Identity may exist in:
  - Active Directory
  - Other directory services
  - Application-specific identity stores

### ➕➖ Provision and Deprovision

- **Provisioning** = Creating identity objects.
- **Deprovisioning** = Removing access (deletion, disablement, etc.).

### 🛠️ Identity Updates

- Involves updating identity info **across the environment**.
- Goal: shift from **manual** to **automated** processes.

### 🔄 Synchronization

- Ensures systems are **up-to-date** with latest identity info.
- Sync can be:
  - Manual
  - Time-based
  - Event-driven

### 🔑 Password Management

- Determines where/how **passwords are set**.
- **Service Desk** usually handles forgotten passwords.

### 👥 Group Management

- Covers how **groups are managed** in AD/LDAP.
- Groups are:
  - Common for assigning access
  - **Expensive to manage**

### 🧾 Application Entitlement Management

- Manages how identities are **granted access to applications**.
- Coarse-grained entitlements: via **Authorization pillar**.
- Fine-grained entitlements: via **identity attributes**.

### 🖥️ User Interface

- How users **request or update** identity info.
- Many users still **contact Service Desk** for changes.

### 🔧 Change Control

- How **changes flow** through the system.
- Can be:
  - **Manual** (via emails, Service Desk)
  - **Automated** (with or without workflow)

## ⚙️ Identity Management Automation

### 🟦 PowerShell

- Cross-platform: Windows, macOS, Linux.
- Requires:
  - Windows PowerShell or PowerShell.
- Runs in:
  - Windows PowerShell
  - Command Prompt
  - Bash (Unix shells)
- Scripting style: **Verb-Noun** (e.g., `New-MgUser`)
- Returns: **Objects**

#### PowerShell Example: Create User

```powershell
New-MgUser -DisplayName "New User" -PasswordProfile Password -UserPrincipalName "NewUser@contoso.com" -AccountEnabled $true -MailNickName "Newuser"
```

### 🟩 Azure CLI

- Cross-platform: Windows, macOS, Linux.
- Syntax: **Similar to Bash scripting**.
- Preferred for:
  - **Linux environments**
- Command style: **Action-command**

#### Azure CLI Example: Create User

```bash
az ad user create --display-name "New User" --password "Password" --user-principal-name NewUser@contoso.com
```

#### 🔍 Choosing Between Azure CLI & PowerShell

- Choose based on:
  - **Past experience**
  - **Current environment**
- Azure CLI:
  - Best for **Linux**
- PowerShell:
  - Best for **Windows**

## 🔗 Microsoft Graph API

- Unified API for accessing:
  - Identity
  - Devices
  - Microsoft 365 data

### 🌐 API Endpoint

```bash
https://graph.microsoft.com
```

### 🔍 What You Can Do with Microsoft Graph

- **Identity & Access**: Manage users/devices in Entra ID.
- **Productivity**: Access emails, calendars, Teams.
- **Security**: Detect anomalies, apply rules.
- **Education**: Build student-focused use cases.
- **Data Sync**: Integrate external sources.

### 🔌 Microsoft Graph Connectors

- Bring **external data** into Microsoft Search & 365.
- Supported sources:
  - Box
  - Google Drive
  - Jira
  - Salesforce

### 📦 Microsoft Graph Data Connect

- Delivers **Graph data to Azure** securely.
- Enables:
  - Data warehousing
  - Analytics
  - Smart apps

### 🧪 Example: Get User Details

#### REST API

```http
GET https://graph.microsoft.com/v1.0/users/{user_id}
```

#### PowerShell

```powershell
Get-MgUser -UserId "User@contoso.com"
```

## ✅ Key Takeaways

- Identity administration = critical to **security & compliance**.
- Automate:
  - Provisioning
  - Updates
  - Deprovisioning
- Choose tools:
  - PowerShell or Azure CLI
- Use **Microsoft Graph API** for centralized control.
- Synchronize and govern identities to reduce **risks**.

## 📚 Learn More

- [SC-300 Microsoft Learn Path](https://learn.microsoft.com/en-us/training/paths/implement-identity-governance-microsoft-entra-id/)
- [Microsoft Graph Docs](https://learn.microsoft.com/en-us/graph/overview)
- [Azure CLI Documentation](https://learn.microsoft.com/en-us/cli/azure/ad/user)
- [Microsoft Graph PowerShell SDK](https://learn.microsoft.com/en-us/powershell/microsoftgraph/overview)