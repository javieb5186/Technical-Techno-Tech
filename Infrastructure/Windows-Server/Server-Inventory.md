# Technical Techno Tech — Windows Server Inventory

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Inventory  
**Document ID:** INF-WS-001  
**Version:** 1.0  
**Status:** Existing Lab — Configuration Verification Ongoing  
**Practice:** Service Configuration Management  
**Function:** Internal IT  
**Infrastructure Platform:** Microsoft Hyper-V  
**Domain:** `technicaltechnotech.com`  
**Last Reviewed:** Pending Verification

---

## 1. Purpose

This document maintains a centralized inventory of the Windows Server systems supporting Technical Techno Tech's internal IT infrastructure.

The inventory provides a reference for:

- Server identification
- Operating system information
- Network configuration
- Installed server roles
- Active Directory responsibilities
- Virtual machine configurations
- Administrative access
- Infrastructure dependencies
- Security and maintenance
- Backup and recovery
- Server lifecycle management
- Configuration verification

The inventory also supports ITIL 4 Service Configuration Management by documenting important server attributes and relationships.

---

## 2. Environment Overview

Technical Techno Tech operates a virtualized Windows Server environment supporting centralized identity and infrastructure services.

The environment currently includes two documented domain controllers:

- **DC01:** Windows Server with Desktop Experience
- **DC02:** Windows Server Core

Both systems support the `technicaltechnotech.com` Active Directory domain.

The servers operate on the dedicated server network and are hosted within the Hyper-V environment.

### Infrastructure Summary

| Component | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| Active Directory Domain | `technicaltechnotech.com` |
| Virtualization Platform | Hyper-V |
| Server Network | `10.20.10.0/24` |
| Server Gateway | `10.20.10.1` |
| Router | RTR01 — VyOS |
| Firewall | FW01 — OPNsense |
| Domain Controllers | DC01 and DC02 |
| Administrative Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Microsoft 365 Infrastructure | Not Yet Deployed |

---

## 3. Server Inventory Summary

| Server ID | Hostname | IP Address | Operating System | Primary Role |
|---|---|---|---|---|
| SRV-001 | DC01 | `10.20.10.10` | Windows Server Desktop Experience | Primary AD DS and DNS infrastructure |
| SRV-002 | DC02 | `10.20.10.11` | Windows Server Core | Additional writable domain controller |

**Inventory Scope:** Existing TTT Windows Server systems.

Additional servers should be added when deployed and verified.

### Server Naming Convention

The current environment uses descriptive hostnames.

| Prefix | Purpose | Example |
|---|---|---|
| DC | Domain Controller | DC01 |
| MGMT | Management Workstation | MGMT01 |
| CLIENT | Employee Workstation | CLIENT01 |

Additional naming conventions may be established as the infrastructure expands.

---

## 4. Server Architecture

```text
                  INTERNET
                     |
                     v
               FW01 - OPNsense
                     |
                     v
                 RTR01 - VyOS
                     |
                     v
              SERVER NETWORK
              10.20.10.0/24
                     |
             +-------+-------+
             |               |
             v               v
           DC01             DC02
       10.20.10.10      10.20.10.11
             |               |
       Windows Server   Windows Server
       Desktop          Core
       Experience
             |               |
             +-------+-------+
                     |
                     v
          technicaltechnotech.com
                 AD DS Domain
```

### Architecture Description

DC01 and DC02 provide domain controller functionality for the TTT Active Directory environment.

Both servers reside on the server network.

Communication with employee and management networks is routed through RTR01.

The Hyper-V platform provides virtual hardware and networking.

---

# 5. Server Record — DC01

## 5.1 General Information

| Attribute | Value |
|---|---|
| Server ID | SRV-001 |
| Hostname | DC01 |
| Fully Qualified Domain Name | `DC01.technicaltechnotech.com` |
| Domain | `technicaltechnotech.com` |
| Operating System | Windows Server |
| Installation Type | Desktop Experience |
| Server Type | Virtual Machine |
| Virtualization Platform | Hyper-V |
| Operational Purpose | Active Directory Domain Services |
| Environment | TTT Infrastructure Lab |
| Status | Previously Configured — Current State Pending Verification |

### Description

DC01 is a Windows Server virtual machine configured to provide centralized domain services.

Its documented responsibilities include:

- Active Directory Domain Services
- DNS
- Domain authentication
- Directory administration
- PDC Emulator functionality

