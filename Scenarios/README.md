# Technical Techno Tech — IT Operational Scenarios

## Overview

This directory contains simulated business scenarios involving the Internal IT Department at **Technical Techno Tech (TTT)**, a fictional technology solutions company.

Each scenario represents a realistic business requirement, technical challenge, or operational situation requiring IT involvement.

Scenarios demonstrate how the IT department applies technical knowledge, administrative procedures, and ITIL-aligned management practices to support business operations.

---

## Purpose

The purpose of these scenarios is to demonstrate practical IT operations within a simulated corporate environment.

Objectives include:

- Apply technical knowledge to realistic business requirements.
- Demonstrate Help Desk and Systems Administration responsibilities.
- Practice troubleshooting, infrastructure administration, and service delivery.
- Apply ITIL management practices to operational situations.
- Document technical implementation and validation.
- Demonstrate communication, documentation, and problem-solving skills.
- Connect related operational records across multiple IT management practices.

Each scenario focuses on the business requirement and overall outcome rather than duplicating detailed technical documentation.

---

## Scenario Structure

Each scenario is maintained in its own numbered directory.

```text
Scenarios/
├── README.md
├── SCN-001-Scenario-Title/
│   └── README.md
├── SCN-002-Scenario-Title/
│   └── README.md
└── SCN-003-Scenario-Title/
    └── README.md
```

Scenario documentation follows the standardized [Scenario Template](../Templates/Scenario-Template.md).

### Scenario Identification

Each scenario receives a unique identifier:

**SCN-XXX — Descriptive Scenario Title**

Examples:

- SCN-001 — Remote Employee Onboarding
- SCN-002 — Department Shared Folder Access Failure
- SCN-003 — Privileged Account Security Improvement
- SCN-004 — New Branch Office Infrastructure Deployment

These examples represent potential scenarios, not necessarily completed projects.

---

## Scenario Lifecycle

Scenarios generally follow five phases.

### 1. Initiation

A business requirement, technical issue, or operational need is identified.

Examples include:

- Human Resources requests IT onboarding for a new employee.
- An employee reports an unexpected service interruption.
- IT identifies an infrastructure security weakness.
- A department requires additional technology resources.

### 2. Assessment & Planning

IT evaluates the requirement and determines:

- Affected services and infrastructure
- Required technical activities
- Applicable ITIL management practices
- Necessary authorization
- Potential risks and dependencies

### 3. Implementation & Investigation

IT performs the technical work required to address the scenario.

Activities may include:

- Configuring Windows Server or Active Directory
- Managing Microsoft Entra ID identities
- Deploying applications through Microsoft Intune
- Troubleshooting network connectivity
- Implementing security controls
- Performing infrastructure maintenance

Detailed technical work is documented in the appropriate operational records.

### 4. Validation

IT verifies that the required outcome has been achieved.

Validation may include:

- Functional testing
- Configuration verification
- Connectivity testing
- Security verification
- Service restoration testing
- Simulated employee confirmation

### 5. Completion & Review

The scenario is reviewed and documented.

Activities may include:

- Confirming business requirements were met
- Updating operational records
- Updating infrastructure documentation
- Creating or revising knowledge articles
- Identifying opportunities for continual improvement

Not every scenario requires every phase or activity.

---

## ITIL Management Practice Integration

Scenarios may involve one or more ITIL-aligned management practices.

| Management Practice | Application Within Scenarios |
|---|---|
| Service Desk | Receives and coordinates employee support interactions. |
| Incident Management | Investigates and restores disrupted IT services. |
| Service Request Management | Fulfills predefined employee requests. |
| Knowledge Management | Provides reusable technical instructions and troubleshooting information. |
| Problem Management | Investigates underlying causes of incidents. |
| Change Enablement | Assesses, authorizes, and manages infrastructure or service changes. |
| Monitoring and Event Management | Detects and evaluates infrastructure events and alerts. |
| Service Configuration Management | Maintains information about systems and their relationships. |
| Information Security Management | Supports security requirements and protective controls. |
| Continual Improvement | Identifies opportunities to improve IT services and processes. |

