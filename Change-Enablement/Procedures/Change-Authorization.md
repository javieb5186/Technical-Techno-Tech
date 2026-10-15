# SOP — Change Authorization

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Change Enablement  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-CE-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Change Enablement

---

## 1. Purpose

This procedure establishes a standardized process for evaluating and authorizing changes to Technical Techno Tech's internal IT services and infrastructure.

Change authorization ensures that proposed modifications are assessed for business value, technical risk, operational impact, security requirements, and implementation readiness before execution.

The procedure supports:

- Controlled infrastructure modifications
- Reduction of change-related incidents
- Consistent risk assessment
- Appropriate authorization
- Clear accountability
- Improved service availability
- Protection of production and lab environments
- Effective change scheduling
- Reliable rollback planning
- Accurate change documentation
- Continual improvement

**Key Principle:** A change must receive the authorization appropriate to its type, risk, and organizational policy before implementation.

Authorization does not guarantee that a change will succeed. It confirms that the proposed change has been evaluated and accepted for implementation under defined conditions.

---

## 2. Scope

This procedure applies to proposed changes affecting Technical Techno Tech's internal IT services and supporting infrastructure.

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

### Technical Environments

Changes may involve:

- Windows 11 workstations
- Windows Server
- Active Directory Domain Services
- Group Policy
- DNS and DHCP
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V virtualization
- Network routers and switches
- OPNsense
- VyOS

### Examples of Changes

- Modifying Group Policy settings
- Updating Windows Server configurations
- Deploying operating system updates
- Changing firewall rules
- Modifying DNS or DHCP settings
- Updating network routing
- Deploying applications
- Changing endpoint management policies
- Modifying authentication configurations
- Adding or removing infrastructure components
- Implementing corrective actions identified through Problem Management

Routine service requests do not automatically require separate change authorization. The applicable service request or change procedure determines how they are controlled.

---

## 3. ITIL 4 Change Enablement

### Purpose

The purpose of Change Enablement is to maximize the number of successful service and product changes by ensuring that risks have been properly assessed, authorizing changes to proceed, and managing the change schedule.

### Important Definitions

**Change:** The addition, modification, or removal of anything that could have a direct or indirect effect on services.

**Change Authorization:** The decision permitting a proposed change to proceed under defined conditions.

**Change Authority:** A person or group responsible for authorizing a change.

**Change Schedule:** Information used to plan changes and identify potential conflicts.

**Rollback / Backout Plan:** A documented approach for returning to an acceptable previous state if implementation fails.

**Change Advisory Board (CAB):** A group that may advise or support the assessment and authorization of certain changes.

### Change Authorization vs. Change Implementation

| Change Authorization | Change Implementation |
|---|---|
| Evaluates whether a change should proceed | Performs the approved technical modification |
| Reviews risk and impact | Executes the implementation plan |
| Confirms required preparation | Follows approved implementation steps |
| Establishes approval conditions | Validates the resulting system state |
| Records the authorization decision | Records execution results |

A technically feasible change is not necessarily an authorized change.

---

## 4. Change Types

Technical Techno Tech uses three change types.

### 4.1 Standard Change

A standard change is a low-risk, preauthorized change that is well understood and fully documented.

Examples may include:

- Repeating an approved routine configuration task
- Deploying an approved application through an established procedure
- Performing a documented low-risk maintenance activity

### Standard Change Requirements

- Documented procedure
- Defined scope
- Known risks
- Established validation
- Appropriate preauthorization
- Consistent execution conditions

**Important:** A change is not automatically standard simply because it is routine. It must meet the organization's preauthorization criteria.

### 4.2 Normal Change

A normal change requires assessment and authorization appropriate to its risk and impact.

Examples:

- Modifying a domain-wide Group Policy
- Changing DNS server configurations
- Deploying a new server role
- Updating network routing
- Modifying firewall access rules

Normal changes may require different authorization levels depending on their risk.

### 4.3 Emergency Change

An emergency change must be implemented as soon as possible to address an urgent situation.

Examples:

- Applying an urgent security correction
- Restoring a critical infrastructure dependency
- Addressing an imminent severe service failure

Emergency changes follow an expedited assessment and authorization process.

**Important:** Emergency does not mean unauthorized. Emergency changes still require appropriate authorization and documentation, with the process adapted to the urgency.

---

## 5. Roles and Responsibilities

### Change Requester

Responsible for:

- Submitting the proposed change
- Explaining the business justification
- Identifying expected benefits
- Providing initial impact information
- Supporting clarification requests

### Change Owner

Responsible for:

- Coordinating the change
- Completing required documentation
- Identifying affected services
- Coordinating technical assessment
- Preparing implementation and rollback plans
- Tracking authorization status

### Technical Reviewer

