# Technical Techno Tech — Active Directory Group Structure

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Configuration  
**Document ID:** INF-AD-003  
**Version:** 1.0  
**Status:** Existing Lab — Configuration Verification Ongoing  
**Practice:** Service Configuration Management  
**Function:** Internal IT  
**Platform:** Active Directory Domain Services (AD DS)  
**Domain:** `technicaltechnotech.com`  
**Domain Controllers:** DC01, DC02  
**Last Reviewed:** Pending Verification

---

## 1. Purpose

This document describes the Active Directory group structure used within Technical Techno Tech's internal IT environment.

It establishes a centralized reference for:

- Security groups
- Distribution groups
- Group scopes
- Departmental group organization
- Group membership
- Group nesting
- Resource access permissions
- Administrative groups
- AGDLP implementation
- Group lifecycle management
- Security and access reviews
- Configuration verification
- Troubleshooting

The document supports centralized identity and access management, least privilege, and ITIL 4 service management practices.

---

## 2. Environment Overview

Technical Techno Tech uses Active Directory Domain Services to centrally manage user accounts, computer accounts, security groups, and access permissions.

### Active Directory Environment

| Component | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| Domain | `technicaltechnotech.com` |
| Domain Controllers | DC01 and DC02 |
| Administrative Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Virtualization Platform | Hyper-V |
| Group Management | Active Directory |
| Administrative Tools | ADUC, ADAC, PowerShell |

### Group Management Objectives

1. Centralize access management.
2. Organize users by department and responsibility.
3. Apply least privilege.
4. Reduce direct permission assignments to individual users.
5. Simplify employee onboarding and offboarding.
6. Support administrative delegation.
7. Improve access auditing.
8. Maintain consistent group naming.
9. Document resource access relationships.
10. Support scalable identity management.

---

## 3. Understanding Active Directory Groups

Active Directory groups simplify administration by allowing multiple accounts to be managed collectively.

Instead of assigning permissions separately to every employee, administrators can assign permissions to security groups.

### Example

A company has three HR employees who need access to an HR shared folder.

Rather than assigning permissions to each employee individually, the administrator creates a security group and grants the appropriate access.

```text
HR Employees
     |
     v
HR Security Group
     |
     v
HR Folder Permissions
```

When a new employee joins HR, the administrator can add the employee to the appropriate group.

### Key Concept

**Security groups manage access.**

**Organizational units organize directory objects.**

Group membership and OU placement serve different purposes.

---

## 4. Active Directory Group Categories

Active Directory supports two primary group categories.

### 4.1 Security Groups

Security groups are used to assign permissions to resources.

Examples include:

- Shared folders
- Printers
- Applications
- Administrative functions
- Other securable resources

Security groups can also be used for email distribution when supported by the messaging environment.

### 4.2 Distribution Groups

Distribution groups are designed for email distribution.

They are not security principals and cannot be used to assign access permissions.

A mail system, such as Exchange, is required to provide the corresponding email functionality.

### 4.3 Comparison

| Feature | Security Group | Distribution Group |
|---|---|---|
| Assign resource permissions | Yes | No |
| Group user accounts | Yes | Yes |
| Support group nesting | Yes, subject to scope rules | Yes, subject to scope rules |
| Support email distribution | When mail-enabled | When mail-enabled |
| Used for access control | Yes | No |

### TTT Implementation

Previous lab exercises included both security and distribution groups.

Actual group categories and memberships must be verified against the current TTT domain.

---

## 5. Active Directory Group Scopes

Group scope determines where a group can contain members and where it can be used to assign permissions.

Active Directory supports three primary scopes.

### 5.1 Global Groups

Global groups are commonly used to organize users according to departments or job responsibilities.

Examples:

- HR Employees
- Sales Employees
- IT Employees

In a typical single-domain environment, global groups are useful for collecting accounts that share a common role.

**Memory Hook:** Global = Who belongs to the group?

### 5.2 Domain Local Groups

Domain local groups are commonly used to assign permissions to resources within their domain.

Examples:

