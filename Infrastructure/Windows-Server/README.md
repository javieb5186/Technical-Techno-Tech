# Windows Server Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Domain:** `technicaltechnotech.com`  
**Platform:** Microsoft Windows Server  
**Virtualization:** Hyper-V  
**Status:** Existing Lab — Documentation and Verification Ongoing

---

## 1. Overview

This project documents the Windows Server infrastructure supporting Technical Techno Tech's internal business environment.

Windows Server provides centralized services for authentication, identity administration, DNS, and other infrastructure capabilities.

The project focuses on practical systems administration, troubleshooting, security, maintenance, and service management.

## 2. Objectives

- Deploy Windows Server virtual machines.
- Configure Windows Server networking.
- Install and manage server roles.
- Deploy Active Directory Domain Services.
- Configure DNS.
- Manage multiple domain controllers.
- Administer Windows Server Core.
- Perform remote administration.
- Manage user and computer accounts.
- Configure security and access controls.
- Monitor server health.
- Troubleshoot infrastructure failures.
- Practice backup and recovery.
- Document server configurations.

## 3. Server Inventory

| Server | IP Address | Operating System | Role |
|---|---|---|---|
| DC01 | `10.20.10.10` | Windows Server Desktop Experience | AD DS, DNS |
| DC02 | `10.20.10.11` | Windows Server Core | Additional domain controller |

### Domain Information

| Attribute | Value |
|---|---|
| Organization | Technical Techno Tech |
| Domain | `technicaltechnotech.com` |
| Server Network | `10.20.10.0/24` |
| Server Gateway | `10.20.10.1` |
| Virtualization Platform | Hyper-V |

## 4. Server Architecture

```text
        technicaltechnotech.com
                   |
         +---------+---------+
         |                   |
         v                   v
        DC01                DC02
   Desktop Experience     Server Core
         |                   |
         +---------+---------+
                   |
          Server Network
          10.20.10.0/24
                   |
                   v
              RTR01 - VyOS
                   |
          +--------+--------+
          |                 |
          v                 v
      Client Network   Management Network
          |                 |
          v                 v
       CLIENT01           MGMT01
```

## 5. Server Roles and Features

### Active Directory Domain Services

AD DS provides:

- Domain authentication
- Directory services
- User administration
- Group management
- Computer account management
- Organizational unit administration
- Group Policy integration

### DNS Server

DNS supports:

- Domain name resolution
- Domain controller discovery
- Active Directory service location
- Client name resolution

### Additional Roles

The project may expand to include:

- DHCP Server
- File and Storage Services
- Additional management services
- Other Windows Server roles

These additional roles should only be marked deployed after implementation and verification.

## 6. Domain Controller Administration

The environment includes two writable domain controllers.

### DC01

DC01 is a Windows Server installation with Desktop Experience.

Documented responsibilities include:

- Active Directory Domain Services
- DNS
- PDC Emulator role
- Domain administration

### DC02

DC02 uses Windows Server Core.

Documented responsibilities include:

- Additional writable domain controller
- Active Directory replication
- Domain service availability

### Administration Topics

- Domain controller promotion
- Replication
- FSMO roles
- DNS
- Time synchronization
- Domain controller discovery
- Server health verification

## 7. Windows Server Core

Windows Server Core provides a reduced graphical management environment.

Administration may use:

- SConfig
- PowerShell
- Windows Admin Center
- RSAT
- Remote PowerShell
- Command-line utilities

### Example Commands

Review system configuration:

```powershell
Get-ComputerInfo
```

Review installed roles:

```powershell
Get-WindowsFeature |
Where-Object Installed
```

Review network configuration:

```powershell
Get-NetIPConfiguration
```

Review services:

```powershell
Get-Service
```

## 8. Remote Administration

MGMT01 serves as an administrative workstation for the TTT environment.

Remote administration activities may include:

- Active Directory administration
- DNS administration
- Server role management
- PowerShell remoting
- Group Policy management
- Windows Server monitoring

### Administrative Tools

- RSAT
- Windows Admin Center
- Server Manager
- PowerShell
- Active Directory Administrative Center
- Active Directory Users and Computers
- DNS Manager
- Group Policy Management

Tool availability and remote connectivity should be verified for each administrative scenario.

## 9. Server Networking

Windows Server depends on the TTT network infrastructure.

### Server Network

`10.20.10.0/24`

### Domain Controllers

- DC01: `10.20.10.10`
- DC02: `10.20.10.11`

### Default Gateway

