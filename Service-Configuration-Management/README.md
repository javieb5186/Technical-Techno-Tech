# Technical Techno Tech — Service Configuration Management

## Overview

Service Configuration Management is responsible for maintaining accurate and reliable information about IT services, infrastructure components, and their relationships within **Technical Techno Tech (TTT)**, a fictional technology solutions company.

The practice helps IT personnel understand which systems support business services, how infrastructure components depend on one another, and how configuration changes may affect service availability, performance, and security.

Technical Techno Tech maintains structured Configuration Item (CI) records for servers, workstations, network devices, cloud services, and other components supporting its internal IT operations.

The practice supports ITIL-aligned Incident Management, Problem Management, Change Enablement, Monitoring and Event Management, and Information Security Management.

Technical Techno Tech applies Service Configuration Management principles through hands-on infrastructure deployment, configuration documentation, dependency mapping, and configuration verification in controlled lab environments.

---

## Purpose

The purpose of Service Configuration Management is to ensure that accurate and reliable information about IT services and their supporting Configuration Items is available when needed.

Primary objectives include:

- Identify important IT infrastructure components.
- Maintain accurate Configuration Item records.
- Document technical configurations.
- Track relationships between infrastructure components.
- Identify dependencies supporting business services.
- Support incident investigation and troubleshooting.
- Improve change impact assessments.
- Support infrastructure monitoring.
- Maintain configuration history.
- Identify unauthorized or unexpected configuration changes.
- Support asset and infrastructure lifecycle management.
- Improve service reliability and operational visibility.

**Key Principle:** Service Configuration Management focuses on understanding what infrastructure exists, how it is configured, and how its components relate to the services they support.

---

## Scope of Service Configuration Management

### In Scope

Service Configuration Management may include:

- Windows servers
- Domain controllers
- Workstations
- Virtual machines
- Network routers
- Network switches
- Firewalls
- Wireless infrastructure
- Microsoft 365 services
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure resources
- DNS and DHCP services
- Active Directory infrastructure
- Service dependencies
- Configuration baselines
- Infrastructure relationships
- Configuration verification
- Configuration lifecycle tracking

The level of documentation depends on the importance of the component and its role in service delivery.

### Out of Scope

Activities primarily handled through other practices include:

- Routine employee support interactions
- Individual incident troubleshooting records
- Problem root cause investigations
- Change authorization
- Service request fulfillment
- General knowledge article creation
- Financial asset accounting

Service Configuration Management may provide information to support these activities.

---

## Configuration Item Definition

A **Configuration Item (CI)** is any component that needs to be managed in order to deliver an IT service.

Configuration Items may include physical devices, virtual resources, software components, cloud services, or other elements relevant to service delivery.

### Examples

| Configuration Item | CI Type | Example |
|---|---|---|
| DC01 | Server | Active Directory Domain Controller |
| DC02 | Server | Additional Domain Controller |
| MGMT01 | Workstation | Administrative Workstation |
| CLIENT01 | Workstation | Domain-Joined Employee Workstation |
| Core Switch | Network Device | Network Infrastructure |
| OPNsense Firewall | Network Device | Firewall and Routing |
| Microsoft Entra ID | Cloud Service | Identity Management |
| Microsoft Intune | Cloud Service | Endpoint Management |
| Microsoft 365 Tenant | Cloud Service | Cloud Productivity and Administration |

These examples represent potential Configuration Items within the TTT lab environment.

Actual CI records should reflect deployed and verified configurations.

---

## Configuration Item vs. IT Asset

A Configuration Item and an IT asset are related concepts, but they serve different management purposes.

### Configuration Item

Focuses on:

- Technical configuration
- Service relationships
- Dependencies
- Operational status
- Change history
- Service impact

### IT Asset

Focuses on:

- Ownership
- Financial value
- Procurement
- Licensing
- Warranty
- Asset lifecycle
- Cost management

### Example

A workstation may be both an IT asset and a Configuration Item.

**IT Asset Information:**

