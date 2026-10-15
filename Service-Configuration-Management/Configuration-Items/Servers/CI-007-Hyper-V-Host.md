# CI-007 — Hyper-V Virtualization Host

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-007 |
| **CI Name** | Hyper-V Host |
| **Organization** | Technical Techno Tech |
| **CI Type** | Virtualization Host |
| **CI Category** | Compute / Virtualization |
| **Environment** | Simulated Enterprise — Hyper-V |
| **Status** | Active — Previously Documented; Current State Pending Verification |
| **Owner** | Internal IT |
| **Managed By** | Systems Administrator |
| **Date Created** | Not Recorded |
| **Last Updated** | 2026-10-14 |
| **Last Verified** | Not Yet Verified for This Record |
| **Related IT Service** | IT-SVC-005 — Server & Infrastructure Services |

---

## 1. Configuration Item Overview

### Description

The Hyper-V Host provides the virtualization infrastructure for Technical Techno Tech's simulated enterprise environment.

It uses Microsoft Hyper-V to host virtual machines representing servers, workstations, and network appliances.

The documented virtual infrastructure includes:

- DC01 — Windows Server domain controller
- DC02 — Windows Server Core domain controller
- MGMT01 — Windows 11 management workstation
- CLIENT01 — Windows 11 employee workstation
- FW01 — OPNsense firewall
- RTR01 — VyOS router

The host also provides virtual networking capabilities that connect these systems.

### Business Purpose

The Hyper-V Host provides a centralized platform for operating TTT's virtual infrastructure.

Its primary purposes include:

- Hosting enterprise infrastructure workloads
- Supporting virtual machine administration
- Providing virtual networking
- Supporting server and workstation deployment
- Enabling controlled troubleshooting scenarios
- Supporting infrastructure testing and recovery exercises
- Reducing the need for dedicated physical hardware for every system

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Hosts Active Directory domain controllers |
| IT-SVC-002 | Endpoint Management | Hosts Windows workstations |
| IT-SVC-004 | Network Connectivity | Hosts virtual network appliances and switching infrastructure |
| IT-SVC-005 | Server & Infrastructure Services | Provides the virtualization platform |
| IT-SVC-006 | Information Security | Hosts network security infrastructure |

