# SOP — Configuration Item Management

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Configuration Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-SCM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Service Configuration Management

---

## 1. Purpose

This procedure establishes a standardized approach for managing Configuration Items (CIs) throughout their lifecycle within Technical Techno Tech.

Configuration Item Management ensures that information about infrastructure components, their configurations, relationships, ownership, and operational status is accurately documented and maintained.

The procedure supports:

- Accurate infrastructure documentation
- Consistent Configuration Item identification
- Improved service dependency visibility
- Effective Incident Management
- Improved Problem Management investigations
- Better change impact assessments
- Infrastructure lifecycle tracking
- Configuration verification
- Operational risk assessment
- Improved troubleshooting efficiency
- Information security accountability
- Continual improvement

**Key Principle:** Configuration Item Management focuses on maintaining accurate, useful information about the components required to deliver IT services and the relationships between those components.

---

## 2. Scope

This procedure applies to Configuration Items supporting Technical Techno Tech's internal IT services.

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

### Configuration Item Categories

This procedure covers:

- Servers
- Workstations
- Network devices
- Virtual machines
- Cloud services
- Directory services
- Business-critical applications
- Infrastructure services
- Selected configuration records
- Service dependencies

### Technical Environments

Configuration Items may exist within:

- Windows Server
- Active Directory Domain Services
- Windows 11
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Cisco Packet Tracer
- OPNsense
- VyOS

### Scope Limitations

Not every technical object must be individually managed as a CI.

The level of configuration detail should be determined by:

- Service importance
- Operational risk
- Security requirements
- Troubleshooting value
- Change impact
- Administrative effort

For example, a domain controller may be a CI, while individual temporary files on that server generally do not require separate CI records.

---

## 3. ITIL 4 Service Configuration Management

### Purpose

The purpose of Service Configuration Management is to ensure that accurate and reliable information about the configuration of services, and the Configuration Items that support them, is available when and where it is needed.

This includes information about how Configuration Items are configured and the relationships between them.

### Important Definitions

**Configuration Item (CI):** Any component that needs to be managed in order to deliver an IT service.

**Configuration Record:** A record containing information about a Configuration Item.

**Configuration Management Database (CMDB):** A database used to store configuration records and relationships.

**Configuration Management System (CMS):** A set of tools, data, and information used to support Service Configuration Management.

**Configuration Baseline:** An agreed reference configuration used to assess subsequent changes.

**CI Relationship:** A documented association or dependency between Configuration Items.

**CI Lifecycle:** The progression of a Configuration Item from identification and registration through operation, modification, and retirement.

**Configuration Verification:** The process of confirming that recorded configuration information matches the actual environment.

**Configuration Audit:** A structured examination of configuration information and supporting evidence.

### Configuration Management vs. Asset Management

| Service Configuration Management | IT Asset Management |
|---|---|
| Focuses on service-supporting components and relationships | Focuses on the lifecycle and value of IT assets |
| Supports operational decisions | Supports financial, contractual, and lifecycle decisions |
| Tracks technical configuration | Tracks ownership, cost, warranty, and asset status |
| Identifies service dependencies | Identifies asset inventory and utilization |

An item may be both an IT asset and a Configuration Item.

For example, a physical server may require both financial asset tracking and technical configuration management.

---

## 4. Configuration Item Management Principles

Technical Techno Tech follows these principles.

### 4.1 Identify Relevant Components

Register components that are important for delivering or supporting IT services.

### 4.2 Maintain Unique Identification

Each CI should have a unique identifier.

### 4.3 Record Accurate Information

Configuration records must reflect verified information whenever possible.

### 4.4 Document Relationships

Identify dependencies between services and infrastructure components.

### 4.5 Maintain Ownership

Each CI should have an identified responsible role or team.

### 4.6 Control Configuration Changes

Significant modifications should follow applicable Change Enablement requirements.

### 4.7 Verify Configuration Information

Periodically compare recorded information with the actual environment.

### 4.8 Track Lifecycle Status

Configuration records should reflect whether a component is planned, active, unavailable, or retired.

### 4.9 Protect Sensitive Information

Configuration records must not expose passwords, private keys, access tokens, or other secrets.

### 4.10 Preserve Historical Traceability

Relevant changes, incidents, and retirement decisions should remain traceable.

---

## 5. Roles and Responsibilities

### Configuration Management Coordinator

Responsible for:

- Maintaining CI documentation standards
- Reviewing CI record completeness
- Coordinating configuration verification
- Managing CI identification conventions
- Supporting dependency documentation
- Reviewing configuration discrepancies

### Systems Administrator

Responsible for:

- Maintaining server configuration information
- Documenting Active Directory infrastructure
- Recording server roles and dependencies
- Verifying relevant server attributes
- Updating records after approved changes

### Network Administrator

Responsible for:

- Maintaining network device records
- Documenting network interfaces
- Recording routing and network dependencies
- Verifying relevant network configuration
- Maintaining network topology information

### Cloud Administrator

Responsible for:

- Maintaining relevant cloud service records
- Documenting Microsoft 365 dependencies
- Recording Entra ID and Intune configuration information
- Maintaining Azure resource documentation
- Verifying cloud configuration attributes

### Endpoint Support Specialist

Responsible for:

- Maintaining workstation records
- Documenting endpoint operating systems
- Recording device management information
- Updating endpoint lifecycle status

### Service Owner

Responsible for:

- Identifying service-critical Configuration Items
- Reviewing service dependencies
- Supporting impact assessments
- Confirming relevant service requirements

### Change Authority

Responsible for:

- Evaluating and authorizing changes according to applicable Change Enablement procedures

### Information Security Personnel

Responsible for:

- Reviewing security-sensitive configuration information
- Identifying documentation security requirements
- Supporting configuration compliance reviews

**Lab Note:** These are simulated organizational roles. A single learner may perform multiple responsibilities in the Technical Techno Tech environment.

