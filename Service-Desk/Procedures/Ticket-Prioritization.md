# SOP — Ticket Prioritization

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Service Desk  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-SD-003  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practices:** Service Desk, Incident Management, Service Request Management

---

## 1. Purpose

This procedure establishes a standardized process for evaluating and assigning priorities to IT support tickets within Technical Techno Tech.

Ticket prioritization helps ensure that IT personnel address issues according to their business impact, urgency, and operational importance.

The procedure supports:

- Consistent ticket prioritization
- Appropriate allocation of IT resources
- Faster response to critical service disruptions
- Reduced business impact
- Effective escalation
- Clear communication with employees
- Improved ticket management
- Accurate service performance reporting

**Key Principle:** Ticket priority should reflect business impact and urgency rather than the order in which requests are received or the job title of the requester.

---

## 2. Scope

This procedure applies to incoming and existing IT support tickets managed by Technical Techno Tech's internal Service Desk.

### Applicable Ticket Types

- Incidents
- Service requests
- Security-related tickets
- Infrastructure-related support tickets

Problem records, change records, and other ITSM work items may use separate prioritization criteria appropriate to their management practices.

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

---

## 3. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Reviewing ticket information
- Assessing business impact
- Assessing urgency
- Assigning initial priority
- Documenting priority justification
- Identifying potential critical incidents
- Escalating tickets when necessary
- Updating priority when circumstances change

### Technical Support Specialist

Responsible for:

- Reviewing assigned ticket priority
- Confirming technical and operational impact
- Reporting changes in service conditions
- Requesting priority adjustments when appropriate
- Escalating significant issues

### IT Administrator

Responsible for:

- Assessing infrastructure-related impact
- Supporting prioritization of complex technical incidents
- Identifying critical service dependencies
- Coordinating technical escalation
- Providing additional impact information

### Service Desk Coordinator

Responsible for:

- Reviewing prioritization consistency
- Coordinating critical ticket handling
- Resolving priority disputes
- Monitoring high-priority tickets
- Reviewing prioritization trends

### Requester

Responsible for:

- Explaining how the issue affects their work
- Identifying relevant business deadlines
- Reporting changes in impact
- Providing information about available workarounds

**Lab Note:** These roles are simulated. A single learner may perform multiple roles during an exercise.

---

## 4. Ticket Priority Fundamentals

Ticket priority determines the relative importance of a ticket and how quickly it should receive attention.

Technical Techno Tech primarily evaluates incident priority using two factors:

1. **Impact**
2. **Urgency**

### Impact

Impact measures the extent of the business disruption.

**Question:** How much of the organization or its operations is affected?

### Urgency

Urgency measures how quickly action is required to avoid or reduce negative consequences.

**Question:** How quickly does this issue need attention?

### Priority

Priority represents the relative importance assigned to the ticket based on the assessed impact and urgency.

**Formula:**

```text
Impact + Urgency = Priority
```

This is a conceptual relationship, not a mathematical calculation.

---

## 5. Impact Assessment

Impact measures how significantly an incident affects employees, services, and business operations.

### Impact Levels

| Impact | Classification | Description |
|---|---|---|
| High | Organization-Wide / Critical | Critical business operations or services are significantly disrupted |
| Medium | Departmental / Multiple Users | A department or multiple employees experience meaningful disruption |
| Low | Individual / Limited | A single employee or limited function is affected |

### High Impact

Examples:

- Organization-wide authentication failure
- Critical network infrastructure unavailable
- Multiple departments unable to access essential systems
- Major infrastructure outage
- Critical business service unavailable

### Medium Impact

Examples:

- Departmental shared folder unavailable
- Several employees unable to access an application
- Network connectivity failure affecting one department
- A business service operating with significant limitations

### Low Impact

Examples:

- Individual employee cannot access a noncritical application
- Single workstation experiencing a limited issue
- Minor software malfunction
- Individual peripheral device failure

### Impact Assessment Questions

1. How many employees are affected?
2. Which departments are affected?
3. Is a critical business service unavailable?
4. Are business operations significantly disrupted?
5. Is there an available workaround?
6. Are other systems dependent on the affected service?

