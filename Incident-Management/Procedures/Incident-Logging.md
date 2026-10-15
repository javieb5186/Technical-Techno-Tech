# SOP — Incident Logging

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Incident Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-IM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practices:** Incident Management, Service Desk

---

## 1. Purpose

This procedure establishes a standardized method for logging and documenting IT incidents within Technical Techno Tech.

Incident logging ensures that unplanned service interruptions and reductions in service quality are recorded accurately, consistently, and with sufficient information to support investigation and service restoration.

The procedure supports:

- Accurate incident documentation
- Consistent incident identification
- Effective troubleshooting
- Clear ticket ownership
- Appropriate incident prioritization
- Reliable communication
- Technical escalation
- Incident history tracking
- Service performance reporting
- Problem identification
- Continual improvement

**Key Principle:** Every incident should have a clear, traceable record describing what happened, who or what was affected, when it occurred, and what actions were taken.

---

## 2. Scope

This procedure applies to all incidents affecting Technical Techno Tech's internal IT services.

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

### Incident Sources

Incidents may be identified through:

- Employee reports
- Service Desk interactions
- Email
- Telephone
- Self-service portals
- Monitoring alerts
- System administrators
- Security monitoring
- Automated diagnostic tools

Jira Service Management is the planned primary ITSM platform.

Only ticketing platforms and monitoring integrations actually configured should be described as operational.

---

## 3. ITIL 4 Incident Management

### Definition

An **incident** is an unplanned interruption to a service or a reduction in the quality of a service.

### Objective

The purpose of Incident Management is to minimize the negative impact of incidents by restoring normal service operation as quickly as possible.

### Examples

- An employee cannot authenticate to the domain.
- A workstation unexpectedly loses network connectivity.
- Microsoft Outlook becomes unavailable.
- A domain controller stops responding.
- A shared folder becomes inaccessible.
- A DNS service fails.
- A business application crashes.

### Incident vs. Service Request

| Incident | Service Request |
|---|---|
| Something is broken or degraded | Someone requests a predefined service action |
| Focuses on restoring service | Focuses on fulfilling a request |
| Usually unplanned | Usually planned or routine |
| Example: Employee cannot access an existing shared folder | Example: Employee requests access to a new shared folder |

Correct classification should occur before or during incident logging.

---

## 4. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Receiving incident reports
- Creating incident records
- Recording requester information
- Documenting symptoms
- Identifying affected services
- Recording initial impact and urgency
- Assigning initial priority
- Performing authorized initial troubleshooting
- Escalating incidents when necessary

### Incident Resolver

Responsible for:

- Reviewing assigned incident records
- Investigating reported symptoms
- Recording diagnostic findings
- Documenting corrective actions
- Updating incident status
- Validating service restoration

### Incident Coordinator

Responsible for:

- Monitoring incident records
- Coordinating support assignments
- Reviewing documentation quality
- Managing significant escalations
- Supporting incident communications

### IT Administrator

Responsible for:

- Investigating infrastructure-related incidents
- Performing authorized administrative actions
- Documenting technical findings
- Supporting service restoration

### Requester

Responsible for:

- Reporting accurate information
- Describing symptoms
- Providing relevant error messages
- Responding to clarification requests
- Confirming restoration when appropriate

**Lab Note:** These roles represent simulated organizational responsibilities. One learner may perform multiple roles during an exercise.

---

## 5. Incident Record Requirements

Each incident must have a unique identifier and sufficient information to support investigation and tracking.

### Required Fields

| Field | Description |
|---|---|
| Incident ID | Unique incident identifier |
| Summary | Short description of the issue |
| Description | Detailed explanation of the reported symptoms |
| Reported By | Person or system reporting the incident |
| Date and Time Reported | When the incident was logged |
| Affected Service | Internal IT service experiencing disruption |
| Category | Technical classification |
| Subcategory | Specific issue type |
| Impact | Extent of business disruption |
| Urgency | Required speed of response |
| Priority | Assigned incident priority |
| Status | Current incident state |
| Assigned Technician / Group | Responsible resolver |
| Initial Symptoms | Observed or reported behavior |
| Next Action | Immediate planned activity |

