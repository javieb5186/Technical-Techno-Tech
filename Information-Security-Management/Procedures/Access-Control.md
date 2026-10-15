# SOP — Access Control

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Information Security Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-ISM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Information Security Management  
**Function:** Internal IT

---

## 1. Purpose

This procedure establishes a standardized approach for controlling access to Technical Techno Tech's information systems, applications, infrastructure, and internal IT services.

Access Control ensures that users, administrators, service accounts, and other authorized identities receive only the permissions necessary to perform their approved responsibilities.

The procedure supports:

- Protection of sensitive information
- Prevention of unauthorized access
- Consistent identity verification
- Least-privilege access
- Role-based access control
- Secure user onboarding and offboarding
- Privileged access management
- Authentication security
- Access monitoring and auditing
- Periodic access reviews
- Regulatory and organizational compliance where applicable
- Reduction of security risks
- Continual improvement

**Key Principle:** Access should be granted only to authorized identities, limited to legitimate business requirements, reviewed periodically, and removed when no longer necessary.

---

## 2. Scope

This procedure applies to identities and systems used to deliver Technical Techno Tech's internal IT services.

### Supported Services

| Service ID | Service Name |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

### Supported Environments

- Windows Server
- Active Directory Domain Services
- Windows 11
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Network infrastructure
- OPNsense
- VyOS

### Access Types

This procedure covers:

1. Standard user access
2. Administrative access
3. Privileged access
4. Application access
5. Shared resource access
6. Remote access
7. Service account access
8. Cloud resource access
9. Temporary access
10. Emergency access

### Scope Limitations

This procedure provides an internal access control framework for a simulated organization.

It does not establish compliance with a specific regulatory framework or certify that security controls are implemented in a production environment.

---

## 3. ITIL 4 Information Security Management

### Purpose

The purpose of Information Security Management is to protect the information needed by the organization to conduct its business.

This includes understanding and managing risks to the confidentiality, integrity, and availability of information.

### The CIA Triad

| Principle | Meaning | Access Control Example |
|---|---|---|
| Confidentiality | Information is accessible only to authorized parties | Restricting HR documents to authorized HR personnel |
| Integrity | Information remains accurate and protected against unauthorized modification | Limiting who can modify Group Policy |
| Availability | Authorized users can access required information and services | Maintaining reliable authentication services |

### Important Definitions

**Access Control:** The process of regulating who or what can access a resource and what actions are permitted.

**Authentication:** Verifying the identity of a user, device, or service.

**Authorization:** Determining what an authenticated identity is permitted to do.

**Accounting / Auditing:** Recording and reviewing access-related activity.

**Identity:** A representation of a user, service, device, or other security principal.

**Security Principal:** An entity that can be authenticated and assigned permissions.

**Least Privilege:** Granting only the permissions required to perform an authorized task.

**Role-Based Access Control (RBAC):** Assigning permissions through roles associated with responsibilities.

**Multi-Factor Authentication (MFA):** Requiring more than one authentication factor.

**Privileged Account:** An account with elevated administrative or security permissions.

**Access Review:** A structured evaluation of whether existing access remains appropriate.

**Separation of Duties:** Dividing sensitive responsibilities to reduce the risk of unauthorized or inappropriate activity.

**Security Group:** A group used to organize identities for permission assignment.

**Access Control List (ACL):** A list of access control entries defining permissions on a resource.

**Conditional Access:** Microsoft Entra ID policy-based access decisions using signals such as identity, application, device, location, and risk, subject to licensing and configuration.

---

## 4. Access Control Principles

Technical Techno Tech follows the principles below.

### 4.1 Least Privilege

Users receive only the permissions necessary for their responsibilities.

### 4.2 Need to Know

Access to sensitive information is limited to identities with a legitimate requirement.

### 4.3 Role-Based Access

Where practical, permissions are assigned through security groups or administrative roles rather than individually.

### 4.4 Default Deny

Access should not be granted without an appropriate authorization basis.

### 4.5 Separation of Duties

Sensitive operations should be divided among appropriate responsibilities when feasible.

### 4.6 Individual Accountability

Administrative activity should be attributable to an identifiable person or appropriately controlled service identity.

### 4.7 Strong Authentication

Authentication controls should reflect the sensitivity of the account and resource.

### 4.8 Periodic Review

Permissions should be reviewed to confirm continued business need.

### 4.9 Prompt Revocation

Access should be removed when no longer authorized.

### 4.10 Traceability

Access requests, approvals, changes, and removals should be documented.

### 4.11 Defense in Depth

Access control should be supported by additional safeguards such as endpoint protection, logging, network segmentation, and security monitoring.

### 4.12 Secure Documentation

Passwords, recovery secrets, tokens, and private keys must not be published in GitHub records.

---

## 5. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Receiving access-related requests
- Verifying request information
- Identifying the requested service
- Performing approved routine access tasks
- Documenting completed actions
- Escalating requests beyond assigned permissions

### Systems Administrator

Responsible for:

- Managing Active Directory accounts and groups
- Configuring Windows permissions
- Managing delegated administrative rights
- Reviewing server access
- Investigating access-related technical issues

### Cloud Administrator

Responsible for:

- Managing Microsoft Entra ID identities
- Reviewing Microsoft 365 access
- Managing supported cloud roles
- Configuring applicable authentication controls
- Reviewing Azure RBAC assignments

### Endpoint Administrator

Responsible for:

- Managing endpoint access configurations
- Reviewing local administrative privileges
- Supporting Intune-managed access controls
- Investigating device-related authentication issues

### Information Security Personnel

Responsible for:

- Establishing access control requirements
- Reviewing privileged access
- Evaluating security risks
- Coordinating access reviews
- Investigating suspicious access activity
- Supporting security exceptions

### Resource Owner

Responsible for:

- Determining legitimate access requirements
- Authorizing appropriate access
- Reviewing access assignments
- Requesting removal when access is no longer needed

### IT Management / Designated Authority

Responsible for:

- Approving access when required by organizational policy
- Resolving access-related conflicts
- Reviewing significant access risks
- Supporting separation-of-duties requirements

