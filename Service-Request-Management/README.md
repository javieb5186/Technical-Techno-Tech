# Technical Techno Tech — Service Request Management

## Overview

Service Request Management is responsible for handling predefined, user-initiated IT service requests within **Technical Techno Tech (TTT)**, a fictional technology solutions company.

The practice provides a structured approach for employees to request IT services, resources, information, and access needed to perform their responsibilities.

Service requests may involve employee onboarding, account administration, software provisioning, device configuration, access management, or other standard IT services.

Technical Techno Tech applies ITIL-aligned Service Request Management principles through simulated business requirements, hands-on technical fulfillment, authorization workflows, and structured documentation.

---

## Purpose

The purpose of Service Request Management is to ensure that employee IT requests are handled consistently, efficiently, and according to established service requirements.

Primary objectives include:

- Provide employees with a clear process for requesting IT services.
- Standardize frequently requested IT activities.
- Record and track service requests.
- Verify request eligibility and authorization.
- Fulfill requests accurately and efficiently.
- Maintain consistent employee communication.
- Protect systems and information through appropriate access controls.
- Validate successful request fulfillment.
- Maintain accurate service request records.
- Identify opportunities for automation and continual improvement.

**Key Principle:** Service Request Management focuses on fulfilling agreed, predefined requests rather than investigating unexpected service disruptions.

---

## Scope of Service Request Management

### In Scope

Service Request Management supports activities including:

- New employee onboarding
- Employee offboarding
- User account creation and modification
- Password resets and account unlocks
- Security group membership requests
- Shared folder access requests
- Microsoft 365 license assignments
- Software installation requests
- Workstation provisioning
- Device replacement requests
- Microsoft Intune application deployment requests
- Standard equipment and resource requests
- Requests for IT information or guidance

Requests must follow applicable authorization, security, and service fulfillment procedures.

### Out of Scope

Activities generally managed through other ITIL practices include:

- Unexpected service interruptions
- Investigation of recurring technical failures
- Unapproved infrastructure modifications
- Complex changes outside established request procedures
- Security incident investigations
- Proactive infrastructure monitoring

These activities are handled through Incident Management, Problem Management, Change Enablement, Information Security Management, or other appropriate practices.

---

## Service Request Definition

A **service request** is a request from a user or authorized representative that initiates a service action agreed upon as part of normal service delivery.

### Examples

| Situation | Classification |
|---|---|
| Human Resources requests IT onboarding for a new employee | Service Request |
| Employee requests access to a departmental shared folder | Service Request |
| Manager requests approved software for an employee | Service Request |
| Employee requests a password reset | Service Request |
| Employee cannot access a previously working shared folder | Incident |
| IT investigates repeated authentication failures | Problem |
| IT proposes a new organization-wide password policy | Change |

---

## Service Request Management Responsibilities

### Service Desk

The Service Desk acts as the primary contact point for employees submitting IT service requests.

Responsibilities include:

- Receiving requests
- Creating request tickets
- Verifying required information
- Categorizing requests
- Identifying applicable fulfillment procedures
- Coordinating authorization
- Performing authorized routine fulfillment
- Communicating request status
- Escalating requests when necessary
- Confirming fulfillment

### Systems Administration

Systems Administrators may fulfill requests involving:

- Active Directory account provisioning
- Organizational Unit administration
- Security group membership
- File share permissions
- Windows Server resources
- Domain-joined workstation configuration

### Endpoint Administration

Endpoint Administrators may fulfill requests involving:

- Workstation provisioning
- Microsoft Intune device enrollment
- Application deployment
- Device configuration
- Endpoint security policies

### Microsoft 365 Administration

Microsoft 365 Administrators may fulfill requests involving:

- Microsoft 365 account management
- License assignments
- Microsoft Entra ID administration
- Application access
- Supported cloud service provisioning

### Information Security

Security personnel may review requests involving:

- Privileged access
- Sensitive information
- Security exceptions
- High-risk permissions
- Access to protected systems

**Note:** These responsibilities represent simulated IT roles within the lab environment and do not imply that separate employees or teams are operating the environment.

---

## Service Request Lifecycle

Technical Techno Tech follows a structured request fulfillment workflow.

### 1. Request Submission