## 5.2 Network Configuration

| Attribute | Value |
|---|---|
| Hostname | DC01 |
| IPv4 Address | `10.20.10.10` |
| Subnet Mask | `255.255.255.0` |
| Network | `10.20.10.0/24` |
| Default Gateway | `10.20.10.1` |
| Preferred DNS | Pending Verification |
| Alternate DNS | Pending Verification |
| MAC Address | Pending Verification |
| Hyper-V Virtual Switch | Pending Verification |

### Network Dependencies

DC01 depends on:

- Hyper-V virtual networking
- Server network connectivity
- VyOS routing for inter-subnet communication
- DNS
- Appropriate network access controls

## 5.3 Installed Server Roles

| Role / Feature | Status |
|---|---|
| Active Directory Domain Services | Previously Configured |
| DNS Server | Previously Documented |
| Group Policy Management | Verify Installation |
| Windows Server Backup | Verify Installation |
| Additional Roles | Pending Inventory |

### Role Verification

```powershell
Get-WindowsFeature |
Where-Object Installed |
Select-Object Name,DisplayName,InstallState
```

**Verification Status:** Pending

## 5.4 Active Directory Responsibilities

DC01 is documented as a writable domain controller.

### Domain Services

- User authentication
- Directory services
- Group management
- Computer account management
- Organizational unit administration
- Group Policy integration
- DNS

### FSMO Responsibilities

DC01 was previously documented as holding the PDC Emulator role.

The current FSMO role distribution should be verified rather than assumed.

```powershell
netdom query fsmo
```

```powershell
Get-ADDomain |
Select-Object PDCEmulator,RIDMaster,InfrastructureMaster
```

```powershell
Get-ADForest |
Select-Object SchemaMaster,DomainNamingMaster
```

## 5.5 Virtual Machine Configuration

| Attribute | Value |
|---|---|
| VM Name | DC01 |
| VM Generation | Pending Verification |
| Virtual Processors | Pending Verification |
| Startup Memory | Pending Verification |
| Dynamic Memory | Pending Verification |
| Virtual Disk Size | Pending Verification |
| Virtual Disk Format | Pending Verification |
| Virtual Switch | Pending Verification |
| Integration Services | Pending Verification |
| Checkpoint Configuration | Pending Verification |

### Hyper-V Verification

Run on an authorized Hyper-V host:

```powershell
Get-VM -Name "DC01" |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

```powershell
Get-VMHardDiskDrive -VMName "DC01"
```

```powershell
Get-VMNetworkAdapter -VMName "DC01"
```

## 5.6 Administrative Access

DC01 may be administered using:

- Server Manager
- Active Directory Users and Computers
- Active Directory Administrative Center
- DNS Manager
- Group Policy Management
- PowerShell
- Windows Admin Center
- Remote Server Administration Tools

Administrative access should be limited to authorized accounts.

## 5.7 Health Verification

### Recommended Checks

- Server availability
- Network connectivity
- DNS functionality
- Active Directory health
- Replication
- Time synchronization
- Event logs
- Storage capacity
- Windows services

### Example Commands

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

```powershell
w32tm /query /status
```

```powershell
Get-Service NTDS,DNS
```

### Verification Record

| Test | Status |
|---|---|
| Server Reachability | Pending |
| DNS Resolution | Pending |
| AD DS Health | Pending |
| Replication | Pending |
| Time Synchronization | Pending |
| Event Log Review | Pending |

---

# 6. Server Record — DC02

## 6.1 General Information

| Attribute | Value |
|---|---|
| Server ID | SRV-002 |
| Hostname | DC02 |
| Fully Qualified Domain Name | `DC02.technicaltechnotech.com` |
| Domain | `technicaltechnotech.com` |
| Operating System | Windows Server |
| Installation Type | Server Core |
| Server Type | Virtual Machine |
| Virtualization Platform | Hyper-V |
| Operational Purpose | Additional Domain Controller |
| Environment | TTT Infrastructure Lab |
| Status | Previously Configured — Current State Pending Verification |

### Description

DC02 is a Windows Server Core virtual machine configured as an additional writable domain controller.

Its purpose is to support:

- Active Directory replication
- Domain authentication
- Directory service availability
- Domain controller administration
- Infrastructure resilience

## 6.2 Network Configuration

| Attribute | Value |
|---|---|
| Hostname | DC02 |
| IPv4 Address | `10.20.10.11` |
| Subnet Mask | `255.255.255.0` |
| Network | `10.20.10.0/24` |
| Default Gateway | `10.20.10.1` |
| Preferred DNS | Pending Verification |
| Alternate DNS | Pending Verification |
| MAC Address | Pending Verification |
| Hyper-V Virtual Switch | Pending Verification |

## 6.3 Installed Server Roles

| Role / Feature | Status |
|---|---|
| Active Directory Domain Services | Previously Configured |
| DNS Server | Pending Verification |
| Additional Roles | Pending Inventory |

### Role Verification

```powershell
Get-WindowsFeature |
Where-Object Installed |
Select-Object Name,DisplayName,InstallState
```

## 6.4 Server Core Administration

DC02 uses Windows Server Core.

Administration may be performed using:

- SConfig
- PowerShell
- PowerShell Remoting
- Windows Admin Center
- RSAT
- Remote administrative consoles

### Example Commands

Open Server Configuration:

```powershell
sconfig
```

Review network configuration:

```powershell
Get-NetIPConfiguration
```

Review computer information:

```powershell
Get-ComputerInfo
```

Review installed roles:

```powershell
Get-WindowsFeature |
Where-Object Installed
```

## 6.5 Active Directory Responsibilities

DC02 operates as an additional writable domain controller.

### Responsibilities

- Replicate directory information
- Process authentication requests
- Provide domain controller availability
- Support directory administration

### Replication Verification

```powershell
repadmin /showrepl
```

```powershell
repadmin /replsummary
```

```powershell
Get-ADReplicationPartnerMetadata -Target "DC02" -Scope Server
```

**Verification Status:** Pending

## 6.6 Virtual Machine Configuration

| Attribute | Value |
|---|---|
| VM Name | DC02 |
| VM Generation | Pending Verification |
| Virtual Processors | Pending Verification |
| Startup Memory | Pending Verification |
| Dynamic Memory | Pending Verification |
| Virtual Disk Size | Pending Verification |
| Virtual Disk Format | Pending Verification |
| Virtual Switch | Pending Verification |
| Integration Services | Pending Verification |
| Checkpoint Configuration | Pending Verification |

### Hyper-V Verification

```powershell
Get-VM -Name "DC02" |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

```powershell
Get-VMHardDiskDrive -VMName "DC02"
```

```powershell
Get-VMNetworkAdapter -VMName "DC02"
```

## 6.7 Health Verification

| Test | Status |
|---|---|
| Server Reachability | Pending |
| Domain Controller Discovery | Pending |
| AD DS Health | Pending |
| Replication | Pending |
| DNS Services | Pending |
| Time Synchronization | Pending |
| Event Log Review | Pending |

---

## 7. Active Directory Domain Information

| Attribute | Value |
|---|---|
| Forest Root Domain | `technicaltechnotech.com` |
| Domain Name | `technicaltechnotech.com` |
| Domain Controllers | DC01, DC02 |
| Forest Functional Level | Pending Verification |
| Domain Functional Level | Pending Verification |
| AD Sites | Pending Verification |
| FSMO Role Holders | Pending Verification |
| Global Catalog Configuration | Pending Verification |
| AD Recycle Bin | Pending Verification |

### Domain Verification

```powershell
Get-ADDomain
```