**Reference:** [IT Service Catalog](../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** Virtualization Host
- **CI Category:** Compute / Virtualization
- **Criticality:** Critical — Proposed Classification
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

The Hyper-V Host supports multiple infrastructure components.

If the host becomes unavailable, the virtual machines running on it may also become unavailable.

Potential impacts include:

- Loss of domain controller availability
- Loss of virtual firewall services
- Loss of internal routing
- Loss of management workstation access
- Loss of employee workstation access
- Interruption of infrastructure testing
- Interruption of IT support simulations

The documented architecture does not establish host-level redundancy or automatic failover.

---

## 3. Technical Specifications

### General Information

| Attribute | Value |
|---|---|
| **Hostname / Device Name** | Pending Verification |
| **Operating System / Platform** | Microsoft Hyper-V |
| **Host Operating System** | Pending Verification |
| **Version / Build** | Pending Verification |
| **Manufacturer / Vendor** | Microsoft — Hypervisor Software |
| **Hardware Manufacturer** | Pending Verification |
| **Model / Instance Type** | Physical or Nested Virtualization Host — Pending Verification |
| **Asset Identifier** | CI-007 |
| **Location** | TTT Lab |
| **Domain / Tenant** | Pending Verification |

### Hardware / Virtual Resources

| Resource | Configuration |
|---|---|
| **CPU / Processor** | Pending Verification |
| **Logical Processors** | Pending Verification |
| **Memory** | Pending Verification |
| **Storage** | Pending Verification |
| **Network Adapters** | Pending Verification |
| **Virtualization Platform** | Microsoft Hyper-V |
| **Hyper-V Role / Feature** | Previously Configured; Verify |
| **Virtual Machine Count** | Six Documented VMs; Current Inventory Pending Verification |

### Network Configuration

| Attribute | Value |
|---|---|
| **Host IP Address** | Pending Verification |
| **Subnet Mask / Prefix** | Pending Verification |
| **Default Gateway** | Pending Verification |
| **DNS Servers** | Pending Verification |
| **Physical Network Adapters** | Pending Verification |
| **Virtual Switches** | Pending Verification |
| **Virtual Network Segments** | WAN, Transit, Servers, Clients, Management — Documented Architecture |
| **FQDN** | Pending Verification |

### Virtual Machine Inventory

| Virtual Machine | Purpose | Documented Network |
|---|---|---|
| DC01 | Primary domain controller | Servers |
| DC02 | Additional domain controller | Servers |
| MGMT01 | Administrative workstation | Management |
| CLIENT01 | Employee workstation | Clients |
| FW01 | OPNsense firewall | WAN / Transit |
| RTR01 | VyOS router | Transit / Servers / Clients / Management |

The current VM inventory, power states, and network adapter assignments require verification.

### Configuration Verification

Run on the Hyper-V host:

```powershell
Get-ComputerInfo |
Select-Object CsName,WindowsProductName,WindowsVersion,OsBuildNumber
```

```powershell
Get-VM |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

```powershell
Get-VMSwitch |
Select-Object Name,SwitchType,NetAdapterInterfaceDescription
```

```powershell
Get-VMNetworkAdapter -All |
Select-Object VMName,Name,SwitchName,MacAddress
```

```powershell
Get-Volume |
Select-Object DriveLetter,FileSystemLabel,Size,SizeRemaining
```

**Verification Status:** Not Yet Executed for This Record

---

## 4. Installed Roles, Services & Software

### Server Roles / Features

| Role / Feature | Purpose | Configuration Status |
|---|---|---|
| Hyper-V | Virtual machine hosting | Previously Configured |
| Hyper-V Virtual Switch | Virtual network connectivity | Previously Configured |
| Hyper-V Management Tools | VM administration | Pending Verification |
| Additional Host Features | Other host functionality | Pending Inventory |

### Installed Applications

| Application | Version | Purpose |
|---|---|---|
| Microsoft Hyper-V | Pending Verification | Virtualization |
| Hyper-V Manager | Pending Verification | VM management |
| PowerShell Hyper-V Module | Pending Verification | Command-line management |
| Additional Applications | Pending Inventory | Other host functionality |

### Running Services

| Service | Purpose | Expected State |
|---|---|---|
| Hyper-V Virtual Machine Management | VM lifecycle management | Running |
| Hyper-V Host Compute Service | Compute management, where applicable | Operational |
| Windows Event Log | System logging | Running |
| Windows Management Instrumentation | System administration | Operational |

The exact service inventory depends on the host operating system and installed features.

### Verification Commands

```powershell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
```

```powershell
Get-Module -ListAvailable Hyper-V
```

```powershell
Get-Service vmms,vmcompute -ErrorAction SilentlyContinue
```

Commands should be adjusted if the host uses Windows Server rather than a Windows client operating system.

---

## 5. Configuration Baseline

### Approved Configuration

The intended Hyper-V Host configuration includes:

- Microsoft Hyper-V installed and operational
- Sufficient CPU, memory, and storage resources
- Virtual machines configured according to documented requirements
- Virtual network switches supporting the TTT architecture
- Restricted administrative access
- Appropriate host security controls
- Supported Windows updates
- Protected virtual machine storage
- Documented backup and recovery procedures
- Controlled changes to virtual machine resources and networking

This is the proposed baseline. Formal approval has not been recorded.

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| Hyper-V Platform | Installed and Operational | Previously Configured | Pending Verification |
| Host Operating System | Supported Version | Unknown | Pending Verification |
| CPU Resources | Sufficient for Workloads | Unknown | Pending Verification |
| Memory Resources | Sufficient for Workloads | Unknown | Pending Verification |
| Storage Capacity | Adequate Free Space | Unknown | Pending Verification |
| Virtual Switches | Match TTT Network Architecture | Previously Configured | Pending Verification |
| VM Network Assignments | Match Documented Topology | Previously Configured | Pending Verification |
| Administrative Access | Restricted | Unknown | Pending Verification |
| Host Firewall | Enabled and Appropriately Configured | Unknown | Pending Verification |
| Windows Updates | Supported and Current | Unknown | Pending Verification |
| Backup Configuration | Documented and Tested | Unknown | Pending Verification |

### Configuration Policies

Potentially applicable controls include:

- Host operating system security policies
- Windows Firewall configuration
- Local administrator restrictions
- Remote management restrictions
- Windows Update policies
- Virtual machine storage permissions
- Backup and recovery policies
- Virtual machine change authorization
- Administrative auditing

Actual applied policies require verification.

### Configuration Verification

**Last Verified:** Not Yet Verified

**Verification Method:** Hyper-V Manager, PowerShell, Windows Administrative Tools

**Verification Result:** Not Assessed

**Notes:**

Previous TTT infrastructure work included deploying and managing virtual machines and configuring virtual networking.

The current host configuration must be verified before establishing a confirmed configuration baseline.

---

## 6. Relationships & Dependencies

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| CI-001 — DC01 | Hosts | Domain controller VM |
| CI-002 — DC02 | Hosts | Additional domain controller VM |
| CI-003 — FW01 | Hosts | OPNsense firewall VM |
| CI-004 — RTR01 | Hosts | VyOS router VM |
| CI-005 — MGMT01 | Hosts | Administrative workstation VM |
| CI-006 — CLIENT01 | Hosts | Employee workstation VM |
| CI-008 — Active Directory Domain | Supports | Hosts domain controller infrastructure |
| CI-009 — Virtual Networks | Provides Infrastructure For | Virtual network connectivity |

### Upstream Dependencies

The Hyper-V Host depends on:

- Physical or underlying compute resources
- System memory
- Storage infrastructure
- Host operating system
- Hyper-V platform
- Network adapters
- Power and hardware availability, where applicable

If Hyper-V is running within another virtual environment, additional upstream dependencies may exist.

### Downstream Dependencies

The Hyper-V Host supports:

- DC01
- DC02
- FW01
- RTR01
- MGMT01
- CLIENT01
- TTT virtual networking
- Active Directory services hosted by the VMs
- Network connectivity provided by the virtual appliances
- Administrative and troubleshooting workflows

### Dependency Diagram

```text
                    Hyper-V Host
                         |
        +----------------+----------------+
        |                |                |
        v                v                v
   Infrastructure     Networking       Workstations
        |                |                |
   +----+----+      +----+----+      +----+----+
   |         |      |         |      |         |
   v         v      v         v      v         v
  DC01      DC02   FW01      RTR01  MGMT01   CLIENT01
```

**Reference:** [Hyper-V Infrastructure](../../../Infrastructure/Virtualization/Hyper-V/README.md)

### Impact of CI Failure

If the Hyper-V Host becomes unavailable:

- Hosted virtual machines may stop operating.
- Domain authentication and DNS services may become unavailable.
- Virtual firewall and router services may become unavailable.
- Internal and external network connectivity may be interrupted.
- Administrative workstations may become unavailable.
- Employee workstation simulations may be interrupted.

The severity depends on the availability of alternative infrastructure and recovery capabilities.

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Host Administration | Authorized Systems Administrators | Full Administration |
| Hyper-V Management | Authorized Virtualization Administrators | Administrative |
| Remote Management | Authorized IT Administrators | As Required |
| Standard Employee Access | Not Intended | Restricted |

Actual account membership and permissions require verification.

### Security Controls

Recommended controls include:

- Restricting host administrative access
- Applying least privilege
- Keeping the host operating system updated
- Enabling Windows Firewall
- Maintaining endpoint protection
- Protecting VM configuration and storage files
- Restricting remote management
- Reviewing administrative event logs
- Protecting backups
- Disabling unnecessary host services

### Virtualization Security Considerations

The Hyper-V Host supports multiple systems with different security requirements.

Recommended practices include:

- Separating management and workload traffic where practical
- Limiting access to virtual switches
- Protecting virtual machine storage
- Controlling VM export and import operations
- Reviewing virtual machine checkpoints
- Restricting changes to virtual network adapters
- Maintaining appropriate host isolation

### Security Review

**Last Security Review:** Not Recorded

**Security Status:** Not Assessed

### Security Notes

Compromise of the Hyper-V Host could affect every virtual machine it manages.

The host should be treated as privileged infrastructure rather than a standard workstation.

---

## 8. Monitoring & Maintenance

### Monitoring Configuration

| Monitoring Item | Tool / Method | Expected Condition |
|---|---|---|
| Host Availability | Windows / Hyper-V Tools | Operational |
| CPU Utilization | Task Manager / Performance Monitor | Sufficient Capacity |
| Memory Utilization | PowerShell / Performance Monitor | Sufficient Capacity |
| Storage Capacity | PowerShell | Adequate Free Space |
| VM Status | Hyper-V Manager / PowerShell | Expected VMs Operational |
| Virtual Switches | PowerShell | Correctly Configured |
| Event Logs | Event Viewer | No Unresolved Critical Errors |
| Host Updates | Windows Update | Supported and Current |
| Backup Status | Backup Tool | Successful According to Policy |

No automated monitoring deployment is confirmed.

### Maintenance Activities

- Review host health.
- Review CPU and memory utilization.
- Check storage capacity.
- Verify virtual machine states.
- Review virtual switch assignments.
- Review event logs.
- Apply approved updates.
- Review administrative access.
- Verify backup procedures.
- Update configuration documentation.

### Maintenance Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Systems Administrator

**Last Maintenance:** Not Recorded

**Next Planned Maintenance:** Not Scheduled

### Diagnostic Commands

Review virtual machine states:

```powershell
Get-VM |
Select-Object Name,State,Uptime
```

Review host memory:

```powershell
Get-CimInstance Win32_OperatingSystem |
Select-Object TotalVisibleMemorySize,FreePhysicalMemory
```

Review virtual switches:

```powershell
Get-VMSwitch
```

Review VM network adapters:

```powershell
Get-VMNetworkAdapter -All
```

Review virtual hard disks:

```powershell
Get-VM |
Get-VMHardDiskDrive |
Select-Object VMName,ControllerType,Path
```

Review Hyper-V management events:

```powershell
Get-WinEvent -LogName "Microsoft-Windows-Hyper-V-VMMS-Admin" -MaxEvents 20
```

**Execution Status:** Commands Provided — Results Not Yet Recorded

---

## 9. Backup & Recovery

### Backup Configuration

**Backup Required:** Yes — Recommended

**Backup Method:** Pending Definition

**Backup Frequency:** Not Yet Established

**Backup Destination:** Pending Verification

**Last Successful Backup:** Not Recorded

### Recovery Information

**Recovery Procedure:** Pending Documentation

**Recovery Dependencies:**

- Available host hardware or replacement environment
- Supported host operating system
- Hyper-V platform
- Virtual machine backups
- Virtual switch configuration
- VM storage
- Network connectivity
- Administrative credentials

**Recovery Testing:** Not Recorded

### Recovery Considerations

A recovery procedure should account for:

1. Restoring or rebuilding the host operating system.
2. Installing and configuring Hyper-V.
3. Restoring virtual switches.
4. Restoring virtual machine files or supported VM backups.
5. Verifying virtual network adapter assignments.
6. Starting infrastructure VMs in an appropriate order.
7. Verifying FW01 and RTR01 connectivity.
8. Verifying DC01 and DC02 health.
9. Testing workstation connectivity.
10. Updating the CI record.

Domain controller backups require supported Active Directory-aware procedures.

Hyper-V checkpoints are not substitutes for backups.

Restoring a complete virtualization environment may require workload-specific recovery sequencing and validation.

---

## 10. Configuration History

Track significant configuration changes affecting the Hyper-V Host.

| Date | Change ID | Description | Result |
|---|---|---|---|
| Not Recorded | N/A | Initial Hyper-V configuration | Previously Documented |
| Not Recorded | N/A | Deployment of Windows Server VMs | Previously Documented |
| Not Recorded | N/A | Deployment of Windows 11 VMs | Previously Documented |
| Not Recorded | N/A | Deployment of OPNsense and VyOS VMs | Previously Documented |
| Not Recorded | N/A | Virtual networking configuration | Previously Documented |

### Current Configuration Summary

The Hyper-V Host is documented as the virtualization platform supporting TTT's Windows Server, Windows 11, OPNsense, and VyOS virtual machines.

The current host operating system, hardware resources, VM inventory, virtual switch configuration, and backup arrangements require verification.

Detailed implementation steps and approvals should remain in associated Change Enablement records.

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

- [Hyper-V Infrastructure](../../../Infrastructure/Virtualization/Hyper-V/README.md)
- [Virtualization Overview](../../../Infrastructure/Virtualization/README.md)
- [Server Inventory](../../../Infrastructure/Windows-Server/Server-Inventory.md)
- [Network Topology](../../../Infrastructure/Networking/Network-Topology.md)
- [OPNsense Infrastructure](../../../Infrastructure/Networking/OPNsense/README.md)
- [VyOS Infrastructure](../../../Infrastructure/Networking/VyOS/README.md)
- [DC01 Configuration Item](CI-001-DC01.md)
- [DC02 Configuration Item](CI-002-DC02.md)
- [FW01 Configuration Item](../Network-Devices/CI-003-FW01.md)
- [RTR01 Configuration Item](../Network-Devices/CI-004-RTR01.md)
- [MGMT01 Configuration Item](../Workstations/CI-005-MGMT01.md)
- [CLIENT01 Configuration Item](../Workstations/CI-006-CLIENT01.md)

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Hostname | Recorded | Not Yet Collected | Pending |
| Host Operating System | Supported Version | Not Yet Collected | Pending |
| Hyper-V Platform | Operational | Not Yet Collected | Pending |
| CPU Resources | Documented | Not Yet Collected | Pending |
| Memory Resources | Documented | Not Yet Collected | Pending |
| Storage Resources | Documented | Not Yet Collected | Pending |
| VM Inventory | Matches Approved Inventory | Not Yet Collected | Pending |
| Virtual Switches | Match Documented Architecture | Not Yet Collected | Pending |
| VM Network Assignments | Correctly Configured | Not Yet Collected | Pending |
| Administrative Access | Restricted | Not Yet Collected | Pending |
| Windows Firewall | Enabled | Not Yet Collected | Pending |
| Windows Updates | Supported and Current | Not Yet Collected | Pending |
| Backup Configuration | Documented and Tested | Not Yet Collected | Pending |

### Supporting Evidence

No evidence files have been attached to this record.

Recommended evidence:

- Host system information
- Hyper-V feature status
- CPU and memory specifications
- Storage configuration
- Virtual machine inventory
- Virtual machine resource allocations
- Virtual switch configuration
- Virtual network adapter assignments
- Host security configuration
- Backup configuration
- Hyper-V event logs

Only verified, sanitized evidence should be added to the repository.

Do not publish passwords, access tokens, private keys, or other sensitive information.

### Verification Summary

**Verification Status:** Not Yet Completed

The Hyper-V Host's documented configuration must be compared against the live environment.

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

Before retiring the Hyper-V Host:

1. Identify all hosted virtual machines.
2. Identify dependent IT services.
3. Review available replacement infrastructure.
4. Back up required virtual machines and configuration data.
5. Plan workload migration or retirement.
6. Document virtual switch and network configurations.
7. Perform an authorized migration or shutdown.
8. Verify services on replacement infrastructure.
9. Securely remove remaining VM and host data.
10. Update CI relationships.
11. Complete the retirement review.

### Lifecycle Notes

No retirement activity is currently documented.

---

## 14. Lessons Learned

### What I Learned

**1. Virtualization**

Hyper-V allows multiple operating systems and infrastructure components to run as virtual machines on shared compute resources.

**2. Infrastructure Consolidation**

Virtualization reduces the need for dedicated hardware for every server or network appliance.

**3. Virtual Networking**

Hyper-V virtual switches connect virtual machines to internal networks and external resources.

**4. Resource Management**

CPU, memory, storage, and networking resources must be allocated appropriately to support virtual workloads.

**5. Infrastructure Dependencies**

A virtualization host can become a single point of failure for multiple IT services.

**6. Service Configuration Management**

Documenting the virtualization host helps identify downstream dependencies and supports incident investigation, change planning, and recovery.

### Skills Practiced

- ITIL 4 Service Configuration Management
- Microsoft Hyper-V
- Virtual Machine Administration
- Virtual Networking
- Windows Server Virtualization
- Infrastructure Dependency Mapping
- PowerShell
- Configuration Baseline Design
- Backup and Recovery Planning
- Technical Documentation

### Improvement Opportunities

- Verify the host operating system.
- Record hardware specifications.
- Inventory all virtual machines.
- Document virtual switches.
- Verify VM network adapter assignments.
- Review host security settings.
- Establish backup procedures.
- Test infrastructure recovery.
- Establish maintenance schedules.
- Link future Jira records to CI-007.

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

CI-007 has been documented using the Technical Techno Tech Configuration Item Template.

The record identifies the Hyper-V Host's purpose, hosted infrastructure, technical specifications, dependencies, security considerations, and intended configuration baseline.

Outstanding activities include:

- Verify host specifications.
- Confirm the virtual machine inventory.
- Document virtual switch configuration.
- Verify network adapter assignments.
- Review host security.
- Establish backup and recovery procedures.
- Collect technical evidence.
- Complete the formal CI review.

**Overall Record Status:** Draft — Awaiting Configuration Verification

---

## 16. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial Hyper-V Host configuration item record aligned with the TTT CI template |

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations and infrastructure relationships are based on previously documented lab activities. Current verification results are not assumed.

Business ownership, administrative responsibilities, and operational processes are simulated for educational and portfolio purposes.
