# SOP-SRM-001 — Request Logging

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Request Management  
**Document Type:** Standard Operating Procedure (SOP)  
**SOP ID:** SOP-SRM-001  
**Version:** 1.0  
**Status:** Draft — Proposed Operating Standard  
**Process Owner:** Internal IT  
**Primary Responsible Function:** Service Desk  
**Effective Date:** Pending Adoption  
**Last Reviewed:** Not Yet Reviewed  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

# 1. Purpose

Establish a standardized procedure for receiving, validating, classifying, and documenting employee IT service requests.

This procedure ensures that requests are consistently recorded with sufficient information for assessment, authorization, fulfillment, and closure.

The objectives are to:

- Provide employees with a consistent method for requesting IT services.
- Ensure service requests are accurately documented.
- Identify the requester and requested service.
- Distinguish service requests from incidents.
- Capture information required for fulfillment.
- Identify requests requiring authorization.
- Assign appropriate ownership.
- Establish traceability throughout the request lifecycle.
- Support reporting and continual improvement.

**Key Principle:** A service request must be sufficiently documented before fulfillment begins.

Logging a request does not automatically authorize the requested action.

---

# 2. Scope

## 2.1 In Scope

This procedure applies to routine employee requests for IT services, including:

- User account creation
- User account modification
- Password reset requests
- Access permission requests
- Software installation requests
- Microsoft 365 license assignments
- Device provisioning requests
- Hardware requests
- Shared folder access
- Distribution group membership
- Microsoft Teams or SharePoint access
- Approved configuration requests
- General IT service inquiries

## 2.2 Out of Scope

The following activities are managed through other procedures:

- Incident investigation and resolution
- Problem investigation
- Emergency security response
- Technical change implementation
- Service request authorization
- Service request fulfillment
- Service request closure

A request may be related to these activities without replacing their established processes.

## 2.3 Supported Environments

Depending on the request, this procedure may involve:

- Windows 11
- Windows Server
- Active Directory Domain Services
- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Hyper-V
- Network infrastructure
- Azure resources

Actual system availability and licensing must be verified before processing requests involving those technologies.

---

# 3. ITIL 4 Alignment

This procedure supports the ITIL 4 Service Request Management practice.

Service Request Management focuses on handling predefined, user-initiated service requests in an effective and user-friendly manner.

Request Logging establishes the initial record required for subsequent activities.

## 3.1 Related Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Provides a primary point of contact for employees |
| Service Request Management | Coordinates request handling |
| Knowledge Management | Provides request guidance and fulfillment instructions |
| Information Security Management | Establishes access and security requirements |
| Service Configuration Management | Provides information about affected configuration items |
| Change Enablement | Supports changes requiring formal change control |
| Continual Improvement | Evaluates request trends and process performance |

### Important

ITIL practices are not separate organizational departments.

A technician may perform activities associated with multiple practices according to assigned responsibilities and permissions.

---

# 4. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Requester | Submits the request and provides required information |
| Service Desk Technician | Receives, validates, classifies, and logs the request |
| Request Owner | Coordinates progress and maintains the request record |
| Fulfillment Technician | Performs authorized technical work |
| Approver | Evaluates requests requiring authorization |
| Service Owner | Defines requirements for the relevant IT service |
| IT Administrator | Handles requests requiring elevated technical permissions |

## 4.1 Service Desk Responsibilities

The Service Desk should:

1. Receive the request.
2. Identify the requester.
3. Determine the requested service.
4. Verify that sufficient information is available.
5. Check for duplicate requests.
6. Determine whether the issue is a service request or incident.
7. Record the request.
8. Identify potential authorization requirements.
9. Assign an appropriate owner or fulfillment group.
10. Communicate the request reference to the requester.

## 4.2 Requester Responsibilities

The requester should:

- Describe the requested service.
- Provide relevant business justification when required.
- Identify the affected user or device.
- Provide supporting information.
- Respond to clarification requests.
- Follow applicable authorization procedures.

---

# 5. Service Request Definition

A **service request** is a request from a user or authorized representative for something that is part of normal service delivery.

Examples include:

- Requesting a new employee account.
- Requesting access to an approved shared folder.
- Requesting installation of approved software.
- Requesting a replacement workstation.
- Requesting a Microsoft 365 license.

## 5.1 Service Request vs. Incident

