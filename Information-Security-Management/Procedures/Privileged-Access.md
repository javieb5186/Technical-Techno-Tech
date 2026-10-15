# SOP — Privileged Access Management

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Information Security Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-ISM-002  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**Function:** Internal IT  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

## 1. Purpose

This Standard Operating Procedure establishes a consistent process for requesting, authorizing, provisioning, monitoring, reviewing, and revoking privileged access within Technical Techno Tech.

Privileged Access Management (PAM) protects administrative identities and permissions capable of modifying critical infrastructure, security configurations, user accounts, and business services.

This procedure supports:

- Least-privilege administration
- Protection of privileged identities
- Role-based access control (RBAC)
- Separation of administrative and standard user accounts
- Just-in-time (JIT) access where supported
- Privileged access monitoring
- Secure administrative authentication
- Emergency access management
- Periodic access reviews
- Timely privilege revocation
- Accountability and auditability
- Reduced risk of unauthorized administrative activity

**Key Principle:** Privileged permissions should be granted only when justified, restricted to the minimum necessary scope, protected by appropriate authentication controls, and removed when no longer required.

---

## 2. Scope

This procedure applies to administrative identities and elevated permissions used to manage Technical Techno Tech's internal IT infrastructure.

### Supported Services

| Service ID | Service |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

### Supported Environments

- Active Directory Domain Services
- Windows Server
- Windows 11
- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- OPNsense
- VyOS
- Network infrastructure

### Privileged Identity Types

- Dedicated administrative user accounts
- Domain administrative accounts
- Cloud administrative accounts
- Local administrator accounts
- Service accounts
- Managed service accounts
- Emergency access accounts
- Automation identities
- Privileged application identities

### Scope Limitations

This procedure describes the intended privileged access management process.

It does not imply that a commercial PAM platform, Microsoft Entra Privileged Identity Management (PIM), automated approval workflow, or centralized monitoring solution has been deployed.

Capabilities requiring specific licensing, integrations, or infrastructure must be verified before implementation.

---

## 3. ITIL 4 Alignment

Privileged Access Management supports the ITIL 4 Information Security Management practice.

### Information Security Management Purpose

Protect the information needed by the organization to conduct its business.

Privileged Access Management contributes to the protection of:

**Confidentiality:** Preventing unauthorized disclosure of sensitive information.

**Integrity:** Preventing unauthorized or inappropriate modification of systems and data.

**Availability:** Reducing the likelihood that misuse of administrative permissions disrupts critical services.

### Related ITIL Practices

Privileged access activities may interact with:

- Service Request Management
- Service Desk
- Incident Management
- Problem Management
- Change Enablement
- Monitoring and Event Management
- Service Configuration Management
- Knowledge Management
- Continual Improvement

**Important:** ITIL 4 does not prescribe one mandatory PAM technology, administrative account naming convention, or approval workflow.

The controls in this document represent proposed internal procedures for Technical Techno Tech.

---

## 4. Key Terminology

| Term | Definition |
|---|---|
| Privileged Access | Permissions allowing sensitive administrative or security-related actions |
| Privileged Account | An identity with elevated permissions |
| PAM | Processes and technologies used to control privileged access |
| Least Privilege | Granting only the permissions necessary for an authorized task |
| RBAC | Assigning permissions according to defined roles |
| JIT Access | Providing elevated permissions only when needed |
| JEA | PowerShell Just Enough Administration, which restricts available administrative commands and capabilities |
| PIM | Microsoft Entra Privileged Identity Management |
| MFA | Multi-Factor Authentication |
| Standing Privilege | Elevated access continuously assigned to an identity |
| Privilege Elevation | Temporarily or permanently increasing permissions |
| Separation of Duties | Dividing sensitive responsibilities to reduce misuse and conflicts |
| Break-Glass Account | Emergency administrative identity used for exceptional recovery scenarios |
| Privileged Session | A session operating with elevated administrative permissions |
| Access Review | Evaluation of whether existing permissions remain appropriate |
| Service Principal | An application or service identity used for authentication and authorization |
| Managed Identity | An identity managed by a supported platform for application or resource authentication |

---

## 5. Privileged Access Principles

Technical Techno Tech follows these proposed principles.

### 5.1 Least Privilege

Assign only the permissions required for an approved task.

### 5.2 Separate Administrative Identities

Use dedicated administrative accounts where practical.

Routine activities should not require highly privileged accounts.

### 5.3 Minimize Standing Access

Prefer temporary or eligible privileged assignments when supported.

### 5.4 Strong Authentication

Protect administrative access using appropriate authentication methods.

Phishing-resistant MFA should be considered for high-risk privileged roles where supported.

### 5.5 Restricted Scope

Assign permissions at the narrowest practical resource or administrative scope.

### 5.6 Individual Accountability

Privileged activity should be attributable to an authorized individual or controlled workload identity.

### 5.7 Separation of Duties

Sensitive administrative actions should involve independent authorization or review where feasible.

### 5.8 Continuous Oversight

Review privileged assignments and relevant administrative activity.

### 5.9 Prompt Revocation

Remove privileged access when authorization expires or responsibilities change.

### 5.10 Emergency Preparedness

Maintain appropriately secured emergency access methods for critical recovery scenarios.

### 5.11 Secure Documentation

Never store privileged passwords, private keys, tokens, or recovery secrets in public GitHub documentation.

---

## 6. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Receiving privileged access requests
- Verifying request details
- Recording business justification
- Routing requests for authorization
- Escalating unauthorized or suspicious requests
- Documenting approved support actions

Service Desk personnel must not grant privileges beyond their assigned administrative authority.

### Systems Administrator

Responsible for:

- Managing authorized Windows and AD DS administrative access
- Reviewing privileged security group memberships
- Configuring delegated administrative permissions
- Maintaining appropriate administrative account separation
- Verifying privilege changes

### Cloud Administrator

Responsible for:

- Managing authorized Microsoft Entra administrative roles
- Reviewing Microsoft 365 administrative assignments
- Managing applicable Azure RBAC assignments
- Supporting privileged cloud access verification

### Endpoint Administrator

Responsible for:

- Reviewing endpoint administrative permissions
- Managing authorized local administrator access
- Supporting endpoint privilege restrictions
- Reviewing Intune administrative assignments

### Information Security Personnel

Responsible for:

- Defining privileged access security requirements
- Reviewing high-risk access requests
- Evaluating excessive permissions
- Coordinating privileged access reviews
- Investigating suspicious privileged activity
- Reviewing emergency access usage

### Resource or Service Owner

Responsible for:

- Confirming the business need for privileged access
- Identifying appropriate administrative responsibilities
- Authorizing access within their assigned authority
- Participating in periodic access reviews

### Designated Change Authority

Responsible for authorizing changes when privileged access modifications fall under an applicable Change Enablement model.

**Lab Note:** These roles are simulated. A single learner may perform multiple technical responsibilities, but simulated approval must not be represented as independent authorization.

---

## 7. Privileged Access Classification

Privileged access should be classified according to its potential impact.

| Classification | Examples | General Risk |
|---|---|---|
| Local Administrative | Local administrator on a designated workstation | Moderate to High |
| Delegated Administrative | Password reset permissions for a specific OU | Moderate |
| Server Administrative | Administrator on a designated server | High |
| Domain Administrative | Domain Admins membership | Critical |
| Forest Administrative | Enterprise Admins membership | Critical |
| Cloud Administrative | Global Administrator | Critical |
| Scoped Cloud Administrative | Selected Entra or Intune role | Varies |
| Azure Resource Administrative | Contributor or Owner assignment | High to Critical |
| Security Administrative | Security configuration and policy management | High to Critical |
| Workload Privileged | Service identity with elevated application permissions | Varies |

Risk depends on actual permissions, scope, resource sensitivity, and available safeguards.

A scoped role may still be high risk if it controls a critical service.

---

## 8. Privileged Access Lifecycle

```text
Privileged Access Requirement
             |
             v
Request Submission
             |
             v
Identity Verification
             |
             v
Business Justification Review
             |
             v
Risk and Least-Privilege Assessment
             |
             v
Authorization
             |
             v
Role or Permission Assignment
             |
             v
Technical Verification
             |
             v
Privileged Activity Monitoring
             |
             v
Periodic Access Review
             |
       +-----+-----+
       |           |
       v           v
    Retain      Modify / Revoke
```

Temporary privileges should expire or be removed according to their authorization conditions.

---

# 9. Privileged Access Management Procedure

## Step 1 — Identify the Administrative Requirement

Determine which administrative task requires elevated permissions.

Examples:

- Resetting passwords for a designated OU
- Managing a specific Windows Server
- Modifying approved Microsoft 365 settings
- Managing selected Intune devices
- Administering a specific Azure resource group
- Troubleshooting a domain controller

Record:

- Requesting identity
- Administrative task
- Target system or service
- Requested permissions
- Business justification
- Expected duration

**Expected Result:** The administrative requirement is documented.

---

## Step 2 — Verify the Requester

Confirm the requester's identity using an approved verification process.

Acceptable approaches may include:

- Authenticated internal request system
- Established identity verification procedure
- Confirmed organizational request
- Authorized manager or resource owner verification

Do not approve sensitive administrative access solely because a request appears to originate from an executive or administrator.

**Expected Result:** The requesting identity is verified.

---

## Step 3 — Determine Whether Privileged Access Is Necessary

Evaluate whether the task can be completed without elevated permissions.

Questions:

1. Does the task require administrative rights?
2. Can an existing delegated role perform it?
3. Can the task be completed through a predefined support workflow?
4. Is a less-privileged account sufficient?
5. Is the requested scope broader than necessary?

### Example

**Task:** Reset a password for a user in the HR OU.

**Excessive Permission:** Domain Admins.

**Preferred Approach:** Appropriately delegated password reset permissions for the designated OU.

**Expected Result:** The minimum necessary privilege level is identified.

---

## Step 4 — Identify the Target Environment

Classify the target system.

| Environment | Permission Mechanism |
|---|---|
| Active Directory | Security groups and delegated permissions |
| Windows Server | Local groups, domain groups, and applicable access controls |
| Microsoft Entra ID | Directory roles |
| Microsoft 365 | Service-specific administrative roles |
| Microsoft Intune | Intune RBAC |
| Microsoft Azure | Azure RBAC |
| Network Devices | Device-specific administrative roles |
| Hyper-V | Supported virtualization platform roles |

**Expected Result:** The correct administrative permission system is identified.

---

## Step 5 — Review Existing Privileges

Determine what access the identity already possesses.

Review:

- Direct permissions
- Group membership
- Nested group membership
- Administrative role assignments
- Resource scope
- Temporary privileges
- Existing access restrictions

### Active Directory Example

```powershell
Get-ADPrincipalGroupMembership -Identity "sconner" |
Select-Object Name, GroupScope, GroupCategory
```

### Nested Group Review

```powershell
Get-ADGroupMember -Identity "Domain Admins" -Recursive
```

**Expected Result:** Existing permissions are understood before changes are made.

---

## Step 6 — Perform a Privilege Risk Assessment

Evaluate the risks associated with the requested access.

### Assessment Factors

- Sensitivity of the target system
- Scope of administrative control
- Ability to modify identities
- Ability to change security policies
- Potential impact on service availability
- Access duration
- Authentication protections
- Existing monitoring
- Separation-of-duties concerns

### Proposed Risk Matrix

| Impact \ Likelihood | Low | Medium | High |
|---|---|---|---|
| High | Medium | High | Critical |
| Medium | Low | Medium | High |
| Low | Low | Low | Medium |

This matrix is a proposed internal assessment model.

**Expected Result:** The request receives an appropriate risk assessment.

---

## Step 7 — Select the Least-Privileged Role

Choose the narrowest permission set capable of performing the approved task.

### Examples

| Task | Potential Appropriate Access |
|---|---|
| Reset selected AD user passwords | Delegated OU permissions |
| View security information | Appropriate read-only security role |
| Manage selected Intune devices | Scoped Intune RBAC assignment |
| View Azure resources | Reader at the appropriate scope |
| Manage one Azure resource group | Appropriate resource-scoped role |
| Perform domain-wide administration | Domain-level privileged role only when justified |