---

## 6. Configuration Item Categories

Technical Techno Tech uses the following proposed CI classification model.

| CI Category | Description | Examples |
|---|---|---|
| Server | Physical or virtual server | DC01, DC02 |
| Workstation | Employee or administrative endpoint | MGMT01, CLIENT01 |
| Network Device | Component providing network functionality | Router, switch, firewall |
| Cloud Service | Cloud-hosted service or resource | Microsoft 365 tenant, Azure VM |
| Directory Service | Identity and directory infrastructure | Active Directory domain |
| Application | Application important to service delivery | Business application |
| Infrastructure Service | Supporting technical service | DNS, DHCP |
| Virtualization Component | Hypervisor or virtualization resource | Hyper-V host, virtual network |
| Service | Managed IT service | IT-SVC-001 |

A service may be represented as a CI when managing its configuration and relationships provides operational value.

---

## 7. Configuration Item Identification

Each CI should receive a unique identifier.

### Proposed CI Naming Convention

```text
CI-001
CI-002
CI-003
CI-004
```

### Example CI Register

| CI ID | CI Name | CI Category |
|---|---|---|
| CI-001 | DC01 | Server |
| CI-002 | DC02 | Server |
| CI-003 | MGMT01 | Workstation |
| CI-004 | CLIENT01 | Workstation |

These IDs are proposed examples and should be checked against the actual CI register before assignment.

### Naming Rules

1. Use unique identifiers.
2. Avoid reusing retired CI IDs.
3. Use consistent CI names.
4. Record the actual system hostname when applicable.
5. Document naming changes.
6. Maintain references between old and new names where necessary.

### Important Distinction

A CI ID identifies the configuration record.

A hostname identifies a system on the network.

They are related but not interchangeable.

---

## 8. Configuration Item Lifecycle

Configuration Items move through defined lifecycle stages.

### Proposed Lifecycle Statuses

| Status | Description |
|---|---|
| Proposed | Component identified but not approved or created |
| Planned | Component approved or scheduled for deployment |
| Provisioning | Component being created or configured |
| Active | Component available for its intended operational purpose |
| Maintenance | Component undergoing maintenance |
| Degraded | Component operating with reduced capability |
| Unavailable | Component not currently providing its intended functionality |
| Retiring | Component being removed from service |
| Retired | Component no longer in operational use |

These are proposed internal CI statuses, not mandatory ITIL status names.

### Lifecycle Workflow

```text
Identify CI
    |
    v
Evaluate Registration Need
    |
    v
Create CI Record
    |
    v
Classify and Assign Ownership
    |
    v
Record Configuration Attributes
    |
    v
Document Relationships
    |
    v
Verify Configuration
    |
    v
Maintain and Update Record
    |
    v
Review Lifecycle Status
    |
    v
Retire When Appropriate
```

A CI may move between Active, Maintenance, Degraded, and Unavailable depending on its operational condition.

---

## 9. Configuration Item Management Procedure

### Step 1 — Identify a Potential Configuration Item

Identify a component that supports an internal IT service.

Potential sources include:

- Infrastructure deployment
- Service onboarding
- Technical discovery
- Change implementation
- Incident investigation
- Network documentation
- Cloud resource provisioning
- Configuration reviews

#### Example

A Windows Server virtual machine named DC01 provides Active Directory Domain Services.

**Expected Result:** A potentially relevant CI is identified.

### Step 2 — Determine Whether CI Registration Is Required

Evaluate the component's importance.

### Registration Criteria

Consider:

1. Does the component support an IT service?
2. Is it required for service availability?
3. Does it have significant operational dependencies?
4. Would its failure affect employees?
5. Does it require configuration tracking?
6. Would its configuration matter during troubleshooting?
7. Does it require controlled modification?

### Example

DC01 should be considered for CI registration because it supports identity and directory services.

**Expected Result:** The need for a configuration record is established.

### Step 3 — Check for an Existing CI Record

Before creating a new record, search existing documentation.

Review:

- CI register
- Server inventory
- Workstation inventory
- Network device records
- Cloud service records
- Existing dependency maps

### Duplicate Prevention

Check:

- Hostname
- CI ID
- Device identifier
- Cloud resource identifier
- System purpose
- Existing configuration records

**Expected Result:** Duplicate records are avoided.

### Step 4 — Assign a Unique CI Identifier

Assign an unused CI ID.

#### Example

```text
CI ID:
CI-001

CI Name:
DC01

CI Category:
Server
```

The identifier should remain stable throughout the CI lifecycle.

**Expected Result:** The CI has a unique record identifier.

### Step 5 — Classify the Configuration Item

Assign the appropriate category.

#### Example

**CI Name:** DC01

**CI Category:** Server

**CI Subcategory:** Domain Controller

**Technology:** Windows Server

**Expected Result:** The CI is classified consistently.

### Step 6 — Record Basic CI Attributes

Capture the relevant identification and technical information.

### Recommended Attributes

| Attribute | Description |
|---|---|
| CI ID | Unique identifier |
| CI Name | Component name |
| CI Category | Component classification |
| Description | Purpose of the component |
| Environment | Lab, development, test, or production |
| Lifecycle Status | Current CI status |
| Responsible Role | Technical ownership |
| Related Service | Supported IT service |
| Operating System | OS where applicable |
| Hostname | System hostname |
| IP Address | Relevant network address |
| Location | Physical, virtual, or cloud environment |
| Dependencies | Related CIs |
| Last Verified | Most recent configuration verification |
| Related Changes | Relevant Change records |
| Related Incidents | Relevant Incident records |

Not all attributes apply to every CI category.

**Expected Result:** The CI record contains sufficient information for operational use.

### Step 7 — Identify the Supported IT Service

Associate the CI with relevant internal services.

#### Example

**CI:** DC01

**Supported Services:**

- IT-SVC-001 — Identity & Access Management
- IT-SVC-005 — Server & Infrastructure Services