**Important:** The number of affected users is not the only measure of impact. A single-user issue may have high business impact if it prevents a critical operation.

---

## 6. Urgency Assessment

Urgency measures how quickly the issue requires attention.

### Urgency Levels

| Urgency | Classification | Description |
|---|---|---|
| High | Immediate | Immediate action is required to prevent or reduce significant consequences |
| Medium | Prompt | Timely action is needed, but immediate intervention is not essential |
| Low | Routine | Work can follow normal scheduling |

### High Urgency

Examples:

- Critical service outage
- Imminent business deadline with no workaround
- Rapidly worsening infrastructure failure
- Security concern requiring immediate escalation
- Significant operational disruption

### Medium Urgency

Examples:

- Departmental application issue
- Limited service degradation
- Business task delayed but not completely blocked
- Temporary workaround available

### Low Urgency

Examples:

- Minor inconvenience
- Noncritical application issue
- Work can continue using another method
- Routine issue without a significant deadline

### Urgency Assessment Questions

1. How quickly must service be restored?
2. Is there an immediate business deadline?
3. Is the issue becoming worse?
4. Is an acceptable workaround available?
5. What happens if the issue remains unresolved?
6. Does the issue present an immediate security or operational risk?

---

## 7. Priority Matrix

Technical Techno Tech uses a proposed four-level priority model.

### Impact and Urgency Matrix

| Impact / Urgency | High Urgency | Medium Urgency | Low Urgency |
|---|---|---|---|
| High Impact | P1 — Critical | P2 — High | P3 — Medium |
| Medium Impact | P2 — High | P3 — Medium | P4 — Low |
| Low Impact | P3 — Medium | P4 — Low | P4 — Low |

This matrix represents an internal lab policy rather than a universal ITIL requirement.

### Priority Definitions

| Priority | Classification | General Handling |
|---|---|---|
| P1 | Critical | Immediate coordination and escalation |
| P2 | High | Expedited attention |
| P3 | Medium | Standard support handling |
| P4 | Low | Routine scheduling |

Priority assignments should be reviewed when new information changes the impact or urgency assessment.

---

## 8. Priority Level Definitions

### P1 — Critical

A P1 incident represents a critical business disruption requiring immediate coordination.

#### Examples

- Organization-wide authentication outage
- Critical network failure affecting business operations
- Major infrastructure outage
- Complete loss of an essential business service

#### Required Actions

1. Confirm the reported impact.
2. Assign P1 priority.
3. Notify the appropriate escalation contact.
4. Coordinate technical response.
5. Record actions and findings.
6. Provide updates according to the applicable communication plan.
7. Review whether major incident procedures should be activated.

**Note:** A P1 incident may qualify as a major incident, but major incident designation should follow the organization's defined criteria.

---

### P2 — High

A P2 incident represents a significant disruption requiring expedited attention.

#### Examples

- Department-wide network outage
- Multiple employees unable to authenticate
- Critical application degraded
- Important business function significantly affected

#### Required Actions

1. Confirm impact and urgency.
2. Assign P2 priority.
3. Route to the appropriate support function.
4. Begin timely investigation.
5. Escalate when necessary.
6. Maintain appropriate requester communication.

---

### P3 — Medium

A P3 incident represents a standard operational issue requiring normal support handling.

#### Examples

- Individual employee unable to access an important application
- Limited network connectivity issue
- Workstation software failure
- Service degradation with manageable impact

#### Required Actions

1. Assign P3 priority.
2. Route according to technical category.
3. Perform troubleshooting.
4. Document findings.
5. Update the requester.
6. Escalate if the issue becomes more significant.

---

### P4 — Low

A P4 incident represents a limited-impact issue that can be handled through routine support scheduling.

#### Examples

- Minor application inconvenience
- Noncritical peripheral issue
- Cosmetic software issue
- Limited issue with an acceptable workaround

#### Required Actions

1. Assign P4 priority.
2. Route to the appropriate support function.
3. Schedule work according to operational availability.
4. Document progress.
5. Update the requester when appropriate.

---

## 9. Ticket Prioritization Procedure

### Step 1 — Review the Ticket

Open the ticket and review:

- Requester information
- Ticket summary
- Description
- Ticket type
- Affected service
- Technical category
- Affected employees
- Business impact
- Relevant deadlines
- Available workarounds

**Expected Result:** Sufficient information is available to begin priority assessment.

### Step 2 — Confirm Ticket Classification

Verify whether the ticket is an incident, service request, or other work type.

Incident priority normally follows the impact and urgency matrix.

Service requests may follow separate fulfillment priorities and target dates.

**Expected Result:** The correct prioritization approach is selected.

### Step 3 — Determine Business Impact

Assess the extent of disruption.

Consider:

- Number of affected users
- Business criticality
- Departmental impact
- Service availability
- Operational consequences
- Infrastructure dependencies

Select:

- High
- Medium
- Low

**Expected Result:** Impact is documented.

### Step 4 — Determine Urgency

Assess how quickly action is required.

Consider:

- Time sensitivity
- Business deadlines
- Availability of workarounds
- Potential escalation of the issue
- Security implications

Select:

- High
- Medium
- Low

**Expected Result:** Urgency is documented.

### Step 5 — Assign Priority

Use the approved priority matrix to determine the ticket's priority.

**Example:**

```text
Impact: Medium
Urgency: High

Assigned Priority: P2 — High
```

**Expected Result:** Ticket priority is assigned consistently.

### Step 6 — Document Priority Justification

Record the reason for the priority assignment.

#### Example

**Priority:** P2 — High

**Justification:** Multiple employees in the Sales department cannot access a required business application. The issue is preventing scheduled work, and no acceptable workaround is available.

Avoid vague explanations such as:

- "Very important"
- "User is upset"
- "Needs fixing ASAP"

Priority justification should describe measurable or observable business consequences.

**Expected Result:** The priority decision is supported by documented evidence.

### Step 7 — Determine Escalation Requirements

Review whether the ticket requires immediate escalation.

Escalation may be necessary when:

- Priority is P1.
- A significant outage is identified.
- Security concerns require specialized handling.
- Required permissions exceed Service Desk authority.
- Critical infrastructure is affected.
- Technical expertise is unavailable.

**Expected Result:** Required escalation is initiated.

### Step 8 — Update the Ticket

Record:

- Impact
- Urgency
- Priority
- Priority justification
- Assigned technician or group
- Escalation details
- Next action

**Expected Result:** The ticket accurately reflects the prioritization decision.

### Step 9 — Communicate With the Requester

Provide an appropriate update.

Communication may include:

- Ticket acknowledgment
- Current priority
- General next steps
- Escalation status
- Requests for additional information

Do not promise a resolution time unless an applicable service target supports that commitment.

**Expected Result:** The requester understands the ticket's current handling status.

### Step 10 — Reassess When Necessary

Reevaluate the priority when circumstances change.

Examples include:

- More employees become affected.
- A workaround becomes unavailable.
- A critical deadline approaches.
- The affected service is restored.
- New security information becomes available.

**Expected Result:** Priority remains aligned with current business impact and urgency.

---

## 10. Service Request Prioritization

Service requests differ from incidents because they generally involve planned or predefined service fulfillment rather than unexpected service disruption.

### Service Request Considerations

Prioritization may depend on:

- Request type
- Business deadline
- Employee start date
- Required approvals
- Fulfillment complexity
- Resource availability
- Service targets

### Example

**Request:** Provision a workstation for a new employee.

The request may be scheduled according to the employee's start date and the organization's onboarding requirements.

A routine service request should not automatically receive P1 priority because the requester asks for immediate completion.

### Proposed Service Request Priority Guidelines

| Priority | General Criteria |
|---|---|
| P1 | Exceptional, formally authorized urgent business requirement |
| P2 | Time-sensitive approved request with significant business impact |
| P3 | Standard request requiring normal fulfillment |
| P4 | Low-urgency request that can follow routine scheduling |

Service request fulfillment targets should be defined separately from incident restoration targets.

---

## 11. Security-Related Prioritization

Security-related tickets require special consideration.

Examples include:

- Suspected account compromise
- Malware detection
- Unauthorized administrative access
- Suspicious authentication activity
- Lost or stolen company equipment

### Security Assessment Factors

