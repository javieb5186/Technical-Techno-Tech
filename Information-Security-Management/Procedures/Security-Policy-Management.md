# SOP — Security Policy Management

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Information Security Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-ISM-003  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**Function:** Internal IT  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

## 1. Purpose

This Standard Operating Procedure establishes a consistent process for developing, reviewing, authorizing, implementing, monitoring, and maintaining information security policies within Technical Techno Tech.

Security Policy Management ensures that security requirements are clearly defined, communicated, technically enforced where appropriate, and periodically evaluated.

The procedure supports:

- Information security governance
- Consistent security requirements
- Protection of organizational information
- Risk-based security decisions
- Standardized technical configurations
- Access control and authentication security
- Endpoint and server protection
- Network security
- Cloud security
- Security policy compliance
- Exception management
- Auditability and accountability
- Continual improvement

**Key Principle:** Security policies define organizational requirements. Technical security controls implement those requirements, while monitoring and reviews determine whether the controls remain appropriate and effective.

---

## 2. Scope

This procedure applies to security policies governing Technical Techno Tech's internal IT services, infrastructure, identities, endpoints, applications, and information assets.

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

### Security Policy Categories

This procedure covers policies related to:

1. Identity and access management
2. Authentication and passwords
3. Privileged access
4. Endpoint security
5. Server security
6. Network security
7. Cloud security
8. Data protection
9. Logging and monitoring
10. Security incident reporting
11. System configuration
12. Vulnerability and patch management
13. Acceptable use
14. Backup and recovery security
15. Remote access
16. Security exceptions

### Scope Limitations

This procedure establishes a proposed security policy management framework for a simulated organization.

It does not claim certification or compliance with ISO 27001, NIST, CIS, HIPAA, PCI DSS, or another external framework.

Specific regulatory or contractual requirements must be identified and validated separately before being treated as applicable.

---

## 3. ITIL 4 Alignment

Security Policy Management supports the ITIL 4 Information Security Management practice.

### Practice Purpose

The purpose of Information Security Management is to protect the information needed by the organization to conduct its business.

This includes managing risks affecting:

- Confidentiality
- Integrity
- Availability

### Confidentiality

Information is protected from unauthorized access or disclosure.

**Example:** Restricting sensitive HR information to authorized personnel.

### Integrity

Information and systems are protected against unauthorized or inappropriate modification.

**Example:** Restricting changes to domain-wide Group Policy settings.

### Availability

Information and services remain accessible to authorized users when required.

**Example:** Maintaining reliable authentication and recovery capabilities.

### Security Policy Management Within ITIL

Security policies provide requirements that may influence multiple ITIL practices.

For example:

- Service Request Management follows access authorization requirements.
- Change Enablement evaluates security risks associated with changes.
- Incident Management responds to security-related service disruptions.
- Monitoring and Event Management detects security-relevant events.
- Service Configuration Management maintains information about protected assets.
- Continual Improvement identifies opportunities to strengthen controls.

**Important:** ITIL 4 does not require one specific security policy structure, document numbering convention, or technical enforcement platform.

The workflow defined here is a proposed internal procedure.

---

## 4. Key Terminology

| Term | Definition |
|---|---|
| Security Policy | An approved statement of security requirements and expectations |
| Security Standard | A specific, measurable requirement supporting a policy |
| Security Procedure | Documented instructions for performing security-related activities |
| Security Guideline | Recommended practices that may allow flexibility |
| Security Control | A safeguard intended to reduce or manage security risk |
| Technical Control | A safeguard implemented through technology |
| Administrative Control | A safeguard implemented through policies, processes, or responsibilities |
| Physical Control | A safeguard protecting physical facilities or equipment |
| Risk | The effect of uncertainty on objectives, often evaluated through likelihood and impact |
| Threat | A potential cause of an unwanted security event |
| Vulnerability | A weakness that could be exploited or contribute to harm |
| Compliance | Conformance with an applicable requirement |
| Exception | A documented authorization to deviate from a defined requirement |
| Baseline | An established reference configuration or expected security state |
| Configuration Drift | Deviation from an approved configuration baseline |
| Policy Owner | Role accountable for maintaining a policy |
| Control Owner | Role responsible for implementing or operating a security control |
| Compensating Control | An alternative safeguard used to reduce risk when the primary requirement cannot be met |
| Evidence | Information supporting a conclusion about configuration, operation, or compliance |

---

## 5. Security Documentation Hierarchy

Technical Techno Tech uses the following proposed documentation model.

```text
Information Security Governance
              |
              v
       Security Policies
              |
              v
       Security Standards
              |
              v
     Security Procedures
              |
              v
      Technical Controls
              |
              v
     Monitoring and Evidence
```

### 5.1 Security Policy

Defines what the organization requires.

**Example:**

"Administrative access must be restricted to authorized personnel."

### 5.2 Security Standard

Defines a measurable requirement.

**Example:**

"Privileged accounts must use approved authentication protections."

### 5.3 Security Procedure

Explains how the requirement is implemented or maintained.

**Example:**

The Privileged Access Management SOP.

### 5.4 Technical Control

Implements the security requirement.

**Example:**

An appropriately scoped Microsoft Entra administrative role assignment.

### 5.5 Monitoring and Evidence

Demonstrates whether the requirement is operating as intended.

**Example:**

A verified role assignment, access review record, or audit log.

### Important Distinction

A written security policy does not automatically enforce security.

Technical controls must be configured, tested, monitored, and maintained separately.

---

## 6. Security Policy Management Principles

### 6.1 Risk-Based Security

Security requirements should address identified risks rather than being selected arbitrarily.

### 6.2 Clear Ownership

Each policy should have an accountable owner.

### 6.3 Defined Scope

Policies should identify the systems, identities, services, or information they govern.

### 6.4 Measurable Requirements

Where practical, requirements should be specific enough to evaluate.

### 6.5 Least Privilege

Security policies should support minimum necessary access.

### 6.6 Defense in Depth

Multiple complementary safeguards should protect important systems and information.

### 6.7 Secure Configuration

Systems should use approved security baselines where appropriate.

### 6.8 Controlled Changes

Significant policy and technical configuration changes should follow applicable authorization processes.

### 6.9 Evidence-Based Verification

Compliance conclusions should be supported by actual evidence.

### 6.10 Periodic Review

Policies should be reviewed when risks, technology, or organizational requirements change.

### 6.11 Exception Accountability

Exceptions should be documented, risk-assessed, authorized, and reviewed.

### 6.12 Continual Improvement

Security findings should inform policy and control improvements.

---

## 7. Roles and Responsibilities

### Information Security Personnel

Responsible for:

- Developing security policy requirements
- Evaluating security risks
- Reviewing proposed policy changes
- Coordinating policy reviews
- Assessing exceptions
- Identifying security control weaknesses
- Recommending improvements

### Systems Administrator

Responsible for:

- Implementing authorized Windows Server security settings
- Managing Active Directory security configurations
- Applying approved Group Policy settings
- Verifying technical configurations
- Documenting configuration changes

