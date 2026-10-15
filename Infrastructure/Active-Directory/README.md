# Active Directory Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Domain:** `technicaltechnotech.com`  
**Platform:** Microsoft Active Directory Domain Services (AD DS)  
**Environment:** Hyper-V Virtualized Infrastructure  
**Status:** Existing Lab — Documentation and Verification Ongoing

---

## 1. Overview

This project documents the deployment, configuration, administration, and troubleshooting of Active Directory Domain Services for Technical Techno Tech, a fictional company used to simulate enterprise IT operations.

The Active Directory environment provides centralized identity management, authentication, authorization, and domain administration for Windows Server and domain-joined workstations.

The project focuses on practical Windows Server administration and ITIL-aligned operational documentation.

## 2. Objectives

- Deploy and administer an Active Directory forest and domain.
- Configure multiple writable domain controllers.
- Implement organizational units and security groups.
- Manage employee accounts and computer objects.
- Delegate administrative responsibilities.
- Configure and test Group Policy.
- Manage access to departmental resources.
- Verify Active Directory replication.
- Troubleshoot domain services and authentication.
- Practice backup and recovery procedures.
- Document administrative actions and verification evidence.

## 3. Domain Architecture

| Component | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| AD Domain | `technicaltechnotech.com` |
| Forest Root | `technicaltechnotech.com` |
| Primary Domain Controller | DC01 |
| Additional Domain Controller | DC02 |
| Domain Controller Type | Writable |
| Administrative Workstation | MGMT01 |
| Domain Client | CLIENT01 |
| Server Subnet | `10.20.10.0/24` |
| Client Subnet | `10.20.20.0/24` |
| Management Subnet | `10.20.30.0/24` |

### Domain Controllers

| Server | IP Address | Role |
|---|---|---|
| DC01 | `10.20.10.10` | AD DS, DNS, PDC Emulator |
| DC02 | `10.20.10.11` | Additional writable domain controller |

### Workstations

| Device | IP Address | Purpose |
|---|---|---|
| MGMT01 | `10.20.30.10` | Domain administration |
| CLIENT01 | `10.20.20.10` | Employee workstation testing |

## 4. Architecture

```text
technicaltechnotech.com
          |
          +-- DC01
          |     AD DS / DNS
          |     PDC Emulator
          |
          +-- DC02
          |     Additional Writable DC
          |
          +-- MGMT01
          |     Administrative Workstation
          |
          +-- CLIENT01
                Domain-Joined Workstation
```

The domain controllers reside on the server network, while management and client systems reside on separate network segments.

Routing between segments is provided through the TTT network infrastructure.

## 5. Active Directory Administration

The project includes practical experience with:

### User Administration

- Creating user accounts
- Modifying account attributes
- Enabling and disabling accounts
- Resetting passwords
- Managing account membership
- Performing employee onboarding and offboarding

### Organizational Units

The lab has included departmental and administrative OUs such as:

- IT
- Executives
- HR
- Sales
- Groups
- Workstations

The organizational structure supports logical administration, delegation, and Group Policy targeting.

### Group Management

Topics practiced include:

- Security groups
- Distribution groups
- Global groups
- Domain local groups
- Group nesting
- Resource permissions

The project applies role-based access principles and the AGDLP model where appropriate.

### Delegated Administration

Delegation exercises include assigning limited administrative responsibilities without granting unrestricted domain administration privileges.

## 6. Group Policy

Group Policy provides centralized management of Windows computer and user settings.

Project activities include:

- Creating Group Policy Objects
- Linking GPOs to organizational units
- Applying security settings
- Testing policy application
- Troubleshooting Group Policy processing
- Verifying effective policies

Example verification commands:

```powershell
gpupdate /force
gpresult /r
gpresult /h C:\Temp\gpresult.html
```

Individual GPO configurations and verified results should be documented separately.

## 7. DNS and Domain Services

Active Directory depends on DNS for domain controller discovery and related services.

Administration and troubleshooting include:

- DNS client configuration
- Domain controller discovery
- DNS record verification
- Domain authentication troubleshooting
- Domain controller replication
- Time synchronization

Example commands:

```powershell
Resolve-DnsName technicaltechnotech.com
nltest /dsgetdc:technicaltechnotech.com
dcdiag /q
repadmin /replsummary
```

These commands are reference examples. Results must be captured from actual lab execution.

## 8. Replication and Time Synchronization

The environment includes two writable domain controllers.

Previous lab work included:

- Configuring DC01 as the PDC Emulator
- Configuring DC01 to use an external time source
- Reviewing Hyper-V time synchronization behavior
- Troubleshooting domain controller advertising
- Verifying domain controller discovery

Time synchronization and replication should be rechecked whenever domain controller configurations change.

## 9. Security and Access Control

Security topics include:

- Least privilege
- Administrative delegation
- Password policies
- Fine-grained password policies
- Protected Users
- Security group membership
- NTFS permissions
- Shared folder access
- Administrative account management
- Auditing

Security configurations must be documented with actual implementation and verification evidence.

## 10. Backup and Recovery

The project includes Active Directory recovery concepts and lab exercises involving:

- System State Backup
- Active Directory Recycle Bin
- Domain controller recovery
- FSMO role management
- Restoration planning

Recovery testing should be documented separately from backup configuration.

A successful backup operation does not independently prove that restoration will succeed.

## 11. Administrative Tools

- Active Directory Users and Computers
- Active Directory Administrative Center
- Active Directory PowerShell Module
- Group Policy Management
- DNS Manager
- Windows Admin Center
- Remote Server Administration Tools
- PowerShell
- Windows Server Manager

## 12. ITIL 4 Integration

| Practice | Example Application |
|---|---|
| Service Request Management | Employee account creation and access requests |
| Incident Management | Domain authentication failures |
| Problem Management | Recurring DNS or replication failures |
| Change Enablement | Domain controller configuration changes |
| Knowledge Management | AD administration and troubleshooting guides |
| Service Configuration Management | Domain controller and dependency records |
| Information Security Management | Access control and privileged administration |
| Continual Improvement | Improving account management workflows |

## 13. Documentation

- [Domain Architecture](Domain-Architecture.md)
- [Organizational Units](Organizational-Units.md)
- [Group Structure](Group-Structure.md)
- [Infrastructure Overview](../README.md)
- [Windows Server](../Windows-Server/README.md)
- [Networking](../Networking/README.md)
- [Hyper-V](../Virtualization/Hyper-V/README.md)

## 14. Skills Practiced

- Active Directory administration
- Windows Server administration
- Domain controller deployment
- DNS troubleshooting
- Group Policy management
- PowerShell administration
- Identity and access management
- Security group design
- Permission management
- Replication troubleshooting
- Backup and recovery planning
- Technical documentation

## 15. What I Learned

This project provides practical experience managing a centralized Windows domain environment.

Key learning areas include:

- How domain controllers provide authentication and directory services.
- Why DNS is critical to Active Directory.
- How organizational units simplify administration.
- How group scopes and permissions control resource access.
- How delegation reduces unnecessary administrative privileges.
- How replication and time synchronization affect domain health.
- How to troubleshoot domain services using administrative tools and PowerShell.

## 16. Future Development

Potential future activities include:

- Additional Group Policy exercises
- Advanced security hardening
- Disaster recovery testing
- Additional automation
- Expanded auditing
- Hybrid identity integration when cloud infrastructure is introduced

Future activities are not represented as completed implementations.

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization used for hands-on IT training.

This README describes the TTT Active Directory project and its documented learning scope. Configuration details and outcomes should be supported by actual lab evidence.