Actual role capabilities must be verified before assignment.

**Expected Result:** A suitable role or permission set is selected.

---

## Step 8 — Determine Access Duration

Classify the assignment as:

- Permanent, subject to periodic review
- Temporary
- Task-specific
- Emergency

### Example

```text
Requested Access:
Administrative access to a designated server

Duration:
Two hours

Reason:
Approved maintenance task

Expiration:
After maintenance completion
```

Where automated expiration is unavailable, a manual removal task and verification must be documented.

**Expected Result:** The authorization period is defined.

---

## Step 9 — Obtain Required Authorization

Identify the appropriate approving authority.

### Proposed Authorization Model

| Privilege Level | Suggested Authorization |
|---|---|
| Routine delegated access | Designated resource or service owner |
| Server administration | Systems administration authority |
| High-risk administrative role | Designated management and security review |
| Domain-wide privilege | Designated high-risk access authority |
| Tenant-wide privilege | Designated high-risk cloud access authority |
| Emergency access | Predefined emergency access policy and post-use review |

These are proposed approval responsibilities, not evidence of an implemented workflow.

### Authorization Record

```text
Privileged Access Request:
PAM-001

Requested Identity:
Example Administrator

Requested Role:
Delegated Password Reset

Target Scope:
HR OU

Business Justification:
Authorized support responsibilities

Authorization Status:
Pending

Approving Role:
Designated Resource Owner
```

**Expected Result:** Required authorization is documented before provisioning, except where an approved emergency process applies.

---

## Step 10 — Prepare the Administrative Identity

Determine whether a dedicated administrative identity is appropriate.

### Example Naming Convention

```text
Standard Account:
jdoe

Administrative Account:
adm-jdoe
```

These names are illustrative.

### Administrative Identity Requirements

- Unique identification
- Appropriate authentication protection
- Minimum necessary privileges
- Documented ownership
- Restricted routine use
- Defined review requirements

### Important

Creating a separate administrative account does not automatically secure it.

Authentication, permissions, monitoring, and account lifecycle controls must also be applied.

**Expected Result:** The administrative identity is suitable for the intended role.

---

## Step 11 — Provision Authorized Privileges

Apply the approved role or permission assignment.

Provisioning must occur only after:

1. Confirming the correct identity
2. Confirming the correct resource
3. Reviewing the approved scope
4. Confirming required authorization
5. Identifying the correct administrative tool

### Possible Tools

- Active Directory Users and Computers
- Active Directory Administrative Center
- PowerShell
- Microsoft Entra Admin Center
- Microsoft 365 Admin Center
- Microsoft Intune Admin Center
- Azure Portal
- Windows administrative tools

**Expected Result:** Only the authorized privileges are assigned.

---

## Step 12 — Verify the Privilege Assignment

Confirm that the intended administrative permissions were applied.

### Verification Methods

- Review security group membership
- Inspect role assignments
- Test authorized administrative operations
- Verify the assigned resource scope
- Test prohibited operations where safe and appropriate

### Example

**Authorized:** Technician resets a password within the delegated HR OU.

**Unauthorized:** Technician modifies unrelated domain-wide security settings.

### Important

A successful role assignment does not prove that every intended administrative task works correctly.

Functional testing may still be required.

**Expected Result:** Privileged access is verified.

---

## Step 13 — Record the Assignment

Document:

- PAM request ID
- Administrative identity
- Target resource
- Assigned role
- Permission scope
- Business justification
- Authorization reference
- Implementation method
- Date and time
- Verification result
- Expiration date
- Review requirements

**Expected Result:** The assignment is traceable.

---

## Step 14 — Monitor Privileged Activity

Review relevant administrative events.

Potential monitoring sources:

- Windows Security Event Log
- Active Directory auditing
- Microsoft Entra audit logs
- Microsoft Entra sign-in logs
- Azure Activity Log
- Microsoft 365 audit capabilities
- Endpoint management logs
- Network device logs

### Monitoring Objectives

- Identify unexpected privileged assignments
- Detect suspicious administrative sign-ins
- Identify unauthorized configuration changes
- Review unusual account activity
- Support incident investigation

**Expected Result:** Relevant privileged activity can be investigated using available evidence.

---

## Step 15 — Review Continued Business Need

Evaluate whether the assignment remains appropriate.

Review:

1. Current job responsibilities
2. Existing privileges
3. Resource scope
4. Last known administrative use
5. Access expiration
6. Security concerns
7. Available lower-privilege alternatives

**Expected Result:** Privileged access remains justified or is identified for modification.

---

## Step 16 — Revoke Unnecessary Privileges

Remove privileged access when:

- The task is complete
- The authorization period expires
- The user changes responsibilities
- The user leaves the organization
- The access is no longer required
- A security decision requires revocation

### Revocation Requirements

- Identify all relevant assignments.
- Remove unnecessary permissions.
- Review nested group access.
- Consider active sessions and tokens.
- Verify the final permission state.
- Document completion.

**Expected Result:** Unnecessary privileged access is removed.

---

## Step 17 — Close the Privileged Access Record

Confirm:

- Requested task completed or appropriately cancelled
- Authorization documented
- Provisioning recorded
- Verification performed
- Monitoring requirements addressed
- Temporary access revoked when required
- Outstanding issues identified

**Expected Result:** The privileged access activity is documented and closed appropriately.

---

# 10. Privileged Access — Active Directory

Active Directory contains security-sensitive administrative roles.

### Common Privileged Groups

| Group | General Purpose |
|---|---|
| Domain Admins | Broad administration within a domain |
| Enterprise Admins | Forest-wide administrative capabilities |
| Schema Admins | Active Directory schema administration |
| Administrators | Broad administrative permissions in the applicable context |
| Account Operators | Selected account administration capabilities |
| Backup Operators | Backup and restore capabilities |
| Server Operators | Selected server administration capabilities on domain controllers |

Built-in group privileges depend on the specific group, system, and directory configuration.

Membership should not be granted solely because a group name appears related to a task.