### Cloud Administrator

Responsible for:

- Implementing authorized Microsoft Entra and Microsoft 365 security controls
- Reviewing applicable cloud security settings
- Supporting Azure security configuration
- Documenting technical implementation and verification

### Endpoint Administrator

Responsible for:

- Implementing authorized endpoint security configurations
- Managing applicable Intune security policies
- Reviewing device compliance settings
- Verifying endpoint security controls

### Network Administrator

Responsible for:

- Implementing authorized network security configurations
- Managing applicable firewall rules
- Reviewing administrative network access
- Maintaining network security documentation

### Service Desk Technician

Responsible for:

- Following applicable security procedures
- Reporting suspected security incidents
- Performing authorized routine security-related tasks
- Escalating requests outside assigned permissions
- Documenting relevant support activity

### Policy Owner

Responsible for:

- Maintaining assigned policy content
- Confirming business relevance
- Coordinating review and approval
- Ensuring obsolete policy versions are identified

### Designated Policy Authority

Responsible for:

- Approving policies within assigned authority
- Evaluating significant security requirements
- Reviewing major policy exceptions
- Resolving conflicts between business needs and security requirements

**Lab Note:** These roles are simulated. Technical execution and independent policy approval must be distinguished in portfolio records.

---

# 8. Security Policy Lifecycle

```text
Security Requirement Identified
             |
             v
Risk and Scope Assessment
             |
             v
Policy Drafting
             |
             v
Stakeholder Review
             |
             v
Authorization
             |
             v
Publication and Communication
             |
             v
Technical Implementation
             |
             v
Verification and Monitoring
             |
             v
Periodic Review
             |
       +-----+-----+
       |           |
       v           v
    Retain       Revise / Retire
```

A policy may require multiple technical controls, and some requirements may be implemented through administrative or physical safeguards rather than software configuration.

---

# 9. Security Policy Management Procedure

## Step 1 — Identify the Security Requirement

Determine why a security policy is needed.

### Potential Triggers

- Identified security risk
- New technology deployment
- Security incident
- Audit finding
- Vulnerability assessment
- Organizational change
- New service requirement
- Configuration weakness
- Applicable legal or contractual requirement
- Continual improvement initiative

### Example

**Finding:** Administrative accounts have inconsistent authentication protections.

**Potential Requirement:** Establish a consistent privileged account authentication policy.

### Required Information

- Identified issue
- Affected service
- Relevant systems
- Security risk
- Proposed objective
- Requesting role

**Expected Result:** The security requirement is documented.

---

## Step 2 — Identify Affected Services and Assets

Determine which services and configuration items are affected.

### Examples

- Active Directory domain controllers
- Windows workstations
- Microsoft Entra identities
- Microsoft 365 applications
- Azure virtual machines
- Network firewalls
- File servers

### Example Assessment

| Asset | Security Requirement |
|---|---|
| DC01 | Domain authentication security |
| DC02 | Domain authentication security |
| MGMT01 | Administrative workstation security |
| CLIENT01 | Endpoint security |
| Microsoft Entra tenant | Cloud identity security |

These are potential policy relationships, not proof that particular controls have been deployed.

**Expected Result:** The affected environment is identified.

---

## Step 3 — Evaluate Security Risk

Assess the risk that the proposed policy is intended to manage.

### Risk Assessment Factors

1. Threat scenario
2. Vulnerability or weakness
3. Potential business impact
4. Likelihood
5. Existing controls
6. Control effectiveness
7. Residual risk

### Proposed Risk Matrix

| Impact \ Likelihood | Low | Medium | High |
|---|---|---|---|
| High | Medium | High | Critical |
| Medium | Low | Medium | High |
| Low | Low | Low | Medium |

This matrix is an illustrative internal model.

### Example

**Risk:** Unauthorized administrative access.

**Potential Impact:** Modification of directory objects or security configurations.

**Possible Controls:**

- Least privilege
- Strong authentication
- Dedicated administrative identities
- Administrative activity monitoring

**Expected Result:** The policy has a documented risk-based justification.

---

## Step 4 — Define the Policy Objective

Establish what the policy should accomplish.

### Example Objectives

- Reduce unauthorized access
- Protect privileged accounts
- Standardize endpoint security
- Improve audit visibility
- Reduce configuration drift
- Protect sensitive data
- Improve incident detection

### Example Objective

"Ensure administrative permissions are assigned only to authorized identities and reviewed periodically."

### Important

An objective should describe the intended security outcome rather than a specific product configuration alone.

**Expected Result:** The policy objective is clearly defined.

---

## Step 5 — Define the Policy Scope

Identify who and what the policy applies to.

### Scope Elements

- Users
- Administrators
- Service accounts
- Devices
- Servers
- Applications
- Network infrastructure
- Cloud resources
- Information categories

### Example

**Policy:** Privileged Account Security

**Scope:** Administrative identities managing Active Directory, Microsoft Entra ID, Microsoft 365, and Azure resources.

### Exclusions

Document exclusions where applicable.

Exclusions must not be assumed to constitute approved exceptions.

**Expected Result:** The policy scope is documented.

---

## Step 6 — Identify Applicable Requirements

Review relevant requirements.

### Potential Sources

- Internal security objectives
- Business requirements
- Service requirements
- Contractual obligations
- Applicable laws and regulations
- Microsoft security documentation
- CIS Benchmarks
- NIST guidance
- Vendor security recommendations

### Important

External frameworks may provide useful reference material, but their recommendations are not automatically mandatory for Technical Techno Tech.

Determine applicability before adopting a requirement.

**Expected Result:** Relevant requirements and reference sources are identified.

---

## Step 7 — Draft the Security Policy

Prepare the policy document.

### Recommended Sections

1. Policy ID
2. Title
3. Version
4. Status
5. Owner
6. Purpose
7. Scope
8. Security requirements
9. Responsibilities
10. Exceptions
11. Monitoring
12. Review schedule
13. Related procedures
14. Revision history

### Writing Requirements

Use clear language.

Avoid ambiguous statements such as:

"Administrators should use strong security."

Prefer measurable requirements such as:

"Privileged accounts must use authentication protections approved for their assigned risk level."

### Important

A policy should establish requirements.

Detailed implementation commands generally belong in procedures or technical standards.

**Expected Result:** A reviewable policy draft is created.

---

## Step 8 — Define Supporting Security Standards

Identify measurable requirements needed to support the policy.

### Example

**Policy Requirement:** Protect administrative identities.

**Supporting Standards:**

- Administrative privileges must be authorized.
- Administrative role assignments must be reviewed.
- Temporary privileges must have defined expiration conditions.
- Administrative authentication must satisfy approved security requirements.
- Unnecessary privileges must be revoked.

### Security Standard Considerations

- Technical feasibility
- System compatibility
- Available licensing
- Administrative overhead
- Operational dependencies
- Security effectiveness

**Expected Result:** Supporting standards are identified.

---

## Step 9 — Identify Technical Enforcement Methods