| Service Request | Incident |
|---|---|
| Employee requests a service or standard action | Employee reports an interruption or degradation |
| Typically follows a defined fulfillment workflow | Requires investigation and restoration |
| May require authorization | May require immediate troubleshooting |
| Example: Request access to an HR folder | Example: Existing HR folder access suddenly stops working |
| Example: Request approved software | Example: Installed software stops launching |

### Classification Rule

If the employee is requesting something new or an approved standard service, classify it as a service request.

If the employee reports something that is broken or unexpectedly unavailable, evaluate it as an incident.

If the submission contains both, create or link appropriate records according to the applicable workflow.

### Important

Do not classify every user contact as a service request.

Correct classification supports accurate reporting, routing, and service management.

---

# 6. Request Submission Channels

Technical Techno Tech may receive requests through approved communication channels.

## 6.1 Proposed Channels

| Channel | Description | Status |
|---|---|---|
| IT Service Portal | Employee submits a structured request | Planned |
| Email | Employee contacts the Service Desk | Proposed |
| Telephone | Employee requests assistance by phone | Proposed |
| In-Person | Employee contacts IT directly | Proposed |
| ITSM Platform | Technician creates or receives a request record | Platform Dependent |

## 6.2 ITSM Platform Considerations

Jira Service Management is a proposed platform for future service management exercises.

**Important:** This procedure does not claim that a service portal, Jira integration, automated routing, or notification workflow has been deployed.

## 6.3 Channel Requirements

Regardless of the submission channel:

1. The request must be documented.
2. The requester must be identified.
3. The requested service must be understood.
4. Relevant information must be collected.
5. The request must receive a unique reference.
6. Ownership must be established.

---

# 7. Request Logging Workflow

## 7.1 High-Level Workflow

```text
Employee Submits Request
          |
          v
Service Desk Receives Request
          |
          v
Identify Requester
          |
          v
Review Request Description
          |
          v
Check for Existing Record
          |
          v
Determine Request Type
          |
          v
Is Information Complete?
       /        \
      No        Yes
      |          |
      v          v
Request       Categorize
Clarification  Request
      |          |
      v          v
Update       Identify Approval
Record       Requirements
      |          |
      +-----+----+
            |
            v
Assign Request Owner
            |
            v
Record Request Details
            |
            v
Acknowledge Request
            |
            v
Assessment and Authorization
```

## 7.2 Procedure Boundaries

This SOP ends when:

- The request has been recorded.
- Required information has been collected or identified as missing.
- The request has been appropriately classified.
- Ownership has been assigned.
- Authorization requirements have been flagged.
- The requester has been acknowledged.
- The request is ready for the next applicable activity.

Actual approval and fulfillment are handled by separate procedures.

---

# 8. Step 1 — Receive the Request

## 8.1 Objective

Capture the initial request through an approved communication channel.

## 8.2 Procedure

1. Receive the employee's request.
2. Record the submission channel.
3. Record the date and time received.
4. Identify the employee submitting the request.
5. Review the initial description.
6. Determine whether immediate clarification is required.

## 8.3 Required Information

| Field | Description |
|---|---|
| Submission Date | Date the request was received |
| Submission Time | Time the request was received |
| Submission Channel | Email, portal, telephone, or other |
| Requester | Person submitting the request |
| Request Summary | Short description of the requested service |
| Request Description | Detailed explanation of the request |

## 8.4 Example

**Scenario:** An HR employee requests access to an approved departmental shared folder.

**Request Summary:** Shared HR Folder Access

**Description:**

The employee requests access to the HR shared folder to perform assigned responsibilities.

**Classification:** Illustrative Scenario — Not an Actual Submitted Request

---

# 9. Step 2 — Identify the Requester

## 9.1 Objective

Establish who submitted the request and who will receive the requested service.

## 9.2 Required Requester Information

| Field | Description |
|---|---|
| Requester Name | Employee submitting the request |
| Requester Username | Corporate username, where applicable |
| Department | Employee's department |
| Contact Information | Approved contact method |
| Affected User | Person receiving the requested service |
| Manager | Manager or designated authority, if relevant |

## 9.3 Procedure

1. Identify the requester.
2. Record the requester information.
3. Determine whether the request is for the requester or another employee.
4. Verify identity using an approved method when required.
5. Record the verification status without exposing sensitive authentication information.

## 9.4 Identity Verification

