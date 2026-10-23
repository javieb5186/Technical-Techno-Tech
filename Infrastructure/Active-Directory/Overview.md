# Active Directory Overview

## Overview

This document provides a high-level overview of the Active Directory environment used within the Technical Techno Tech lab.

The environment supports:

- User identity management
- Authentication and authorization
- Group-based access control
- Hybrid identity synchronization with Microsoft Entra ID
- Windows domain management

## Domain Information

| Setting | Value |
|----------|----------|
| Domain Name | technicaltechnotech.com |
| Forest Functional Level | Windows Server 2025 |
| Domain Functional Level | Windows Server 2025 |
| Domain Controllers | DC01, MGMT01-DC02 |
| Microsoft Entra Connect | Enabled |

## Infrastructure Summary

| Component | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| AD Domain | `technicaltechnotech.com` |
| Forest Root Domain | `technicaltechnotech.com` |
| Forest Structure | Single-Domain Design |
| Domain Controllers | DC01 and MGMT01-DC02 |
| Domain Controller Type | Writable |
| Virtualization Platform | Hyper-V |
| Server Network | `10.20.10.0/24` |
| Client Network | `10.20.20.0/24` |
| Router | RTR01 — VyOS |
| Firewall | FW01 — OPNsense |
| Microsoft 365 | Limited |

### Domain Controller Inventory

| Server | IP Address | Installation Type | Role |
|---|---|---|---|
| DC01 | `10.20.10.10` | Windows Server Core | Writable Domain Controller |
| MGMT01-DC02 | `10.20.10.11` | Windows Server Desktop Experience | Additional Writable Domain Controller |

### FSMO Configuration

| FSMO Role | Current Holder |
|---|---|
| Schema Master | DC01 |
| Domain Naming Master | DC01 |
| RID Master | DC01 |
| PDC Emulator | DC01 |
| Infrastructure Master | DC01 |

### Active Directory Sites and Services

| Network | Subnet | Purpose |
|---|---|---|
| Servers | `10.20.10.0/24` | Domain controllers |
| Clients | `10.20.20.0/24` | Employee workstations |

## Active Directory Structure

### Microsoft Default Containers

These containers are automatically created by Active Directory.

- Builtin
- Computers
- Domain Controllers
- ForeignSecurityPrincipals
- Managed Service Accounts
- Users

### Organizational Units

| OU | Purpose |
|------|------|
| CloudSync | Objects synchronized to Microsoft Entra ID |
| Executives | Executive user accounts |
| HR | Human Resources users |
| IT | Information Technology users |
| Sales | Sales users |
| Disabled Users | Decommissioned user accounts |
| Groups | Security and distribution groups |
| Workstations | Domain-joined endpoint devices |

### Current Structure

```text
technicaltechnotech.com
├── Builtin
├── CloudSync
|   ├── Contractors
│   ├── Executives
│   ├── HR
│   ├── IT
│   └── Sales
├── Computers
├── Disabled Users
├── Domain Controllers
├── ForeignSecurityPrincipals
├── Groups
├── Managed Service Accounts
├── Users
└── Workstations
 
```

## Users

### User Statistics

| Account Type | Count |
|-------------|---------|
| Employees | 10 |
| Contractors | 2 |
| Service Accounts | 0 |
| Disabled Accounts | 0 |

### User Naming Convention

```text
firstname.lastname
```

Examples:

```text
anne.hathaway
tom.hanks
```

## Groups

### Security Groups

| Group Name | Purpose |
|------------|------------|
| Finance_RW | Finance file share access |
| Finance_Users | Finance department membership |

### Group Strategy

Access permissions are assigned through security groups rather than directly to user accounts.

Examples:

- File share access
- Departmental access
- Resource permissions

## Computers

### Workstations

| Computer Name | Purpose |
|---------------|-------------|
| CLIENT-01 | Domain-joined workstation |

### Servers

| Server | Role |
|--------|------|
| DC01 | Domain Controller |
| MGMT01-DC02 | Domain Controller and Management Server |

## Group Policy

### Configured GPOs

| GPO | Purpose |
|------|------|
| Default Domain Policy | Domain-wide security settings |
| Default Domain Controllers Policy | Domain controller security configuration |

## Hybrid Identity

### Microsoft Entra Integration

#### Synchronization Method

Microsoft Entra Connect

#### Synchronized Objects

- User accounts
- Password hashes

#### Synchronization Scope

Objects located within the CloudSync OU are synchronized to Microsoft Entra ID.

#### Manual Synchronization

```powershell
Start-ADSyncSyncCycle -PolicyType Delta
```

## Administrative Practices

### Identity Management

- Users are created in department-specific OUs.
- Disabled accounts are moved to the Disabled Users OU.
- Access is assigned through security groups.
- User identities are synchronized to Microsoft Entra ID through Entra Connect.

### Access Management

- Least privilege principles are followed.
- Group-based access control is used whenever possible.
- Administrative access is restricted to authorized accounts.