Determine how the policy can be implemented.

### Potential Technologies

| Environment | Enforcement Method |
|---|---|
| Active Directory | Group Policy, permissions, account controls |
| Windows Server | Local security settings, Group Policy, Windows Defender Firewall |
| Windows 11 | Local security settings, Group Policy, Intune |
| Microsoft Entra ID | Authentication policies, Conditional Access where licensed |
| Microsoft Intune | Configuration profiles, endpoint security policies, compliance policies |
| Microsoft Azure | Azure Policy, Azure RBAC, resource security settings |
| Networking | Firewall rules, ACLs, administrative access controls |
| Hyper-V | Platform permissions and supported security settings |

### Important

Different products may enforce different aspects of the same security policy.

A technical setting must not be described as active until it has been configured and verified.

**Expected Result:** Suitable enforcement methods are identified.

---

## Step 10 — Evaluate Operational Impact

Assess the consequences of implementing the proposed policy.

### Review Areas

- User access
- Administrator access
- Application compatibility
- Network connectivity
- Authentication dependencies
- Server availability
- Device management
- Recovery procedures
- Licensing requirements
- Support workload

### Example

A restrictive authentication policy could prevent a legacy application from connecting.

A firewall policy could block required management traffic.

A Group Policy change could affect multiple computers.

### Required Considerations

- Affected identities
- Affected systems
- Expected benefit
- Potential disruption
- Testing requirements
- Rollback approach

**Expected Result:** Operational risks are documented.

---

## Step 11 — Conduct Stakeholder Review

Submit the draft for appropriate review.

### Potential Reviewers

- Information Security
- Systems Administration
- Cloud Administration
- Endpoint Administration
- Network Administration
- Service Owner
- Business Resource Owner
- IT Management

### Review Questions

1. Is the requirement understandable?
2. Does it address the identified risk?
3. Is the scope appropriate?
4. Can it be implemented?
5. Are responsibilities clear?
6. Are exceptions addressed?
7. Can compliance be measured?
8. Does it conflict with another policy?

**Expected Result:** Review findings are documented.

---

## Step 12 — Obtain Policy Authorization

Submit the proposed policy to the designated authority.

### Possible Decisions

- Approved
- Approved with conditions
- Returned for revision
- Deferred
- Rejected

### Authorization Record

```text
Policy ID:
SEC-POL-001

Policy Name:
Privileged Account Security

Version:
1.0

Authorization Status:
Pending

Approving Role:
Designated Policy Authority

Decision Date:
Not Recorded

Conditions:
To Be Determined
```

This is an illustrative record.

### Important

Policy approval and technical change authorization are distinct decisions.

An approved security policy does not automatically authorize every production configuration change needed to implement it.

**Expected Result:** The policy decision is documented.

---

## Step 13 — Publish the Authorized Policy

Publish the approved version in an appropriate controlled location.

### Publication Requirements

- Approved version identified
- Effective date recorded
- Policy owner identified
- Superseded versions distinguished
- Related procedures referenced
- Intended audience identified

### Proposed Portfolio Approach

GitHub can document fictional policy examples and sanitized lab procedures.

It should not contain real credentials, private security information, or sensitive production configurations.

### Important

A GitHub commit is evidence that documentation changed.

It is not proof of organizational policy approval.

**Expected Result:** The authorized policy is available to its intended audience.

---

## Step 14 — Communicate the Policy

Inform affected personnel of relevant requirements.

### Potential Communication Methods

- Internal documentation
- Service Desk knowledge articles
- Administrative guidance
- Training materials
- Change communications
- Organizational announcements

### Communication Should Explain

- What changed
- Who is affected
- Effective date
- Required actions
- Available support
- Exception process

**Expected Result:** Affected roles understand the applicable requirements.

---

## Step 15 — Plan Technical Implementation

Translate policy requirements into specific implementation activities.

### Implementation Planning

Identify:

1. Target systems
2. Required settings
3. Responsible administrator
4. Dependencies
5. Prerequisites
6. Test environment
7. Expected results
8. Rollback method
9. Change authorization requirements
10. Evidence requirements

### Example

**Policy Requirement:** Restrict administrative access.

**Technical Implementation Options:**

- Review privileged group membership.
- Apply delegated permissions.
- Configure appropriate administrative roles.
- Restrict local administrator membership.
- Apply supported authentication controls.

**Expected Result:** An implementation plan is prepared.

---

## Step 16 — Determine Change Enablement Requirements

Evaluate whether the technical implementation requires a Change record.

### Potential Change-Controlled Activities

- Domain-wide Group Policy changes
- Significant authentication policy changes
- Major Conditional Access changes
- Firewall policy modifications
- Privileged role restructuring
- Large-scale endpoint security configuration changes

### Change Considerations

- Risk
- Scope
- Business impact
- Testing
- Authorization
- Implementation schedule
- Rollback

### Important

Not every routine security configuration action requires a separate Change record.

The appropriate change model depends on the activity and organizational requirements.

**Expected Result:** Applicable change controls are identified.

---

## Step 17 — Test the Proposed Security Controls

Test configuration changes in a controlled environment before broader deployment when practical.

### Testing Objectives

- Verify expected security behavior
- Identify compatibility problems
- Confirm authorized access
- Confirm unauthorized actions are restricted
- Assess service availability
- Evaluate rollback readiness

### Example

**Policy:** Restrict access to an HR shared folder.

**Tests:**

1. Authorized HR user can access the folder.
2. Unauthorized Sales user cannot access the folder.
3. Required administrative access remains available.
4. Normal file operations function as intended.

### Important

A successful configuration command does not necessarily prove the intended security outcome.

**Expected Result:** Technical behavior is evaluated and documented.

---

## Step 18 — Implement the Security Controls

Apply the approved configuration through appropriate administrative tools.

### Possible Tools

- Group Policy Management Console
- Active Directory Administrative Center
- PowerShell
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Microsoft 365 Admin Center
- Azure Portal
- OPNsense management interface
- VyOS CLI

### Implementation Requirements

- Confirm authorization.
- Verify the target system.
- Capture relevant baseline information.
- Apply only approved settings.
- Monitor for unexpected impact.
- Record actual changes.

**Expected Result:** Approved security controls are implemented.

---

## Step 19 — Verify Technical Enforcement

Confirm that the implemented settings are active and functioning.

### Verification Methods

- Configuration inspection
- Effective policy reporting
- Authorized functional tests
- Negative access tests
- Audit log inspection
- Device compliance review
- Role assignment review
- Network connectivity testing

### Verification Record

```text
Policy ID:
SEC-POL-001

Control:
Administrative Access Restriction

Target:
To Be Identified

Expected Configuration:
To Be Defined

Actual Configuration:
Not Yet Verified

Verification Status:
Pending

Evidence:
Not Collected
```

**Expected Result:** Technical enforcement is verified or outstanding issues are documented.

---

## Step 20 — Monitor Policy Compliance

Evaluate whether systems continue to meet applicable requirements.

### Monitoring Methods

