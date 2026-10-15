# Technical Techno Tech — Windows Server Roles and Features

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Configuration  
**Document ID:** INF-WS-002  
**Version:** 1.0  
**Status:** Existing Lab — Configuration Verification Ongoing  
**Practice:** Service Configuration Management  
**Function:** Internal IT  
**Platform:** Microsoft Windows Server  
**Virtualization:** Microsoft Hyper-V  
**Domain:** `technicaltechnotech.com`  
**Last Reviewed:** Pending Verification

---

## 1. Purpose

This document identifies and describes the Windows Server roles and features supporting Technical Techno Tech's internal IT infrastructure.

It provides a centralized reference for:

- Installed Windows Server roles
- Server role assignments
- Active Directory Domain Services
- DNS infrastructure
- Domain controller responsibilities
- Windows Server features
- Administrative tools
- Role dependencies
- Configuration verification
- Security considerations
- Maintenance and troubleshooting
- Future infrastructure expansion

This document supports infrastructure administration, configuration management, incident investigation, and change enablement.

---

## 2. Environment Overview

Technical Techno Tech operates a virtualized Windows Server environment supporting centralized identity management and network services.

The existing environment includes two documented domain controllers.

| Server | IP Address | Installation Type | Primary Function |
|---|---|---|---|
| DC01 | `10.20.10.10` | Desktop Experience | Active Directory and DNS |
| DC02 | `10.20.10.11` | Server Core | Additional writable domain controller |

### Domain Information

| Attribute | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| Domain | `technicaltechnotech.com` |
| Virtualization Platform | Hyper-V |
| Server Network | `10.20.10.0/24` |
| Default Gateway | `10.20.10.1` |
| Router | RTR01 — VyOS |
| Firewall | FW01 — OPNsense |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |

The environment is designed to support Windows infrastructure administration and realistic IT service management exercises.

---

## 3. Windows Server Roles vs. Features

Windows Server provides roles and features that extend the operating system's capabilities.

### Server Roles

A **server role** provides a primary service or function to users, devices, or other systems.

Examples include:

- Active Directory Domain Services
- DNS Server
- DHCP Server
- File and Storage Services
- Web Server (IIS)

### Server Features

A **server feature** provides supporting functionality, administrative capabilities, or additional operating system services.

Examples include:

- Group Policy Management
- Windows Server Backup
- Failover Clustering
- .NET Framework Features
- Remote Server Administration Tools

### Key Difference

**Role = What the server provides.**

**Feature = Additional functionality that supports the server or its administration.**

Some roles automatically install required supporting features.

---

## 4. Server Role Inventory

The following table summarizes the documented Windows Server roles.

| Role / Feature | DC01 | DC02 | Status |
|---|---|---|---|
| Active Directory Domain Services | Documented | Documented | Previously Configured |
| DNS Server | Documented | Pending Verification | Partially Verified |
| Group Policy Management | Pending Verification | Pending Verification | Inventory Required |
| Windows Server Backup | Pending Verification | Pending Verification | Inventory Required |
| DHCP Server | Not Documented | Not Documented | Deployment Not Confirmed |
| File and Storage Services | Pending Verification | Pending Verification | Inventory Required |
| Web Server (IIS) | Not Documented | Not Documented | Deployment Not Confirmed |
| Additional Roles | Pending Inventory | Pending Inventory | Inventory Required |

### Important

"Not documented" does not necessarily mean a role is absent.

The actual installed role inventory must be collected directly from each server.

---

## 5. Active Directory Domain Services (AD DS)

### 5.1 Overview

Active Directory Domain Services provides centralized directory and identity services for Windows environments.

AD DS allows administrators to manage:

- User accounts
- Computer accounts
- Security groups
- Organizational units
- Authentication
- Authorization
- Domain policies
- Directory replication

### 5.2 TTT Implementation

| Attribute | Configuration |
|---|---|
| Role | Active Directory Domain Services |
| Domain | `technicaltechnotech.com` |
| DC01 | Writable Domain Controller |
| DC02 | Writable Domain Controller |
| Replication | Domain Controller Replication |
| Current Health | Pending Verification |

