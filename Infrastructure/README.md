x# Technical Techno Tech — IT Infrastructure

## Overview

The Infrastructure directory documents the internal IT environment supporting **Technical Techno Tech (TTT)**, a fictional technology solutions company developed for hands-on IT training and professional portfolio development.

This environment simulates the infrastructure of a growing organization that requires centralized identity management, reliable networking, endpoint administration, server infrastructure, cloud services, and secure IT operations.

The infrastructure is developed through practical lab exercises involving Windows Server, Active Directory Domain Services, Microsoft 365, Microsoft Entra ID, Microsoft Intune, Microsoft Azure, Hyper-V, OPNsense, VyOS, and PowerShell.

The objective is to design, deploy, configure, administer, troubleshoot, secure, and maintain infrastructure using real-world IT administration techniques.

Infrastructure documentation also supports Technical Techno Tech's ITIL-aligned service management practices.

---

## Purpose

The purpose of this directory is to maintain centralized technical documentation for the organization's internal IT infrastructure.

Primary objectives include:

- Document infrastructure architecture and design.
- Maintain accurate technical configuration information.
- Explain the purpose of deployed technologies.
- Record server and workstation configurations.
- Document Active Directory architecture.
- Maintain network topology and addressing information.
- Document cloud service configurations.
- Explain infrastructure dependencies.
- Support technical troubleshooting.
- Support infrastructure expansion and maintenance.
- Provide evidence of hands-on technical administration.
- Connect technical infrastructure with IT service management activities.

**Key Principle:** Infrastructure documentation explains how the environment is designed, configured, and operated. ITIL management records explain the business and operational activities involving that infrastructure.

---

## Infrastructure Scope

Technical Techno Tech's infrastructure documentation is organized into five primary areas.

| Infrastructure Area | Primary Purpose |
|---|---|
| Active Directory | Centralized identity, authentication, and directory administration |
| Windows Server | Server operating systems, roles, and infrastructure services |
| Microsoft 365 | Cloud identity, productivity, endpoint management, and administration |
| Networking | Connectivity, routing, switching, segmentation, and network security |
| Virtualization | Virtual machine deployment, hosting, and virtual networking |

Microsoft Azure resources are documented within the relevant cloud or server infrastructure sections as the environment expands.

---

## Infrastructure Directory Structure

```text
Infrastructure/
├── README.md
├── Active-Directory/
│   ├── Domain-Architecture.md
│   ├── Organizational-Units.md
│   └── Group-Structure.md
├── Windows-Server/
│   ├── Server-Inventory.md
│   └── Server-Roles.md
├── Microsoft-365/
│   ├── Tenant-Overview.md
│   ├── Entra-ID/
│   └── Intune/
├── Networking/
│   ├── Network-Topology.md
│   ├── OPNsense/
│   └── VyOS/
└── Virtualization/
    └── Hyper-V/
```

This structure represents the intended documentation organization.

Files and directories will be populated as the corresponding infrastructure components and lab activities are documented.

---

## Infrastructure Design Objectives

The Technical Techno Tech environment is designed to simulate the infrastructure requirements of a small organization that can expand over time.

### Centralized Administration

Provide centralized management of:

- User accounts
- Computer accounts
- Security groups
- Authentication
- Authorization
- Device configurations
- Server infrastructure
- Cloud identities

### Reliability

Support reliable IT operations through:

- Appropriate infrastructure redundancy
- Service health monitoring
- Backup and recovery planning
- Dependency documentation
- Controlled configuration changes
- Technical validation

### Security

Protect infrastructure through:

- Least-privilege access
- Role-based administration
- Security groups
- Group Policy
- Multifactor authentication
- Firewall controls
- Network segmentation
- Security monitoring

### Scalability

Design infrastructure that can support:

- Additional employees
- New departments
- Additional workstations
- New servers
- Expanded network segments
- Cloud services
- Hybrid infrastructure

### Maintainability

Maintain infrastructure through:

- Standardized configurations
- Technical documentation
- Administrative procedures
- Configuration verification
- Monitoring
- Automation
- Change tracking

---

## Infrastructure Architecture

Technical Techno Tech uses a combination of local virtual infrastructure, simulated network environments, and Microsoft cloud services.

### Architecture Layers

| Layer | Components | Purpose |
|---|---|---|
| Identity | Active Directory, Microsoft Entra ID | Authentication and identity administration |
| Server | Windows Server | Directory, DNS, and other infrastructure services |
| Endpoint | Windows workstations | Employee and administrative computing |
| Network | Routers, switches, firewalls | Connectivity and traffic control |
| Virtualization | Hyper-V | Virtual infrastructure hosting |
| Cloud | Microsoft 365, Intune, Azure | Cloud administration and services |
| Management | PowerShell, RSAT, Windows Admin Center | Infrastructure administration |

Not all technologies are necessarily integrated into a single live environment.

Individual labs may operate independently until an integration is implemented and verified.

---

## Active Directory Infrastructure

**Directory:** `Active-Directory/`

Active Directory Domain Services provides centralized identity and directory administration for the Windows domain environment.

### Primary Functions

- User authentication
- Computer authentication
- Directory services
- Security group management
- Organizational Unit management
- Group Policy administration
- Administrative delegation
- Domain controller replication
- Identity-related infrastructure services

### Lab Domain

The Windows Server lab uses the following domain:

**Domain:** `homelab.local`

### Domain Controllers

The lab includes the following domain controller systems:

| Hostname | Role | Operating Environment |
|---|---|---|
| DC01 | Domain Controller | Windows Server with Desktop Experience |
| DC02 | Additional Domain Controller | Windows Server Core |

Domain controller configurations and operational status should be verified and maintained in the relevant technical records.

### Active Directory Documentation

| Document | Purpose |
|---|---|
| `Domain-Architecture.md` | Domain structure, domain controllers, replication, and directory architecture |
| `Organizational-Units.md` | OU structure and administrative organization |
| `Group-Structure.md` | Security groups, group scopes, and permission relationships |

### Administrative Activities

Hands-on activities may include:

- Creating users and groups
- Organizing directory objects
- Configuring Group Policy
- Delegating administrative permissions
- Managing domain controllers
- Verifying replication
- Configuring directory-related services
- Performing backup and recovery operations

---

## Windows Server Infrastructure

**Directory:** `Windows-Server/`

Windows Server provides infrastructure services supporting the internal IT environment.

### Primary Functions

- Active Directory Domain Services
- DNS
- Server administration
- Authentication infrastructure
- Administrative management
- Infrastructure monitoring
- Backup and recovery

Additional server roles may be introduced as the lab expands.

### Server Inventory

The server inventory documents:

- Hostnames
- Operating systems
- Server roles
- Network configurations
- Domain membership
- Virtualization information
- Operational status

**Document:** `Windows-Server/Server-Inventory.md`

### Server Roles

Server role documentation explains:

- Installed server roles
- Business and technical purpose
- Configuration requirements
- Dependencies
- Administrative tools
- Validation procedures

**Document:** `Windows-Server/Server-Roles.md`

### Administrative Tools

Windows Server administration may involve:

- Server Manager
- Windows Admin Center
- Active Directory Administrative Center
- Active Directory Users and Computers
- Remote Server Administration Tools
- PowerShell
- Windows Event Viewer
- Windows Server Backup

---

## Microsoft 365 Infrastructure

**Directory:** `Microsoft-365/`

Microsoft 365 provides cloud-based identity, administration, productivity, and endpoint management capabilities.

### Primary Technologies

- Microsoft 365 Admin Center
- Microsoft Entra ID
- Microsoft Intune
- Microsoft 365 licensing and user administration

### Tenant Documentation

**Document:** `Microsoft-365/Tenant-Overview.md`

The tenant overview may document:

