# Technical Techno Tech — Active Directory Domain Architecture

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Architecture  
**Document ID:** INF-AD-001  
**Version:** 1.0  
**Status:** Existing Lab — Configuration Verification Ongoing  
**Practice:** Service Configuration Management  
**Function:** Internal IT  
**Platform:** Microsoft Active Directory Domain Services (AD DS)  
**Virtualization:** Microsoft Hyper-V  
**Domain:** `technicaltechnotech.com`  
**Last Reviewed:** Pending Verification

---

## 1. Purpose

This document describes the Active Directory Domain Services architecture supporting Technical Techno Tech's internal IT environment.

It establishes a centralized reference for:

- Active Directory forest and domain structure
- Domain controllers
- Domain Name System (DNS)
- Authentication and authorization
- Active Directory replication
- Flexible Single Master Operations (FSMO) roles
- Active Directory Sites and Services
- Organizational units
- Security groups
- Group Policy
- Administrative delegation
- Security controls
- Backup and recovery
- Infrastructure dependencies
- Configuration verification

This document supports Windows Server administration, identity management, infrastructure troubleshooting, and ITIL 4 service management practices.

---

## 2. Environment Overview

Technical Techno Tech operates a virtualized Windows Server environment with centralized identity management through Active Directory Domain Services.

The Active Directory environment supports authentication, authorization, and administration of domain-joined Windows systems.

### Infrastructure Summary

| Component | Configuration |
|---|---|
| Organization | Technical Techno Tech |
| AD Domain | `technicaltechnotech.com` |
| Forest Root Domain | `technicaltechnotech.com` |
| Forest Structure | Single-Domain Design |
| Domain Controllers | DC01 and DC02 |
| Domain Controller Type | Writable |
| Virtualization Platform | Hyper-V |
| Server Network | `10.20.10.0/24` |
| Client Network | `10.20.20.0/24` |
| Management Network | `10.20.30.0/24` |
| Router | RTR01 — VyOS |
| Firewall | FW01 — OPNsense |
| Microsoft 365 | Not Yet Deployed |

### Architecture Objectives

1. Centralize identity management.
2. Provide domain authentication.
3. Manage users, groups, and computers.
4. Support centralized security policies.
5. Provide directory replication.
6. Enable administrative delegation.
7. Support domain-joined workstations.
8. Maintain a documented and manageable infrastructure.
9. Practice enterprise Active Directory administration.
10. Support troubleshooting and recovery exercises.

---

## 3. Active Directory Forest Architecture

### 3.1 Forest Overview

An Active Directory forest is the highest-level logical structure in AD DS.

A forest provides a shared:

- Schema
- Configuration partition
- Global Catalog framework
- Trust framework
- Directory service structure

The forest acts as an administrative and security boundary for the Active Directory environment.

### 3.2 TTT Forest Design

| Attribute | Configuration |
|---|---|
| Forest Root Domain | `technicaltechnotech.com` |
| Forest Type | Single-Domain |
| Additional Domains | None Documented |
| Forest Functional Level | Pending Verification |
| Schema Master | Pending Verification |
| Domain Naming Master | Pending Verification |

### 3.3 Forest Structure

```text
Active Directory Forest
          |
          v
technicaltechnotech.com
          |
          +-- DC01
          |
          +-- DC02
```

Both domain controllers belong to the same Active Directory domain.

No additional child domains or separate domain trees are documented.

### 3.4 Forest Verification

Review forest information:

```powershell
Get-ADForest
```

Review the forest functional level:

```powershell
Get-ADForest |
Select-Object Name,RootDomain,ForestMode
```

Review forest-wide FSMO roles:

```powershell
Get-ADForest |
Select-Object SchemaMaster,DomainNamingMaster
```

### Verification Checklist

- [ ] Forest name verified
- [ ] Forest root domain verified
- [ ] Forest functional level recorded
- [ ] Schema Master identified
- [ ] Domain Naming Master identified
- [ ] Additional domains reviewed
- [ ] Forest configuration documented

---

## 4. Active Directory Domain Architecture

### 4.1 Domain Overview

An Active Directory domain provides a centralized directory for managing identities, computers, groups, and other directory objects.

The domain supports:

- Authentication
- Authorization
- Group Policy
- Directory administration
- Resource access
- Administrative delegation

### 4.2 TTT Domain Configuration

| Attribute | Configuration |
|---|---|
| Domain Name | `technicaltechnotech.com` |
| Domain Type | Active Directory Domain Services |
| Forest Root | Yes |
| Domain Functional Level | Pending Verification |
| NetBIOS Domain Name | Pending Verification |
| Domain Controllers | DC01 and DC02 |
| Domain Administrator Accounts | Pending Inventory |
| Domain Trusts | Pending Verification |