**Important:** ITIL management practices are not separate departments or mandatory sequential stages.

A scenario may involve several practices simultaneously, depending on the business requirement.

---

## Operational Record Integration

Scenarios act as a central reference connecting related IT operational records.

### Example: Remote Employee Onboarding

**Business Requirement:** Human Resources requests IT resources and access for a newly hired remote employee.

Potential related activities include:

| Record Type | Example Activity |
|---|---|
| Service Request | Create employee accounts and assign appropriate access. |
| Service Request | Provision and configure the employee's workstation. |
| Change | Implement a new endpoint configuration policy, if required. |
| Configuration Item | Record the newly provisioned workstation. |
| Knowledge Article | Document reusable employee setup instructions. |

The scenario README summarizes the business situation and links to the relevant records.

The individual operational records contain detailed implementation steps, troubleshooting findings, approvals, and evidence.

**Documentation Principle:** Maintain technical details in their appropriate operational records and use scenarios to connect them without unnecessary duplication.

---

## Scenario Index

The following table tracks scenarios created within the Technical Techno Tech environment.

| Scenario ID | Scenario Title | Primary ITIL Practice | Status |
|---|---|---|---|
| SCN-001 | [Scenario Title] | [Management Practice] | Planned |
| SCN-002 | [Scenario Title] | [Management Practice] | Planned |

Update this table as scenarios are created. Remove placeholder entries until actual scenarios exist.

### Scenario Status Definitions

- **Planned:** Scenario identified but work has not started.
- **In Progress:** Technical or operational work is underway.
- **Completed:** Business requirements and applicable validation activities are complete.
- **Partially Completed:** Some requirements were fulfilled, but outstanding work remains.
- **Cancelled:** Scenario discontinued before completion.

---

## Supporting Technologies

Scenarios may involve technologies deployed within Technical Techno Tech's simulated IT environment.

### Systems Administration

- Windows Server
- Active Directory Domain Services
- Group Policy
- PowerShell
- VMware

### Cloud & Endpoint Administration

- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure

### Networking

- Cisco Networking
- Cisco Packet Tracer
- OPNsense
- VyOS
- DNS, DHCP, Routing, and Switching

### IT Service Management

- Jira Service Management
- Spiceworks
- ITIL-aligned operational workflows
- Knowledge Base Documentation

Technologies are included in scenarios according to their actual implementation and relevance.

---

## Documentation Standards

Scenario documentation should:

1. Describe a realistic business requirement or operational situation.
2. Identify affected IT services and infrastructure.
3. Explain why IT involvement was necessary.
4. Identify relevant ITIL management practices.
5. Link to associated operational records.
6. Summarize technical activities without duplicating detailed records.
7. Document validation results and business outcomes.
8. Identify lessons learned and skills practiced.
9. Clearly distinguish simulated activities from hands-on technical work.
10. Maintain accurate links to related documentation.

Scenarios should be concise, organized, and understandable to both technical readers and prospective employers.

---

## Related Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Scenario Template](../Templates/Scenario-Template.md)
- [Service Desk](../Service-Desk/)
- [Incident Management](../Incident-Management/)
- [Service Request Management](../Service-Request-Management/)
- [Knowledge Management](../Knowledge-Management/)
- [Problem Management](../Problem-Management/)
- [Change Enablement](../Change-Enablement/)
- [Monitoring and Event Management](../Monitoring-and-Event-Management/)
- [Service Configuration Management](../Service-Configuration-Management/)
- [Information Security Management](../Information-Security-Management/)
- [Continual Improvement](../Continual-Improvement/)
- [Infrastructure Documentation](../Infrastructure/)

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Business requirements, employees, service requests, incidents, and operational scenarios are simulated.

Technical implementation, troubleshooting, and validation are documented based on work performed in controlled lab environments.

The scenarios demonstrate practical technical skills and IT service management knowledge, not employment experience within an actual production organization.
