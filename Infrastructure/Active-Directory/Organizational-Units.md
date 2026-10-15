# Technical Techno Tech — Active Directory Organizational Units

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Configuration  
**Document ID:** INF-AD-002  
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

This document describes the organizational unit (OU) structure used within Technical Techno Tech's Active Directory environment.

It provides a centralized reference for:

- Organizational unit hierarchy
- Departmental organization
- User and computer account placement
- Administrative delegation
- Group Policy application
- Distinguished names
- OU management
- Security considerations
- Configuration verification
- Troubleshooting
- Change management

The document supports centralized identity administration and ITIL 4 service management practices.

---

## 2. Environment Overview

Technical Techno Tech uses Active Directory Domain Services to manage internal identities, computers, groups, and administrative responsibilities.

### Active Directory Environment

| Component | Configuration |
|---|---|
| Domain | `technicaltechnotech.com` |
| Forest Root | `technicaltechnotech.com` |
| Domain Controllers | DC01 and DC02 |
| Administrative Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Server Network | `10.20.10.0/24` |
| Client Network | `10.20.20.0/24` |
| Management Network | `10.20.30.0/24` |

### OU Design Objectives

1. Organize directory objects.
2. Separate departmental identities.
3. Support administrative delegation.
4. Simplify Group Policy targeting.
5. Improve account management.
6. Maintain consistent object placement.
7. Support scalable directory administration.
8. Reduce unnecessary administrative complexity.

---

## 3. Understanding Organizational Units

An organizational unit is an Active Directory container used to organize directory objects.

OUs can contain:

- User accounts
- Computer accounts
- Groups
- Other organizational units
- Supported directory objects

### Primary Functions

**Organization**

Group related directory objects into manageable structures.

**Administrative Delegation**

Assign specific administrative permissions over an OU or its contents.

**Group Policy**

Link Group Policy Objects to an OU to configure applicable users and computers.

### Important Distinction

An OU is not a security group.

| Organizational Unit | Security Group |
|---|---|
| Organizes directory objects | Groups security principals |
| Supports administrative delegation | Supports permission assignment |
| Supports GPO linking | Can be used for GPO security filtering |
| Represents a directory container | Represents group membership |
| Does not directly grant resource access | Can be assigned resource permissions |

**Memory Hook:** OUs organize objects; security groups manage access.

---

## 4. TTT Organizational Unit Structure

Previous TTT Active Directory lab work included the following organizational units:

- IT
- Executives
- HR
- Sales
- Groups
- Workstations

These OUs represent departments and administrative categories within the fictional organization.

### 4.1 Documented Logical Structure

```text
technicaltechnotech.com
│
├── IT
│
├── Executives
│
├── HR
│
├── Sales
│
├── Groups
│
└── Workstations
```

**Verification Note:** This represents the previously documented logical structure. The current OU hierarchy and distinguished names must be confirmed in Active Directory.

### 4.2 OU Inventory

| OU ID | OU Name | Purpose | Current Status |
|---|---|---|---|
| OU-001 | IT | IT personnel and administration | Previously Configured |
| OU-002 | Executives | Executive personnel | Previously Configured |
| OU-003 | HR | Human Resources personnel | Previously Configured |
| OU-004 | Sales | Sales personnel | Previously Configured |
| OU-005 | Groups | Centralized group organization | Previously Configured |
| OU-006 | Workstations | Employee computer objects | Previously Configured |

The OU identifiers are documentation references, not native Active Directory object identifiers.

---

## 5. Organizational Unit — IT

### 5.1 Purpose

The IT OU organizes directory objects associated with Technical Techno Tech's internal IT personnel.

### 5.2 Intended Responsibilities

IT personnel may perform authorized activities involving:

- User account administration
- Computer account administration
- Password resets
- Group membership management
- Windows Server administration
- Infrastructure troubleshooting
- Technical support

Actual permissions depend on group membership, delegated rights, and other access controls.

### 5.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-001 |
| OU Name | IT |
| Purpose | IT personnel organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 5.4 Security Considerations

- Apply least privilege.
- Use dedicated administrative accounts where appropriate.
- Avoid unnecessary Domain Admins membership.
- Review delegated permissions.
- Separate administrative responsibilities from ordinary user access.