Responsible for:

- Reviewing technical feasibility
- Assessing implementation risks
- Identifying dependencies
- Evaluating validation methods
- Reviewing rollback readiness
- Recommending approval conditions

### Change Authority

Responsible for:

- Reviewing the change assessment
- Evaluating business and technical risks
- Confirming required information
- Authorizing, rejecting, or requesting revisions
- Documenting the decision

### Change Coordinator

Responsible for:

- Maintaining the change schedule
- Coordinating reviews
- Identifying scheduling conflicts
- Recording authorization outcomes
- Monitoring compliance with the change process

### Information Security Personnel

Responsible for:

- Reviewing security-sensitive changes
- Assessing security control implications
- Identifying relevant compliance or access risks
- Providing required security authorization when applicable

### Implementation Technician

Responsible for:

- Confirming authorization before execution
- Following the approved implementation plan
- Recording technical results
- Performing validation
- Initiating approved rollback procedures when required

### Change Advisory Board

A CAB may provide advice on:

- Complex changes
- High-risk infrastructure modifications
- Changes affecting multiple services
- Significant scheduling conflicts
- Business-critical changes

**ITIL Note:** ITIL 4 does not require every change to be approved by a CAB. Change authorities should be assigned according to the change's characteristics and organizational policy.

**Lab Note:** These roles represent simulated organizational responsibilities. A single learner may perform multiple roles during a controlled lab exercise. Simulated authorization must not be represented as independent organizational approval.

---

## 6. Change Authorization Principles

### 6.1 Risk-Based Authorization

Authorization requirements should reflect the potential risk and impact of the change.

### 6.2 Appropriate Change Authority

The person or group authorizing a change must have the appropriate responsibility and authority.

### 6.3 Complete Change Documentation

The change must contain sufficient information to support an informed decision.

### 6.4 Business Justification

The expected benefit or necessity of the change should be documented.

### 6.5 Technical Readiness

Implementation, validation, and recovery requirements should be reviewed before approval.

### 6.6 Security Considerations

Changes must preserve applicable security controls and access requirements.

### 6.7 Scheduling Awareness

Authorization should consider service availability, dependencies, and conflicting changes.

### 6.8 Traceability

All authorization decisions should be documented and linked to the relevant Change record.

### 6.9 Separation of Approval and Execution

Where practical, higher-risk changes should receive review from someone other than the implementer.

### 6.10 Controlled Reassessment

Material changes to the approved scope, risk, or implementation plan should trigger reassessment.

---

## 7. Change Authorization Requirements

A normal change should contain sufficient information for assessment.

### Required Information

| Field | Description |
|---|---|
| Change ID | Unique change identifier |
| Change Title | Concise description |
| Change Type | Standard, Normal, or Emergency |
| Requester | Person proposing the change |
| Change Owner | Responsible coordinator |
| Business Justification | Reason the change is needed |
| Affected Services | Services potentially impacted |
| Affected Configuration Items | Relevant infrastructure components |
| Technical Description | Proposed modification |
| Risk Assessment | Potential failure and security risks |
| Impact Assessment | Expected operational consequences |
| Implementation Plan | Planned technical steps |
| Validation Plan | How success will be verified |
| Rollback Plan | How an unsuccessful change will be handled |
| Proposed Schedule | Intended implementation window |
| Dependencies | Required systems, personnel, or preceding activities |
| Authorization Decision | Approval, rejection, or revision outcome |

Additional requirements may apply to significant or security-sensitive changes.

---

## 8. Change Authorization Decision Matrix

Technical Techno Tech uses a proposed risk-based authorization model.

| Change Type / Risk | Proposed Change Authority | Authorization Approach |
|---|---|---|
| Standard — Preauthorized | Designated owner of the approved standard change model | Confirm that the change meets the preauthorized conditions |
| Normal — Low Risk | Delegated Change Authority | Review and authorize |
| Normal — Medium Risk | Change Coordinator or designated IT authority | Technical and operational assessment |
| Normal — High Risk | Senior IT authority, supported by relevant technical and business reviewers | Formal risk review and authorization |
| Emergency | Designated Emergency Change Authority | Expedited assessment and authorization |

### Additional Authorization

Depending on the change, authorization may also be required from:

- Information Security
- Service Owner
- Infrastructure Owner
- Business Stakeholder
- Cloud Administrator
- Network Administrator

### Important Distinction

Technical review and change authorization are separate decisions.

A technical reviewer may recommend approval without being the authorized decision-maker.

This matrix is a proposed internal governance model, not a mandatory ITIL 4 approval structure.

---

## 9. Change Risk Assessment

Before authorization, the proposed change should be assessed for potential risk.

### Risk Factors