### Additional Information

Collect when applicable:

- Affected hostname
- Device type
- Operating system
- IP address
- Application name
- Error message
- Time symptoms began
- Number of affected employees
- Department
- Recent changes
- Troubleshooting already attempted
- Related monitoring events
- Relevant Configuration Items
- Screenshots
- Diagnostic logs

Do not collect passwords, authentication tokens, MFA codes, or other sensitive secrets.

---

## 6. Incident Identification

An incident may be identified by an employee, administrator, monitoring system, or other authorized source.

### Employee-Reported Incidents

Examples:

- "I cannot sign in to my computer."
- "My network drive disappeared."
- "Outlook keeps crashing."
- "I cannot connect to Wi-Fi."

### Monitoring-Detected Incidents

Examples:

- Domain controller unavailable
- Critical Windows service stopped
- Network device unreachable
- Server disk space exhausted
- Authentication service failure

Not every monitoring event is an incident.

An event should be assessed to determine whether it represents an actual or potential service interruption or degradation.

### Administrator-Detected Incidents

Examples:

- Active Directory replication errors affecting directory service health
- DNS resolution failures
- Unexpected server unavailability
- Application service failure

**Expected Result:** A suspected service interruption or degradation is identified for assessment and logging.

---

## 7. Incident Logging Procedure

### Step 1 — Receive the Incident Report

Receive the incident through an approved support channel or monitoring source.

Record:

- Reporting source
- Requester or reporting system
- Date and time
- Initial description
- Affected user or system

If the incident was reported outside the ticketing system, create an incident record.

**Expected Result:** The reported incident is captured.

### Step 2 — Verify the Incident Classification

Determine whether the reported issue represents an unplanned interruption or degradation of an existing service.

#### Decision Questions

1. Was the service previously working?
2. Is the service unexpectedly unavailable?
3. Has service quality decreased?
4. Is the employee requesting new access or functionality instead?
5. Is the report actually a monitoring event requiring further assessment?

#### Example

**Report:** "I cannot access the HR shared folder."

If the employee previously had authorized access and it stopped working, classify the issue as an incident.

If the employee is requesting access they never had, classify it as a service request.

**Expected Result:** The correct work type is selected.

### Step 3 — Check for Existing Incident Records

Search the ticketing system for similar or related incidents.

Review:

- Matching symptoms
- Affected services
- Affected devices
- Time of occurrence
- Existing major incidents
- Previously reported outages

#### Duplicate Incident Handling

If an existing incident covers the same underlying service disruption:

1. Determine whether the new report provides additional information.
2. Link or associate the report with the existing incident when supported.
3. Record the additional affected user or system.
4. Avoid unnecessary duplicate investigations.
5. Preserve relevant reporting information.

Separate employee reports may remain as individual linked tickets when required for communication or service tracking.

**Expected Result:** Duplicate work is minimized without losing important information.

### Step 4 — Generate the Incident ID

Assign a unique incident identifier.

#### Portfolio Naming Convention

```text
INC-001
INC-002
INC-003
```

#### Example Record Location

```text
Incident-Management/
└── Records/
    └── INC-001-Domain-Authentication-Failure/
        ├── README.md
        └── Evidence/
```

Incident IDs should remain unique and consistent.

When using Jira Service Management, retain the platform-generated ticket ID and reference the corresponding portfolio incident ID where appropriate.

**Expected Result:** The incident has a traceable identifier.

### Step 5 — Create the Incident Summary

Write a concise summary describing the affected service or system and the observed issue.

#### Recommended Format

```text
[Affected Service or System] — [Observed Failure]
```

#### Examples

- `Active Directory — User Authentication Failure`
- `Windows Server — DNS Service Unavailable`
- `Networking — Workstation Cannot Reach Gateway`
- `Microsoft 365 — Outlook Sign-In Failure`
- `Endpoint Management — Windows Application Crash`

Avoid vague summaries such as:

- "Computer broken"
- "Not working"
- "Help needed"
- "Server issue"

**Expected Result:** The incident can be understood from its summary.

### Step 6 — Record the Incident Description

Document the reported symptoms using factual language.

Include:

- What the user was attempting
- What happened
- What was expected
- When the issue began
- Whether the issue is ongoing
- Relevant error messages
- Known affected systems

#### Example

**Summary:** Active Directory — User Authentication Failure

**Description:**

An employee reports being unable to sign in to their domain-joined Windows workstation.

The employee states that authentication worked previously but now fails.

The workstation displays an authentication error.

The cause has not yet been determined.

**Expected Result:** The incident description provides enough information to begin investigation.

### Step 7 — Identify the Affected Service

Associate the incident with the appropriate internal IT service.

| Incident | Affected Service |
|---|---|
| Domain authentication failure | IT-SVC-001 — Identity & Access Management |
| Workstation application failure | IT-SVC-002 — Endpoint Management |
| Outlook unavailable | IT-SVC-003 — Microsoft 365 & Collaboration |
| Network connectivity failure | IT-SVC-004 — Network Connectivity |
| DNS service unavailable | IT-SVC-005 — Server & Infrastructure Services |
| Suspected unauthorized access | IT-SVC-006 — Information Security |

A security-related incident may also affect another primary service.

Record the primary affected service and relevant secondary services where appropriate.

**Expected Result:** The incident is associated with the correct service.

### Step 8 — Categorize the Incident

Assign the appropriate technical category and subcategory.

#### Example

| Field | Value |
|---|---|
| Service | Identity & Access Management |
| Category | Active Directory |
| Subcategory | Authentication Failure |

Other examples:

| Category | Subcategory |
|---|---|
| Networking | DNS Resolution |
| Windows Server | Service Availability |
| Microsoft 365 | Outlook |
| Endpoint Management | Application Failure |
| Microsoft Entra ID | Sign-In Issue |
| Virtualization | Virtual Machine Availability |

Use the best-supported category based on current evidence.

Categories may be updated when troubleshooting reveals additional information.

**Expected Result:** The incident is classified for investigation and reporting.

### Step 9 — Assess Business Impact

Determine the extent of the disruption.

#### Impact Levels

| Impact | Description |
|---|---|
| High | Critical business service or organization-wide disruption |
| Medium | Departmental or multiple-user disruption |
| Low | Individual user or limited operational impact |

Consider:

- Number of affected users
- Business criticality
- Service dependencies
- Operational consequences
- Availability of workarounds

**Expected Result:** Impact is recorded.

### Step 10 — Assess Urgency

Determine how quickly the incident requires attention.

#### Urgency Levels

| Urgency | Description |
|---|---|
| High | Immediate attention required |
| Medium | Prompt attention required |
| Low | Routine handling appropriate |

Consider:

- Business deadlines
- Availability of workarounds
- Potential for worsening conditions
- Security exposure
- Operational consequences

**Expected Result:** Urgency is recorded.

### Step 11 — Assign Incident Priority

Use the organization's proposed impact and urgency matrix.

| Impact / Urgency | High | Medium | Low |
|---|---|---|---|
| High | P1 | P2 | P3 |
| Medium | P2 | P3 | P4 |
| Low | P3 | P4 | P4 |

#### Priority Definitions

| Priority | Classification |
|---|---|
| P1 | Critical |
| P2 | High |
| P3 | Medium |
| P4 | Low |

Record the justification for the assigned priority.

Security-related escalation requirements may apply independently of the normal priority matrix.

**Expected Result:** The incident receives an appropriate priority.

### Step 12 — Identify Affected Systems

Record known technical components involved in the incident.

Examples:

- DC01
- DC02
- MGMT01
- CLIENT01
- Microsoft 365 tenant
- Network switch
- Router
- Virtual machine
- DNS service

Where available, reference the related Configuration Item.

#### Example

```text
Affected System: DC01
Hostname: DC01
Service: Active Directory Domain Services
Related CI: CI-001
```

Do not assume that an affected component is the root cause before investigation.