Other service dependencies may exist and should be verified.

**Expected Result:** The relationship between the component and service delivery is documented.

### Step 8 — Assign CI Ownership

Identify the responsible technical role.

#### Example

```text
CI:
DC01

Responsible Role:
Systems Administrator

Service Owner:
Identity & Access Management Service Owner
```

### Ownership Responsibilities

The assigned role should support:

- Configuration accuracy
- Technical verification
- Lifecycle updates
- Change coordination
- Incident investigation
- Dependency documentation

**Expected Result:** CI accountability is established.

### Step 9 — Record Technical Configuration

Document relevant configuration attributes.

#### Example — DC01

```text
CI Name:
DC01

Hostname:
DC01

Domain:
homelab.local

Operating System:
Windows Server

IP Address:
10.20.10.10

Subnet Mask:
255.255.255.0

Role:
Active Directory Domain Services

Additional Role:
DNS
```

The operating system version, role configuration, and current IP settings should be verified before recording them as current facts.

**Expected Result:** The configuration record describes the component accurately.

### Step 10 — Identify CI Relationships

Determine which components depend on or interact with the CI.

### Relationship Types

- Depends On
- Provides Service To
- Hosted On
- Connected To
- Managed By
- Replicates With
- Authenticates Through
- Monitored By

#### Example

```text
DC01
 |
 +-- Provides Active Directory services
 |
 +-- Provides DNS functionality
 |
 +-- Replicates with DC02
 |
 +-- Supports domain-joined workstations
```

Relationships must reflect actual configured dependencies.

**Expected Result:** Relevant CI relationships are documented.

### Step 11 — Establish a Configuration Baseline

Record the approved or accepted configuration state.

### Baseline Information

May include:

- Operating system version
- Installed server roles
- Network configuration
- Domain membership
- Relevant security settings
- Service configuration
- Important dependencies
- Verification date

### Example

```text
Configuration Baseline

CI ID:
CI-001

CI Name:
DC01

Baseline Version:
1.0

Baseline Status:
Proposed

Verification Date:
Not Yet Recorded

Approved By:
Not Yet Recorded
```

### Important

A documented configuration snapshot is not automatically an approved baseline.

Approval and verification must be distinguished.

**Expected Result:** A reference configuration is established or proposed.

### Step 12 — Verify the Actual Configuration

Compare the CI record with the real environment.

#### Example — Computer Information

```powershell
Get-ComputerInfo |
Select-Object CsName, WindowsProductName, WindowsVersion, OsBuildNumber
```

#### Example — IP Configuration

```powershell
Get-NetIPConfiguration
```

#### Example — Installed Windows Server Roles

On Windows Server:

```powershell
Get-WindowsFeature |
Where-Object Installed -eq $true
```

#### Example — Domain Membership

```powershell
Get-CimInstance Win32_ComputerSystem |
Select-Object Name, Domain, PartOfDomain
```

### Verification Requirements

Record:

1. Diagnostic command
2. Execution date and time
3. Target system
4. Actual output
5. Expected configuration
6. Identified differences

**Expected Result:** Configuration information is verified or discrepancies are documented.

### Step 13 — Identify Configuration Discrepancies

Compare documented and actual configuration.

#### Example

**Documented IP Address:** 10.20.10.10

**Actual IP Address:** 10.20.10.20

### Possible Explanations

- Documentation is outdated.
- A change was implemented.
- An unauthorized modification occurred.
- The wrong system was inspected.
- The original record was incorrect.

### Discrepancy Procedure

1. Confirm the observed difference.
2. Verify the correct system.
3. Review relevant Change records.
4. Determine operational significance.
5. Document the discrepancy.
6. Assign investigation or correction.
7. Update the CI record when justified.

**Expected Result:** Configuration differences are identified and tracked.

### Step 14 — Review Configuration Security

Ensure the CI record does not expose sensitive information.

### Do Not Store

- Passwords
- Private keys
- Access tokens
- Recovery secrets
- Authentication cookies
- Unredacted credentials
- Other sensitive authentication material

### Public Repository Considerations

Technical Techno Tech uses GitHub for portfolio documentation.

Before publishing CI records:

1. Review screenshots.
2. Remove credentials.
3. Remove secrets.
4. Avoid publishing sensitive tenant identifiers unnecessarily.
5. Review network information for disclosure risk.
6. Use fictional or sanitized data where appropriate.
7. Distinguish public portfolio information from private operational records.

**Expected Result:** CI documentation is appropriate for its storage location.

### Step 15 — Register the Configuration Item

Create the CI record in the appropriate repository directory.

### Proposed Structure

```text
Service-Configuration-Management/
├── README.md
├── Procedures/
│   └── Configuration-Item-Management.md
├── Configuration-Items/
│   ├── Servers/
│   │   ├── CI-001-DC01.md
│   │   └── CI-002-DC02.md
│   ├── Workstations/
│   │   ├── CI-003-MGMT01.md
│   │   └── CI-004-CLIENT01.md
│   ├── Network-Devices/
│   └── Cloud-Services/
└── Dependency-Maps/
```

These CI record filenames are examples and should only be created when appropriate.

**Expected Result:** The CI record is stored in the designated location.

### Step 16 — Link the CI to Infrastructure Documentation

Connect the CI record with relevant technical documentation.

#### Example

**CI Record:**

```text
08-Service-Configuration-Management/
Configuration-Items/Servers/CI-001-DC01.md
```

**Infrastructure Documentation:**

```text
Infrastructure/
Windows-Server/Server-Inventory.md
```

### Documentation Distinction

**Infrastructure Documentation:** Describes the architecture, configuration, and technical implementation.

**CI Record:** Describes the managed component, its status, relationships, ownership, and configuration baseline.

Both may reference the same system.

**Expected Result:** Related documentation is connected without unnecessary duplication.