- Configuration reviews
- Group Policy reporting
- Administrative role reviews
- Endpoint compliance reporting
- Security event monitoring
- Azure Policy compliance results where configured
- Manual security assessments

### Potential Findings

- Compliant
- Noncompliant
- Not evaluated
- Not applicable
- Approved exception

### Important

A device reporting compliant with one Intune compliance policy does not demonstrate compliance with every organizational security requirement.

**Expected Result:** Policy compliance is evaluated using defined evidence.

---

## Step 21 — Manage Noncompliance

Investigate systems or identities that do not meet the policy.

### Possible Causes

- Incorrect configuration
- Missing policy assignment
- Technical incompatibility
- Configuration drift
- Unsupported platform
- Incomplete deployment
- Unauthorized modification
- Expired exception

### Response Options

- Correct configuration
- Investigate technical failure
- Escalate security risk
- Request an exception
- Initiate a Change
- Create an Incident where appropriate
- Document a Problem for recurring underlying issues

**Expected Result:** Noncompliance is documented and assigned for appropriate action.

---

## Step 22 — Review and Update the Policy

Review policies according to their defined schedule and significant triggering events.

### Review Questions

1. Is the policy still necessary?
2. Has the underlying risk changed?
3. Are the requirements still appropriate?
4. Have technologies changed?
5. Are controls effective?
6. Are exceptions increasing?
7. Are users experiencing unnecessary disruption?
8. Are supporting procedures current?

### Review Outcomes

- Retain
- Revise
- Consolidate
- Replace
- Retire

**Expected Result:** The policy remains current and relevant.

---

# 10. Security Policy Categories

Technical Techno Tech may establish policies in the following categories.

| Policy Category | Example Requirement |
|---|---|
| Identity & Access | Access must be authorized and reviewed |
| Authentication | Accounts must use approved authentication protections |
| Privileged Access | Administrative permissions must follow least privilege |
| Endpoint Security | Managed endpoints must meet applicable security requirements |
| Server Security | Servers must use approved security configurations |
| Network Security | Network access must be restricted according to business requirements |
| Cloud Security | Cloud resources must use appropriate identity and security controls |
| Data Protection | Sensitive information must be protected according to classification |
| Logging & Monitoring | Security-relevant activity must be recorded where required |
| Vulnerability Management | Identified vulnerabilities must be assessed and addressed according to risk |
| Patch Management | Applicable security updates must be evaluated and deployed through approved processes |
| Remote Access | Remote administrative access must use approved methods |
| Backup Security | Backups must be protected against unauthorized access and modification |
| Acceptable Use | Organizational technology must be used according to defined requirements |

These are proposed policy categories rather than a list of approved organizational policies.

---

# 11. Security Policy — Active Directory Group Policy

Active Directory Group Policy can centrally manage many Windows security settings.

### Common Security Areas

- Password and account lockout policies
- Audit policies
- Windows Defender Firewall
- User rights assignments
- Security options
- Windows security settings
- Administrative restrictions
- Supported Windows Defender configurations

### Lab Environment

**Domain:** `homelab.local`

| System | IP Address |
|---|---|
| DC01 | 10.20.10.10 |
| DC02 | 10.20.10.11 |
| MGMT01 | 10.20.30.10 |
| CLIENT01 | 10.20.20.10 |

## 11.1 Review Existing Group Policy Objects

```powershell
Get-GPO -All |
Select-Object DisplayName, Id, GpoStatus
```

**Requirements:**

- GroupPolicy PowerShell module
- Appropriate directory access
- Connectivity to the domain

### Purpose

Identify existing GPOs before creating or modifying security configurations.

---

## 11.2 Review Domain Password Policy

```powershell
Get-ADDefaultDomainPasswordPolicy
```

### Relevant Settings

- Minimum password length
- Password history
- Maximum password age
- Minimum password age
- Account lockout threshold
- Lockout duration

### Important

The default domain password policy and Fine-Grained Password Policies (FGPPs) are separate mechanisms.

Fine-Grained Password Policies can apply different password and lockout requirements to supported users or global security groups.

---

## 11.3 Review Fine-Grained Password Policies

```powershell
Get-ADFineGrainedPasswordPolicy -Filter *
```

### Review a User's Resultant Policy

```powershell
Get-ADUserResultantPasswordPolicy -Identity "sconner"
```

A null result may indicate that no Fine-Grained Password Policy applies to the user.

### Security Considerations

- Verify the intended target.
- Avoid unnecessary policy conflicts.
- Review authentication compatibility.
- Document the business justification.

---

## 11.4 Review Effective Group Policy

On a target Windows computer:

```powershell
gpresult /r
```

### Generate an HTML Report

```powershell
gpresult /h C:\Temp\GPO-Report.html
```

The destination directory must exist and be writable.

### Purpose

Identify Group Policy processing results and applied GPOs.

### Important

A GPO existing in Active Directory does not prove that it applies to a particular computer or user.

GPO links, scope, security filtering, WMI filtering, inheritance, processing, and other conditions may affect application.

---

# 12. Security Policy — Password and Account Lockout

Authentication policies help reduce risks associated with unauthorized account access.

### Potential Requirements

- Minimum password length
- Password reuse restrictions
- Account lockout controls
- Secure password handling
- MFA where applicable
- Protection against compromised credentials

### Active Directory Tools

- Group Policy Management Console
- Active Directory Administrative Center
- Active Directory PowerShell module

### Domain Password Policy

For domain user accounts, the default domain password policy is typically configured through an appropriate domain-linked GPO, commonly the Default Domain Policy.

### Fine-Grained Password Policies

FGPPs are managed through Active Directory Password Settings Objects.

### Example Scenario

**Requirement:** Apply a more restrictive password policy to a designated administrative user population.

### Proposed Workflow

1. Identify the target identities.
2. Review existing password policies.
3. Determine the appropriate policy mechanism.
4. Evaluate authentication dependencies.
5. Document authorization.
6. Configure the policy.
7. Verify the resultant policy.
8. Test authentication behavior.
9. Record results.

### Important

Password policies should be selected based on current security guidance, actual system capabilities, and organizational requirements.

A shorter password expiration interval does not automatically provide better security.

---

# 13. Security Policy — Account Lockout

Account lockout settings may reduce some automated password-guessing risks but can also create denial-of-service or operational problems.

### Relevant Settings

- Account lockout threshold
- Account lockout duration
- Reset account lockout counter after

### Proposed Procedure

1. Review current settings.
2. Identify authentication risks.
3. Evaluate potential user disruption.
4. Review service account dependencies.
5. Select appropriate settings.
6. Obtain required authorization.
7. Test in a controlled environment.
8. Implement approved changes.
9. Monitor lockout activity.

### Security Considerations

- Repeated failed authentication
- Password spraying
- Incorrect saved credentials
- Service account password mismatches
- Application authentication failures

### Important

An account lockout is not automatically evidence of an attack.

Investigate relevant authentication activity before drawing conclusions.

---

# 14. Security Policy — Audit Logging