**Lab Note:** These roles are simulated responsibilities. One learner may perform multiple roles, but documentation should distinguish technical execution from independent approval.

---

## 6. Access Control Model

Technical Techno Tech uses a proposed role-based access approach.

### Access Control Workflow

```text
Access Requirement Identified
             |
             v
Access Request Submitted
             |
             v
Identity and Request Verified
             |
             v
Business Need Evaluated
             |
             v
Authorization Obtained
             |
             v
Appropriate Role / Group Selected
             |
             v
Access Provisioned
             |
             v
Permissions Verified
             |
             v
Access Documented
             |
             v
Periodic Review
             |
        +----+----+
        |         |
        v         v
    Retain      Modify / Revoke
```

Access may also be provisioned through an authorized predefined workflow when individual approval is not required for each execution.

---

## 7. Access Control Categories

### 7.1 Standard User Access

Permissions required for routine employee responsibilities.

Examples:

- Access to department folders
- Microsoft 365 applications
- Approved business applications
- Standard workstation sign-in

### 7.2 Administrative Access

Permissions required to manage specific systems or services.

Examples:

- Resetting user passwords
- Managing workstations
- Updating approved group memberships
- Managing selected Microsoft 365 settings

### 7.3 Privileged Access

Permissions capable of making significant security or infrastructure changes.

Examples:

- Domain Admins
- Enterprise Admins
- Global Administrator
- Privileged Azure RBAC roles
- Local Administrators

### 7.4 Service Account Access

Permissions assigned to identities used by applications, services, or scheduled processes.

### 7.5 Temporary Access

Permissions granted for a defined task or period.

### 7.6 Emergency Access

Access intended for exceptional recovery or emergency administrative situations.

Emergency access should be controlled, monitored, and reviewed after use.

---

## 8. Access Control Procedure

### Step 1 — Identify the Access Requirement

Determine what resource requires access.

Examples:

- HR shared folder
- Sales shared folder
- Windows Server
- Microsoft 365 mailbox
- Entra ID administrative role
- Azure resource
- Managed workstation

Record:

- Requesting identity
- Requested resource
- Required permissions
- Business justification
- Requested duration
- Resource owner

**Expected Result:** The access requirement is clearly defined.

### Step 2 — Verify the Requesting Identity

Confirm the requester is authorized to submit the request.

Verification methods may include:

- Authenticated service portal
- Established identity verification process
- Approved internal request workflow
- Verification through an authorized manager or resource owner

Do not rely solely on an unverified email or message requesting sensitive access.

**Expected Result:** The requester is appropriately verified.

### Step 3 — Determine the Access Type

Classify the request.

| Access Type | Example |
|---|---|
| Standard | Employee requires departmental folder access |
| Administrative | Technician requires delegated password reset capability |
| Privileged | Administrator requires elevated directory permissions |
| Temporary | Contractor requires time-limited application access |
| Service | Application requires a managed service identity |
| Emergency | Authorized recovery access is required |

**Expected Result:** The access request receives an appropriate classification.

### Step 4 — Evaluate Business Justification

Determine whether access is necessary.

Questions:

1. What task requires access?
2. Is the requested permission level appropriate?
3. Can a lower-privilege role satisfy the requirement?
4. Does the resource contain sensitive information?
5. Is the access temporary or ongoing?
6. Does the request introduce a separation-of-duties conflict?

**Expected Result:** The business need and associated risks are evaluated.

### Step 5 — Identify the Resource Owner

Determine who is authorized to approve access.

Examples:

- Department manager for departmental resources
- Application owner for application access
- Service owner for service administration
- Designated security authority for sensitive privileged access

Approval authority should be defined by organizational policy.

**Expected Result:** The appropriate authorization responsibility is identified.

### Step 6 — Obtain Required Authorization

Confirm that access is approved before provisioning.

### Approval Record

```text
Access Request ID:
REQ-001

Requested Identity:
Example User

Resource:
HR Shared Folder

Requested Access:
Read

Business Justification:
Required for assigned HR responsibilities

Approval Status:
Pending

Approving Role:
Resource Owner
```

This is an illustrative request record.

**Important:** A simulated manager approval must not be represented as independent organizational authorization.

**Expected Result:** Authorization is documented or the request remains pending.

### Step 7 — Identify the Appropriate Permission Method

Select the least-privileged method.

Possible methods:

- Active Directory security group
- NTFS permissions
- Share permissions
- Delegated AD DS permissions
- Microsoft Entra ID role
- Microsoft 365 service role
- Azure RBAC role
- Application-specific role

Prefer established groups or roles where practical.

**Expected Result:** The permission assignment method is selected.

### Step 8 — Review Existing Access

Before granting new permissions, inspect existing assignments.

Check:

- Direct permissions
- Security group memberships
- Nested group memberships
- Inherited permissions
- Existing administrative roles
- Resource-specific access

### Active Directory Example

```powershell
Get-ADPrincipalGroupMembership -Identity "sconner" |
Select-Object Name, GroupCategory, GroupScope
```

This command requires the Active Directory PowerShell module and appropriate access.

**Expected Result:** Existing permissions are understood.

### Step 9 — Evaluate Least Privilege

Determine the minimum permissions required.

### Example

An HR employee needs to read HR documentation.

**Appropriate:** Read access.

**Potentially Excessive:** Full Control.

Full Control may permit permission changes or other operations beyond the employee's responsibilities.

**Expected Result:** The requested permissions are limited appropriately.

### Step 10 — Provision Authorized Access

Perform the approved access change using the appropriate administrative tools.

Possible tools:

- Active Directory Users and Computers
- Active Directory Administrative Center
- Windows PowerShell
- Microsoft Entra Admin Center
- Microsoft 365 Admin Center
- Azure Portal
- Microsoft Intune Admin Center

The following sections provide environment-specific examples.

**Expected Result:** The authorized access configuration is applied.

### Step 11 — Verify Access

Confirm that the intended permission was granted.

Verification may include:

- Reviewing group membership
- Inspecting effective permissions
- Testing access with an authorized test account
- Reviewing role assignments
- Confirming application functionality

