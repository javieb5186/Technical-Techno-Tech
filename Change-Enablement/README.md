# Technical Techno Tech — Change Enablement

## Overview

Change Enablement is responsible for managing changes to IT services and infrastructure within **Technical Techno Tech (TTT)**, a fictional technology solutions company.

The practice ensures that changes are appropriately assessed, authorized, planned, implemented, and reviewed to minimize unnecessary risks and service disruptions.

Changes may involve Windows Server, Active Directory Domain Services, Group Policy, Microsoft 365, Microsoft Entra ID, Microsoft Intune, Microsoft Azure, network infrastructure, virtualization, and other technologies supporting internal business operations.

Technical Techno Tech applies ITIL-aligned Change Enablement principles through emulated business requirements, technical risk assessments, hands-on infrastructure changes, implementation planning, rollback procedures, and validation.

## Purpose

The purpose of Change Enablement is to maximize the number of successful service and product changes by ensuring that risks have been properly assessed, authorizing changes to proceed, and managing the change schedule.

Primary objectives include:

- Evaluate proposed changes to IT services and infrastructure.
- Identify potential business and technical impacts.
- Assess implementation risks.
- Ensure appropriate change authorization.
- Establish clear implementation procedures.
- Coordinate changes affecting multiple systems or services.
- Reduce unnecessary service disruptions.
- Establish backup and rollback procedures.
- Validate successful change implementation.
- Maintain accurate change records.
- Support configuration documentation updates.
- Review change outcomes and identify improvements.

**Key Principle:** Change Enablement is not intended to prevent changes. It enables necessary changes to be implemented successfully while managing risk.

## Scope of Change Enablement

### In Scope

Change Enablement may apply to activities including:

- Windows Server configuration changes
- Active Directory infrastructure modifications
- Domain controller deployment or replacement
- Group Policy changes
- DNS and DHCP configuration changes
- Network routing and switching modifications
- Firewall rule changes
- Microsoft Entra ID configuration changes
- Microsoft Intune policy deployments
- Microsoft 365 administrative configuration changes
- Microsoft Azure infrastructure changes
- Virtual machine infrastructure modifications
- Server role installations
- Security configuration changes
- Software upgrades affecting shared services
- Infrastructure migrations

The required level of assessment and authorization depends on the change type, risk, and organizational procedures.

### Out of Scope

Activities that do not require separate Change Enablement handling may include:

- Routine troubleshooting without configuration changes
- Standard user support interactions
- General information requests
- Routine monitoring
- Read-only administrative investigations
- Predefined service request activities managed through established procedures

Some routine configuration activities may be managed as preauthorized standard changes.

Not every technical action requires a separate change record.

### Important Definitions

**Change:** The addition, modification, or removal of anything that could have a direct or indirect effect on services.

**Change Authorization:** The decision permitting a proposed change to proceed under defined conditions.

**Change Implementation:** The controlled execution of an authorized modification.

**Change Schedule:** Information used to plan changes and identify potential conflicts.

**Rollback / Backout:** Actions taken to return to an acceptable previous state when implementation fails.

**Post-Implementation Review (PIR):** An evaluation of the change's outcome, including its effectiveness, impact, and lessons learned.
A **change** is the addition, modification, or removal of anything that could have a direct or indirect effect on services.

## Change Types

Technical Techno Tech recognizes three primary change types.

### 1. Standard Change

A standard change is a low-risk, preauthorized change that is well understood and follows an established procedure.

Characteristics include:

- Low risk
- Repeatable implementation
- Documented procedure
- Established authorization
- Predictable outcomes
- Appropriate validation

Standard changes do not require individual authorization each time when they remain within their approved scope.

### 2. Normal Change

A normal change requires assessment and authorization before implementation.

Characteristics include:

- Risk assessment
- Impact analysis
- Appropriate authorization
- Implementation planning
- Validation requirements
- Rollback planning when applicable

Normal changes may be low, medium, or high risk.

### 3. Emergency Change

An emergency change requires expedited assessment and authorization because delaying implementation could result in significant business harm.

Characteristics include:

- Urgent business or technical need
- Expedited assessment
- Appropriate emergency authorization
- Focused implementation planning
- Necessary risk controls
- Post-implementation review