- HR Folder Read
- Sales Folder Modify
- IT Share Access

**Memory Hook:** Domain Local = What resource can they access?

### 5.3 Universal Groups

Universal groups can contain eligible members from multiple domains within the same forest and can be used to assign permissions across domains in the forest.

They are particularly useful in multidomain environments.

TTT currently documents a single-domain design, so universal groups are not required merely to organize departmental access.

### 5.4 Scope Comparison

| Scope | Common Purpose | Membership Considerations | Permission Scope |
|---|---|---|---|
| Global | Organize accounts by role | Accounts and eligible global groups from the same domain | Resources in trusted domains |
| Domain Local | Assign resource permissions | Eligible accounts and groups from permitted domains | Resources in the group's own domain |
| Universal | Organize access across domains | Eligible accounts and groups from domains in the same forest | Resources in trusted domains |

Actual membership rules depend on domain relationships and group scope.

### Important

Domain local groups can contain individual users when permitted by scope rules.

Using global groups inside domain local groups is a recommended administrative design, not a technical requirement.

---

## 6. TTT Group Architecture

The TTT environment uses a departmental structure that supports group-based resource access.

### 6.1 Logical Structure

```text
technicaltechnotech.com
          |
          v
       Groups OU
          |
          +-- Departmental Groups
          |      |
          |      +-- IT
          |      +-- Executives
          |      +-- HR
          |      +-- Sales
          |
          +-- Resource Access Groups
          |
          +-- Distribution Groups
          |
          +-- Administrative Groups
```

This is a logical classification of group types, not a verified hierarchy of nested OUs.

### 6.2 Previously Practiced Group Types

| Group Type | Purpose | Status |
|---|---|---|
| Departmental Security Groups | Organize employees by department | Previously Configured |
| Domain Local Resource Groups | Control resource access | Previously Practiced |
| Distribution Groups | Group users for email distribution | Previously Configured |
| Administrative Groups | Support delegated permissions | Pending Inventory |
| Built-in Privileged Groups | Provide directory administration capabilities | Present in AD DS; Membership Pending Review |

### 6.3 Group Inventory Status

Exact group names, scopes, categories, and memberships require verification.

This document distinguishes previously practiced configurations from proposed naming examples.

---

## 7. Departmental Security Groups

### 7.1 Purpose

Departmental security groups organize employees according to their business responsibilities.

These groups can simplify:

- Onboarding
- Department transfers
- Access assignment
- Access reviews
- Offboarding

### 7.2 Departmental Structure

| Department | Group Purpose | Group Scope |
|---|---|---|
| IT | IT personnel | Global — Verify |
| Executives | Executive personnel | Global — Verify |
| HR | Human Resources personnel | Global — Verify |
| Sales | Sales personnel | Global — Verify |

### 7.3 Proposed Naming Convention

The following names illustrate a consistent naming standard.

| Proposed Group Name | Category | Scope |
|---|---|---|
| GG_IT_Employees | Security | Global |
| GG_Executives | Security | Global |
| GG_HR_Employees | Security | Global |
| GG_Sales_Employees | Security | Global |

**Status:** Naming Examples — Not Confirmed Existing Objects

### 7.4 Group Membership Verification

```powershell
Get-ADGroup -Filter * |
Select-Object Name,GroupScope,GroupCategory,DistinguishedName
```

Review members of a specific group:

```powershell
Get-ADGroupMember -Identity "GroupName"
```

Replace `GroupName` with a verified group name.

---

## 8. AGDLP Permission Model

### 8.1 Overview

AGDLP is a common Active Directory group nesting strategy.

AGDLP stands for:

- **A** — Accounts
- **G** — Global Groups
- **DL** — Domain Local Groups
- **P** — Permissions

### 8.2 AGDLP Structure

```text
User Accounts
      |
      v
Global Security Group
      |
      v
Domain Local Security Group
      |
      v
Resource Permissions
```

### 8.3 Example — HR Folder Access