Verification should include negative testing where appropriate.

For example:

- Authorized HR user can open the HR folder.
- Unauthorized Sales user cannot open the HR folder.

**Expected Result:** Access behaves according to the approved requirement.

### Step 12 — Document the Access Change

Record:

- Request ID
- Affected identity
- Resource
- Permissions granted
- Approval reference
- Implementing technician
- Date and time
- Verification method
- Actual result
- Related Change record when applicable

**Expected Result:** The access change is traceable.

### Step 13 — Communicate Completion

Notify the requester through an approved communication method.

Include:

- Access request reference
- Resource granted
- Completion status
- Relevant instructions
- Any restrictions

Do not include passwords or secrets in insecure communication.

**Expected Result:** The requester receives appropriate status information.

### Step 14 — Schedule Access Review

Determine whether the access requires periodic review or automatic expiration.

Examples:

- Standard access: periodic review
- Privileged access: more frequent review
- Temporary access: defined expiration
- Emergency access: prompt post-use review

**Expected Result:** Continued authorization can be evaluated.

### Step 15 — Modify or Revoke Access

Remove or modify permissions when:

- Employment ends
- Job responsibilities change
- Temporary access expires
- Business justification no longer exists
- A security concern requires action
- Resource ownership changes

**Expected Result:** Access remains aligned with current authorization.

---

## 9. Access Control — Active Directory Domain Services

Active Directory provides centralized authentication and authorization capabilities for domain environments.

### Common Administrative Tools

- Active Directory Users and Computers (ADUC)
- Active Directory Administrative Center (ADAC)
- Active Directory PowerShell module
- Group Policy Management Console (GPMC)

### Lab Environment

**Domain:** homelab.local

**Domain Controllers:**

| Server | IP Address |
|---|---|
| DC01 | 10.20.10.10 |
| DC02 | 10.20.10.11 |

### Active Directory Security Groups

Security groups can be used to assign permissions to resources.

Example departmental groups:

- HR security group
- Sales security group
- IT security group

Actual group names should be verified against the directory before running commands.

### View User Information

```powershell
Get-ADUser -Identity "sconner" -Properties Enabled, Department |
Select-Object Name, SamAccountName, Enabled, Department
```

### Review Group Membership

```powershell
Get-ADPrincipalGroupMembership -Identity "sconner" |
Select-Object Name, GroupScope, GroupCategory
```

### Add a User to a Security Group

```powershell
Add-ADGroupMember -Identity "HR_Security" -Members "sconner"
```

**Important:** `HR_Security` is an illustrative group name. Verify the actual group, target user, approval, and intended permissions before executing.

### Verify Membership

```powershell
Get-ADGroupMember -Identity "HR_Security"
```

### Remove a User From a Group

```powershell
Remove-ADGroupMember -Identity "HR_Security" -Members "sconner"
```

### Security Considerations

- Avoid unnecessary membership in privileged groups.
- Review nested memberships.
- Use appropriate group scopes.
- Verify the target identity.
- Document authorization.
- Test resulting access.

---

## 10. Active Directory Group Scope and Permissions

Active Directory supports different group scopes.

| Group Scope | Primary Use |
|---|---|
| Global | Organizing accounts and roles within a domain |
| Domain Local | Assigning permissions to resources within a domain |
| Universal | Organizing membership across domains in a forest |

### AGDLP Model

**Accounts → Global Groups → Domain Local Groups → Permissions**

### Example

```text
Sarah Connor
     |
     v
HR_Global
     |
     v
HR_Folder_Access
     |
     v
NTFS Permissions
     |
     v
HR Shared Folder
```

### Purpose

This model separates:

- User membership
- Organizational roles
- Resource access permissions

### Benefits

- Easier access management
- Reduced direct user permissions
- Consistent resource authorization
- Simplified employee onboarding
- Simplified access removal

### Important

AGDLP is a useful design pattern, not a requirement for every environment.

Group nesting rules depend on group scope, domain, and forest relationships.

---

## 11. Access Control — NTFS and Shared Folders

Windows supports file access through NTFS permissions and, for network shares, share permissions.

### Common NTFS Permissions

| Permission | Capability |
|---|---|
| Read | View files and folder contents |
| Read & Execute | Read and execute permitted files |
| List Folder Contents | View directory contents |
| Write | Create or modify permitted content |
| Modify | Read, write, and delete permitted content |
| Full Control | Includes changing permissions and ownership-related capabilities |

### Example — Departmental Folder

```text
D:\Departments\HR
```

### Proposed Permission Model

| Security Principal | Permission |
|---|---|
| SYSTEM | Full Control |
| Administrators | Full Control |
| HR_Folder_Access | Modify |
| Unauthorized users | No intended access |

Actual inherited permissions must be reviewed.

### Inspect NTFS Permissions

```powershell
Get-Acl -Path "D:\Departments\HR" |
Format-List
```

### Alternative — ICACLS

```powershell
icacls "D:\Departments\HR"
```

### Access Verification

Use authorized test accounts to verify:

1. HR user can access the HR folder.
2. HR user can perform permitted operations.
3. Sales user cannot access restricted HR content.
4. Administrative access remains appropriate.

### Important

When accessing a folder through a network share, both share permissions and NTFS permissions affect effective access.

Group membership changes may require a new logon session or refreshed authentication token before they affect access.

---

## 12. Access Control — Delegated Administration

Delegation allows selected administrative tasks to be performed without granting full domain administrative privileges.

### Example

A designated HR support role may be permitted to reset passwords for accounts in a specific Organizational Unit.

### Delegation Workflow

1. Identify the required administrative task.
2. Identify the target OU.
3. Select the authorized security group.
4. Define permitted operations.
5. Apply delegation.
6. Verify permissions.
7. Test with an authorized delegated account.
8. Confirm unrelated administrative actions remain restricted.

### Example

**Permitted:** Reset passwords for authorized HR user accounts.

**Not Permitted:** Create users in unrelated OUs or modify domain-wide settings.

### Administrative Tool

Active Directory Users and Computers:

```text
Active Directory Users and Computers
    |
    v
Select Target OU
    |
    v
Delegate Control
    |
    v
Select Security Group
    |
    v
Select Allowed Tasks
    |
    v
Complete Wizard
```

### Security Considerations

- Delegate to security groups where practical.
- Limit delegation scope.
- Avoid excessive rights.
- Review inherited permissions.
- Test with a nonprivileged account.
- Document delegated responsibilities.

---

## 13. Access Control — Privileged Accounts

Privileged accounts require additional protection because they can make significant system changes.

### Examples

- Domain Admins
- Enterprise Admins
- Global Administrator
- Azure subscription Owner
- Local Administrators

### Privileged Access Principles

1. Use dedicated administrative identities where appropriate.
2. Avoid routine daily work using highly privileged accounts.
3. Apply MFA where supported.
4. Minimize standing privileges.
5. Review privileged role assignments.
6. Monitor privileged activity.
7. Remove unnecessary administrative access.
8. Protect emergency access mechanisms.
9. Avoid shared administrative credentials.
10. Use approved privileged access workflows.

### Example — Active Directory Privileged Membership

```powershell
Get-ADGroupMember -Identity "Domain Admins"
```

### Review Nested Memberships

```powershell
Get-ADGroupMember -Identity "Domain Admins" -Recursive
```

### Important

The `Protected Users` security group provides additional authentication protections for supported Active Directory accounts.

Membership does not automatically establish a complete privileged access management program.

Compatibility and operational requirements should be evaluated before adding accounts.

---

## 14. Access Control — Microsoft Entra ID

Microsoft Entra ID provides identity and access management capabilities for Microsoft cloud services and integrated applications.

### Common Access Controls

- User identities
- Security groups
- Administrative roles
- MFA
- Conditional Access
- Enterprise application assignments
- Authentication methods
- Access reviews where licensed and configured

### Example — Help Desk Role Delegation

**Objective:** Allow an authorized technician to perform selected user administration tasks.

### Proposed Workflow

1. Identify the required administrative tasks.
2. Review the appropriate Entra role.
3. Determine whether a lower-privilege role is sufficient.
4. Identify the technician or role-assignable group.
5. Obtain authorization.
6. Assign the appropriate role.
7. Verify the assignment.
8. Test permitted operations.
9. Document restrictions and limitations.

### Example Roles

| Role | General Purpose |
|---|---|
| Global Administrator | Broad tenant administration |
| User Administrator | Selected user and group administration |
| Helpdesk Administrator | Selected support and password reset functions |
| Authentication Administrator | Selected authentication method management |
| Security Reader | Read access to supported security information |

Role capabilities and restrictions must be verified against current Microsoft documentation and the actual tenant configuration.

### Important

Assigning an administrative role to a group requires supported role-assignable group configuration and appropriate licensing.

An ordinary security group does not automatically support every type of role assignment.

---

## 15. Access Control — Microsoft 365

Microsoft 365 access may involve:

- User accounts
- Licenses
- Administrative roles
- Application access
- SharePoint permissions
- Exchange permissions
- Microsoft Teams access where licensed
- Group-based access

### Access Control Workflow

1. Identify the requested service.
2. Confirm the user's identity.
3. Review licensing requirements.
4. Identify appropriate permissions.
5. Obtain required authorization.
6. Apply the supported assignment.
7. Verify access.
8. Document the result.

### Important

A Microsoft 365 license grants entitlement to applicable services but does not automatically grant administrative permissions.

Similarly, an unlicensed account may retain an identity and certain directory capabilities, but access to specific services depends on licensing and service requirements.

---

## 16. Access Control — Microsoft Intune

Intune access control may involve:

- Administrative RBAC
- Scope groups
- Scope tags
- Device management permissions
- Application deployment permissions
- Device enrollment controls

### Example

**Requirement:** Allow a technician to perform selected endpoint management tasks.

### Proposed Workflow

1. Identify required endpoint tasks.
2. Review available Intune roles.
3. Select the least-privileged role.
4. Define appropriate scope groups.
5. Apply scope tags where necessary.
6. Assign the authorized technician or group.
7. Verify role effectiveness.
8. Test permitted operations.
9. Document results.

### Important

Microsoft Entra administrative roles and Intune RBAC are related but distinct permission systems.

An Entra role does not necessarily provide the same scope or capabilities as a custom Intune role.

---

## 17. Access Control — Microsoft Azure

Azure uses role-based access control to manage access to Azure resources.

### Azure RBAC Components

- Security principal
- Role definition
- Scope
- Role assignment

### Common Azure RBAC Roles

| Role | General Capability |
|---|---|
| Owner | Manage resources and role assignments |
| Contributor | Manage resources without general permission to assign Azure RBAC roles |
| Reader | View resources |
| Virtual Machine Contributor | Manage virtual machines within the role's permissions |

### Azure Scope Hierarchy

```text
Management Group
       |
       v
Subscription
       |
       v
Resource Group
       |
       v
Resource
```

Role assignments may be inherited from broader scopes.

### Example

**Requirement:** Allow an administrator to manage a specific lab virtual machine.

**Preferred Approach:** Evaluate an appropriate role assignment at the narrowest practical scope.

### Security Considerations

- Avoid unnecessary subscription-wide Owner assignments.
- Review inherited permissions.
- Verify the exact role definition.
- Document authorization.
- Review assignments periodically.

### Important

Azure RBAC permissions for Azure resources are separate from Microsoft Entra directory administrative roles.

---

## 18. Authentication and Multi-Factor Authentication

Authentication verifies identity before access is granted.

### Authentication Factors

| Factor | Example |
|---|---|
| Something You Know | Password or PIN |
| Something You Have | Authenticator or security key |
| Something You Are | Biometric characteristic |

### MFA Requirements

Apply MFA according to:

- Account privilege
- Resource sensitivity
- Organizational security requirements
- Licensing
- Technical compatibility

### Recommended Priorities

- Administrative accounts
- Remote access
- Cloud applications
- Sensitive business systems
- Accounts with elevated risk

### Important

MFA improves account security but does not eliminate every authentication threat.

Additional protections may include:

- Phishing-resistant authentication
- Conditional Access
- Sign-in monitoring
- Device compliance
- Privileged access controls

---

## 19. Access Control — User Onboarding

Employee onboarding requires establishing appropriate access for a new identity.

### Proposed Workflow

```text
Approved Onboarding Request
             |
             v
Create User Identity
             |
             v
Assign Department / Role
             |
             v
Apply Approved Group Membership
             |
             v
Assign Required Licenses
             |
             v
Configure Authentication Requirements
             |
             v
Verify Access
             |
             v
Document Completion
```

### Example — Active Directory User

```powershell
Get-ADUser -Identity "sconner" -Properties Department, Enabled
```

### Verify Group Membership

```powershell
Get-ADPrincipalGroupMembership -Identity "sconner" |
Select-Object Name
```

### Onboarding Controls

- Verify approved employment or role information.
- Apply least privilege.
- Use established security groups.
- Avoid unnecessary privileged access.
- Apply required authentication protections.
- Verify authorized access.
- Document completed tasks.

---

## 20. Access Control — Employee Transfers

Employee transfers may require changes to access permissions.

### Examples

- Sales employee transfers to HR.
- Technician moves to a different support role.
- Administrator changes responsibilities.

### Transfer Procedure

1. Confirm the approved role change.
2. Review current access.
3. Identify permissions no longer required.
4. Identify new access requirements.
5. Obtain necessary authorization.
6. Remove obsolete permissions.
7. Grant new permissions.
8. Verify effective access.
9. Document changes.

### Important

Adding new permissions without removing obsolete access can create privilege accumulation.

Access reviews should address this risk.

---

## 21. Access Control — User Offboarding

Offboarding ensures that access is removed when an identity is no longer authorized.

### Potential Actions

- Block sign-in
- Disable on-premises account
- Revoke applicable sessions
- Remove privileged roles
- Remove security group memberships
- Remove application access
- Recover assigned devices
- Review account ownership dependencies
- Address service account dependencies
- Apply data retention requirements
- Remove licenses when appropriate
- Delete identities according to approved retention requirements

### Active Directory Example

```powershell
Disable-ADAccount -Identity "sconner"
```

### Verify Account Status

```powershell
Get-ADUser -Identity "sconner" -Properties Enabled |
Select-Object Name, Enabled
```

### Important

Disabling an Active Directory account does not necessarily terminate every existing session immediately.

Cloud session revocation, token behavior, application sessions, and synchronization dependencies must be considered separately.

### Offboarding Documentation

Record:

- Request reference
- Identity
- Authorized offboarding date
- Actions completed
- Systems reviewed
- Verification results
- Outstanding dependencies
- Completion status

---

## 22. Service Account Access Control

Service accounts are used by applications, services, and automated processes.

### Examples

- Windows services
- Scheduled tasks
- Application integrations
- Automated maintenance
- Background processing

### Security Principles

- Use dedicated service identities.
- Avoid interactive logon where unnecessary.
- Grant only required permissions.
- Document service ownership.
- Protect credentials.
- Review dependencies.
- Monitor account activity.
- Use managed identities where supported.

### Active Directory Options

- Traditional service accounts
- Managed Service Accounts (MSAs)
- Group Managed Service Accounts (gMSAs)

### Important

A gMSA can provide managed password functionality for supported workloads.

Deployment requirements and application compatibility must be verified.

Do not use Domain Admin privileges for ordinary service accounts.

---

## 23. Temporary and Emergency Access

### Temporary Access

Temporary permissions should have:

- Documented justification
- Defined resource scope
- Appropriate authorization
- Expiration or review date
- Verification
- Revocation process

### Emergency Access

Emergency access may be required during:

- Identity service outages
- Administrative lockouts
- Critical infrastructure recovery
- Security response activities

### Emergency Access Controls

1. Establish an approved emergency access method.
2. Protect emergency credentials or authentication methods.
3. Limit use to authorized situations.
4. Record emergency access activity.
5. Review use after the event.
6. Restore normal access controls when appropriate.

### Important

Emergency access should not become a routine workaround for missing administrative permissions.

---

## 24. Access Reviews

Access reviews determine whether permissions remain appropriate.

### Review Categories

- Standard user access
- Departmental resource access
- Administrative roles
- Privileged accounts
- Service accounts
- Temporary access
- Cloud resource permissions

### Proposed Review Frequency

| Access Category | Suggested Review |
|---|---|
| Standard user access | Semiannual |
| Departmental sensitive access | Quarterly |
| Administrative access | Quarterly |
| Highly privileged access | Monthly |
| Temporary access | At expiration |
| Emergency access | After use |

These intervals are proposed lab policy examples, not mandatory ITIL requirements.

### Access Review Procedure

1. Identify the resource or role.
2. Export or inspect current assignments.
3. Identify the responsible reviewer.
4. Evaluate business justification.
5. Identify unnecessary access.
6. Document review decisions.
7. Remove or modify inappropriate permissions.
8. Verify changes.
9. Record completion.

### Possible Decisions

- Retain
- Modify
- Revoke
- Investigate
- Defer with documented justification

---

## 25. Access Monitoring and Auditing

Access-related events may indicate legitimate activity, configuration issues, or security concerns.

### Windows Security Events

| Event ID | Description |
|---|---|
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4720 | User account created |
| 4722 | User account enabled |
| 4725 | User account disabled |
| 4726 | User account deleted |
| 4728 | Member added to a security-enabled global group |
| 4732 | Member added to a security-enabled local group |
| 4756 | Member added to a security-enabled universal group |

Events are recorded only when the relevant activity and auditing configuration support their generation.

### Example — Failed Logons

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4625
    StartTime = (Get-Date).AddHours(-24)
} -MaxEvents 50
```

### Example — Account Management Events

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4720, 4722, 4725, 4726
    StartTime = (Get-Date).AddDays(-7)
} -MaxEvents 50
```

### Security Considerations

- Review relevant events in context.
- Avoid assuming every failed logon is malicious.
- Protect audit records.
- Review privileged activity.
- Escalate suspicious patterns appropriately.

---