Emergency changes are not automatically exempt from authorization or documentation requirements.

## Change Classification Summary

| Change Type | Risk Profile | Authorization |
|---|---|---|
| Standard | Low and well understood | Preauthorized |
| Normal | Varies by change | Appropriate change authority |
| Emergency | Urgent; risk varies | Expedited authorization |

The change type determines the appropriate workflow rather than the technical complexity alone.

## Change Enablement Responsibilities

### Change Requester

The change requester identifies the business or technical need for a change.

Responsibilities include:

- Describing the proposed change
- Providing business justification
- Identifying expected benefits
- Identifying affected services
- Providing relevant supporting information

### Change Owner

The change owner coordinates the change throughout its lifecycle.

Responsibilities include:

- Maintaining the change record
- Coordinating risk assessment
- Identifying required authorization
- Preparing implementation plans
- Coordinating affected personnel
- Tracking change status
- Documenting implementation results
- Coordinating post-implementation review

### Change Implementer

The change implementer performs the authorized technical activities.

Responsibilities include:

- Reviewing the approved implementation plan
- Confirming prerequisites
- Preparing backup or recovery options
- Executing implementation steps
- Recording technical results
- Performing validation
- Executing rollback when required

### Change Authority

The change authority is the person or group authorized to approve a particular change.

The appropriate authority depends on:

- Change type
- Business impact
- Technical risk
- Security implications
- Affected services
- Organizational policy

A Change Advisory Board (CAB) may assist with assessing selected changes, but it is not required for every change.

### Service Desk

The Service Desk may support Change Enablement by:

- Communicating planned service interruptions
- Informing affected employees
- Receiving reports of post-change issues
- Linking incidents to recent changes
- Providing feedback about user impact

**Note:** These responsibilities represent emulated IT roles within the lab environment and do not imply that separate employees or teams are operating the environment.

## Change Enablement Lifecycle

Technical Techno Tech follows a structured change management workflow.

### 1. Change Identification

A need for change is identified.

Potential sources include:

- Business requirements
- Service improvement initiatives
- Problem investigations
- Incident resolution activities
- Security requirements
- Infrastructure expansion
- Technology upgrades
- Configuration reviews

### 2. Change Logging

A change record is created.

Information may include:

- Change ID
- Change title
- Requester
- Change owner
- Change type
- Business justification
- Affected services
- Affected Configuration Items
- Proposed implementation date
- Expected outcomes

### 3. Change Assessment

The proposed change is evaluated for:

- Business impact
- Technical risk
- Security implications
- Service availability
- Infrastructure dependencies
- Required resources
- Implementation complexity
- Potential failure scenarios
- Recovery requirements

### 4. Change Authorization

The change is reviewed by the appropriate change authority.

Possible outcomes include:

- Approved
- Rejected
- Deferred
- Additional Information Required

Authorization requirements depend on the change type and organizational procedures.

### 5. Change Planning

The implementation plan identifies:

- Prerequisites
- Required tools
- Required permissions
- Affected systems
- Implementation steps
- Expected results
- Maintenance window, if applicable
- Communication requirements
- Backup procedures
- Rollback procedures
- Validation steps

### 6. Change Scheduling

The change is scheduled according to business and technical requirements.

Considerations include:

- Employee availability
- Business operating hours
- Service dependencies
- Planned maintenance windows
- Conflicting changes
- Required technical resources
- Potential service interruptions

Not every change requires a dedicated maintenance window.

### 7. Change Implementation

The authorized change is implemented according to the approved plan.

Activities should be documented chronologically.

Implementation records may include:

- Commands executed
- Configuration settings modified
- Systems affected
- Screenshots
- Diagnostic outputs
- Unexpected behavior
- Deviations from the plan
- Corrective actions

### 8. Change Validation

The implementer verifies that the change achieved its intended outcome.

Validation may include:

- Service availability checks
- Authentication testing
- Network connectivity tests
- Group Policy verification
- Application functionality
- Security configuration verification
- System health checks
- Employee acceptance, when appropriate

### 9. Post-Implementation Review

The change outcome is evaluated.

Questions may include:

- Was the intended objective achieved?
- Was implementation completed as planned?
- Were unexpected issues encountered?
- Were services disrupted?
- Was rollback required?
- Were risks accurately assessed?
- Is additional work required?
- What improvements can be made?