## 10.1 Review Domain Administrators

```powershell
Get-ADGroupMember -Identity "Domain Admins"
```

### Recursive Review

```powershell
Get-ADGroupMember -Identity "Domain Admins" -Recursive
```

### Verification Questions

- Who has Domain Admin membership?
- Is each assignment justified?
- Are dedicated administrative accounts used?
- Are any memberships unnecessary?
- Are privileged identities appropriately protected?

## 10.2 Review Enterprise Administrators

```powershell
Get-ADGroupMember -Identity "Enterprise Admins"
```

The command should be run with appropriate directory access in an environment where the group is available.

## 10.3 Delegation Instead of Domain Admin

### Scenario

A Help Desk technician requires password reset permissions for HR users.

### Preferred Approach

Delegate the required operation on the appropriate Organizational Unit.

### Proposed Workflow

```text
HR Support Requirement
         |
         v
Identify HR OU
         |
         v
Identify Support Group
         |
         v
Delegate Password Reset
         |
         v
Verify Authorized Operation
         |
         v
Verify Unrelated Actions Remain Restricted
```

### Benefits

- Reduced administrative risk
- More precise permissions
- Easier access review
- Improved separation of duties

---

# 11. Privileged Access — Protected Users

Active Directory provides a **Protected Users** security group that applies additional authentication protections to supported domain accounts.

### Purpose

Reduce exposure to certain credential theft and authentication risks.

### Considerations

Membership can affect authentication behavior and compatibility.

Before assigning an account:

1. Confirm domain and client compatibility.
2. Review authentication requirements.
3. Evaluate service and application dependencies.
4. Test with an appropriate noncritical account.
5. Confirm the account can still perform required tasks.
6. Document results.

### Review Membership

```powershell
Get-ADGroupMember -Identity "Protected Users"
```

### Important

Protected Users membership is not equivalent to:

- A complete PAM solution
- MFA
- Just-in-time privilege elevation
- Privileged session recording
- Automatic administrative approval

It is one potential component of a broader privileged identity protection strategy.

---

# 12. Privileged Access — Windows Server

Windows Server administrative permissions may include:

- Local Administrators membership
- Domain administrative groups
- Delegated server administration
- Service-specific administrative permissions
- Remote management permissions

## 12.1 Review Local Administrators

On a supported member server or workstation:

```powershell
Get-LocalGroupMember -Group "Administrators"
```

### Important

The LocalAccounts module and local group cmdlets are not applicable in the same way on domain controllers, which do not maintain ordinary local user and group databases.

Use appropriate domain administrative tools when reviewing domain controller privileges.

## 12.2 Server Administrative Access

### Proposed Workflow

1. Identify the target server.
2. Confirm the required task.
3. Review existing access.
4. Select an appropriate administrative group or delegation.
5. Obtain authorization.
6. Assign access.
7. Verify permitted operations.
8. Document results.
9. Revoke temporary access when complete.

### Security Considerations

- Avoid broad administrative group membership.
- Restrict remote administrative access.
- Protect administrative credentials.
- Review remote management settings.
- Monitor privileged sign-ins.

---

# 13. Privileged Access — PowerShell JEA

PowerShell Just Enough Administration (JEA) can restrict administrative tasks exposed through configured PowerShell endpoints.

### Purpose

Allow authorized users to perform specific administrative functions without granting unrestricted administrative access.

### Example Use Case

A Help Desk technician needs to restart an approved Windows service but should not receive general server administrator privileges.

### Conceptual Workflow

```text
Help Desk Technician
         |
         v
Authorized JEA Endpoint
         |
         v
Permitted Commands Only
         |
         v
Specific Administrative Task
```

### JEA Implementation Considerations

A functional deployment requires appropriate configuration of:

- Role capability files
- Session configuration files
- Endpoint registration
- Identity-to-role mappings
- Allowed commands
- Logging
- Security testing

### Important

JEA is not automatically enabled by installing PowerShell.

A restricted endpoint must be deliberately configured and tested.

**Lab Status:** Proposed advanced lab capability; no JEA endpoint deployment is claimed.

---

# 14. Privileged Access — Microsoft Entra ID

Microsoft Entra ID supports administrative roles for managing directory and cloud identity resources.

### Example Roles

| Role | General Function |
|---|---|
| Global Administrator | Broad Microsoft Entra administrative authority |
| Privileged Role Administrator | Management of supported privileged role assignments |
| User Administrator | Selected user and group administration |
| Helpdesk Administrator | Selected support and password reset tasks |
| Authentication Administrator | Selected authentication method administration |
| Security Reader | Read access to supported security information |

Role capabilities and limitations should be verified against current Microsoft documentation.

## 14.1 Role Assignment Procedure

1. Identify the required administrative task.
2. Review available roles.
3. Select the least-privileged role.
4. Confirm the target identity.
5. Review assignment scope where supported.
6. Obtain authorization.
7. Assign the role.
8. Verify the assignment.
9. Test relevant operations.
10. Document results.

## 14.2 Group-Based Role Assignment

Microsoft Entra supports role assignment through appropriately configured role-assignable groups.

### Important

Role-assignable groups have specific creation, management, and licensing requirements.

An ordinary security group cannot automatically be assumed to support all Microsoft Entra role assignments.

## 14.3 Separate Administrative Accounts

Where appropriate:

```text
Standard Identity:
jdoe@company.example

Administrative Identity:
adm-jdoe@company.example
```

These addresses are illustrative.

### Security Requirements

- Appropriate authentication protection
- Restricted administrative use
- Role assignment review
- Audit logging
- Secure recovery procedures

---

# 15. Microsoft Entra Privileged Identity Management

Microsoft Entra Privileged Identity Management (PIM) supports governance of certain privileged role assignments and eligible access.

### Potential Capabilities

Depending on licensing and configuration:

- Eligible role assignments
- Time-limited role activation
- MFA requirements for activation
- Approval requirements
- Activation justification
- Role assignment reviews
- Privileged access alerts

### Conceptual Workflow