### 5.3 Domain Controller Responsibilities

#### DC01

DC01 is documented as providing:

- Active Directory Domain Services
- Domain authentication
- Directory administration
- DNS
- PDC Emulator functionality

The current FSMO role distribution must be verified.

#### DC02

DC02 is documented as providing:

- Additional writable domain controller functionality
- Active Directory replication
- Domain authentication
- Directory service availability

### 5.4 AD DS Dependencies

AD DS depends on:

- DNS
- Network connectivity
- Time synchronization
- Domain controller communication
- Windows Server services
- Appropriate security permissions

### 5.5 Role Verification

Check whether AD DS is installed:

```powershell
Get-WindowsFeature -Name AD-Domain-Services
```

List domain controllers:

```powershell
Get-ADDomainController -Filter *
```

Review domain information:

```powershell
Get-ADDomain
```

Review forest information:

```powershell
Get-ADForest
```

Review FSMO role holders:

```powershell
netdom query fsmo
```

### 5.6 Health Verification

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

```powershell
repadmin /showrepl
```

### Verification Checklist

- [ ] AD DS role installed on DC01
- [ ] AD DS role installed on DC02
- [ ] Both servers recognized as domain controllers
- [ ] Domain name verified
- [ ] FSMO roles verified
- [ ] Replication verified
- [ ] Domain controller discovery verified
- [ ] AD DS health checks completed

### Related Documentation

[Active Directory Overview](../Active-Directory/README.md)

[Domain Architecture](../Active-Directory/Domain-Architecture.md)

---

## 6. DNS Server

### 6.1 Overview

The DNS Server role provides name resolution services.

Active Directory relies on DNS to locate domain controllers and other directory services.

DNS is required for:

- Domain controller discovery
- Domain authentication
- Active Directory replication
- Service location records
- Internal hostname resolution

### 6.2 TTT Implementation

| Attribute | Configuration |
|---|---|
| DNS Domain | `technicaltechnotech.com` |
| DC01 | DNS Server Documented |
| DC02 | DNS Role Pending Verification |
| DNS Zone Configuration | Pending Verification |
| Forwarders | Pending Verification |
| Reverse Lookup Zones | Pending Verification |

### 6.3 DNS Responsibilities

The DNS infrastructure supports:

- Internal name resolution
- Active Directory service discovery
- Domain controller location
- Client access to domain services

### 6.4 DNS Role Verification

Check the installed role:

```powershell
Get-WindowsFeature -Name DNS
```

Check the DNS service:

```powershell
Get-Service -Name DNS
```

List DNS zones:

```powershell
Get-DnsServerZone
```

Review DNS forwarders:

```powershell
Get-DnsServerForwarder
```

### 6.5 DNS Resolution Testing

Resolve the domain:

```powershell
Resolve-DnsName technicaltechnotech.com
```

Check Active Directory service records:

```powershell
Resolve-DnsName -Type SRV _ldap._tcp.dc._msdcs.technicaltechnotech.com
```

Check configured DNS servers:

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

### Verification Checklist

- [ ] DNS role verified on DC01
- [ ] DNS role status verified on DC02
- [ ] DNS service running
- [ ] Forward lookup zones documented
- [ ] DNS zone replication settings reviewed
- [ ] DNS forwarders reviewed
- [ ] Domain records resolve
- [ ] Domain controller SRV records resolve
- [ ] Client DNS configuration verified

---

## 7. Group Policy Management

### 7.1 Overview

Group Policy provides centralized management of Windows user and computer configurations.

Group Policy Objects (GPOs) can be used to configure:

- Security policies
- Password and account settings
- Windows Firewall settings
- Desktop restrictions
- Administrative templates
- Windows configuration settings
- Logon scripts
- Other supported user and computer policies

### 7.2 TTT Application

Group Policy is relevant to the TTT Active Directory environment.