- Purchase date
- Purchase cost
- Warranty
- Assigned employee
- Asset tag

**Configuration Item Information:**

- Hostname
- Operating system
- IP configuration
- Domain membership
- Installed management software
- Related services
- Configuration dependencies

Technical Techno Tech primarily focuses on configuration information relevant to IT service delivery.

---

## Configuration Management System

A **Configuration Management System (CMS)** provides the information and tools needed to manage configuration data and relationships.

A **Configuration Management Database (CMDB)** is a repository used to store information about Configuration Items and their relationships.

### Technical Techno Tech Approach

Technical Techno Tech uses structured GitHub documentation to maintain configuration records and dependency information.

The repository serves as a documentation-based configuration register for the lab.

It is not represented as a fully implemented enterprise CMDB.

### Configuration Information Sources

Configuration information may be obtained from:

- Windows Server
- Active Directory
- PowerShell
- Windows Admin Center
- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Microsoft Azure
- VMware
- Network device configurations
- Administrative verification commands

Information should be verified against the actual lab environment when practical.

---

## Configuration Item Categories

Technical Techno Tech organizes Configuration Items into four primary categories.

### 1. Servers

Includes physical and virtual servers providing infrastructure services.

Examples:

- Domain controllers
- DNS servers
- DHCP servers
- File servers
- Application servers
- Management servers

### 2. Workstations

Includes employee and administrative endpoints.

Examples:

- Domain-joined Windows workstations
- Administrative workstations
- Managed employee laptops
- Test endpoints

### 3. Network Devices

Includes infrastructure supporting network connectivity and security.

Examples:

- Routers
- Switches
- Firewalls
- Wireless access points
- Virtual network appliances

### 4. Cloud Services

Includes managed cloud resources and services.

Examples:

- Microsoft 365 tenant
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure virtual machines
- Azure networking resources

Additional CI categories may be introduced as the lab environment expands.

---

## Service Configuration Management Responsibilities

### Configuration Management Owner

The configuration management owner coordinates the maintenance of CI information.

Responsibilities include:

- Defining documentation standards
- Maintaining the configuration register
- Identifying required CI attributes
- Reviewing configuration accuracy
- Tracking CI relationships
- Coordinating configuration updates
- Supporting configuration audits

### Systems Administration

Systems Administrators maintain configuration information involving:

- Windows Server
- Active Directory
- DNS and DHCP
- Group Policy
- Virtual machines
- Server roles
- Server dependencies

### Network Administration

Network Administrators maintain configuration information involving:

- Routers
- Switches
- Firewalls
- IP addressing
- VLANs
- Network topology
- Routing
- Network dependencies

### Endpoint Administration

Endpoint Administrators maintain configuration information involving:

- Workstations
- Operating systems
- Device enrollment
- Endpoint policies
- Installed applications
- Device management relationships

### Cloud Administration

Cloud Administrators maintain configuration information involving:

- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Cloud resource dependencies
- Cloud service configurations

### Information Security

Information Security personnel may review:

- Sensitive configuration information
- Privileged access relationships
- Security configurations
- Configuration compliance
- Unauthorized configuration changes

**Note:** These responsibilities represent simulated IT roles within the lab environment and do not imply that separate employees or teams are operating the environment.

---

## Configuration Item Lifecycle

Technical Techno Tech follows a structured Configuration Item lifecycle.

### 1. Identification

Determine whether a component should be tracked as a Configuration Item.

Considerations include:

- Business importance
- Service dependencies
- Technical complexity
- Security requirements
- Operational risk
- Change impact
- Monitoring requirements

### 2. Registration

Create a Configuration Item record.

Information may include:

- CI identifier
- CI name
- CI type
- Description
- Operational status
- Responsible role
- Technical specifications
- Supported services
- Related Configuration Items

### 3. Configuration Documentation

Record the relevant technical configuration.

Examples include:

- Hostname
- Operating system
- IP address
- Domain membership
- Installed roles
- Network configuration
- Cloud resource information
- Management tools
- Security settings