### 5.5 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "IT"' |
Select-Object Name,DistinguishedName
```

---

## 6. Organizational Unit — Executives

### 6.1 Purpose

The Executives OU organizes user accounts associated with company leadership.

### 6.2 Example Personnel

Previous lab exercises included Bruce Wayne as an executive user.

This represents a fictional employee identity.

### 6.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-002 |
| OU Name | Executives |
| Purpose | Executive user organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 6.4 Administrative Considerations

Executive accounts may require:

- Standardized account configuration
- Appropriate resource access
- Security policies
- Account lifecycle management
- Authorized support procedures

Executive status alone should not automatically grant elevated IT privileges.

### 6.5 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "Executives"' |
Select-Object Name,DistinguishedName
```

---

## 7. Organizational Unit — HR

### 7.1 Purpose

The HR OU organizes Human Resources user accounts.

### 7.2 Intended Responsibilities

HR users may require access to approved departmental resources.

Examples include:

- HR shared folders
- Departmental applications
- Employee documentation
- Authorized internal resources

### 7.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-003 |
| OU Name | HR |
| Purpose | Human Resources user organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 7.4 Administrative Delegation

Previous Active Directory lab work included an exercise involving delegated password reset permissions.

The current TTT delegation configuration must be verified.

### 7.5 Security Considerations

HR resources may contain sensitive business information.

Access should be controlled through appropriate security groups and resource permissions rather than OU membership alone.

### 7.6 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "HR"' |
Select-Object Name,DistinguishedName
```

---

## 8. Organizational Unit — Sales

### 8.1 Purpose

The Sales OU organizes user accounts associated with the Sales department.

### 8.2 Intended Responsibilities

Sales users may require access to:

- Sales shared folders
- Departmental resources
- Approved applications
- Internal business systems

### 8.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-004 |
| OU Name | Sales |
| Purpose | Sales personnel organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 8.4 Access Management

Access to Sales resources should be managed through security groups and permissions.

Placing an account inside the Sales OU does not automatically grant access to Sales files or applications.

### 8.5 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "Sales"' |
Select-Object Name,DistinguishedName
```

---

## 9. Organizational Unit — Groups

### 9.1 Purpose

The Groups OU provides a centralized location for organizing Active Directory group objects.

### 9.2 Group Categories

The OU may contain:

- Departmental security groups
- Resource access groups
- Administrative groups
- Distribution groups

Actual group placement should be verified.

### 9.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-005 |
| OU Name | Groups |
| Purpose | Group object organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 9.4 Group Management

Previous lab work included:

- Global security groups
- Domain local security groups
- Distribution groups
- Group nesting
- Group-based resource access

### 9.5 AGDLP Model

A common approach to Active Directory permission management is AGDLP.

```text
Accounts
   |
   v
Global Groups
   |
   v
Domain Local Groups
   |
   v
Permissions
```

### 9.6 Important Distinction

The Groups OU organizes group objects.

The groups themselves provide membership and permission-management functionality.

