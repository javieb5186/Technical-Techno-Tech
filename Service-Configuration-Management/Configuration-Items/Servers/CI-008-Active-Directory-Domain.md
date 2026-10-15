# CI-008 — Active Directory Domain

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-008 |
| **CI Name** | Active Directory Domain — technicaltechnotech.com |
| **Organization** | Technical Techno Tech |
| **CI Type** | Logical Infrastructure — Directory Service |
| **CI Category** | Identity & Access Management |
| **Environment** | Simulated Enterprise — On-Premises Active Directory |
| **Status** | Active — Previously Documented; Current State Pending Verification |
| **Owner** | Internal IT |
| **Managed By** | Identity & Systems Administrator |
| **Date Created** | Not Recorded |
| **Last Updated** | 2026-10-14 |
| **Last Verified** | Not Yet Verified for This Record |
| **Related IT Service** | IT-SVC-001 — Identity & Access Management |

---

## 1. Configuration Item Overview

### Description

`technicaltechnotech.com` is the Active Directory Domain Services (AD DS) domain used within Technical Techno Tech's simulated enterprise environment.

The domain provides centralized identity management, authentication, authorization, and Group Policy administration for domain-joined systems.

The documented domain controller infrastructure consists of:

- **DC01:** Windows Server with Desktop Experience
- **DC02:** Windows Server Core

Both domain controllers are associated with the server network.

The domain is a logical configuration item. Its operation depends on the domain controllers, DNS services, networking, and virtualization infrastructure.

### Business Purpose

The Active Directory domain supports centralized administration of organizational identities and resources.

Its primary purposes include:

- Centralized user authentication
- Computer account management
- Security group management
- Organizational unit administration
- Group Policy management
- Delegated administration
- Access control for network resources
- Domain controller replication
- Directory service availability
- Employee onboarding and offboarding

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Primary directory and authentication infrastructure |
| IT-SVC-002 | Endpoint Management | Supports domain-joined workstation administration |
| IT-SVC-005 | Server & Infrastructure Services | Provides directory services to Windows infrastructure |
| IT-SVC-006 | Information Security | Supports authentication, authorization, and security policies |
| IT-SVC-007 | Employee IT Lifecycle | Supports user provisioning and deprovisioning |