- Potential data exposure
- Privileged account involvement
- Number of affected systems
- Likelihood of ongoing compromise
- Potential business impact
- Required containment urgency

### Important Distinction

A security concern may require immediate security escalation even when the normal incident priority matrix produces a lower priority.

Security escalation and ticket priority are related but separate decisions.

Security incidents should follow applicable Information Security Management and incident response procedures.

---

## 12. Priority Escalation

Priority escalation occurs when the ticket's significance increases or specialized coordination becomes necessary.

### Escalation Triggers

- Organization-wide service disruption
- Increased number of affected users
- Loss of critical business functionality
- Unavailable workarounds
- Significant security risk
- Approaching critical business deadlines
- Failure to meet applicable response requirements

### Escalation Procedure

1. Review updated information.
2. Reassess impact.
3. Reassess urgency.
4. Determine whether priority should change.
5. Document the justification.
6. Notify the appropriate support function.
7. Update the requester when appropriate.

### Example

**Initial Condition:**

One employee cannot access a shared application.

- Impact: Low
- Urgency: Medium
- Priority: P4

**Updated Condition:**

The entire department loses access, and an immediate business deadline is affected.

- Impact: Medium
- Urgency: High
- Priority: P2

**Action:** Increase priority to P2 and coordinate expedited investigation.

---

## 13. Priority Downgrading

Priority may be reduced when business impact or urgency decreases.

### Examples

- A reliable workaround becomes available.
- The affected service is partially restored.
- Fewer employees remain affected.
- A critical deadline is no longer at risk.

### Downgrading Procedure

1. Confirm the change in circumstances.
2. Reassess impact and urgency.
3. Assign the updated priority.
4. Document the reason.
5. Notify relevant personnel.
6. Continue appropriate ticket handling.

Priority should not be reduced simply to improve performance reports or avoid escalation requirements.

---

## 14. Prioritization vs. Assignment

Priority and assignment serve different purposes.

### Priority

Determines how urgently the ticket should be addressed relative to other work.

### Assignment

Determines which technician or support group is responsible for the ticket.

### Example

**Ticket:** Domain controller replication failure.

**Priority:** Determined by actual business impact and urgency.

**Assignment:** Systems Administration.

A technically complex ticket is not automatically high priority.

Similarly, a simple issue may require immediate attention if its business consequences are significant.

---

## 15. Example Prioritization Scenarios

### Scenario 1 — Organization-Wide Authentication Failure

**Description:** Employees across the organization cannot authenticate to the domain.

**Impact:** High  
**Urgency:** High  
**Priority:** P1 — Critical

**Justification:** Critical authentication services are unavailable to the organization.

**Action:** Immediate escalation and coordinated incident response.

---

### Scenario 2 — Departmental Network Outage

**Description:** The HR department cannot access internal network resources.

**Impact:** Medium  
**Urgency:** High  
**Priority:** P2 — High

**Justification:** Multiple employees are unable to perform time-sensitive business activities.

**Action:** Expedited troubleshooting and network administration escalation.

---

### Scenario 3 — Individual Application Failure

**Description:** One employee cannot open a required application.

**Impact:** Low  
**Urgency:** High  
**Priority:** P3 — Medium

**Justification:** The issue affects one employee but prevents an immediate required task.

**Action:** Standard support handling with attention to the time-sensitive requirement.

---

### Scenario 4 — Minor Peripheral Issue

**Description:** One employee's secondary monitor intermittently disconnects, but work can continue.

**Impact:** Low  
**Urgency:** Low  
**Priority:** P4 — Low

**Justification:** Limited operational impact with an acceptable workaround.

**Action:** Routine troubleshooting and scheduling.

---

### Scenario 5 — New Employee Onboarding

**Description:** HR requests account and workstation provisioning for a new employee starting next week.

**Ticket Type:** Service Request

**Priority:** P3 — Medium, under the proposed request guidelines

**Justification:** Standard onboarding activity with a defined fulfillment deadline.

**Action:** Verify authorization and schedule fulfillment before the employee's start date.

---

## 16. Common Prioritization Errors

### Error 1 — Prioritizing Based on Job Title

