## KB-002 - Contractor Offboarding

### Overview

#### Purpose

This article provides guidance for offboarding employees and removing organizational access within the Technical Techno Tech environment.

#### Applies To

- Active Directory
- Microsoft Entra ID
- Windows Server

### Requirements

#### Required Access

- Domain Administrator
- Account Operator

#### Required Tools

- Active Directory UC / AC
- Microsoft Entra Connect
- Microsoft Entra Admin Center
- PowerShell

### Procedure

#### Step 1 - Verify Authorization

Review the offboarding request and confirm:

- Human Resources authorization
- Manager approval
- Employee identity
- Last working date

Ensure all required approvals are documented before proceeding.

#### Step 2 - Disable and Remove Access

In Active Directory UC / AC:

- Locate the user account.
- Disable the user account.
- Remove departmental security group memberships.
- Remove resource access groups.
- Move the account to the Disabled Users OU.

#### Step 3 - Synchronize and Validate

Run a Microsoft Entra Connect synchronization.

```powershell
Start-ADSyncSyncCycle -PolicyType Delta
```

Verify:

- Account is disabled in Active Directory.
- Group memberships were removed.
- Account exists in the Disabled Users OU.
- Microsoft Entra ID access has been revoked.

### Verification

Verify the procedure completed successfully.

#### Validation Checks

- Account disabled
- Security groups removed
- Resource access removed
- Account moved to Disabled Users OU
- Entra ID synchronization completed
- Cloud sign-in access revoked

#### Example Commands

```powershell
Get-ADUser username
```

```powershell
Get-ADPrincipalGroupMembership username
```

```powershell
Start-ADSyncSyncCycle -PolicyType Delta
```

### Common Issues

| Issue | Resolution |
|---------|---------|
| User account cannot be disabled | Verify administrative permissions |
| Group memberships remain assigned | Review direct and nested group memberships |
| User still appears active in Entra ID | Run synchronization and allow time for replication |
| Access remains after offboarding | Review security groups and assigned permissions |

### Related Documentation

- SR-002 Contractor Offboarding
- KB-001 New Employee Onboarding

### Notes

- Disabled accounts should remain in the Disabled Users OU until retention requirements are met.
- Do not delete accounts immediately unless explicitly approved.
- Validate access removal before closing the ticket.