Potential uses include:

- Applying security configurations
- Managing departmental settings
- Configuring workstation restrictions
- Controlling Windows settings
- Standardizing computer configurations

Specific GPOs should be documented after their configuration and verification.

### 7.3 Group Policy Management Feature

Group Policy Management provides administrative tools for managing GPOs.

Verify installation:

```powershell
Get-WindowsFeature -Name GPMC
```

List GPOs:

```powershell
Get-GPO -All
```

Review a GPO:

```powershell
Get-GPO -Name "Default Domain Policy"
```

Generate a GPO report:

```powershell
Get-GPOReport -All -ReportType HTML -Path "C:\Temp\GPO-Report.html"
```

Ensure the destination directory exists before generating the report.

### 7.4 Client Verification

Refresh Group Policy:

```powershell
gpupdate /force
```

Review applied policies:

```powershell
gpresult /r
```

Generate a policy report:

```powershell
gpresult /h C:\Temp\GPResult.html
```

### Verification Checklist

- [ ] Group Policy Management availability verified
- [ ] Existing GPOs inventoried
- [ ] GPO links documented
- [ ] Security filtering reviewed
- [ ] Policy application tested
- [ ] Results captured
- [ ] Unnecessary policies identified

### Related Documentation

[Organizational Units](../Active-Directory/Organizational-Units.md)

---

## 8. Windows Server Backup

### 8.1 Overview

Windows Server Backup provides backup capabilities for Windows Server systems.

Depending on the configuration, it can support:

- Volume backups
- System State backups
- Bare-metal recovery preparation
- Scheduled backups
- Recovery operations

### 8.2 TTT Application

Backup and recovery are important for protecting domain services.

The current Windows Server Backup installation and backup configuration must be verified.

### 8.3 Installation Verification

```powershell
Get-WindowsFeature -Name Windows-Server-Backup
```

### 8.4 Backup Information

Review backup versions:

```powershell
wbadmin get versions
```

Review configured backup schedules:

```powershell
wbadmin get schedule
```

### 8.5 Backup Considerations

Domain controller backup planning should account for:

- Active Directory database
- SYSVOL
- System State
- DNS configuration
- Recovery procedures
- Backup storage
- Restore testing

### 8.6 Verification Checklist

- [ ] Backup feature installation verified
- [ ] Backup method identified
- [ ] Backup destination documented
- [ ] Backup schedule documented
- [ ] Last successful backup recorded
- [ ] Backup errors reviewed
- [ ] Recovery procedure documented
- [ ] Restore testing performed

### Important

A successful backup does not independently prove successful recovery.

Restore procedures must be tested using supported recovery methods.

Hyper-V checkpoints should not replace proper backups.

---

## 9. DHCP Server

### 9.1 Overview

Dynamic Host Configuration Protocol (DHCP) automatically assigns network configuration to clients.

DHCP can provide:

- IP addresses
- Subnet masks
- Default gateways
- DNS server addresses
- DNS suffixes
- Additional DHCP options

### 9.2 TTT Deployment Status

**Status:** Not Documented as Deployed

The TTT environment has an established IP addressing plan, but a Windows Server DHCP deployment has not been confirmed.

### 9.3 Potential DHCP Design

| Network | Subnet | Gateway |
|---|---|---|
| Clients | `10.20.20.0/24` | `10.20.20.1` |
| Management | `10.20.30.0/24` | `10.20.30.1` |

These networks could use DHCP if appropriate for the environment.

Infrastructure systems such as domain controllers should maintain stable addresses.

### 9.4 Deployment Considerations

A future DHCP implementation would require:

1. Selecting the DHCP server.
2. Installing the DHCP Server role.
3. Authorizing the DHCP server in Active Directory, when applicable.
4. Creating DHCP scopes.
5. Configuring exclusions and reservations.
6. Configuring gateway options.
7. Configuring DNS options.
8. Configuring DHCP relay where required.
9. Testing client address assignment.
10. Documenting results.