### 9.7 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "Groups"' |
Select-Object Name,DistinguishedName
```

List groups and their locations:

```powershell
Get-ADGroup -Filter * |
Select-Object Name,GroupScope,GroupCategory,DistinguishedName
```

### Related Documentation

[Group Structure](Group-Structure.md)

---

## 10. Organizational Unit — Workstations

### 10.1 Purpose

The Workstations OU organizes employee computer objects.

### 10.2 TTT Workstation Environment

| Hostname | IP Address | Purpose |
|---|---|---|
| CLIENT01 | `10.20.20.10` | Employee workstation |
| MGMT01 | `10.20.30.10` | Administrative workstation |

The current OU placement of each computer object requires verification.

### 10.3 Configuration

| Attribute | Value |
|---|---|
| OU ID | OU-006 |
| OU Name | Workstations |
| Purpose | Computer object organization |
| Parent Container | Pending Verification |
| Distinguished Name | Pending Verification |
| Linked GPOs | Pending Verification |
| Delegated Permissions | Pending Verification |

### 10.4 Group Policy Applications

The Workstations OU can support computer-targeted Group Policy settings such as:

- Windows Firewall configuration
- Security auditing
- Windows security settings
- Desktop configuration
- Administrative restrictions
- Other supported workstation policies

Specific GPO assignments must be verified.

### 10.5 Administrative Considerations

Separating workstations from servers allows different policies and administrative procedures to be applied.

A dedicated administrative workstation may also require additional security controls.

### 10.6 Verification

```powershell
Get-ADOrganizationalUnit -Filter 'Name -eq "Workstations"' |
Select-Object Name,DistinguishedName
```

Review computer locations:

```powershell
Get-ADComputer -Filter * |
Select-Object Name,DistinguishedName
```

---

## 11. Distinguished Names

### 11.1 Overview

A distinguished name (DN) identifies an object's location within Active Directory.

It describes the object's position in the directory hierarchy.

### 11.2 Distinguished Name Components

| Component | Meaning |
|---|---|
| CN | Common Name |
| OU | Organizational Unit |
| DC | Domain Component |

### 11.3 Example

If the HR OU is located directly beneath the domain root, its DN would be:

```text
OU=HR,DC=technicaltechnotech,DC=com
```

A user inside that OU might have a DN similar to:

```text
CN=Example User,OU=HR,DC=technicaltechnotech,DC=com
```

These are illustrative examples.

### 11.4 Verification

```powershell
Get-ADOrganizationalUnit -Filter * |
Select-Object Name,DistinguishedName
```

### 11.5 Importance

Distinguished names are used in:

- PowerShell administration
- Directory searches
- Object creation
- Object movement
- Administrative delegation
- LDAP operations

---

## 12. User Account Placement

### 12.1 Overview

User accounts should be placed in organizational units that support the company's administrative structure.

### 12.2 Example Departmental Placement

| Department | Intended OU |
|---|---|
| IT | IT |
| Executives | Executives |
| Human Resources | HR |
| Sales | Sales |

Actual placement should be based on verified directory configuration.

### 12.3 Previous Lab Accounts

Previous Active Directory exercises included fictional identities such as:

- Bruce Wayne
- Diana Prince
- Sarah Connor

Additional accounts were used in departmental administration exercises.

Their current existence, department assignments, and OU locations in the TTT domain require verification.

### 12.4 User Inventory Command

```powershell
Get-ADUser -Filter * -Properties Department |
Select-Object Name,SamAccountName,Department,DistinguishedName
```

### 12.5 Account Placement Procedure

1. Identify the user's department.
2. Confirm the appropriate OU.
3. Create or locate the user account.
4. Assign the required account attributes.
5. Move the account if necessary.
6. Assign approved security group memberships.
7. Verify account placement.
8. Document the result.

---

## 13. Computer Account Placement

### 13.1 Overview

Computer accounts represent domain-joined devices within Active Directory.

### 13.2 TTT Computers

| Computer | Purpose | OU Placement |
|---|---|---|
| CLIENT01 | Employee workstation | Pending Verification |
| MGMT01 | Management workstation | Pending Verification |
| DC01 | Domain controller | Domain Controllers container — Verify |
| DC02 | Domain controller | Domain Controllers container — Verify |

### 13.3 Domain Controllers

Domain controllers are normally located in the built-in Domain Controllers OU.

This allows domain-controller-specific policies to be applied.

The actual locations of DC01 and DC02 should be verified.

### 13.4 Computer Verification

```powershell
Get-ADComputer -Filter * |
Select-Object Name,DistinguishedName
```

### 13.5 Design Considerations

- Separate workstations from domain controllers.
- Apply appropriate computer policies.
- Document administrative ownership.
- Review stale computer objects.
- Avoid unnecessary computer object movement.

---

## 14. Creating Organizational Units

### 14.1 Purpose

Establish a consistent method for creating new OUs.

### 14.2 Prerequisites

- Authorized administrative account
- Appropriate permissions
- Active Directory connectivity
- Approved OU name
- Identified parent container
- Documented administrative purpose

### 14.3 Graphical Method

Using Active Directory Users and Computers:

1. Open Active Directory Users and Computers.
2. Navigate to the intended parent container.
3. Right-click the parent container.
4. Select **New > Organizational Unit**.
5. Enter the OU name.
6. Review accidental deletion protection.
7. Create the OU.
8. Verify its location.

### 14.4 PowerShell Method

Example: Create a new OU at the domain root.

```powershell
New-ADOrganizationalUnit `
    -Name "ExampleDepartment" `
    -Path "DC=technicaltechnotech,DC=com" `
    -ProtectedFromAccidentalDeletion $true
```