### 10. Change Closure

The change record is closed after applicable implementation, validation, review, and documentation requirements are satisfied.

The final record should identify:

- Implementation outcome
- Validation results
- Rollback status
- Remaining issues
- Related incidents or problems
- Updated configuration documentation
- Lessons learned

## Change Risk Assessment

Risk assessment helps determine how a proposed change may affect IT services.

### Risk Factors

Potential factors include:

- Number of affected users
- Importance of affected services
- Complexity of implementation
- Security implications
- Infrastructure dependencies
- Probability of failure
- Recovery difficulty
- Availability of tested rollback procedures
- Expected downtime

### Risk Matrix

| Impact / Likelihood | High Likelihood | Medium Likelihood | Low Likelihood |
|---|---|---|---|
| High Impact | High Risk | High Risk | Medium Risk |
| Medium Impact | High Risk | Medium Risk | Low Risk |
| Low Impact | Medium Risk | Low Risk | Low Risk |

### Risk Levels

| Risk Level | Description |
|---|---|
| Low | Limited impact with predictable implementation and recovery |
| Medium | Moderate potential disruption requiring additional planning |
| High | Significant potential business impact or difficult recovery |

Risk level helps determine the necessary assessment and authorization, but it does not automatically determine whether a change is standard, normal, or emergency.

## Change Impact Assessment

Impact assessment identifies the services and users that may be affected by a change.

### Assessment Questions

1. Which IT services will be affected?
2. Which employees or departments depend on those services?
3. Which servers, endpoints, or network devices are involved?
4. Could the change interrupt authentication or connectivity?
5. Are other systems dependent on the affected components?
6. Could the change affect security or compliance requirements?
7. What is the expected downtime?
8. What happens if implementation fails?
9. How will normal service be restored?

## Change Authorization

Authorization ensures that changes are reviewed by the appropriate authority before implementation.

### Authorization Principles

- Standard changes may be preauthorized.
- Normal changes require appropriate assessment and authorization.
- Emergency changes use expedited authorization.
- Authorization should match the change's risk and business impact.
- Technical personnel should not exceed their assigned authority.
- Approval decisions should be documented when required.

### Authorization Documentation

Change records should identify:

- Change authority
- Authorization status
- Approval date, when applicable
- Conditions or restrictions
- Relevant risk considerations

### Emulated Authorization

Within the Technical Techno Tech lab, business approvals and change authorities may be emulated.

Emulated approvals must be clearly identified and must not be presented as actual production authorizations.

## Change Scheduling & Communication

Changes should be coordinated to minimize unnecessary disruption.

### Scheduling Considerations

- Business operating hours
- Maintenance windows
- Service dependencies
- Availability of technical personnel
- Conflicting changes
- Expected implementation duration
- Recovery time

### Communication Requirements

Affected stakeholders may need information about:

- Purpose of the change
- Scheduled implementation
- Expected service impact
- Potential downtime
- Available alternatives
- Completion status
- Unexpected issues

### Service Desk Coordination

The Service Desk may communicate planned changes to employees and receive reports of unexpected post-change issues.

## Implementation Planning

Each applicable change should have a clear implementation plan.

### Implementation Checklist

- [ ] Business justification documented
- [ ] Affected services identified
- [ ] Configuration Items identified
- [ ] Technical dependencies reviewed
- [ ] Risk assessment completed
- [ ] Authorization confirmed
- [ ] Prerequisites verified
- [ ] Backup or recovery method prepared
- [ ] Implementation steps documented
- [ ] Validation steps defined
- [ ] Rollback criteria established
- [ ] Communication requirements identified

The depth of planning should be proportional to the change's risk and complexity.

## Backup & Rollback Planning

Rollback planning helps restore the previous service state when implementation produces unacceptable results.

### Rollback Considerations

- What configuration is being modified?
- Can the previous configuration be restored?
- Is a backup or export required?
- Are virtual machine snapshots appropriate?
- What dependencies could prevent recovery?
- How long would restoration take?
- What conditions should trigger rollback?
- How will recovery be validated?

**Important:** Virtual machine snapshots are not substitutes for supported backup procedures. Domain controllers and other stateful systems require special consideration when planning recovery.

