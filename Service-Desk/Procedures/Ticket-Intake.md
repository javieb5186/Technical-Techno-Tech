# SOP — Ticket Intake and Initial Triage

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Service Desk  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-SD-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practices:** Service Desk, Incident Management, Service Request Management

---

## 1. Purpose

This procedure establishes a standardized process for receiving, documenting, categorizing, prioritizing, and routing incoming IT support tickets.

The objective is to ensure that every support request is handled consistently, with sufficient information for efficient troubleshooting, fulfillment, or escalation.

This procedure supports:

- Accurate ticket documentation
- Consistent request classification
- Appropriate ticket prioritization
- Effective communication
- Clear ticket ownership
- Timely escalation
- Reliable operational reporting

**Key Principle:** Every ticket should clearly explain who needs assistance, what they need, how the issue affects them, and what action should happen next.

---

## 2. Scope

This procedure applies to incoming requests for Technical Techno Tech's internal IT services.

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

### Ticket Sources

Tickets may originate from:

- Employee self-service portal
- Email
- Telephone
- Live chat
- Walk-up support
- Monitoring alerts
- Internal IT personnel

Jira Service Management is the proposed primary ticketing platform for this portfolio.

Only channels actually configured in the lab should be represented as operational.

---

## 3. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Receiving incoming tickets
- Verifying requester information
- Recording issue details
- Identifying the affected service
- Classifying the ticket
- Assessing impact and urgency
- Assigning priority
- Performing initial troubleshooting when appropriate
- Routing or escalating tickets
- Communicating with the requester
- Maintaining accurate ticket records

### Technical Support Specialist

Responsible for:

- Investigating assigned technical issues
- Performing advanced troubleshooting
- Recording findings and actions
- Updating ticket status
- Escalating when necessary

### IT Administrator

Responsible for:

- Handling issues requiring elevated permissions
- Reviewing requests for infrastructure modifications
- Performing authorized administrative activities
- Supporting complex technical investigations

### Requester

Responsible for:

- Providing accurate information
- Describing the issue or request
- Responding to clarification questions
- Participating in validation when appropriate

**Lab Note:** These roles are simulated. A single learner may perform multiple roles during an exercise.

---

## 4. Ticket Classification

Every incoming ticket must be evaluated to determine the appropriate type of work.

### 4.1 Incident

An **incident** is an unplanned interruption to a service or a reduction in service quality.

Examples:

- Employee cannot sign in to Windows.
- Network connectivity is unavailable.
- Outlook stops working.
- A shared folder becomes inaccessible.
- A critical Windows service fails.

**Primary Objective:** Restore normal service as quickly as appropriate.

**Related Practice:** Incident Management

### 4.2 Service Request

A **service request** is a request from a user or authorized representative for a predefined service action.

Examples:

- Request a new user account.
- Request access to a shared folder.
- Request software installation.
- Request a password reset.
- Request a new workstation.
- Request an employee onboarding task.

**Primary Objective:** Fulfill the authorized request according to established procedures.

**Related Practice:** Service Request Management

### 4.3 Security-Related Ticket

A ticket may involve a potential information security concern.

Examples:

- Suspected account compromise
- Suspicious authentication activity
- Unauthorized access
- Malware alert
- Lost company device

Security-related tickets must be assessed for appropriate confidentiality, urgency, and escalation.

A security concern may also be classified as an incident or another work type depending on the situation.

**Related Practice:** Information Security Management

### 4.4 Other Work Types

Some activities may require separate records for:

- Problem investigation
- Change assessment
- Monitoring events
- Continual improvement

These records should be created when the corresponding management practice is applicable.

**Important:** A user reporting a service failure does not automatically create a Problem record. A Problem record is used when investigation of an underlying cause is warranted.

---

## 5. Required Ticket Information

The Service Desk should collect enough information to understand and route the ticket.

### Required Fields