### 4.3 Domain Structure

```text
technicaltechnotech.com
          |
          +-- Domain Controllers
          |      |
          |      +-- DC01
          |      |
          |      +-- DC02
          |
          +-- Organizational Units
          |
          +-- User Accounts
          |
          +-- Computer Accounts
          |
          +-- Security Groups
          |
          +-- Group Policy Objects
```

The diagram represents the logical directory structure rather than the exact distinguished names of existing objects.

### 4.4 Domain Verification

```powershell
Get-ADDomain
```

Review the domain functional level:

```powershell
Get-ADDomain |
Select-Object DNSRoot,NetBIOSName,DomainMode
```

Review domain controllers:

```powershell
Get-ADDomainController -Filter *
```

Review domain trusts:

```powershell
Get-ADTrust -Filter *
```

### Verification Checklist

- [ ] Domain name verified
- [ ] NetBIOS name recorded
- [ ] Domain functional level recorded
- [ ] Domain controllers identified
- [ ] Domain trusts reviewed
- [ ] Domain authentication tested

---

## 5. Logical Domain Architecture

The TTT domain supports centralized administration across separate network segments.

```text
                  Hyper-V Host
                       |
                       v
                Virtual Networking
                       |
                       v
                  RTR01 - VyOS
                       |
          +------------+------------+
          |            |            |
          v            v            v
       Servers       Clients     Management
       Network       Network      Network
          |            |            |
          v            v            v
     DC01 / DC02     CLIENT01      MGMT01
          |            |            |
          +------------+------------+
                       |
                       v
             technicaltechnotech.com
                       |
                 Authentication
                 Authorization
                 Group Policy
```

### Architecture Description

- DC01 and DC02 provide directory services.
- CLIENT01 represents an employee workstation.
- MGMT01 provides an administrative management environment.
- RTR01 routes traffic between internal network segments.
- Hyper-V provides the underlying virtual infrastructure.

The actual communication paths depend on the configured routing, firewall rules, and virtual network assignments.

---

## 6. Domain Controller Architecture

### 6.1 Overview

Domain controllers store and manage Active Directory directory information.

They process authentication requests and participate in directory replication.

### 6.2 Domain Controller Inventory

| Server | IP Address | Installation Type | Role |
|---|---|---|---|
| DC01 | `10.20.10.10` | Windows Server Desktop Experience | Writable Domain Controller |
| DC02 | `10.20.10.11` | Windows Server Core | Additional Writable Domain Controller |

### 6.3 DC01

**Hostname:** DC01  
**FQDN:** `DC01.technicaltechnotech.com`  
**IP Address:** `10.20.10.10`

Documented responsibilities:

- Active Directory Domain Services
- DNS
- Domain authentication
- Directory administration
- PDC Emulator functionality, subject to current verification

### 6.4 DC02

**Hostname:** DC02  
**FQDN:** `DC02.technicaltechnotech.com`  
**IP Address:** `10.20.10.11`

Documented responsibilities:

- Active Directory Domain Services
- Additional writable domain controller
- Directory replication
- Domain authentication

DNS and Global Catalog configuration require verification.

### 6.5 Domain Controller Verification

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName,IPv4Address,Site,IsGlobalCatalog,IsReadOnly
```

### 6.6 Domain Controller Health

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

### Verification Checklist

- [ ] DC01 domain controller status verified
- [ ] DC02 domain controller status verified
- [ ] Both controllers confirmed writable
- [ ] IP addresses verified
- [ ] DNS configuration reviewed
- [ ] Global Catalog configuration reviewed
- [ ] Replication tested
- [ ] Domain controller health verified

---

## 7. DNS Architecture

### 7.1 Overview

Active Directory Domain Services depends on DNS.

DNS enables domain-joined systems to locate domain controllers and other directory services.

### 7.2 TTT DNS Configuration

| Attribute | Configuration |
|---|---|
| AD DNS Namespace | `technicaltechnotech.com` |
| DC01 | DNS Server Documented |
| DC02 | DNS Server Pending Verification |
| DNS Zone Type | Pending Verification |
| Zone Replication Scope | Pending Verification |
| DNS Forwarders | Pending Verification |
| Reverse Lookup Zones | Pending Verification |

### 7.3 DNS Dependencies

DNS supports:

- Domain controller discovery
- Kerberos authentication
- LDAP service discovery
- Active Directory replication
- Domain-joined workstation operations

### 7.4 DNS Service Records

Active Directory uses SRV records to identify available directory services.

Example:

```text
_ldap._tcp.dc._msdcs.technicaltechnotech.com
```

### 7.5 DNS Verification

```powershell
Resolve-DnsName technicaltechnotech.com
```

```powershell
Resolve-DnsName -Type SRV _ldap._tcp.dc._msdcs.technicaltechnotech.com
```

Review DNS client configuration:

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

Review DNS zones on DC01:

```powershell
Get-DnsServerZone -ComputerName DC01
```

### Verification Checklist

- [ ] DNS role verified on DC01
- [ ] DNS role status verified on DC02
- [ ] DNS zones inventoried
- [ ] Domain DNS records resolve
- [ ] SRV records resolve
- [ ] DNS client settings verified
- [ ] DNS forwarders reviewed
- [ ] DNS replication settings documented

---

## 8. Active Directory Replication

### 8.1 Overview

Active Directory uses multimaster replication to synchronize directory changes between writable domain controllers.

Replication allows domain controllers to maintain consistent directory information.

### 8.2 TTT Replication Architecture

```text
          DC01
     10.20.10.10
          |
          | AD DS Replication
          |
          v
          DC02
     10.20.10.11