### Step 17 — Link Relevant Operational Records

Associate the CI with applicable records.

### Potential Relationships

- Incidents affecting the CI
- Problems involving the CI
- Changes modifying the CI
- Events detected on the CI
- Knowledge articles supporting the CI

#### Example

```text
CI:
CI-001 — DC01

Related Incident:
INC-001

Related Problem:
PRB-001

Related Change:
CHG-001

Related Event:
EVT-001
```

These identifiers are illustrative.

Only link records that actually exist.

**Expected Result:** Operational history is traceable.

### Step 18 — Update the CI After Configuration Changes

Review CI information following applicable configuration modifications.

### Potential Update Triggers

- Operating system upgrade
- IP address change
- Server role installation
- DNS configuration change
- Domain membership change
- Network topology modification
- Cloud resource migration
- Security configuration update
- Service dependency change

### Update Procedure

1. Review the implemented change.
2. Identify affected CI attributes.
3. Verify the actual configuration.
4. Update the CI record.
5. Update relevant relationships.
6. Record the change reference.
7. Review the baseline.
8. Document verification results.

### Important

The CI record should reflect the actual state.

An approved but unimplemented change must not be recorded as completed configuration.

**Expected Result:** Configuration information remains current.

### Step 19 — Review CI Lifecycle Status

Determine whether the component remains active or requires a status update.

### Examples

**Active:** Server is available for its intended purpose.

**Maintenance:** Server is undergoing planned maintenance.

**Degraded:** Server is functioning with reduced capability.

**Unavailable:** Server is not providing its intended functionality.

**Retiring:** Server is being decommissioned.

**Retired:** Server is no longer in operational use.

### Important

Lifecycle status and technical health are related but distinct concepts.

A CI can remain an active managed component while temporarily degraded or unavailable.

**Expected Result:** CI status accurately reflects its current condition.

### Step 20 — Perform Periodic Configuration Verification

Review CI records at an appropriate interval.

### Proposed Review Approach

| CI Criticality | Suggested Verification Frequency |
|---|---|
| High | Monthly or after significant changes |
| Medium | Quarterly or after significant changes |
| Low | Semiannually or after significant changes |

These are proposed lab review intervals, not mandatory ITIL requirements or established production SLAs.

### Verification Activities

- Confirm system identity.
- Verify operating system information.
- Review network configuration.
- Check installed roles.
- Confirm ownership.
- Review service relationships.
- Check lifecycle status.
- Review related changes.
- Identify outdated documentation.

**Expected Result:** CI information remains reliable.

### Step 21 — Retire the Configuration Item

Retire a CI when the associated component is permanently removed from operational use.

### Potential Retirement Triggers

- Server decommissioning
- Workstation replacement
- Network device replacement
- Cloud resource deletion
- Service retirement
- Infrastructure migration

### Retirement Procedure

1. Confirm the component is no longer required.
2. Review service dependencies.
3. Verify applicable retirement authorization.
4. Coordinate with Change Enablement where required.
5. Confirm relevant data retention and security requirements.
6. Verify the component has been decommissioned.
7. Update CI lifecycle status.
8. Record the retirement date.
9. Preserve relevant historical references.
10. Update dependency documentation.

### Important

Do not delete a CI record simply because the component has been retired.

Historical records may be necessary for auditability and incident investigation.

**Expected Result:** The CI is retired while relevant configuration history is preserved.

### Step 22 — Review the Completed CI Record

Confirm:

- CI ID is unique.
- CI category is correct.
- Required attributes are documented.
- Ownership is identified.
- Related services are recorded.
- Dependencies are documented.
- Configuration has been verified where possible.
- Sensitive information is excluded.
- Lifecycle status is accurate.
- Related operational records are linked where applicable.
- Verification date is recorded.

**Expected Result:** The CI record meets documentation requirements.

---

## 10. Configuration Item Record Template

Use the existing repository template:

[Configuration Item Template](../../Templates/Configuration-Item-Template.md)

The following fields are recommended for CI records.

```text
CONFIGURATION ITEM RECORD

CI ID:
CI Name:
CI Category:
CI Subcategory:

Description:
Environment:
Lifecycle Status:

Responsible Role:
Service Owner:

Hostname:
Operating System:
Operating System Version:
IP Address:
Network Segment:
Hosting Platform:

Installed Roles:
Primary Function:

Related Services:
Related Configuration Items:
Dependencies:

Configuration Baseline:
Baseline Version:
Baseline Approval Status:

Related Incidents:
Related Problems:
Related Changes:
Related Events:

Last Verified:
Verification Method:
Verification Result:

Security Classification:
Documentation Location:

Date Created:
Last Updated:
Retirement Date:

Notes:
```

Only include fields relevant to the CI category.

---

## 11. Configuration Item Relationships

CI relationships describe how components support or depend on each other.

### Common Relationship Types

| Relationship | Description | Example |
|---|---|---|
| Depends On | One component requires another | Client depends on DNS |
| Provides Service To | Component supports a service | DC01 supports identity services |
| Hosted On | Component runs on another platform | VM hosted on Hyper-V |
| Connected To | Network or system connection | Server connected to switch |
| Replicates With | Data or directory replication | DC01 replicates with DC02 |
| Managed By | Administrative responsibility | Workstation managed through Intune |
| Authenticates Through | Identity dependency | Domain client uses AD DS |
| Monitored By | Monitoring relationship | Server monitored by a monitoring platform |

### Relationship Documentation Requirements

For each important relationship, record:

1. Source CI
2. Target CI or service
3. Relationship type
4. Description
5. Verification status
6. Last verified date

### Important

Do not infer technical dependencies solely from component names.

Relationships should be based on actual configuration or clearly identified design assumptions.

---

## 12. Dependency Mapping

Dependency mapping illustrates how services rely on supporting infrastructure.

### Example — Identity & Access Management

