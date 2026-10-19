# SOP — Change Authorization

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Change Enablement  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-CE-001  
**Version:** 1.1  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Change Enablement

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

Routine service requests do not automatically require separate change authorization. The applicable service request or change procedure determines how they are controlled.

A technically feasible change is not necessarily an authorized change.

## 3. Change Types

Technical Techno Tech uses three change types.

### 3.1 Standard Change

A standard change is a low-risk, preauthorized change that is well understood and fully documented.

### Standard Change Requirements

- Documented procedure
- Defined scope
- Known risks
- Established validation
- Appropriate preauthorization
- Consistent execution conditions

**Important:** A change is not automatically standard simply because it is routine. It must meet the organization's preauthorization criteria.

### 3.2 Normal Change

A normal change requires assessment and authorization appropriate to its risk and impact.

Normal changes may require different authorization levels depending on their risk.

### 3.3 Emergency Change

An emergency change must be implemented as soon as possible to address an urgent situation.

Emergency changes follow an expedited assessment and authorization process.

**Important:** Emergency does not mean unauthorized. Emergency changes still require appropriate authorization and documentation, with the process adapted to the urgency.

## 4. Roles and Responsibilities

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

**Lab Note:** These roles represent emulated organizational responsibilities. A single learner may perform multiple roles during a controlled lab exercise. Emulated authorization must not be represented as independent organizational approval.

---

## 5. Change Authorization Principles

### 5.1 Risk-Based Authorization

Authorization requirements should reflect the potential risk and impact of the change.

### 5.2 Appropriate Change Authority

The person or group authorizing a change must have the appropriate responsibility and authority.

### 5.3 Complete Change Documentation

The change must contain sufficient information to support an informed decision.

### 5.4 Business Justification

The expected benefit or necessity of the change should be documented.

### 5.5 Technical Readiness

Implementation, validation, and recovery requirements should be reviewed before approval.

### 5.6 Security Considerations

Changes must preserve applicable security controls and access requirements.

### 5.7 Scheduling Awareness

Authorization should consider service availability, dependencies, and conflicting changes.

### 5.8 Traceability

All authorization decisions should be documented and linked to the relevant Change record.

### 5.9 Separation of Approval and Execution

Where practical, higher-risk changes should receive review from someone other than the implementer.

### 5.10 Controlled Reassessment

Material changes to the approved scope, risk, or implementation plan should trigger reassessment.

---

## 5. Change Authorization Requirements

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

## 6. Change Authorization Decision Matrix

Technical Techno Tech uses a risk-based authorization model.

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

## 7. Change Risk Assessment

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

### Risk Levels

| Risk Level | Description |
|---|---|
| Low | Limited impact, predictable implementation, and straightforward recovery |
| Medium | Moderate service impact or technical uncertainty |
| High | Significant service impact, complex dependencies, or difficult recovery |
| Critical | Potential for severe disruption, significant security exposure, or widespread operational impact |

## 8. Change Authorization Workflow

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

## 9. Change Authorization Procedure

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

### Step 9 — Review the Validation Plan

Determine how successful implementation will be verified.

Validation should address:

- Technical functionality
- Service availability
- Business requirements
- Security requirements
- Configuration accuracy
- Unexpected side effects

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

### Step 14 — Identify the Change Authority

Determine who is authorized to approve the proposed change.

The decision should reflect:

- Change type
- Risk level
- Business impact
- Security requirements
- Technical complexity
- Organizational responsibility

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

## 10. Standard Change Authorization

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

## 11. Normal Change Authorization

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

## 12. Emergency Change Authorization

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

The Emergency Change Authority evaluates the proposed action and authorizes an appropriately scoped response.

**Lab Note:** Emergency approval scenarios may be emulated. A fictional approval does not authorize changes to systems outside the learner's control.

## 13. Change Advisory Board

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

A emulated CAB meeting may be documented as an exercise.

It must not be represented as a real meeting involving independent participants unless that actually occurred.

## 14. Conditional Authorization

A change may be approved subject to specific conditions.

### Conditional Approval Rule

A change must not proceed until all required conditions have been satisfied.

## 15. Rejected or Deferred Changes

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

## 16. Change Reauthorization

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

### Reauthorization Procedure

1. Document the proposed revision.
2. Identify changed risks.
3. Update affected services and Configuration Items.
4. Revise implementation and rollback plans.
5. Obtain appropriate authorization.
6. Record the new decision.

## 17. Authorization Documentation Standards

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

Emulated approvals should be explicitly identified as emulated.

## 18. Change Record Storage

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

## 19. Common Change Authorization Errors

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

**Correct:** Clearly label emulated decisions and self-review activities.

## 20. Change Authorization Quality Checklist

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

## 21. Change Authorization Performance Metrics

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

Metrics should be calculated using actual records or clearly labeled emulated datasets.

## 22. Procedure Review

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
| 1.1 | Remove unneccesary information |