**Execution Status:** Reference Example — Not Executed

### 14.5 Verification

```powershell
Get-ADOrganizationalUnit -Identity "OU=ExampleDepartment,DC=technicaltechnotech,DC=com"
```

### 14.6 Documentation Requirements

Record:

- OU name
- Distinguished name
- Purpose
- Parent container
- Administrative owner
- Delegated permissions
- GPO links
- Date created
- Change reference

---

## 15. Moving Active Directory Objects

### 15.1 Overview

Active Directory objects can be moved between organizational units when organizational or administrative requirements change.

### 15.2 Example Scenarios

- Employee changes departments.
- Computer is assigned a new administrative classification.
- Directory structure is reorganized.
- User account is placed in the wrong OU.

### 15.3 PowerShell Example

Move an example user into the HR OU:

```powershell
Move-ADObject `
    -Identity "CN=Example User,CN=Users,DC=technicaltechnotech,DC=com" `
    -TargetPath "OU=HR,DC=technicaltechnotech,DC=com"
```

This command assumes the example source and destination paths exist.

**Execution Status:** Reference Example — Not Executed

### 15.4 Verification

```powershell
Get-ADUser -Identity "exampleuser" |
Select-Object Name,DistinguishedName
```

### 15.5 Important Considerations

Moving an object can affect:

- Group Policy application
- Delegated administration
- Object management
- Inherited directory permissions

Moving a user to a different OU does not automatically change the user's security group memberships.

### 15.6 Recommended Procedure

1. Identify the object.
2. Confirm the current location.
3. Identify the destination OU.
4. Review GPO and delegation implications.
5. Obtain authorization if required.
6. Move the object.
7. Verify the new location.
8. Confirm expected functionality.
9. Document the change.

---

## 16. Administrative Delegation

### 16.1 Overview

Administrative delegation allows specific management responsibilities to be assigned over an OU or its objects.

This supports least privilege by reducing the need for broad domain administrative access.

### 16.2 Delegation Examples

- Reset user passwords.
- Unlock user accounts.
- Manage selected user attributes.
- Create or delete specific object types.
- Manage computer accounts.

### 16.3 TTT Lab Experience

Previous Active Directory exercises included delegating password reset responsibilities within an organizational unit.

The current delegation assignments must be verified.

### 16.4 Delegation Example

**Scenario:** An authorized HR support account needs permission to reset passwords for users within the HR OU.

Potential implementation:

1. Identify the required task.
2. Identify the authorized account or security group.
3. Open Active Directory Users and Computers.
4. Locate the HR OU.
5. Launch the Delegation of Control Wizard.
6. Select the account or group.
7. Assign the required password reset permissions.
8. Complete the wizard.
9. Test using the delegated account.
10. Confirm that unrelated administrative permissions were not granted.
11. Document the result.

### 16.5 Security Considerations

- Delegate to security groups where practical.
- Avoid unnecessary broad permissions.
- Test delegated access.
- Review inherited permissions.
- Periodically review delegation assignments.

### 16.6 Verification Checklist

- [ ] Delegated accounts identified
- [ ] Delegated groups identified
- [ ] Permissions reviewed
- [ ] Authorized tasks tested
- [ ] Unauthorized tasks tested
- [ ] Evidence recorded

---

## 17. Group Policy and OU Relationships

### 17.1 Overview

Group Policy Objects can be linked to domains, sites, and organizational units.

OU placement helps determine which policies apply to users and computers.

### 17.2 Group Policy Processing

The general processing order is:

```text
Local
  |
  v
Site
  |
  v
Domain
  |
  v
Organizational Unit
```

This is commonly remembered as **LSDOU**.

Nested OU processing, inheritance, enforcement, security filtering, WMI filtering, and other settings can affect the final policy result.

### 17.3 TTT GPO Planning

| OU | Potential Policy Focus |
|---|---|
| IT | Administrative workstation and user settings |
| Executives | Executive workstation and user settings |
| HR | Departmental user settings |
| Sales | Departmental user settings |
| Groups | Group object organization; GPO linking generally not the primary purpose |
| Workstations | Computer security and configuration |