```text
IT-SVC-001
Identity & Access Management
          |
          v
Active Directory Domain Services
          |
      +---+---+
      |       |
      v       v
    DC01     DC02
      |       |
      +---+---+
          |
          v
DNS and Domain Services
          |
          v
Domain-Joined Workstations
```

This is a simplified conceptual diagram.

Actual service dependencies, DNS client settings, replication health, and network connectivity must be verified.

### Dependency Map Requirements

- Identify the service.
- Identify supporting CIs.
- Show relevant relationships.
- Document critical dependencies.
- Identify redundancy where applicable.
- Record verification status.
- Update maps after significant changes.

### Repository Location

```text
08-Service-Configuration-Management/
Dependency-Maps/
```

---

## 13. Configuration Baseline Management

A configuration baseline provides a reference for evaluating future changes.

### Example Baseline — DC01

| Attribute | Proposed Baseline |
|---|---|
| Hostname | DC01 |
| Domain | homelab.local |
| IP Address | 10.20.10.10 |
| Subnet Mask | 255.255.255.0 |
| Server Role | Active Directory Domain Services |
| DNS Role | Subject to verification |
| Baseline Status | Proposed |

### Baseline Procedure

1. Identify important configuration attributes.
2. Record the current configuration.
3. Verify the information.
4. Review relevant operational requirements.
5. Obtain applicable baseline approval.
6. Assign a baseline version.
7. Store the baseline reference.
8. Compare future changes against the baseline.

### Important

An initial technical inventory is not automatically an approved configuration baseline.

---

## 14. Configuration Verification and Auditing

Configuration verification determines whether documented information matches the actual environment.

### Verification Methods

- PowerShell commands
- Windows administrative tools
- Server Manager
- Active Directory Administrative Center
- Network device commands
- Microsoft 365 administrative portals
- Azure resource inspection
- Hyper-V configuration inspection

### Example — Windows Server

```powershell
Get-ComputerInfo |
Select-Object CsName, WindowsProductName, OsBuildNumber
```

```powershell
Get-NetIPConfiguration
```

```powershell
Get-WindowsFeature |
Where-Object Installed -eq $true
```

### Example — Active Directory

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName, IPv4Address, Site
```

### Example — Workstation

```powershell
Get-CimInstance Win32_ComputerSystem |
Select-Object Name, Domain, PartOfDomain
```

### Verification Outcomes

| Outcome | Description |
|---|---|
| Verified | Recorded information matches observed configuration |
| Discrepancy | Recorded and observed information differ |
| Partially Verified | Only selected attributes were confirmed |
| Not Verified | No sufficient verification evidence available |

### Audit Considerations

A configuration audit may examine:

- Record completeness
- CI ownership
- Relationship accuracy
- Baseline consistency
- Change traceability
- Lifecycle status
- Security of stored configuration data

---

## 15. Configuration Discrepancy Management

A discrepancy occurs when documented configuration differs from the observed environment.

### Example

**Recorded Configuration:**

```text
DC01 IP Address:
10.20.10.10
```

**Observed Configuration:**

```text
DC01 IP Address:
10.20.10.20
```

This is a hypothetical discrepancy.

### Investigation Procedure

1. Confirm the correct CI was inspected.
2. Repeat the relevant verification.
3. Review configuration history.
4. Review related Change records.
5. Determine whether the difference is authorized.
6. Assess service impact.
7. Document the finding.
8. Assign corrective action.
9. Update documentation or initiate change control as appropriate.
10. Verify the final state.

### Possible Outcomes

- Documentation corrected
- Authorized change confirmed
- Unauthorized modification investigated
- Configuration restored through an authorized process
- Discrepancy remains under investigation

### Important

Do not automatically modify the live configuration to match outdated documentation.

Determine which configuration is correct before taking action.

---

## 16. Configuration Item Management — Windows Server

Windows Server CIs may require:

- Hostname
- Operating system
- IP configuration
- Domain membership
- Installed roles
- Hosting platform
- Service dependencies
- Administrative ownership
- Lifecycle status

### Example — DC01

```text
CI ID:
CI-001

CI Name:
DC01

Category:
Server

Domain:
homelab.local

IP Address:
10.20.10.10

Primary Role:
Active Directory Domain Services

Environment:
Hyper-V Lab
```

### Potential Verification Commands

```powershell
hostname
```

```powershell
Get-NetIPConfiguration
```

```powershell
Get-WindowsFeature |
Where-Object Installed -eq $true
```

---

## 17. Configuration Item Management — Active Directory

Active Directory configuration information may include:

- Domain name
- Forest information
- Domain controllers
- Sites
- Replication relationships
- DNS dependencies
- Organizational structure
- Relevant security configuration

### Example — Domain Information

```powershell
Get-ADDomain
```

### Example — Forest Information

```powershell
Get-ADForest
```

### Example — Domain Controllers

```powershell
Get-ADDomainController -Filter *
```

### Example — Replication

```powershell
repadmin /replsummary
```

### Important

Not every Active Directory object needs an individual CI record.

For example, ordinary user accounts are typically managed through identity lifecycle processes rather than being registered individually as infrastructure CIs.

---

## 18. Configuration Item Management — Networking

Network CI records may include:

- Device name
- Device type
- Management IP address
- Operating system or firmware
- Network interfaces
- VLAN information
- Routing role
- Connected devices
- Security function
- Physical or virtual location

### Example

```text
CI ID:
To Be Assigned

CI Name:
Core Switch

Category:
Network Device

Environment:
Packet Tracer Lab

Primary Function:
Network Connectivity

