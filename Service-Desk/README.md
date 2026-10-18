# Technical Techno Tech — Service Desk

## Overview

The Service Desk serves as the **primary point of contact** between employees and the Internal IT Department at Technical Techno Tech (TTT), a fictional technology solutions company.

The Service Desk provides a **centralized function for receiving, recording, coordinating, and communicating IT support requests and service-related issues**.

It supports employees across the organization's business divisions, including Information Technology, Software Development, Web Development, Game Development, and other business departments.

The Service Desk operates using ITIL-aligned practices to support consistent service delivery, effective communication, and efficient IT operations.

## Purpose

The purpose of the Service Desk is to provide employees with a reliable and accessible point of contact for IT assistance.

Primary objectives include:

- Provide a centralized point of contact for IT support.
- Receive and document employee issues and service requests.
- Perform initial troubleshooting and technical assistance.
- Categorize and prioritize incoming tickets.
- Resolve issues within the Service Desk's capabilities.
- Escalate issues requiring specialized technical expertise.
- Communicate ticket status and progress to employees.
- Coordinate support activities across IT teams.
- Maintain accurate support documentation.
- Promote consistent and professional customer service.

The Service Desk focuses on effective communication and support coordination while working closely with other IT management practices.

## Scope of Service Desk Operations

### In Scope

The Service Desk supports activities including:

- Employee technical assistance
- Windows workstation troubleshooting
- Account and authentication support
- Password resets and account unlocks
- Microsoft 365 application assistance
- Basic network connectivity troubleshooting
- Software installation assistance
- Remote technical support
- Ticket intake and documentation
- Ticket categorization and prioritization
- Initial incident diagnosis
- Service request coordination
- Technical escalation
- Employee communication and follow-up

### Out of Scope

The Service Desk does not independently perform activities requiring authorization or expertise beyond its assigned responsibilities.

Examples include:

- Unauthorized infrastructure modifications
- Unapproved privileged access assignments
- Major server or network architecture changes
- Security policy changes without authorization
- Specialized engineering work outside Service Desk responsibilities

These activities are coordinated with the appropriate IT personnel and management practices.

## Service Desk Responsibilities

### 1. Single Point of Contact

The Service Desk provides employees with a consistent channel for reporting technical issues and requesting assistance.

Responsibilities include:

- Receiving employee contacts
- Identifying the affected user or service
- Gathering relevant information
- Recording support interactions
- Directing requests to the appropriate workflow

### 2. Ticket Management

The Service Desk records and manages support tickets throughout their lifecycle.

Responsibilities include:

- Creating tickets
- Assigning categories
- Assessing impact and urgency
- Setting priorities
- Assigning responsible personnel
- Updating ticket status
- Documenting troubleshooting and communication
- Coordinating escalation
- Confirming resolution or fulfillment
- Closing tickets according to established procedures

### 3. Initial Troubleshooting

Service Desk technicians perform initial diagnosis and troubleshooting for supported technologies.

Examples include:

- Verifying user account status
- Checking network connectivity
- Reviewing workstation configuration
- Investigating application errors
- Checking service availability
- Performing authorized password resets
- Using remote support tools
- Consulting existing knowledge articles

### 4. Employee Communication

The Service Desk maintains communication with affected employees throughout support activities.

Responsibilities include:

- Acknowledging reported issues
- Providing ticket references
- Explaining troubleshooting steps
- Communicating expected next actions
- Providing progress updates
- Explaining resolutions in understandable language
- Confirming successful service restoration or request fulfillment

### 5. Escalation & Coordination

The Service Desk coordinates support with specialized IT personnel when an issue cannot be resolved at the initial support level.

Escalation may involve:

- Systems Administration
- Network Administration
- Endpoint Administration
- Microsoft 365 Administration
- Information Security
- External technology vendors, when applicable

The Service Desk may continue to coordinate communication and track progress after escalation.

## Support Channels

Technical Techno Tech's emulated Service Desk may receive employee requests through the following channels:

| Support Channel | Purpose | Implementation Status |
|---|---|---|
| Jira Service Management Portal | Centralized ticket submission and tracking | Planned / In Development |
| Email | Employee support requests and communication | Planned |
| Chat | Direct communication and troubleshooting | Simulated |
| Monitoring Alerts | Automated detection of technical events | Planned |

The availability of these channels will be updated as the environment develops.

## Service Desk Ticket Workflow

### 1. Contact & Intake

An employee contacts the Service Desk to report an issue or request an IT service.

The technician gathers relevant information, including:

- Employee or requester
- Department
- Affected device or application
- Description of the issue or request
- Business impact
- Relevant error messages
- Time the issue began, if applicable