### 4. Relationship Mapping

Identify relationships between the CI and other components.

Examples include:

- Workstation depends on DNS.
- Domain controller provides authentication.
- Application server depends on a database.
- Network device provides connectivity.
- Managed endpoint depends on cloud management services.

### 5. Configuration Verification

Verify that documented configuration information matches the actual environment.

Methods may include:

- PowerShell queries
- Administrative console review
- Network configuration checks
- Server role verification
- Cloud resource inspection

### 6. Configuration Maintenance

Update CI information when relevant changes occur.

Examples include:

- Operating system upgrades
- IP address changes
- Server role modifications
- Network configuration changes
- Device replacement
- Cloud service changes
- Infrastructure migrations

### 7. Retirement

A Configuration Item may be retired when it is no longer required.

Retirement documentation may include:

- Retirement date
- Reason for retirement
- Related change record
- Data retention considerations
- Service dependency updates
- Final operational status

---

## Configuration Item Identification

Each Configuration Item receives a unique identifier.

**Format: CI-XXX — Configuration Item Name**

Examples:

- CI-001 — DC01
- CI-002 — DC02
- CI-003 — MGMT01
- CI-004 — CLIENT01
- CI-005 — Core Switch
- CI-006 — OPNsense Firewall
- CI-007 — Microsoft 365 Tenant

These identifiers are illustrative until assigned to actual records.

### Naming Standards

Configuration Item names should:

- Clearly identify the component.
- Use consistent naming conventions.
- Avoid duplicate identifiers.
- Reflect the actual infrastructure.
- Remain understandable to other IT personnel.

---

## Configuration Item Attributes

CI records should contain enough information to support operational management.

### General Information

| Attribute | Description |
|---|---|
| CI ID | Unique configuration identifier |
| CI Name | Component name |
| CI Type | Server, workstation, network device, cloud service, etc. |
| Description | Purpose of the component |
| Operational Status | Planned, active, maintenance, retired |
| Responsible Role | Role responsible for maintaining the CI |
| Supported Service | IT service supported by the component |

### Technical Information

| Attribute | Description |
|---|---|
| Hostname | System hostname, when applicable |
| Operating System | Installed operating system |
| IP Address | Relevant network address |
| Domain | Domain membership or directory relationship |
| Server Roles | Installed or assigned roles |
| Software | Relevant installed software |
| Management Platform | Administrative or monitoring platform |
| Virtualization Platform | Hypervisor or hosting environment |

### Relationship Information

| Attribute | Description |
|---|---|
| Depends On | Components required for operation |
| Provides Service To | Components or services supported |
| Connected To | Relevant infrastructure connections |
| Related Changes | Changes affecting the CI |
| Related Incidents | Incidents involving the CI |
| Related Problems | Problems involving the CI |

Not every attribute applies to every CI type.

---

## Configuration Baselines

A **configuration baseline** is a documented and agreed reference configuration used to evaluate future changes.

Baselines help identify deviations from expected settings.

### Example: Domain Controller Baseline

A domain controller baseline may include:

- Operating system version
- Hostname
- Static IP configuration
- DNS settings
- Domain membership
- Installed AD DS role
- DNS Server role
- Time synchronization configuration
- Security settings
- Monitoring requirements

### Baseline Management

Configuration baselines should:

1. Identify expected settings.
2. Record the configuration version or date.
3. Document applicable approval when required.
4. Support comparison with actual settings.
5. Be updated following authorized changes.

A baseline should not be marked verified unless its settings have been checked against the actual environment.

---

## Configuration Verification

Configuration verification helps maintain accurate CI records.

### Verification Objectives

- Confirm documented configurations.
- Identify outdated information.
- Detect unexpected differences.
- Validate infrastructure relationships.
- Support change reviews.
- Improve troubleshooting accuracy.

### Windows Server Verification

Example commands:

```powershell
# Display computer information
Get-ComputerInfo

# Display network configuration
Get-NetIPConfiguration

# Display installed Windows Server roles
Get-WindowsFeature | Where-Object Installed

# Display computer domain information
Get-CimInstance Win32_ComputerSystem
```

### Active Directory Verification

Example commands:

```powershell
# List domain controllers
Get-ADDomainController -Filter *

# Display domain information
Get-ADDomain

# Display forest information
Get-ADForest

# Display Active Directory sites
Get-ADReplicationSite -Filter *
```

### Network Verification

Example commands:

```powershell
# Display IP addresses
Get-NetIPAddress

# Display network adapters
Get-NetAdapter

# Display routing information
Get-NetRoute

# Test network connectivity
Test-Connection -ComputerName DC01 -Count 4
```

Commands require appropriate tools, permissions, and applicable operating systems.

Verification results should be documented when used as evidence.

---

## Configuration Relationships & Dependencies

Configuration relationships help explain how infrastructure components support one another.

### Example: Active Directory Infrastructure

```text
Employee Workstation
        |
        v
Network Infrastructure
        |
        v
DNS Service
        |
        v
Active Directory Domain Controller
        |
        v
Authentication and Directory Services
```

This diagram illustrates a simplified dependency model. Actual authentication and DNS interactions may involve multiple components and paths.

### Example Relationships

| Configuration Item | Relationship | Related Component |
|---|---|---|
| CLIENT01 | Uses directory services provided by | DC01 / DC02 |
| CLIENT01 | Uses DNS services provided by | Configured DNS Server |
| DC01 | Replicates Active Directory data with | DC02 |
| MGMT01 | Administratively manages | Domain Infrastructure |
| Domain Controllers | Depend on connectivity through | Network Infrastructure |
| Managed Workstation | Receives cloud management through | Microsoft Intune |

Relationships must be verified against the actual lab configuration before being recorded as implemented.

---

## Dependency Mapping

Dependency maps provide a visual representation of infrastructure relationships.

### Purpose

Dependency mapping helps IT personnel:

- Identify affected services during incidents.
- Understand infrastructure dependencies.
- Assess change impact.
- Identify potential single points of failure.
- Support recovery planning.
- Improve operational troubleshooting.

### Dependency Map Directory

```text
Service-Configuration-Management/
└── Dependency-Maps/
    ├── Active-Directory-Dependencies.md
    ├── Network-Dependencies.md
    └── Cloud-Service-Dependencies.md
```

These are proposed documentation examples. Create maps as the related infrastructure is documented.

### Dependency Mapping Standards

Maps should:

- Clearly identify components.
- Describe meaningful relationships.
- Distinguish direct and indirect dependencies where useful.
- Reflect verified infrastructure.
- Identify critical service dependencies.
- Be updated following relevant changes.

---

## Configuration Item Status

| Status | Description |
|---|---|
| Planned | Component is proposed but not yet deployed |
| Provisioning | Component is being configured |
| Active | Component is operational |
| Maintenance | Component is undergoing maintenance |
| Degraded | Component is operating with reduced functionality |
| Retired | Component is no longer in active service |

Status information should reflect the documented state of the component.

---

## Configuration Management Repository

Technical Techno Tech maintains configuration documentation in the following directory.

### Directory Structure

```text
Service-Configuration-Management/
├── README.md
├── Procedures/
├── Configuration-Items/
│   ├── Servers/
│   ├── Workstations/
│   ├── Network-Devices/
│   └── Cloud-Services/
└── Dependency-Maps/
```

### Example CI Record

```text
Configuration-Items/
└── Servers/
    └── CI-001-DC01/
        ├── README.md
        └── Evidence/
```

Each CI record follows the standardized [Configuration Item Template](../Templates/Configuration-Item-Template.md).

---

## Configuration Item Register

The following register tracks documented Configuration Items.

| CI ID | Configuration Item | CI Type | Status |
|---|---|---|---|
| CI-XXX | [CI Name] | [CI Type] | [Status] |