- Tenant purpose
- Tenant identity
- Administrative roles
- User administration
- Licensing
- Security requirements
- Connected services
- Operational limitations

Sensitive tenant information and credentials must not be published.

### Microsoft Entra ID

**Directory:** `Microsoft-365/Entra-ID/`

Microsoft Entra ID supports cloud identity and access management.

Potential activities include:

- User account administration
- Security group management
- Administrative role assignment
- Multifactor authentication
- Device registration
- Sign-in monitoring
- Access management

### Microsoft Intune

**Directory:** `Microsoft-365/Intune/`

Microsoft Intune supports endpoint management.

Potential activities include:

- Device enrollment
- Configuration profiles
- Compliance policies
- Application deployment
- Endpoint security
- Device administration
- Windows update management

### Hybrid Identity

Future infrastructure exercises may explore integration between Active Directory Domain Services and Microsoft Entra ID.

Potential topics include:

- Identity synchronization
- Hybrid identity administration
- Authentication models
- Device identity
- Hybrid endpoint management

Hybrid integration should only be documented as implemented after configuration and validation.

---

## Microsoft Azure Infrastructure

Microsoft Azure may be used to extend the infrastructure beyond the local virtualization environment.

### Potential Azure Resources

- Azure Virtual Machines
- Azure Virtual Networks
- Network Security Groups
- Azure storage
- Azure Monitor
- Hybrid infrastructure services

### Azure Learning Objectives

Potential activities include:

- Deploying Windows Server virtual machines
- Configuring virtual networking
- Managing cloud resources
- Monitoring virtual machines
- Evaluating cloud infrastructure costs
- Exploring hybrid server administration

### Cost Management

Azure resources may generate usage charges.

Lab planning should consider:

- Virtual machine compute costs
- Storage costs
- Networking charges
- Monitoring charges
- Resource cleanup
- Budget alerts

Stopping a virtual machine from within its operating system does not necessarily stop Azure compute billing. Deallocation is generally required to stop VM compute charges, while storage and certain other resources may continue to incur costs.

Azure infrastructure records should identify actual deployed resources rather than proposed configurations.

---

## Network Infrastructure

**Directory:** `Networking/`

Network infrastructure provides connectivity between servers, workstations, administrative systems, and supporting services.

### Primary Functions

- Network connectivity
- IP addressing
- Routing
- Switching
- Network segmentation
- DNS communication
- DHCP services
- Firewall enforcement
- Network troubleshooting
- Network monitoring

### Networking Technologies

The portfolio includes networking exercises involving:

- Routers
- Switches
- VLANs
- IP subnetting
- Routing
- Wireless networking
- OPNsense
- VyOS

### Network Documentation

**Document:** `Networking/Network-Topology.md`

The network topology document may include:

- Network diagrams
- Device roles
- IP address assignments
- Subnet information
- VLAN assignments
- Routing relationships
- Firewall placement
- Network dependencies

### OPNsense

**Directory:** `Networking/OPNsense/`

OPNsense provides firewall and routing capabilities for networking labs.

Potential activities include:

- Firewall rules
- Interface configuration
- Routing
- Network segmentation
- Network address translation
- Traffic monitoring

### VyOS

**Directory:** `Networking/VyOS/`

VyOS provides software-based routing and networking capabilities.

Potential activities include:

- Interface configuration
- Static routing
- Routing protocols
- Firewall configuration
- Network troubleshooting
- Virtual network integration

---

## Virtualization Infrastructure

**Directory:** `Virtualization/`

Virtualization provides the foundation for deploying multiple operating systems and infrastructure components in controlled lab environments.

### VMware

**Directory:** `Virtualization/Hyper-V/`

VMware is used to create and administer virtual machines supporting the Windows Server and workstation labs.

### Virtual Machine Roles

| Virtual Machine | Purpose |
|---|---|
| DC01 | Primary domain controller in the lab |
| DC02 | Additional domain controller |
| MGMT01 | Administrative workstation |
| CLIENT01 | Domain-joined workstation |