**Expected Result:** Known affected infrastructure is documented.

### Step 13 — Record Initial Evidence

Attach or reference relevant evidence.

Examples:

- Error screenshots
- Event Viewer entries
- PowerShell output
- Network diagnostic results
- Service status information
- Monitoring alerts

#### Example Commands

**Network Connectivity**

```powershell
ping 10.20.10.10
```

**DNS Resolution**

```powershell
nslookup dc01.homelab.local
```

**Active Directory Domain Controller Discovery**

```powershell
nltest /dsgetdc:homelab.local
```

**Active Directory Replication**

```powershell
repadmin /replsummary
```

Commands should only be executed when appropriate to the incident and within authorized administrative permissions.

#### Evidence Naming Examples

```text
Evidence/
├── 01-Error-Message.png
├── 02-Connectivity-Test.txt
├── 03-Event-Viewer.png
└── 04-Validation-Results.txt
```

**Expected Result:** Initial findings are preserved for investigation.

### Step 14 — Assign the Incident

Identify the appropriate technician or support group.

Potential assignments include:

- Service Desk
- Endpoint Support
- Identity Administration
- Systems Administration
- Network Administration
- Microsoft 365 Administration
- Information Security

Assignment should reflect:

- Technical category
- Required permissions
- Complexity
- Priority
- Escalation requirements

**Expected Result:** The incident has a responsible owner.

### Step 15 — Set the Incident Status

Assign the appropriate incident status.

| Status | Description |
|---|---|
| New | Incident received |
| Open | Incident accepted for processing |
| In Progress | Active investigation or restoration underway |
| Pending User | Awaiting requester information |
| Pending External | Awaiting an external dependency |
| Escalated | Specialized support engaged |
| Resolved | Service restored and resolution recorded |
| Closed | Closure requirements completed |

Actual workflow states may differ by ticketing platform.

**Expected Result:** Incident status reflects the current work.

### Step 16 — Acknowledge the Incident

Notify the requester when appropriate.

The acknowledgment should include:

- Incident reference
- Confirmation that the report was received
- General understanding of the issue
- Current handling status
- Next steps

Do not promise a resolution time without an applicable service target.

**Expected Result:** The requester knows the incident has been recorded.

### Step 17 — Save and Verify the Record

Before completing incident logging, verify that all required fields are populated.

Confirm:

- Unique incident ID
- Clear summary
- Accurate description
- Correct classification
- Affected service
- Impact and urgency
- Priority
- Assignment
- Status
- Available evidence
- Next action

**Expected Result:** The incident record is ready for investigation and service restoration.

---

## 8. Incident Logging Workflow

```text
Incident Reported or Detected
             |
             v
     Review Information
             |
             v
    Confirm Incident Type
             |
             v
   Check Existing Incidents
             |
             v
      Create / Link Record
             |
             v
     Assign Incident ID
             |
             v
   Document Initial Symptoms
             |
             v
   Identify Affected Service
             |
             v
       Categorize Incident
             |
             v
    Assess Impact & Urgency
             |
             v
       Assign Priority
             |
             v
   Record Systems & Evidence
             |
             v
      Assign Incident Owner
             |
             v
    Acknowledge and Save
             |
             v
   Investigation & Restoration
```

For critical incidents, escalation and restoration activities may begin before all routine logging fields are completed.

Incident documentation should be updated as soon as practical.

---

## 9. Incident Logging Standards

### Accuracy

Record observable facts and clearly distinguish them from assumptions.

**Incorrect:**

"The domain controller is broken."

**Correct:**

"CLIENT01 cannot authenticate to the domain. Domain controller connectivity has not yet been verified."

### Completeness

Record sufficient information for another technician to continue the investigation.

### Chronology

Document significant actions and findings in chronological order.

### Consistency

Use standardized:

- Incident IDs
- Service names
- Technical categories
- Priority definitions
- Status values
- Evidence naming conventions

### Traceability

Link related:

- Monitoring events
- Configuration Items
- Change records
- Problem records
- Knowledge articles