```

Directory changes can originate on either writable domain controller, subject to operations requiring specific FSMO role holders.

### 8.3 Replication Responsibilities

Replication maintains consistency for:

- User accounts
- Group membership
- Computer objects
- Organizational units
- Directory attributes
- Applicable directory partitions

SYSVOL replication is a related but separate component and should be verified independently.

### 8.4 Replication Verification

Review replication health:

```powershell
repadmin /replsummary
```

Review replication connections:

```powershell
repadmin /showrepl
```

Review replication partner metadata:

```powershell
Get-ADReplicationPartnerMetadata -Target "DC01" -Scope Server
```

```powershell
Get-ADReplicationPartnerMetadata -Target "DC02" -Scope Server
```

### 8.5 Replication Dependencies

Replication requires:

- DNS
- Network connectivity
- RPC communication
- Appropriate authentication
- Healthy domain controllers
- Correct directory configuration

### Verification Checklist

- [ ] Replication partners identified
- [ ] Replication summary reviewed
- [ ] Replication failures investigated
- [ ] Directory changes verified across controllers
- [ ] SYSVOL replication status reviewed
- [ ] Replication evidence recorded

---

## 9. Flexible Single Master Operations (FSMO)

### 9.1 Overview

Active Directory uses five FSMO roles for operations requiring a designated domain controller.

### 9.2 FSMO Roles

| FSMO Role | Scope | Responsibility |
|---|---|---|
| Schema Master | Forest | Controls schema updates |
| Domain Naming Master | Forest | Controls domain additions and removals |
| RID Master | Domain | Allocates RID pools |
| PDC Emulator | Domain | Supports time synchronization and password-related operations |
| Infrastructure Master | Domain | Maintains certain cross-domain object references |

### 9.3 TTT FSMO Configuration

Previous lab documentation identified DC01 as the PDC Emulator.

The current holders of all five FSMO roles must be verified.

| FSMO Role | Current Holder |
|---|---|
| Schema Master | Pending Verification |
| Domain Naming Master | Pending Verification |
| RID Master | Pending Verification |
| PDC Emulator | DC01 — Previously Documented; Verify |
| Infrastructure Master | Pending Verification |

### 9.4 FSMO Verification

```powershell
netdom query fsmo
```

Review domain FSMO roles:

```powershell
Get-ADDomain |
Select-Object PDCEmulator,RIDMaster,InfrastructureMaster
```

Review forest FSMO roles:

```powershell
Get-ADForest |
Select-Object SchemaMaster,DomainNamingMaster
```

### 9.5 FSMO Management Considerations

- Document role holders.
- Monitor domain controller health.
- Understand service dependencies.
- Transfer roles using supported procedures.
- Avoid unnecessary FSMO changes.
- Plan recovery procedures.

FSMO role transfer and seizure are different operations and should not be treated interchangeably.

### Verification Checklist

- [ ] All five FSMO holders identified
- [ ] Role holders documented
- [ ] PDC Emulator verified
- [ ] Domain controller health checked
- [ ] Recovery procedures reviewed

---

## 10. Active Directory Sites and Services

### 10.1 Overview

Active Directory Sites and Services represents the physical network topology used by AD DS.

Sites help domain controllers and clients make appropriate decisions about:

- Domain controller selection
- Replication topology
- Replication scheduling
- Network location

### 10.2 TTT Network Segments

| Network | Subnet | Purpose |
|---|---|---|
| Servers | `10.20.10.0/24` | Domain controllers |
| Clients | `10.20.20.0/24` | Employee workstations |
| Management | `10.20.30.0/24` | Administrative systems |

### 10.3 Site Configuration

Previous Active Directory lab work included an HQ-Site configuration.

The current site names, subnet objects, and domain controller assignments for the TTT domain require verification.

### 10.4 Important Distinction

An Active Directory site is not the same as an IP subnet.

A site can contain multiple subnet objects.

Likewise, multiple IP networks do not automatically require multiple Active Directory sites.

### 10.5 Site Verification

List AD sites:

```powershell
Get-ADReplicationSite -Filter *
```

List AD subnet objects:

```powershell
Get-ADReplicationSubnet -Filter *
```

Review domain controller site assignments:

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName,Site
```