These are potential applications, not confirmed GPO deployments.

### 17.4 GPO Verification

List GPOs:

```powershell
Get-GPO -All
```

Review inheritance for the HR OU:

```powershell
Get-GPInheritance -Target "OU=HR,DC=technicaltechnotech,DC=com"
```

Review policy results on a workstation:

```powershell
gpresult /r
```

### 17.5 Important

Group Policy application depends on the applicable user or computer scope and policy processing rules.

A GPO linked to an OU containing only group objects does not automatically apply settings to the group's members.

### 17.6 Verification Checklist

- [ ] Existing GPOs inventoried
- [ ] OU links documented
- [ ] Inheritance reviewed
- [ ] Security filtering reviewed
- [ ] Policy processing tested
- [ ] Results documented

---

## 18. OU Security and Protection

### 18.1 Security Objectives

- Prevent unauthorized directory changes.
- Protect important organizational structures.
- Restrict administrative permissions.
- Reduce accidental deletion.
- Maintain traceability.

### 18.2 Accidental Deletion Protection

Active Directory supports protection against accidental deletion.

### Verification

```powershell
Get-ADOrganizationalUnit -Filter * -Properties ProtectedFromAccidentalDeletion |
Select-Object Name,ProtectedFromAccidentalDeletion
```

### 18.3 Administrative Permissions

OU permissions should be reviewed when:

- Delegation changes
- Department responsibilities change
- New administrative accounts are introduced
- Security incidents occur
- Directory restructuring is planned

### 18.4 Security Checklist

- [ ] Accidental deletion protection reviewed
- [ ] Delegated permissions documented
- [ ] Excessive privileges reviewed
- [ ] Administrative groups reviewed
- [ ] Sensitive OUs identified
- [ ] Changes documented

---

## 19. OU Naming Standards

### 19.1 Naming Objectives

A consistent naming convention improves directory administration.

### 19.2 Current OU Names

| OU | Naming Category |
|---|---|
| IT | Department |
| Executives | Department |
| HR | Department |
| Sales | Department |
| Groups | Administrative |
| Workstations | Device |

### 19.3 Naming Recommendations

- Use descriptive names.
- Avoid unnecessary abbreviations.
- Maintain consistent capitalization.
- Avoid duplicate names at the same hierarchy level.
- Document OU purpose.
- Keep the structure manageable.

### 19.4 Future OU Examples

Potential future OUs include:

- Servers
- Service Accounts
- Administrative Accounts
- Disabled Accounts

These are proposed additions and are not documented as existing.

---

## 20. OU Lifecycle Management

### 20.1 Creation

Create an OU when there is a justified administrative, organizational, or policy requirement.

### 20.2 Modification

Update OU configuration when responsibilities or policies change.

### 20.3 Object Management

Maintain accurate placement of user, computer, and group objects.

### 20.4 Review

Periodically review:

- OU purpose
- Object placement
- Delegation
- GPO links
- Accidental deletion protection
- Unused structures

### 20.5 Decommissioning

Before removing an OU:

1. Identify contained objects.
2. Review GPO links.
3. Review delegated permissions.
4. Identify dependencies.
5. Obtain applicable authorization.
6. Relocate or remove objects appropriately.
7. Verify the impact.
8. Remove the OU using supported procedures.
9. Update documentation.

OU deletion should not be performed without reviewing the objects and permissions involved.

---

## 21. OU Inventory Verification

### 21.1 Purpose

Confirm the actual Active Directory organizational unit structure.

### 21.2 Inventory Command

```powershell
Get-ADOrganizationalUnit -Filter * -Properties Description,ProtectedFromAccidentalDeletion |
Select-Object Name,DistinguishedName,Description,ProtectedFromAccidentalDeletion |
Sort-Object DistinguishedName
```

### 21.3 Export OU Inventory

```powershell
Get-ADOrganizationalUnit -Filter * -Properties Description,ProtectedFromAccidentalDeletion |
Select-Object Name,DistinguishedName,Description,ProtectedFromAccidentalDeletion |
Export-Csv -Path "C:\Temp\TTT-OU-Inventory.csv" -NoTypeInformation
```

