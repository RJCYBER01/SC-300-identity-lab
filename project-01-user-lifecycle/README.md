# Project 1: User Lifecycle (in progress)

## Evidence

**1. Joiner input:** bulk-create CSV validated in the Entra admin center before import
![CSV validated](screenshots/SC300-Bulk-01-before-3-users-csv-validated.png)

**2. Joiner result:** new CLD- users created across IT, HR, Finance and Sales
![Users created](screenshots/SC300-Bulk-03-after-11-users.png)

**3. Leaver:** cld.user08 shown as disabled (Account enabled = No)
![Leaver disabled](screenshots/SC300-Bulk-06-all-users-account-enabled-column.png)

**4. Leaver negative test:** disabled user cannot sign in (sign-in log error 50057)
![Leaver sign-in blocked](screenshots/SC300-Bulk-07-leaver-signin-blocked.png)

**5. Mover:** bulk location update with Microsoft Graph PowerShell (Update-MgUser from CSV)
![Bulk update output](screenshots/SC300-PS-03-bulk-update-output.png)

**6. Mover verified:** Get-MgUser confirms new City/Country (New York, London, Hong Kong)
![Cities verified](screenshots/SC300-PS-04-verify-cities-getmguser.png)