An employee or authorized representative submits an IT service request.

Requests may originate from:

- Jira Service Management portal
- Service Desk communication
- Email
- Simulated Human Resources requests
- Authorized management requests

### 2. Request Logging

The request is recorded in the IT service management platform.

Information collected may include:

- Request ID
- Requester
- Department
- Requested service
- Business justification
- Required resources or access
- Requested completion date
- Affected user or device
- Related service catalog entry

### 3. Request Classification

The request is categorized according to the requested service.

Examples include:

- Identity & Access Management
- Endpoint Management
- Microsoft 365
- Software Provisioning
- Employee Lifecycle
- Network Access
- Information Requests

### 4. Eligibility & Authorization

IT determines whether the request is eligible for fulfillment.

Verification may include:

- Confirming requester identity
- Reviewing access requirements
- Verifying license availability
- Checking applicable security policies
- Confirming required management approval
- Reviewing standard fulfillment procedures

Not every request requires individual approval.

Preauthorized requests may proceed directly to fulfillment when all established conditions are satisfied.

### 5. Fulfillment Planning

The assigned technician identifies:

- Required administrative tools
- Necessary permissions
- Applicable procedures
- Technical dependencies
- Security requirements
- Potential service impacts

### 6. Request Fulfillment

The technician performs the authorized actions.

Examples include:

- Creating an Active Directory user
- Assigning security group membership
- Configuring folder permissions
- Assigning a Microsoft 365 license
- Enrolling a device into Microsoft Intune
- Installing approved software
- Configuring a workstation

Actions and results should be documented in the service request record.

### 7. Validation

The technician verifies that the requested service or resource has been successfully provided.

Validation may include:

- Confirming account creation
- Verifying security group membership
- Testing resource access
- Confirming license assignment
- Verifying software installation
- Checking device enrollment
- Obtaining employee confirmation when appropriate

### 8. Communication & Closure

The requester is informed of the fulfillment outcome.

The request is closed after applicable fulfillment, validation, and documentation requirements are satisfied.

---

## Service Request Categories

Technical Techno Tech organizes requests into categories aligned with its internal IT Service Catalog.

| Service ID | Service Category | Example Requests |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Account creation, password resets, group membership |
| IT-SVC-002 | Endpoint Management | Device provisioning, software installation, device enrollment |
| IT-SVC-003 | Microsoft 365 & Collaboration | License assignment, application access |
| IT-SVC-004 | Network Connectivity | Standard network access provisioning |
| IT-SVC-005 | Server & Infrastructure Services | Approved infrastructure resource provisioning |
| IT-SVC-006 | Information Security | Standard security-related access or information requests |
| IT-SVC-007 | Employee IT Lifecycle | Onboarding, offboarding, employee transfers |

**Reference:** [IT Service Catalog](../Service-Catalog.md)

---

## Request Prioritization

Service requests are scheduled according to business needs, service agreements, dependencies, and available resources.

### Priority Considerations

Factors may include:

- Business importance
- Requested completion date
- Employee start or departure date
- Number of affected employees
- Required authorization
- Resource availability
- Security or compliance requirements

### Priority Levels

| Priority | Description | Example |
|---|---|---|
| P1 — Critical | Exceptional business-critical request requiring urgent coordination | Urgent access revocation following an employee departure |
| P2 — High | Time-sensitive business requirement | New employee starting the next business day |
| P3 — Medium | Standard request requiring normal scheduling | Approved application installation |
| P4 — Low | Nonurgent request or information inquiry | General software usage guidance |

Priority does not bypass authorization or security requirements.

---

## Request Authorization

Some service requests require authorization before fulfillment.

### Authorization Examples

| Request Type | Possible Authorization |
|---|---|
| Standard password reset | Identity verification and established procedure |
| New employee account | Authorized Human Resources or management request |
| Shared folder access | Resource owner or designated approver |
| Microsoft 365 license | License eligibility and applicable approval |
| Privileged group membership | Designated security or administrative authority |
| Approved software installation | Established software policy or designated approver |

### Authorization Documentation

Request records should identify:

- Whether approval was required
- The applicable approval authority
- Approval status
- Date of authorization, when applicable
- Any restrictions or conditions

For simulated scenarios, fictional approvals must be clearly identified as simulated.

