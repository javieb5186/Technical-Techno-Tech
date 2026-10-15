# CI-006 — CLIENT01 Employee Workstation

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-006 |
| **CI Name** | CLIENT01 |
| **Organization** | Technical Techno Tech |
| **CI Type** | Workstation — Employee Endpoint |
| **CI Category** | Compute / Endpoint |
| **Environment** | Simulated Enterprise — Hyper-V |
| **Status** | Active — Previously Documented; Current State Pending Verification |
| **Owner** | Internal IT |
| **Managed By** | Endpoint Administrator |
| **Date Created** | Not Recorded |
| **Last Updated** | 2026-10-14 |
| **Last Verified** | Not Yet Verified for This Record |
| **Related IT Service** | IT-SVC-002 — Endpoint Management |

---

## 1. Configuration Item Overview

### Description

CLIENT01 is a Windows 11 virtual workstation representing a standard employee computer within Technical Techno Tech.

It is connected to the client network and is intended to operate as a domain-joined workstation within `technicaltechnotech.com`.

CLIENT01 serves as a testing environment for Windows endpoint administration, Active Directory authentication, Group Policy, security configuration, and IT support troubleshooting.

### Business Purpose

CLIENT01 represents an employee endpoint used to access organizational IT services.

Its primary purposes include:

- Providing a workstation for a simulated employee
- Supporting domain authentication
- Testing Group Policy application
- Validating user and computer permissions
- Testing Windows security settings
- Practicing remote troubleshooting
- Simulating service desk incidents and requests
- Supporting endpoint management exercises

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Uses domain authentication and access controls |
| IT-SVC-002 | Endpoint Management | Represents a managed Windows workstation |
| IT-SVC-004 | Network Connectivity | Uses internal routing and network services |
| IT-SVC-006 | Information Security | Receives applicable endpoint security controls |
| IT-SVC-007 | Employee IT Lifecycle | Represents an employee-assigned endpoint |