```text
HR Employee Accounts
         |
         v
GG_HR_Employees
         |
         v
DL_HR_Folder_Modify
         |
         v
HR Shared Folder
         |
         v
NTFS Modify Permission
```

This example demonstrates a recommended access model.

The exact group names and permissions are not confirmed as deployed.

### 8.4 Why Use AGDLP?

AGDLP separates employee membership from resource permissions.

This provides several benefits:

1. Simplifies permission management.
2. Reduces direct user permission assignments.
3. Supports consistent access control.
4. Makes access reviews easier.
5. Simplifies department changes.
6. Reduces unnecessary changes to resource permissions.

### 8.5 Example — New HR Employee

When a new HR employee joins the company:

1. Create the employee account.
2. Verify the employee's department.
3. Add the employee to the approved HR global group.
4. Confirm the global group is nested in the appropriate resource access group.
5. Verify the employee's effective access.
6. Document the request.

The administrator does not need to modify folder permissions for each new employee if the group-based permissions are already configured correctly.

---

## 9. Resource Access Groups

### 9.1 Purpose

Resource access groups represent permissions to specific business resources.

Examples include:

- Departmental shared folders
- Administrative shares
- Application resources
- Printers

### 9.2 Proposed Resource Group Inventory

| Proposed Group Name | Scope | Intended Resource | Permission |
|---|---|---|---|
| DL_HR_Folder_Read | Domain Local | HR folder | Read |
| DL_HR_Folder_Modify | Domain Local | HR folder | Modify |
| DL_Sales_Folder_Read | Domain Local | Sales folder | Read |
| DL_Sales_Folder_Modify | Domain Local | Sales folder | Modify |
| DL_IT_Folder_Modify | Domain Local | IT folder | Modify |

**Status:** Proposed Naming Examples

### 9.3 Previous Lab Experience

Previous Active Directory lab exercises included:

- HR folder permissions
- Sales folder permissions
- IT folder permissions
- NTFS permission inheritance
- Security group nesting
- Authorized and unauthorized access tests

The current TTT resource locations, group assignments, and effective permissions require verification.

### 9.4 Resource Permission Principles

- Assign permissions to security groups where practical.
- Apply least privilege.
- Separate read and modify access when required.
- Review inherited permissions.
- Avoid unnecessary broad access.
- Test effective permissions using appropriate accounts.

### 9.5 Important Distinction

Share permissions and NTFS permissions are separate access control mechanisms.

When accessing an SMB share over the network, both can affect effective access.

The most restrictive applicable combination determines the effective access permitted through the share.

---

## 10. Distribution Groups

### 10.1 Purpose

Distribution groups organize recipients for email communication.

### 10.2 Previously Documented Groups

Previous lab work included distribution groups such as:

- AllEmployees
- All Department Staff

The exact current names and group attributes require verification.

### 10.3 Group Inventory

| Group Name | Category | Intended Purpose | Status |
|---|---|---|---|
| AllEmployees | Distribution | Organization-wide communications | Previously Documented |
| All Department Staff | Distribution | Departmental communications | Previously Documented |

### 10.4 Important

Creating a distribution group in Active Directory does not automatically provide email delivery.

Email distribution requires an appropriate messaging system and mail-enabled group configuration.

Microsoft 365 and Exchange have not yet been deployed for TTT.

### 10.5 Verification

```powershell
Get-ADGroup -Filter 'GroupCategory -eq "Distribution"' |
Select-Object Name,GroupScope,GroupCategory,DistinguishedName
```

### Verification Checklist

- [ ] Distribution groups identified
- [ ] Group categories verified
- [ ] Group scopes verified
- [ ] Membership reviewed
- [ ] Email functionality distinguished from directory configuration
- [ ] Actual group names documented

---

## 11. Administrative Security Groups

### 11.1 Purpose

Administrative groups organize accounts that require specific IT management permissions.

### 11.2 Administrative Responsibilities

Examples include:

- Password resets
- Account unlocking
- User account management
- Computer account management
- Group membership administration
- Server administration

### 11.3 Built-in Administrative Groups