---

## Standard Request Fulfillment

Frequently performed, low-risk requests may follow standardized fulfillment procedures.

### Examples

- Resetting a verified user's password
- Creating a standard employee account
- Assigning approved group membership
- Installing approved applications
- Provisioning a standard workstation
- Assigning an available Microsoft 365 license

### Standardization Benefits

- Reduces fulfillment time
- Improves consistency
- Reduces administrative errors
- Supports automation
- Improves documentation
- Simplifies training
- Supports predictable service delivery

Standardized fulfillment does not eliminate the need for appropriate identity verification, eligibility checks, or authorization.

---

## Employee Lifecycle Requests

Employee lifecycle management is an important Service Request Management activity.

### Employee Onboarding

Potential activities include:

1. Receive an authorized onboarding request.
2. Verify employee details and start date.
3. Create required user accounts.
4. Assign appropriate security groups.
5. Provision Microsoft 365 access.
6. Prepare and configure a workstation.
7. Apply endpoint management policies.
8. Verify access and device functionality.
9. Communicate completion.

### Employee Offboarding

Potential activities include:

1. Receive an authorized offboarding request.
2. Verify employee identity and departure requirements.
3. Disable or block account access at the authorized time.
4. Revoke active sessions where appropriate.
5. Remove unnecessary group memberships and permissions.
6. Handle license removal according to retention requirements.
7. Coordinate device return or reassignment.
8. Preserve required business data.
9. Verify access removal.
10. Document completion.

### Employee Role Changes

Potential activities include:

- Updating department information
- Modifying security group membership
- Removing access no longer required
- Assigning new role-based access
- Updating device or application requirements

Employee lifecycle activities should follow applicable security, data retention, and authorization policies.

---

## Supported Technologies

Service Request Management scenarios may involve the following technologies.

### Windows & Active Directory

- Windows Server
- Active Directory Domain Services
- Active Directory Users and Computers
- Active Directory Administrative Center
- Group Policy
- PowerShell

### Microsoft Cloud Services

- Microsoft 365 Admin Center
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure

### Endpoint Management

- Windows 11
- Microsoft Intune
- Microsoft Company Portal
- Remote Support Tools

### IT Service Management

- Jira Service Management
- Spiceworks
- Knowledge Base Documentation

Technologies are included in individual request records according to their actual use.

---

## Service Request Management Procedures

The [`Procedures/` directory](./Procedures/) contains repeatable operational instructions for handling requests.

- Request Assessment
- Request Logging
- Request Fulfillment
- Request Closure 

Procedures will be developed and updated as the simulated IT environment evolves.

---

## Service Request Records

The [`Records/` directory](./Records/) contains individual service requests and their fulfillment documentation.

Each record should include:

- Request identification
- Business requirement
- Requester information
- Requested service
- Authorization status
- Technical requirements
- Fulfillment actions
- Commands and configurations
- Validation results
- Communication
- Related documentation
- Lessons learned
- Supporting evidence

### Directory Structure

```text
03-Service-Request-Management/
├── README.md
├── Procedures/
└── Records/
    └── SR-001-Request-Title/
        ├── README.md
        └── Evidence/
```

Each request follows the standardized [Service Request Template](../Templates/Service-Request-Template.md).

### Service Request Register

| Request ID | Request Title | Service Category | Status |
|---|---|---|---|
| SR-XXX | [Request Title] | [Service Category] | [Status] |

Add requests to this register as they are documented. Remove placeholder entries until actual records exist.

---

## Integration With Other ITIL Practices

Service Request Management works alongside other ITIL-aligned management practices.

| Management Practice | Relationship to Service Request Management |
|---|---|
| Service Desk | Receives requests and coordinates employee communication |
| Incident Management | Handles unexpected interruptions rather than standard requests |
| Knowledge Management | Provides reusable fulfillment instructions |
| Problem Management | Investigates underlying causes of recurring service issues |
| Change Enablement | Manages changes requiring appropriate risk assessment and authorization |
| Monitoring and Event Management | Provides information about service and infrastructure conditions |
| Service Configuration Management | Tracks devices, systems, and services affected by fulfillment |
| Information Security Management | Supports identity verification, authorization, and access controls |
| Continual Improvement | Improves request fulfillment efficiency and quality |