### Confidentiality

Do not publish:

- Passwords
- MFA codes
- Authentication tokens
- Private keys
- Sensitive employee information
- Unredacted confidential logs

---

## 10. Incident Documentation Example

### Incident Information

**Incident ID:** INC-001  
**Summary:** Active Directory — Domain Authentication Failure  
**Reported By:** Simulated Employee  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Category:** Active Directory  
**Subcategory:** Authentication Failure  
**Status:** New

### Description

An employee reports being unable to authenticate to a domain-joined Windows workstation.

The employee states that authentication previously worked.

The cause of the issue is currently unknown.

### Initial Assessment

**Impact:** Low  
**Urgency:** Medium  
**Priority:** P4 — Low

**Priority Justification:** One employee is affected, and no broader service disruption has been confirmed.

### Affected Infrastructure

**Workstation:** CLIENT01  
**Domain:** homelab.local  
**Potential Dependency:** Domain Controller / DNS

### Initial Evidence

Not yet collected.

### Next Action

Verify:

1. Workstation network connectivity.
2. DNS configuration.
3. Domain controller availability.
4. Authentication error details.

### Assigned Group

Service Desk

### Related Records

None identified at initial logging.

**Example Status:** Illustrative scenario — not an actual completed incident investigation.

---

## 11. Incident Logging vs. Investigation

Incident logging and incident investigation are related but separate activities.

### Incident Logging

Focuses on:

- Recording the incident
- Capturing symptoms
- Identifying affected services
- Categorization
- Prioritization
- Assignment
- Initial evidence

### Incident Investigation

Focuses on:

- Diagnosing the issue
- Testing potential causes
- Reviewing technical evidence
- Identifying workarounds
- Restoring service
- Validating resolution

Incident logging should not be delayed until the root cause is known.

---

## 12. Incident Logging vs. Problem Management

An incident record documents a service interruption or degradation.

A Problem record manages the underlying cause or potential cause of one or more incidents.

### Example

**Incident:**

An employee cannot authenticate to the domain.

**Problem:**

Repeated authentication incidents are linked to an underlying infrastructure issue requiring investigation.

A Problem record should be created when warranted by the nature, frequency, risk, or significance of the underlying issue.

Not every incident requires a separate Problem record.

---

## 13. Incident Record Storage

Incident records are maintained under:

```text
Incident-Management/
└── Records/
    ├── INC-001-Incident-Title/
    │   ├── README.md
    │   └── Evidence/
    ├── INC-002-Incident-Title/
    │   ├── README.md
    │   └── Evidence/
    └── INC-003-Incident-Title/
        ├── README.md
        └── Evidence/
```

### Record Contents

Each incident record should include:

- Incident details
- Business impact
- Technical symptoms
- Troubleshooting history
- Diagnostic evidence
- Escalation information
- Resolution or workaround
- Validation results
- Related ITSM records
- Closure information

### Incident Template

Use:

[Incident Template](../../Templates/Incident-Template.md)

The template provides a consistent structure for documenting individual incidents.

---

## 14. Common Incident Logging Errors

### Error 1 — Incomplete Description

**Incorrect:** "Cannot log in."

**Correct:** Record the affected system, symptoms, error message, and time the issue began.

### Error 2 — Incorrect Work Type

**Incorrect:** Logging a new software installation request as an incident.

**Correct:** Classify predefined service fulfillment as a service request.

### Error 3 — Missing Impact Information

**Incorrect:** Assigning priority without determining the number of affected users or business consequences.

**Correct:** Record impact and urgency before assigning priority when practical.

### Error 4 — Assuming the Root Cause

**Incorrect:** Recording "DNS failure" as the confirmed cause before testing.

**Correct:** Record DNS as a suspected dependency until evidence supports the conclusion.

### Error 5 — Duplicate Incident Records

**Incorrect:** Creating unrelated tickets for the same known outage without linking them.

**Correct:** Associate related reports while preserving relevant requester information.

### Error 6 — Missing Evidence

**Incorrect:** Recording that a diagnostic test failed without preserving the result.