## 26. Access Control Records

Access-related activity should be documented.

### Proposed Repository Structure

```text
Information-Security-Management/
├── README.md
├── Procedures/
│   └── Access-Control.md
└── Records/
    └── ACCESS-001-HR-Folder-Permissions/
        ├── README.md
        └── Evidence/
            ├── 01-Access-Request.md
            ├── 02-Authorization.md
            ├── 03-Permission-Configuration.md
            ├── 04-Access-Verification.md
            └── 05-Access-Review.md
```

These filenames are illustrative and should only be created when relevant.

### Record Requirements

- Access request ID
- Requester
- Target identity
- Resource
- Requested permissions
- Business justification
- Authorization status
- Implementing role
- Date and time
- Technical actions
- Verification results
- Review date
- Related records

---

## 27. Access Control Record Template

```text
ACCESS CONTROL RECORD

Access Record ID:
Related Request ID:

Requesting Identity:
Target Identity:
Department / Role:

Resource:
Service ID:
Access Type:
Requested Permissions:

Business Justification:
Resource Owner:
Approval Status:
Approval Reference:

Existing Access:
Proposed Access:
Least-Privilege Assessment:

Implementation Method:
Implementing Role:
Implementation Date/Time:

Verification Method:
Expected Result:
Actual Result:
Verification Status:

Access Expiration:
Next Review Date:

Related Incident:
Related Change:
Related CI:

Current Status:
Outstanding Actions:
Notes:
```

---

## 28. Example Lab Scenario — HR Folder Access

### Scenario Overview

An authorized HR employee requires access to the department's shared folder.

**Scenario ID:** Illustrative  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Environment:** homelab.local

### Objective

Grant authorized HR access while preventing unauthorized departmental access.

### Proposed Access Model

```text
HR Employee
    |
    v
HR_Global
    |
    v
HR_Folder_Access
    |
    v
NTFS Permissions
    |
    v
HR Department Folder
```

Group names are illustrative.

### Step 1 — Review Existing Groups

```powershell
Get-ADGroup -Filter * |
Where-Object Name -like "*HR*" |
Select-Object Name, GroupScope, GroupCategory
```

### Step 2 — Review User Membership

```powershell
Get-ADPrincipalGroupMembership -Identity "sconner" |
Select-Object Name
```

### Step 3 — Review Folder Permissions

```powershell
icacls "D:\Departments\HR"
```

### Step 4 — Confirm Authorization

Verify that the employee is approved for HR folder access.

### Step 5 — Apply Approved Membership

After confirming the actual group name and authorization:

```powershell
Add-ADGroupMember -Identity "HR_Global" -Members "sconner"
```

### Step 6 — Verify Membership

```powershell
Get-ADGroupMember -Identity "HR_Global"
```

### Step 7 — Test Effective Access

Using authorized test accounts:

1. Sign in as an HR user.
2. Attempt to access the HR folder.
3. Confirm permitted operations.
4. Sign in as an unauthorized Sales user.
5. Attempt to access the HR folder.
6. Confirm restricted access.

### Expected Results

| Test | Expected Result |
|---|---|
| Authorized HR user opens folder | Allowed |
| Authorized HR user performs approved operations | Allowed |
| Unauthorized Sales user opens restricted folder | Denied |
| Standard HR user changes folder permissions | Denied unless separately authorized |

### Evidence

Capture:

- Security group configuration
- Group membership
- NTFS permissions
- Authorized access test
- Unauthorized access test
- Relevant timestamps

### Lab Status

This is a reusable scenario design.

Actual group names, access tests, permissions, and results must be verified during execution.

---

## 29. Example Lab Scenario — Delegated Password Reset

### Scenario Overview

A support technician requires permission to reset passwords for users in a designated OU.

### Objective

Demonstrate delegated administration without granting Domain Admin privileges.

### Proposed Workflow

1. Identify the target OU.
2. Identify the support security group.
3. Review the required administrative task.
4. Apply approved delegation.
5. Sign in using a delegated test account.
6. Attempt an authorized password reset.
7. Attempt an unrelated administrative action.
8. Document results.

### Expected Results

**Authorized Task:** Reset a permitted user's password.

**Unauthorized Task:** Perform unrelated domain administration.

### Security Principle

Delegated administration should provide only the permissions necessary for the assigned support function.

### Lab Status

This scenario illustrates a controlled access test. Record actual execution results separately.

---

## 30. Access Control Evidence Standards

Evidence should demonstrate what was actually configured and tested.

### Evidence Types

- Active Directory group membership
- NTFS permission output
- Delegation settings
- Microsoft Entra role assignments
- Azure RBAC assignments
- Intune RBAC configuration
- Authentication policy configuration
- Access review results
- Audit logs
- Authorized test results

### Evidence Requirements

Each item should identify:

1. Source system
2. Collection date and time
3. Administrative tool
4. Target identity or resource
5. Action performed
6. Actual result
7. Related request or change
8. Verification status

### Documentation Standard

Distinguish:

**Requested Access:** What was requested.

**Authorized Access:** What was approved.

**Configured Access:** What was technically assigned.

**Verified Access:** What was confirmed through testing or inspection.

**Effective Access:** What the identity can actually do after considering applicable permissions and restrictions.

These may differ.

---

## 31. Access Control and Service Request Management

Routine access provisioning may be managed through Service Request Management.

### Examples

- Department folder access
- Approved application access
- Standard user onboarding
- Approved group membership changes

### Service Request Responsibilities

- Capture requirements
- Verify requester information
- Obtain required authorization
- Fulfill approved access
- Document actions
- Confirm completion

### Important

Not every access request requires a separate Change record.

The appropriate workflow depends on risk, authorization requirements, and the organization's change model.

---

## 32. Access Control and Incident Management

Access-related incidents may include:

- Unauthorized account access
- Authentication service failure
- Unexpected account lockouts
- Incorrect permissions
- Privileged access misuse
- Account compromise indicators

### Example

**Incident:** Employee cannot access an authorized shared folder.

### Investigation

Review:

- Account status
- Group membership
- NTFS permissions
- Share permissions
- Authentication
- Recent changes
- Effective access