Because TTT uses multiple routed subnets, DHCP relay may be required for clients located outside the DHCP server's local broadcast domain.

### 9.5 Role Verification

```powershell
Get-WindowsFeature -Name DHCP
```

If the DHCP role and management tools are installed, review scopes:

```powershell
Get-DhcpServerv4Scope
```

### Verification Checklist

- [ ] Determine whether DHCP is required
- [ ] Identify the intended DHCP server
- [ ] Confirm existing DHCP services
- [ ] Plan address scopes
- [ ] Plan exclusions and reservations
- [ ] Determine DHCP relay requirements
- [ ] Implement approved configuration
- [ ] Test client address assignment
- [ ] Document evidence

---

## 10. File and Storage Services

### 10.1 Overview

Windows Server supports centralized file storage and shared folder access.

Relevant capabilities include:

- SMB file sharing
- NTFS permissions
- Shared folder permissions
- Storage management
- File access auditing
- Storage quotas
- Additional file server services

### 10.2 TTT Application

File and storage services can support departmental resources such as:

- HR shared folders
- Sales shared folders
- IT shared folders
- Common business resources

Previous Active Directory lab exercises included departmental folder permissions and group-based access testing.

The actual TTT file server role assignments and shared folder configurations must be verified before they are recorded as deployed.

### 10.3 Role Verification

Review file-related Windows Server features:

```powershell
Get-WindowsFeature |
Where-Object Name -like "FS-*"
```

Review SMB shares:

```powershell
Get-SmbShare
```

Review share permissions:

```powershell
Get-SmbShareAccess -Name "ShareName"
```

Review NTFS permissions:

```powershell
Get-Acl "C:\FolderPath"
```

Replace example names and paths with actual configured resources.

### 10.4 Security Considerations

- Apply least privilege.
- Use security groups for access management.
- Separate departmental resources.
- Review inherited permissions.
- Document share and NTFS permissions.
- Test access using appropriate accounts.
- Avoid granting unnecessary broad access.

### Verification Checklist

- [ ] Installed file server roles verified
- [ ] Existing shares inventoried
- [ ] Share permissions reviewed
- [ ] NTFS permissions reviewed
- [ ] Group-based access verified
- [ ] Access tests documented
- [ ] Storage capacity reviewed

---

## 11. Remote Server Administration Tools (RSAT)

### 11.1 Overview

Remote Server Administration Tools allow administrators to manage Windows Server services remotely.

RSAT supports administrative tasks involving:

- Active Directory
- DNS
- Group Policy
- DHCP
- Other supported Windows Server services

### 11.2 TTT Administrative Workstation

**MGMT01** is the documented administrative workstation.

Its intended purpose includes centralized management of TTT infrastructure.

### 11.3 Administrative Tools

Relevant tools include:

- Active Directory Users and Computers
- Active Directory Administrative Center
- Group Policy Management
- DNS Manager
- PowerShell
- Server Manager
- Windows Admin Center

The exact installed tools should be verified on MGMT01.

### 11.4 Server-Side Verification

```powershell
Get-WindowsFeature |
Where-Object Name -like "RSAT-*"
```

### 11.5 Windows 11 Verification

On MGMT01, review RSAT capabilities:

```powershell
Get-WindowsCapability -Online |
Where-Object Name -like "Rsat*"
```

### Verification Checklist

- [ ] MGMT01 administrative tools inventoried
- [ ] AD DS management access tested
- [ ] DNS management access tested
- [ ] Group Policy management access tested
- [ ] Administrative permissions verified
- [ ] Remote connectivity verified

---

## 12. Windows Admin Center

### 12.1 Overview

Windows Admin Center is a browser-based management tool for Windows Server and related infrastructure.

It supports various administrative functions, including:

- Server management
- Performance monitoring
- Event log inspection
- Service management
- Storage management
- Network configuration
- Remote PowerShell
- Supported extensions

### 12.2 TTT Application

Windows Admin Center has been used in previous Windows Server administration exercises.