| Field | Description |
|---|---|
| Ticket ID | Unique ticket identifier |
| Summary | Short description of the issue or request |
| Requester | Person reporting the issue |
| Contact Information | Approved method of contacting the requester |
| Date and Time | When the ticket was received |
| Affected Service | Relevant internal IT service |
| Ticket Type | Incident, service request, or applicable work type |
| Description | Detailed explanation of the issue or request |
| Impact | Extent of business or service disruption |
| Urgency | How quickly action is required |
| Priority | Assigned response priority |
| Status | Current ticket state |
| Assigned Technician | Responsible technician or support group |

### Additional Information

Collect when relevant:

- Affected hostname
- Device type
- Operating system
- Application name
- Error message
- Time the issue began
- Number of affected users
- Business process affected
- Recent changes
- Troubleshooting already attempted
- Screenshots or diagnostic evidence

Do not collect passwords, MFA codes, or other authentication secrets.

---

## 6. Ticket Intake Procedure

### Step 1 — Receive the Ticket

Receive the support request through an approved communication channel.

Confirm:

- Who is reporting the issue
- Whether the request is for themselves or another employee
- What assistance is required
- Whether the issue is currently occurring

If the request was received outside the ticketing system, create a ticket using the information provided.

**Expected Result:** The support interaction is recorded.

### Step 2 — Verify Requester Information

Confirm the requester's identity using an appropriate verification method.

Verification requirements depend on the action being requested.

For example:

- General troubleshooting may require basic requester confirmation.
- Password resets require approved identity verification.
- Privileged access requests require additional authorization.

Do not rely solely on the caller's claimed identity for sensitive operations.

**Expected Result:** Requester information is sufficiently verified for the next action.

### Step 3 — Identify the Issue or Request

Ask questions to establish the nature of the ticket.

Suggested questions:

1. What are you trying to accomplish?
2. What happens when you attempt it?
3. When did the issue begin?
4. Are you receiving an error message?
5. Is anyone else experiencing the same issue?
6. Has anything changed recently?
7. Have you attempted any troubleshooting?

Not every question is required for every ticket.

**Expected Result:** The ticket contains a clear description of the issue or request.

### Step 4 — Determine the Ticket Type

Classify the ticket based on the information collected.

**Decision Guide:**

- Is an existing service unexpectedly unavailable or degraded? → **Incident**
- Is the user requesting an authorized, predefined service action? → **Service Request**
- Does the ticket indicate a possible security threat? → **Apply security escalation requirements**
- Does investigation reveal a recurring underlying issue? → **Consider Problem Management**
- Does resolution require a controlled modification? → **Consider Change Enablement**

**Expected Result:** The ticket is assigned the appropriate classification.

### Step 5 — Identify the Affected Service

Associate the ticket with the relevant service in the IT Service Catalog.

Examples:

| Ticket Description | Service |
|---|---|
| Employee cannot sign in | Identity & Access Management |
| Laptop requires configuration | Endpoint Management |
| Outlook is unavailable | Microsoft 365 & Collaboration |
| Employee cannot access the network | Network Connectivity |
| DNS service is unavailable | Server & Infrastructure Services |
| Suspicious account activity | Information Security |
| New employee needs IT access | Employee IT Lifecycle |

A ticket may involve multiple services. Identify the primary affected service and document important dependencies.

**Expected Result:** The ticket is associated with an internal IT service.

### Step 6 — Assess Impact

Determine the extent of the issue.

| Impact | Description |
|---|---|
| High | Organization-wide or critical business service disruption |
| Medium | Department or multiple users significantly affected |
| Low | Individual user or limited operational impact |

Consider:

- Number of affected users
- Business criticality
- Service availability
- Operational consequences

**Expected Result:** Business impact is documented.

### Step 7 — Assess Urgency

Determine how quickly the issue requires attention.

| Urgency | Description |
|---|---|
| High | Immediate action is required |
| Medium | Prompt action is needed |
| Low | Work can follow normal scheduling |

Consider:

- Business deadlines
- Availability of workarounds
- Operational consequences
- Security exposure
- Potential for worsening conditions

**Expected Result:** Urgency is documented.

### Step 8 — Assign Priority

Use impact and urgency to determine ticket priority.

#### Proposed Priority Matrix

| Impact / Urgency | High | Medium | Low |
|---|---|---|---|
| High Impact | P1 | P2 | P3 |
| Medium Impact | P2 | P3 | P4 |
| Low Impact | P3 | P4 | P4 |