`10.20.10.1`

### Network Dependencies

- VyOS routing
- OPNsense firewall
- DNS
- Domain controller connectivity
- Hyper-V virtual networking

## 10. Server Health Monitoring

Server health checks may include:

- CPU usage
- Memory usage
- Storage capacity
- Network connectivity
- Windows services
- Event logs
- DNS health
- AD DS replication
- Time synchronization

### Example PowerShell Commands

```powershell
Get-Service
Get-Volume
Get-NetIPConfiguration
Get-WinEvent -LogName System -MaxEvents 20
```

### Active Directory Health

```powershell
dcdiag /q
repadmin /replsummary
```

Actual results should be captured and documented.

## 11. Security Administration

Security topics include:

- Administrative account management
- Least privilege
- Windows Firewall
- Security groups
- NTFS permissions
- Shared folder permissions
- Password policies
- Account auditing
- Windows updates
- Privileged access

## 12. Backup and Recovery

Windows Server recovery topics include:

- Windows Server Backup
- System State Backup
- Active Directory recovery
- Backup scheduling
- Recovery verification
- FSMO role management
- Domain controller recovery planning

Backup and restoration are separate operational activities.

Successful backup completion does not establish successful recovery without testing.

## 13. PowerShell Administration

PowerShell supports:

- Server inventory
- Service management
- User administration
- Group management
- Network diagnostics
- Event log inspection
- Remote administration
- Configuration verification
- Administrative automation

### Example Commands

List domain controllers:

```powershell
Get-ADDomainController -Filter *
```

Review domain information:

```powershell
Get-ADDomain
```

Review FSMO role holders:

```powershell
netdom query fsmo
```

Review replication:

```powershell
repadmin /replsummary
```

## 14. Troubleshooting Scenarios

Potential exercises include:

- Domain controller unavailable
- DNS resolution failure
- Replication failure
- Windows service stopped
- Incorrect network configuration
- Server Core administration failure
- Domain authentication issue
- Time synchronization failure
- Group Policy processing issue
- Insufficient administrative permissions
- Disk capacity issue

Each scenario should document:

1. Symptoms
2. Business impact
3. Investigation
4. Technical findings
5. Corrective action
6. Verification
7. Lessons learned

## 15. ITIL 4 Integration

| Practice | Example |
|---|---|
| Service Request Management | Account and server resource requests |
| Incident Management | Server or domain service failures |
| Problem Management | Recurring server issues |
| Change Enablement | Server role or configuration changes |
| Monitoring and Event Management | Server health events |
| Service Configuration Management | Server inventory and dependencies |
| Information Security Management | Administrative access and security configuration |
| Knowledge Management | Server troubleshooting articles |
| Continual Improvement | Improving maintenance and recovery procedures |

## 16. Documentation

- [Server Inventory](Server-Inventory.md)
- [Server Roles](Server-Roles.md)
- [Infrastructure Overview](../README.md)
- [Active Directory](../Active-Directory/README.md)
- [Networking](../Networking/README.md)
- [Hyper-V](../Virtualization/Hyper-V/README.md)
- [Configuration Item Standards](../../Service-Configuration-Management/Configuration-Items/README.md)

## 17. Skills Practiced

- Windows Server administration
- Server Core administration
- Active Directory Domain Services
- DNS administration
- PowerShell
- Remote administration
- Server troubleshooting
- Replication monitoring
- Windows security
- Access control
- Backup and recovery
- Infrastructure documentation

## 18. What I Learned

This project provides practical experience managing Windows Server systems within a business network.

Key learning areas include:

- How Windows Server provides centralized infrastructure services.
- How domain controllers support authentication and directory operations.
- How Server Core differs from Desktop Experience.
- How remote administration reduces the need for direct server access.
- How DNS, networking, and virtualization affect server availability.
- How to use PowerShell and administrative tools to diagnose problems.
- Why server security, maintenance, and recovery planning matter.

## 19. Future Development

Potential future activities include:

- DHCP deployment
- File server administration
- Additional Group Policy exercises
- Advanced PowerShell automation
- Server security hardening
- Monitoring and alerting
- Disaster recovery testing
- Additional Windows Server roles
- Hybrid infrastructure integration when cloud services are introduced

Future activities are not represented as completed implementations.

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This README documents the Windows Server infrastructure and its associated administration activities.

Technical configurations, implementation results, and operational claims should be supported by actual lab evidence.

Microsoft 365 infrastructure has not yet been deployed as part of the TTT environment.