The current installation, gateway location, managed systems, and extensions should be verified.

### 12.3 Verification Requirements

- [ ] Installation location identified
- [ ] Gateway configuration documented
- [ ] Managed servers inventoried
- [ ] Authentication method reviewed
- [ ] Administrative permissions verified
- [ ] Installed extensions documented
- [ ] Remote management tested

### Important

Windows Admin Center is an administrative application, not a Windows Server role.

It is documented here because it supports Windows Server operations.

---

## 13. PowerShell and Remote Administration

### 13.1 Overview

PowerShell provides command-line administration and automation capabilities.

It supports:

- Server role management
- Service administration
- Active Directory administration
- DNS administration
- Network configuration
- Event log inspection
- Remote administration
- Configuration verification

### 13.2 PowerShell Remoting

PowerShell Remoting allows authorized administrators to execute commands on remote Windows systems.

### 13.3 Example Commands

Review remoting service:

```powershell
Get-Service WinRM
```

Test remote management:

```powershell
Test-WSMan DC01
```

Execute a remote command:

```powershell
Invoke-Command -ComputerName DC01 -ScriptBlock {
    Get-Service NTDS,DNS
}
```

These commands require appropriate connectivity, authentication, and permissions.

### 13.4 Remote Administration Security

- Use authorized administrative accounts.
- Restrict remote management access.
- Apply least privilege.
- Use supported authentication methods.
- Review firewall rules.
- Log relevant administrative activity.
- Protect privileged credentials.

---

## 14. Windows Server Core Administration

### 14.1 Overview

Windows Server Core provides a reduced graphical installation option.

It is designed for supported server workloads that can be managed primarily through command-line and remote administration tools.

### 14.2 TTT Implementation

**Server:** DC02

**Installation Type:** Windows Server Core

### 14.3 Administrative Methods

- SConfig
- PowerShell
- PowerShell Remoting
- Windows Admin Center
- RSAT
- Remote management consoles

### 14.4 Example Commands

Open SConfig:

```powershell
sconfig
```

Review computer information:

```powershell
Get-ComputerInfo
```

Review network configuration:

```powershell
Get-NetIPConfiguration
```

Review installed roles:

```powershell
Get-WindowsFeature |
Where-Object Installed
```

### 14.5 Learning Objectives

- Administer Windows Server without relying on a full desktop interface.
- Configure networking through PowerShell.
- Manage installed roles.
- Troubleshoot services.
- Perform remote administration.
- Understand Server Core operational differences.

---

## 15. Server Role Dependencies

Windows Server roles depend on other infrastructure components.

### 15.1 Dependency Matrix

| Role / Service | Dependencies |
|---|---|
| AD DS | DNS, networking, time synchronization |
| DNS | Windows Server, network connectivity |
| Group Policy | AD DS, DNS, SYSVOL |
| Windows Server Backup | Storage, backup configuration |
| DHCP | Network connectivity, scope configuration, relay where required |
| File Services | Storage, SMB connectivity, permissions |
| Remote Administration | Network connectivity, authentication, management services |

### 15.2 Logical Dependency Diagram

```text
                   Hyper-V
                      |
                      v
               Virtual Networking
                      |
                      v
                Server Network
                      |
              +-------+-------+
              |               |
              v               v
            DC01             DC02
              |               |
              +-------+-------+
                      |
                Windows Server
                      |
              +-------+-------+
              |               |
              v               v
             AD DS           DNS
              |               |
              +-------+-------+
                      |
                      v
              Domain Authentication
                      |
              +-------+-------+
              |               |
              v               v
           CLIENT01         MGMT01
```

This diagram represents logical service relationships rather than a complete physical or virtual topology.

---

## 16. Role Installation and Configuration Procedure

### 16.1 Purpose

Establish a consistent approach to installing and configuring Windows Server roles.

### 16.2 Proposed Workflow