#### Priority Definitions

| Priority | Classification | Description |
|---|---|---|
| P1 | Critical | Critical service disruption requiring immediate coordination |
| P2 | High | Significant business impact requiring expedited attention |
| P3 | Medium | Standard operational issue |
| P4 | Low | Limited impact or routine work |

This matrix is a proposed lab policy rather than a universal ITIL requirement.

Service requests may use separate fulfillment targets and priority rules.

Security issues may require escalation independent of the normal priority matrix.

**Expected Result:** Priority is documented with an appropriate justification.

### Step 9 — Review Existing Knowledge

Search available documentation for relevant troubleshooting or fulfillment instructions.

Potential sources include:

- Internal Knowledge Base
- Existing support procedures
- Previous tickets
- Infrastructure documentation
- Approved vendor documentation

Use only instructions appropriate to the situation and the technician's authorization.

**Expected Result:** Relevant existing knowledge is identified before unnecessary troubleshooting is repeated.

### Step 10 — Perform Initial Troubleshooting

For incidents, perform safe and authorized initial diagnostic steps when appropriate.

Examples:

- Confirm network connectivity.
- Verify the affected service.
- Review the error message.
- Check whether the issue affects other users.
- Review relevant system status.
- Identify recent changes.

Record:

- Diagnostic action
- Command or tool used
- Result
- Time performed
- Technician

Avoid making significant infrastructure changes without the required authorization.

**Expected Result:** Initial findings are documented.

### Step 11 — Assign or Escalate

Determine whether the Service Desk can continue handling the ticket.

#### Assign to Service Desk

Appropriate when:

- The issue is within the technician's responsibilities.
- Required permissions are available.
- An approved procedure exists.
- No specialized escalation is required.

#### Escalate to Technical Support or Administration

Appropriate when:

- Elevated permissions are required.
- The issue involves complex infrastructure.
- Specialized technical knowledge is necessary.
- A significant service disruption is identified.
- A security concern requires specialized handling.

#### Escalation Information

Include:

- Ticket summary
- Business impact
- Priority
- Affected systems
- Troubleshooting completed
- Diagnostic results
- Reason for escalation
- Outstanding questions

**Expected Result:** The ticket has an appropriate owner and next action.

### Step 12 — Communicate With the Requester

Provide a clear status update.

The communication should include:

- Confirmation that the ticket was received
- Ticket reference number
- General understanding of the issue
- Next steps
- Any information still required

Do not promise a resolution time unless supported by an applicable service target.

**Expected Result:** The requester understands the ticket's current status and next steps.

### Step 13 — Update Ticket Status

Set the appropriate ticket status.

| Status | Description |
|---|---|
| New | Ticket has been received |
| Open | Ticket is accepted for processing |
| In Progress | Active work is underway |
| Pending User | Awaiting requester information or action |
| Pending Approval | Awaiting required authorization |
| Escalated | Assigned for specialized handling |
| Resolved | Required action has been completed and validated |
| Closed | Ticket documentation and closure requirements are complete |

Actual status names may vary depending on the configured ticketing platform.

**Expected Result:** Ticket status accurately reflects the work being performed.

---

## 7. Ticket Routing Guidelines

| Ticket Category | Initial Routing |
|---|---|
| Password reset | Service Desk / Identity Administration |
| Account lockout | Service Desk / Identity Administration |
| Shared folder access request | Service Request Management |
| Workstation troubleshooting | Service Desk / Endpoint Support |
| Microsoft 365 issue | Service Desk / Microsoft 365 Administration |
| Network connectivity failure | Service Desk / Network Administration |
| Domain controller failure | Systems Administration |
| Suspected account compromise | Information Security escalation |
| New employee onboarding | Service Request Management / Employee IT Lifecycle |
| Infrastructure configuration change | Change Enablement, when applicable |

Routing should reflect technician permissions, technical complexity, and organizational requirements.

---

## 8. Ticket Documentation Standards

Ticket descriptions should be clear, factual, and concise.

### Recommended Ticket Summary Format

`[Affected Service or System] — [Issue or Request]`