Security audit policies determine which categories of activity Windows records.

### Common Audit Categories

- Logon and logoff
- Account management
- Directory service access
- Policy changes
- Privilege use
- Object access
- System events

## Review Current Audit Policy

```powershell
auditpol /get /category:*
```

### Example — Review Logon Events

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4624, 4625
    StartTime = (Get-Date).AddHours(-24)
} -MaxEvents 50
```

### Example — Review Account Management

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4720, 4722, 4725, 4726
    StartTime = (Get-Date).AddDays(-7)
} -MaxEvents 50
```

### Important

Relevant audit policies must be enabled for many events to be generated.

Audit logs should be protected against unauthorized modification and reviewed according to applicable requirements.

---

# 15. Security Policy — Windows Defender Firewall

Windows Defender Firewall can enforce host-based network traffic restrictions.

### Policy Objectives

- Restrict unnecessary inbound traffic
- Permit required service communication
- Reduce exposed network services
- Protect administrative access
- Support network segmentation

## Review Firewall Profiles

```powershell
Get-NetFirewallProfile |
Select-Object Name, Enabled, DefaultInboundAction, DefaultOutboundAction
```

## Review Enabled Firewall Rules

```powershell
Get-NetFirewallRule -Enabled True |
Select-Object DisplayName, Direction, Action
```

### Proposed Implementation Workflow

1. Identify required traffic.
2. Review existing firewall rules.
3. Document the security requirement.
4. Assess affected services.
5. Obtain authorization.
6. Test proposed rules.
7. Implement approved configuration.
8. Verify required connectivity.
9. Confirm prohibited traffic is restricted.
10. Document results.

### Important

Firewall changes can interrupt remote administration.

Confirm a suitable recovery or rollback method before modifying rules on remote systems.

---

# 16. Security Policy — Microsoft Entra ID

Microsoft Entra ID supports cloud identity security controls.

### Potential Security Areas

- MFA
- Authentication methods
- Conditional Access
- Administrative roles
- Sign-in restrictions
- Identity protection capabilities
- Application access

### Proposed Policy Example

**Policy:** Administrative Authentication Security

**Objective:** Protect privileged cloud identities.

### Potential Requirements

- Appropriate MFA
- Restricted administrative roles
- Sign-in monitoring
- Dedicated administrative identities
- Periodic privileged access review

### Implementation Considerations

- Tenant licensing
- Supported authentication methods
- Emergency access
- Application compatibility
- Device requirements
- Policy exclusions
- Administrative access recovery

### Important

Conditional Access requires qualifying licensing.

Microsoft 365 Business Premium generally includes Microsoft Entra ID P1 capabilities, but additional identity governance and risk-based capabilities may require higher-tier licensing.

Confirm current licensing before documenting a feature as available.

---

# 17. Security Policy — Microsoft Intune

Microsoft Intune can deploy and evaluate supported endpoint security configurations.

### Potential Policy Types

- Device configuration profiles
- Endpoint security policies
- Device compliance policies
- Security baselines
- Windows Defender Firewall settings
- Microsoft Defender Antivirus settings
- Disk encryption configurations
- Account protection settings

### Proposed Workflow

1. Identify the endpoint security requirement.
2. Select the appropriate Intune policy type.
3. Review available settings.
4. Identify target devices or users.
5. Evaluate licensing.
6. Create a test assignment.
7. Deploy to authorized test devices.
8. Review deployment status.
9. Verify the actual device configuration.
10. Document results.

### Important

Intune configuration profiles and compliance policies serve different purposes.

A compliance policy evaluates defined conditions.

A configuration profile applies supported settings.

A device reporting compliant does not necessarily mean every security configuration has been deployed successfully.

---

# 18. Security Policy — Microsoft Azure

Microsoft Azure provides multiple mechanisms for managing security requirements.

### Potential Controls

- Azure RBAC
- Azure Policy
- Network security groups
- Resource configuration
- Managed identities
- Encryption settings
- Azure Monitor
- Microsoft Defender for Cloud where available

## Azure Policy

Azure Policy can evaluate Azure resources against defined rules and, depending on the policy effect and configuration, enforce or remediate certain requirements.

### Example Requirements

- Restrict deployment locations
- Require resource tags
- Audit selected security configurations
- Restrict certain resource types
- Evaluate resource configuration

### Important

Azure Policy and Azure RBAC perform different functions.

**Azure Policy:** Evaluates or governs resource configurations.

**Azure RBAC:** Controls who can perform operations on Azure resources.

### Proposed Workflow

1. Identify the Azure security requirement.
2. Review applicable built-in or custom policy definitions.
3. Determine the assignment scope.
4. Evaluate policy effects.
5. Assess resource impact.
6. Obtain authorization.
7. Test the policy.
8. Apply the assignment.
9. Review compliance results.
10. Document findings.

### Cost Considerations

Some Azure security and monitoring capabilities may introduce additional costs.

Evaluate licensing and consumption before deploying optional services.

---

# 19. Security Policy — Network Infrastructure

Network security policies govern access to network resources and management interfaces.

### Potential Requirements

- Restrict administrative access
- Control traffic between network segments
- Limit unnecessary services
- Protect network management protocols
- Use secure authentication
- Maintain approved firewall configurations
- Record relevant security events

### Supported Lab Technologies

- Cisco Packet Tracer
- OPNsense
- VyOS
- Windows networking tools

### Example

**Policy Requirement:** Restrict unauthorized access between departmental network segments.

### Potential Technical Controls

- VLAN segmentation
- Firewall rules
- Router ACLs
- Administrative access restrictions
- Network monitoring

### Important

VLANs alone do not guarantee isolation when routing between VLANs is permitted.

Effective restrictions must be implemented and verified at the appropriate enforcement points.

---

# 20. Security Policy — Secure Configuration Baselines

A security baseline defines an expected configuration for a system or device category.

### Potential Baseline Categories

- Domain controllers
- Member servers
- Windows workstations
- Administrative workstations
- Network devices
- Cloud resources

### Example Baseline Requirements

- Approved authentication settings
- Appropriate firewall configuration
- Required audit settings
- Restricted administrative access
- Supported security updates
- Appropriate endpoint protection

### Baseline Management Procedure

1. Identify the device category.
2. Review security requirements.
3. Select applicable baseline settings.
4. Evaluate compatibility.
5. Document the proposed baseline.
6. Test configuration.
7. Obtain authorization.
8. Implement approved settings.
9. Verify effective configuration.
10. Monitor for drift.

### Important

Microsoft security baselines and CIS Benchmarks can provide useful starting points.

They should be evaluated for compatibility and operational impact before implementation.

---

# 21. Security Policy — Configuration Drift

Configuration drift occurs when a system deviates from its intended baseline.

### Potential Causes

- Unauthorized changes
- Incomplete policy application
- Manual administrative modifications
- Software updates
- Device management conflicts
- Configuration errors

### Drift Detection Methods