### Rollback Validation

After rollback, verify that:

- Previous configuration has been restored.
- Affected services are operational.
- Authentication and connectivity function as expected.
- No additional service disruption remains.
- The change record reflects the actual outcome.

## Change Validation

Successful implementation does not automatically mean the change was successful.

The intended business and technical outcomes must be verified.

### Validation Methods

Potential validation methods include:

- PowerShell verification commands
- Windows Event Viewer
- Active Directory diagnostic utilities
- DNS resolution testing
- Network connectivity testing
- Group Policy result verification
- Microsoft 365 administrative checks
- Microsoft Intune deployment status
- Application functionality testing

### Validation Record

| Validation Item | Expected Result | Status |
|---|---|---|
| Configuration Applied | Intended settings are present | Pass / Fail |
| Service Availability | Required services remain operational | Pass / Fail |
| Functional Testing | Intended functionality works correctly | Pass / Fail |
| Security Verification | Required controls remain effective | Pass / Fail |
| Business Outcome | Change objective is achieved | Pass / Fail |

Actual validation results should be documented within the individual change record.

## Emergency Change Management

Emergency changes require an expedited workflow when delaying implementation presents significant risk.

### Emergency Change Workflow

1. Identify the urgent business or technical requirement.
2. Assess the immediate impact and risk.
3. Identify the appropriate emergency change authority.
4. Obtain expedited authorization.
5. Prepare a focused implementation and recovery plan.
6. Implement the authorized correction.
7. Verify service restoration or risk reduction.
8. Document implementation results.
9. Conduct a post-implementation review.

### Emergency Change Documentation

Emergency changes should document:

- Reason for urgency
- Affected services
- Risks of delaying the change
- Authorization
- Implementation actions
- Validation results
- Unexpected issues
- Recovery actions
- Post-implementation findings

Emergency classification should not be used merely to avoid normal change controls.

## Change Status Definitions

| Status | Description |
|---|---|
| Proposed | Change has been identified and recorded |
| Under Assessment | Impact, risk, and requirements are being evaluated |
| Awaiting Authorization | Change requires an approval decision |
| Approved | Change is authorized for implementation |
| Scheduled | Implementation has been planned |
| In Progress | Change implementation is underway |
| Validation | Implementation is complete and results are being verified |
| Completed | Change achieved its intended outcome |
| Failed | Change did not achieve its intended outcome |
| Rolled Back | Previous configuration or service state was restored |
| Closed | Required review and documentation are complete |
| Rejected | Change was not authorized |
| Cancelled | Change will not proceed |

A completed change may still require documentation review before closure.

## Supported Technologies

Change Enablement activities may involve the following technologies.

### Windows & Active Directory

- Windows Server
- Active Directory Domain Services
- Group Policy
- DNS and DHCP
- PowerShell
- Windows Admin Center

### Microsoft Cloud Services

- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure

### Networking

- OPNsense
- VyOS
- Routing and Switching
- Firewall Configuration
- Network Segmentation

### Virtualization

- Hyper-V
- Virtual Machines
- Virtual Networking

### IT Service Management

- Jira Service Management
- GitHub Documentation

Technologies are included in individual change records according to their actual use.

## Change Enablement Procedures

The `Procedures/` directory contains repeatable operational instructions.

| Procedure | Purpose | Status |
|---|---|---|
| Change Submission | Defines how proposed changes are recorded | Planned |
| Change Classification | Defines standard, normal, and emergency change criteria | Planned |
| Change Risk Assessment | Defines technical and business risk evaluation | Planned |
| Change Authorization | Defines approval requirements and responsibilities | Planned |
| Change Implementation | Defines implementation and evidence requirements | Planned |
| Change Rollback | Defines recovery and rollback expectations | Planned |
| Change Validation | Defines post-implementation verification | Planned |
| Change Closure | Defines review and documentation requirements | Planned |

Procedures will be developed and refined as the emulated environment evolves.

## Change Records

The `Records/` directory contains individual infrastructure and service changes.

Each record should document:

- Change identification
- Business justification
- Change classification
- Affected services
- Affected Configuration Items
- Risk assessment
- Impact analysis
- Authorization
- Implementation plan
- Backup and rollback procedures
- Implementation activities
- Technical evidence
- Validation results
- Post-implementation review
- Related records
- Lessons learned
- Final change status