**Identity Verification Required:** [Yes / No / To Be Determined]

**Verification Method:** [Approved Method]

**Verification Status:** [Verified / Pending / Not Required]

### Security Requirements

Do not request or record:

- Passwords
- MFA recovery codes
- Authentication tokens
- Private keys
- Security question answers

### Important

An employee's ability to submit a request does not establish authorization to receive the requested access.

Identity verification and access authorization are separate controls.

---

# 10. Step 3 — Review the Request Description

## 10.1 Objective

Determine what the employee needs and whether the request is understandable.

## 10.2 Review Questions

- What service is being requested?
- Who needs the service?
- Why is the service needed?
- Which system or resource is involved?
- Is the request for a new service or an existing service problem?
- Is a deadline specified?
- Is the requested service available?
- Does the request require approval?
- Is any important information missing?

## 10.3 Information Quality

A complete request should be:

- Clear
- Specific
- Actionable
- Relevant
- Sufficiently detailed
- Free from unnecessary sensitive information

## 10.4 Incomplete Requests

If information is missing:

1. Record the information already provided.
2. Identify the missing details.
3. Contact the requester.
4. Document the clarification request.
5. Update the record when the requester responds.
6. Continue processing when sufficient information is available.

**Suggested Status:** Awaiting Requester Information

### Important

Do not invent missing information to complete a request record.

---

# 11. Step 4 — Check for Duplicate Requests

## 11.1 Objective

Prevent unnecessary duplicate work and maintain accurate service request records.

## 11.2 Procedure

1. Search existing request records.
2. Compare requester information.
3. Compare the requested service.
4. Compare the affected user or resource.
5. Review open or recently completed requests.
6. Determine whether the new submission duplicates an existing request.

## 11.3 Duplicate Indicators

- Same requester
- Same requested service
- Same affected resource
- Similar submission time
- Same business justification
- Existing unresolved request

## 11.4 Duplicate Handling

If a duplicate is identified:

1. Confirm that both submissions represent the same request.
2. Link or consolidate records when the ITSM tool supports it.
3. Preserve relevant information.
4. Inform the requester of the existing reference.
5. Avoid performing the same fulfillment action twice.

**Important:** Similar requests from different employees are not necessarily duplicates.

---

# 12. Step 5 — Classify the Request

## 12.1 Objective

Assign the request to the correct service and request category.

## 12.2 Request Categories

| Category | Example |
|---|---|
| Identity & Access | New account, group membership, shared folder access |
| Endpoint Management | Device provisioning, approved software installation |
| Microsoft 365 | License assignment, collaboration access |
| Networking | New network access or approved connectivity configuration |
| Server Services | Standard server resource request |
| Information Security | Approved security-related service request |
| Employee Lifecycle | Onboarding, role change, offboarding |

## 12.3 Service Catalog Mapping

| Service ID | Service |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

## 12.4 Classification Procedure

1. Identify the requested service.
2. Review the Service Catalog.
3. Select the appropriate service category.
4. Identify the request type.
5. Determine whether a standard fulfillment procedure exists.
6. Record the classification.

### Example

**Request:** Employee requests access to an HR shared folder.

**Service:** IT-SVC-001 — Identity & Access Management

**Category:** Access Request

**Request Type:** Shared Folder Access

**Authorization Required:** To Be Assessed

---

# 13. Step 6 — Determine Initial Priority

## 13.1 Objective

Identify the relative urgency and business importance of the request.

## 13.2 Priority Considerations

Consider:

- Business need
- Requested completion date
- Operational impact
- Number of affected employees
- Employee lifecycle deadlines
- Security requirements
- Available resources
- Existing service commitments

## 13.3 Proposed Request Priority Levels

| Priority | Description | Example |
|---|---|---|
| High | Time-sensitive request with significant operational consequences | Access required for an approved, imminent business-critical activity |
| Medium | Standard request with a documented business need | Approved software required for routine work |
| Low | Routine request with limited urgency | Nonessential software or equipment request |

These are proposed prioritization guidelines, not established service level commitments.

## 13.4 Priority Procedure

1. Review the business justification.
2. Identify relevant deadlines.
3. Assess operational impact.
4. Consider existing request commitments.
5. Assign an initial priority.
6. Record the reason for the decision.
7. Escalate uncertainty when necessary.

### Important