Management IP:
To Be Verified
```

### Packet Tracer Considerations

Packet Tracer devices are simulated network components.

They should be identified as simulated infrastructure rather than physical deployed equipment.

### OPNsense and VyOS

Records may include:

- Virtual machine information
- Network interfaces
- Routing configuration
- Firewall role
- Relevant dependencies
- Verification evidence

Do not claim a specific routing or firewall configuration unless it has been implemented and tested.

---

## 19. Configuration Item Management — Microsoft 365

Microsoft 365 configuration records may include:

- Tenant purpose
- Associated domain
- Administrative ownership
- Licensed services
- Identity dependencies
- Relevant configuration settings
- Supported internal IT services

### Potential CIs

- Microsoft 365 tenant
- Microsoft Entra ID service configuration
- Microsoft Intune service configuration
- Critical cloud applications

### Important

A cloud service can be represented as a CI without creating separate records for every user, license, or configuration setting.

The required level of detail depends on operational value.

### Security Considerations

Avoid publishing:

- Authentication secrets
- Access tokens
- Private keys
- Sensitive tenant configuration exports
- Confidential account information

---

## 20. Configuration Item Management — Microsoft Azure

Azure CI records may include:

- Resource name
- Resource type
- Subscription or resource group reference
- Region
- Operating system
- Network configuration
- Hosting dependencies
- Lifecycle status
- Related services

### Example — Proposed Azure VM

```text
CI ID:
To Be Assigned

CI Name:
AZ-DC01

Category:
Cloud Service / Virtual Machine

Platform:
Microsoft Azure

Deployment Status:
Proposed

Operating System:
Windows Server

IP Address:
Not Assigned

Resource Group:
Not Assigned
```

This example represents a proposed resource, not an existing deployment.

### Azure Cost Considerations

Azure resources may generate charges based on:

- Compute usage
- Storage
- Networking
- Monitoring
- Data retention
- Other enabled services

Stopping a virtual machine may reduce compute charges, but associated resources may continue generating costs.

Configuration records should distinguish:

- Running
- Stopped
- Deallocated
- Deleted

These states have different operational and potential billing implications.

---

## 21. Configuration Item Management — Virtualization

Virtualization CI records may include:

- Virtual machine name
- Guest operating system
- Hosting platform
- Virtual CPU
- Assigned memory
- Virtual disks
- Virtual network connections
- Power state
- Dependencies

### Example

```text
CI Name:
DC01

Hosting Platform:
Hyper-V

Guest Operating System:
Windows Server

Virtual CPU:
To Be Verified

Memory:
To Be Verified

Virtual Disk:
To Be Verified

Network:
To Be Verified
```

### Important

A virtual machine's power state is not the same as its service health.

A powered-on virtual machine may still have unavailable applications or services.

---

## 22. Configuration Item Records and Repository Structure

Technical Techno Tech stores configuration documentation in GitHub.

### Proposed Structure

```text
Service-Configuration-Management/
├── README.md
├── Procedures/
│   └── Configuration-Item-Management.md
├── Configuration-Items/
│   ├── Servers/
│   │   ├── CI-001-DC01.md
│   │   └── CI-002-DC02.md
│   ├── Workstations/
│   │   ├── CI-003-MGMT01.md
│   │   └── CI-004-CLIENT01.md
│   ├── Network-Devices/
│   └── Cloud-Services/
└── Dependency-Maps/
```

### GitHub Documentation Approach

GitHub serves as a version-controlled documentation repository.

It can support:

- CI record history
- Technical documentation
- Dependency maps
- Configuration snapshots
- Change references
- Reviewable documentation updates

### Important Distinction

A GitHub repository containing Markdown CI records is not automatically a fully implemented CMDB.

A CMDB generally provides structured configuration information and relationships that can be queried and maintained through supporting tools and processes.

The Technical Techno Tech repository represents a lightweight configuration documentation system unless additional capabilities are implemented.

---

## 23. Configuration Item Example — DC01

### Example Record

**CI ID:** CI-001  
**CI Name:** DC01  
**CI Category:** Server  
**Environment:** Hyper-V Lab  
**Domain:** homelab.local  
**IP Address:** 10.20.10.10

### Purpose

DC01 supports Active Directory Domain Services within the Technical Techno Tech lab environment.

### Proposed Attributes

| Attribute | Value |
|---|---|
| CI ID | CI-001 |
| CI Name | DC01 |
| Category | Server |
| Operating System | Windows Server |
| Domain | homelab.local |
| IP Address | 10.20.10.10 |
| Primary Role | Domain Controller |
| Hosting Platform | Hyper-V |
| Responsible Role | Systems Administrator |
| Related Service | IT-SVC-001 |
| Verification Status | Pending |
| Baseline Status | Proposed |

### Potential Dependencies

- DC02
- DNS services
- Domain-joined workstations
- Hyper-V virtual networking
- Relevant network infrastructure

### Verification Procedure

On DC01:

```powershell
Get-ComputerInfo |
Select-Object CsName, WindowsProductName, OsBuildNumber
```

```powershell
Get-NetIPConfiguration
```

```powershell
Get-WindowsFeature |
Where-Object Installed -eq $true
```

### Expected Outcome

The CI record accurately describes DC01 and identifies its relationships with supporting infrastructure.

**Example Status:** Proposed documentation example. No new verification or configuration audit is claimed.

---

## 24. Configuration Item Evidence Standards

Evidence should demonstrate actual configuration information.

### Evidence Types

- PowerShell output
- Windows Server configuration screenshots
- Active Directory administrative screenshots
- Network device configuration output
- Hyper-V settings
- Azure resource configuration
- Microsoft 365 administrative information
- Configuration comparison results
- Approved Change records

### Evidence Requirements

Each evidence item should identify:

1. Source system
2. Collection date and time
3. Verification method
4. Actual observed configuration
5. Related CI ID
6. Relevant baseline
7. Identified discrepancies

### Documentation Standard

Distinguish:

**Expected Configuration:** The intended technical configuration.

**Actual Configuration:** The observed configuration.

**Proposed Baseline:** A reference configuration awaiting acceptance.

**Approved Baseline:** A reference configuration that has received the required authorization.

**Verified Configuration:** Information confirmed through appropriate technical inspection.

Do not fabricate verification output, approval records, or configuration history.

---

## 25. Integration With Incident Management

CI records support incident investigation by identifying affected components and dependencies.

### Example

**Incident:** Employees cannot authenticate.

### Relevant CIs

- DC01
- DC02
- DNS infrastructure
- Affected workstations

### Benefits

- Faster identification of dependencies
- Better impact assessment
- Improved troubleshooting
- More accurate incident documentation

### Important

A CI relationship may identify a possible cause but does not prove the cause of an incident.

---

## 26. Integration With Problem Management

CI information supports recurring issue analysis.

### Example

Multiple incidents involve DNS failures.

### Potential Problem Investigation

Review:

- Affected DNS servers
- Related domain controllers
- Network dependencies
- Configuration changes
- Historical failure patterns

### Benefits

- Improved root cause analysis
- Identification of shared dependencies
- Better tracking of recurring infrastructure issues

---

## 27. Integration With Change Enablement

Configuration records support change assessment and implementation.

### Before a Change

Review:

- Affected CIs
- Current configuration
- Service dependencies
- Operational risks
- Configuration baseline

### During a Change

Record:

- Relevant implementation activity
- Configuration modifications
- Validation evidence
- Unexpected results

### After a Change

1. Verify the final configuration.
2. Update CI attributes.
3. Update dependency relationships.
4. Review baseline information.
5. Link the Change record.
6. Record verification results.

### Important

Change authorization and CI documentation are separate activities.

An approved change does not establish that the change was successfully implemented.

---

## 28. Integration With Monitoring and Event Management

Monitoring events should identify affected CIs when possible.

### Example

```text
Event ID:
EVT-001