Add Configuration Items to this register as they are documented. Remove placeholder entries until actual records exist.

### Register Maintenance

The register should be updated when:

- A new CI is created.
- An existing CI is modified.
- A CI changes operational status.
- A CI is retired.
- A relevant dependency changes.

---

## Service Configuration Management Procedures

The `Procedures/` directory contains repeatable configuration management instructions.

| Procedure | Purpose | Status |
|---|---|---|
| CI Identification | Defines which components should be tracked | Planned |
| CI Registration | Defines how Configuration Items are recorded | Planned |
| CI Attribute Maintenance | Defines required configuration information | Planned |
| Configuration Verification | Defines configuration accuracy checks | Planned |
| Relationship Mapping | Defines dependency documentation | Planned |
| CI Lifecycle Management | Defines creation, modification, and retirement processes | Planned |
| Configuration Review | Defines periodic documentation review | Planned |

Procedures will be developed and refined as the infrastructure documentation expands.

---

## Integration With Incident Management

Configuration information supports technical troubleshooting and impact assessment.

### Example

**Incident:** Employees cannot authenticate to Active Directory.

The technician may review Configuration Item records to identify:

- Available domain controllers
- DNS server configurations
- Affected workstations
- Network dependencies
- Authentication service relationships

The incident record documents the service interruption and troubleshooting.

The CI records provide information about the affected infrastructure.

**Reference:** [Incident Management](../Incident-Management/)

---

## Integration With Problem Management

Configuration information supports investigations into recurring technical failures.

### Example

**Problem:** Recurring authentication failures across multiple workstations.

Problem Management may use configuration records to:

- Compare workstation DNS settings.
- Identify common infrastructure dependencies.
- Review domain controller relationships.
- Examine configuration history.
- Identify unexpected configuration differences.

**Reference:** [Problem Management](../Problem-Management/)

---

## Integration With Change Enablement

Changes may create, modify, or retire Configuration Items.

### Example

**Change:** Deploy a second domain controller.

**Change Enablement:**

- Assesses risks.
- Plans implementation.
- Coordinates authorization.
- Documents deployment.
- Validates results.

**Service Configuration Management:**

- Registers the new domain controller.
- Documents its configuration.
- Records its service relationships.
- Updates Active Directory dependency maps.
- Maintains the CI's lifecycle information.

### Documentation Relationship

- **Change Record:** Explains why and how the modification occurred.
- **Configuration Item Record:** Describes the component and its current documented configuration.

**Reference:** [Change Enablement](../Change-Enablement/)

---

## Integration With Monitoring and Event Management

Configuration records help identify which infrastructure components require monitoring.

### Example

**Configuration Item:** DC01

Potential monitoring requirements include:

- Server availability
- DNS service status
- Active Directory replication
- CPU utilization
- Memory utilization
- Disk capacity
- Time synchronization

Monitoring events may reference the affected Configuration Item.

**Reference:** [Monitoring and Event Management](../Monitoring-and-Event-Management/)

---

## Integration With Information Security Management

Configuration information supports security administration and risk assessment.

Potential activities include:

- Identifying privileged infrastructure
- Reviewing security configurations
- Documenting administrative access
- Identifying unsupported operating systems
- Reviewing configuration compliance
- Investigating unauthorized changes
- Understanding security dependencies

Sensitive configuration information should be protected from unauthorized disclosure.

**Reference:** [Information Security Management](../Information-Security-Management/)

---

## Integration With Knowledge Management

Configuration documentation and knowledge articles serve different purposes.

### Configuration Item Record

Documents the current configuration and relationships of a specific component.

### Knowledge Article

Provides reusable instructions for administering or troubleshooting a technology.

### Example

**CI-001 — DC01**

Documents:

- Hostname
- Operating system
- Network configuration
- Installed server roles
- Domain information
- Service dependencies

**KB-001 — Promote a Windows Server to a Domain Controller**

Documents:

- Prerequisites
- Installation steps
- Administrative commands
- Validation procedures
- Troubleshooting guidance