Requester seniority alone does not determine priority.

Service request priority is also distinct from incident priority.

---

# 14. Step 7 — Identify Authorization Requirements

## 14.1 Objective

Determine whether the requested service requires approval before fulfillment.

## 14.2 Requests That May Require Authorization

- Access to restricted folders
- Privileged account creation
- Security group membership changes
- Software purchases
- License assignments
- Hardware purchases
- Sensitive data access
- Changes to security configurations
- Requests submitted on behalf of another employee

## 14.3 Authorization Assessment

| Field | Value |
|---|---|
| Authorization Required | Yes / No / Pending |
| Approval Authority | [Role] |
| Approval Status | Not Yet Evaluated |
| Supporting Policy | [Reference] |
| Approval Evidence | Not Available |

## 14.4 Procedure

1. Review the request category.
2. Check applicable service requirements.
3. Identify whether approval is necessary.
4. Record the required approving role.
5. Flag the request for assessment and authorization.
6. Do not perform restricted fulfillment actions.

### Important

Request Logging identifies authorization requirements.

It does not replace the authorization process.

Do not assume that a request submitted by a manager is automatically approved.

---

# 15. Step 8 — Assign Request Ownership

## 15.1 Objective

Ensure that each request has a clearly identified owner responsible for coordinating its progress.

## 15.2 Assignment Considerations

- Service category
- Required technical skills
- Administrative permissions
- Current workload
- Service ownership
- Security restrictions
- Escalation requirements

## 15.3 Assignment Procedure

1. Identify the appropriate fulfillment function.
2. Determine the responsible role.
3. Assign a request owner.
4. Record the assignment.
5. Identify any required escalation.
6. Confirm the next action.

## 15.4 Example Assignment

| Request Type | Potential Responsible Role |
|---|---|
| Standard Account Request | Service Desk or Identity Administrator |
| Restricted Access Request | Authorized Identity Administrator |
| Software Installation | Endpoint Support |
| Microsoft 365 License Request | Microsoft 365 Administrator |
| Network Access Request | Network Administrator |
| Hardware Provisioning | Endpoint Support |

These are illustrative assignments.

Actual responsibility depends on organizational policies, access permissions, and staffing.

---

# 16. Step 9 — Create the Service Request Record

## 16.1 Objective

Create a traceable record containing the information needed to process the request.

## 16.2 Required Record Fields

| Field | Requirement |
|---|---|
| Request ID | Required |
| Request Summary | Required |
| Request Description | Required |
| Requester | Required |
| Affected User | Required when applicable |
| Department | When applicable |
| Submission Date/Time | Required |
| Submission Channel | Required |
| Service ID | Required |
| Request Category | Required |
| Initial Priority | Required |
| Request Owner | Required |
| Authorization Requirement | Required |
| Request Status | Required |
| Business Justification | When applicable |
| Requested Completion Date | When applicable |
| Related CI | When applicable |
| Related Records | When applicable |

## 16.3 Record Identifier

Use the request identifier generated by the selected ITSM platform.

For standalone GitHub lab documentation, use:

```text
SR-###
```

Example:

```text
SR-001
```

### Important

GitHub documentation identifiers are not necessarily identical to ticket identifiers assigned by an ITSM platform.

Where both exist, record the relationship between them.

## 16.4 Record Creation Procedure

1. Open the selected ITSM platform or documentation template.
2. Create a new service request record.
3. Assign or capture the unique identifier.
4. Enter requester information.
5. Enter the request summary and description.
6. Select the service and request category.
7. Record the initial priority.
8. Record authorization requirements.
9. Assign request ownership.
10. Save the record.
11. Confirm that the information was retained.

## 16.5 GitHub Record Template

Use:

[Service Request Template](../../Templates/Service-Request-Template.md)

Store documented scenarios or records in the appropriate repository location.

**Important:** Do not claim that a request exists in Jira unless the record was actually created in that platform.

---

# 17. Step 10 — Acknowledge the Request

## 17.1 Objective

Confirm that the request has been received and provide the requester with a reference.

## 17.2 Acknowledgment Information

An acknowledgment should include:

- Confirmation of receipt
- Request reference
- Summary of the requested service
- Current status
- Next expected action
- Any required clarification

## 17.3 Example Acknowledgment

**Subject:** Service Request SR-001 — Shared Folder Access

Hello,

