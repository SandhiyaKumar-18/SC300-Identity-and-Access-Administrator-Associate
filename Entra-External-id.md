
# 📘 Microsoft Entra External ID – Full Notes with Explanations + Examples

---

## 🔹 1. What is Microsoft Entra External ID?

### ✅ Explanation:
Microsoft Entra External ID helps you securely manage **external identities** like:
- **Consumers** (public customers)
- **Partners** (vendors, suppliers)
- **Contractors**

It offers **two main modes**:
- **B2B Collaboration** – For businesses to invite external partners
- **CIAM (Customer Identity and Access Management)** – For public-facing apps

### 💡 Example:
- A company like Contoso wants to let customers log in to their **shopping app** using Google or phone OTP.
- At the same time, they want **partners** like Fabrikam to access SharePoint or Teams.

---

## 🔹 2. CIAM – Customer Identity & Access Management

### ✅ Explanation:
CIAM is used when you build a public-facing app or website that **customers** (not employees) will use.

You manage:
- Sign-up & login flows
- Identity providers (Google, Apple, Email, etc.)
- Branding & policy controls
- Consent and custom user attributes

### 💡 Example:
**“MyMovieApp”** lets people book movie tickets. It uses:
- Sign-up with email or Facebook
- OTP for passwordless login
- Customized login screen with app branding
- External tenant holds all user data

---

## 🔹 3. B2B Collaboration

### ✅ Explanation:
Business-to-Business (B2B) lets you securely **collaborate with partners**, vendors, or consultants by inviting them to your Microsoft tenant.

Instead of creating local accounts, you:
- Invite their existing email (e.g., john@vendor.com)
- They access Teams, SharePoint, or your apps
- You can control permissions via **Conditional Access**

### 💡 Example:
- Contoso wants to collaborate with `lucy@fabrikam.com`.
- They invite her as a guest user.
- Lucy logs in using her own company's credentials.
- She can access Teams shared channels or documents.

---

## 🔹 4. Tenant Types

### ✅ Explanation:
There are **two kinds of tenants** in Entra External ID:

#### A. Workforce Tenant
Used by internal employees and for B2B guest collaboration.

#### B. External (CIAM) Tenant
Dedicated tenant used for managing **public consumer identities**.

### 💡 Example:

| Type              | Real Case                                                           |
|-------------------|---------------------------------------------------------------------|
| Workforce Tenant  | Contoso’s main Microsoft 365 tenant for staff + partner access     |
| CIAM Tenant       | A separate tenant for Contoso’s **customer portal**                |

---

## 🔹 5. Comparison: CIAM vs B2B

| Feature                     | CIAM (Customer)                          | B2B (Partner)                            |
|-----------------------------|------------------------------------------|-------------------------------------------|
| User Type                  | Public, consumer                         | External business partner                 |
| Sign-in Options            | Social login, email, phone               | Microsoft/Work identity                   |
| Where stored               | External tenant                          | Your tenant (as guest)                    |
| Example                    | `amy@gmail.com` logging into a shopping site | `john@fabrikam.com` joining Teams         |
| UI Customization           | Fully branded experience                 | Minimal branding                          |

---

## 🔹 6. B2B Direct Connect

### ✅ Explanation:
Used to **collaborate across tenants without inviting users**. Common for **Teams Shared Channels**.

You set **cross-tenant trust** to allow external users to:
- Use their identity
- Bring their MFA/compliance claims

### 💡 Example:
- Contoso and Fabrikam have a **shared Teams channel**.
- Emma from Fabrikam joins directly via her login.
- No guest invitation needed.

---

## 🔹 7. Cross-Tenant Access Settings

### ✅ Explanation:
This feature controls **who can access what** between your org and other orgs.

You define:
- Inbound rules (who can access your resources)
- Outbound rules (what your users can access outside)
- Trust settings (MFA, device compliance)

### 💡 Example:
- Contoso **trusts Fabrikam’s MFA**.
- Users from Fabrikam are not prompted for MFA again.
- Access is seamless and secure.

---

## 🔹 8. Entitlement Management

### ✅ Explanation:
Gives you automation for:
- Group & app access
- Approval workflows
- Auto expiration

Great for **temporary access** or **partner self-service**.

### 💡 Example:
- A supplier wants access to the billing portal.
- They request an **access package**.
- Their request goes through an **approval workflow**.
- Access expires in 30 days.

---

## 🔹 9. Identity Providers for CIAM

### ✅ Explanation:
These are services that authenticate users.

Supported identity providers:
- Google
- Facebook
- Microsoft Account
- Apple
- Email One-time passcode (OTP)
- Phone OTP
- GitHub (via OpenID)

### 💡 Example:
Your app supports:
- Sign in with Gmail or
- Sign in with Email OTP (for users without a social account)

---

## 🔹 10. Conditional Access (for External Users)

### ✅ Explanation:
Set security policies like:
- Require MFA
- Block risky sign-ins
- Require compliant devices

Applies differently to CIAM & B2B users.

### 💡 Example:
- CIAM: Require **Email OTP** and block login from certain countries.
- B2B: Require MFA **unless their org already did MFA** and is trusted.

---

## 🔹 11. Multitenancy

### ✅ Explanation:
#### A. Multitenant App:
One app can be used by users from **many different tenants**.

#### B. Multitenant Organization:
Multiple tenants working together with unified policies.

### 💡 Example:
- A single SaaS HR app used by Contoso, Fabrikam, and Tailspin.
- All log in via Microsoft Entra — but get routed to their tenant-specific data.

---

## 🔹 12. Microsoft Graph API for External ID

### ✅ Example 1: Invite a B2B Guest User
```http
POST https://graph.microsoft.com/v1.0/invitations
{
  "invitedUserEmailAddress": "lucy@partner.com",
  "inviteRedirectUrl": "https://portal.contoso.com",
  "sendInvitationMessage": true
}
```

### ✅ Example 2: Cross-Tenant Access Policy
```http
PATCH https://graph.microsoft.com/beta/policies/crossTenantAccessPolicy
{
  "partnerConfiguration": {
    "default": {
      "b2bCollaborationInbound": {
        "trustFrameworkPolicy": "mfa"
      }
    }
  }
}
```

---

## 🔹 13. Pricing & Billing

### ✅ Explanation:
- You’re billed per **Monthly Active User (MAU)**.
- First **50,000 MAUs per month are free**.
- B2B and CIAM have different billing models.

### 💡 Example:
- 10,000 customers sign up, but only 4,000 log in this month.
- You’re billed for 4,000 MAUs (first 50k free).

🔗 [Microsoft Entra External ID Pricing](https://azure.microsoft.com/en-us/pricing/details/entra/)