1. Identify the service requirement.
2. Select the appropriate server.
3. Review system requirements.
4. Review infrastructure dependencies.
5. Assess security implications.
6. Determine whether change authorization is required.
7. Prepare a recovery plan.
8. Install the role.
9. Configure the service.
10. Verify functionality.
11. Update the server inventory.
12. Update configuration records.
13. Capture technical evidence.
14. Review the implementation.

### 16.3 Role Installation Methods

Windows Server roles may be installed through:

- Server Manager
- PowerShell
- Supported deployment and automation tools

### 16.4 Example — Inspecting an Installed Role

```powershell
Get-WindowsFeature -Name DNS
```

### 16.5 Example — Installing a Role

The following is an illustrative command and should only be executed when an installation is required and authorized:

```powershell
Install-WindowsFeature -Name DNS -IncludeManagementTools
```

Installing a role does not automatically complete its service configuration.

### 16.6 Post-Installation Verification

Verify:

- Installation status
- Service status
- Required configuration
- Network connectivity
- Security settings
- Operational functionality
- Relevant event logs

---

## 17. Role Verification and Evidence

### 17.1 Verification Objectives

Confirm which roles and features are installed and operational.

### 17.2 General Inventory Command

```powershell
Get-WindowsFeature |
Where-Object Installed |
Select-Object Name,DisplayName,InstallState
```

### 17.3 Remote Inventory Example

From an authorized administrative workstation:

```powershell
Invoke-Command -ComputerName DC01,DC02 -ScriptBlock {
    Get-WindowsFeature |
    Where-Object Installed |
    Select-Object Name,DisplayName,InstallState
}
```

### 17.4 Verification Matrix

| Test ID | Server | Verification | Result |
|---|---|---|---|
| WS-ROLE-001 | DC01 | Installed role inventory | Pending |
| WS-ROLE-002 | DC02 | Installed role inventory | Pending |
| WS-ROLE-003 | DC01 | AD DS operational status | Pending |
| WS-ROLE-004 | DC02 | AD DS operational status | Pending |
| WS-ROLE-005 | DC01 | DNS role and service | Pending |
| WS-ROLE-006 | DC02 | DNS role and service | Pending |
| WS-ROLE-007 | DC01 | Group Policy Management | Pending |
| WS-ROLE-008 | DC02 | Group Policy Management | Pending |
| WS-ROLE-009 | DC01 | Backup feature and configuration | Pending |
| WS-ROLE-010 | DC02 | Backup feature and configuration | Pending |

### 17.5 Evidence Requirements

For each completed verification, record:

- Test ID
- Date
- Server
- Command or tool
- Expected result
- Actual result
- Pass/fail status
- Supporting evidence
- Notes

### Evidence Status

**Installed Role Reports:** Pending Collection

**Service Verification:** Pending

**Configuration Screenshots:** Pending Collection

**Operational Tests:** Pending

---

## 18. Security Considerations

Windows Server roles can expose network services and increase system complexity.

### Security Principles

- Least privilege
- Role-based access
- Secure configuration
- Reduced attack surface
- Appropriate firewall restrictions
- Regular updates
- Auditing
- Backup protection
- Configuration change control

### 18.1 Role Separation

Where appropriate, separate infrastructure roles to reduce operational dependencies and security exposure.

Domain controllers should not be used unnecessarily for unrelated application workloads.

### 18.2 Administrative Access

Administrative access should be restricted to authorized personnel.

### 18.3 Network Access

Only required service communication should be permitted.

### 18.4 Configuration Review

Review installed roles periodically to identify:

- Unnecessary services
- Unsupported configurations
- Outdated features
- Excessive administrative access
- Missing security controls

---

## 19. Troubleshooting Windows Server Roles

### 19.1 General Troubleshooting Workflow

1. Identify the affected service.
2. Confirm the reported symptoms.
3. Determine the affected server.
4. Verify network connectivity.
5. Check role installation.
6. Check service status.
7. Review event logs.
8. Review dependencies.
9. Identify the probable cause.
10. Implement an authorized corrective action.
11. Verify service restoration.
12. Document findings.