### Verification Checklist

- [ ] AD sites inventoried
- [ ] Site names verified
- [ ] Subnet objects inventoried
- [ ] Server subnet associated with appropriate site
- [ ] Client subnet association reviewed
- [ ] Management subnet association reviewed
- [ ] Domain controller site assignments verified

---

## 11. Organizational Unit Architecture

### 11.1 Overview

Organizational units provide logical containers for Active Directory objects.

OUs support:

- Administrative organization
- Delegation
- Group Policy targeting
- Object management

### 11.2 Departmental Structure

Previous Active Directory exercises included OUs such as:

- IT
- Executives
- HR
- Sales
- Groups
- Workstations

The current distinguished names and hierarchy within the TTT domain should be verified.

### 11.3 Example Logical Structure

```text
technicaltechnotech.com
          |
          +-- IT
          |
          +-- Executives
          |
          +-- HR
          |
          +-- Sales
          |
          +-- Groups
          |
          +-- Workstations
```

This diagram is an illustrative structure and does not establish that each OU exists at the domain root.

### 11.4 OU Verification

```powershell
Get-ADOrganizationalUnit -Filter * |
Select-Object Name,DistinguishedName
```

### 11.5 Design Considerations

- Organize objects according to administrative needs.
- Avoid unnecessary OU complexity.
- Apply delegation at appropriate levels.
- Consider Group Policy requirements.
- Document OU ownership and purpose.

### Related Documentation

[Organizational Units](Organizational-Units.md)

---

## 12. Security Group Architecture

### 12.1 Overview

Active Directory groups simplify access management by allowing permissions to be assigned to collections of users or computers.

### 12.2 Group Categories

**Security Groups**

Used to assign permissions to resources.

**Distribution Groups**

Used for email distribution and are not used to assign access permissions.

### 12.3 Group Scopes

| Scope | Primary Purpose |
|---|---|
| Global | Group accounts according to roles or departments |
| Domain Local | Assign permissions to resources |
| Universal | Group members across domains within a forest, subject to scope rules |

### 12.4 AGDLP Model

The AGDLP model provides a structured approach to resource access.

```text
Accounts
   |
   v
Global Groups
   |
   v
Domain Local Groups
   |
   v
Permissions
```

### 12.5 TTT Application

Previous Active Directory lab work included:

- Departmental security groups
- Distribution groups
- Group nesting
- Shared folder permissions
- Group-based access testing

The current TTT group inventory and resource assignments require verification.

### 12.6 Group Verification

```powershell
Get-ADGroup -Filter * |
Select-Object Name,GroupScope,GroupCategory
```

### Related Documentation

[Group Structure](Group-Structure.md)

---

## 13. Authentication Architecture

### 13.1 Overview

Active Directory provides centralized authentication for domain identities.

### 13.2 Primary Authentication Protocol

**Kerberos** is the primary authentication protocol used by modern Active Directory domains.

NTLM may still be used in supported scenarios, depending on configuration and application requirements.

### 13.3 Authentication Flow

```text
CLIENT01
    |
    v
DNS Lookup
    |
    v
Domain Controller Discovery
    |
    v
DC01 or DC02
    |
    v
Kerberos Authentication
    |
    v
Access to Authorized Resources
```

### 13.4 Authentication Dependencies

- DNS
- Domain controller availability
- Network connectivity
- Time synchronization
- Valid account credentials
- Appropriate permissions

### 13.5 Authentication Verification

Discover a domain controller:

```powershell
nltest /dsgetdc:technicaltechnotech.com
```

Review Kerberos tickets:

```powershell
klist
```

Review domain information:

```powershell
whoami /all
```

### Verification Checklist

- [ ] Domain controller discovery succeeds
- [ ] DNS records resolve
- [ ] Domain authentication tested
- [ ] Kerberos functionality reviewed
- [ ] Authentication-related errors investigated

