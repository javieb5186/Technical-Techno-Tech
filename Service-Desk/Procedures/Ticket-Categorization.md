# SOP — Ticket Categorization

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Service Desk  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-SD-002  
**Version:** 1.1  
**Status:** Draft — Lab Procedure  
**ITIL Practices:** Service Desk, Incident Management, Service Request Management

## 1. Purpose

This procedure establishes a standardized method for categorizing incoming IT support tickets within Technical Techno Tech.

Accurate ticket categorization helps ensure that support activities are assigned to the appropriate IT service, technical area, and support personnel.

The procedure supports:

- Consistent ticket classification
- Accurate identification of affected IT services
- Efficient ticket routing
- Improved troubleshooting
- Appropriate escalation
- Reliable ticket reporting
- Identification of recurring technical issues
- Service performance analysis
- Continual improvement

**Key Principle:** Every ticket should be categorized according to the type of work required, the affected IT service, and the underlying technical area.

## 2. Scope

This procedure applies to all incoming IT support tickets received by Technical Techno Tech's internal Service Desk.

Tickets may originate from:

- Employee self-service requests
- Email
- Telephone
- Live chat
- Walk-up support
- Monitoring alerts
- Internal IT personnel

This procedure applies regardless of the ticketing platform used.

**Supported Ticketing Platform**

- Jira Service Management — primary ITSM platform

## 3. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Reviewing incoming ticket information
- Identifying the ticket type
- Selecting the affected IT service
- Assigning the appropriate category
- Selecting a technical subcategory
- Identifying the appropriate support group
- Updating incorrect classifications
- Documenting categorization decisions

### Technical Support Specialist

Responsible for:

- Reviewing assigned tickets
- Confirming technical categorization
- Correcting inaccurate categories
- Escalating tickets when necessary
- Recording technical findings

### IT Administrator

Responsible for:

- Reviewing complex infrastructure tickets
- Identifying affected systems and services
- Confirming technical ownership
- Supporting categorization of specialized issues

### Service Desk Coordinator

Responsible for:

- Reviewing categorization consistency
- Identifying misrouted tickets
- Maintaining categorization standards
- Reviewing ticket reporting
- Recommending category improvements

**Lab Note:** These responsibilities represent emulated organizational roles. A single learner may perform multiple roles during an exercise.

## 4. Ticket Categorization Structure

Technical Techno Tech uses a structured categorization model.

### Categorization Levels

| Level | Field | Purpose |
|---|---|---|
| 1 | Ticket Type | Identifies the type of work |
| 2 | Affected Service | Identifies the business-facing IT service |
| 3 | Technical Category | Identifies the technology area |
| 4 | Subcategory | Identifies the specific issue or request |
| 5 | Assignment Group | Identifies the responsible support function |

### Example

**Ticket:** Employee cannot sign in to their domain workstation.

| Field | Classification |
|---|---|
| Ticket Type | Incident |
| Affected Service | IT-SVC-001 — Identity & Access Management |
| Technical Category | Active Directory |
| Subcategory | Authentication Failure |
| Assignment Group | Service Desk / Identity Administration |

### Categorization Flow

```text
Incoming IT Ticket
        |
        v
Identify Ticket Type
        |
        v
Identify Affected IT Service
        |
        v
Select Technical Category
        |
        v
Select Subcategory
        |
        v
Determine Assignment Group
        |
        v
Validate and Save Categorization
```

## 5. Ticket Type Classification

The first step is determining the type of work represented by the ticket.

### 5.1 Incident

An incident is an unplanned interruption to a service or a reduction in service quality.

**Objective:** Restore normal service.

**Related Practice:** Incident Management

### 5.2 Service Request

A service request is a request from a user or authorized representative for a predefined service action.

**Objective:** Fulfill an authorized request.

**Related Practice:** Service Request Management

### 5.3 Security-Related Ticket

Security-related tickets involve potential risks to organizational information or systems.

Security-related work may be classified as an incident or another appropriate work type.

**Security is a classification attribute and escalation consideration, not necessarily a separate ITIL ticket type.**

### 5.4 Other ITSM Records

Some support activities may result in additional records.

| Record Type | Purpose |
|---|---|
| Problem | Investigate actual or potential underlying causes of incidents |
| Change | Assess and control modifications to services or infrastructure |
| Event | Record relevant changes of state detected through monitoring |
| Improvement | Track opportunities to improve services or practices |

These records should be created only when applicable.

---

## 6. IT Service Categorization

Every ticket should be associated with the most relevant service from the Technical Techno Tech IT Service Catalog.

### Internal IT Services

