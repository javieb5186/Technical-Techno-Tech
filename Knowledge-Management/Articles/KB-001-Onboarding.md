# KB-001 - New Employee Onboarding

## Overview

### Purpose

This article provides a standardized procedure for onboarding a new employee in the Technical Techno Tech environment.

### Applies To

- Active Directory
- Microsoft 365
- Microsoft Entra ID
- Windows Server

---

## Requirements

### Required Access

- Domain Administrator or delegated account management permissions
- Microsoft 365 administrative access
- Authorization from Human Resources or the employee's manager

### Required Tools

- Active Directory Users and Computers (ADUC) / Active Directory Administrative Center (ADAC)
- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- PowerShell (optional)

---

## Procedure

### Step 1 - Review the Request

Verify:

- Employee name
- Department
- Job role
- Required start date
- Required applications and access

Confirm authorization has been received before proceeding.

---

### Step 2 - Create the Active Directory Account

1. Open ADUC or ADAC.
2. Navigate to the appropriate Organizational Unit (OU).
3. Create the new user account.
4. Configure:
   - Display Name
   - Username
   - Department
   - Job Title
5. Assign an initial password according to organizational policy.

---

### Step 3 - Assign Security Groups

Add the employee to the required security groups.

Examples:

- Departmental Access
- Shared Folder Access
- Remote Access Groups
- Application Access Groups

Follow least-privilege principles when assigning permissions.

---

### Step 4 - Configure Microsoft 365 Access

1. Verify the Microsoft 365 account exists or has synchronized.

To force sync use this powershell command:
```powershell
Start-ADSyncSyncCycle -PolicyType Delta
```

2. Assign the required license.
3. Confirm mailbox provisioning.
4. Verify required services are enabled.

Examples:

- Exchange Online
- Microsoft Teams
- OneDrive

---

### Step 5 - Configure Additional Access

Assign any additional approved resources:

- Shared folders
- Distribution groups
- Microsoft Teams memberships
- Application access
- Department-specific permissions

---

### Step 6 - Document Completion

Record:

- User account created
- Security groups assigned
- Licenses assigned
- Additional access granted
- Validation results

Update the related service request.

---

## Verification

### Validation Checks

- User account exists in Active Directory
- Required security groups assigned
- Microsoft 365 license assigned
- Mailbox successfully provisioned
- Required resources accessible

### Example Commands

Verify user account:

```powershell
Get-ADUser username
```

Verify group membership:

```powershell
Get-ADPrincipalGroupMembership username
```

Verify Microsoft 365 licensing:

```powershell
Get-MgUserLicenseDetail -UserId username@company.com
```

---

## Common Issues

| Issue | Resolution |
|---------|---------|
| User account not found | Verify account was created in the correct OU |
| Group membership missing | Review onboarding requirements and security groups |
| Microsoft 365 license unavailable | Verify available licensing inventory |
| Mailbox not provisioned | Allow synchronization time and verify licensing |
| User cannot access resources | Verify group membership and assigned permissions |

---

## Related Documentation

### Service Requests

- SR-001 New Employee Onboarding

### Procedures

- Request Logging
- Request Assessment
- Request Fulfillment
- Request Closure

---

## Notes

- Follow least-privilege principles.
- Do not assign permissions that were not approved.
- Do not record passwords or sensitive credentials in documentation.
- Validate all assigned access before closing the request.

---

## Skills Practiced

- Active Directory Administration
- Microsoft 365 Administration
- Microsoft Entra ID Administration
- User Lifecycle Management
- Access Management
- Service Request Fulfillment
- ITIL Service Request Management