### Virtualization Activities

Potential activities include:

- Creating virtual machines
- Installing operating systems
- Configuring virtual hardware
- Managing virtual disks
- Configuring virtual networking
- Connecting virtual machines
- Managing resource allocation
- Performing backup and recovery exercises

### Virtual Networking

Virtual networking may include:

- NAT
- Bridged networking
- Host-only networking
- Virtual network segmentation
- Internal connectivity testing

The selected network mode depends on the lab's technical requirements.

### Virtualization Documentation

Documentation should identify:

- Hypervisor
- Virtual machine name
- Operating system
- Virtual CPU allocation
- Memory allocation
- Virtual storage
- Network adapter configuration
- Network mode
- Dependencies
- Operational status

---

## Infrastructure Inventory

The following table provides a high-level overview of the Windows Server lab components.

| Component | Type | Purpose |
|---|---|---|
| DC01 | Windows Server VM | Active Directory and supporting services |
| DC02 | Windows Server Core VM | Additional domain controller |
| MGMT01 | Windows Workstation VM | Administrative management |
| CLIENT01 | Windows Workstation VM | Domain-joined client testing |

Detailed configuration information belongs in the relevant infrastructure documents and Configuration Item records.

Additional devices and services should be added as they are deployed and documented.

---

## Infrastructure Networking Reference

The Windows Server lab has used the following IP assignments:

| System | IP Address | Subnet |
|---|---|---|
| DC01 | 10.20.10.10 | 10.20.10.0/24 |
| DC02 | 10.20.10.11 | 10.20.10.0/24 |
| MGMT01 | 10.20.30.10 | 10.20.30.0/24 |
| CLIENT01 | 10.20.20.10 | 10.20.20.0/24 |

These values represent documented lab configurations and should be reverified before being treated as the current environment.

Routing, DNS, gateway assignments, and virtual network connectivity should be documented separately.

---

## Infrastructure Dependencies

Infrastructure components frequently depend on other systems and services.

### Example: Domain Authentication

A domain-joined workstation may require:

- Network connectivity
- DNS resolution
- Access to a domain controller
- Appropriate authentication services

### Example: Administrative Management

An administrative workstation may require:

- Network connectivity
- Appropriate administrative credentials
- Remote management permissions
- RSAT or other management tools
- Access to target servers

### Example: Cloud Endpoint Management

A managed endpoint may require:

- Internet connectivity
- Microsoft Entra ID identity
- Appropriate licensing
- Microsoft Intune enrollment
- Applicable management policies

Dependencies should be documented according to actual implementation.

Detailed CI relationships are maintained through [Service Configuration Management](../Service-Configuration-Management/).

---

## Infrastructure Security

Security controls are incorporated into infrastructure design and administration.

### Identity Security

- Least-privilege administration
- Security group management
- Administrative delegation
- Password policies
- Multifactor authentication
- Privileged role restrictions

### Server Security

- Operating system updates
- Restricted administrative access
- Security auditing
- Service configuration
- Backup and recovery
- Security monitoring

### Network Security

- Firewall rules
- Network segmentation
- Secure administration
- Access restrictions
- Network monitoring

### Endpoint Security

- Device compliance
- Endpoint protection
- Configuration policies
- Operating system updates
- Local administrator restrictions

Security requirements and assessments are managed through [Information Security Management](../Information-Security-Management/).

---

## Infrastructure Monitoring

Monitoring helps identify conditions affecting infrastructure health, availability, and performance.

### Potential Monitoring Areas

| Component | Monitoring Focus |
|---|---|
| Domain Controllers | Availability, replication, DNS, authentication |
| Windows Servers | CPU, memory, disk, services, Event Logs |
| Workstations | Device health, connectivity, compliance |
| Network Devices | Availability, interfaces, routing, traffic |
| Microsoft 365 | Service health, identity-related events |
| Azure Resources | Resource health, metrics, alerts |