```text
Eligible Administrator
          |
          v
Request Role Activation
          |
          v
Satisfy Activation Requirements
          |
          v
Approval If Required
          |
          v
Temporary Role Activation
          |
          v
Perform Authorized Task
          |
          v
Role Activation Expires
```

### Example

**Task:** Perform an approved high-privilege administrative operation.

**Access Model:** Eligible assignment activated for a limited period.

### Licensing Considerations

Microsoft Entra PIM generally requires qualifying licensing, such as Microsoft Entra ID P2 or supported Microsoft Entra governance licensing.

The exact requirements depend on the feature and current Microsoft licensing terms.

### Important

A Microsoft 365 Business Premium subscription does not, by itself, establish entitlement to all Microsoft Entra PIM features.

**Lab Status:** PIM is a potential future capability unless a qualifying license is obtained and the feature is configured.

---

# 16. Privileged Access — Microsoft 365

Microsoft 365 contains service-specific administrative permissions.

### Administrative Areas

- Exchange administration
- SharePoint administration
- User management
- Licensing administration
- Security administration
- Compliance administration
- Teams administration where applicable

### Example

**Requirement:** Manage selected Exchange Online settings.

**Potential Approach:** Evaluate an appropriate Exchange administrative role instead of automatically assigning Global Administrator.

### Procedure

1. Identify the Microsoft 365 service.
2. Determine the required administrative operation.
3. Review the applicable service role.
4. Confirm licensing and service availability.
5. Obtain authorization.
6. Assign the appropriate role.
7. Verify administrative access.
8. Document the result.

### Important

Microsoft 365 service administration and Microsoft Entra directory administration may involve different permission models.

A role should be selected based on the actual task rather than assumed capabilities.

---

# 17. Privileged Access — Microsoft Intune

Microsoft Intune provides role-based access control for endpoint management.

### Relevant Components

- Built-in roles
- Custom roles
- Scope groups
- Scope tags
- Role assignments

### Example

**Requirement:** Allow a technician to manage a designated set of workstations.

### Proposed Approach

Use an appropriate Intune role with restricted administrative scope.

### Workflow

1. Identify required endpoint tasks.
2. Review available Intune roles.
3. Select the least-privileged role.
4. Define appropriate scope groups.
5. Apply scope tags where relevant.
6. Obtain authorization.
7. Assign the role.
8. Verify effective permissions.
9. Test authorized operations.
10. Document the configuration.

### Security Considerations

- Avoid unrestricted device administration when unnecessary.
- Review assignments regularly.
- Protect administrative identities.
- Monitor relevant management activity.
- Distinguish Intune RBAC from Microsoft Entra directory roles.

---

# 18. Privileged Access — Microsoft Azure

Microsoft Azure uses Azure Role-Based Access Control to manage permissions for Azure resources.

### RBAC Components

1. Security principal
2. Role definition
3. Scope
4. Role assignment

### Scope Hierarchy

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
Individual Resource
```

### Common Roles

| Role | General Capability |
|---|---|
| Owner | Broad resource management and role assignment authority |
| Contributor | Resource management without general role assignment authority |
| Reader | View resources |
| Virtual Machine Contributor | Selected VM management capabilities |

## 18.1 Azure Privileged Assignment Procedure

1. Identify the target resource.
2. Determine the administrative task.
3. Review available role definitions.
4. Select the minimum required permissions.
5. Select the narrowest practical scope.
6. Obtain authorization.
7. Apply the assignment.
8. Verify effective access.
9. Document the result.
10. Remove access when no longer required.

### Example

**Requirement:** Manage a designated Azure lab virtual machine.

**Potential Approach:** Assign a suitable VM management role at an appropriately restricted scope.

### Important

Azure RBAC is distinct from Microsoft Entra directory role assignments.

Microsoft Entra PIM for Azure resource roles may provide eligible assignment capabilities where appropriately licensed and configured.

---

# 19. Privileged Access — Local Administrator Accounts

Local administrator permissions allow elevated operations on an individual Windows device.

### Security Risks

- Credential reuse
- Unauthorized software installation
- Security control modification
- Local privilege abuse
- Lateral movement opportunities

### Recommended Controls

- Minimize local administrator membership.
- Avoid shared local administrator passwords.
- Use unique credentials.
- Review local administrator assignments.
- Protect credentials.
- Use supported password management capabilities.

## Windows LAPS

Windows Local Administrator Password Solution (Windows LAPS) supports management of local administrator passwords on supported Windows devices.

Depending on configuration and environment, passwords may be backed up to supported Active Directory or Microsoft Entra destinations.

### Potential Benefits

- Unique managed local administrator passwords
- Automatic password rotation
- Reduced password reuse
- Controlled password retrieval

### Important

Windows LAPS requires appropriate configuration, permissions, and supported systems.

It must not be assumed to be active merely because Windows supports the feature.

**Lab Status:** Document deployment and verification only if Windows LAPS is actually configured and tested.

---

# 20. Privileged Service Accounts and Workload Identities

Service accounts and workload identities may possess significant permissions.

### Examples

- Windows service identities
- Scheduled task accounts
- Application service principals
- Azure managed identities
- Automation accounts

### Security Principles

1. Assign minimum necessary permissions.
2. Avoid unnecessary interactive logon.
3. Document ownership.
4. Protect credentials.
5. Review assigned roles.
6. Limit resource scope.
7. Monitor relevant activity.
8. Remove unused identities.

### Active Directory Options

- Traditional service accounts
- Managed Service Accounts (MSAs)
- Group Managed Service Accounts (gMSAs)

### Azure Options

- System-assigned managed identities
- User-assigned managed identities
- Service principals

### Important

Managed identities and managed service accounts can reduce some credential management burdens, but they do not automatically enforce least privilege.

Assigned permissions must still be reviewed.

---

# 21. Emergency Privileged Access

Emergency access supports recovery when normal administrative access is unavailable.

### Example Scenarios

- Cloud administrative lockout
- Identity provider configuration failure
- Critical authentication outage
- Loss of normal administrative access

### Emergency Access Requirements

- Defined emergency purpose
- Strong protection of credentials
- Limited authorized use
- Appropriate authentication strategy
- Monitoring and alerting where available
- Secure recovery documentation
- Periodic readiness testing
- Post-use review

### Emergency Access Procedure

1. Confirm the emergency condition.
2. Identify the appropriate emergency access method.
3. Follow the established emergency authorization policy.
4. Access only the systems necessary for recovery.
5. Document administrative actions.
6. Restore normal service or access.
7. Review emergency activity.
8. Secure or rotate credentials where required.
9. Document lessons learned.

### Important

Emergency accounts may require authentication configurations that differ from ordinary administrative accounts to avoid common points of failure.

Such exceptions must be carefully designed and secured.

Do not disable MFA or weaken authentication casually to create an emergency account.

---

# 22. Privileged Access Monitoring

Monitoring privileged activity supports the detection and investigation of security-relevant events.

### Monitoring Sources

| Platform | Potential Evidence |
|---|---|
| Windows Server | Security Event Log |
| Active Directory | Account and group management events |
| Microsoft Entra ID | Audit and sign-in logs |
| Microsoft 365 | Supported audit records |
| Microsoft Azure | Azure Activity Log |
| Microsoft Intune | Administrative audit information |
| Network Devices | Administrative authentication and configuration logs |

## 22.1 Windows Event IDs

| Event ID | Description |
|---|---|
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4672 | Special privileges assigned to a new logon |
| 4728 | Member added to a security-enabled global group |
| 4729 | Member removed from a security-enabled global group |
| 4732 | Member added to a security-enabled local group |
| 4733 | Member removed from a security-enabled local group |
| 4756 | Member added to a security-enabled universal group |
| 4757 | Member removed from a security-enabled universal group |

Availability depends on event generation and applicable audit policy.

### Example — Privileged Logon Events

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4672
    StartTime = (Get-Date).AddHours(-24)
} -MaxEvents 50
```