### Important

An access failure may result from incorrect permissions, authentication problems, network issues, or service availability.

Do not assume the cause without investigation.

---

## 33. Access Control and Change Enablement

Some access modifications may require formal Change Enablement.

### Examples

- Domain-wide security policy modifications
- Privileged access model changes
- Major Conditional Access changes
- Administrative role restructuring
- Significant authentication configuration changes

### Change Considerations

- Security risk
- Business impact
- Affected identities
- Service dependencies
- Testing requirements
- Rollback requirements
- Authorization

### Important

Routine approved access provisioning may follow a predefined fulfillment workflow.

Higher-risk security configuration changes may require additional authorization and change control.

---

## 34. Access Control and Service Configuration Management

Access Control may depend on accurate Configuration Item information.

### Examples

- Server ownership
- Administrative responsibility
- Resource dependencies
- Application configuration
- Cloud service ownership
- Security-sensitive infrastructure

### Benefits

- Better resource identification
- Improved access reviews
- More accurate change impact analysis
- Improved security accountability

### Important

A CI record does not automatically grant access or establish permission ownership.

Authorization must follow the applicable access control process.

---

## 35. Access Control and Monitoring and Event Management

Monitoring can help identify access-related conditions.

### Examples

- Repeated failed logons
- Unexpected privileged group membership changes
- Suspicious sign-in activity
- Authentication policy modifications
- Account lockout patterns

### Proposed Workflow

```text
Security-Relevant Event
          |
          v
Event Detection
          |
          v
Alert Triage
          |
          v
Security Significance Assessment
          |
          v
Appropriate Escalation
          |
          v
Investigation / Response
```

### Important

Monitoring alerts are indicators requiring evaluation.

An alert alone does not prove unauthorized activity.

---

## 36. Access Control and Continual Improvement

Access Control activities may identify opportunities to improve security and administration.

### Examples

- Excessive group membership
- Outdated privileged access
- Inconsistent onboarding
- Delayed offboarding
- Missing access approvals
- Incomplete access reviews
- Poor role definitions
- Unnecessary direct permissions

### Example Improvement Record

```text
Improvement ID:
IMP-001

Source:
Access Review

Finding:
Some departmental folder permissions
are assigned directly to user accounts.

Proposed Improvement:
Use approved security groups for
consistent resource access management.

Owner:
To Be Assigned

Status:
Proposed
```

This is an illustrative improvement opportunity.

---

## 37. Common Access Control Errors

### Error 1 — Excessive Permissions

**Incorrect:** Granting Full Control when Read access is sufficient.

**Correct:** Apply least privilege.

### Error 2 — Direct Permissions Everywhere

**Incorrect:** Assigning individual users directly to every resource.

**Correct:** Use appropriate groups and roles where practical.

### Error 3 — Unverified Authorization

**Incorrect:** Granting sensitive access based only on an unverified message.

**Correct:** Confirm requester identity and required authorization.

### Error 4 — Privileged Daily-Use Accounts

**Incorrect:** Using Domain Admin credentials for ordinary workstation activities.

**Correct:** Separate routine and privileged responsibilities where appropriate.

### Error 5 — Ignoring Nested Groups

**Incorrect:** Reviewing only direct membership.

**Correct:** Evaluate effective access and nested memberships.

### Error 6 — Failing to Remove Old Access

**Incorrect:** Granting new departmental access while retaining unnecessary previous permissions.

**Correct:** Review access during role changes.

### Error 7 — Assuming MFA Solves Every Security Risk

**Incorrect:** Treating MFA as complete account protection.

**Correct:** Combine MFA with appropriate authorization, monitoring, and security controls.

### Error 8 — Confusing Authentication and Authorization

**Incorrect:** Assuming successful sign-in means access to every resource is permitted.

**Correct:** Verify authentication and authorization separately.

### Error 9 — Failing to Test Access

**Incorrect:** Assuming group membership guarantees the intended effective permissions.

**Correct:** Verify actual access.

### Error 10 — Publishing Secrets

**Incorrect:** Storing passwords, tokens, or private keys in GitHub.

**Correct:** Exclude secrets from public documentation.

### Error 11 — Treating Simulated Approval as Independent Approval

**Incorrect:** Recording a fictional manager's authorization as an actual organizational decision.

**Correct:** Clearly identify simulated approvals.

---

## 38. Access Control Quality Checklist

### Request Evaluation

- [ ] Access requirement identified
- [ ] Requester identity verified
- [ ] Target identity confirmed
- [ ] Resource identified
- [ ] Business justification documented
- [ ] Access type classified
- [ ] Resource owner identified

### Authorization

- [ ] Required approval obtained
- [ ] Least privilege evaluated
- [ ] Separation of duties considered
- [ ] Temporary access duration defined where applicable
- [ ] Privileged access requirements reviewed
- [ ] Approval evidence documented

### Implementation

- [ ] Existing permissions reviewed
- [ ] Correct group or role selected
- [ ] Appropriate scope confirmed
- [ ] Access configured
- [ ] No unnecessary privileges granted
- [ ] Configuration documented

### Verification

- [ ] Assigned permissions inspected
- [ ] Authorized access tested
- [ ] Unauthorized access tested where appropriate
- [ ] Effective access evaluated
- [ ] Actual results recorded
- [ ] Unexpected results investigated

### Security

- [ ] MFA requirements reviewed
- [ ] Privileged access restrictions considered
- [ ] Sensitive information protected
- [ ] Credentials excluded from documentation
- [ ] Audit requirements considered

### Lifecycle

- [ ] Access review requirements identified
- [ ] Expiration recorded where applicable
- [ ] Transfer requirements considered
- [ ] Offboarding requirements considered
- [ ] Access revocation process documented
- [ ] Outstanding actions assigned

---

## 39. Access Control Performance Metrics