Examples:

- `Active Directory — Employee Account Locked`
- `Microsoft 365 — Outlook Sign-In Failure`
- `Networking — Workstation Cannot Reach Gateway`
- `Endpoint Management — Software Installation Request`
- `Windows Server — DNS Service Unavailable`

### Documentation Requirements

Every ticket should:

1. Identify the requester.
2. Describe the issue or request.
3. Identify the affected service.
4. Record the ticket classification.
5. Document impact and urgency when applicable.
6. Record assigned priority.
7. Identify the responsible technician or group.
8. Document troubleshooting or fulfillment activities.
9. Include relevant evidence.
10. Record communication and escalation.
11. Identify the next action.
12. Document resolution and validation before closure.

---

## 9. Example Ticket Intake

### Scenario

An employee contacts the Service Desk because they cannot access a shared departmental folder.

### Initial Ticket

**Summary:** Active Directory — Shared Folder Access Denied

**Requester:** Sarah Connor  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Ticket Type:** Incident — pending confirmation  
**Impact:** Low  
**Urgency:** Medium  
**Proposed Priority:** P4

### Description

The employee reports receiving an access-denied message when attempting to open a departmental shared folder.

The employee states that access previously worked.

### Initial Assessment

The technician should determine:

- Whether the employee previously had authorized access
- Whether other employees are affected
- Whether the folder is reachable
- Whether security group membership changed
- Whether file permissions changed
- Whether the employee is requesting new access instead of reporting lost access

### Classification Decision

**If previously authorized access stopped working:** Treat as an incident.

**If the employee is requesting access they never had:** Treat as a service request requiring applicable authorization.

### Next Action

Route the ticket according to its confirmed classification and the technician's permissions.

This is an illustrative fictional scenario, not a claim that a live ticket was processed.

---

## 10. Quality Assurance Checklist

Before completing ticket intake, verify:

- [ ] Ticket created
- [ ] Requester identified
- [ ] Required identity verification completed
- [ ] Issue or request clearly described
- [ ] Ticket type assigned
- [ ] Affected service identified
- [ ] Impact assessed
- [ ] Urgency assessed
- [ ] Priority assigned
- [ ] Relevant evidence attached
- [ ] Existing knowledge reviewed when appropriate
- [ ] Initial troubleshooting documented when performed
- [ ] Ticket owner assigned
- [ ] Escalation completed when required
- [ ] Requester updated
- [ ] Ticket status updated
- [ ] Next action documented

---

## 11. Ticket Intake Performance Metrics

Ticket intake effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Ticket Classification Accuracy | Measures correct classification of incoming work |
| First Response Time | Measures time from ticket creation to initial response |
| Ticket Reassignment Rate | Identifies routing and classification issues |
| Ticket Documentation Completeness | Measures required information captured |
| First Contact Resolution Rate | Tracks tickets resolved during the initial interaction |
| Escalation Accuracy | Evaluates whether tickets reach appropriate support personnel |
| Ticket Backlog | Tracks unresolved incoming work |

Metrics should be based on actual ticket data or clearly labeled simulated datasets.

---

## 12. Related Procedures and Documentation

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Incident Management](../../Incident-Management/)
- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Problem Management](../../Problem-Management/)
- [Change Enablement](../../Change-Enablement/)
- [Information Security Management](../../Information-Security-Management/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

### Templates

- [Incident Template](../../Templates/Incident-Template.md)
- [Service Request Template](../../Templates/Service-Request-Template.md)

---

## 13. Procedure Review

This procedure should be reviewed when:

- Ticketing workflows change.
- New support channels are introduced.
- Service categories are updated.
- Escalation responsibilities change.
- Priority criteria are revised.
- Ticket quality reviews identify documentation gaps.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial ticket intake and triage procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee identities, business requests, ticket examples, organizational responsibilities, and approval workflows may be simulated.

Ticketing configurations, troubleshooting actions, technical investigations, and validation are documented based on hands-on work performed in controlled lab environments where indicated.

This procedure demonstrates ITIL-aligned Service Desk operations, ticket classification, prioritization, communication, and escalation rather than employment experience within an actual production organization.