Not every service request requires a separate record in another management practice.

---

## Knowledge Management Integration

Service Request Management uses Knowledge Management to provide consistent fulfillment instructions.

Examples include:

- Creating Active Directory user accounts
- Resetting passwords
- Assigning Microsoft 365 licenses
- Managing security group membership
- Enrolling Windows devices into Intune
- Installing approved applications

Reusable technical instructions should be documented in knowledge articles rather than duplicated across multiple service request records.

**Reference:** [Knowledge Management](../Knowledge-Management/)

---

## Change Enablement Integration

Some service requests may require changes to infrastructure or service configurations.

### Example

**Service Request:** A department requests access to a new shared resource.

**Standard Fulfillment:**

- Verify authorization.
- Assign access using an existing approved security group.
- Validate permissions.
- Document fulfillment.

**Potential Change Enablement Activity:**

If the request requires creating a new organization-wide access policy or modifying a shared infrastructure configuration, a separate change assessment may be appropriate.

The required process depends on the change's risk, scope, and established authorization rules.

**Reference:** [Change Enablement](../Change-Enablement/)

---

## Service Configuration Management Integration

Service requests may create, modify, or retire Configuration Items.

Examples include:

- Provisioning a new workstation
- Deploying a new server
- Assigning a managed endpoint
- Retiring an employee device
- Modifying a tracked cloud service configuration

Relevant configuration records should be updated when required.

**Reference:** [Service Configuration Management](../Service-Configuration-Management/)

---

## Information Security Integration

Security controls are important throughout the request lifecycle.

### Security Requirements

- Verify requester identity.
- Confirm appropriate authorization.
- Follow least-privilege principles.
- Avoid unnecessary privileged access.
- Protect employee and organizational information.
- Validate access assignments.
- Document sensitive administrative actions appropriately.
- Remove access when no longer required.

Requests involving privileged access or sensitive resources may require additional review.

**Reference:** [Information Security Management](../Information-Security-Management/)

---

## Request Fulfillment Automation

Standardized service requests may be suitable for automation.

Potential examples include:

- Automatically creating Jira request tickets
- Routing requests to the appropriate support queue
- Requesting approval from designated authorities
- Generating standard fulfillment checklists
- Running authorized PowerShell provisioning scripts
- Updating request status after successful validation
- Sending fulfillment notifications

Automation should include appropriate authorization, access control, error handling, and verification.

Automation opportunities will be evaluated as the simulated environment develops.

---

## Service Request Performance Metrics

Service Request Management effectiveness may be evaluated using operational metrics.

| Metric | Purpose |
|---|---|
| Request Volume | Tracks the number of submitted service requests |
| Average Fulfillment Time | Measures the time required to complete requests |
| Fulfillment Success Rate | Tracks successfully completed requests |
| Approval Processing Time | Measures time spent awaiting authorization |
| Request Backlog | Tracks outstanding requests |
| Reopened Request Rate | Identifies requests requiring additional work |
| Automation Rate | Tracks requests fulfilled through automated workflows |
| User Satisfaction | Evaluates the request fulfillment experience |

Metrics will be introduced when sufficient request data becomes available.

Results may support improvement initiatives under [Continual Improvement](../Continual-Improvement/).

---

## Documentation Standards

Service request records should:

1. Clearly identify the requested service or resource.
2. Document the business requirement.
3. Record relevant requester and employee information.
4. Verify eligibility and authorization.
5. Identify required technical resources.
6. Document fulfillment activities accurately.
7. Include relevant commands, configurations, and evidence.
8. Validate successful fulfillment.
9. Record employee communication.
10. Link related knowledge articles and configuration records.
11. Protect sensitive information.
12. Distinguish simulated approvals from actual lab implementation.

---

## Related Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Operational Scenarios](../Scenarios/)
- [Service Desk](../Service-Desk/)
- [Incident Management](../Incident-Management/)
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

Employee requests, business requirements, authorization workflows, and operational responsibilities may be simulated.

Technical provisioning, account administration, endpoint configuration, access management, and validation are documented based on hands-on work performed in controlled lab environments.

This documentation demonstrates practical IT administration and service management knowledge rather than employment experience within an actual production organization.