### Example — Group Membership Changes

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4728, 4729, 4732, 4733, 4756, 4757
    StartTime = (Get-Date).AddDays(-7)
} -MaxEvents 50
```

### Important

Event 4672 does not, by itself, prove malicious or unauthorized administrative activity.

Events require contextual analysis.

---

# 23. Privileged Access Review

Privileged access should be reviewed more frequently than routine user access when justified by risk.

### Proposed Review Schedule

| Privilege Category | Suggested Review |
|---|---|
| Domain-wide administrative roles | Monthly |
| Tenant-wide administrative roles | Monthly |
| High-risk Azure roles | Monthly |
| Server administrative roles | Quarterly |
| Scoped administrative roles | Quarterly |
| Service account privileges | Quarterly |
| Temporary access | At expiration |
| Emergency access | After use and during periodic readiness reviews |

These intervals are proposed lab standards.

## Review Procedure

1. Identify privileged identities.
2. Collect current role assignments.
3. Identify account owners.
4. Review business justification.
5. Review resource scope.
6. Identify unused or excessive privileges.
7. Confirm continued authorization.
8. Document review decisions.
9. Remove inappropriate assignments.
10. Verify the final access state.

### Review Decisions

- Retain
- Reduce
- Modify
- Revoke
- Investigate
- Temporarily extend with justification

---

# 24. Privileged Access Revocation

Privileged access must be removed when it is no longer authorized.

### Revocation Triggers

- Completion of temporary work
- Role change
- Employment termination
- Expired authorization
- Security investigation
- Administrative restructuring
- Decommissioned resource

### Revocation Procedure

1. Identify the administrative identity.
2. Review direct role assignments.
3. Review privileged group memberships.
4. Identify inherited permissions.
5. Remove unauthorized assignments.
6. Revoke relevant sessions where supported and necessary.
7. Verify effective access.
8. Review service dependencies.
9. Document completion.

### Active Directory Example

Review membership:

```powershell
Get-ADGroupMember -Identity "Domain Admins"
```

An approved membership removal can be performed using:

```powershell
Remove-ADGroupMember `
    -Identity "Domain Admins" `
    -Members "adm-example"
```

**Warning:** This is an illustrative high-impact command. Do not execute it against an actual account without confirming identity, authorization, dependencies, and recovery access.

### Important

Removing a group membership may not immediately invalidate existing authentication tokens or sessions.

Session behavior must be considered during urgent revocation.

---

# 25. Privileged Access Incident Response

Potential privileged access security incidents include:

- Unauthorized role assignments
- Compromised administrator credentials
- Suspicious administrative sign-ins
- Unexpected Domain Admin membership
- Unauthorized security policy changes
- Privileged service account misuse
- Emergency account misuse

### Response Workflow

```text
Suspicious Privileged Activity
             |
             v
Event Detection
             |
             v
Security Triage
             |
             v
Determine Potential Impact
             |
             v
Escalate as Appropriate
             |
             v
Containment and Investigation
             |
             v
Recovery and Validation
             |
             v
Documentation and Review
```

### Initial Investigation Considerations

- Which identity was involved?
- What permissions did it possess?
- Which systems were accessed?
- When did the activity occur?
- Was the activity authorized?
- Were configuration changes made?
- Is the activity ongoing?
- What evidence must be preserved?

### Important

Do not delete relevant logs or remove evidence before determining appropriate preservation requirements.

Containment actions should follow authorized security response procedures.

---

# 26. Example Lab — Delegated Help Desk Administration

## Scenario

A Help Desk technician requires permission to reset passwords for selected users in an Active Directory OU.

### Objective

Demonstrate least-privilege administrative delegation without assigning Domain Admin membership.

### Lab Environment

**Domain:** `homelab.local`

**Domain Controllers:**

- DC01 — `10.20.10.10`
- DC02 — `10.20.10.11`

### Proposed Procedure

1. Identify the target OU.
2. Identify the technician's administrative identity.
3. Identify the appropriate support security group.
4. Confirm the permitted task.
5. Document simulated authorization.
6. Delegate the required permission.
7. Sign in using the delegated account.
8. Test an authorized password reset.
9. Test an unrelated administrative action.
10. Document actual results.

### Verification Matrix

| Test | Expected Result |
|---|---|
| Reset authorized user's password | Allowed |
| Reset unrelated user's password | Denied unless separately authorized |
| Modify domain-wide security settings | Denied |
| Create unauthorized administrative accounts | Denied |
| Perform permitted delegated operations | Allowed |

### Evidence

- OU configuration
- Delegated permissions
- Group membership
- Successful authorized operation
- Restricted operation result
- Relevant timestamps

### Lab Status

This is a reusable lab scenario.

Actual results must be recorded after execution.

---

# 27. Example Lab — Privileged Group Audit

## Scenario

A Systems Administrator performs a review of high-privilege Active Directory group membership.

### Objective

Identify privileged assignments and evaluate whether they remain necessary.

### Step 1 — Review Domain Admins

```powershell
Get-ADGroupMember -Identity "Domain Admins" |
Select-Object Name, SamAccountName, ObjectClass
```

### Step 2 — Review Enterprise Admins

```powershell
Get-ADGroupMember -Identity "Enterprise Admins" |
Select-Object Name, SamAccountName, ObjectClass
```

### Step 3 — Review Protected Users

```powershell
Get-ADGroupMember -Identity "Protected Users" |
Select-Object Name, SamAccountName, ObjectClass
```

### Step 4 — Document Findings

Record:

- Group name
- Member identity
- Administrative purpose
- Business justification
- Review decision
- Required corrective action

### Example Review Record

```text
Review ID:
PAM-REVIEW-001

