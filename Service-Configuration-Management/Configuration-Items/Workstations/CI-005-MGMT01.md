# CI-005 — MGMT01 Management Workstation

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-005 |
| **CI Name** | MGMT01 |
| **Organization** | Technical Techno Tech |
| **CI Type** | Workstation — Administrative |
| **CI Category** | Compute / Endpoint |
| **Environment** | Simulated Enterprise — Hyper-V |
| **Status** | Active — Previously Documented; Current State Pending Verification |
| **Owner** | Internal IT |
| **Managed By** | Systems Administrator |
| **Date Created** | Not Recorded |
| **Last Updated** | 2026-10-14 |
| **Last Verified** | Not Yet Verified for This Record |
| **Related IT Service** | IT-SVC-001 — Identity & Access Management; IT-SVC-002 — Endpoint Management; IT-SVC-005 — Server & Infrastructure Services |

---

## 1. Configuration Item Overview

### Description

MGMT01 is a Windows 11 virtual workstation used for centralized administration of Technical Techno Tech's IT infrastructure.

It is connected to the management network and provides an administrative environment for managing Windows Server, Active Directory Domain Services, and other infrastructure components.

MGMT01 has previously been used for Active Directory administration and remote management exercises.

### Business Purpose

MGMT01 provides IT administrators with a dedicated workstation for performing administrative tasks.

Its primary purposes include:

- Managing Active Directory users, groups, and organizational units
- Administering Windows Server infrastructure
- Managing Group Policy
- Performing PowerShell administration
- Accessing remote management tools
- Troubleshooting infrastructure issues
- Supporting controlled administrative workflows

Separating administrative activities from standard employee workstations can support stronger access control and operational security.

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Provides administrative access to directory services |
| IT-SVC-002 | Endpoint Management | Supports workstation administration and troubleshooting |
| IT-SVC-005 | Server & Infrastructure Services | Provides remote server administration |
| IT-SVC-006 | Information Security | Supports controlled privileged administration |
| IT-SVC-007 | Employee IT Lifecycle | Supports employee account administration |