- Group Policy reports
- Intune configuration status
- PowerShell configuration checks
- Azure Policy evaluations
- Manual configuration reviews
- Configuration management tools

### Response Procedure

1. Identify the deviation.
2. Confirm the expected baseline.
3. Determine whether the change was authorized.
4. Evaluate security impact.
5. Identify the responsible system or service owner.
6. Correct unauthorized deviations through the appropriate process.
7. Verify the final configuration.
8. Document findings.

### Important

Not every deviation is a security incident.

Some differences may result from approved exceptions or necessary technical variations.

---

# 22. Security Policy Exception Management

Security exceptions allow a documented deviation from a requirement when justified and authorized.

### Example

A legacy application cannot support a newly proposed authentication requirement.

### Exception Requirements

- Policy reference
- Affected resource
- Business justification
- Risk assessment
- Compensating controls
- Responsible owner
- Authorization
- Expiration or review date
- Remediation plan where applicable

## Exception Procedure

1. Receive the exception request.
2. Identify the affected policy.
3. Confirm the business requirement.
4. Evaluate the security risk.
5. Identify alternatives.
6. Identify compensating controls.
7. Define the requested duration.
8. Obtain appropriate authorization.
9. Document the decision.
10. Review the exception before expiration.
11. Renew, remediate, or close the exception.

### Example Exception Record

```text
Exception ID:
SEC-EXC-001

Related Policy:
SEC-POL-001

Affected Resource:
Legacy Application

Requested Deviation:
Alternative authentication requirement

Business Justification:
Application compatibility limitation

Risk Classification:
Pending Assessment

Compensating Controls:
To Be Evaluated

Authorization Status:
Pending

Expiration:
To Be Determined

Remediation Plan:
Pending
```

### Important

An exception is not automatically approved because it has been documented.

A risk acceptance decision must be made by the appropriate authority.

---

# 23. Security Policy Noncompliance

Noncompliance occurs when an applicable requirement is not satisfied.

### Potential Findings

- Missing security configuration
- Excessive administrative access
- Disabled required logging
- Unauthorized firewall rule
- Unapproved software
- Unmanaged endpoint
- Expired security exception
- Incorrect policy assignment

### Noncompliance Procedure

1. Identify the requirement.
2. Identify the affected system.
3. Collect evidence.
4. Confirm the finding.
5. Evaluate impact and risk.
6. Determine whether an exception exists.
7. Identify corrective actions.
8. Assign responsibility.
9. Track remediation.
10. Verify the corrected state.
11. Document closure.

### Possible Outcomes

- Remediated
- Approved exception
- Under investigation
- Pending authorized change
- Risk accepted by appropriate authority
- Escalated

### Important

A finding should not be marked remediated until the corrective action has been verified.

---

# 24. Security Policy Review and Retirement

Security policies should remain aligned with organizational needs.

### Proposed Review Frequency

| Policy Category | Suggested Review |
|---|---|
| Identity and Access | Annual or after significant change |
| Privileged Access | Annual or after significant change |
| Authentication | Annual or after significant change |
| Endpoint Security | Annual or after significant change |
| Server Security | Annual or after significant change |
| Network Security | Annual or after significant change |
| Cloud Security | Annual or after significant change |
| Data Protection | Annual or after significant change |
| Logging and Monitoring | Annual or after significant change |

These are proposed review intervals, not mandatory ITIL requirements.

### Review Triggers

- New threats
- Significant incidents
- Infrastructure changes
- Licensing changes
- New business requirements
- Applicable regulatory changes
- Audit findings
- Repeated exceptions
- Continual improvement findings

### Retirement Procedure

1. Confirm the policy is obsolete or superseded.
2. Identify dependent standards and procedures.
3. Evaluate the impact of retirement.
4. Obtain required authorization.
5. Record the retirement decision.
6. Update references.
7. Archive the superseded version appropriately.
8. Communicate relevant changes.

### Important

Retiring a policy does not automatically remove technical controls.

Any required configuration changes must be evaluated separately.

---

# 25. Example Lab — Active Directory Security Policy Review

## Scenario Overview

Technical Techno Tech conducts a review of Active Directory security configurations.

**Environment:** `homelab.local`  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Primary Systems:** DC01 and DC02

### Objective

Review password, account lockout, and audit configurations against proposed security requirements.

### Step 1 — Review Default Domain Password Policy

```powershell
Get-ADDefaultDomainPasswordPolicy |
Format-List
```

### Step 2 — Review Fine-Grained Password Policies

```powershell
Get-ADFineGrainedPasswordPolicy -Filter * |
Format-List
```

### Step 3 — Review Applied Group Policy

```powershell
Get-GPO -All |
Select-Object DisplayName, GpoStatus
```

### Step 4 — Review Audit Policy

On the appropriate Windows system:

```powershell
auditpol /get /category:*
```

### Step 5 — Document Actual Configuration

Record:

- Password policy settings
- Lockout settings
- Relevant GPOs
- Audit configuration
- Date and time
- Administrative tool
- Observed values

### Step 6 — Compare Against Proposed Requirements

| Control | Expected State | Actual State |
|---|---|---|
| Password policy | Defined by approved baseline | Not yet evaluated |
| Account lockout | Defined by approved baseline | Not yet evaluated |
| Audit policy | Required events enabled | Not yet evaluated |
| Administrative access | Restricted to authorized identities | Not yet evaluated |

### Step 7 — Identify Findings

Potential outcomes:

- Meets proposed requirement
- Does not meet proposed requirement
- Not applicable
- Requires further investigation

### Step 8 — Document Recommendations

Any proposed configuration change should include:

- Business justification
- Security benefit
- Potential impact
- Testing requirements
- Authorization requirements
- Rollback considerations

### Lab Status

This scenario defines a review procedure.

No specific compliance findings or configuration results are claimed until the checks are performed.

---

# 26. Example Lab — Group Policy Security Configuration

## Scenario Overview

A Systems Administrator evaluates a proposed security configuration for Windows workstations.

### Objective

Demonstrate the process of developing, testing, and verifying a security configuration through Group Policy.

### Proposed Workflow

1. Identify the security requirement.
2. Review current workstation configuration.
3. Identify the appropriate Group Policy setting.
4. Evaluate compatibility.
5. Create or select an authorized test GPO.
6. Scope the GPO to designated test systems.
7. Configure the approved setting.
8. Update Group Policy on the test computer.
9. Verify effective configuration.
10. Document results.

### Example Commands

Refresh policy:

```powershell
gpupdate /force
```

Review resultant policy:

```powershell
gpresult /r
```

Generate a report:

```powershell
gpresult /h C:\Temp\Workstation-Policy-Report.html
```

The destination directory must exist.

### Verification Questions

- Was the GPO applied?
- Did the intended setting take effect?
- Were unrelated systems affected?
- Did required applications continue functioning?
- Did the configuration create unexpected restrictions?

### Important

`gpupdate /force` requests Group Policy processing but does not guarantee every setting is immediately effective.

Some settings require a restart, sign-out, or other conditions.

### Lab Status