Your request for access to the HR shared folder has been received and recorded as SR-001.

The request is pending assessment of the applicable access requirements.

You will be contacted if additional information or authorization is required.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 17.4 Procedure

1. Confirm the request record exists.
2. Verify the request reference.
3. Review the acknowledgment for accuracy.
4. Send the acknowledgment through the approved channel.
5. Record the communication when applicable.

### Important

Do not promise a fulfillment date unless an applicable commitment has been established.

---

# 18. Request Status Management

## 18.1 Proposed Statuses

| Status | Description |
|---|---|
| New | Request received but not fully reviewed |
| Awaiting Information | Additional details required |
| Logged | Request documented and classified |
| Pending Assessment | Awaiting evaluation |
| Pending Approval | Authorization required |
| Approved | Required authorization obtained |
| In Progress | Fulfillment underway |
| Pending Verification | Fulfillment awaiting confirmation |
| Completed | Fulfillment completed |
| Closed | Final closure activities completed |
| Rejected | Request not authorized or accepted |
| Cancelled | Request withdrawn or cancelled |

## 18.2 Logging Stage Statuses

The statuses most relevant to this procedure are:

- New
- Awaiting Information
- Logged
- Pending Assessment

## 18.3 Status Requirements

- Record the current status.
- Update the status when conditions change.
- Document significant transitions.
- Identify who is responsible for the next action.

### Important

Status names may differ between Jira Service Management and GitHub documentation.

Use the configured platform's actual status values and map them to the conceptual workflow where necessary.

---

# 19. Logging Quality Verification

Before transferring the request to assessment or fulfillment, verify that the record contains sufficient information.

## 19.1 Verification Checklist

- [ ] Requester identified
- [ ] Affected user identified where applicable
- [ ] Submission channel recorded
- [ ] Submission date/time recorded
- [ ] Request summary clear
- [ ] Request description sufficient
- [ ] Duplicate request check completed
- [ ] Request correctly classified
- [ ] Service Catalog entry identified
- [ ] Initial priority recorded
- [ ] Authorization requirements identified
- [ ] Request owner assigned
- [ ] Unique request reference recorded
- [ ] Request acknowledged
- [ ] Current status accurate

## 19.2 Incomplete Records

If required information is missing:

1. Record the missing fields.
2. Set an appropriate waiting status.
3. Request clarification.
4. Update the record when information is received.
5. Recheck completeness.

## 19.3 Logging Completion Criteria

Request Logging is complete when:

- A valid request record exists.
- The request is understandable.
- The appropriate service has been identified.
- Required assessment information is available or explicitly pending.
- Authorization requirements are flagged.
- Responsibility is assigned.
- The requester has been acknowledged.

---

# 20. Handoff to Request Assessment and Authorization

## 20.1 Handoff Objective

Transfer the request to the next applicable activity without losing context.

## 20.2 Required Handoff Information

| Information | Requirement |
|---|---|
| Request ID | Required |
| Requester | Required |
| Requested Service | Required |
| Business Justification | When applicable |
| Service Category | Required |
| Priority | Required |
| Authorization Requirement | Required |
| Request Owner | Required |
| Supporting Documentation | When applicable |

## 20.3 Handoff Procedure

1. Confirm logging completeness.
2. Identify outstanding clarification requirements.
3. Confirm request ownership.
4. Update the request status.
5. Route the request for assessment.
6. Preserve the request history.

### Next Procedure

`Request-Assessment-and-Authorization.md`

**Status:** Planned Procedure

### Important

Some predefined, low-risk requests may not require a separate approval.

However, the request must still meet the applicable fulfillment requirements.

---

# 21. Practical Lab Example

## 21.1 Scenario

**Scenario ID:** SCN-###  
**Scenario Type:** Service Request  
**Service:** IT-SVC-001 — Identity & Access Management  
**Request Type:** Shared Folder Access  
**Environment:** Active Directory Lab  
**Classification:** Proposed Simulation

### Business Context

An employee in the HR department requests access to a departmental shared folder.

The Service Desk is responsible for recording the request and identifying any required authorization.

## 21.2 Example Lab Environment

| Component | Example Configuration |
|---|---|
| Domain | homelab.local |
| Domain Controller | DC01 |
| Secondary Domain Controller | DC02 |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Identity Platform | Active Directory Domain Services |

These components reflect the intended lab context.