| Service ID | Service Name | Examples |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Authentication, passwords, permissions |
| IT-SVC-002 | Endpoint Management | Workstations, applications, device configuration |
| IT-SVC-003 | Microsoft 365 & Collaboration | Outlook, Microsoft 365 applications, collaboration |
| IT-SVC-004 | Network Connectivity | Wired, wireless, routing, network access |
| IT-SVC-005 | Server & Infrastructure Services | Windows Server, DNS, DHCP, virtualization |
| IT-SVC-006 | Information Security | Security alerts, suspicious access, security controls |
| IT-SVC-007 | Employee IT Lifecycle | Onboarding, offboarding, employee transitions |

### Service Selection Guidelines

Select the service based on:

1. The service the employee is attempting to use.
2. The business function affected.
3. The primary purpose of the request.
4. The information available during initial assessment.

The affected service may differ from the technical component causing the issue.

## 7. Technical Categories

Technical categories identify the technology or infrastructure area associated with the ticket.

### Category 1 — Active Directory

Used for issues involving on-premises directory services.

**Subcategories:**

- User Account
- Password Reset
- Account Lockout
- Authentication Failure
- Security Group
- Group Membership
- Organizational Unit
- Group Policy
- Administrative Delegation
- Domain Controller
- Replication

---

### Category 2 — Microsoft Entra ID

Used for cloud identity and access management.

**Subcategories:**

- Cloud User Account
- Authentication
- Multifactor Authentication
- Security Group
- Administrative Role
- Device Registration
- Account Access
- Sign-In Issue
- Identity Configuration

---

### Category 3 — Microsoft 365

Used for Microsoft 365 applications and administration.

**Subcategories:**

- Outlook
- Exchange Online
- Microsoft Teams
- OneDrive
- SharePoint
- Licensing
- Application Access
- Collaboration
- Service Availability

---

### Category 4 — Endpoint Management

Used for workstations and managed devices.

**Subcategories:**

- Windows Workstation
- Operating System
- Application Installation
- Application Failure
- Device Enrollment
- Microsoft Intune
- Device Compliance
- Device Configuration
- Windows Updates
- Hardware
- Peripheral Device

---

### Category 5 — Networking

Used for network connectivity and infrastructure issues.

**Subcategories:**

- Wired Connectivity
- Wireless Connectivity
- IP Addressing
- DNS Resolution
- DHCP
- Routing
- Switching
- VLAN
- Firewall
- VPN
- Network Performance

---

### Category 6 — Windows Server

Used for server operating systems and infrastructure administration.

**Subcategories:**

- Server Availability
- Server Roles
- Windows Services
- DNS Server
- DHCP Server
- File Services
- Storage
- Performance
- Backup
- Recovery
- Server Configuration

---

### Category 7 — Cloud Infrastructure

Used for cloud infrastructure resources.

**Subcategories:**

- Azure Virtual Machine
- Azure Virtual Network
- Cloud Storage
- Cloud Resource Access
- Cloud Monitoring
- Cloud Configuration
- Resource Availability

---

### Category 8 — Information Security

Used for security-related issues and requests.

**Subcategories:**

- Suspicious Authentication
- Account Compromise
- Unauthorized Access
- Malware
- Endpoint Protection
- Firewall Security
- Privileged Access
- Vulnerability
- Security Configuration
- Security Monitoring

---

### Category 9 — Employee IT Lifecycle

Used for employee lifecycle activities.

**Subcategories:**

- Employee Onboarding
- Employee Offboarding
- Employee Transfer
- Account Provisioning
- Account Deactivation
- Equipment Provisioning
- Access Modification
- License Assignment
- License Removal

## 8. Ticket Categorization Procedure

### Step 1 — Review the Ticket

Open the incoming ticket and review the available information.

Identify:

- Requester
- Ticket summary
- Description
- Affected user or department
- Error messages
- Affected device or application
- Business impact
- Existing troubleshooting information

**Expected Result:** The technician understands the reported issue or request.

### Step 2 — Determine the Ticket Type

Decide whether the ticket represents:

- Incident
- Service Request
- Security-related work requiring additional handling
- Another applicable ITSM work type

Use the distinction between service interruption and predefined service fulfillment.

**Expected Result:** Ticket type is assigned.

### Step 3 — Identify the Affected IT Service

Select the appropriate service from the IT Service Catalog.

Consider the service being consumed rather than immediately assuming the technical cause.

**Expected Result:** The ticket is associated with the correct internal IT service.

### Step 4 — Select the Technical Category

Identify the most relevant technical area.

Examples:

- Active Directory
- Microsoft Entra ID
- Microsoft 365
- Endpoint Management
- Networking
- Windows Server
- Virtualization
- Cloud Infrastructure
- Information Security
- Employee IT Lifecycle

If the technical cause is unknown, use the best-supported initial category and update it when new information becomes available.

**Expected Result:** Technical category is assigned.

### Step 5 — Select the Subcategory

Choose the most specific supported subcategory.

Examples:

| Category | Subcategory |
|---|---|
| Active Directory | Account Lockout |
| Microsoft Entra ID | Multifactor Authentication |
| Microsoft 365 | Outlook |
| Endpoint Management | Application Installation |
| Networking | DNS Resolution |
| Windows Server | Server Availability |
| Information Security | Unauthorized Access |
| Employee IT Lifecycle | Employee Onboarding |

Avoid selecting a highly specific subcategory without supporting evidence.

**Expected Result:** Subcategory accurately describes the issue or request.

### Step 6 — Determine Assignment Group

Identify the appropriate support function.

Potential assignment groups include:

- Service Desk
- Identity Administration
- Endpoint Support
- Microsoft 365 Administration
- Network Administration
- Systems Administration
- Cloud Administration
- Information Security

Assignment should reflect:

- Technical expertise
- Required permissions
- Existing procedures
- Escalation requirements
- Business impact

**Expected Result:** Ticket is routed to the appropriate support function.

### Step 7 — Validate Categorization

Before saving, confirm:

- Ticket type is appropriate.
- Affected service is correct.
- Technical category matches available evidence.
- Subcategory is sufficiently specific.
- Assignment group is appropriate.
- Security concerns are recognized.
- Ticket description supports the classification.

**Expected Result:** Ticket categorization is consistent and defensible.

### Step 8 — Save and Document

Update the ticketing platform with the selected categories.

If necessary, document why the classification was chosen.

**Expected Result:** The ticket is ready for troubleshooting, fulfillment, or escalation.

## 9. Categorization vs. Prioritization

Categorization and prioritization are separate activities.

### Categorization

Determines:

- What type of work is required?
- Which service is affected?
- Which technology is involved?
- Who should handle the ticket?

### Prioritization

Determines:

- How significant is the business impact?
- How urgently is action required?
- How should work be scheduled?

## 10. Recategorization

Ticket categorization may change as additional information becomes available.

### Reasons for Recategorization

- Initial information was incomplete.
- Troubleshooting identified a different technical cause.
- The request was incorrectly classified.
- The affected service was misidentified.
- A ticket was routed to the wrong support group.

### Recategorization Procedure

1. Review new findings.
2. Confirm the appropriate classification.
3. Update affected fields.
4. Record the reason for the change.
5. Reassign the ticket if necessary.
6. Notify relevant support personnel.

Avoid unnecessary reassignment when the current technician can appropriately resolve the issue.

---

## 11. Categorization Errors

Common errors include:

### Incorrect Ticket Type

**Example:** A request for new folder access is classified as an incident.

**Correction:** Classify it as a service request unless an existing authorized service has failed.

### Incorrect Technical Category

**Example:** A Microsoft Entra ID authentication issue is categorized as on-premises Active Directory without supporting evidence.

**Correction:** Identify the affected identity system before selecting the category.

### Excessively Broad Category

**Example:** Every workstation issue is categorized simply as "Hardware."

**Correction:** Select the most relevant supported technical subcategory.

### Incorrect Assignment Group

**Example:** A domain controller replication failure is routed to general endpoint support.

**Correction:** Route the ticket to the appropriate systems administration function.

### Premature Root Cause Assumption

**Example:** An employee reports no internet access, and the ticket is immediately categorized as a firewall failure.

**Correction:** Begin with the reported network connectivity symptom and update the category after investigation.

---

## 12. Ticket Categorization Quality Checklist

Before completing categorization, verify:

- [ ] Ticket information reviewed
- [ ] Ticket type identified
- [ ] Affected IT service selected
- [ ] Technical category assigned
- [ ] Appropriate subcategory selected
- [ ] Assignment group identified
- [ ] Security implications considered
- [ ] Classification supported by available information
- [ ] Priority handled separately
- [ ] Ticket fields updated
- [ ] Recategorization reason documented, if applicable

---

## 13. Performance Metrics

Categorization effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Categorization Accuracy | Measures correctly classified tickets |
| Recategorization Rate | Tracks tickets requiring classification changes |
| Ticket Reassignment Rate | Identifies routing problems |
| Uncategorized Ticket Volume | Tracks tickets missing required categories |
| Category Distribution | Identifies common support areas |
| Incident Category Trends | Identifies recurring service disruptions |
| Service Request Category Trends | Identifies common fulfillment activities |
| Assignment Accuracy | Evaluates correct initial routing |

These metrics can support Continual Improvement initiatives.

## 14. Procedure Review

This procedure should be reviewed when:

- New IT services are introduced.
- Technical support responsibilities change.
- Ticketing categories are modified.
- New technologies are deployed.
- Categorization errors increase.
- Ticket reporting identifies classification gaps.
- ITSM workflows are updated.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial ticket categorization procedure |
| 1.1 | Remove unneccesary information |