Ensure the destination directory exists before exporting.

### 21.4 Verification Matrix

| Test ID | Verification | Result |
|---|---|---|
| AD-OU-001 | IT OU exists | Pending |
| AD-OU-002 | Executives OU exists | Pending |
| AD-OU-003 | HR OU exists | Pending |
| AD-OU-004 | Sales OU exists | Pending |
| AD-OU-005 | Groups OU exists | Pending |
| AD-OU-006 | Workstations OU exists | Pending |
| AD-OU-007 | Distinguished names verified | Pending |
| AD-OU-008 | Object placement reviewed | Pending |
| AD-OU-009 | Delegation reviewed | Pending |
| AD-OU-010 | GPO links reviewed | Pending |

### 21.5 Evidence Requirements

Each completed verification should record:

- Test ID
- Date
- Domain controller or management workstation
- Command or tool
- Expected result
- Actual result
- Pass/fail status
- Supporting evidence
- Notes

---

## 22. Troubleshooting OU-Related Issues

### 22.1 Common Scenarios

| Scenario | Potential Cause | Investigation |
|---|---|---|
| User receives unexpected GPO settings | Incorrect OU placement or GPO inheritance | Review object DN and GPO results |
| Help Desk cannot reset password | Missing delegation | Review OU permissions |
| User account created in wrong location | Incorrect creation path | Review object DN |
| Workstation policy not applying | Incorrect computer OU or policy scope | Review computer location and GPO |
| OU cannot be deleted | Accidental deletion protection or permissions | Review OU security |
| Object cannot be moved | Insufficient permissions | Review source and destination permissions |
| Group access unchanged after OU move | Group membership not modified | Review security groups |

### 22.2 Troubleshooting Workflow

1. Identify the affected object.
2. Confirm its current distinguished name.
3. Review OU hierarchy.
4. Check delegated permissions.
5. Review applicable GPOs.
6. Check relevant security groups.
7. Identify the probable cause.
8. Apply an authorized correction.
9. Verify the result.
10. Document findings.

### 22.3 Example — Incorrect User Placement

**Scenario:** A user assigned to HR is located in the Sales OU.

**Potential Impact:** Unexpected GPO application or administrative scope.

**Investigation:**

1. Locate the account.
2. Confirm its distinguished name.
3. Review department attributes.
4. Confirm the intended OU.
5. Review potential policy changes.
6. Move the account if authorized.
7. Verify its new location.
8. Confirm expected policy processing.

**Status:** Illustrative Scenario — Not Executed

---

## 23. ITIL 4 Integration

Organizational unit administration supports multiple ITIL 4 practices.

| Practice | Application |
|---|---|
| Service Desk | Receives account administration requests |
| Incident Management | Investigates access or policy failures |
| Service Request Management | Processes authorized account changes |
| Problem Management | Investigates recurring OU or delegation issues |
| Change Enablement | Controls OU restructuring and permission changes |
| Knowledge Management | Documents OU administration procedures |
| Monitoring and Event Management | Reviews relevant directory events |
| Service Configuration Management | Maintains directory configuration records |
| Information Security Management | Manages delegation and administrative access |
| Continual Improvement | Improves directory organization and workflows |

### Example — Department Transfer

**Scenario:** An employee transfers from Sales to HR.

Potential workflow:

1. Service Request Management receives the transfer request.
2. The request is assessed and authorized.
3. IT verifies the employee's current account configuration.
4. Appropriate security group memberships are reviewed.
5. The user account is moved to the intended OU if required.
6. Applicable Group Policy changes are evaluated.
7. Access permissions are updated.
8. Changes are verified.
9. The request is documented and closed.

This is an example operational workflow.

---

## 24. Service Configuration Management

OU structures are part of the Active Directory configuration.

### Configuration Attributes

Relevant attributes include:

- OU name
- Distinguished name
- Parent container
- Description
- Object types
- Administrative ownership
- Delegated permissions
- Linked GPOs
- Accidental deletion protection
- Change history

### Configuration Relationships

```text
Active Directory Domain
          |
          v
Organizational Units
          |
          +-- User Accounts
          |
          +-- Computer Accounts
          |
          +-- Group Objects
          |
          +-- GPO Links
          |
          +-- Delegated Permissions
```