```powershell
Get-ADForest
```

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName,IPv4Address,Site,IsGlobalCatalog
```

### Functional Level Verification

```powershell
Get-ADDomain |
Select-Object DNSRoot,DomainMode
```

```powershell
Get-ADForest |
Select-Object RootDomain,ForestMode
```

---

## 8. Windows Server Operating System Inventory

Operating system information should be verified directly from each server.

### Required Attributes

- Windows Server edition
- Windows Server version
- Build number
- Installation type
- Activation status
- Installed updates
- Last boot time

### Verification Commands

```powershell
Get-ComputerInfo |
Select-Object CsName,WindowsProductName,WindowsVersion,OsBuildNumber
```

```powershell
Get-CimInstance Win32_OperatingSystem |
Select-Object Caption,Version,BuildNumber,LastBootUpTime
```

```powershell
Get-HotFix |
Sort-Object InstalledOn -Descending |
Select-Object -First 10
```

### Operating System Inventory

| Attribute | DC01 | DC02 |
|---|---|---|
| Windows Server Edition | Pending | Pending |
| Windows Version | Pending | Pending |
| Build Number | Pending | Pending |
| Installation Type | Desktop Experience | Server Core |
| Activation Status | Pending | Pending |
| Latest Installed Update | Pending | Pending |
| Last Boot Time | Pending | Pending |

---

## 9. Server Hardware and Resource Inventory

Virtual server resource allocations should be recorded from Hyper-V.

### Resource Inventory

| Resource | DC01 | DC02 |
|---|---|---|
| Virtual CPUs | Pending | Pending |
| Startup RAM | Pending | Pending |
| Dynamic Memory | Pending | Pending |
| Virtual Disk Capacity | Pending | Pending |
| Available Disk Space | Pending | Pending |
| Virtual Network Adapters | Pending | Pending |
| VM Generation | Pending | Pending |

### Guest Resource Verification

```powershell
Get-CimInstance Win32_ComputerSystem |
Select-Object Name,TotalPhysicalMemory,NumberOfLogicalProcessors
```

```powershell
Get-Volume |
Select-Object DriveLetter,FileSystemLabel,Size,SizeRemaining
```

### Resource Management Considerations

- Monitor storage capacity.
- Review memory utilization.
- Avoid excessive host resource allocation.
- Maintain sufficient resources for domain services.
- Document resource changes.
- Verify system performance after modifications.

---

## 10. Network Configuration Inventory

### Server Network

**Network:** `10.20.10.0/24`

**Default Gateway:** `10.20.10.1`

### Server Addresses

| Server | IPv4 Address |
|---|---|
| DC01 | `10.20.10.10` |
| DC02 | `10.20.10.11` |

### Network Verification

```powershell
Get-NetIPConfiguration
```

```powershell
Get-NetIPAddress -AddressFamily IPv4
```

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

```powershell
Get-NetRoute -AddressFamily IPv4
```

### Network Requirements

Servers require appropriate connectivity for:

- DNS
- Kerberos
- LDAP
- SMB
- RPC
- Active Directory replication
- Time synchronization
- Administrative access

### Network Dependencies

- Hyper-V virtual networking
- RTR01 — VyOS
- FW01 — OPNsense
- Domain DNS infrastructure

---

## 11. Server Role Inventory

The Windows Server role inventory identifies installed infrastructure services.

| Role | DC01 | DC02 |
|---|---|---|
| Active Directory Domain Services | Documented | Documented |
| DNS Server | Documented | Verify |
| DHCP Server | Not Documented as Deployed | Not Documented as Deployed |
| File and Storage Services | Verify | Verify |
| Windows Server Backup | Verify | Verify |
| Group Policy Management | Verify | Verify |

### Verification Procedure

1. Connect to the server.
2. Review installed roles.
3. Identify enabled services.
4. Confirm the operational purpose.
5. Record the actual configuration.
6. Capture supporting evidence.
7. Update the inventory.

### Example

```powershell
Get-WindowsFeature |
Where-Object Installed
```

### Related Documentation

[Server Roles](Server-Roles.md)

---

## 12. Administrative Access Inventory

### Administrative Systems

| System | Purpose |
|---|---|
| MGMT01 | Centralized Windows infrastructure administration |
| DC01 | Local and remote domain administration |
| DC02 | Remote and command-line administration |

### Administrative Tools

- Server Manager
- Windows Admin Center
- Active Directory Users and Computers
- Active Directory Administrative Center
- Group Policy Management
- DNS Manager
- RSAT
- PowerShell
- PowerShell Remoting

### Administrative Access Requirements

- Authorized administrative account
- Appropriate role membership
- Network connectivity
- Required management services
- Applicable firewall permissions

### Security Considerations

Administrative privileges should be assigned according to least privilege.

Domain administrator credentials should not be used unnecessarily for routine workstation tasks.

---

## 13. Server Health and Monitoring

Server monitoring supports early identification of infrastructure problems.

### Recommended Health Checks

| Category | Check |
|---|---|
| Availability | Server responds and required services are running |
| CPU | Processor utilization |
| Memory | Memory availability |
| Storage | Available disk space |
| Networking | Interface and routing configuration |
| DNS | Name resolution |
| Active Directory | Domain controller health |
| Replication | Replication status |
| Time | Time synchronization |
| Security | Relevant security events |
| Updates | Installed patches |

### Example Commands

```powershell
Get-Service
```

```powershell
Get-Volume
```

```powershell
Get-WinEvent -LogName System -MaxEvents 20
```

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

### Monitoring Status

**Automated Monitoring:** Not Yet Verified

**Alerting:** Not Yet Verified

**Baseline Metrics:** Not Yet Established

**Monitoring Frequency:** To Be Defined

---

## 14. Backup and Recovery Inventory

Backup and recovery planning is essential for infrastructure availability.

### Potential Recovery Requirements

- Domain controller recovery
- Active Directory object recovery
- System State recovery
- Server configuration recovery
- Virtual machine recovery
- DNS recovery

### Backup Inventory

| Server | Backup Method | Last Successful Backup | Restore Test |
|---|---|---|---|
| DC01 | Pending Verification | Pending | Pending |
| DC02 | Pending Verification | Pending | Pending |

### Backup Verification

Confirm:

1. The backup method.
2. The backup destination.
3. The backup schedule.
4. The last successful backup.
5. Backup integrity.
6. Recovery documentation.
7. Restore test results.

### Important

A successful backup does not guarantee successful recovery.

Restoration should be tested using supported recovery methods.

Hyper-V checkpoints should not be treated as a replacement for backups.

---

## 15. Security Configuration Inventory

### Security Controls

| Control | DC01 | DC02 |
|---|---|---|
| Windows Firewall | Verify | Verify |
| Windows Updates | Verify | Verify |
| Administrative Access | Verify | Verify |
| Password Policies | Domain-Level Review | Domain-Level Review |
| Account Auditing | Verify | Verify |
| Time Synchronization | Verify | Verify |
| Remote Management | Verify | Verify |
| Backup Protection | Verify | Verify |

### Security Review

The security inventory should consider:

- Least privilege
- Administrative delegation
- Privileged account management
- Windows Firewall
- Security updates
- Audit policies
- Event logs
- Backup protection
- Domain controller hardening

### Security Verification

```powershell
Get-NetFirewallProfile
```

```powershell
Get-Service WinRM
```

```powershell
auditpol /get /category:*
```

Actual results should be documented before marking controls as implemented.

---

## 16. Windows Update and Maintenance

### Maintenance Objectives

- Maintain operating system stability.
- Apply approved security updates.
- Reduce known vulnerabilities.
- Preserve service availability.
- Maintain accurate configuration records.

### Proposed Maintenance Workflow

1. Review available updates.
2. Assess operational impact.
3. Identify affected services.
4. Determine whether change authorization is required.
5. Prepare a recovery plan.
6. Apply approved updates.
7. Restart if required.
8. Verify server health.
9. Verify domain services.
10. Document results.

### Maintenance Register

| Server | Last Update Review | Last Maintenance | Status |
|---|---|---|---|
| DC01 | Pending | Pending | Not Verified |
| DC02 | Pending | Pending | Not Verified |

---

## 17. Service Dependencies

Windows Server infrastructure depends on several interconnected systems.

### Dependency Overview

```text
                  Hyper-V
                     |
                     v
              Virtual Networking
                     |
                     v
                 RTR01
                     |
             Server Network
                     |
             +-------+-------+
             |               |
             v               v
           DC01             DC02
             |               |
             +-------+-------+
                     |
              Active Directory
                     |
                     v
             Domain Authentication
                     |
             +-------+-------+
             |               |
             v               v
          CLIENT01         MGMT01