**Reference:** [IT Service Catalog](../../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** Workstation — Employee Endpoint
- **CI Category:** Compute / Endpoint
- **Criticality:** Medium — Proposed Classification
- **Lifecycle Status:** Active — Pending Current-State Verification

### Ownership

| Responsibility | Assigned Role |
|---|---|
| **Service Owner** | Internal IT |
| **Technical Owner** | Endpoint Administrator |
| **Primary Administrator** | Endpoint Administrator |
| **Support Team** | Service Desk / Internal IT |

These responsibilities are simulated for the TTT environment.

### Business Criticality

CLIENT01 represents a standard employee workstation.

Its failure could affect:

- The assigned employee's productivity
- Access to business applications
- Domain authentication
- Network resource access
- Local application availability
- Completion of assigned work

Unlike a domain controller or router, CLIENT01 is not expected to provide shared infrastructure services.

Its failure would primarily affect its assigned user and any lab activities dependent on the workstation.

---

## 3. Technical Specifications

### General Information

| Attribute | Value |
|---|---|
| **Hostname / Device Name** | CLIENT01 |
| **Operating System / Platform** | Windows 11 |
| **Version / Build** | Pending Verification |
| **Manufacturer / Vendor** | Microsoft |
| **Model / Instance Type** | Hyper-V Virtual Machine |
| **Asset Identifier** | CI-006 |
| **Location** | TTT Hyper-V Lab |
| **Domain / Tenant** | `technicaltechnotech.com` — Expected; Verify |
| **Assigned User** | Simulated Employee — Not Yet Assigned |

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
| **IP Address** | `10.20.20.10` |
| **Subnet Mask / Prefix** | `255.255.255.0` / `/24` |
| **Default Gateway** | `10.20.20.1` |
| **DNS Servers** | Pending Verification |
| **VLAN / Network Segment** | Clients — `10.20.20.0/24` |
| **FQDN** | `CLIENT01.technicaltechnotech.com` — Expected; Verify |
| **IP Assignment Method** | Pending Verification |

### Configuration Verification

Run on CLIENT01:

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
Get-VM -Name "CLIENT01" |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

**Verification Status:** Not Yet Executed for This Record

---

## 4. Installed Roles, Services & Software

### Endpoint Features

| Feature | Purpose | Configuration Status |
|---|---|---|
| Windows 11 | Employee workstation operating system | Previously Documented |
| Domain Membership | Centralized authentication | Previously Documented; Verify |
| Group Policy Client | Applies applicable domain policies | Expected |
| Windows Defender Firewall | Host-based network protection | Pending Verification |
| Microsoft Defender Antivirus | Endpoint malware protection | Pending Verification |
| Remote Desktop | Remote access, if enabled | Pending Verification |
| Quick Assist | Remote support, if available | Pending Verification |

### Installed Applications

| Application | Version | Purpose |
|---|---|---|
| Windows 11 | Pending Verification | Workstation operating system |
| Microsoft Edge | Pending Verification | Web browsing |
| Additional Applications | Pending Inventory | Employee productivity and support |

Microsoft 365 applications and Intune enrollment are not assumed to be deployed.

### Running Services

| Service | Purpose | Expected State |
|---|---|---|
| DNS Client | Name resolution | Operational |
| Group Policy Client | Applies applicable policies | Operational |
| Windows Event Log | Event logging | Running |
| Windows Defender Firewall | Host-based firewall protection | Enabled |
| Windows Update | Operating system updates | Available |
| Windows Remote Management | Remote management, if configured | As Required |

### Verification Commands

Review installed applications:

```powershell
Get-Package |
Select-Object Name,Version,ProviderName
```

Review selected services:

```powershell
Get-Service Dnscache,gpsvc,EventLog,WinRM
```

Review Windows features:

```powershell
Get-WindowsOptionalFeature -Online |
Where-Object State -eq Enabled
```

**Execution Status:** Not Yet Recorded

---

## 5. Configuration Baseline

### Approved Configuration

The intended CLIENT01 configuration includes:

- Windows 11
- Membership in `technicaltechnotech.com`
- Connectivity to the client network
- Correct DNS and default gateway configuration
- Applicable domain Group Policy
- Windows Defender Firewall enabled
- Endpoint antivirus protection
- Supported Windows updates
- Restricted local administrator privileges
- Standard employee access
- Approved applications only

This is a proposed configuration baseline. Formal approval has not been recorded.

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| Hostname | CLIENT01 | Previously Documented | Pending Verification |
| Operating System | Windows 11 | Previously Documented | Pending Verification |
| Domain | `technicaltechnotech.com` | Previously Documented | Pending Verification |
| IPv4 Address | `10.20.20.10` | Previously Documented | Pending Verification |
| Subnet | `10.20.20.0/24` | Previously Documented | Pending Verification |
| Default Gateway | `10.20.20.1` | Previously Documented | Pending Verification |
| DNS Configuration | Domain DNS resolution operational | Unknown | Pending Verification |
| Group Policy | Applicable policies processed | Previously Practiced | Pending Verification |
| Windows Firewall | Enabled | Unknown | Pending Verification |
| Antivirus | Active | Unknown | Pending Verification |
| Windows Updates | Supported and current | Unknown | Pending Verification |
| Local Administrator Access | Restricted | Unknown | Pending Verification |
| Remote Support | Authorized access only | Unknown | Pending Verification |

### Configuration Policies

Potentially applicable policies include:

- Password and account policies
- Windows Firewall policy
- User Rights Assignment
- Local administrator restrictions
- Screen lock and session controls
- Security auditing
- Windows Update policy
- Remote Desktop restrictions
- Software installation restrictions

Actual applied policies require verification.

### Configuration Verification

**Last Verified:** Not Yet Verified

**Verification Method:** PowerShell, Group Policy Results, Windows Administrative Tools

**Verification Result:** Not Assessed

**Notes:**

Previous TTT lab activities included Group Policy and workstation security testing.

The current applied policies and security settings must be verified before recording compliance.

---

## 6. Relationships & Dependencies

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| CI-001 — DC01 | Uses Services From | Domain authentication and DNS |
| CI-002 — DC02 | Uses Services From | Additional domain controller services |
| CI-003 — FW01 | Uses Connectivity Through | External network access |
| CI-004 — RTR01 | Uses As Gateway | Client network routing |
| CI-005 — MGMT01 | Managed From | Administrative workstation |
| CI-007 — Hyper-V Host | Hosted On | Virtualization infrastructure |
| CI-008 — Active Directory Domain | Member Of | Domain membership and authentication |
| CI-009 — Virtual Networks | Connected To | Client network |

### Upstream Dependencies

CLIENT01 depends on:

- Hyper-V host availability
- Virtual machine storage
- Client virtual network
- Windows 11 operating system
- Correct network configuration
- DNS services
- Domain controllers for domain-based authentication
- RTR01 for off-subnet communication
- FW01 for external connectivity

### Downstream Dependencies

CLIENT01 is an endpoint rather than a shared infrastructure service.

Its primary downstream dependencies are:

- Assigned employee workflows
- Endpoint administration exercises
- Group Policy testing
- IT support simulations
- Remote troubleshooting scenarios

### Dependency Diagram

```text
                    Hyper-V Host
                         |
                         v
                  CLIENT01 (Win11)
                    10.20.20.10
                         |
                   Client Network
                   10.20.20.0/24
                         |
                         v
                   RTR01 (VyOS)
                         |
              +----------+----------+
              |                     |
              v                     v
        Server Network        External Access
              |                     |
         +----+----+                v
         |         |               FW01
         v         v
        DC01      DC02
```

**Reference:** [Network Topology](../../../../Infrastructure/Networking/Network-Topology.md)

### Impact of CI Failure

If CLIENT01 becomes unavailable:

- Its assigned employee may be unable to perform work.
- Local applications may become unavailable.
- The user may lose access to organizational resources from this device.
- Endpoint troubleshooting exercises may be interrupted.

Shared infrastructure services should generally remain operational.

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Employee Sign-In | Assigned Domain User | Standard User |
| Local Administration | Authorized IT Administrators | Administrative |
| Remote Support | Authorized Support Personnel | As Required |
| Domain Administration | Not Intended for Routine Employee Use | Restricted |

Actual accounts and permissions require verification.

### Security Controls

Recommended controls include:

- Standard user permissions
- Restricted local administrator membership
- Windows Defender Firewall
- Microsoft Defender Antivirus
- Windows security updates
- Group Policy security settings
- Screen locking
- Account lockout controls
- Security event auditing
- Restricted remote access
- Approved software installation

### Endpoint Security Review

| Security Control | Expected Configuration | Status |
|---|---|---|
| Windows Firewall | Enabled | Pending Verification |
| Antivirus | Active | Pending Verification |
| Local Administrators | Authorized accounts only | Pending Verification |
| Windows Updates | Supported and current | Pending Verification |
| Group Policy | Applicable policies processed | Pending Verification |
| Remote Desktop | Disabled unless required and authorized | Pending Verification |
| Screen Lock | Configured according to policy | Pending Verification |
| Security Auditing | Applicable events recorded | Pending Verification |

### Security Review

**Last Security Review:** Not Recorded

**Security Status:** Not Assessed

### Security Notes

CLIENT01 represents a standard employee endpoint.

Employees should normally operate without administrative privileges.

Administrative access should be granted only when necessary and authorized.

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
| Group Policy | `gpresult` | Applicable policies processed |
| Network Connectivity | Ping / DNS / TCP Tests | Required services reachable |

No automated monitoring deployment is confirmed.

### Maintenance Activities

- Review Windows updates.
- Verify domain connectivity.
- Review antivirus status.
- Review firewall configuration.
- Check available storage.
- Review event logs.
- Verify Group Policy application.
- Review installed applications.
- Review local administrator membership.
- Test approved remote support methods.

### Maintenance Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Endpoint Administrator

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

Test connectivity to DC01:

```powershell
Test-NetConnection 10.20.10.10 -Port 389
```

Test connectivity to DC02:

```powershell
Test-NetConnection 10.20.10.11 -Port 389
```

Review applied Group Policy:

```powershell
gpresult /r
```

Review Windows Firewall:

```powershell
Get-NetFirewallProfile |
Select-Object Name,Enabled
```

Review antivirus:

```powershell
Get-MpComputerStatus |
Select-Object AMServiceEnabled,AntivirusEnabled,RealTimeProtectionEnabled
```

Review local administrators:

```powershell
Get-LocalGroupMember -Group "Administrators"
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
- Client network connectivity
- Active Directory
- Approved applications
- Authorized administrator credentials

**Recovery Testing:** Not Recorded

### Recovery Considerations

A recovery procedure should account for:

1. Restoring or redeploying the Windows 11 virtual machine.
2. Configuring the client virtual network adapter.
3. Verifying IP and DNS configuration.
4. Joining the workstation to the domain, if necessary.
5. Installing approved applications.
6. Applying applicable Group Policy.
7. Verifying user authentication.
8. Testing access to required network resources.
9. Verifying endpoint security.
10. Updating the CI record.

User data should be backed up or stored in approved locations according to organizational requirements.

---

## 10. Configuration History

Track significant configuration changes affecting CLIENT01.

| Date | Change ID | Description | Result |
|---|---|---|---|
| Not Recorded | N/A | Initial Windows 11 deployment | Previously Documented |
| Not Recorded | N/A | Domain membership configuration | Previously Documented |
| Not Recorded | N/A | Group Policy testing | Previously Practiced |
| Not Recorded | N/A | Endpoint security configuration exercises | Previously Practiced |

### Current Configuration Summary

CLIENT01 is documented as a Windows 11 employee workstation connected to the client network.

Its last documented address is `10.20.20.10`, with an expected default gateway of `10.20.20.1`.

The current operating system build, domain membership, installed applications, security settings, and applied policies require verification.

Detailed implementation steps should remain in associated Change Enablement records.

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
- [MGMT01 Configuration Item](CI-005-MGMT01.md)

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Hostname | CLIENT01 | Not Yet Collected | Pending |
| Operating System | Windows 11 | Not Yet Collected | Pending |
| Domain Membership | `technicaltechnotech.com` | Not Yet Collected | Pending |
| IPv4 Address | `10.20.20.10` | Not Yet Collected | Pending |
| Default Gateway | `10.20.20.1` | Not Yet Collected | Pending |
| DNS Configuration | Domain services resolve | Not Yet Collected | Pending |
| DC01 Connectivity | Required services reachable | Not Yet Collected | Pending |
| DC02 Connectivity | Required services reachable | Not Yet Collected | Pending |
| Group Policy | Applicable policies processed | Not Yet Collected | Pending |
| Windows Firewall | Enabled | Not Yet Collected | Pending |
| Antivirus | Active | Not Yet Collected | Pending |
| Windows Updates | Supported and current | Not Yet Collected | Pending |
| Local Administrator Access | Restricted appropriately | Not Yet Collected | Pending |
| Remote Support | Authorized access only | Not Yet Collected | Pending |

### Supporting Evidence

No evidence files have been attached to this record.

Recommended evidence:

- Windows system information
- Network configuration
- Domain membership
- Group Policy results
- Windows Firewall status
- Antivirus status
- Local administrator membership
- Installed applications
- Connectivity test results
- Hyper-V virtual machine configuration

Only verified, sanitized evidence should be added to the repository.

Do not publish passwords, access tokens, private keys, or other sensitive information.

### Verification Summary

**Verification Status:** Not Yet Completed

CLIENT01's documented configuration must be compared against the live Windows 11 environment.

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

Before retiring CLIENT01:

1. Identify the assigned user.
2. Identify required applications and data.
3. Back up or migrate necessary user data.
4. Revoke unnecessary access.
5. Remove or disable the computer account as appropriate.
6. Securely remove the virtual machine and its data.
7. Update related configuration records.
8. Verify that the endpoint is no longer required.

### Lifecycle Notes

No retirement activity is currently documented.

---

## 14. Lessons Learned

### What I Learned

**1. Domain-Joined Workstations**

Domain-joined endpoints can use centralized authentication and receive applicable Active Directory policies.

**2. Group Policy**

Group Policy provides centralized configuration and security management for Windows computers and users.

**3. Endpoint Security**

Employee workstations require security controls such as firewalls, antivirus protection, updates, and appropriate permissions.

**4. Network Dependencies**

A client workstation depends on network connectivity, DNS, and domain services for many organizational functions.

**5. Endpoint Troubleshooting**

Systematic troubleshooting includes checking network settings, authentication, policies, services, and event logs.

**6. Service Configuration Management**

A workstation CI record connects endpoint configuration to incidents, service requests, changes, and lifecycle activities.

### Skills Practiced

- ITIL 4 Service Configuration Management
- Windows 11 Administration
- Active Directory Domain Membership
- Group Policy
- Endpoint Security
- PowerShell
- Windows Troubleshooting
- DNS and Network Connectivity Testing
- Configuration Baseline Design
- Technical Documentation

### Improvement Opportunities

- Verify the Windows 11 build.
- Record virtual machine resources.
- Confirm domain membership.
- Verify IP assignment method.
- Inventory installed applications.
- Review Group Policy results.
- Review local administrator membership.
- Verify firewall and antivirus settings.
- Establish an endpoint recovery procedure.
- Link future Jira records to CI-006.

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

CI-006 has been documented using the Technical Techno Tech Configuration Item Template.

The record identifies CLIENT01's purpose as an employee workstation, its technical specifications, supported services, dependencies, security requirements, and intended configuration baseline.

Outstanding activities include:

- Verify operating system and virtual resources.
- Confirm network and domain configuration.
- Inventory installed applications.
- Review Group Policy.
- Verify endpoint security.
- Review local administrator permissions.
- Document recovery procedures.
- Collect technical evidence.
- Complete the formal CI review.

**Overall Record Status:** Draft — Awaiting Configuration Verification

---

## 16. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial CLIENT01 configuration item record aligned with the TTT CI template |

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations and infrastructure relationships are based on previously documented lab activities. Current verification results are not assumed.

Business ownership, administrative responsibilities, and operational processes are simulated for educational and portfolio purposes.