This is a proposed lab workflow. Record the actual GPO, setting, test scope, and results during execution.

---

# 27. Example Lab — Intune Security Policy

## Scenario Overview

Technical Techno Tech evaluates an endpoint security requirement for managed Windows devices.

### Objective

Demonstrate the relationship between a security policy, an Intune configuration, and technical verification.

### Proposed Workflow

1. Identify the endpoint security requirement.
2. Review supported Intune policy types.
3. Confirm licensing and device enrollment.
4. Select an appropriate configuration.
5. Define a limited test group.
6. Create the policy.
7. Assign the test group.
8. Monitor deployment status.
9. Verify the device configuration.
10. Document actual results.

### Example Verification Record

```text
Policy ID:
SEC-POL-002

Platform:
Microsoft Intune

Target:
Windows Test Device

Security Requirement:
To Be Defined

Configuration Profile:
Not Yet Created

Assignment:
Not Yet Configured

Deployment Status:
Not Tested

Device Verification:
Pending
```

### Important

An Intune policy appearing in the administrative portal does not prove successful application to the endpoint.

Device-level verification is required.

### Lab Status

This scenario is proposed. It does not claim that an Intune policy has been deployed.

---

# 28. Security Policy Record Template

```text
SECURITY POLICY RECORD

Policy ID:
Policy Title:
Version:
Status:

Policy Owner:
Responsible Function:

Purpose:
Business Justification:
Related Security Risk:

Scope:
Affected Services:
Affected Systems:
Related Configuration Items:

Policy Requirements:
Supporting Standards:
Related Procedures:

Technical Controls:
Control Owners:

Operational Impact:
Testing Requirements:
Rollback Considerations:

Review Status:
Authorization Status:
Approving Role:
Authorization Reference:

Effective Date:
Publication Date:
Next Review Date:

Compliance Method:
Evidence Requirements:

Exceptions:
Known Limitations:

Related Service Request:
Related Incident:
Related Problem:
Related Change:
Related Improvement:

Current Status:
Outstanding Actions:
Revision History:
```

---

# 29. Security Policy Exception Template

```text
SECURITY POLICY EXCEPTION

Exception ID:
Related Policy ID:

Requesting Role:
Resource Owner:
Affected System:
Related CI:

Requested Exception:
Business Justification:

Security Risk:
Risk Classification:
Existing Controls:
Proposed Compensating Controls:

Alternative Solutions:
Remediation Plan:

Requested Start Date:
Requested Expiration Date:

Authorization Status:
Approving Role:
Decision Reference:

Monitoring Requirements:
Review Date:

Current Status:
Outstanding Actions:
Notes:
```

---

# 30. Proposed Repository Structure

```text
Information-Security-Management/
├── README.md
├── Procedures/
│   ├── Access-Control.md
│   ├── Privileged-Access.md
│   └── Security-Policy-Management.md
└── Records/
    └── SEC-POL-001-Example-Policy-Review/
        ├── README.md
        └── Evidence/
            ├── 01-Policy-Requirements.md
            ├── 02-Risk-Assessment.md
            ├── 03-Policy-Review.md
            ├── 04-Implementation.md
            └── 05-Verification.md
```

This is an illustrative structure.

Record directories and evidence files should be created only when corresponding activities are documented.

---

# 31. Security Policy Evidence Standards

Security policy documentation should distinguish written requirements from implemented controls.

### Evidence Categories

**Policy Evidence**

- Draft policy
- Review comments
- Authorization record
- Published version
- Revision history

**Implementation Evidence**

- Group Policy settings
- Intune configuration
- Microsoft Entra configuration
- Azure Policy assignment
- Firewall configuration
- Security group configuration

**Verification Evidence**

- Effective policy reports
- Device configuration results
- Audit events
- Access tests
- Compliance reports
- Configuration comparisons

**Review Evidence**

- Periodic review records
- Exception decisions
- Noncompliance findings
- Corrective action verification

### Evidence Requirements

Each item should identify:

1. Source system
2. Date and time
3. Relevant policy
4. Target resource
5. Administrative tool
6. Action or observation
7. Actual result
8. Verification status

### Evidence Integrity

Do not fabricate:

- Policy approvals
- Compliance results
- Security configurations
- Audit findings
- Test outcomes
- Exception authorizations
- Remediation completion

### Sensitive Information

Do not publish:

- Passwords
- Private keys
- Access tokens
- Recovery secrets
- Sensitive production security settings
- Unredacted credentials

---

# 32. Security Policy Management and Change Enablement

Security policy changes and technical implementation changes are related but distinct.

### Example

**Policy Decision:** Require additional authentication protection for privileged accounts.

**Technical Changes:** Configure applicable identity security settings.

### Potential Change Requirements

- Risk assessment
- Change authorization
- Implementation plan
- Validation plan
- Rollback plan
- Communication
- Post-implementation review

### Important

A policy revision may not require a technical change if existing controls already satisfy the new requirements.

Conversely, a technical configuration change may be necessary without changing the underlying policy.

---

# 33. Security Policy Management and Service Configuration Management

Service Configuration Management helps identify assets affected by security requirements.

### Examples

- Domain controllers
- File servers
- Workstations
- Network devices
- Microsoft 365 tenant
- Azure virtual machines

### Benefits

- Improved policy scoping
- Better impact assessment
- Identification of control owners
- More accurate compliance reviews
- Improved change planning

### Important

A Configuration Item record identifies relevant information about a system or service.

It does not automatically verify security compliance.

---

# 34. Security Policy Management and Monitoring

Monitoring supports detection of conditions that may indicate security policy violations.

### Examples

- Unexpected administrative role assignment
- Repeated authentication failures
- Disabled security logging
- Unauthorized firewall modifications
- Endpoint security control failures
- Configuration drift

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
Policy Requirement Review
          |
          v
Determine Security Significance
          |
          v
Appropriate Response / Escalation
```

### Important

An alert is not automatically proof of noncompliance or malicious activity.

The event must be evaluated against the applicable requirement and supporting evidence.

---

# 35. Security Policy Management and Continual Improvement

Security policy reviews may identify opportunities to improve technical controls and operational processes.

### Potential Improvement Sources

- Repeated security incidents
- Configuration drift
- Failed policy deployments
- Excessive administrative access
- Recurring exceptions
- Audit findings
- User support trends
- New security capabilities

### Example Improvement Record

```text
Improvement ID:
IMP-001

Source:
Security Policy Review

Finding:
Administrative access assignments
are not consistently documented.

Proposed Improvement:
Standardize privileged access records
and periodic reviews.

Owner:
To Be Assigned

