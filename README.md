# SC-300 Identity Lab — Microsoft Entra ID

Hands-on identity and access management (IAM) labs built while preparing for
**Microsoft SC-300: Identity and Access Administrator**. Each project follows a
real business scenario, with step-by-step configuration, masked screenshots as
evidence, verification tests (positive and negative), and the problems I hit
along the way.

**Author:** Ravi Puri — career changer moving into IAM / identity administration

[LinkedIn](https://linkedin.com/in/ravicyberops) · [Portfolio](https://ravicyberops.com)

## Lab environment
- **Cloud:** Microsoft Entra ID tenant ("ABC Enterprise"), Azure subscription
- **On-premises (VMware):** Windows Server 2025 domain controller (AD DS + DNS),
  domain-joined Windows 11 client
- **Tools:** Entra admin center, Microsoft 365 admin center, Microsoft Graph PowerShell

## Projects

| # | Project | Skills | Status |
|---|---------|--------|--------|
| 1 | [User Lifecycle — Joiner / Mover / Leaver](project-01-user-lifecycle/) | Bulk CSV import, Microsoft Graph PowerShell, account disable + sign-in verification | Evidence published, write-up in progress |
| 2 | Conditional Access + MFA | CA policies, MFA, Identity Secure Score before/after | Planned |
| 3 | Privileged Identity Management | Just-in-time admin access, permanent → eligible roles | Planned |
| 4 | Hybrid Identity with Entra Cloud Sync | On-prem AD → Entra ID sync, UPN suffix planning | Planned |
| 5 | Access Reviews & Entitlement Management | Identity governance, recurring access reviews | Planned |

## Security note
All screenshots are masked (tenant IDs, object IDs, UPNs, IPs, personal emails).
All user accounts shown are fictional lab users (CLD- prefix).