1. Business impact
2. Service criticality
3. Number of affected users
4. Technical complexity
5. Implementation uncertainty
6. Security implications
7. Dependency relationships
8. Recovery capability
9. Testing completeness
10. Scheduling conflicts

### Proposed Risk Levels

| Risk Level | Description |
|---|---|
| Low | Limited impact, predictable implementation, and straightforward recovery |
| Medium | Moderate service impact or technical uncertainty |
| High | Significant service impact, complex dependencies, or difficult recovery |
| Critical | Potential for severe disruption, significant security exposure, or widespread operational impact |

### Risk Assessment Example

**Proposed Change:** Modify DNS settings on one lab workstation.

**Potential Risk:** Low, assuming the configuration is isolated and easily reversible.

**Alternative Change:** Modify DHCP DNS options used by multiple departments.

**Potential Risk:** Medium or High, depending on affected services, scope, and recovery capability.

Risk should be determined by the actual circumstances, not only the technology involved.

---

## 10. Change Authorization Workflow

```text
Change Request Submitted
           |
           v
Review Change Documentation
           |
           v
Determine Change Type
           |
           v
Evaluate Business Justification
           |
           v
Assess Technical Risk and Impact
           |
           v
Review Implementation Plan
           |
           v
Review Validation and Rollback
           |
           v
Check Dependencies and Schedule
           |
           v
Identify Required Change Authority
           |
           v
Submit for Authorization
           |
           v
    Authorization Decision
           |
     +-----+------+----------+
     |            |          |
  Approved     Revisions   Rejected
     |          Required      |
     v            |           v
Record Approval   v       Document
Conditions     Return to   Decision
     |         Requester
     v            |
Confirm Schedule  |
     |            |
     v            |
Authorized for    |
Implementation    |
                  |
                  v
              Reassessment
```

An approved change proceeds to implementation only when its authorization conditions have been satisfied.

---

## 11. Change Authorization Procedure

### Step 1 — Receive the Change Request

Open the submitted Change record.

Review:

- Change ID
- Title
- Description
- Requester
- Change owner
- Proposed change type
- Business justification
- Affected services
- Proposed implementation date

#### Example

```text
Change ID: CHG-001

Title:
Update DNS Configuration for Domain-Joined Workstations

Change Type:
Normal

Affected Service:
IT-SVC-004 — Network Connectivity

Related Problem:
PRB-001
```

**Expected Result:** The proposed change is available for authorization review.

### Step 2 — Verify Documentation Completeness

Check that the Change record contains the information required for assessment.

Confirm:

- Scope is defined.
- Business justification is documented.
- Affected systems are identified.
- Implementation steps are available.
- Validation requirements are documented.
- Recovery considerations are addressed.
- Required dependencies are identified.

If critical information is missing, return the request for clarification.

**Expected Result:** The Change record contains sufficient information for review.

### Step 3 — Confirm the Change Type

Determine whether the change is:

- Standard
- Normal
- Emergency

#### Standard Change

Verify that the proposed activity falls within an approved standard change model.

#### Normal Change

Proceed through the applicable risk-based assessment and authorization process.

#### Emergency Change

Use the expedited authorization process defined in this procedure.

**Expected Result:** The change follows the appropriate authorization path.

### Step 4 — Review Business Justification

Determine why the change is necessary.

Possible justifications include:

- Resolving an identified problem
- Improving service reliability
- Addressing a security risk
- Supporting a new business requirement
- Increasing capacity
- Improving system performance
- Replacing unsupported technology

#### Review Questions

1. What problem or requirement does the change address?
2. What benefit is expected?
3. What happens if the change is not implemented?
4. Is the proposed scope appropriate?
5. Are alternative solutions available?

**Expected Result:** The change has a documented business or technical justification.

### Step 5 — Identify Affected Services and Configuration Items

Review the services and infrastructure potentially affected.

#### Example

**Proposed Change:** Modify DHCP DNS server options.

**Potentially Affected Components:**

- DHCP server
- Domain controllers
- DNS servers
- Domain-joined workstations
- Network segments receiving the DHCP configuration

**Potentially Affected Services:**

- IT-SVC-001 — Identity & Access Management
- IT-SVC-004 — Network Connectivity
- IT-SVC-005 — Server & Infrastructure Services

Review available Configuration Item records and dependency maps.

**Expected Result:** Relevant dependencies and affected services are identified.

### Step 6 — Evaluate Technical Risk

Assess the potential consequences of implementation failure.

Consider:

- Loss of connectivity
- Authentication disruption
- Application downtime
- Incorrect access permissions
- Configuration conflicts
- Security exposure
- Service dependency failures
- Recovery difficulties

#### Example

Changing DNS configuration may affect domain controller discovery.

An incorrect configuration could prevent workstations from locating required directory services.