### 2. Logging & Classification

The interaction is documented in the IT service management platform.

The technician determines whether the issue should be handled as:

- An incident
- A service request
- A security-related report
- Another appropriate IT management activity

### 3. Prioritization

The technician evaluates the business impact and urgency of the issue.

Priority is assigned according to the organization's established [prioritization procedure](./Procedures/Ticket-Prioritization.md).

### 4. Initial Diagnosis & Assistance

The Service Desk performs authorized troubleshooting or request-handling activities.

Existing knowledge articles and operational procedures should be consulted when appropriate.

### 5. Resolution, Fulfillment, or Escalation

If the Service Desk can resolve the issue or fulfill the request within its authority, it proceeds with the appropriate actions.

Otherwise, the ticket is assigned or escalated to the responsible IT personnel.

### 6. Validation & Communication

The technician verifies the outcome and communicates the results to the employee.

Validation may include:

- Confirming that the affected service functions correctly
- Verifying successful account access
- Testing application functionality
- Confirming successful request fulfillment
- Obtaining employee confirmation when appropriate

### 7. Closure

The ticket is closed after the applicable resolution or fulfillment criteria are satisfied.

Documentation should include:

- Actions performed
- Final outcome
- Relevant technical findings
- User communication
- Related records or knowledge articles

## Ticket Classification

The Service Desk distinguishes between different types of IT work.

| Classification | Description | Example |
|---|---|---|
| Incident | An unplanned interruption or reduction in the quality of an IT service | Employee cannot access a previously working shared drive |
| Service Request | A request for a predefined service or resource | Employee requests access to a shared folder |
| Security Report | A report of suspicious activity or a potential security issue | Employee reports a suspicious email |
| General Inquiry | A request for information or guidance | Employee asks how to use an approved application |

Security reports are assessed and routed according to the appropriate security and incident response procedures.

## Ticket Prioritization

Ticket priority is determined by evaluating business impact and urgency.

### Impact

- **High:** Critical business services or many employees are affected.
- **Medium:** A department, multiple employees, or an important business function is affected.
- **Low:** Limited disruption affecting an individual or noncritical service.

### Urgency

- **High:** Immediate attention is required.
- **Medium:** Timely action is necessary.
- **Low:** The issue can be addressed through normal support scheduling.

### Example Priority Matrix

| Impact / Urgency | High Urgency | Medium Urgency | Low Urgency |
|---|---|---|---|
| High Impact | P1 | P2 | P3 |
| Medium Impact | P2 | P3 | P4 |
| Low Impact | P3 | P4 | P4 |

### Priority Definitions

| Priority | Description |
|---|---|
| P1 — Critical | Severe disruption requiring immediate coordination |
| P2 — High | Significant business impact requiring prompt attention |
| P3 — Medium | Moderate disruption handled through normal support processes |
| P4 — Low | Limited impact or low-urgency issue |

Actual response targets and escalation rules will be established as Service Desk procedures are developed.

## Support Levels & Escalation

Technical Techno Tech uses a emulated tiered support structure to demonstrate realistic IT responsibilities.

| Support Level | Primary Responsibilities |
|---|---|
| Tier 1 — Service Desk | Ticket intake, initial troubleshooting, password resets, basic endpoint and application support |
| Tier 2 — Technical Support | Advanced workstation troubleshooting, endpoint administration, complex account and application issues |
| Tier 3 — Systems & Infrastructure | Windows Server, Active Directory, networking, infrastructure, and complex technical problems |

### Escalation Criteria

Escalation may be necessary when:

- The issue exceeds the technician's technical capabilities.
- Required administrative permissions are unavailable.
- The incident affects critical business services.
- Initial troubleshooting does not restore service.
- Specialized infrastructure changes are required.
- A security concern requires additional investigation.
- The issue requires coordination with another technical team.

### Escalation Documentation

Escalated tickets should include:

- Description of the issue
- Business impact and priority
- Troubleshooting already performed
- Relevant error messages and evidence
- Current findings
- Reason for escalation
- Actions required from the receiving team

**Note:** Support tiers represent emulated responsibilities and do not imply that separate employees or teams are currently operating the lab.

## Supported IT Services

The Service Desk provides assistance for the internal IT services documented in the company's Service Catalog.

| Service ID | IT Service | Service Desk Responsibilities |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Account assistance, password resets, access request coordination |
| IT-SVC-002 | Endpoint Management | Workstation troubleshooting, software support, device assistance |
| IT-SVC-003 | Microsoft 365 & Collaboration | Application support, account assistance, license request coordination |
| IT-SVC-004 | Network Connectivity | Basic connectivity troubleshooting and network support coordination |
| IT-SVC-005 | Server & Infrastructure Services | Service issue reporting and infrastructure escalation |
| IT-SVC-006 | Information Security | Security report intake, MFA assistance, security escalation |
| IT-SVC-007 | Employee IT Lifecycle | Onboarding, offboarding, and employee change coordination |