### Directory Structure

```text
Change-Enablement/
├── README.md
├── Procedures/
└── Records/
    └── CHG-001-Change-Title/
        ├── README.md
        └── Evidence/
```

Each change record follows the standardized [Change Template](../Templates/Change-Template.md).

### Change Register

| Change ID | Change Title | Change Type | Risk | Status |
|---|---|---|---|---|
| CHG-XXX | [Change Title] | [Standard / Normal / Emergency] | [Low / Medium / High] | [Status] |

Add changes to this register as they are documented. Remove placeholder entries until actual records exist.

## Integration With Incident Management

Incidents may require changes to restore normal service.

An urgent correction may qualify for an emergency change if the defined criteria are met.

**Reference:** [Incident Management](../Incident-Management/)

## Integration With Problem Management

Problem investigations may identify permanent corrective actions requiring changes.

Problem Management may continue monitoring for recurrence after the change is completed.

**Reference:** [Problem Management](../Problem-Management/)

## Integration With Service Request Management

Some service requests require changes to infrastructure or service configurations.

If the request can be fulfilled using an established, authorized procedure, a separate change record may not be necessary.

If fulfillment requires a new shared infrastructure configuration with broader service impact, Change Enablement may be required.

**Reference:** [Service Request Management](../Service-Request-Management/)

## Integration With Service Configuration Management

Changes may create, modify, or retire Configuration Items.

Relevant Configuration Item records should be updated after successful implementation.

**Reference:** [Service Configuration Management](../Service-Configuration-Management/)

## Integration With Knowledge Management

Infrastructure changes may require updates to technical documentation.

Knowledge articles should reflect the current supported environment.

**Reference:** [Knowledge Management](../Knowledge-Management/)

## Integration With Information Security Management

Changes should be evaluated for potential security impacts.

Security considerations may include:

- Privileged access
- Authentication requirements
- Firewall rules
- Network segmentation
- Encryption
- Endpoint protection
- Identity and access policies
- Security logging
- Compliance requirements

High-risk security changes may require additional review or authorization.

**Reference:** [Information Security Management](../Information-Security-Management/)

## Change Enablement Performance Metrics

Change Enablement effectiveness may be evaluated using operational metrics.

| Metric | Purpose |
|---|---|
| Change Volume | Tracks the number of implemented changes |
| Change Success Rate | Measures changes achieving intended outcomes |
| Failed Change Rate | Tracks unsuccessful changes |
| Change-Related Incident Count | Identifies incidents associated with changes |
| Emergency Change Rate | Measures the proportion of emergency changes |
| Rollback Rate | Tracks changes requiring recovery actions |
| Average Change Lead Time | Measures time from submission to implementation |
| Post-Implementation Review Completion | Tracks required review activities |

Metrics will be introduced when sufficient change data becomes available.

Findings may support improvement initiatives under [Continual Improvement](../Continual-Improvement/).

## Continual Improvement

Change Enablement contributes to continual improvement by evaluating implementation outcomes and identifying opportunities to reduce risk.

Potential improvements include:

- Standardizing repeatable low-risk changes
- Improving risk assessment accuracy
- Reducing failed changes
- Strengthening rollback procedures
- Improving change scheduling
- Automating appropriate standard changes
- Improving stakeholder communication
- Identifying recurring implementation issues
- Improving change documentation
- Strengthening validation procedures

Improvements should be based on actual change results, observed risks, and documented lessons learned.

## Documentation Standards

Change records should:

1. Clearly describe the proposed modification.
2. Explain the business or technical justification.
3. Identify affected services and Configuration Items.
4. Document the change type.
5. Assess potential risks and business impacts.
6. Record applicable authorization.
7. Include a clear implementation plan.
8. Document backup and rollback procedures when appropriate.
9. Record technical implementation activities accurately.
10. Include commands, configurations, and supporting evidence.
11. Verify the intended outcome.
12. Document unexpected issues and recovery actions.
13. Record post-implementation findings.
14. Update related infrastructure and knowledge documentation.
15. Protect sensitive information.
16. Distinguish emulated authorization from actual lab implementation.
