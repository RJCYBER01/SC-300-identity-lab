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
| 1 | [User Lifecycle — Joiner / Mover / Leaver](project-01-user-lifecycle/) | Bulk CSV import, Microsoft Graph PowerShell, account disable + sign-in verification | Complete |
| 2 | Conditional Access + MFA | 4 CA policies, MFA, Identity Secure Score 68.42% → 80.00% | Lab done · write-up in progress |
| 3 | Privileged Identity Management | PIM for Azure resources, custom RBAC role (Entra roles next) | Partly done · write-up in progress |
| 4 | Hybrid Identity with Entra Cloud Sync | On-prem AD → Entra ID sync, UPN suffix planning | Planned |
| 5 | Access Reviews & Entitlement Management | Identity governance, recurring access reviews | Planned |
| 6 | Zero Trust Identity Baseline | Break-glass accounts, authentication strengths, risk-based CA, PIM for Entra roles, Administrative Units | Planned |
| 7 | Azure Monitoring & Identities | Managed identities, Log Analytics + KQL, dynamic group licensing | Lab done · write-up in progress |

## Security note
All screenshots are masked (tenant IDs, object IDs, UPNs, IPs, personal emails).
All user accounts shown are fictional lab users (CLD- prefix).