**Expected Result:** Technical risks are documented.

### Step 7 — Evaluate Business Impact

Determine how the change may affect employees and business operations.

Review:

- Number of affected employees
- Criticality of affected services
- Expected downtime
- Potential service degradation
- Availability of alternatives
- Business operating hours
- Required stakeholder communication

### Impact Levels

| Impact | Description |
|---|---|
| High | Significant disruption to critical services or multiple departments |
| Medium | Moderate disruption to a department or several users |
| Low | Limited disruption to an individual system or small user group |

**Expected Result:** Business impact is understood.

### Step 8 — Review the Implementation Plan

Verify that the technical implementation is documented.

The plan should include:

1. Prerequisites
2. Required permissions
3. Affected systems
4. Preparation steps
5. Implementation sequence
6. Required tools
7. Expected results
8. Validation checkpoints
9. Communication requirements

### Example

**Proposed Change:** Update DHCP DNS server options.

**Implementation Plan:**

1. Review the existing DHCP configuration.
2. Record current DNS options.
3. Verify approved replacement values.
4. Confirm affected scopes.
5. Schedule the change.
6. Apply the authorized configuration.
7. Test client DHCP renewal.
8. Verify DNS resolution.
9. Confirm domain controller discovery.

**Expected Result:** The proposed implementation is sufficiently defined.

### Step 9 — Review the Validation Plan

Determine how successful implementation will be verified.

Validation should address:

- Technical functionality
- Service availability
- Business requirements
- Security requirements
- Configuration accuracy
- Unexpected side effects

#### Example Validation Commands

**DNS Configuration**

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

**DNS Resolution**

```powershell
nslookup dc01.homelab.local
```

**Domain Controller Discovery**

```powershell
nltest /dsgetdc:homelab.local
```

These commands are examples of possible validation activities.

They do not indicate that the change has been executed.

**Expected Result:** Success criteria are defined before authorization.

### Step 10 — Review the Rollback Plan

Verify that the change includes an appropriate recovery strategy.

The plan should identify:

- Conditions requiring rollback
- Previous configuration values
- Required backups or exports
- Recovery steps
- Responsible personnel
- Expected recovery time
- Post-rollback validation

### Example

**Change:** Modify DHCP DNS server options.

**Rollback Plan:**

1. Stop further implementation if validation fails.
2. Restore the previously documented DHCP options.
3. Apply the appropriate client renewal procedure.
4. Verify DNS resolution.
5. Confirm domain controller discovery.
6. Record rollback results.

Rollback feasibility should be assessed before authorization.

**Expected Result:** A recovery approach is documented.

### Step 11 — Review Security Requirements

Determine whether the change affects:

- Authentication
- Authorization
- Privileged access
- Firewall controls
- Endpoint security
- Logging and auditing
- Data protection
- Network segmentation
- Security policies

Security-sensitive changes may require additional review.

#### Example

**Proposed Change:** Modify a firewall rule permitting administrative access.

The change should be evaluated for:

- Source restrictions
- Destination restrictions
- Required ports
- Administrative authorization
- Security monitoring
- Potential unauthorized access

**Expected Result:** Relevant security risks are assessed.

### Step 12 — Review Change Dependencies

Determine whether the change depends on other activities.

Examples:

- Required server availability
- Backup completion
- Network connectivity
- Vendor support
- Administrative credentials
- Completion of another change
- Maintenance window availability

#### Example

A domain controller configuration change may depend on:

- Healthy Active Directory replication
- Available domain controller backups
- Functional DNS services
- Administrative access

**Expected Result:** Required dependencies are identified.

### Step 13 — Review the Change Schedule

Evaluate the proposed implementation window.

Consider:

1. Business operating hours
2. Expected downtime
3. Other scheduled changes
4. Service maintenance requirements
5. Available technical personnel
6. Required stakeholder communication
7. Recovery time

### Scheduling Conflicts

Avoid scheduling changes that could interfere with each other without appropriate coordination.

#### Example

A DNS infrastructure change and an Active Directory maintenance activity may affect overlapping services.

The Change Coordinator should review the combined risk.

**Expected Result:** Scheduling conflicts are evaluated.

### Step 14 — Identify the Change Authority

Determine who is authorized to approve the proposed change.

The decision should reflect:

- Change type
- Risk level
- Business impact
- Security requirements
- Technical complexity
- Organizational responsibility

#### Example

```text
Change Type: Normal
Risk Level: Medium

Proposed Authority:
Designated IT Change Authority

Additional Review:
Systems Administration
```

The named authority must reflect the organization's adopted governance model.

**Expected Result:** The appropriate authorization responsibility is identified.

### Step 15 — Submit for Authorization

Provide the Change record and supporting assessment to the designated authority.

The authorization package should include:

- Change description
- Business justification
- Risk assessment
- Impact assessment
- Implementation plan
- Validation plan
- Rollback plan
- Schedule
- Required technical reviews
- Outstanding concerns

**Expected Result:** The proposed change is ready for an authorization decision.

### Step 16 — Evaluate the Authorization Decision

The Change Authority reviews the proposal and records a decision.

### Possible Decisions

| Decision | Description |
|---|---|
| Approved | Change may proceed under the approved conditions |
| Approved With Conditions | Change may proceed after specified requirements are satisfied |
| Changes Required | Proposal must be revised and reassessed |
| Rejected | Change is not authorized |
| Deferred | Decision is postponed pending additional information or a suitable schedule |

### Example

**Decision:** Approved With Conditions

**Conditions:**

- Complete a current configuration backup.
- Confirm domain controller health.
- Perform the change during the approved maintenance window.
- Validate DNS and authentication after implementation.

**Expected Result:** A documented authorization decision is available.

### Step 17 — Record the Authorization

Update the Change record with:

- Decision
- Authorizing role
- Authorization date and time
- Risk level
- Conditions
- Approved scope
- Approved implementation window
- Review comments

### Example Authorization Record

```text
CHANGE AUTHORIZATION RECORD

Change ID:
Change Type:
Risk Level:
Affected Services:

Authorization Decision:
Authorized By:
Authorization Date/Time:

Approved Scope:

Implementation Window:

Authorization Conditions:

Required Technical Reviews:

Security Review:

Additional Notes:
```

**Expected Result:** The authorization is traceable.

### Step 18 — Communicate the Decision

Notify relevant participants.

Potential recipients include:

- Change requester
- Change owner
- Implementation technician
- Service owner
- Affected IT teams
- Information Security
- Relevant stakeholders

### Communication Requirements

For approved changes, communicate:

- Approved scope
- Implementation window
- Conditions
- Responsible personnel
- Expected service impact

For rejected or deferred changes, communicate the decision and relevant reasons.

**Expected Result:** Relevant participants understand the authorization outcome.

### Step 19 — Confirm Implementation Readiness

Before implementation, verify:

- Authorization is recorded.
- Conditions have been satisfied.
- Required backups are available.
- Implementation personnel are prepared.
- Validation steps are ready.
- Rollback procedures are available.
- The implementation window is confirmed.
- Relevant stakeholders have been notified.

**Expected Result:** The change is ready for controlled implementation.

### Step 20 — Release the Change for Implementation

When all applicable requirements are satisfied, update the change status.

**Proposed Status:** Authorized / Scheduled

The implementation technician may proceed within the approved scope and conditions.

If material changes occur before implementation, reassessment may be required.

**Expected Result:** The change is formally authorized for implementation.

---

## 12. Standard Change Authorization

Standard changes use preauthorization rather than requiring a new individual approval each time.

### Requirements

A standard change should have:

- A documented change model
- Defined eligibility criteria
- A known implementation procedure
- Established risk controls
- Validation requirements
- Recovery instructions
- An identified preauthorizing authority

### Standard Change Procedure

1. Confirm that an approved standard change model exists.
2. Verify that the proposed activity meets its conditions.
3. Record the change or fulfillment activity as required.
4. Follow the approved procedure.
5. Document implementation and validation.
6. Escalate exceptions for reassessment.

### Example

A routine software deployment may qualify as a standard change when it follows an approved, low-risk, repeatable deployment procedure.

A new application deployment with unknown compatibility risks should not automatically be treated as standard.

---

## 13. Normal Change Authorization

Normal changes require risk-based assessment.

### Low-Risk Normal Change

May require delegated authorization.

### Medium-Risk Normal Change

May require additional technical review and coordination.

### High-Risk Normal Change

May require:

- Formal technical assessment
- Service owner input
- Security review
- Senior IT authorization
- Detailed rollback planning
- Maintenance window coordination

### Example

**Change:** Modify domain-wide password policy.

Potential considerations:

- Organization-wide authentication impact
- Security requirements
- User communication
- Application compatibility
- Policy inheritance
- Recovery requirements

The change should receive authorization appropriate to its actual risk.

---

## 14. Emergency Change Authorization

Emergency changes use an expedited process when delay could create unacceptable business or security consequences.

### Emergency Change Triggers

- Critical service outage
- Active security threat
- Imminent infrastructure failure
- Severe operational disruption
- Urgent correction necessary to restore critical functionality

### Emergency Authorization Procedure

1. Confirm the emergency condition.
2. Document the immediate business or security risk.
3. Identify the minimum necessary change.
4. Evaluate critical implementation risks.
5. Review available recovery options.
6. Contact the designated Emergency Change Authority.
7. Obtain and record authorization.
8. Implement within the approved scope.
9. Validate the result.
10. Complete any required retrospective documentation and review.