Environment:
homelab.local

Group:
Domain Admins

Member:
To Be Verified

Business Justification:
Pending Review

Review Status:
Not Started

Decision:
Pending
```

### Expected Outcome

Privileged membership is documented and evaluated against least-privilege requirements.

### Lab Status

No audit results are claimed until the commands are executed and the findings recorded.

---

# 28. Example Lab — Azure Privileged Access

## Scenario

An administrator requires temporary access to manage an Azure lab virtual machine.

### Objective

Demonstrate scoped administrative permissions without unnecessarily granting subscription-wide control.

### Proposed Procedure

1. Identify the Azure virtual machine.
2. Review the required management tasks.
3. Identify the appropriate Azure RBAC role.
4. Determine the narrowest practical scope.
5. Document authorization.
6. Apply the role assignment.
7. Verify access.
8. Perform the authorized task.
9. Remove temporary access.
10. Verify revocation.

### Verification

| Test | Expected Result |
|---|---|
| View assigned VM | Allowed |
| Perform approved VM management task | Allowed |
| Manage unrelated resources | Restricted according to role and scope |
| Assign unrelated privileged roles | Denied unless separately authorized |
| Access after revocation takes effect | Denied |

### Important

Azure RBAC changes can take time to propagate.

Verification should account for propagation and cached authorization.

### Lab Status

This is a proposed Azure lab, not evidence of a deployed Azure VM or completed role assignment.

---

# 29. Privileged Access Record Template

```text
PRIVILEGED ACCESS RECORD

PAM Record ID:
Related Service Request:

Requesting Identity:
Administrative Identity:
Department / Role:

Target Environment:
Target Resource:
Related CI:
Related Service:

Requested Administrative Task:
Requested Role:
Requested Scope:
Business Justification:

Existing Privileges:
Least-Privilege Assessment:
Risk Classification:

Authorization Status:
Approving Role:
Authorization Reference:

Assignment Type:
Temporary / Standing / Emergency

Start Date/Time:
Expiration Date/Time:

Implementation Method:
Implementing Role:
Implementation Date/Time:

Authentication Controls:
Monitoring Requirements:

Verification Method:
Expected Result:
Actual Result:
Verification Status:

Review Date:
Review Decision:

Revocation Date/Time:
Revocation Verification:

Related Incident:
Related Change:

Current Status:
Outstanding Actions:
Notes:
```

---

# 30. Privileged Access Records and Repository Structure

### Proposed Structure

```text
Information-Security-Management/
├── README.md
├── Procedures/
│   ├── Access-Control.md
│   └── Privileged-Access.md
└── Records/
    └── PAM-001-Delegated-Administration/
        ├── README.md
        └── Evidence/
            ├── 01-Access-Request.md
            ├── 02-Authorization.md
            ├── 03-Role-Assignment.md
            ├── 04-Verification.md
            └── 05-Access-Review.md