Affected CI:
CI-001 — DC01

Detected Condition:
DNS service failure
```

### Benefits

- Improved event correlation
- Better escalation routing
- Faster service impact analysis
- Improved technical ownership
- More accurate dependency evaluation

### Important

A monitoring event may indicate that a CI's operational condition has changed.

It does not automatically mean that the CI's recorded configuration has changed.

---

## 29. Integration With Information Security Management

CI records support security management by identifying:

- Critical infrastructure
- Administrative ownership
- Relevant system configurations
- Security-sensitive dependencies
- Configuration discrepancies
- Systems requiring security review

### Security Considerations

- Protect configuration records.
- Limit access to sensitive details.
- Avoid storing secrets.
- Review unauthorized modifications.
- Preserve appropriate audit evidence.
- Maintain accurate system ownership.

### Example

An unexpected change to a domain controller's security configuration may require:

- Configuration verification
- Security investigation
- Change record review
- Updated CI documentation

---

## 30. Integration With Continual Improvement

CI management can reveal documentation and process improvement opportunities.

### Examples

- Missing CI records
- Incomplete dependency maps
- Outdated IP addresses
- Incorrect ownership
- Unverified configurations
- Missing change references
- Duplicate records
- Inconsistent naming conventions

### Example Improvement Record

```text
Improvement ID:
IMP-001

Source:
Configuration Verification

Finding:
Several server records do not include
a last verified date.

Proposed Improvement:
Introduce a standard verification field
and periodic review schedule.

Owner:
To Be Assigned