---

## 14. Authorization and Access Control

### 14.1 Overview

Authentication establishes identity.

Authorization determines which resources and operations an authenticated identity is permitted to access.

### 14.2 TTT Access Control

Access control activities include:

- Security group membership
- Resource permissions
- Administrative delegation
- NTFS permissions
- Shared folder permissions
- Privileged account management

### 14.3 Least Privilege

Accounts should receive only the permissions necessary to perform their assigned responsibilities.

### 14.4 Delegated Administration

Delegation allows specific administrative responsibilities to be assigned without granting unrestricted domain administration.

Previous lab exercises included delegated password reset responsibilities.

Current TTT delegation assignments require verification.

### 14.5 Access Control Verification

Review group membership:

```powershell
Get-ADPrincipalGroupMembership -Identity "username"
```

Review directory object permissions using appropriate administrative tools.

---

## 15. Group Policy Architecture

### 15.1 Overview

Group Policy allows administrators to centrally configure supported Windows settings.

### 15.2 Group Policy Components

- Group Policy Objects
- GPO links
- Organizational units
- Security filtering
- WMI filtering
- Client-side policy processing

### 15.3 TTT Application

Potential Group Policy configurations include:

- Password and account policies
- Security settings
- Windows Firewall configuration
- Workstation restrictions
- Administrative templates
- User environment settings

Specific TTT GPOs should be documented after their configuration is verified.

### 15.4 Group Policy Verification

List GPOs:

```powershell
Get-GPO -All
```

Review linked policies:

```powershell
Get-GPInheritance -Target "DC=technicaltechnotech,DC=com"
```

Review applied policies on a workstation:

```powershell
gpresult /r
```

### Verification Checklist

- [ ] GPOs inventoried
- [ ] GPO links documented
- [ ] Security filtering reviewed
- [ ] Policy application tested
- [ ] Group Policy errors reviewed
- [ ] Supporting evidence captured

---

## 16. Time Synchronization Architecture

### 16.1 Overview

Accurate time synchronization is important for Kerberos authentication and Active Directory operations.

### 16.2 Active Directory Time Hierarchy

In a typical AD DS environment:

- The forest-root PDC Emulator is configured to use an appropriate reliable time source.
- Other domain controllers follow the domain time hierarchy.
- Domain-joined clients synchronize through the domain time hierarchy.

### 16.3 TTT Configuration

Previous lab work included troubleshooting DC01 time synchronization and configuring an external time source.

The current time source and synchronization status require verification.

### 16.4 Time Verification

```powershell
w32tm /query /status
```

```powershell
w32tm /query /source
```

```powershell
w32tm /query /configuration
```

### 16.5 Hyper-V Considerations

Hyper-V integration services can affect guest time synchronization.

Domain controller time configuration should be consistent with Active Directory's time hierarchy.

Integration settings should be reviewed carefully rather than disabled indiscriminately.

### Verification Checklist

- [ ] PDC Emulator identified
- [ ] PDC time source verified
- [ ] DC01 time synchronization checked
- [ ] DC02 time synchronization checked
- [ ] Hyper-V time settings reviewed
- [ ] Client time synchronization tested

---

## 17. Global Catalog Architecture

### 17.1 Overview

The Global Catalog contains a partial replica of objects from the forest's domains and supports forest-wide searches and certain authentication operations.

### 17.2 TTT Configuration

| Domain Controller | Global Catalog Status |
|---|---|
| DC01 | Pending Verification |
| DC02 | Pending Verification |

### 17.3 Verification

```powershell
Get-ADDomainController -Filter * |
Select-Object HostName,IsGlobalCatalog
```

### 17.4 Design Considerations

Global Catalog availability affects directory searches and certain authentication scenarios.

The appropriate configuration depends on the forest design and service requirements.

---

## 18. Active Directory Security Architecture

### 18.1 Security Objectives

- Protect domain identities.
- Restrict privileged access.
- Prevent unauthorized directory changes.
- Maintain appropriate authentication controls.
- Protect domain controllers.
- Support auditing and investigation.
- Reduce unnecessary administrative exposure.

### 18.2 Security Controls

| Control | Purpose | Status |
|---|---|---|
| Security Groups | Centralize access management | Previously Practiced; Verify |
| Administrative Delegation | Limit administrative privileges | Previously Practiced; Verify |
| Password Policies | Enforce password requirements | Pending Verification |
| Fine-Grained Password Policies | Apply targeted password requirements | Pending Verification |
| Protected Users | Add protections for eligible accounts | Pending Verification |
| Account Auditing | Record security-relevant events | Pending Verification |
| Privileged Access Review | Restrict administrative permissions | Pending Verification |
| Domain Controller Hardening | Protect directory infrastructure | Pending Review |