**Incorrect:** Automatically assigning P1 because the requester is an executive.

**Correct:** Evaluate the actual business impact and urgency.

### Error 2 — Prioritizing Based on User Frustration

**Incorrect:** Increasing priority because the requester is upset.

**Correct:** Acknowledge the concern while applying consistent priority criteria.

### Error 3 — Confusing Technical Complexity With Priority

**Incorrect:** Assigning P1 because troubleshooting requires advanced technical knowledge.

**Correct:** Assess the business consequences of the issue.

### Error 4 — Ignoring Available Workarounds

**Incorrect:** Assigning high urgency without considering whether business operations can continue.

**Correct:** Evaluate the effectiveness of available workarounds.

### Error 5 — Failing to Reassess Priority

**Incorrect:** Leaving a ticket at P4 after the issue expands to multiple departments.

**Correct:** Update priority when impact or urgency changes.

### Error 6 — Using Priority to Replace Escalation

**Incorrect:** Assuming a P1 label automatically notifies the correct personnel.

**Correct:** Follow the required escalation and communication procedures.

---

## 17. Ticket Prioritization Quality Checklist

Before completing prioritization, verify:

- [ ] Ticket type confirmed
- [ ] Affected service identified
- [ ] Number of affected users assessed
- [ ] Business impact documented
- [ ] Urgency assessed
- [ ] Available workarounds considered
- [ ] Relevant deadlines identified
- [ ] Security implications considered
- [ ] Priority assigned using the applicable criteria
- [ ] Priority justification documented
- [ ] Assignment group confirmed
- [ ] Escalation initiated when required
- [ ] Requester updated when appropriate
- [ ] Priority reassessment planned if conditions change

---

## 18. Performance Metrics

Ticket prioritization effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Priority Assignment Accuracy | Measures consistency with defined priority criteria |
| Priority Reassessment Rate | Tracks tickets requiring priority changes |
| P1 Incident Volume | Measures critical incident frequency |
| High-Priority Response Time | Measures response performance for urgent tickets |
| Priority Escalation Time | Measures time required to initiate necessary escalation |
| Priority Documentation Completeness | Tracks recorded impact, urgency, and justification |
| Service Target Compliance | Evaluates performance against applicable service targets |
| Incorrect Priority Assignments | Identifies opportunities to improve assessments |

Metrics should use actual ticket data or clearly labeled simulated datasets.

---

## 19. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Performs initial impact and urgency assessment |
| Incident Management | Uses priority to coordinate incident response |
| Service Request Management | Applies request-specific fulfillment priorities |
| Knowledge Management | Provides guidance for common issues |
| Problem Management | Evaluates the significance of recurring incidents |
| Change Enablement | Assesses risk and urgency for proposed changes |
| Monitoring and Event Management | Provides alerts and service impact information |
| Service Configuration Management | Identifies critical infrastructure dependencies |
| Information Security Management | Evaluates security impact and escalation requirements |
| Continual Improvement | Reviews prioritization effectiveness and performance trends |

---

## 20. Related Procedures and Documentation

### Service Desk

- [Service Desk Overview](../README.md)
- [Ticket Intake Procedure](Ticket-Intake.md)
- [Ticket Categorization Procedure](Ticket-Categorization.md)

### ITIL Practices

- [Incident Management](../../Incident-Management/)
- [Service Request Management](../../Service-Request-Management/)
- [Monitoring and Event Management](../../Monitoring-and-Event-Management/)
- [Service Configuration Management](../../Service-Configuration-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

---

## 21. Procedure Review

This procedure should be reviewed when:

- Business service priorities change.
- New critical services are introduced.
- Priority assignment errors increase.
- Escalation requirements change.
- Service targets are updated.
- Ticket analysis identifies inconsistent prioritization.
- ITSM workflows are modified.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial ticket prioritization procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Business impact assessments, urgency classifications, service targets, support roles, and ticket scenarios may be simulated.

Ticket prioritization activities, technical investigations, and operational outcomes are documented based on hands-on lab exercises where indicated.

This procedure demonstrates ITIL-aligned Service Desk prioritization, business impact assessment, urgency evaluation, and escalation practices rather than employment experience within an actual production organization.