Active Directory includes privileged groups such as:

- Domain Admins
- Enterprise Admins
- Schema Admins
- Account Operators
- Server Operators
- Backup Operators

These groups have different privileges and scopes.

Membership should be reviewed carefully.

### 11.4 Delegated Administration

Previous TTT-related Active Directory exercises included delegated password reset permissions.

A recommended design is to assign delegated permissions to a dedicated security group rather than directly to multiple individual accounts.

### 11.5 Example Delegation Group

```text
GG_HelpDesk_PasswordReset
```

**Status:** Proposed Example — Not Confirmed Deployed

### 11.6 Security Requirements

- Apply least privilege.
- Avoid unnecessary Domain Admins membership.
- Separate standard and administrative accounts.
- Review privileged group membership.
- Document delegated permissions.
- Audit sensitive administrative operations.

### 11.7 Verification

Review Domain Admins:

```powershell
Get-ADGroupMember -Identity "Domain Admins"
```

Review Enterprise Admins:

```powershell
Get-ADGroupMember -Identity "Enterprise Admins"
```

Review all security groups:

```powershell
Get-ADGroup -Filter 'GroupCategory -eq "Security"' |
Select-Object Name,GroupScope,DistinguishedName
```

---

## 12. Group Naming Standards

### 12.1 Purpose

Consistent group names help administrators identify a group's scope and intended purpose.

### 12.2 Proposed Naming Convention

| Prefix | Meaning | Example |
|---|---|---|
| GG | Global Group | GG_HR_Employees |
| DL | Domain Local Group | DL_HR_Folder_Modify |
| UG | Universal Group | UG_Company_Resources |
| DIST | Distribution Group | DIST_AllEmployees |

### 12.3 Naming Format

```text
[Scope]_[Department or Resource]_[Purpose]
```

Examples:

```text
GG_HR_Employees
GG_Sales_Employees
DL_HR_Folder_Read
DL_Sales_Folder_Modify
DIST_AllEmployees
```

### 12.4 Naming Recommendations

- Use descriptive names.
- Maintain consistent prefixes.
- Avoid ambiguous abbreviations.
- Identify the group's purpose.
- Avoid unnecessary duplicate groups.
- Document exceptions.

### Important

These naming standards are proposed for future consistency.

Existing groups should not be renamed without reviewing dependencies and obtaining appropriate authorization.

---

## 13. Group Membership Management

### 13.1 Overview

Group membership determines which accounts belong to a group.

Membership changes can affect access to resources and administrative permissions.

### 13.2 Adding Members

Example:

```powershell
Add-ADGroupMember `
    -Identity "GG_HR_Employees" `
    -Members "exampleuser"
```

**Execution Status:** Reference Example — Not Executed

The group and account must exist before running the command.

### 13.3 Removing Members

```powershell
Remove-ADGroupMember `
    -Identity "GG_HR_Employees" `
    -Members "exampleuser"
```

### 13.4 Reviewing Membership

```powershell
Get-ADGroupMember -Identity "GG_HR_Employees"
```

### 13.5 Reviewing User Group Membership

```powershell
Get-ADPrincipalGroupMembership -Identity "exampleuser"
```

### 13.6 Recommended Workflow

1. Receive an authorized request.
2. Identify the user.
3. Identify the required group.
4. Review the group's purpose.
5. Confirm the requested access is appropriate.
6. Add or remove membership.
7. Verify the change.
8. Test effective access when required.
9. Document the result.

### 13.7 Important

Changes to security group membership may not immediately affect an existing logon session.

A new authentication session or refreshed security token may be required for updated permissions to take effect.

---

## 14. Group Nesting

### 14.1 Overview

Group nesting allows one group to become a member of another group, subject to Active Directory scope rules.

### 14.2 TTT Application

Previous lab exercises included nesting departmental global groups inside domain local resource groups.

### 14.3 Example

```text
GG_HR_Employees
       |
       v
DL_HR_Folder_Modify
       |
       v
HR Shared Folder
```

### 14.4 Benefits