Their availability and current configuration should be verified before performing the scenario.

## 21.3 Example Request Information

| Field | Example |
|---|---|
| Request ID | SR-001 |
| Requester | HR Employee |
| Requested Service | Shared Folder Access |
| Service ID | IT-SVC-001 |
| Request Category | Access Request |
| Resource | HR Shared Folder |
| Business Justification | Departmental work |
| Priority | To Be Assessed |
| Authorization | Pending Assessment |
| Request Owner | Service Desk |
| Status | New |

## 21.4 Lab Tasks

1. Create a simulated employee request.
2. Identify the requester.
3. Document the requested resource.
4. Determine the service category.
5. Check whether the request represents an incident.
6. Identify the potential approval requirement.
7. Assign request ownership.
8. Create the request record.
9. Record the acknowledgment.
10. Prepare the request for assessment.

## 21.5 Expected Learning Outcomes

- Distinguish service requests from incidents.
- Apply consistent request classification.
- Record employee requests accurately.
- Identify potential authorization requirements.
- Establish request ownership.
- Maintain traceable documentation.
- Prepare requests for subsequent fulfillment.

## 21.6 Evidence to Capture

- Service request record
- Request category
- Initial priority
- Authorization requirement
- Request owner
- Request status
- Acknowledgment record

### Important

This is an example scenario, not evidence of completed lab activity.

Actual execution details and screenshots should be added only after performing the exercise.

---

# 22. Common Logging Errors

| Error | Potential Consequence | Prevention |
|---|---|---|
| Incorrect classification | Wrong workflow or assignment | Confirm request type |
| Missing requester information | Delayed clarification | Validate identity fields |
| Incomplete description | Fulfillment errors | Request additional details |
| Duplicate request | Repeated work | Check existing records |
| Incorrect service category | Misrouting | Reference Service Catalog |
| Unsupported priority | Inconsistent handling | Document priority rationale |
| Missing authorization flag | Unauthorized fulfillment risk | Check approval requirements |
| Unassigned request | Ownership ambiguity | Assign a responsible role |
| Missing acknowledgment | Poor communication | Confirm receipt |
| Sensitive data in ticket | Information exposure | Follow security requirements |

---

# 23. Metrics and Performance Measurement

Request Logging can be evaluated using service metrics.

## 23.1 Proposed Metrics

| Metric | Description | Potential Measurement |
|---|---|---|
| Request Logging Time | Time from receipt to completed logging | Minutes |
| Request Classification Accuracy | Percentage correctly classified | Percentage |
| Request Record Completeness | Percentage containing required fields | Percentage |
| Duplicate Request Rate | Percentage identified as duplicates | Percentage |
| Request Acknowledgment Time | Time from receipt to acknowledgment | Minutes |
| Requests Awaiting Information | Requests delayed by missing details | Count |

## 23.2 Example Metric Definition

**Metric:** Request Record Completeness

**Formula:**

```text
Request Record Completeness (%) =

Complete Request Records
------------------------ x 100
Total Evaluated Requests
```

**Baseline:** Not Yet Established

**Target:** Not Yet Established

**Actual Result:** Not Yet Measured

## 23.3 Measurement Requirements

- Define required record fields.
- Establish a measurement period.
- Identify the data source.
- Review actual request records.
- Apply a consistent calculation.
- Preserve supporting evidence.
- Document limitations.

### Related Documentation

[Service Metrics Documentation Standards](../../Continual-Improvement/Service-Metrics/README.md)

[Service Metric Template](../../Templates/Service-Metric-Template.md)

### Important

No service performance targets, automated measurements, or achieved results are claimed by this SOP.

---

# 24. Security and Compliance Considerations

## 24.1 Sensitive Information

Service request records may contain:

- Employee identity information
- Department information
- Access requirements
- Device information
- Internal resource names
- Business justifications

## 24.2 Security Requirements

- Use approved request channels.
- Verify identity when required.
- Apply least-privilege access.
- Limit access to sensitive records.
- Do not collect passwords.
- Do not store authentication secrets.
- Identify privileged access requests.
- Preserve authorization evidence.
- Sanitize documentation before publication.

## 24.3 Access Request Considerations

For requests involving access to restricted resources:

1. Identify the requested resource.
2. Identify the affected user.
3. Record the business justification.
4. Identify the resource owner or appropriate authority.
5. Flag the request for authorization.
6. Do not grant access during logging.