### Monitoring Tools

Potential tools include:

- Windows Event Viewer
- Windows Performance Monitor
- PowerShell
- Windows Admin Center
- Azure Monitor
- Network diagnostic utilities
- Syslog
- SNMP-based monitoring tools

Monitoring configurations and events should be documented through [Monitoring and Event Management](../Monitoring-and-Event-Management/).

---

## Infrastructure Backup & Recovery

Backup and recovery procedures help protect infrastructure availability and recoverability.

### Potential Activities

- Windows Server Backup
- System State backup
- Active Directory recovery exercises
- Configuration backups
- Virtual machine recovery
- Network device configuration exports
- Recovery validation

### Recovery Considerations

- Critical service dependencies
- Backup integrity
- Recovery procedures
- Recovery permissions
- Restoration testing
- Recovery time requirements
- Data protection

Virtual machine snapshots should not be treated as substitutes for supported backups, particularly for domain controllers and other stateful systems.

Backup procedures and recovery results should be documented based on actual lab activities.

---

## Infrastructure Administration

Technical Techno Tech uses multiple administrative tools.

| Tool | Primary Purpose |
|---|---|
| PowerShell | Scripting, automation, and administration |
| Windows Admin Center | Windows Server management |
| RSAT | Remote Windows Server and Active Directory administration |
| Server Manager | Server roles and features |
| Active Directory Administrative Center | Directory object administration |
| Microsoft 365 Admin Center | Microsoft 365 administration |
| Microsoft Entra Admin Center | Cloud identity management |
| Microsoft Intune Admin Center | Endpoint management |
| Azure Portal | Azure resource administration |
| Hyper-V | Virtual machine administration |
| OPNsense | Firewall and network administration |
| VyOS | Routing and network administration |

Tools should be documented according to their actual use in each exercise.

---

## Infrastructure Configuration Standards

Infrastructure documentation should follow consistent technical standards.

### Naming Conventions

Use descriptive and consistent names for:

- Servers
- Workstations
- Network devices
- Security groups
- Organizational Units
- Cloud resources
- Configuration Items

### Network Configuration

Document:

- IP addresses
- Subnet masks
- Default gateways
- DNS servers
- VLAN assignments
- Routing relationships

### Server Configuration

Document:

- Operating system
- Installed roles
- Hostname
- Domain membership
- Network configuration
- Administrative tools
- Service dependencies

### Security Configuration

Document relevant:

- Access controls
- Security policies
- Firewall rules
- Authentication requirements
- Administrative permissions

### Verification

Configuration information should be validated through administrative tools, commands, or observable system behavior.

---

## Infrastructure Documentation Workflow

Technical infrastructure documentation follows a practical workflow.

### 1. Identify the Requirement

Determine the business or technical purpose of the infrastructure component.

### 2. Design the Configuration

Plan the required:

- Architecture
- Components
- Network settings
- Dependencies
- Security controls
- Administrative requirements

### 3. Implement the Configuration

Deploy and configure the technology in the lab.

### 4. Validate Functionality

Confirm that the component operates as intended.

Examples include:

- Network connectivity testing
- DNS resolution
- Domain authentication
- Active Directory replication
- Service availability
- Access control testing

### 5. Document the Configuration

Record:

- Technical specifications
- Configuration steps
- Commands
- Screenshots
- Validation results
- Dependencies

### 6. Update Related Records

Update applicable:

- Infrastructure documents
- Configuration Item records
- Change records
- Knowledge articles
- Operational scenarios

### 7. Maintain Documentation

Review and update documentation when the environment changes.

---

## Integration With ITIL Management Practices

Infrastructure supports the organization's ITIL-aligned management practices.