- Simplifies access management.
- Reduces repetitive permission assignments.
- Separates organizational roles from resource permissions.
- Improves administrative consistency.

### 14.5 Verification

Review direct membership:

```powershell
Get-ADGroupMember -Identity "DL_HR_Folder_Modify"
```

Review recursive membership:

```powershell
Get-ADGroupMember `
    -Identity "DL_HR_Folder_Modify" `
    -Recursive
```

### 14.6 Security Considerations

- Avoid unnecessary nesting complexity.
- Document group relationships.
- Review effective permissions.
- Avoid circular membership designs.
- Periodically review nested privileged groups.

---

## 15. Group Membership and Organizational Units

### 15.1 Overview

Organizational units and security groups work together but perform different functions.

### Example

An HR employee account may be stored in the HR OU while belonging to multiple security groups.

```text
Active Directory Domain
          |
          v
        HR OU
          |
          v
     Employee Account
          |
          +-- GG_HR_Employees
          |
          +-- Other Approved Groups
```

### 15.2 Key Differences

**OU Placement**

Determines the object's directory location and can influence delegation and Group Policy.

**Group Membership**

Determines membership-based permissions and access relationships.

### 15.3 Important

Moving a user account to another OU does not automatically update security group membership.

Department transfers may require both OU changes and group membership changes.

### Related Documentation

[Organizational Units](Organizational-Units.md)

---

## 16. Group Creation Procedure

### 16.1 Prerequisites

- Authorized administrative account
- Appropriate directory permissions
- Approved group name
- Identified group category
- Identified group scope
- Documented purpose
- Identified group owner

### 16.2 Graphical Method

Using Active Directory Users and Computers:

1. Open Active Directory Users and Computers.
2. Navigate to the intended OU.
3. Right-click the OU.
4. Select **New > Group**.
5. Enter the group name.
6. Select the appropriate group scope.
7. Select Security or Distribution.
8. Create the group.
9. Verify its configuration.
10. Document the result.

### 16.3 PowerShell Example

```powershell
New-ADGroup `
    -Name "GG_ExampleDepartment_Employees" `
    -SamAccountName "GG_ExampleDepartment_Employees" `
    -GroupCategory Security `
    -GroupScope Global `
    -Path "OU=Groups,DC=technicaltechnotech,DC=com" `
    -Description "Example departmental security group"
```

**Execution Status:** Reference Example — Not Executed

The specified OU must exist.

### 16.4 Verification

```powershell
Get-ADGroup -Identity "GG_ExampleDepartment_Employees" |
Select-Object Name,GroupScope,GroupCategory,DistinguishedName
```

### 16.5 Documentation Requirements

Record:

- Group name
- Group category
- Group scope
- Distinguished name
- Purpose
- Group owner
- Members
- Nested groups
- Resource permissions
- Date created
- Change reference

---

## 17. Group Modification Procedure

### 17.1 Common Modifications

- Add members
- Remove members
- Update descriptions
- Change group ownership
- Modify nesting
- Update resource permissions
- Rename groups

### 17.2 Modification Workflow

1. Identify the group.
2. Confirm the requested modification.
3. Review the group's purpose.
4. Assess access implications.
5. Obtain applicable authorization.
6. Implement the change.
7. Verify the result.
8. Document the modification.

### 17.3 Example — Update Group Description

```powershell
Set-ADGroup `
    -Identity "GG_HR_Employees" `
    -Description "Human Resources departmental security group"
```

**Execution Status:** Reference Example — Not Executed

### 17.4 Important

Changing group membership can grant or revoke access.

Privileged groups and sensitive resource groups require additional review.

---

## 18. Group Lifecycle Management

### 18.1 Creation

Create groups when a legitimate administrative or access requirement exists.

### 18.2 Operation

Maintain accurate membership and permission assignments.

### 18.3 Review

Periodically review:

- Group purpose
- Group ownership
- Membership
- Nested groups
- Resource permissions
- Administrative privileges
- Unused groups

### 18.4 Modification

Update groups when organizational requirements change.