**Reference:** [Knowledge Management](../Knowledge-Management/)

---

## Integration With Other ITIL Practices

| Management Practice | Relationship to Service Configuration Management |
|---|---|
| Service Desk | Uses CI information to identify affected systems |
| Incident Management | Uses configuration relationships during troubleshooting |
| Service Request Management | May create or modify tracked resources |
| Knowledge Management | Maintains reusable configuration and administration instructions |
| Problem Management | Uses configuration data to investigate underlying causes |
| Change Enablement | Controls changes affecting Configuration Items |
| Monitoring and Event Management | Associates monitoring data with infrastructure components |
| Information Security Management | Uses configuration data to assess security risks |
| Continual Improvement | Identifies documentation and configuration management improvements |

Service Configuration Management supports multiple ITIL-aligned practices without requiring every infrastructure detail to become a separate Configuration Item.

---

## Service Configuration Management Performance Metrics

Service Configuration Management effectiveness may be evaluated using operational metrics.

| Metric | Purpose |
|---|---|
| CI Coverage | Measures the proportion of relevant components documented |
| Configuration Accuracy | Evaluates whether CI records match actual configurations |
| Relationship Completeness | Measures documented infrastructure dependencies |
| Outdated CI Records | Identifies configuration information requiring updates |
| Unregistered Components | Identifies relevant infrastructure missing from the register |
| CI Review Compliance | Tracks scheduled configuration reviews |
| Change-to-CI Update Completion | Tracks configuration updates following changes |
| Retired CI Accuracy | Evaluates whether retired components are correctly documented |

Metrics will be introduced when sufficient configuration data becomes available.

Findings may support improvement initiatives under [Continual Improvement](../Continual-Improvement/).

---

## Continual Improvement

Service Configuration Management contributes to continual improvement by maintaining accurate infrastructure information and identifying documentation gaps.

Potential improvements include:

- Expanding CI coverage
- Improving configuration accuracy
- Standardizing CI naming conventions
- Automating configuration discovery
- Improving dependency maps
- Reducing outdated records
- Strengthening configuration verification
- Improving integration with Change Enablement
- Identifying critical infrastructure dependencies
- Improving configuration review procedures

Improvements should be based on observed configuration discrepancies and operational requirements.

---

## Documentation Standards

Configuration Item records should:

1. Clearly identify the component.
2. Assign a unique CI identifier.
3. Document the component's operational purpose.
4. Identify supported IT services.
5. Record relevant technical specifications.
6. Document important configuration settings.
7. Identify related Configuration Items.
8. Describe service dependencies.
9. Record configuration baselines when applicable.
10. Link relevant change, incident, and problem records.
11. Include technical verification evidence when available.
12. Document configuration updates.
13. Identify operational status.
14. Protect sensitive infrastructure information.
15. Distinguish planned configurations from deployed configurations.
16. Reflect actual lab configurations rather than invented technical details.

---

## Related Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Operational Scenarios](../Scenarios/)
- [Service Desk](../Service-Desk/)
- [Incident Management](../Incident-Management/)
- [Service Request Management](../Service-Request-Management/)
- [Knowledge Management](../Knowledge-Management/)
- [Problem Management](../Problem-Management/)
- [Change Enablement](../Change-Enablement/)
- [Monitoring and Event Management](../Monitoring-and-Event-Management/)
- [Information Security Management](../Information-Security-Management/)
- [Continual Improvement](../Continual-Improvement/)
- [Infrastructure Documentation](../Infrastructure/)
- [Configuration Item Template](../Templates/Configuration-Item-Template.md)

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Configuration ownership, operational responsibilities, service relationships, and management workflows may be simulated.

Technical configurations, infrastructure components, verification commands, and dependency relationships are documented based on hands-on work performed in controlled lab environments where indicated.

This documentation demonstrates practical infrastructure administration, configuration documentation, dependency analysis, and IT service management knowledge rather than employment experience within an actual production organization.