Status:
Proposed
```

### Important

A proposed improvement is not considered implemented until the necessary actions are completed and verified.

---

# 36. Common Security Policy Management Errors

### Error 1 — Confusing Policy With Configuration

**Incorrect:** Assuming a written password policy automatically configures Active Directory.

**Correct:** Implement and verify the corresponding technical controls.

### Error 2 — Unclear Requirements

**Incorrect:** "All systems must be secure."

**Correct:** Define specific, measurable security requirements.

### Error 3 — Missing Policy Ownership

**Incorrect:** Creating policies without assigning responsibility for review and maintenance.

**Correct:** Identify an accountable policy owner.

### Error 4 — Unverified Compliance

**Incorrect:** Declaring compliance because a setting was configured.

**Correct:** Verify effective behavior and collect evidence.

### Error 5 — Ignoring Operational Impact

**Incorrect:** Applying restrictive settings without testing dependencies.

**Correct:** Assess compatibility and service impact.

### Error 6 — Uncontrolled Exceptions

**Incorrect:** Allowing policy deviations without documentation.

**Correct:** Evaluate and authorize exceptions appropriately.

### Error 7 — Overly Broad Policy Scope

**Incorrect:** Applying a security setting to all devices without evaluating differences.

**Correct:** Define appropriate target populations and exclusions.

### Error 8 — Confusing Intune Compliance and Configuration

**Incorrect:** Assuming device compliance means all security settings are configured.

**Correct:** Evaluate compliance and configuration results separately.

### Error 9 — Ignoring Policy Conflicts

**Incorrect:** Deploying overlapping configurations without checking for conflicting settings.

**Correct:** Review existing assignments and effective policy behavior.

### Error 10 — Claiming Regulatory Compliance Without Evidence

**Incorrect:** Declaring the lab compliant with a regulatory framework based only on documentation.

**Correct:** Identify applicable requirements and verify conformance before making compliance claims.

### Error 11 — Publishing Sensitive Information

**Incorrect:** Including credentials or private security information in GitHub.

**Correct:** Publish sanitized documentation.

### Error 12 — Treating Simulated Approval as Real Approval

**Incorrect:** Recording fictional management authorization as an actual independent decision.

**Correct:** Clearly label simulated organizational decisions.

---

# 37. Security Policy Quality Checklist

## Policy Development

- [ ] Security requirement identified
- [ ] Business justification documented
- [ ] Relevant risks evaluated
- [ ] Affected services identified
- [ ] Affected systems identified
- [ ] Policy owner identified
- [ ] Policy scope defined
- [ ] Requirements written clearly
- [ ] Supporting standards identified

## Review and Authorization

- [ ] Operational impact evaluated
- [ ] Technical feasibility reviewed
- [ ] Relevant stakeholders identified
- [ ] Review comments documented
- [ ] Required authorization obtained
- [ ] Policy version recorded
- [ ] Effective date documented

## Implementation

- [ ] Technical controls identified
- [ ] Control owners identified
- [ ] Licensing requirements reviewed
- [ ] Testing requirements defined
- [ ] Change requirements evaluated
- [ ] Implementation documented
- [ ] Configuration verified

## Monitoring and Compliance

- [ ] Compliance method defined
- [ ] Evidence requirements documented
- [ ] Noncompliance findings tracked
- [ ] Exceptions documented
- [ ] Corrective actions assigned
- [ ] Remediation verified

## Lifecycle Management

- [ ] Review schedule defined
- [ ] Policy owner confirmed
- [ ] Revision history maintained
- [ ] Superseded versions identified
- [ ] Related procedures reviewed
- [ ] Continual improvement opportunities recorded

## Portfolio Documentation

- [ ] Fictional scenarios clearly labeled
- [ ] Simulated approvals identified
- [ ] Proposed controls distinguished from implemented controls
- [ ] Actual test results supported by evidence
- [ ] Sensitive information removed
- [ ] Relative documentation links verified

---

# 38. Security Policy Performance Metrics

| Metric | Purpose |
|---|---|
| Policy Review Completion Rate | Measures completion of scheduled policy reviews |
| Policy Authorization Rate | Tracks policies receiving required authorization |
| Security Control Verification Rate | Measures verified technical controls |
| Policy Noncompliance Findings | Tracks confirmed deviations |
| Noncompliance Remediation Time | Measures time required to correct findings |
| Exception Review Completion Rate | Tracks review of active exceptions |
| Expired Exception Count | Identifies exceptions requiring attention |
| Configuration Drift Findings | Tracks deviations from approved baselines |
| Security Policy Documentation Completeness | Evaluates policy record quality |
| Policy Implementation Coverage | Measures applicable systems with required controls |
| Corrective Action Verification Rate | Tracks verified remediation |

### Example Calculations

**Policy Review Completion Rate**

```text
Policy Review Completion (%) =
Completed Policy Reviews
------------------------ x 100
Scheduled Policy Reviews
```

**Security Control Verification Rate**

```text
Control Verification (%) =
Verified Security Controls
-------------------------- x 100
Security Controls Requiring Verification
```

**Corrective Action Verification Rate**

```text
Corrective Action Verification (%) =
Verified Corrective Actions
--------------------------- x 100
Completed Corrective Actions Requiring Verification
```

### Measurement Requirements

- Define the reporting period.
- Use actual records.
- Identify the measurement population.
- Distinguish proposed requirements from approved requirements.
- Exclude unverified assumptions.
- Do not invent compliance results.

---

# 39. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Follows security policies and routes security-related requests |
| Incident Management | Responds to incidents involving security controls or policy violations |
| Service Request Management | Fulfills authorized requests according to security requirements |
| Knowledge Management | Maintains security procedures and technical guidance |
| Problem Management | Investigates recurring security configuration issues |
| Change Enablement | Evaluates and authorizes applicable security configuration changes |
| Monitoring and Event Management | Detects events relevant to security policy enforcement |
| Service Configuration Management | Identifies assets, configurations, and dependencies affected by policies |
| Information Security Management | Defines security requirements and manages information security risks |
| Continual Improvement | Evaluates security control effectiveness and process improvements |

---

# 40. Procedure Review

Review this procedure when:

- Organizational security requirements change.
- New technologies are introduced.
- Authentication or authorization requirements change.
- Security incidents reveal control weaknesses.
- New security policies are developed.
- Existing policies are revised or retired.
- Significant configuration changes occur.
- Applicable external requirements change.
- Policy reviews identify recurring exceptions.
- Continual improvement identifies opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Security Policy Management procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Security policies, organizational requirements, approving authorities, business risks, compliance objectives, and operational scenarios may be simulated.

Technical configurations, Group Policy settings, Microsoft Entra security controls, Intune policies, Azure Policy assignments, network security settings, and verification results are documented as hands-on lab activities only when supporting evidence exists.

Proposed policies, standards, security baselines, exception workflows, compliance monitoring capabilities, and automated enforcement mechanisms must not be represented as implemented or approved without supporting evidence.

Simulated policy approvals do not constitute independent organizational authorization.

Expected technical outcomes and illustrative compliance findings must not be represented as actual observations.

GitHub publication does not imply production security operations, regulatory compliance, independent security approval, or professional employment experience.

This procedure demonstrates ITIL-aligned Information Security Management, security policy governance, risk-based control selection, Windows security administration, Group Policy management, cloud security configuration, compliance verification, exception management, and continual security improvement.

---