### Important Requirements

Emergency changes should not be used merely to bypass normal planning.

Urgency does not eliminate the need for:

- Accountability
- Appropriate authorization
- Risk awareness
- Technical validation
- Documentation

### Example

A critical security vulnerability requires an urgent configuration change to reduce immediate exposure.

The Emergency Change Authority evaluates the proposed action and authorizes an appropriately scoped response.

**Lab Note:** Emergency approval scenarios may be simulated. A fictional approval does not authorize changes to systems outside the learner's control.

---

## 15. Change Advisory Board

A Change Advisory Board may support the evaluation of changes that require multiple perspectives.

### Potential Participants

- Change Coordinator
- Systems Administrator
- Network Administrator
- Cloud Administrator
- Information Security
- Service Owner
- Business Representative

### CAB Responsibilities

A CAB may:

- Review significant technical risks
- Identify conflicting changes
- Evaluate business impact
- Recommend implementation conditions
- Review recovery planning
- Provide advice to the designated Change Authority

### CAB vs. Change Authority

A CAB is not automatically the authorizing body for every change.

The organization must define whether the CAB advises, authorizes, or performs both functions for particular changes.

### Portfolio Consideration

A simulated CAB meeting may be documented as an exercise.

It must not be represented as a real meeting involving independent participants unless that actually occurred.

---

## 16. Conditional Authorization

A change may be approved subject to specific conditions.

### Examples

- Complete a verified backup.
- Obtain security review.
- Confirm affected services.
- Update the implementation plan.
- Perform testing in a lab.
- Schedule a maintenance window.
- Prepare a rollback procedure.
- Notify affected stakeholders.

### Conditional Approval Rule

A change must not proceed until all required conditions have been satisfied.

### Example

```text
Change ID: CHG-001

Decision:
Approved With Conditions

Conditions:
1. Complete DHCP configuration backup.
2. Verify DNS server availability.
3. Confirm affected DHCP scopes.
4. Schedule implementation.
5. Prepare rollback procedure.

Implementation Authorized:
Only After Conditions Are Satisfied
```

---

## 17. Rejected or Deferred Changes

Not every proposed change should be approved.

### Reasons for Rejection

- Unacceptable risk
- Insufficient business justification
- Incomplete implementation planning
- Inadequate rollback capability
- Security concerns
- Unsupported technical assumptions
- Conflicting infrastructure requirements

### Reasons for Deferral

- Additional testing required
- Missing technical information
- Scheduling conflict
- Resource limitations
- Pending dependency
- Required stakeholder unavailable

### Procedure

1. Record the decision.
2. Document the reasons.
3. Notify the requester.
4. Identify required corrective actions.
5. Preserve the Change record.
6. Permit resubmission when appropriate.

A rejected change must not be implemented under the rejected authorization.

---

## 18. Change Reauthorization

Previously authorized changes may require reassessment.

### Reauthorization Triggers

- Significant scope changes
- New affected systems
- Increased business impact
- New security risks
- Major implementation plan revisions
- Changed rollback capability
- Material scheduling changes
- New infrastructure dependencies

### Example

**Originally Approved:** Modify DNS settings on one workstation.

**Revised Scope:** Modify DNS settings across multiple DHCP scopes.

The revised change may affect substantially more systems.

The original authorization should not automatically cover the expanded scope.

### Reauthorization Procedure

1. Document the proposed revision.
2. Identify changed risks.
3. Update affected services and Configuration Items.
4. Revise implementation and rollback plans.
5. Obtain appropriate authorization.
6. Record the new decision.

---

## 19. Authorization Documentation Standards

Authorization records should be:

- Accurate
- Complete
- Traceable
- Consistent
- Chronological
- Appropriate to the change risk

### Required Authorization Fields

| Field | Description |
|---|---|
| Change ID | Unique change identifier |
| Change Type | Standard, Normal, or Emergency |
| Risk Level | Assessed risk |
| Authorization Decision | Recorded outcome |
| Change Authority | Responsible authorizing role |
| Authorization Date | Date of decision |
| Authorization Conditions | Requirements before implementation |
| Approved Scope | Boundaries of the authorized change |
| Approved Window | Permitted implementation period |
| Supporting Reviews | Technical and security assessments |
| Decision Rationale | Reason for the outcome |

### Approval Integrity

Do not fabricate:

- Approval signatures
- Manager identities
- CAB meeting attendance
- Authorization timestamps
- Independent review outcomes

Simulated approvals should be explicitly identified as simulated.

---

## 20. Change Record Storage

Change records are maintained under:

```text
Change-Enablement/
├── README.md
├── Procedures/
│   └── Change-Authorization.md
└── Records/
    ├── CHG-001-Change-Title/
    │   ├── README.md
    │   └── Evidence/
    └── CHG-002-Change-Title/
        ├── README.md
        └── Evidence/
```

### Recommended Evidence

- Change assessment
- Risk analysis
- Impact assessment
- Implementation plan
- Validation plan
- Rollback plan
- Authorization decision
- Relevant technical reviews
- Configuration backups or exports
- Post-change validation results

Use the standardized:

[Change Template](../../Templates/Change-Template.md)

---

## 21. Example Change Authorization Scenario

### Scenario — Correcting DHCP DNS Configuration

**Change ID:** CHG-001  
**Change Type:** Normal  
**Affected Service:** IT-SVC-004 — Network Connectivity  
**Related Problem:** PRB-001  
**Environment:** homelab.local

### Business Context

Employees use domain-joined Windows workstations that depend on internal DNS services for domain controller discovery.

A simulated Problem Management investigation identifies incorrect DNS settings distributed through DHCP.

### Proposed Change

Update the DHCP DNS server options to distribute the approved internal DNS server addresses.

### Proposed DNS Servers

| Server | IP Address |
|---|---|
| DC01 | 10.20.10.10 |
| DC02 | 10.20.10.11 |

These addresses reflect the documented lab design. Their current availability and configuration must be verified before implementation.

### Business Justification

Correcting the DHCP configuration is intended to improve domain controller discovery and reduce recurring authentication failures.

### Preliminary Risk Assessment

**Risk Level:** Medium — Illustrative

Potential risks:

- Incorrect DNS server values
- Client connectivity disruption
- Authentication failures
- DHCP scope misconfiguration
- Incomplete rollback

### Proposed Implementation Plan

1. Review the current DHCP configuration.
2. Export or document existing settings.
3. Verify the approved DNS server addresses.
4. Identify affected DHCP scopes.
5. Apply the authorized configuration.
6. Renew DHCP configuration on an appropriate test workstation.
7. Verify DNS settings.
8. Test domain controller discovery.
9. Confirm domain authentication.

### Proposed Validation

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

```powershell
nslookup dc01.homelab.local
```

```powershell
nltest /dsgetdc:homelab.local
```

### Proposed Rollback

1. Restore the previously documented DHCP DNS options.
2. Verify the restored configuration.
3. Renew client DHCP settings when appropriate.
4. Confirm DNS resolution.
5. Validate domain controller discovery.
6. Document rollback results.

### Simulated Authorization Assessment

| Requirement | Assessment |
|---|---|
| Business Justification | Documented |
| Affected Services | Identified |
| Risk Assessment | Proposed |
| Implementation Plan | Drafted |
| Validation Plan | Drafted |
| Rollback Plan | Drafted |
| Technical Review | Pending |
| Authorization | Pending |

### Proposed Authorization Conditions

- Verify both DNS servers are available.
- Confirm the correct DHCP scopes.
- Complete configuration backup.
- Review the implementation plan.
- Confirm rollback readiness.
- Obtain the required simulated or actual authorization appropriate to the exercise.

### Authorization Status

**Pending — Not Authorized**

### Expected Outcome

The change may proceed after the applicable authorization requirements have been satisfied.

**Scenario Status:** Illustrative authorization exercise. No approval, implementation, or validation is claimed as completed.

---

## 22. Common Change Authorization Errors

### Error 1 — Implementing Before Authorization

**Incorrect:** Making a configuration change before obtaining required approval.

**Correct:** Confirm the applicable authorization before implementation.

### Error 2 — Treating Every Change as Standard

**Incorrect:** Assuming a routine activity is automatically preauthorized.

**Correct:** Verify that an approved standard change model applies.

### Error 3 — Ignoring Business Impact

**Incorrect:** Evaluating only whether the change is technically possible.

**Correct:** Consider affected services, employees, and business operations.

### Error 4 — Missing Rollback Planning

**Incorrect:** Approving a high-risk change without considering recovery.

**Correct:** Review rollback feasibility and recovery requirements.

### Error 5 — Incomplete Risk Assessment

**Incorrect:** Assigning low risk without examining dependencies.

**Correct:** Evaluate technical complexity, impact, security, and recovery.

### Error 6 — Using Emergency Classification to Bypass Review

**Incorrect:** Classifying a poorly planned change as emergency to avoid normal authorization.

**Correct:** Use emergency procedures only when urgency justifies expedited handling.

### Error 7 — Confusing Technical Review With Approval

**Incorrect:** Assuming a technician's recommendation authorizes implementation.

**Correct:** Obtain authorization from the designated Change Authority.

### Error 8 — Exceeding Approved Scope

**Incorrect:** Expanding a workstation change into a domain-wide change without reassessment.