### 19.2 Example Scenarios

| Scenario | Possible Cause | Investigation |
|---|---|---|
| Domain authentication failure | AD DS or DNS issue | Verify domain controller and DNS health |
| DNS resolution failure | DNS service or configuration | Review DNS service and records |
| GPO not applying | DNS, SYSVOL, or policy configuration | Review GPO processing |
| Backup failure | Storage or backup configuration | Review backup logs and destination |
| DHCP not assigning addresses | Scope, relay, or service issue | Review DHCP configuration if deployed |
| Shared folder inaccessible | SMB, permissions, or network issue | Review share and NTFS permissions |
| Remote administration fails | WinRM, firewall, or permissions | Review remote management configuration |

These scenarios are examples, not completed incident records.

---

## 20. ITIL 4 Integration

Windows Server roles support multiple ITIL 4 practices.

| Practice | Application |
|---|---|
| Service Desk | Receives server-related support requests |
| Incident Management | Restores interrupted infrastructure services |
| Service Request Management | Handles authorized service provisioning requests |
| Problem Management | Investigates recurring role or service failures |
| Change Enablement | Controls role installation and configuration changes |
| Knowledge Management | Documents server administration procedures |
| Monitoring and Event Management | Detects server role failures |
| Service Configuration Management | Maintains role assignments and dependencies |
| Information Security Management | Reviews role security and access |
| Continual Improvement | Improves service reliability and administration |

### Example — DNS Service Failure

A possible incident workflow:

1. CLIENT01 reports a domain connectivity issue.
2. Service Desk records the incident.
3. Incident Management investigates DNS resolution.
4. The technician identifies a DNS service failure.
5. An authorized corrective action is performed.
6. DNS resolution is tested.
7. Domain controller discovery is verified.
8. The incident is resolved.
9. Relevant knowledge documentation is updated.

This is an illustrative scenario.

---

## 21. Service Configuration Management

Windows Server roles should be associated with the servers that provide them.

### Proposed Configuration Relationships

| Configuration Item | Associated Role / Service |
|---|---|
| DC01 | Active Directory Domain Services |
| DC01 | DNS |
| DC02 | Active Directory Domain Services |
| DC02 | DNS — Pending Verification |

### Configuration Records

Each role record should identify:

- Hosting server
- Installed role
- Service purpose
- Configuration details
- Dependencies
- Security requirements
- Operational status
- Related changes
- Supporting evidence

---

## 22. Change Management

Changes to Windows Server roles may affect business services.

Examples include:

- Installing a new role
- Removing a role
- Changing DNS configuration
- Modifying Active Directory settings
- Changing DHCP scopes
- Updating file share configuration
- Changing server security settings

### Proposed Change Workflow

1. Identify the required change.
2. Document the technical justification.
3. Identify affected services.
4. Assess risk and impact.
5. Obtain required authorization.
6. Prepare implementation steps.
7. Prepare recovery procedures.
8. Implement the change.
9. Verify service functionality.
10. Update documentation.
11. Review the outcome.

---

## 23. Monitoring and Maintenance

### 23.1 Monitoring Objectives

Potential monitoring activities include:

- Service availability
- Role-specific errors
- DNS health
- AD DS replication
- Windows Event Logs
- CPU and memory utilization
- Storage capacity
- Backup status
- Security events

### 23.2 Proposed Monitoring Matrix

| Role / Service | Monitoring Focus | Status |
|---|---|---|
| AD DS | Authentication and replication | Automated Monitoring Not Verified |
| DNS | Resolution and service availability | Automated Monitoring Not Verified |
| Group Policy | Processing errors | Automated Monitoring Not Verified |
| Backup | Job success and failure | Automated Monitoring Not Verified |
| File Services | Availability and storage | Deployment and Monitoring Pending Verification |
| DHCP | Scope utilization and service availability | Deployment Not Confirmed |

### 23.3 Maintenance Activities