### 18.5 Decommissioning

Before deleting a group:

1. Identify the group.
2. Review membership.
3. Identify nested group relationships.
4. Review assigned permissions.
5. Identify dependent applications and resources.
6. Obtain applicable authorization.
7. Remove or migrate dependencies.
8. Delete the group using supported procedures.
9. Verify the impact.
10. Update documentation.

### Important

Deleting a security group can affect access to resources that reference the group's security identifier (SID).

Group deletion should not be performed without dependency review.

---

## 19. Access Review and Auditing

### 19.1 Purpose

Access reviews help verify that users retain only the permissions required for their responsibilities.

### 19.2 Review Objectives

- Identify unnecessary memberships.
- Identify excessive privileges.
- Review administrative groups.
- Review sensitive resource groups.
- Identify unused groups.
- Confirm group ownership.
- Validate group nesting.

### 19.3 Proposed Review Matrix

| Group Category | Review Focus | Status |
|---|---|---|
| Departmental Groups | Membership accuracy | Pending |
| Resource Access Groups | Effective permissions | Pending |
| Administrative Groups | Privileged access | Pending |
| Distribution Groups | Membership and purpose | Pending |
| Nested Groups | Access relationships | Pending |

### 19.4 Group Inventory Command

```powershell
Get-ADGroup -Filter * -Properties Description,ManagedBy |
Select-Object Name,GroupScope,GroupCategory,Description,ManagedBy,DistinguishedName
```

### 19.5 Export Group Inventory

```powershell
Get-ADGroup -Filter * -Properties Description,ManagedBy |
Select-Object Name,GroupScope,GroupCategory,Description,ManagedBy,DistinguishedName |
Export-Csv -Path "C:\Temp\TTT-Group-Inventory.csv" -NoTypeInformation
```

Ensure the destination directory exists before exporting.

### 19.6 Audit Considerations

Relevant security events may include:

- Group creation
- Group deletion
- Membership additions
- Membership removals
- Changes to privileged groups

The availability of these events depends on auditing configuration and the group operation involved.

---

## 20. Group Structure Verification

### 20.1 Verification Objectives

Confirm the actual groups, scopes, categories, memberships, and resource relationships in the TTT domain.

### 20.2 Verification Matrix

| Test ID | Verification | Result |
|---|---|---|
| AD-GRP-001 | Security groups inventoried | Pending |
| AD-GRP-002 | Distribution groups inventoried | Pending |
| AD-GRP-003 | Global group scopes verified | Pending |
| AD-GRP-004 | Domain local group scopes verified | Pending |
| AD-GRP-005 | Group distinguished names verified | Pending |
| AD-GRP-006 | Departmental memberships reviewed | Pending |
| AD-GRP-007 | Nested groups reviewed | Pending |
| AD-GRP-008 | Resource permissions reviewed | Pending |
| AD-GRP-009 | Administrative groups reviewed | Pending |
| AD-GRP-010 | Group ownership documented | Pending |

### 20.3 Evidence Requirements

Each completed verification should include:

- Test identifier
- Date
- Domain controller or management workstation
- Command or administrative tool
- Expected result
- Actual result
- Pass/fail status
- Supporting evidence
- Notes

### 20.4 Evidence Status

**Group Inventory:** Pending Collection

**Membership Reports:** Pending Collection

**Resource Permission Reports:** Pending Collection

**Administrative Access Review:** Pending

---

## 21. Troubleshooting Group-Related Issues

### 21.1 Common Scenarios

| Scenario | Potential Cause | Investigation |
|---|---|---|
| User cannot access a shared folder | Missing group membership | Review group and resource permissions |
| User has excessive access | Unnecessary membership | Review nested groups |
| Permission change not effective | Existing authentication token | Review session and token |
| Group membership update fails | Insufficient permissions | Review administrative delegation |
| Distribution group cannot send email | Messaging system not configured | Review mail infrastructure |
| User retains access after department transfer | Old membership remains | Review account memberships |
| Group not found | Incorrect name or directory location | Search Active Directory |
| Nested access behaves unexpectedly | Scope or nesting configuration | Review group relationships |