```

### Dependency Matrix

| Service | Dependencies |
|---|---|
| Domain Authentication | Domain controllers, DNS, networking |
| Active Directory Replication | DC01, DC02, DNS, network connectivity |
| Group Policy | AD DS, DNS, SYSVOL, network connectivity |
| Administrative Access | Management network, authentication, management services |
| Domain Name Resolution | DNS infrastructure |
| Server Availability | Hyper-V, virtual storage, virtual networking |

---

## 18. Configuration Management

Windows Server systems should be tracked as configuration items.

### Proposed Configuration Item Mapping

| Server ID | Hostname | Proposed CI ID |
|---|---|---|
| SRV-001 | DC01 | CI-003 |
| SRV-002 | DC02 | CI-004 |

These CI identifiers are placeholders until reconciled with the configuration item register.

### Configuration Item Attributes

Each server CI record should include:

- CI identifier
- Hostname
- Operating system
- IP address
- Virtualization platform
- Server roles
- Service relationships
- Dependencies
- Configuration baseline
- Operational status
- Change history
- Supporting evidence

---

## 19. Server Lifecycle Management

### 19.1 Planning

Identify the business or technical requirement for a server.

### 19.2 Deployment

Create the virtual machine, install the operating system, configure networking, and install required roles.

### 19.3 Configuration

Apply security settings, administrative access controls, and service configurations.

### 19.4 Operation

Monitor server availability and maintain required services.

### 19.5 Maintenance

Apply updates, review configurations, and resolve operational issues.

### 19.6 Recovery

Restore services using approved recovery procedures.

### 19.7 Decommissioning

Before decommissioning a server:

1. Identify dependent services.
2. Review operational impact.
3. Obtain applicable authorization.
4. Confirm recovery and retention requirements.
5. Migrate or retire services appropriately.
6. Remove the server using supported procedures.
7. Update DNS and directory records where applicable.
8. Update the server inventory.
9. Update related configuration items.
10. Preserve relevant evidence.

### Important

Domain controllers require specialized decommissioning procedures.

They should not be removed by simply deleting their virtual machines.

---

## 20. Troubleshooting Scenarios

The server inventory supports realistic IT troubleshooting exercises.

| Scenario | Potential Cause | Relevant Systems |
|---|---|---|
| Domain authentication failure | DNS or AD DS issue | DC01, DC02 |
| Replication failure | DNS, RPC, or network issue | DC01, DC02 |
| Server unavailable | VM, operating system, or network failure | DC01, DC02 |
| Incorrect time | Time service configuration | DC01, DC02 |
| Group Policy failure | DNS, SYSVOL, or policy issue | DC01, DC02 |
| Server Core management failure | Remote management or permissions | DC02 |
| Administrative connection failure | Routing, firewall, or authentication | MGMT01, DC01, DC02 |
| Low disk space | Storage utilization | DC01, DC02 |
| DNS resolution failure | DNS configuration | DC01, DC02 |

These are proposed scenarios, not claims of observed incidents.

### Troubleshooting Documentation

Each completed scenario should record:

1. Symptoms
2. Affected services
3. Business impact
4. Investigation
5. Technical findings
6. Root cause, when established
7. Corrective action
8. Verification
9. Lessons learned

---

## 21. ITIL 4 Integration

The Windows Server inventory supports the following practices.

| ITIL Practice | Application |
|---|---|
| Service Desk | Receives and coordinates server-related support requests |
| Incident Management | Investigates server and infrastructure interruptions |
| Problem Management | Identifies recurring infrastructure failures |
| Change Enablement | Controls server configuration changes |
| Monitoring and Event Management | Reviews server events and health |
| Service Configuration Management | Maintains server inventory and dependencies |
| Information Security Management | Reviews administrative access and server security |
| Knowledge Management | Maintains server administration procedures |
| Continual Improvement | Improves server reliability and administration |

### Example Operational Scenario

**Scenario:** DC02 experiences a replication failure.

Potential workflow:

1. Monitoring or a technician identifies the failure.
2. An incident is recorded.
3. The technician investigates replication and DNS.
4. A corrective action is selected.
5. Any required change authorization is obtained.
6. The corrective action is implemented.
7. Replication is verified.
8. The incident is resolved and closed.
9. Related documentation is updated.

This example is instructional and does not represent a completed incident.

---

## 22. Verification and Evidence Plan

### 22.1 Verification Objectives

Confirm the actual configuration of each server.

### 22.2 Verification Checklist

#### General Information

- [ ] Hostname verified
- [ ] Domain membership verified
- [ ] Operating system edition verified
- [ ] Operating system version verified
- [ ] Installation type verified

#### Network

- [ ] IPv4 address verified
- [ ] Subnet mask verified
- [ ] Default gateway verified
- [ ] DNS configuration verified
- [ ] Network connectivity tested

#### Virtualization

- [ ] Hyper-V VM identified
- [ ] VM generation recorded
- [ ] CPU allocation recorded
- [ ] Memory allocation recorded
- [ ] Virtual disk configuration recorded
- [ ] Virtual switch assignment verified

#### Server Roles

- [ ] Installed roles inventoried
- [ ] AD DS verified
- [ ] DNS verified
- [ ] Additional roles documented

#### Active Directory

- [ ] Domain controller status verified
- [ ] FSMO roles verified
- [ ] Replication checked
- [ ] DNS health checked
- [ ] Time synchronization checked

#### Security

- [ ] Administrative access reviewed
- [ ] Windows Firewall reviewed
- [ ] Security updates reviewed
- [ ] Audit configuration reviewed

#### Recovery

- [ ] Backup configuration reviewed
- [ ] Last successful backup identified
- [ ] Restore testing status recorded

---

## 23. Evidence Register

The following evidence records are placeholders until actual verification is performed.

| Evidence ID | Server | Evidence | Status |
|---|---|---|---|
| EVD-WS-001 | DC01 | Operating system information | Pending |
| EVD-WS-002 | DC01 | Network configuration | Pending |
| EVD-WS-003 | DC01 | Installed server roles | Pending |
| EVD-WS-004 | DC01 | Hyper-V configuration | Pending |
| EVD-WS-005 | DC01 | AD DS health | Pending |
| EVD-WS-006 | DC02 | Operating system information | Pending |
| EVD-WS-007 | DC02 | Network configuration | Pending |
| EVD-WS-008 | DC02 | Installed server roles | Pending |
| EVD-WS-009 | DC02 | Hyper-V configuration | Pending |
| EVD-WS-010 | DC02 | Replication verification | Pending |

### Evidence Requirements

Evidence should:

- Come from the actual TTT lab.
- Identify the relevant system.
- Show the configuration or result.
- Be dated when practical.
- Exclude credentials.
- Exclude unnecessary sensitive information.
- Distinguish expected results from observed results.
- Support the documented claim.

---

## 24. Future Infrastructure Expansion

Potential future Windows Server projects include:

- DHCP Server
- File Server
- Additional server roles
- Windows Server security hardening
- Advanced PowerShell automation
- Centralized event collection
- Monitoring and alerting
- Backup automation
- Disaster recovery testing
- Additional administrative tools
- Hybrid infrastructure integration

### Microsoft 365

Microsoft 365 infrastructure has not yet been deployed for Technical Techno Tech.

Future integration may include Microsoft Entra ID, Microsoft Intune, and hybrid identity services.

These services will be documented when implementation begins.

---

## 25. Skills Practiced

This project supports practical experience with:

- Windows Server administration
- Windows Server Core
- Active Directory Domain Services
- DNS administration
- Hyper-V
- Server inventory management
- IP configuration
- Remote administration
- PowerShell
- FSMO role management
- Active Directory replication
- Server health diagnostics
- Windows security
- Backup and recovery planning
- Configuration management
- Technical documentation
- ITIL-aligned infrastructure operations

---

## 27. What I Learned

The Windows Server inventory demonstrates the importance of maintaining accurate infrastructure records.

### Key Learning Areas

**1. Server Identification**

Every server should have a documented identity, purpose, and configuration.

**2. Infrastructure Dependencies**

Windows Server relies on networking, virtualization, DNS, and other services.

**3. Domain Controller Responsibilities**

Domain controllers provide authentication and directory services and must be maintained carefully.

**4. Server Core Administration**

Windows Server Core emphasizes command-line and remote administration.

**5. Configuration Verification**

Infrastructure documentation should reflect actual system settings rather than assumptions.

**6. Security and Maintenance**

Server security, updates, monitoring, and recovery planning are essential to reliable operations.

**7. Service Configuration Management**

Accurate server inventories help IT teams understand service dependencies, investigate incidents, and assess changes.

---

## 28. Document Review and Revision History

### Review Triggers

Review this inventory when:

- A server is deployed.
- A server is decommissioned.
- An IP address changes.
- A server role is installed or removed.
- Virtual hardware changes.
- Administrative responsibilities change.
- Security configurations change.
- A server is migrated.
- Infrastructure dependencies change.
- Configuration verification identifies inaccurate information.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT Windows Server inventory documenting DC01, DC02, infrastructure dependencies, configuration attributes, and verification requirements |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This inventory documents the existing TTT Windows Server lab and provides a structured method for validating its configuration.

Previously documented server details are included for continuity. Information that has not been verified is identified as pending.

Example commands, proposed operational procedures, and planned improvements do not represent completed technical activities.

All verification results and evidence must originate from actual authorized lab work.

The separate legacy homelab environment is excluded from this project.