### 18.3 Administrative Security

Recommended practices include:

- Use separate administrative accounts.
- Apply least privilege.
- Limit Domain Admins membership.
- Review privileged groups.
- Protect domain controller access.
- Audit sensitive administrative operations.
- Document security changes.

### 18.4 Security Verification

Review privileged group membership:

```powershell
Get-ADGroupMember -Identity "Domain Admins"
```

Review default domain password policy:

```powershell
Get-ADDefaultDomainPasswordPolicy
```

Review fine-grained password policies:

```powershell
Get-ADFineGrainedPasswordPolicy -Filter *
```

---

## 19. Backup and Recovery Architecture

### 19.1 Overview

Active Directory recovery planning helps restore directory services after accidental deletion, corruption, or infrastructure failure.

### 19.2 Recovery Components

Potential recovery capabilities include:

- Windows Server Backup
- System State Backup
- Active Directory Recycle Bin
- Domain controller recovery
- FSMO role recovery
- Authoritative restoration
- Non-authoritative restoration

### 19.3 TTT Recovery Status

Previous Active Directory lab work included:

- Active Directory Recycle Bin exercises
- System State Backup
- FSMO role management

Current TTT backup configuration, backup results, and recovery readiness require verification.

### 19.4 Backup Inventory

| Server | Backup Configuration | Last Successful Backup | Restore Test |
|---|---|---|---|
| DC01 | Pending Verification | Pending | Pending |
| DC02 | Pending Verification | Pending | Pending |

### 19.5 Active Directory Recycle Bin Verification

```powershell
Get-ADOptionalFeature -Filter 'Name -eq "Recycle Bin Feature"' |
Select-Object Name,EnabledScopes
```

### 19.6 Recovery Considerations

- Document backup destinations.
- Review backup schedules.
- Protect backup storage.
- Verify successful backup completion.
- Test supported restoration procedures.
- Document recovery dependencies.
- Maintain current recovery instructions.

### Important

A successful backup does not independently demonstrate recoverability.

Restoration must be tested using supported procedures.

Hyper-V checkpoints should not be treated as replacements for Active Directory backups.

---

## 20. Infrastructure Dependencies

### 20.1 Dependency Overview

Active Directory depends on several infrastructure services.

| Service | Dependencies |
|---|---|
| Domain Authentication | DNS, domain controllers, network connectivity |
| Directory Replication | Domain controllers, DNS, RPC, networking |
| Group Policy | AD DS, DNS, SYSVOL |
| Administrative Access | Authentication, routing, management tools |
| DNS | Windows Server, networking |
| Time Synchronization | Windows Time service, configured time hierarchy |
| Recovery | Backups, storage, recovery procedures |

### 20.2 Logical Dependency Diagram

```text
                   Hyper-V
                      |
                      v
               Virtual Networking
                      |
                      v
                 RTR01 - VyOS
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
                      v
             Active Directory
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
         DNS      Authentication  Group Policy
                      |
                      v
              Domain-Joined Systems
```

---

## 21. Active Directory Health Verification

### 21.1 Verification Objectives

Confirm that the domain controllers and required directory services are operating correctly.

### 21.2 Verification Matrix

| Test ID | Component | Verification | Result |
|---|---|---|---|
| AD-TST-001 | Forest | Forest information | Pending |
| AD-TST-002 | Domain | Domain information | Pending |
| AD-TST-003 | DC01 | Domain controller health | Pending |
| AD-TST-004 | DC02 | Domain controller health | Pending |
| AD-TST-005 | Replication | Replication summary | Pending |
| AD-TST-006 | DNS | Domain resolution | Pending |
| AD-TST-007 | DNS | SRV records | Pending |
| AD-TST-008 | FSMO | Role holder inventory | Pending |
| AD-TST-009 | Sites | Site and subnet inventory | Pending |
| AD-TST-010 | Time | Time synchronization | Pending |
| AD-TST-011 | Authentication | Domain logon test | Pending |
| AD-TST-012 | Group Policy | Policy processing | Pending |

### 21.3 Recommended Verification Commands

```powershell
Get-ADForest
Get-ADDomain
Get-ADDomainController -Filter *
netdom query fsmo
dcdiag /q
repadmin /replsummary
w32tm /query /status
```

### 21.4 Evidence Requirements

Each completed test should include:

- Test identifier
- Date
- System
- Command or tool
- Expected result
- Actual result
- Pass/fail status
- Supporting evidence
- Notes

---

## 22. Troubleshooting Scenarios