Access Control effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Access Request Fulfillment Time | Measures time required to fulfill approved access requests |
| Access Review Completion Rate | Tracks completion of scheduled reviews |
| Unauthorized Access Findings | Tracks confirmed inappropriate access |
| Excessive Privilege Findings | Identifies permissions beyond business requirements |
| Privileged Access Review Coverage | Measures review of elevated permissions |
| Offboarding Access Removal Time | Measures delay between authorized termination trigger and access removal |
| Temporary Access Expiration Compliance | Tracks timely removal of temporary permissions |
| Access Verification Rate | Measures completed access testing |
| Access Documentation Completeness | Evaluates record quality |
| MFA Coverage | Measures applicable identities protected by MFA |
| Direct Permission Reduction | Tracks movement toward group-based access where appropriate |
| Access Revocation Completion Rate | Measures completed removal actions |

### Example Calculations

**Access Review Completion Rate**

```text
Access Review Completion Rate (%) =
Completed Access Reviews
------------------------ x 100
Scheduled Access Reviews
```

**Access Verification Rate**

```text
Access Verification Rate (%) =
Verified Access Changes
----------------------- x 100
Total Implemented Access Changes
```

**Temporary Access Expiration Compliance**

```text
Expiration Compliance (%) =
Temporary Access Grants Revoked On Time
--------------------------------------- x 100
Temporary Access Grants Due for Revocation
```

### Measurement Considerations

- Define the measurement period.
- Use actual timestamps.
- Distinguish simulated data from real observations.
- Do not invent completion rates.
- Document exceptions.
- Review trends over time.

---

## 40. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Receives and routes access-related support requests |
| Incident Management | Responds to access failures and related service disruptions |
| Service Request Management | Coordinates approved access provisioning and removal |
| Knowledge Management | Maintains access control and troubleshooting documentation |
| Problem Management | Investigates recurring access-related issues |
| Change Enablement | Controls applicable security configuration changes |
| Monitoring and Event Management | Detects access-related events and alerts |
| Service Configuration Management | Identifies systems and services requiring controlled access |
| Information Security Management | Establishes access control requirements and manages associated risks |
| Continual Improvement | Improves access governance, reviews, and administrative procedures |

---

## 41. Related Procedures and Documentation

### Information Security Management

- [Information Security Management Overview](../README.md)

### Service Desk

- [Service Desk Overview](../../Service-Desk/)
- [Ticket Intake](../../Service-Desk/Procedures/Ticket-Intake.md)
- [Ticket Categorization](../../Service-Desk/Procedures/Ticket-Categorization.md)
- [Ticket Prioritization](../../Service-Desk/Procedures/Ticket-Prioritization.md)
- [Ticket Escalation](../../Service-Desk/Procedures/Ticket-Escalation.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Logging](../../Incident-Management/Procedures/Incident-Logging.md)
- [Incident Investigation](../../Incident-Management/Procedures/Incident-Investigation.md)
- [Incident Resolution](../../Incident-Management/Procedures/Incident-Resolution.md)
- [Incident Closure](../../Incident-Management/Procedures/Incident-Closure.md)

### Service Request Management

- [Service Request Management Overview](../../Service-Request-Management/)

### Knowledge Management

- [Knowledge Management Overview](../../Knowledge-Management/)
- [Knowledge Article Lifecycle](../../Knowledge-Management/Procedures/Knowledge-Article-Lifecycle.md)

### Problem Management

- [Problem Management Overview](../../Problem-Management/)
- [Problem Identification](../../Problem-Management/Procedures/Problem-Identification.md)
- [Root Cause Analysis](../../Problem-Management/Procedures/Root-Cause-Analysis.md)

### Change Enablement

- [Change Enablement Overview](../../Change-Enablement/)
- [Change Authorization](../../Change-Enablement/Procedures/Change-Authorization.md)
- [Change Implementation](../../Change-Enablement/Procedures/Change-Implementation.md)
- [Change Review](../../Change-Enablement/Procedures/Change-Review.md)

### Monitoring and Event Management

- [Monitoring and Event Management Overview](../../Monitoring-and-Event-Management/)
- [Event Detection](../../Monitoring-and-Event-Management/Procedures/Event-Detection.md)
- [Alert Triage](../../Monitoring-and-Event-Management/Procedures/Alert-Triage.md)
- [Event Escalation](../../Monitoring-and-Event-Management/Procedures/Event-Escalation.md)

### Service Configuration Management

- [Service Configuration Management Overview](../../Service-Configuration-Management/)
- [Configuration Item Management](../../Service-Configuration-Management/Procedures/Configuration-Item-Management.md)

### Continual Improvement

- [Continual Improvement Overview](../../Continual-Improvement/)

### Infrastructure Documentation

- [Infrastructure Overview](../../Infrastructure/)
- [Active Directory](../../Infrastructure/Active-Directory/)
- [Windows Server](../../Infrastructure/Windows-Server/)
- [Microsoft 365](../../Infrastructure/Microsoft-365/)
- [Networking](../../Infrastructure/Networking/)
- [Virtualization](../../Infrastructure/Virtualization/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

---

## 42. Procedure Review

This procedure should be reviewed when:

- Access control requirements change.
- New infrastructure technologies are introduced.
- Administrative responsibilities change.
- Authentication requirements are updated.
- Microsoft 365 or Entra ID configurations change.
- Privileged access policies change.
- Access reviews identify significant weaknesses.
- Security incidents reveal control deficiencies.
- Employee lifecycle processes change.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Access Control procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Organizational roles, resource owners, access approval workflows, business requirements, employee requests, and operational scenarios may be simulated.

Active Directory configuration, Windows permissions, Microsoft 365 administration, Entra ID roles, Intune RBAC, Azure RBAC, authentication settings, access reviews, and technical findings are documented based on hands-on lab activities where indicated.

Proposed access assignments, security controls, administrative delegations, and cloud configurations must not be represented as implemented or verified without supporting evidence.

Expected access results and hypothetical security findings must not be represented as actual observations.

Simulated approvals do not constitute independent organizational authorization.

GitHub publication does not imply production security operations, regulatory compliance, independent security approval, or employment experience.

This procedure demonstrates ITIL-aligned Information Security Management, identity and access administration, least privilege, role-based access control, privileged access management, access verification, auditing, lifecycle management, and security documentation practices.