**Reference:** [IT Service Catalog](../Service-Catalog.md)

## IT Service Management Tools

The following technologies support or may support Service Desk operations.

### Jira Service Management

Intended as the primary IT service management platform for:

- Ticket intake and tracking
- Incident management workflows
- Service request fulfillment
- Ticket assignment and escalation
- Employee communication
- Automation
- Reporting

### Remote Support Tools

Examples include:

- Microsoft Quick Assist
- Windows Remote Desktop, where authorized
- Other approved remote administration tools

### Administrative & Diagnostic Tools

- Active Directory Users and Computers (ADUC)
- Active Directory Administrative Center (ADAC)
- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Windows Event Viewer
- PowerShell
- Windows networking utilities

Tool availability and usage depend on the emulated environment and assigned permissions.

## Knowledge Management Integration

The Service Desk uses Knowledge Management to improve troubleshooting consistency and reduce repeated investigation.

Knowledge articles may provide:

- Step-by-step troubleshooting instructions
- Password reset procedures
- Account administration guidance
- Application support instructions
- Network diagnostic procedures
- Common error resolutions

Technicians should consult relevant knowledge articles before repeating previously documented troubleshooting work.

When new technical information is discovered, the Service Desk may recommend creating or updating a knowledge article.

**Reference:** [Knowledge Management](../Knowledge-Management/)

## ITIL Management Practice Relationships

The Service Desk works alongside other ITIL-aligned management practices such as:
- Incident Management
- Service Request Management
- Knowledge Management
- Problem Management
- Change Enablement
- Monitoring and Event Management
- Service Configuration Management
- Information Security Management
- Continual Improvement

The Service Desk is a point of contact and coordination function, not a mandatory approval stage for every IT activity.

## Service Desk Procedures

Standardized procedures establish consistent support practices.

| Procedure | Purpose |
|---|---|
| [Ticket Intake](Procedures/Ticket-Intake.md) | Defines how employee contacts are received and documented |
| [Ticket Categorization](Procedures/Ticket-Categorization.md) | Defines how tickets are classified |
| [Ticket Prioritization](Procedures/Ticket-Prioritization.md) | Defines how impact, urgency, and priority are assessed |
| [Ticket Escalation](Procedures/Ticket-Escalation.md) | Defines escalation requirements and responsibilities |

Procedures will be developed and tested as the Service Desk environment evolves.

## Service Desk Records

The [`Records/` directory](./Records/) contains supporting records of Service Desk activities that are not already documented in another management practice.

Examples may include:

- General support interactions
- Ticket intake exercises
- Customer communication exercises
- Service Desk operational reviews
- Ticket classification and routing exercises

Detailed incident investigations are maintained under Incident Management.

Service request fulfillment records are maintained under Service Request Management.

This separation reduces duplicate documentation while preserving links between related activities.

### Directory Structure

```text id="x9m4bk"
Service-Desk/
├── README.md
├── Procedures/
│   ├── Ticket-Intake.md
│   ├── Ticket-Categorization.md
│   ├── Ticket-Prioritization.md
│   └── Ticket-Escalation.md
└── Records/
```

## Service Desk Performance & Improvement

Service Desk performance may be evaluated using operational metrics such as:

| Metric | Purpose |
|---|---|
| Ticket Volume | Measures the number of support interactions |
| First Contact Resolution Rate | Measures issues resolved during the initial support interaction |
| Average Resolution Time | Tracks time required to resolve incidents |
| Request Fulfillment Time | Tracks time required to complete service requests |
| Escalation Rate | Measures the proportion of tickets requiring escalation |
| Reopened Tickets | Identifies issues requiring additional support |
| User Satisfaction | Evaluates the employee support experience |

Metrics will be introduced as sufficient ticket data becomes available.

Findings may support improvement initiatives documented under [Continual Improvement](../10-Continual-Improvement/).

## Documentation Standards

Service Desk documentation should:

1. Clearly identify the reported issue or request.
2. Record relevant user and service information.
3. Document troubleshooting and support actions accurately.
4. Distinguish observed facts from assumptions.
5. Record escalation decisions and outcomes.
6. Include relevant technical evidence.
7. Document user communication.
8. Verify resolution or fulfillment before closure.
9. Link related operational records when appropriate.
10. Avoid including passwords, access tokens, or sensitive information.

Documentation should be concise, professional, and understandable to other IT personnel.
