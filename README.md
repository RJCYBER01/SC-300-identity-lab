# Project 1: User Lifecycle — Joiner / Mover / Leaver

## Problem
Organizations need a repeatable, auditable way to onboard new hires, update people
who change roles or locations, and shut off access the moment someone leaves.
Manual, one-by-one changes are slow and error-prone, and a missed leaver is a
classic security gap.

## Environment
- **Tenant:** Microsoft Entra ID ("ABC Enterprise"), Entra ID Free, Security Defaults on
- **Admin tools:** Microsoft Entra admin center, Microsoft Graph PowerShell SDK
- **Accounts:** fictional cloud-only lab users with the `CLD-` prefix across IT, HR, Finance and Sales

## What I configured
1. **Joiner (bulk create):** prepared a CSV from the Entra bulk-create template and
   imported 8 new users through *Users > Bulk operations > Bulk create*. Portal bulk
   import is the fastest no-code option for HR-driven onboarding.
2. **Mover (bulk update with PowerShell):** the portal CSV import did not set City and
   Office, so I wrote a Graph PowerShell script that reads an HR CSV and runs
   `Update-MgUser` to set City, Country and UsageLocation for 7 users
   (New York, London, Hong Kong). Connected with delegated access and the
   least-privileged scope needed for writes: `User.ReadWrite.All`.
3. **Leaver (disable):** disabled the leaver account (Account enabled = No) rather than
   deleting it, so the account and its data stay available for review while
   access is cut immediately.

## Evidence

**1. Joiner input:** bulk-create CSV validated in the Entra admin center before import
![CSV validated](screenshots/SC300-Bulk-01-before-3-users-csv-validated.png)

**2. Joiner result:** new CLD- users created across IT, HR, Finance and Sales
![Users created](screenshots/SC300-Bulk-03-after-11-users.png)

**3. Leaver:** cld.user08 shown as disabled (Account enabled = No)
![Leaver disabled](screenshots/SC300-Bulk-06-all-users-account-enabled-column.png)

**4. Leaver negative test:** disabled user cannot sign in (sign-in log error 50057)
![Leaver sign-in blocked](screenshots/SC300-Bulk-07-leaver-signin-blocked.png)

**5. Mover:** bulk location update with Microsoft Graph PowerShell (Update-MgUser from CSV), 7/7 users OK after fixing the empty State field
![Bulk update output](screenshots/SC300-PS-03-bulk-update-output.png)

**6. Mover verified:** Get-MgUser confirms new City, Country and UsageLocation (US, GB, HK); leaver and admin accounts correctly untouched
![Cities verified](screenshots/SC300-PS-04-verify-cit