The Active Directory environment supports realistic administrative and troubleshooting exercises.

| Scenario | Potential Cause | Investigation |
|---|---|---|
| User cannot sign in | Authentication or account issue | Review account status and DC availability |
| Domain controller unavailable | Server or network failure | Review server and network health |
| Replication failure | DNS, RPC, or connectivity issue | Review replication diagnostics |
| Group Policy not applying | DNS, SYSVOL, or GPO issue | Review policy processing |
| Domain controller not discovered | DNS or site configuration | Review SRV records and DC discovery |
| Account locked out | Repeated authentication failures | Review security events |
| Incorrect system time | Time service configuration | Review Windows Time |
| User cannot access shared folder | Group membership or permissions | Review access controls |
| Administrative delegation fails | Insufficient permissions | Review delegation configuration |

These scenarios are examples and do not represent completed incidents.

### Troubleshooting Workflow

1. Identify the affected service.
2. Confirm symptoms.
3. Determine affected users or systems.
4. Check network connectivity.
5. Verify DNS.
6. Review domain controller health.
7. Review event logs.
8. Identify the cause.
9. Implement an authorized corrective action.
10. Verify service restoration.
11. Document findings.

---

## 23. ITIL 4 Integration

The Active Directory environment supports multiple ITIL 4 practices.

| Practice | Example Application |
|---|---|
| Service Desk | Receives account and authentication support requests |
| Incident Management | Restores interrupted authentication services |
| Service Request Management | Handles account and access requests |
| Problem Management | Investigates recurring authentication failures |
| Change Enablement | Controls directory and domain configuration changes |
| Knowledge Management | Documents Active Directory procedures |
| Monitoring and Event Management | Detects domain controller and replication issues |
| Service Configuration Management | Tracks domain controllers and dependencies |
| Information Security Management | Manages identity and privileged access |
| Continual Improvement | Improves identity administration processes |

### Example — Domain Authentication Failure

A possible workflow:

1. CLIENT01 reports a domain authentication failure.
2. Service Desk records the incident.
3. Incident Management investigates.
4. The technician checks DNS and domain controller connectivity.
5. Active Directory health is reviewed.
6. The identified issue is corrected through an authorized action.
7. Authentication is tested.
8. The incident is resolved.
9. Relevant knowledge documentation is updated.

This example is instructional and does not represent a completed operational record.

---

## 24. Service Configuration Management

Active Directory components should be tracked through configuration item records.

### Proposed Configuration Items

| CI | Configuration Item | Type |
|---|---|---|
| CI-003 | DC01 | Windows Server |
| CI-004 | DC02 | Windows Server |
| Pending | Active Directory Domain | Directory Service |
| Pending | DNS Service | Infrastructure Service |

Existing CI identifiers must be reconciled with the configuration item register before final assignment.

### Configuration Relationships

```text
technicaltechnotech.com
          |
          +-- DC01
          |     |
          |     +-- AD DS
          |     +-- DNS
          |
          +-- DC02
                |
                +-- AD DS
                +-- DNS (Verify)
```

### Configuration Management Requirements

- Maintain accurate domain controller records.
- Document service dependencies.
- Track important configuration changes.
- Review configuration baselines.
- Record verification evidence.
- Update related infrastructure documentation.

---

## 25. Change Management

Changes to Active Directory may affect authentication, authorization, and other infrastructure services.

### Examples of Changes

- Promoting a domain controller
- Demoting a domain controller
- Transferring FSMO roles
- Modifying DNS configuration
- Changing Group Policy
- Modifying OU structure
- Updating delegated permissions
- Changing password policies
- Modifying Active Directory Sites and Services

### Proposed Change Workflow

1. Identify the required change.
2. Document the technical justification.
3. Identify affected services and systems.
4. Assess risk and impact.
5. Obtain applicable authorization.
6. Prepare implementation steps.
7. Prepare a recovery plan.
8. Implement the change.
9. Verify functionality.
10. Update configuration documentation.
11. Review the outcome.

---

## 26. Monitoring and Maintenance

### 26.1 Monitoring Objectives

Potential monitoring activities include:

- Domain controller availability
- Authentication failures
- Replication health
- DNS availability
- Time synchronization
- Security events
- Storage capacity
- Windows services

### 26.2 Monitoring Matrix

| Component | Monitoring Focus | Status |
|---|---|---|
| DC01 | Domain controller availability | Automated Monitoring Not Verified |
| DC02 | Domain controller availability | Automated Monitoring Not Verified |
| AD DS | Authentication health | Automated Monitoring Not Verified |
| Replication | Replication failures | Automated Monitoring Not Verified |
| DNS | Name resolution | Automated Monitoring Not Verified |
| Windows Time | Synchronization health | Automated Monitoring Not Verified |