- Review installed roles.
- Apply approved updates.
- Review service health.
- Review event logs.
- Verify configuration baselines.
- Check backups.
- Update documentation.
- Review role dependencies.

---

## 24. Future Server Role Development

Potential future projects include:

### DHCP Server

Deploy centralized IP address assignment for appropriate network segments.

### File Server

Configure departmental shares, security groups, and NTFS permissions.

### Windows Server Backup

Implement and test documented backup and recovery procedures.

### Additional DNS Administration

Practice DNS forwarding, zones, records, and troubleshooting.

### Advanced Group Policy

Configure and test additional security and workstation management policies.

### Monitoring

Implement server health monitoring and event collection.

### Automation

Develop PowerShell scripts for role inventory, configuration checks, and routine administration.

### Hybrid Infrastructure

Evaluate future integration with Microsoft Entra ID and Azure services.

**Microsoft 365 infrastructure has not yet been deployed for TTT.**

Future projects should be documented only after implementation begins.

---

## 25. Skills Practiced

This project supports practical experience with:

- Windows Server administration
- Server role management
- Active Directory Domain Services
- DNS administration
- Group Policy Management
- Windows Server Core
- Remote Server Administration Tools
- PowerShell
- Server Manager
- Windows Admin Center
- Windows Server Backup concepts
- DHCP administration concepts
- File and storage services
- Server security
- Infrastructure troubleshooting
- Configuration management
- ITIL-aligned infrastructure operations

---

## 27. What I Learned

The Windows Server Roles project demonstrates how different server services work together to support a business IT environment.

### Key Learning Areas

**1. Server Roles and Features**

Roles provide services, while features add supporting functionality.

**2. Active Directory**

AD DS provides centralized identity management and authentication.

**3. DNS**

DNS is essential for Active Directory domain controller discovery and name resolution.

**4. Group Policy**

Group Policy allows administrators to centrally manage Windows configurations.

**5. Remote Administration**

Administrative tools and PowerShell allow Windows Server management without requiring direct access to each server.

**6. Server Core**

Windows Server Core provides a command-line-focused installation that can be managed remotely.

**7. Service Dependencies**

A server role may depend on DNS, networking, storage, authentication, and other services.

**8. Configuration Management**

Accurate documentation helps administrators understand which servers provide each service.

**9. Change Management**

Server role changes should be assessed, authorized where required, verified, and documented.

---

## 28. Verification Checklist

### Role Inventory

- [ ] DC01 installed roles inventoried
- [ ] DC02 installed roles inventoried
- [ ] Installed features documented
- [ ] Unnecessary roles reviewed

### Active Directory

- [ ] AD DS verified on DC01
- [ ] AD DS verified on DC02
- [ ] Domain information verified
- [ ] FSMO role holders verified
- [ ] Replication verified

### DNS

- [ ] DNS role verified on DC01
- [ ] DNS role status verified on DC02
- [ ] DNS zones documented
- [ ] DNS resolution tested

### Administration

- [ ] RSAT tools inventoried
- [ ] Windows Admin Center configuration verified
- [ ] Remote administration tested
- [ ] Administrative access reviewed

### Backup and Security

- [ ] Backup features verified
- [ ] Backup configuration documented
- [ ] Security controls reviewed
- [ ] Relevant logs reviewed

### Documentation

- [ ] Command output captured
- [ ] Screenshots sanitized
- [ ] Server inventory updated
- [ ] CI relationships reviewed
- [ ] Unverified details identified
- [ ] Revision history updated

---

## 29. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT Windows Server roles and features documentation, including AD DS, DNS, administration tools, role dependencies, and verification procedures |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization created for hands-on IT training and professional portfolio development.

This document describes Windows Server roles and features associated with the TTT infrastructure.

Previously documented configurations are included for continuity. Roles, features, and operational results that have not been verified are clearly identified.

Example commands, proposed procedures, future deployments, and illustrative scenarios do not represent completed activities.

All technical evidence should originate from actual authorized lab work and be sanitized before publication.

The separate legacy homelab environment is excluded from this project.