Status:
Proposed
```

This is an illustrative improvement opportunity.

---

## 31. Common Configuration Item Management Errors

### Error 1 — Registering Every Technical Object

**Incorrect:** Creating CI records for every file, account, or temporary object.

**Correct:** Register components that require management to support IT services.

### Error 2 — Confusing Assets and CIs

**Incorrect:** Assuming every IT asset requires the same configuration detail.

**Correct:** Determine configuration management needs based on service relevance.

### Error 3 — Creating Duplicate Records

**Incorrect:** Registering the same server under multiple unrelated CI IDs.

**Correct:** Search existing records before registration.

### Error 4 — Failing to Document Dependencies

**Incorrect:** Recording a server without its relevant service relationships.

**Correct:** Document dependencies needed for operational decisions.

### Error 5 — Recording Unverified Information as Fact

**Incorrect:** Claiming a server configuration has been verified without inspecting it.

**Correct:** Clearly identify verification status.

### Error 6 — Treating a Snapshot as an Approved Baseline

**Incorrect:** Labeling an initial configuration inventory as approved.

**Correct:** Distinguish proposed and approved baselines.

### Error 7 — Updating Records Before Changes Are Implemented

**Incorrect:** Recording a proposed configuration as the current state.

**Correct:** Update current-state information after implementation and verification.

### Error 8 — Ignoring CI Retirement

**Incorrect:** Leaving decommissioned systems marked Active.

**Correct:** Update lifecycle status and preserve relevant history.

### Error 9 — Publishing Sensitive Information

**Incorrect:** Storing credentials or private keys in GitHub.

**Correct:** Exclude secrets and sanitize sensitive documentation.

### Error 10 — Assuming GitHub Is a Full CMDB

**Incorrect:** Claiming that Markdown records provide all CMDB capabilities.

**Correct:** Describe the repository as a lightweight configuration documentation system.

---

## 32. Configuration Item Management Quality Checklist

### CI Identification

- [ ] Component identified
- [ ] Registration requirement evaluated
- [ ] Existing records checked
- [ ] Unique CI ID assigned
- [ ] CI category selected
- [ ] CI name recorded

### Configuration Documentation

- [ ] Purpose documented
- [ ] Environment identified
- [ ] Responsible role assigned
- [ ] Supported services identified
- [ ] Relevant technical attributes recorded
- [ ] Dependencies documented
- [ ] Lifecycle status assigned

### Verification

- [ ] Verification method identified
- [ ] Actual configuration inspected where possible
- [ ] Verification evidence preserved
- [ ] Discrepancies documented
- [ ] Last verified date recorded
- [ ] Baseline status accurately identified

### Security

- [ ] Credentials excluded
- [ ] Secrets excluded
- [ ] Sensitive information reviewed
- [ ] Public documentation sanitized
- [ ] Access requirements considered

### Operational Integration

- [ ] Related incidents linked when applicable
- [ ] Related problems linked when applicable
- [ ] Related changes linked when applicable
- [ ] Related events linked when applicable
- [ ] Infrastructure documentation referenced
- [ ] Dependency maps updated when necessary

### Lifecycle

- [ ] Current lifecycle status confirmed
- [ ] Configuration changes reflected accurately
- [ ] Ownership remains current
- [ ] Periodic verification considered
- [ ] Retirement requirements evaluated
- [ ] Historical information preserved

---

## 33. Configuration Item Management Performance Metrics

Configuration Management effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| CI Record Completeness | Measures required attribute coverage |
| CI Verification Rate | Tracks records verified against actual infrastructure |
| Configuration Accuracy Rate | Measures agreement between records and observed configuration |
| CI Ownership Coverage | Tracks CIs with assigned responsibility |
| Dependency Documentation Coverage | Measures recorded service relationships |
| Duplicate CI Rate | Identifies redundant configuration records |
| Configuration Discrepancy Rate | Measures mismatches between documented and actual configuration |
| Change-to-CI Update Compliance | Tracks configuration updates following implemented changes |
| CI Review Completion Rate | Measures completion of scheduled reviews |
| Retired CI Accuracy | Evaluates lifecycle status accuracy |
| Baseline Coverage | Tracks CIs with appropriate configuration baselines |
| Configuration Documentation Timeliness | Measures delays in updating records |

### Example Calculations

**CI Record Completeness**

```text
CI Record Completeness (%) =
Complete Required Attributes
---------------------------- x 100
Total Required Attributes
```

**CI Verification Rate**

```text
CI Verification Rate (%) =
Verified CI Records
------------------- x 100
Total In-Scope CI Records
```

**Configuration Accuracy Rate**

```text
Configuration Accuracy Rate (%) =
Verified Attributes Matching Actual Configuration
------------------------------------------------ x 100
Total Attributes Checked
```

### Measurement Considerations

- Define required fields by CI category.
- Use consistent verification criteria.
- Exclude irrelevant attributes.
- Distinguish simulated data from actual measurements.
- Do not invent audit or verification results.
- Review trends over time.

---

## 34. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Uses CI information to identify affected systems and route support requests |
| Incident Management | Uses CI records for impact assessment and troubleshooting |
| Service Request Management | May initiate predefined activities involving managed components |
| Knowledge Management | Maintains reusable configuration and troubleshooting guidance |
| Problem Management | Uses CI relationships during root cause investigation |
| Change Enablement | Assesses affected CIs and controls relevant configuration modifications |
| Monitoring and Event Management | Associates events and alerts with managed components |
| Service Configuration Management | Maintains accurate configuration records and relationships |
| Information Security Management | Uses CI information to support security oversight |
| Continual Improvement | Identifies and addresses configuration management weaknesses |

---

## 35. Related Procedures and Documentation

### Service Configuration Management

- [Service Configuration Management Overview](../README.md)
- [Configuration Item Template](../../Templates/Configuration-Item-Template.md)

### Change Enablement

- [Change Enablement Overview](../../Change-Enablement/)
- [Change Authorization](../../Change-Enablement/Procedures/Change-Authorization.md)
- [Change Implementation](../../Change-Enablement/Procedures/Change-Implementation.md)
- [Change Review](../../Change-Enablement/Procedures/Change-Review.md)

### Monitoring and Event Management

- [Monitoring and Event Management Overview](../../Monitoring-and-Event-Management/)
- [Event Detection](../../Monitoring-and-Event-Management/Procedures/Event-Detection.md)
- [Alert Triage](../../Monitoring-and-Event-Management/Procedures/Alert-Triage.md)
- [Event Escalation](../../Monitoring-and-Event-Management/Procedures/Event-Escalation.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Logging](../../Incident-Management/Procedures/Incident-Logging.md)
- [Incident Investigation](../../Incident-Management/Procedures/Incident-Investigation.md)

### Problem Management

- [Problem Management Overview](../../Problem-Management/)
- [Problem Identification](../../Problem-Management/Procedures/Problem-Identification.md)
- [Root Cause Analysis](../../Problem-Management/Procedures/Root-Cause-Analysis.md)

### Other ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

### Infrastructure Documentation

- [Infrastructure Overview](../../Infrastructure/)
- [Active Directory](../../Infrastructure/Active-Directory/)
- [Windows Server](../../Infrastructure/Windows-Server/)
- [Microsoft 365](../../Infrastructure/Microsoft-365/)
- [Networking](../../Infrastructure/Networking/)
- [Virtualization](../../Infrastructure/Virtualization/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

---

## 36. Procedure Review

This procedure should be reviewed when:

- Configuration management responsibilities change.
- New infrastructure technologies are introduced.
- CI classification requirements change.
- Configuration verification requirements change.
- Change Enablement procedures are updated.
- Service dependency documentation changes.
- New cloud services are introduced.
- Significant configuration discrepancies are identified.
- CI records become outdated.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Configuration Item Management procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Organizational roles, service ownership, configuration approval workflows, lifecycle decisions, and operational scenarios may be simulated.

Infrastructure configuration, technical commands, Configuration Item attributes, dependency relationships, verification results, and technical findings are documented based on hands-on lab activities where indicated.

Proposed Configuration Items, baselines, cloud resources, and dependency relationships must not be represented as deployed, approved, or verified until appropriate evidence exists.

Expected configurations and hypothetical discrepancies must not be represented as actual technical observations.

GitHub publication does not imply operation of a production CMDB, independent technical approval, or employment experience.

This procedure demonstrates ITIL-aligned Service Configuration Management, Configuration Item registration, configuration verification, dependency mapping, lifecycle management, change traceability, and infrastructure documentation practices.