### 26.3 Maintenance Activities

- Review domain controller health.
- Review replication.
- Verify DNS.
- Review privileged groups.
- Review security events.
- Verify backup status.
- Apply approved Windows updates.
- Update configuration documentation.

---

## 27. Future Development

Potential future Active Directory projects include:

### Advanced Group Policy

Implement and test additional workstation and security configurations.

### Fine-Grained Password Policies

Practice targeted password policy administration.

### Privileged Access Management

Improve administrative account security and delegation.

### Active Directory Recovery

Perform documented backup and recovery exercises.

### PowerShell Automation

Automate routine user, group, and computer administration.

### Monitoring

Implement domain controller health monitoring and alerting.

### Hybrid Identity

Evaluate future integration with Microsoft Entra ID and Azure services.

### Microsoft 365

Microsoft 365 infrastructure has not yet been deployed for Technical Techno Tech.

Cloud identity integration will be documented separately when implementation begins.

Future projects are not represented as completed implementations.

---

## 28. Skills Practiced

This project supports practical experience with:

- Active Directory Domain Services
- Windows Server administration
- Domain controller deployment
- Forest and domain architecture
- DNS administration
- Active Directory replication
- FSMO role management
- Active Directory Sites and Services
- Organizational unit management
- Security group administration
- Group Policy
- Kerberos authentication
- Administrative delegation
- Identity and access management
- PowerShell
- Domain controller troubleshooting
- Backup and recovery planning
- Configuration management
- ITIL-aligned infrastructure operations

---

## 30. What I Learned

The Technical Techno Tech Active Directory project demonstrates how centralized identity infrastructure supports business IT operations.

### Key Learning Areas

**1. Forest and Domain Architecture**

An Active Directory forest provides the overall directory structure, while domains organize identities and administrative policies.

**2. Domain Controllers**

Multiple writable domain controllers support authentication and directory replication.

**3. DNS Dependencies**

Active Directory relies on DNS for locating domain controllers and related services.

**4. Replication**

Domain controllers synchronize directory changes to maintain consistent directory information.

**5. FSMO Roles**

Certain Active Directory operations require designated FSMO role holders.

**6. Organizational Units**

OUs simplify directory administration, delegation, and Group Policy targeting.

**7. Security Groups**

Group-based access management supports centralized permission administration.

**8. Authentication and Authorization**

Authentication verifies identity, while authorization determines permitted access.

**9. Infrastructure Dependencies**

Active Directory relies on Windows Server, networking, DNS, time synchronization, and virtualization.

**10. Operational Documentation**

Accurate architecture documentation supports troubleshooting, maintenance, change management, and recovery planning.

---

## 31. Verification Checklist

### Forest and Domain

- [ ] Forest name verified
- [ ] Domain name verified
- [ ] Functional levels documented
- [ ] NetBIOS name verified
- [ ] Domain trusts reviewed

### Domain Controllers

- [ ] DC01 configuration verified
- [ ] DC02 configuration verified
- [ ] Both controllers confirmed writable
- [ ] Global Catalog configuration verified
- [ ] FSMO roles documented

### DNS and Replication

- [ ] DNS zones reviewed
- [ ] SRV records verified
- [ ] DNS client settings reviewed
- [ ] Replication health verified
- [ ] SYSVOL replication reviewed

### Sites and Directory Structure

- [ ] AD sites inventoried
- [ ] Subnet objects documented
- [ ] OU structure verified
- [ ] Security groups inventoried
- [ ] Administrative delegation reviewed

### Security and Recovery

- [ ] Password policies reviewed
- [ ] Privileged groups reviewed
- [ ] Security auditing reviewed
- [ ] Backup configuration verified
- [ ] Recovery testing status documented
- [ ] Time synchronization verified

### Documentation

- [ ] Command output captured
- [ ] Screenshots sanitized
- [ ] CI relationships reviewed
- [ ] Dependencies documented
- [ ] Unverified information identified
- [ ] Revision history updated

---

## 32. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT Active Directory architecture documentation covering forest, domain, domain controllers, DNS, replication, FSMO roles, security, and infrastructure dependencies |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This document describes the Active Directory architecture associated with the TTT infrastructure.

Previously documented configurations are included for continuity. Details that have not been confirmed through current system inspection are identified as pending verification.

Example commands, proposed procedures, future improvements, and illustrative scenarios do not represent completed activities.

All technical evidence should originate from actual authorized lab work and be sanitized before publication.