| ITIL Practice | Infrastructure Relationship |
|---|---|
| Service Desk | Uses infrastructure information to support employees |
| Incident Management | Troubleshoots infrastructure service disruptions |
| Service Request Management | Fulfills authorized infrastructure-related requests |
| Knowledge Management | Maintains reusable technical procedures |
| Problem Management | Investigates recurring infrastructure failures |
| Change Enablement | Manages infrastructure modifications |
| Monitoring and Event Management | Observes infrastructure health and detects events |
| Service Configuration Management | Tracks individual infrastructure components and relationships |
| Information Security Management | Protects infrastructure and information |
| Continual Improvement | Evaluates opportunities to improve infrastructure and operations |

### Infrastructure vs. Operational Records

Infrastructure documentation and ITIL operational records serve different purposes.

**Infrastructure Documentation**

Describes:

- Architecture
- Technical configurations
- Network topology
- Installed services
- Infrastructure dependencies
- Administrative technologies

**Operational Records**

Describe:

- Business requirements
- Support activities
- Incidents
- Service requests
- Problems
- Changes
- Security assessments
- Monitoring events
- Improvement initiatives

### Example

**Scenario:** Technical Techno Tech requires an additional domain controller to improve directory service availability.

Related documentation may include:

- `Infrastructure/Active-Directory/Domain-Architecture.md` — Updated domain architecture
- `Infrastructure/Windows-Server/Server-Inventory.md` — Updated server inventory
- `Change-Enablement/Records/CHG-XXX/` — Change assessment and deployment
- `Service-Configuration-Management/Configuration-Items/Servers/CI-XXX/` — DC02 configuration record
- `Knowledge-Management/Knowledge-Base/Active-Directory/` — Reusable deployment instructions

Not every infrastructure activity requires a separate record under every ITIL practice.

---

## Infrastructure Documentation Standards

Infrastructure documents should:

1. Clearly identify the technology or component.
2. Explain its business and technical purpose.
3. Describe the implemented configuration.
4. Identify relevant infrastructure dependencies.
5. Document administrative tools and procedures.
6. Include commands and configuration examples when useful.
7. Provide technical validation evidence.
8. Distinguish proposed designs from deployed configurations.
9. Link related Configuration Item records.
10. Reference applicable change or incident records.
11. Avoid duplicating information unnecessarily.
12. Protect credentials and sensitive configuration details.
13. Identify known limitations.
14. Record configuration updates.
15. Reflect actual lab work rather than invented technical implementations.

---

## Future Infrastructure Expansion

Potential future infrastructure projects include:

### Windows Server

- Additional server roles
- Group Policy administration
- DNS and DHCP enhancements
- Server backup and recovery
- Hybrid Windows Server administration

### Microsoft 365

- Microsoft Entra ID administration
- Microsoft Intune device management
- Endpoint security
- Cloud identity management
- Microsoft 365 administration

### Microsoft Azure

- Azure Virtual Machines
- Azure Virtual Networks
- Cloud monitoring
- Hybrid infrastructure
- Cost management

### Networking

- VLAN segmentation
- Routing
- Firewall configuration
- Network monitoring
- Network security

### Automation

- PowerShell administration
- Automated health checks
- User provisioning
- Configuration verification
- IT service management integration

Future projects should be documented as planned until implementation and validation are completed.

---

## Related Documentation

### Company Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Operational Scenarios](../Scenarios/)

### ITIL Management Practices

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

### Infrastructure Documentation

- [Active Directory](Active-Directory/)
- [Windows Server](Windows-Server/)
- [Microsoft 365](Microsoft-365/)
- [Networking](Networking/)
- [Virtualization](Virtualization/)

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Business requirements, organizational structures, infrastructure planning, and operational responsibilities may be simulated.

Technical deployments, configurations, administrative activities, troubleshooting, and validation are documented based on hands-on work performed in controlled lab environments where indicated.

The infrastructure may contain separate or partially integrated lab environments. Technologies are not represented as interconnected unless their integration has been implemented and verified.

This documentation demonstrates practical IT infrastructure administration, technical configuration, troubleshooting, and IT service management knowledge rather than employment experience within an actual production organization.