**Reference:** [IT Service Catalog](../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** Logical Infrastructure — Directory Service
- **CI Category:** Identity & Access Management
- **Criticality:** Critical — Proposed Classification
- **Lifecycle Status:** Active — Pending Current-State Verification

### Ownership

| Responsibility | Assigned Role |
|---|---|
| **Service Owner** | Internal IT |
| **Technical Owner** | Identity & Systems Administrator |
| **Primary Administrator** | Active Directory Administrator |
| **Support Team** | Internal IT |

These responsibilities are simulated for the TTT environment.

### Business Criticality

The Active Directory domain provides authentication and identity services for the TTT infrastructure.

Its failure could affect:

- Domain user authentication
- Computer authentication
- Group Policy processing
- Access to domain-controlled resources
- DNS-based domain controller discovery
- Centralized user administration
- Security group authorization
- Administrative operations

The actual impact depends on which domain controllers and supporting services remain available.

---

## 3. Technical Specifications

### General Information

| Attribute | Value |
|---|---|
| **Domain DNS Name** | `technicaltechnotech.com` |
| **Directory Service** | Active Directory Domain Services |
| **Domain Type** | On-Premises AD DS |
| **Forest Root Domain** | Expected: `technicaltechnotech.com` — Verify |
| **Forest Name** | Expected: `technicaltechnotech.com` — Verify |
| **NetBIOS Domain Name** | Pending Verification |
| **Domain Functional Level** | Pending Verification |
| **Forest Functional Level** | Pending Verification |
| **Schema Version** | Pending Verification |
| **Domain Controllers** | DC01 and DC02 — Previously Documented |
| **AD Sites** | Pending Verification |
| **Global Catalog Servers** | Pending Verification |
| **FSMO Role Holders** | Pending Verification |
| **Domain Recycle Bin** | Previously Practiced; Current State Pending Verification |

### Domain Controller Infrastructure

| Domain Controller | Operating System | IP Address | Role |
|---|---|---|---|
| DC01 | Windows Server — Desktop Experience | `10.20.10.10` | Domain Controller / DNS |
| DC02 | Windows Server Core | `10.20.10.11` | Additional Domain Controller; DNS Role Pending Verification |

The current domain controller roles, DNS services, and replication health require verification.

### Network Configuration

| Attribute | Value |
|---|---|
| **Domain DNS Namespace** | `technicaltechnotech.com` |
| **Server Network** | `10.20.10.0/24` |
| **Server Gateway** | `10.20.10.1` |
| **DC01 Address** | `10.20.10.10` |
| **DC02 Address** | `10.20.10.11` |
| **Client Network** | `10.20.20.0/24` |
| **Management Network** | `10.20.30.0/24` |
| **DNS Zone Configuration** | Pending Verification |
| **DNS Replication Scope** | Pending Verification |

### Domain Verification

Run from an authorized management workstation or domain controller with the Active Directory PowerShell module:

```powershell
Get-ADDomain
```

```powershell
Get-ADForest
```

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName,Site,IPv4Address,IsGlobalCatalog
```

Review the FSMO role holders:

```powershell
netdom query fsmo
```

**Verification Status:** Not Yet Completed

---

## 4. Installed Roles, Services & Software

### Directory Services and Features

| Service / Feature | Purpose | Configuration Status |
|---|---|---|
| Active Directory Domain Services | Centralized directory and authentication | Previously Deployed |
| Active Directory DNS Integration | Domain name resolution and service discovery | Previously Practiced |
| Group Policy | Centralized configuration management | Previously Practiced |
| Security Groups | Authorization and access management | Previously Practiced |
| Organizational Units | Logical organization and delegation | Previously Configured |
| AD Replication | Synchronizes directory data between DCs | Previously Practiced |
| Fine-Grained Password Policies | Additional password policy control | Previously Practiced |
| AD Recycle Bin | Recovery of deleted directory objects | Previously Practiced |

### Administrative Tools

| Tool | Purpose | Usage Status |
|---|---|---|
| Active Directory Users and Computers | Manage users, groups, and OUs | Previously Used |
| Active Directory Administrative Center | Advanced AD management | Previously Used |
| Group Policy Management Console | Manage GPOs | Previously Used |
| Active Directory PowerShell Module | Automate directory administration | Previously Used |
| Repadmin | Diagnose replication | Available for Verification |
| Dcdiag | Diagnose domain controller health | Previously Used |
| Windows Admin Center | Remote server administration | Previously Used |

### Running Services

Active Directory relies on services hosted by domain controllers.

| Service | Purpose | Expected State |
|---|---|---|
| Active Directory Domain Services | Directory database and authentication | Operational |
| DNS Server | Domain name resolution, where installed | Operational |
| Kerberos Key Distribution Center | Kerberos authentication | Operational |
| Netlogon | Domain authentication and DC discovery | Operational |
| DFS Replication | SYSVOL replication, where configured | Operational |

Actual service states must be checked on each domain controller.

---

## 5. Configuration Baseline

### Approved Configuration

The intended domain configuration includes:

- Domain namespace `technicaltechnotech.com`
- Two writable domain controllers
- Functional Active Directory replication
- Operational DNS-based domain controller discovery
- Appropriate organizational unit structure
- Departmental security groups
- Group Policy administration
- Restricted privileged access
- Delegated administration where appropriate
- Documented FSMO role holders
- Reliable domain time synchronization
- Supported backup and recovery procedures

This is a proposed configuration baseline. Formal approval has not been recorded.

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| Domain Name | `technicaltechnotech.com` | Previously Documented | Pending Verification |
| Forest Root | `technicaltechnotech.com` | Expected | Pending Verification |
| Domain Controllers | DC01 and DC02 | Previously Documented | Pending Verification |
| AD Replication | Healthy | Previously Practiced | Pending Verification |
| DNS Services | Operational | Previously Practiced | Pending Verification |
| SYSVOL | Available and Replicated | Unknown | Pending Verification |
| FSMO Roles | Assigned to Healthy DCs | Previously Practiced | Pending Verification |
| Time Synchronization | Reliable Domain Time Hierarchy | Previously Troubleshot | Pending Verification |
| Organizational Units | Match Approved Structure | Previously Configured | Pending Verification |
| Security Groups | Match Access Requirements | Previously Configured | Pending Verification |
| Group Policy | Approved Policies Applied | Previously Practiced | Pending Verification |
| Privileged Access | Restricted | Unknown | Pending Verification |
| AD Recycle Bin | Enabled if Approved | Previously Practiced | Pending Verification |
| System State Backup | Successful According to Policy | Previously Practiced | Pending Verification |

### Organizational Unit Baseline

The previously documented organizational unit structure includes:

```text
technicaltechnotech.com
|
+-- IT
+-- Executives
+-- HR
+-- Sales
+-- Groups
+-- Workstations
```

The current OU hierarchy and any additional nested OUs require verification.

### Group Configuration

Previously practiced group-management activities include:

- Departmental security groups
- Distribution groups
- Group scope selection
- Group nesting
- Resource permission assignments
- Delegated administration

The current group inventory and membership must be verified.

### Configuration Policies

Potentially applicable policies include:

- Domain password policy
- Account lockout policy
- Fine-grained password policies
- Privileged access restrictions
- Organizational unit delegation
- Group Policy change management
- Security auditing
- Domain controller backup procedures
- Active Directory recovery procedures

### Configuration Verification

**Last Verified:** Not Yet Verified

**Verification Method:** Active Directory PowerShell, ADAC, GPMC, Dcdiag, Repadmin

**Verification Result:** Not Assessed

**Notes:**

Previous TTT exercises included domain controller administration, replication troubleshooting, password policies, security groups, OU delegation, and Active Directory recovery features.

The current domain state must be verified before recording compliance.

---

## 6. Relationships & Dependencies

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| CI-001 — DC01 | Hosted By / Depends On | Domain controller providing directory services |
| CI-002 — DC02 | Hosted By / Depends On | Additional domain controller |
| CI-004 — RTR01 | Depends On | Routing between internal network segments |
| CI-005 — MGMT01 | Administered From | Management workstation |
| CI-006 — CLIENT01 | Provides Services To | Domain-joined employee workstation |
| CI-007 — Hyper-V Host | Depends On | Virtualization platform hosting domain controllers |
| CI-009 — Virtual Networks | Depends On | Network connectivity between systems |

### Upstream Dependencies

The Active Directory domain depends on:

- Domain controller availability
- DNS services
- Network connectivity
- Domain controller replication
- Reliable time synchronization
- SYSVOL availability
- Hyper-V infrastructure
- Storage availability
- Appropriate security configuration

### Downstream Dependencies

Services and systems relying on Active Directory include:

- Domain-joined workstations
- Domain-joined servers
- Employee authentication
- Administrative authentication
- Group Policy processing
- Security group authorization
- User provisioning
- Domain-controlled resource access

### Dependency Diagram

```text
                     Hyper-V Host
                          |
                 +--------+--------+
                 |                 |
                 v                 v
                DC01              DC02
                 |                 |
                 +--------+--------+
                          |
                          v
              Active Directory Domain
              technicaltechnotech.com
                          |
             +------------+------------+
             |                         |
             v                         v
          MGMT01                    CLIENT01
       Administration          Employee Endpoint
```

**Reference:** [Domain Architecture](../../../Infrastructure/Active-Directory/Domain-Architecture.md)

### Impact of CI Failure

If domain services become unavailable:

- Users may be unable to authenticate to domain resources.
- New domain logons may fail.
- Group Policy processing may be interrupted.
- Directory administration may become unavailable.
- Domain-integrated applications may experience authentication failures.
- Access to shared resources may be affected.

Some previously authenticated users may still sign in using cached credentials, depending on workstation configuration and applicable policies.

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Domain Administration | Domain Admins | Privileged Administration |
| Enterprise Administration | Enterprise Admins | Forest-Level Administration |
| Standard User Access | Domain Users | Standard Domain Access |
| Delegated Administration | Authorized Delegated Groups | Scoped Permissions |
| Domain Controller Administration | Authorized Administrators | Restricted Privileged Access |

Actual memberships, delegations, and permissions require verification.

### Security Controls

Recommended controls include:

- Least-privilege administration
- Separate privileged accounts
- Protected Users group where appropriate
- Strong password policies
- Fine-grained password policies where required
- Account lockout controls
- Security event auditing
- Restricted domain controller access
- Secure DNS configuration
- Domain controller patching
- Active Directory backups
- Controlled Group Policy changes

### Privileged Group Review

Review membership of:

- Domain Admins
- Enterprise Admins
- Schema Admins
- Administrators
- Account Operators
- Server Operators
- Backup Operators

Membership should be reviewed against documented administrative responsibilities.

### Security Review

**Last Security Review:** Not Recorded

**Security Status:** Not Assessed

### Security Notes

The Active Directory domain is a critical identity and security component.

Unauthorized changes to privileged groups, authentication policies, directory permissions, or Group Policy can affect multiple systems.

---

## 8. Monitoring & Maintenance

### Monitoring Configuration

| Monitoring Item | Tool / Method | Expected Condition |
|---|---|---|
| Domain Controller Availability | Connectivity / Service Checks | Required DCs Operational |
| AD Replication | Repadmin | Healthy |
| Domain Controller Health | Dcdiag | No Unresolved Critical Failures |
| DNS | DNS Diagnostics | Required Records Resolve |
| SYSVOL | Share and Replication Checks | Available |
| FSMO Roles | Netdom / PowerShell | Assigned to Available DCs |
| Time Synchronization | W32tm | Correct Time Source |
| Security Events | Event Viewer | Reviewed |
| Directory Backups | Backup Tool | Successful According to Policy |

No automated monitoring deployment is confirmed.

### Maintenance Activities

- Review domain controller health.
- Verify replication.
- Verify DNS.
- Review security logs.
- Review privileged group membership.
- Review Group Policy changes.
- Verify time synchronization.
- Review password policies.
- Verify backups.
- Test documented recovery procedures.

### Maintenance Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Identity & Systems Administrator

**Last Maintenance:** Not Recorded

**Next Planned Maintenance:** Not Scheduled

### Diagnostic Commands

Review replication:

```powershell
repadmin /replsummary
```

Review detailed replication status:

```powershell
repadmin /showrepl
```

Run domain controller diagnostics:

```powershell
dcdiag /q
```

Verify domain controller discovery:

```powershell
nltest /dsgetdc:technicaltechnotech.com
```

Review FSMO role holders:

```powershell
netdom query fsmo
```

Review domain controllers:

```powershell
Get-ADDomainController -Filter *
```

Review time synchronization:

```powershell
w32tm /query /status
```

**Execution Status:** Commands Provided — Results Not Yet Recorded

---

## 9. Backup & Recovery

### Backup Configuration

**Backup Required:** Yes

**Backup Method:** Supported Active Directory System State Backup — Recommended

**Backup Frequency:** Not Yet Established

**Backup Destination:** Pending Verification

**Last Successful Backup:** Not Recorded

### Recovery Information

**Recovery Procedure:** Pending Documentation

**Recovery Dependencies:**

- Supported domain controller backups
- Windows Server recovery environment
- Available compute and storage resources
- Network connectivity
- DNS configuration
- Authorized recovery credentials
- Documented Active Directory recovery procedures

**Recovery Testing:** Not Recorded

### Recovery Considerations

Active Directory recovery procedures depend on the failure scenario.

Possible scenarios include:

1. Accidental deletion of directory objects
2. Failure of an individual domain controller
3. DNS configuration corruption
4. Replication failures
5. Loss of all domain controllers
6. Forest-wide recovery requirements

Potential recovery methods include:

- Active Directory Recycle Bin recovery
- Rebuilding an additional domain controller from a healthy DC
- System State recovery
- Authoritative or non-authoritative recovery, where appropriate
- Forest recovery procedures

The recovery method must match the incident and follow supported Microsoft procedures.

### Recovery Planning

A recovery plan should identify:

- Backup locations
- Backup integrity verification
- Recovery credentials
- FSMO role holders
- DNS dependencies
- Replication dependencies
- Recovery sequence
- Post-recovery verification procedures

Hyper-V checkpoints are not substitutes for supported Active Directory backups.

---

## 10. Configuration History

Track significant changes affecting the Active Directory domain.

| Date | Change ID | Description | Result |
|---|---|---|---|
| Not Recorded | N/A | Initial AD DS domain deployment | Previously Documented |
| Not Recorded | N/A | Additional domain controller deployment | Previously Documented |
| Not Recorded | N/A | OU and group configuration | Previously Practiced |
| Not Recorded | N/A | Delegated administration | Previously Practiced |
| Not Recorded | N/A | Password policy exercises | Previously Practiced |
| Not Recorded | N/A | Replication and time service troubleshooting | Previously Practiced |
| Not Recorded | N/A | Active Directory Recycle Bin configuration | Previously Practiced |
| Not Recorded | N/A | System State backup exercises | Previously Practiced |

### Current Configuration Summary

The Active Directory domain is documented as `technicaltechnotech.com`.

DC01 and DC02 provide the documented domain controller infrastructure.

Previous lab activities included:

- User and group management
- Organizational units
- Delegation
- Group Policy
- Password policies
- Replication troubleshooting
- FSMO role management
- Backup and recovery exercises

The current domain configuration and health require verification.

---

## 11. Related Operational Records

### Incidents

N/A — No incident linked to this CI record.

### Problems

N/A — No problem record linked.

### Changes

N/A — No change record linked.

### Service Requests

N/A — No service request linked.

### Knowledge Articles

N/A — No knowledge article linked.

### Infrastructure Documentation

- [Domain Architecture](../../../Infrastructure/Active-Directory/Domain-Architecture.md)
- [Organizational Units](../../../Infrastructure/Active-Directory/Organizational-Units.md)
- [Group Structure](../../../Infrastructure/Active-Directory/Group-Structure.md)
- [Server Inventory](../../../Infrastructure/Windows-Server/Server-Inventory.md)
- [Network Topology](../../../Infrastructure/Networking/Network-Topology.md)
- [DC01 Configuration Item](CI-001-DC01.md)
- [DC02 Configuration Item](CI-002-DC02.md)
- [MGMT01 Configuration Item](../Workstations/CI-005-MGMT01.md)
- [CLIENT01 Configuration Item](../Workstations/CI-006-CLIENT01.md)

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Domain Name | `technicaltechnotech.com` | Not Yet Collected | Pending |
| Forest Root | Documented | Not Yet Collected | Pending |
| Domain Functional Level | Recorded | Not Yet Collected | Pending |
| Forest Functional Level | Recorded | Not Yet Collected | Pending |
| Domain Controllers | DC01 and DC02 | Not Yet Collected | Pending |
| Global Catalog | Required GC Availability | Not Yet Collected | Pending |
| DNS | Required Domain Records Resolve | Not Yet Collected | Pending |
| AD Replication | Healthy | Not Yet Collected | Pending |
| SYSVOL | Available | Not Yet Collected | Pending |
| FSMO Roles | Assigned to Healthy DCs | Not Yet Collected | Pending |
| Time Synchronization | Correct Domain Time Hierarchy | Not Yet Collected | Pending |
| Organizational Units | Match Approved Structure | Not Yet Collected | Pending |
| Security Groups | Match Access Requirements | Not Yet Collected | Pending |
| Group Policy | Applicable Policies Operational | Not Yet Collected | Pending |
| Privileged Access | Restricted Appropriately | Not Yet Collected | Pending |
| AD Recycle Bin | Configuration Documented | Not Yet Collected | Pending |
| System State Backup | Successful According to Policy | Not Yet Collected | Pending |

### Supporting Evidence

No evidence files have been attached to this record.

Recommended evidence:

- `Get-ADDomain` output
- `Get-ADForest` output
- Domain controller inventory
- FSMO role holders
- Replication summary
- Dcdiag results
- DNS verification
- Organizational unit structure
- Group inventory
- Group Policy inventory
- Time synchronization status
- Backup verification

Only verified, sanitized evidence should be added to the repository.

Do not publish passwords, privileged credentials, recovery secrets, or other sensitive information.

### Verification Summary

**Verification Status:** Not Yet Completed

The documented Active Directory configuration must be compared against the live domain.

No verification item is marked as passed without supporting evidence.

---

## 13. Lifecycle Management

### Lifecycle Information

| Field | Details |
|---|---|
| **Deployment Date** | Not Recorded |
| **Current Lifecycle Stage** | Active — Pending Verification |
| **Last Major Update** | Not Recorded |
| **Planned Replacement / Retirement** | Not Scheduled |
| **Retirement Date** | N/A |

### Retirement Considerations

Before retiring the Active Directory domain:

1. Identify all dependent users, computers, and applications.
2. Review authentication and authorization dependencies.
3. Identify replacement identity services.
4. Develop a migration plan.
5. Back up required directory data.
6. Migrate users, groups, and resources as appropriate.
7. Update domain-joined systems.
8. Verify replacement authentication services.
9. Decommission domain controllers using supported procedures.
10. Update DNS and network configuration.
11. Update CI relationships and documentation.
12. Complete the retirement review.

### Lifecycle Notes

No domain retirement activity is currently documented.

---

## 14. Lessons Learned

### What I Learned

**1. Active Directory Domain Services**

AD DS provides centralized authentication, authorization, and directory management.

**2. Domain Controllers**

Domain controllers host directory services and replicate directory information.

**3. Organizational Units**

OUs organize directory objects and support delegation and Group Policy targeting.

**4. Security Groups**

Security groups simplify access management by assigning permissions to groups rather than individual users.

**5. Group Policy**

Group Policy provides centralized configuration management for domain users and computers.

**6. Active Directory Replication**

Replication helps maintain directory consistency between domain controllers.

**7. FSMO Roles**

FSMO roles provide specialized operations that require designated role holders.

**8. Backup and Recovery**

Active Directory requires recovery planning that accounts for directory data, replication, DNS, and domain controller availability.

**9. Service Configuration Management**

Documenting the domain as a logical CI helps connect individual servers, workstations, and services to the broader identity infrastructure.

### Skills Practiced

- ITIL 4 Service Configuration Management
- Active Directory Domain Services
- Windows Server Administration
- Domain Controller Management
- DNS
- Organizational Unit Management
- Security Group Management
- Group Policy
- Delegated Administration
- Fine-Grained Password Policies
- Active Directory Replication
- FSMO Role Management
- PowerShell
- Active Directory Backup and Recovery
- Configuration Baseline Design
- Technical Documentation

### Improvement Opportunities

- Verify the forest and domain functional levels.
- Document the current FSMO role holders.
- Verify replication health.
- Verify DNS configuration.
- Inventory OUs and groups.
- Review privileged group membership.
- Review delegated permissions.
- Verify password policies.
- Review Group Policy objects.
- Establish routine domain health checks.
- Document tested backup and recovery procedures.
- Link future Jira records to CI-008.

---

## 15. Configuration Item Review

| Field | Details |
|---|---|
| **CI Status** | Active — Pending Verification |
| **Configuration Verified** | No |
| **Documentation Current** | No — Initial Draft Pending Verification |
| **Dependencies Documented** | Partially |
| **Security Reviewed** | No |
| **Last Review Date** | Not Yet Reviewed |
| **Next Review Date** | Not Scheduled |

### Review Summary

CI-008 has been documented using the Technical Techno Tech Configuration Item Template.

The record identifies the Active Directory domain as a logical configuration item supporting identity, authentication, authorization, and centralized administration.

Outstanding activities include:

- Verify domain and forest properties.
- Confirm domain controller roles.
- Verify replication and DNS health.
- Document FSMO role holders.
- Review OU and group structures.
- Review security policies and privileged access.
- Verify backup and recovery capabilities.
- Collect technical evidence.
- Complete the formal CI review.

**Overall Record Status:** Draft — Awaiting Configuration Verification

---

## 16. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial Active Directory domain configuration item record aligned with the TTT CI template |

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations and infrastructure relationships are based on previously documented lab activities. Current verification results are not assumed.

Business ownership, administrative responsibilities, and operational processes are simulated for educational and portfolio purposes.