---

## 25. Change Management

OU changes may affect administrative permissions and Group Policy processing.

### Changes Requiring Review

Examples include:

- Creating an OU
- Deleting an OU
- Renaming an OU
- Moving directory objects
- Changing delegated permissions
- Modifying GPO links
- Restructuring the OU hierarchy

### Proposed Change Workflow

1. Identify the requested change.
2. Document the justification.
3. Identify affected objects.
4. Review GPO and delegation dependencies.
5. Assess potential impact.
6. Obtain applicable authorization.
7. Prepare implementation steps.
8. Prepare a recovery plan.
9. Implement the change.
10. Verify the result.
11. Update documentation.
12. Review the outcome.

---

## 26. Future Improvements

Potential improvements include:

### Administrative Account Separation

Create a dedicated structure for privileged administrative accounts.

### Service Account Organization

Establish appropriate organization for service accounts.

### Computer Management

Review whether additional workstation or server OUs would improve policy targeting.

### Delegation Documentation

Maintain a detailed record of delegated administrative permissions.

### Group Policy Documentation

Create a centralized inventory of GPO links and policy scopes.

### PowerShell Automation

Develop scripts to:

- Inventory OUs
- Validate object placement
- Review OU protection
- Export configuration information
- Identify unexpected changes

These improvements are proposed and not documented as completed.

---

## 27. Skills Practiced

This project supports practical experience with:

- Active Directory Domain Services
- Organizational unit management
- Active Directory Users and Computers
- Active Directory Administrative Center
- Distinguished names
- LDAP directory structure
- User account administration
- Computer account administration
- Security group organization
- Administrative delegation
- Group Policy targeting
- PowerShell
- Identity and access management
- Least privilege
- Configuration management
- Technical documentation
- ITIL-aligned service operations

---

## 29. What I Learned

The Technical Techno Tech OU project demonstrates how Active Directory structures support centralized administration.

### Key Learning Areas

**1. Organizational Units**

OUs organize directory objects and support delegation and Group Policy.

**2. Security Groups**

Security groups manage membership and access permissions.

**3. Distinguished Names**

Distinguished names identify where objects exist in the directory.

**4. Administrative Delegation**

Specific administrative responsibilities can be assigned without granting full domain administration.

**5. Group Policy**

OU placement influences which policies apply to users and computers.

**6. Object Management**

User and computer objects can be created, moved, and managed through administrative tools or PowerShell.

**7. Security**

Accidental deletion protection and least privilege help protect directory structures.

**8. Configuration Management**

Documenting OU structures supports troubleshooting, administration, and change management.

---

## 30. Final Verification Checklist

### OU Structure

- [ ] IT OU verified
- [ ] Executives OU verified
- [ ] HR OU verified
- [ ] Sales OU verified
- [ ] Groups OU verified
- [ ] Workstations OU verified
- [ ] OU hierarchy documented
- [ ] Distinguished names recorded

### Object Placement

- [ ] User account locations reviewed
- [ ] Computer account locations reviewed
- [ ] Group object locations reviewed
- [ ] Domain controller locations verified

### Security and Administration

- [ ] Delegated permissions reviewed
- [ ] Accidental deletion protection reviewed
- [ ] Administrative ownership documented
- [ ] Excessive privileges reviewed

### Group Policy

- [ ] GPO links inventoried
- [ ] GPO inheritance reviewed
- [ ] Policy application tested
- [ ] Unexpected policy behavior investigated

### Documentation

- [ ] PowerShell inventory captured
- [ ] Screenshots sanitized
- [ ] Verification results recorded
- [ ] Unverified information identified
- [ ] Revision history updated

---

## 31. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT organizational unit documentation covering departmental structure, object placement, administrative delegation, Group Policy, and verification procedures |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This document describes the organizational unit structure associated with the TTT Active Directory environment.

Previously documented lab configurations are included for continuity. Exact distinguished names, object placement, delegated permissions, and GPO links require verification against the current domain.

Example commands, proposed procedures, and illustrative scenarios do not represent completed activities.

All published technical evidence should originate from actual authorized lab work and be sanitized before inclusion in the public GitHub repository.