**Correct:** Obtain appropriate reauthorization for material scope changes.

### Error 9 — Ignoring Authorization Conditions

**Incorrect:** Beginning implementation before required backups or reviews are completed.

**Correct:** Verify all approval conditions before proceeding.

### Error 10 — Fabricating Approval Records

**Incorrect:** Recording fictional manager approval as an actual authorization.

**Correct:** Clearly label simulated decisions and self-review activities.

---

## 23. Change Authorization Quality Checklist

Before authorizing a change, verify:

- [ ] Change record exists
- [ ] Unique Change ID assigned
- [ ] Change title and description completed
- [ ] Requester identified
- [ ] Change owner assigned
- [ ] Change type confirmed
- [ ] Business justification documented
- [ ] Affected services identified
- [ ] Affected Configuration Items identified
- [ ] Technical dependencies reviewed
- [ ] Business impact assessed
- [ ] Technical risk assessed
- [ ] Security requirements reviewed
- [ ] Implementation plan documented
- [ ] Required permissions identified
- [ ] Validation plan completed
- [ ] Rollback plan reviewed
- [ ] Backup requirements identified
- [ ] Proposed schedule reviewed
- [ ] Scheduling conflicts evaluated
- [ ] Required technical reviews completed
- [ ] Appropriate Change Authority identified
- [ ] Authorization decision documented
- [ ] Authorization conditions recorded
- [ ] Relevant stakeholders informed
- [ ] Implementation readiness confirmed
- [ ] Approval status accurately represented

---

## 24. Change Authorization Performance Metrics

Change authorization effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Change Authorization Rate | Measures the proportion of submitted changes approved |
| Average Authorization Time | Measures time required to reach an authorization decision |
| Change Rejection Rate | Tracks rejected proposals |
| Change Deferral Rate | Identifies changes awaiting additional information or scheduling |
| Emergency Change Rate | Tracks changes using emergency authorization |
| Unauthorized Change Rate | Identifies changes implemented without required authorization |
| Change Assessment Completeness | Measures required documentation quality |
| Conditional Approval Compliance | Tracks completion of authorization conditions |
| Change Reauthorization Rate | Measures material revisions requiring reassessment |
| Change Success Rate | Evaluates successful implementation outcomes |
| Change-Related Incident Rate | Tracks incidents associated with implemented changes |

Metrics should be calculated using actual records or clearly labeled simulated datasets.

---

## 25. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Communicates relevant changes and identifies employee impact |
| Incident Management | May require authorized changes to restore services |
| Service Request Management | May initiate changes through predefined fulfillment workflows |
| Knowledge Management | Maintains approved implementation and recovery instructions |
| Problem Management | Recommends corrective changes based on investigation findings |
| Change Enablement | Evaluates risk and authorizes appropriate modifications |
| Monitoring and Event Management | Provides service health information and post-change validation |
| Service Configuration Management | Identifies affected Configuration Items and dependencies |
| Information Security Management | Reviews security-sensitive changes |
| Continual Improvement | Evaluates authorization effectiveness and change outcomes |

---

## 26. Related Procedures and Documentation

### Change Enablement

- [Change Enablement Overview](../README.md)
- [Change Template](../../Templates/Change-Template.md)

### Problem Management

- [Problem Management Overview](../../Problem-Management/)
- [Problem Identification](../../Problem-Management/Procedures/Problem-Identification.md)
- [Root Cause Analysis](../../Problem-Management/Procedures/Root-Cause-Analysis.md)
- [Known Error Management](../../Problem-Management/Procedures/Known-Error-Management.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Resolution](../../Incident-Management/Procedures/Incident-Resolution.md)

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Monitoring and Event Management](../../Monitoring-and-Event-Management/)
- [Service Configuration Management](../../Service-Configuration-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

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

## 27. Procedure Review

This procedure should be reviewed when:

- Change authorization responsibilities change.
- Risk assessment requirements are updated.
- New infrastructure technologies are introduced.
- Standard change models are revised.
- Emergency change procedures change.
- Security requirements are modified.
- Change-related incidents increase.
- Authorization documentation issues are identified.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Change Authorization procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee requests, organizational roles, business impact assessments, Change Advisory Board activities, authorization decisions, and approval workflows may be simulated.

Technical implementations, infrastructure modifications, diagnostic commands, validation results, and rollback activities are documented based on hands-on lab work where indicated.

Simulated approvals do not constitute actual authorization to modify systems outside the learner's controlled environment.

GitHub publication does not imply independent technical approval, production deployment, or organizational authorization.

This procedure demonstrates ITIL-aligned Change Enablement, risk-based authorization, technical assessment, change governance, implementation readiness, and operational documentation rather than employment experience within an actual production organization.