**Reference:** [IT Service Catalog](../../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** Workstation — Administrative
- **CI Category:** Compute / Endpoint
- **Criticality:** Medium — Proposed Classification
- **Lifecycle Status:** Active — Pending Current-State Verification

### Ownership

| Responsibility | Assigned Role |
|---|---|
| **Service Owner** | Internal IT |
| **Technical Owner** | Systems Administrator |
| **Primary Administrator** | Systems Administrator |
| **Support Team** | Internal IT |

These responsibilities are simulated for the TTT environment.

### Business Criticality

MGMT01 provides administrative access to infrastructure systems.

Its failure could affect:

- Active Directory administration
- Group Policy management
- Remote server administration
- Administrative troubleshooting
- Infrastructure maintenance
- IT support workflows

Core infrastructure services may continue operating even if MGMT01 becomes unavailable.

Alternative management methods may be available through other authorized systems.

---

## 3. Technical Specifications

### General Information

| Attribute | Value |
|---|---|
| **Hostname / Device Name** | MGMT01 |
| **Operating System / Platform** | Windows 11 |
| **Version / Build** | Pending Verification |
| **Manufacturer / Vendor** | Microsoft |
| **Model / Instance Type** | Hyper-V Virtual Machine |
| **Asset Identifier** | CI-005 |
| **Location** | TTT Hyper-V Lab |
| **Domain / Tenant** | `technicaltechnotech.com` — Expected; Verify |

### Hardware / Virtual Resources

| Resource | Configuration |
|---|---|
| **CPU / vCPU** | Pending Verification |
| **Memory** | Pending Verification |
| **Storage** | Pending Verification |
| **Network Adapters** | Pending Verification |
| **Virtualization Platform** | Microsoft Hyper-V |
| **VM Generation** | Pending Verification |

### Network Configuration

| Attribute | Value |
|---|---|
| **IP Address** | `10.20.30.10` |
| **Subnet Mask / Prefix** | `255.255.255.0` / `/24` |
| **Default Gateway** | `10.20.30.1` |
| **DNS Servers** | Pending Verification |
| **VLAN / Network Segment** | Management — `10.20.30.0/24` |
| **FQDN** | `MGMT01.technicaltechnotech.com` — Expected; Verify |

### Configuration Verification

Run on MGMT01:

```powershell
hostname
```

```powershell
Get-ComputerInfo |
Select-Object CsName,WindowsProductName,WindowsVersion,OsBuildNumber
```

```powershell
Get-NetIPConfiguration
```

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

Verify domain membership:

```powershell
Get-CimInstance Win32_ComputerSystem |
Select-Object Name,Domain,PartOfDomain
```

Run on the Hyper-V host:

```powershell
Get-VM -Name "MGMT01" |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

**Verification Status:** Not Yet Executed for This Record

---

## 4. Installed Roles, Services & Software

### Administrative Tools

| Tool | Purpose | Configuration Status |
|---|---|---|
| Active Directory Users and Computers | Manage AD users, groups, and OUs | Previously Used |
| Active Directory Administrative Center | Advanced AD administration | Previously Used |
| Group Policy Management Console | Manage Group Policy | Previously Practiced |
| PowerShell | Command-line administration | Available — Verify Version |
| Remote Server Administration Tools | Remote Windows Server administration | Previously Used |
| Remote Desktop Connection | Remote access to authorized systems | Available — Verify Configuration |
| Windows Admin Center | Browser-based server administration | Previously Used; Current Access Pending Verification |

### Installed Applications

| Application | Version | Purpose |
|---|---|---|
| Windows 11 | Pending Verification | Workstation operating system |
| RSAT | Pending Verification | Remote server administration |
| PowerShell | Pending Verification | Administrative scripting |
| Additional Applications | Pending Inventory | Other administrative functionality |

### Running Services

| Service | Purpose | Expected State |
|---|---|---|
| DNS Client | Name resolution | Operational |
| Group Policy Client | Applies applicable Group Policy settings | Operational |
| Windows Defender Firewall | Host-based network protection | Enabled |
| Windows Event Log | System and security event logging | Running |
| Windows Remote Management | Remote administration, if configured | As Required |

Expected states do not represent verified results.

### Verification Commands

Review installed RSAT capabilities:

```powershell
Get-WindowsCapability -Online |
Where-Object Name -like 'Rsat*' |
Select-Object Name,State
```

Review administrative tools:

```powershell
Get-Command Get-ADUser,Get-GPO -ErrorAction SilentlyContinue
```

Review relevant services:

```powershell
Get-Service Dnscache,gpsvc,EventLog,WinRM
```

---

## 5. Configuration Baseline

### Approved Configuration

The intended MGMT01 configuration includes:

- Windows 11
- Membership in `technicaltechnotech.com`
- Management network connectivity
- Appropriate DNS configuration
- Authorized administrative tools
- Restricted privileged access
- Windows Firewall enabled
- Appropriate security policies
- Current supported Windows updates
- Access to approved infrastructure management interfaces

This is the proposed configuration baseline. Formal approval has not been recorded.

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| Hostname | MGMT01 | Previously Documented | Pending Verification |
| Domain | `technicaltechnotech.com` | Previously Documented | Pending Verification |
| IPv4 Address | `10.20.30.10` | Previously Documented | Pending Verification |
| Subnet | `10.20.30.0/24` | Previously Documented | Pending Verification |
| Gateway | `10.20.30.1` | Previously Documented | Pending Verification |
| DNS Configuration | Resolves domain services | Unknown | Pending Verification |
| RSAT | Required tools installed | Previously Used | Pending Verification |
| PowerShell | Available | Previously Used | Pending Verification |
| Windows Firewall | Enabled | Unknown | Pending Verification |
| Security Updates | Supported and current | Unknown | Pending Verification |
| Administrative Access | Restricted | Unknown | Pending Verification |

### Configuration Policies

Potentially applicable policies include:

- Workstation security Group Policy
- Windows Firewall policy
- User Rights Assignment
- Local administrator restrictions
- Remote management restrictions
- Windows Update policy
- Security auditing
- Screen lock and session controls

Actual applied policies require verification.

### Configuration Verification

**Last Verified:** Not Yet Verified

**Verification Method:** PowerShell, Windows Administrative Tools, Group Policy Results

**Verification Result:** Not Assessed

**Notes:**

Previous lab work included Active Directory administration from a management workstation.

The current installed tools, network settings, permissions, and applied policies must be verified.

---

## 6. Relationships & Dependencies

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| CI-001 — DC01 | Connects To | Domain controller and DNS services |
| CI-002 — DC02 | Connects To | Additional domain controller |
| CI-003 — FW01 | Uses Connectivity Through | External network connectivity |
| CI-004 — RTR01 | Uses As Gateway | Management network routing |
| CI-007 — Hyper-V Host | Hosted On | Virtualization infrastructure |
| CI-008 — Active Directory Domain | Member Of | Domain membership and authentication |
| CI-009 — Virtual Networks | Connected To | Management network |

### Upstream Dependencies

MGMT01 depends on:

- Hyper-V host availability
- Virtual machine storage
- Management virtual network
- Windows 11 operating system
- Correct IP configuration
- DNS services
- Domain authentication, for domain-based administration
- Appropriate administrative permissions

### Downstream Dependencies

MGMT01 is an administrative endpoint rather than a primary infrastructure service.

Administrative workflows that may depend on MGMT01 include:

- User and group management
- Group Policy administration
- Windows Server management
- Remote troubleshooting
- Configuration verification
- Infrastructure maintenance

### Dependency Diagram

```text
                     Hyper-V Host
                          |
                          v
                    MGMT01 (Win11)
                     10.20.30.10
                          |
                  Management Network
                    10.20.30.0/24
                          |
                          v
                    RTR01 (VyOS)
                          |
              +-----------+-----------+
              |                       |
              v                       v
         Server Network          External Access
              |                       |
         +----+----+                  v
         |         |              FW01
         v         v
        DC01      DC02
```

**Reference:** [Network Topology](../../../../Infrastructure/Networking/Network-Topology.md)

### Impact of CI Failure

If MGMT01 becomes unavailable:

- Administrators may lose access to their primary management workstation.
- Remote administration workflows may be interrupted.
- Some troubleshooting activities may be delayed.
- Administrative tools installed only on MGMT01 may become temporarily unavailable.

Active Directory and other infrastructure services may continue operating independently.

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Workstation Sign-In | Authorized IT Personnel | Interactive Access |
| Administrative Access | Authorized Administrators | Privileged Access |
| Remote Management | Authorized IT Administrators | As Required |
| Standard Employee Access | Not Intended | Restricted |

Actual access permissions require verification.

### Security Controls

Recommended controls include:

- Dedicated administrative accounts
- Least-privilege access
- Windows Defender Firewall
- Microsoft Defender Antivirus
- Windows security updates
- Screen locking
- Account lockout controls
- Security event auditing
- Restricted remote administration
- Protection of administrative credentials

### Privileged Access Considerations

MGMT01 is intended for administrative tasks.

Recommended practices include:

- Avoiding routine web browsing with privileged accounts
- Separating standard and administrative credentials
- Restricting local administrator membership
- Limiting access to sensitive management interfaces
- Reviewing privileged account usage
- Avoiding unnecessary software installation

### Security Review

**Last Security Review:** Not Recorded

**Security Status:** Not Assessed

### Security Notes

Compromise of MGMT01 could expose administrative access to other infrastructure components.

Its security posture should therefore receive greater attention than that of a standard employee workstation.

---

## 8. Monitoring & Maintenance

### Monitoring Configuration

| Monitoring Item | Tool / Method | Expected Condition |
|---|---|---|
| Workstation Availability | Hyper-V / Connectivity Testing | Operational when required |
| CPU / Memory | Task Manager / PowerShell | Sufficient resources |
| Storage | PowerShell | Adequate available capacity |
| Windows Updates | Windows Update | Supported and current |
| Windows Firewall | PowerShell | Enabled |
| Antivirus | Windows Security / PowerShell | Active |
| Event Logs | Event Viewer | No unresolved critical errors |
| Domain Connectivity | PowerShell / Network Diagnostics | Domain services reachable |
| Administrative Tools | Manual Verification | Required tools operational |

No automated monitoring deployment is confirmed.

### Maintenance Activities

- Review Windows updates.
- Verify administrative tools.
- Review security configuration.
- Check domain connectivity.
- Review event logs.
- Verify available storage.
- Review local administrator membership.
- Verify remote management access.
- Update documentation after approved changes.

### Maintenance Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Systems Administrator

**Last Maintenance:** Not Recorded

**Next Planned Maintenance:** Not Scheduled

### Diagnostic Commands

Verify domain controller discovery:

```powershell
nltest /dsgetdc:technicaltechnotech.com
```

Verify DNS resolution:

```powershell
Resolve-DnsName technicaltechnotech.com
```

Verify connectivity to DC01:

```powershell
Test-NetConnection 10.20.10.10 -Port 389
```

Verify connectivity to DC02:

```powershell
Test-NetConnection 10.20.10.11 -Port 389
```

Review applied Group Policy:

```powershell
gpresult /r
```

Review firewall profiles:

```powershell
Get-NetFirewallProfile |
Select-Object Name,Enabled
```

Review antivirus status:

```powershell
Get-MpComputerStatus |
Select-Object AMServiceEnabled,AntivirusEnabled,RealTimeProtectionEnabled
```

**Execution Status:** Commands Provided — Results Not Yet Recorded

---

## 9. Backup & Recovery

### Backup Configuration

**Backup Required:** To Be Determined Based on Stored Data and Recovery Requirements

**Backup Method:** Pending Definition

**Backup Frequency:** Not Yet Established

**Backup Destination:** Pending Verification

**Last Successful Backup:** Not Recorded

### Recovery Information

**Recovery Procedure:** Pending Documentation

**Recovery Dependencies:**

- Hyper-V infrastructure
- Windows 11 installation media or approved VM image
- Management network connectivity
- Active Directory
- Administrative tools
- Authorized administrator credentials

**Recovery Testing:** Not Recorded

### Recovery Considerations

A recovery procedure should account for:

1. Restoring or redeploying the Windows 11 virtual machine.
2. Configuring its virtual network adapter.
3. Verifying IP and DNS configuration.
4. Joining the workstation to the domain, if necessary.
5. Installing required administrative tools.
6. Applying approved security policies.
7. Verifying domain authentication.
8. Testing remote administration.
9. Updating the CI record.

Any locally stored administrative scripts or documentation should be backed up or maintained in an appropriate version-controlled repository.

---

## 10. Configuration History

Track significant configuration changes affecting MGMT01.

| Date | Change ID | Description | Result |
|---|---|---|---|
| Not Recorded | N/A | Initial Windows 11 deployment | Previously Documented |
| Not Recorded | N/A | Domain membership configuration | Previously Documented |
| Not Recorded | N/A | Installation and use of administrative tools | Previously Practiced |
| Not Recorded | N/A | Active Directory administration exercises | Previously Practiced |

### Current Configuration Summary

MGMT01 is documented as a Windows 11 administrative workstation connected to the management network.

Its last documented address is `10.20.30.10`, with an expected default gateway of `10.20.30.1`.

The current operating system build, installed tools, security settings, and network configuration require verification.

Detailed change implementation evidence should remain in associated Change Enablement records.

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

- [Network Topology](../../../../Infrastructure/Networking/Network-Topology.md)
- [Domain Architecture](../../../../Infrastructure/Active-Directory/Domain-Architecture.md)
- [Organizational Units](../../../../Infrastructure/Active-Directory/Organizational-Units.md)
- [Group Structure](../../../../Infrastructure/Active-Directory/Group-Structure.md)
- [Windows Server Overview](../../../../Infrastructure/Windows-Server/README.md)
- [Hyper-V Infrastructure](../../../../Infrastructure/Virtualization/Hyper-V/README.md)

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Hostname | MGMT01 | Not Yet Collected | Pending |
| Operating System | Windows 11 | Not Yet Collected | Pending |
| Domain Membership | `technicaltechnotech.com` | Not Yet Collected | Pending |
| IPv4 Address | `10.20.30.10` | Not Yet Collected | Pending |
| Default Gateway | `10.20.30.1` | Not Yet Collected | Pending |
| DNS Configuration | Domain services resolve | Not Yet Collected | Pending |
| DC01 Connectivity | Required services reachable | Not Yet Collected | Pending |
| DC02 Connectivity | Required services reachable | Not Yet Collected | Pending |
| RSAT | Required tools installed | Not Yet Collected | Pending |
| PowerShell | Available | Not Yet Collected | Pending |
| Group Policy | Applicable policies processed | Not Yet Collected | Pending |
| Windows Firewall | Enabled | Not Yet Collected | Pending |
| Antivirus | Active | Not Yet Collected | Pending |
| Administrative Access | Restricted appropriately | Not Yet Collected | Pending |

### Supporting Evidence

No evidence files have been attached to this record.

Recommended evidence:

- Windows system information
- Network configuration
- Domain membership
- Installed RSAT capabilities
- Administrative tool availability
- Group Policy results
- Windows Firewall status
- Antivirus status
- Connectivity test results
- Hyper-V virtual machine configuration

Only verified, sanitized evidence should be added to the repository.

Do not publish administrative credentials, access tokens, private keys, or other sensitive information.

### Verification Summary

**Verification Status:** Not Yet Completed

MGMT01's documented configuration must be compared against the live Windows 11 environment.

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

Before retiring MGMT01:

1. Identify administrative workflows that depend on the workstation.
2. Identify replacement management capabilities.
3. Back up necessary scripts and documentation.
4. Review stored credentials and sensitive data.
5. Revoke unnecessary access.
6. Remove or disable the computer account as appropriate.
7. Securely remove the virtual machine and its data.
8. Update related CI records.
9. Verify that required administration remains available.

### Lifecycle Notes

No retirement activity is currently documented.

---

## 14. Lessons Learned

### What I Learned

**1. Centralized Administration**

A management workstation provides a dedicated environment for administering multiple infrastructure components.

**2. Remote Server Administration**

RSAT and other administrative tools allow administrators to manage Windows Server and Active Directory without signing in directly to each server.

**3. Network Segmentation**

Placing management workstations on a separate network creates opportunities to restrict and monitor administrative traffic.

**4. Privileged Access Security**

Administrative workstations require appropriate security controls because they can access sensitive infrastructure.

**5. Configuration Baselines**

A workstation baseline defines expected operating system settings, network configuration, administrative tools, and security controls.

**6. Service Configuration Management**

Documenting MGMT01 as a CI helps track dependencies, changes, security reviews, and operational history.

### Skills Practiced

- ITIL 4 Service Configuration Management
- Windows 11 Administration
- Active Directory Administration
- Remote Server Administration Tools
- Group Policy Management
- PowerShell
- Remote Administration
- Endpoint Security
- Network Troubleshooting
- Configuration Baseline Design
- Technical Documentation

### Improvement Opportunities

- Verify the Windows 11 build.
- Record actual virtual machine resources.
- Verify domain membership.
- Inventory installed administrative tools.
- Review local administrator membership.
- Verify Group Policy application.
- Review firewall and antivirus settings.
- Establish a workstation recovery procedure.
- Document administrative access restrictions.
- Link future Jira records to CI-005.

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

CI-005 has been documented using the Technical Techno Tech Configuration Item Template.

The record identifies MGMT01's administrative purpose, technical specifications, supported services, dependencies, security requirements, and intended configuration baseline.

Outstanding activities include:

- Verify operating system and virtual resources.
- Confirm network and domain configuration.
- Inventory administrative tools.
- Review privileged access.
- Verify security controls.
- Document recovery procedures.
- Collect technical evidence.
- Complete the formal CI review.

**Overall Record Status:** Draft — Awaiting Configuration Verification

---

## 16. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial MGMT01 configuration item record aligned with the TTT CI template |

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations and infrastructure relationships are based on previously documented lab activities. Current verification results are not assumed.

Business ownership, administrative responsibilities, and operational processes are simulated for educational and portfolio purposes.