```

This structure is illustrative.

Create records only when corresponding activities are documented.

### Documentation Requirements

Privileged access records should distinguish:

**Requested Privilege:** Permission requested.

**Authorized Privilege:** Permission approved.

**Assigned Privilege:** Permission technically configured.

**Verified Privilege:** Permission confirmed through inspection or testing.

**Revoked Privilege:** Permission removed and verified.

---

# 31. Evidence Standards

Evidence should demonstrate actual privileged access activity.

### Acceptable Evidence

- Active Directory group membership output
- Delegation configuration screenshots
- Windows administrative role information
- Microsoft Entra role assignments
- Azure RBAC assignments
- Intune role assignments
- Relevant audit events
- Access verification tests
- Revocation verification

### Evidence Requirements

Each item should identify:

1. Target environment
2. Administrative identity
3. Relevant resource
4. Collection date and time
5. Administrative tool
6. Action performed
7. Actual result
8. Related PAM record

### Sensitive Information

Do not publish:

- Passwords
- Private keys
- Access tokens
- Recovery codes
- Authentication secrets
- Unredacted privileged credentials
- Sensitive production configuration details

### Evidence Integrity

Do not fabricate:

- Role assignments
- Approvals
- Audit events
- Access review results
- Privilege revocations
- Successful security tests

---

# 32. Common Privileged Access Management Errors

### Error 1 — Excessive Administrative Permissions

**Incorrect:** Assigning Domain Admins for routine password resets.

**Correct:** Use appropriate delegated permissions.

### Error 2 — Shared Administrative Accounts

**Incorrect:** Multiple technicians routinely use one administrator account without individual accountability.

**Correct:** Use attributable administrative identities where practical.

### Error 3 — Standing Privilege Without Review

**Incorrect:** Retaining high-risk permissions indefinitely without evaluating business need.

**Correct:** Review privileges and remove unnecessary assignments.

### Error 4 — Confusing Entra Roles and Azure RBAC

**Incorrect:** Assuming Global Administrator automatically provides all Azure resource permissions.

**Correct:** Evaluate Microsoft Entra directory roles and Azure resource roles separately.

### Error 5 — Unrestricted Scope

**Incorrect:** Granting subscription-wide administrative access when a resource-scoped role is sufficient.

**Correct:** Use the narrowest practical scope.

### Error 6 — Unverified Administrative Access

**Incorrect:** Assuming an assigned role provides the expected capabilities.

**Correct:** Verify role assignments and effective permissions.

### Error 7 — Ignoring Service Accounts

**Incorrect:** Reviewing only human administrators.

**Correct:** Include privileged workload identities.

### Error 8 — No Emergency Access Plan

**Incorrect:** Depending entirely on one ordinary administrative identity.

**Correct:** Establish appropriately secured recovery access.

### Error 9 — Publishing Credentials

**Incorrect:** Storing privileged passwords in GitHub.

**Correct:** Exclude secrets and use appropriate secure storage.

### Error 10 — Claiming PIM Is Deployed

**Incorrect:** Documenting PIM as active without licensing and configuration evidence.

**Correct:** Distinguish planned capabilities from implemented controls.

---

# 33. Privileged Access Quality Checklist

## Request and Authorization

- [ ] Administrative task identified
- [ ] Requesting identity verified
- [ ] Target resource identified
- [ ] Business justification documented
- [ ] Existing privileges reviewed
- [ ] Least privilege evaluated
- [ ] Risk assessment completed
- [ ] Authorization documented

## Provisioning

- [ ] Correct administrative identity selected
- [ ] Appropriate role selected
- [ ] Resource scope restricted
- [ ] Duration defined
- [ ] Authentication protections reviewed
- [ ] Privilege assignment completed
- [ ] Assignment verified

## Monitoring and Security

- [ ] Relevant audit capabilities identified
- [ ] Privileged activity monitoring considered
- [ ] Administrative account separation reviewed
- [ ] Service account risks evaluated where relevant
- [ ] Secrets excluded from documentation
- [ ] Emergency access requirements considered

## Review and Revocation

- [ ] Access review date established
- [ ] Temporary access expiration documented
- [ ] Unnecessary privileges identified
- [ ] Revocation completed where required
- [ ] Effective access verified after removal
- [ ] Related records updated

## Documentation

- [ ] PAM record completed
- [ ] Actual results recorded
- [ ] Evidence preserved
- [ ] Related service identified
- [ ] Related CI identified where applicable
- [ ] Simulated approvals clearly labeled
- [ ] Outstanding actions documented

---

# 34. Privileged Access Performance Metrics

| Metric | Purpose |
|---|---|
| Privileged Account Inventory Coverage | Measures identification of privileged identities |
| Privileged Access Review Completion | Tracks scheduled review completion |
| Excessive Privilege Findings | Identifies permissions beyond approved requirements |
| Standing Privilege Reduction | Measures reduction in unnecessary persistent access |
| Temporary Privilege Revocation Compliance | Tracks timely privilege removal |
| Privileged MFA Coverage | Measures applicable administrative identities protected by MFA |
| Privileged Assignment Verification Rate | Measures completed assignment verification |
| Privileged Revocation Verification Rate | Measures verified permission removal |
| Emergency Access Review Completion | Tracks post-use review completion |
| Privileged Access Documentation Completeness | Evaluates record quality |

### Example Calculations

**Privileged Access Review Completion Rate**

```text
Review Completion (%) =
Completed Privileged Access Reviews
----------------------------------- x 100
Scheduled Privileged Access Reviews
```

**Privileged Assignment Verification Rate**

```text
Verification Rate (%) =
Verified Privileged Assignments
------------------------------- x 100
Total Privileged Assignments Reviewed
```

**Temporary Privilege Revocation Compliance**

```text
Revocation Compliance (%) =
Temporary Privileges Revoked On Time
------------------------------------ x 100
Temporary Privileges Due for Revocation
```

### Measurement Requirements

- Define the reporting period.
- Use actual assignment records.
- Use verified timestamps.
- Identify incomplete records.
- Distinguish simulated measurements.
- Do not invent compliance percentages.

---

# 35. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Receives and routes privileged access requests |
| Incident Management | Responds to privileged access failures or suspected misuse |
| Service Request Management | Coordinates approved routine administrative access requests |
| Knowledge Management | Maintains privileged access procedures and technical guidance |
| Problem Management | Investigates recurring administrative access issues |
| Change Enablement | Controls applicable high-risk permission and security configuration changes |
| Monitoring and Event Management | Detects and triages privileged activity events |
| Service Configuration Management | Identifies systems and services requiring administrative protection |
| Information Security Management | Defines privileged access controls and manages related risks |
| Continual Improvement | Evaluates and improves privileged access governance |

---

# 36. Procedure Review

Review this procedure when:

- Administrative role requirements change.
- New cloud services are introduced.
- Privileged access licensing changes.
- Authentication requirements change.
- New administrative tools are deployed.
- Security incidents identify control weaknesses.
- Privileged access reviews identify excessive permissions.
- Employee lifecycle processes change.
- Emergency access procedures change.
- Continual improvement identifies process weaknesses.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Privileged Access Management procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Administrative roles, access requests, business approvals, privileged access policies, emergency procedures, and operational scenarios may be simulated.

Technical configurations, administrative assignments, PowerShell commands, security findings, and verification results are documented as hands-on lab activities only when supporting evidence exists.

Proposed capabilities such as Microsoft Entra Privileged Identity Management, PowerShell JEA, Windows LAPS, automated privileged access workflows, and centralized monitoring must not be represented as deployed without actual configuration and verification.

Simulated approvals do not constitute independent organizational authorization.

Expected results and illustrative security findings must not be represented as actual observations.

GitHub publication does not imply production PAM operations, regulatory compliance, independent security approval, or professional employment experience.

This procedure demonstrates ITIL-aligned Information Security Management, privileged identity protection, least-privilege administration, role-based access control, administrative delegation, privileged access monitoring, access reviews, and secure privilege lifecycle management.