**Correct:** Document the command, observed output, and relevant evidence.

### Error 7 — Delayed Critical Escalation

**Incorrect:** Spending excessive time completing routine fields during a critical outage.

**Correct:** Initiate urgent response and complete documentation as practical.

---

## 15. Incident Logging Quality Checklist

Before completing initial incident logging, verify:

- [ ] Incident report received
- [ ] Incident classification confirmed
- [ ] Existing incidents checked
- [ ] Unique incident ID assigned
- [ ] Requester or reporting source recorded
- [ ] Date and time documented
- [ ] Incident summary completed
- [ ] Symptoms clearly described
- [ ] Affected IT service identified
- [ ] Technical category assigned
- [ ] Subcategory selected
- [ ] Business impact assessed
- [ ] Urgency assessed
- [ ] Priority assigned
- [ ] Priority justification recorded
- [ ] Known affected systems documented
- [ ] Initial evidence attached when available
- [ ] Incident owner assigned
- [ ] Status updated
- [ ] Requester acknowledged when appropriate
- [ ] Next action documented
- [ ] Related records linked when applicable

---

## 16. Incident Logging Performance Metrics

Incident logging effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Incident Logging Completeness | Measures required fields completed |
| Incident Classification Accuracy | Evaluates correct identification of incidents |
| Incident Categorization Accuracy | Measures correct technical classification |
| Duplicate Incident Rate | Identifies unnecessary duplicate records |
| Time to Log Incident | Measures time between report and record creation |
| Initial Assignment Accuracy | Evaluates correct first assignment |
| Priority Assignment Accuracy | Measures consistency with prioritization rules |
| Evidence Documentation Rate | Measures preservation of relevant diagnostic information |
| Incident Reassignment Rate | Identifies routing issues |

Metrics should use actual incident records or clearly labeled simulated datasets.

---

## 17. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Receives reports and creates incident records |
| Incident Management | Coordinates incident investigation and service restoration |
| Service Request Management | Handles requests that do not represent incidents |
| Knowledge Management | Provides troubleshooting and documentation guidance |
| Problem Management | Uses incident records to identify underlying causes |
| Change Enablement | Manages applicable corrective configuration changes |
| Monitoring and Event Management | Supplies monitoring events and alerts |
| Service Configuration Management | Identifies affected infrastructure components |
| Information Security Management | Supports security-related incident handling |
| Continual Improvement | Analyzes incident data to improve services |

---

## 18. Related Procedures and Documentation

### Incident Management

- [Incident Management Overview](../README.md)

### Service Desk Procedures

- [Ticket Intake](../../Service-Desk/Procedures/Ticket-Intake.md)
- [Ticket Categorization](../../Service-Desk/Procedures/Ticket-Categorization.md)
- [Ticket Prioritization](../../Service-Desk/Procedures/Ticket-Prioritization.md)
- [Ticket Escalation](../../Service-Desk/Procedures/Ticket-Escalation.md)

### ITIL Practices

- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Problem Management](../../Problem-Management/)
- [Change Enablement](../../Change-Enablement/)
- [Monitoring and Event Management](../../Monitoring-and-Event-Management/)
- [Service Configuration Management](../../Service-Configuration-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

### Templates and Organization Documentation

- [Incident Template](../../Templates/Incident-Template.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Company Overview](../../Company-Overview.md)
- [Operational Scenarios](../../Scenarios/)

---

## 19. Procedure Review

This procedure should be reviewed when:

- Incident logging requirements change.
- New ticketing platforms are introduced.
- Incident classification standards change.
- Required ticket fields are updated.
- Monitoring integrations are modified.
- Documentation quality issues are identified.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial incident logging procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee reports, organizational roles, incident scenarios, and business impact assessments may be simulated.

Incident investigations, troubleshooting actions, technical configurations, and validation results are documented based on hands-on lab activities where indicated.

This procedure demonstrates ITIL-aligned Incident Management, incident documentation, service impact assessment, and technical support practices rather than employment experience within an actual production organization.