### 21.2 Troubleshooting Workflow

1. Identify the affected user.
2. Identify the affected resource.
3. Review the user's group memberships.
4. Review nested groups.
5. Review group scope and category.
6. Review resource permissions.
7. Review effective access.
8. Identify the probable cause.
9. Apply an authorized correction.
10. Verify the result.
11. Document findings.

### 21.3 Example — HR Folder Access

**Scenario:** An HR employee cannot access an authorized departmental folder.

Potential investigation:

1. Verify the employee account.
2. Review departmental security group membership.
3. Review the domain local resource group.
4. Confirm nesting.
5. Review share permissions.
6. Review NTFS permissions.
7. Test effective access.
8. Document the findings.

**Status:** Illustrative Scenario — Not Executed

---

## 22. ITIL 4 Integration

Active Directory group administration supports several ITIL 4 practices.

| Practice | Application |
|---|---|
| Service Desk | Receives group membership and access requests |
| Incident Management | Investigates access failures |
| Service Request Management | Processes authorized access changes |
| Problem Management | Investigates recurring permission issues |
| Change Enablement | Controls significant group and permission changes |
| Knowledge Management | Maintains group administration procedures |
| Monitoring and Event Management | Reviews relevant security events |
| Service Configuration Management | Documents group relationships and dependencies |
| Information Security Management | Enforces least privilege and access control |
| Continual Improvement | Improves access management workflows |

### Example — Employee Department Transfer

**Scenario:** An employee transfers from Sales to HR.

Potential workflow:

1. Service Request Management receives the request.
2. Authorization is verified.
3. IT reviews the employee's existing memberships.
4. Unnecessary Sales access is removed.
5. Approved HR group membership is added.
6. OU placement is reviewed separately.
7. Resource access is tested.
8. The request is documented and closed.

This is an example workflow, not a completed service request.

---

## 23. Service Configuration Management

Active Directory groups are important components of the identity and access management configuration.

### Configuration Attributes

Relevant group attributes include:

- Group name
- Group category
- Group scope
- Distinguished name
- Description
- Group owner
- Members
- Nested groups
- Resource permissions
- Administrative purpose
- Change history

### Configuration Relationships

```text
Active Directory Domain
          |
          v
Security Groups
          |
          +-- Departmental Groups
          |
          +-- Resource Access Groups
          |
          +-- Administrative Groups
          |
          v
Resource Permissions
```

---

## 24. Change Management

Group changes can affect business access and administrative privileges.

### Changes Requiring Review

Examples include:

- Creating a new security group
- Deleting a group
- Modifying privileged group membership
- Changing group nesting
- Updating resource permissions
- Renaming a group
- Changing group scope
- Modifying access control design

### Proposed Change Workflow

1. Identify the requested change.
2. Document the business justification.
3. Identify affected users and resources.
4. Assess access and security impact.
5. Obtain applicable authorization.
6. Prepare implementation steps.
7. Implement the change.
8. Verify the result.
9. Update documentation.
10. Review the outcome.

---

## 25. Security Considerations

### 25.1 Least Privilege

Users should receive only the permissions necessary for their responsibilities.

### 25.2 Group-Based Access

Assign permissions through appropriate security groups where practical.

### 25.3 Privileged Group Protection

Membership in privileged groups should be restricted and reviewed.

### 25.4 Administrative Separation

Separate routine user accounts from privileged administrative accounts where appropriate.

### 25.5 Membership Auditing

Review changes to sensitive groups and maintain relevant audit records.

### 25.6 Periodic Access Reviews

Identify and remove unnecessary access.

### Security Checklist

- [ ] Privileged groups reviewed
- [ ] Departmental memberships reviewed
- [ ] Resource permissions reviewed
- [ ] Nested groups documented
- [ ] Excessive permissions investigated
- [ ] Administrative delegation reviewed
- [ ] Group changes documented

---

## 26. Future Improvements

Potential improvements include:

### Standardized Naming

Apply a consistent naming convention to new groups.

### Access Review Process

Establish a repeatable process for reviewing group membership and permissions.

### Automated Inventory

Develop PowerShell scripts to export group membership and nesting information.

### Administrative Group Separation

Create dedicated groups for specific delegated responsibilities.

### Resource Permission Documentation

Maintain a centralized record of group-to-resource access relationships.

### Onboarding and Offboarding Integration

Connect group membership changes to documented employee lifecycle procedures.

### Hybrid Identity

Evaluate group synchronization and cloud identity integration when Microsoft Entra ID is introduced.

**Microsoft 365 has not yet been deployed for Technical Techno Tech.**

These improvements are proposed rather than completed.

---

## 27. Skills Practiced

This project supports practical experience with:

- Active Directory Domain Services
- Security group administration
- Distribution groups
- Global groups
- Domain local groups
- Universal group concepts
- AGDLP
- Group nesting
- Identity and access management
- NTFS permissions
- Shared folder permissions
- Administrative delegation
- Least privilege
- Access reviews
- PowerShell
- Active Directory Users and Computers
- Active Directory Administrative Center
- Group troubleshooting
- Configuration management
- ITIL-aligned access management

---

## 29. What I Learned

The Technical Techno Tech group structure project demonstrates how Active Directory groups support centralized permission management.

### Key Learning Areas

**1. Security Groups**

Security groups allow permissions to be assigned to collections of accounts.

**2. Distribution Groups**

Distribution groups organize email recipients but do not provide resource access permissions.

**3. Global Groups**

Global groups commonly organize users by department or responsibility.

**4. Domain Local Groups**

Domain local groups commonly represent access to resources.

**5. AGDLP**

AGDLP separates user membership from resource permission assignments.

**6. Group Nesting**

Nested groups simplify permission administration and support scalable access control.

**7. Least Privilege**

Users should receive only the access required for their responsibilities.

**8. Group Membership Management**

Adding and removing group memberships supports employee onboarding, transfers, and offboarding.

**9. Administrative Delegation**

Security groups can help assign limited administrative responsibilities.

**10. Configuration Documentation**

Accurate group inventories support troubleshooting, access reviews, security, and change management.

---

## 30. Final Verification Checklist

### Group Inventory

- [ ] All groups inventoried
- [ ] Group categories verified
- [ ] Group scopes verified
- [ ] Distinguished names documented
- [ ] Group descriptions reviewed
- [ ] Group ownership documented

### Departmental Groups

- [ ] IT groups reviewed
- [ ] Executive groups reviewed
- [ ] HR groups reviewed
- [ ] Sales groups reviewed
- [ ] Membership verified

### Resource Access

- [ ] Domain local groups reviewed
- [ ] Group nesting verified
- [ ] Shared folder permissions reviewed
- [ ] NTFS permissions reviewed
- [ ] Effective access tested

### Distribution Groups

- [ ] Distribution groups identified
- [ ] Membership reviewed
- [ ] Messaging functionality distinguished from directory configuration

### Administrative Security

- [ ] Domain Admins membership reviewed
- [ ] Enterprise Admins membership reviewed
- [ ] Delegated administrative groups reviewed
- [ ] Excessive privileges investigated

### Documentation

- [ ] Group inventory exported
- [ ] Membership evidence collected
- [ ] Resource access relationships documented
- [ ] Screenshots sanitized
- [ ] Unverified information identified
- [ ] Revision history updated

---

## 31. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT Active Directory group structure documentation covering security groups, distribution groups, group scopes, AGDLP, resource permissions, administrative access, and verification procedures |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This document describes Active Directory group management concepts and previously documented group administration exercises associated with the TTT infrastructure.

Exact group names, scopes, memberships, resource permissions, and administrative assignments must be verified against the current domain.

Proposed naming conventions, example commands, future improvements, and illustrative scenarios do not represent completed activities.

All published technical evidence should originate from actual authorized lab work and be sanitized before inclusion in the public GitHub repository.