## 24.4 Portfolio Requirements

When documenting simulated requests:

- Use fictional employee information.
- Remove confidential data.
- Distinguish simulated approvals from real authorization.
- Avoid publishing credentials or sensitive configurations.

---

# 25. Records and Evidence

## 25.1 Required Records

A completed logging activity should produce:

- A service request record
- Request classification
- Initial priority
- Request ownership
- Authorization requirement
- Current request status
- Acknowledgment documentation

## 25.2 Supporting Evidence

| Evidence Type | Purpose |
|---|---|
| Ticket Screenshot | Demonstrate request record creation |
| Request Record | Document request information |
| Classification Record | Show selected service and category |
| Assignment Record | Demonstrate ownership |
| Communication Record | Document acknowledgment |
| Request History | Demonstrate traceability |

## 25.3 Evidence Integrity

Do not fabricate:

- Submitted requests
- ITSM tickets
- Requester communications
- Authorization decisions
- Ticket timestamps
- Assigned technicians
- Fulfillment activities

Simulated evidence must be clearly labeled.

---

# 26. Continual Improvement

## 26.1 Improvement Opportunities

Potential improvements include:

- Standardized request forms
- Required field validation
- Service Catalog integration
- Automated categorization
- Duplicate detection
- Automated acknowledgment
- Improved routing
- Knowledge article recommendations
- Request trend analysis

## 26.2 Improvement Procedure

1. Identify a logging inefficiency.
2. Document supporting observations.
3. Evaluate the operational impact.
4. Propose an improvement.
5. Record the opportunity.
6. Assess feasibility and risk.
7. Implement authorized improvements.
8. Measure the results.
9. Update this SOP when necessary.

## 26.3 Related Documentation

[Improvement Management SOP](../../Continual-Improvement/Procedures/Improvement-Management.md)

[Improvement Register](../../Continual-Improvement/Improvement-Register.md)

[Improvement Template](../../Templates/Improvement-Template.md)

---

# 27. Procedure Quality Checklist

## Process Definition

- [ ] Purpose documented
- [ ] Scope established
- [ ] Responsibilities defined
- [ ] Submission channels identified
- [ ] Request classification explained
- [ ] Logging workflow documented
- [ ] Handoff requirements established

## Operational Requirements

- [ ] Requester identification covered
- [ ] Request information requirements defined
- [ ] Duplicate handling documented
- [ ] Priority assessment included
- [ ] Authorization requirements addressed
- [ ] Ownership assignment included
- [ ] Acknowledgment process defined
- [ ] Logging completion criteria established

## Security Requirements

- [ ] Sensitive information handling addressed
- [ ] Identity verification considerations included
- [ ] Access authorization separated from logging
- [ ] Least-privilege principles respected
- [ ] Portfolio sanitization requirements documented

## Lab Readiness

- [ ] Example scenario included
- [ ] Expected tasks identified
- [ ] Evidence requirements documented
- [ ] Simulated activities clearly labeled
- [ ] No fabricated execution results

## Documentation Quality

- [ ] SOP identifier correct
- [ ] Version recorded
- [ ] Related procedures referenced
- [ ] Relative links verified
- [ ] Revision history maintained

---

# 28. Document Review and Revision History

## 28.1 Review Triggers

Review this SOP when:

- Request submission channels change.
- New services are added to the Service Catalog.
- Request categories change.
- Authorization requirements change.
- ITSM platform workflows change.
- Security requirements are updated.
- Ticket quality reviews identify issues.
- Continual improvement initiatives introduce new procedures.

## 28.2 Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Request Logging SOP aligned with ITIL 4 Service Request Management |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This SOP establishes a proposed standard for receiving, validating, classifying, recording, and acknowledging employee IT service requests within a simulated corporate environment.

Organizational roles, request scenarios, communication channels, approval requirements, and service workflows may be fictional or proposed.

Actual ticket creation, requester communication, platform configuration, technical fulfillment, and verification results must be supported by documented lab evidence.

Jira Service Management and associated automation capabilities are planned unless implementation and verification are explicitly documented.

Simulated employee requests and organizational decisions must not be represented as real production activity or professional employment experience.

This procedure demonstrates service request intake, classification, ownership, documentation, security awareness, and preparation for assessment and fulfillment.
