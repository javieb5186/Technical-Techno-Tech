# Technical Techno Tech — Hyper-V Virtualization Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Document ID:** INF-VIRT-001  
**Document Type:** Virtualization Infrastructure Documentation  
**Version:** 1.0  
**Status:** Existing Lab — Verification Ongoing  
**Platform:** Microsoft Hyper-V  
**Function:** Internal IT  
**ITIL 4 Practice:** Service Configuration Management

---

## 1. Purpose

This document describes the Hyper-V virtualization infrastructure supporting Technical Techno Tech.

It provides a centralized reference for:

- Virtualization architecture
- Virtual machine inventory
- Virtual networking
- Virtual switches
- Virtual machine resources
- Storage
- Hyper-V administration
- Checkpoints
- Backup and recovery
- Security
- Monitoring
- Troubleshooting
- Configuration management
- Change management

Hyper-V provides the virtualization platform used to operate TTT's Windows Server, workstation, firewall, and router environments.

---

## 2. Environment Overview

Technical Techno Tech operates a virtualized IT infrastructure using Microsoft Hyper-V.

The environment includes:

- Windows Server domain controllers
- Windows 11 workstations
- OPNsense firewall
- VyOS router
- Segmented virtual networks

### Platform Inventory

| Attribute | Configuration |
|---|---|
| Virtualization Platform | Microsoft Hyper-V |
| Hyper-V Host | Pending Verification |
| Host Operating System | Pending Verification |
| Host CPU | Pending Verification |
| Host Memory | Pending Verification |
| Virtual Machine Storage | Pending Verification |
| Virtual Switch Configuration | Pending Verification |
| Backup Configuration | Pending Verification |

---

## 3. Virtualization Architecture

### 3.1 Logical Architecture

```text
                    Hyper-V Host
                         |
             +-----------+-----------+
             |                       |
             v                       v
        Virtual Machines       Virtual Switches
             |                       |
      +------+------+                |
      |             |                |
      v             v                v
 Windows VMs    Network VMs    Virtual Networks
      |             |                |
      |             |                |
      +-------------+----------------+
                    |
                    v
            TTT Infrastructure
```

### 3.2 Infrastructure Topology

```text
                     Internet
                        |
                        v
                   FW01 - OPNsense
                        |
                        v
                   RTR01 - VyOS
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
       Servers        Clients      Management
       Network        Network       Network
          |             |             |
          v             v             v
       DC01/DC02      CLIENT01       MGMT01
```

The virtual machines communicate through the Hyper-V networking configuration.

---

## 4. Virtual Machine Inventory

### 4.1 Documented Virtual Machines

| VM | Operating System / Platform | Function | IP Address |
|---|---|---|---|
| FW01 | OPNsense | Firewall | `10.10.10.1` |
| RTR01 | VyOS | Router | `10.10.10.2` |
| DC01 | Windows Server Desktop Experience | Domain Controller | `10.20.10.10` |
| DC02 | Windows Server Core | Domain Controller | `10.20.10.11` |
| CLIENT01 | Windows 11 | Employee Workstation | `10.20.20.10` |
| MGMT01 | Windows 11 | Management Workstation | `10.20.30.10` |

FW01 also has a previously documented WAN address of `192.168.1.176`.

### 4.2 Inventory Requirements

For each VM, document:

- VM name
- Operating system
- VM generation
- Virtual processors
- Assigned memory
- Virtual disk configuration
- Network adapters
- Virtual switches
- VM state
- Checkpoint status
- Backup status

### 4.3 VM Configuration Matrix

| VM | Generation | vCPU | RAM | Disk | Status |
|---|---|---|---|---|---|
| FW01 | Pending | Pending | Pending | Pending | Verify |
| RTR01 | Pending | Pending | Pending | Pending | Verify |
| DC01 | Pending | Pending | Pending | Pending | Verify |
| DC02 | Pending | Pending | Pending | Pending | Verify |
| CLIENT01 | Pending | Pending | Pending | Pending | Verify |
| MGMT01 | Pending | Pending | Pending | Pending | Verify |

---

## 5. Hyper-V Virtual Networking

### 5.1 Overview

Hyper-V virtual switches allow virtual machines to communicate with each other and, depending on configuration, external networks.

### 5.2 Virtual Switch Types

**External Switch**

Connects virtual machines to an external physical network through a host network adapter.

**Internal Switch**

Allows communication between virtual machines and the Hyper-V host.

**Private Switch**

Allows communication between virtual machines attached to the same switch without direct host network connectivity through that switch.

### 5.3 TTT Virtual Networks

The documented TTT network includes:

| Network | Subnet | Purpose |
|---|---|---|
| Transit | `10.10.10.0/24` | FW01-to-RTR01 connectivity |
| Servers | `10.20.10.0/24` | Domain controllers |
| Clients | `10.20.20.0/24` | Employee workstations |
| Management | `10.20.30.0/24` | Administrative workstation |

### 5.4 Virtual Switch Inventory

| Network | Virtual Switch Name | Switch Type |
|---|---|---|
| Transit | Pending Verification | Pending Verification |
| Servers | Pending Verification | Pending Verification |
| Clients | Pending Verification | Pending Verification |
| Management | Pending Verification | Pending Verification |
| WAN / Upstream | Pending Verification | Pending Verification |

### 5.5 Verification

On the Hyper-V host:

```powershell
Get-VMSwitch
```

Review VM network adapters:

```powershell
Get-VMNetworkAdapter -VMName *
```

Review network adapter connections:

```powershell
Get-VMNetworkAdapter -VMName * |
Select-Object VMName,Name,SwitchName,Status
```

### Verification Checklist

- [ ] Virtual switches inventoried
- [ ] Switch types verified
- [ ] VM adapter assignments reviewed
- [ ] Transit network verified
- [ ] Server network verified
- [ ] Client network verified
- [ ] Management network verified
- [ ] WAN connectivity reviewed

---

## 6. Virtual Machine Networking

### 6.1 Overview

Each virtual machine uses virtual network adapters to connect to the appropriate network.

### 6.2 Expected Connectivity

| VM | Network Connection |
|---|---|
| FW01 | WAN and Transit |
| RTR01 | Transit, Servers, Clients, Management |
| DC01 | Servers |
| DC02 | Servers |
| CLIENT01 | Clients |
| MGMT01 | Management |

Actual adapter and switch assignments require verification.

### 6.3 Network Verification

Review a VM's network adapters:

```powershell
Get-VMNetworkAdapter -VMName "DC01"
```

Review all VM adapters:

```powershell
Get-VMNetworkAdapter -VMName * |
Select-Object VMName,Name,SwitchName
```

### 6.4 Important

Incorrect virtual switch assignments can interrupt:

- Domain authentication
- DNS
- Routing
- Internet connectivity
- Remote administration
- Active Directory replication

---

## 7. Virtual Machine Resource Management

### 7.1 Overview

Hyper-V allocates virtualized computing resources to guest operating systems.

### 7.2 Primary Resources

- Virtual processors
- Memory
- Virtual storage
- Network adapters
- Virtual firmware settings

### 7.3 CPU Configuration

Review virtual processor assignments:

```powershell
Get-VMProcessor -VMName *
```

### 7.4 Memory Configuration

Review VM memory:

```powershell
Get-VMMemory -VMName *
```

### 7.5 VM Status

```powershell
Get-VM |
Select-Object Name,State,CPUUsage,MemoryAssigned,Uptime
```

### 7.6 Resource Planning

Consider:

- Host resource limitations
- VM workload requirements
- Available memory
- Storage capacity
- CPU utilization
- Simultaneous VM operation

### 7.7 Important

Resource allocation should be based on actual workload requirements and available host capacity.

VM resource settings have not yet been inventoried.

---

## 8. Virtual Storage

### 8.1 Overview

Hyper-V virtual machines use virtual storage to host operating systems, applications, and data.

### 8.2 Storage Components

- Virtual hard disks
- VHDX files
- Virtual storage controllers
- Host storage volumes
- Checkpoint-related storage

### 8.3 VM Storage Verification

Review VM hard disks:

```powershell
Get-VMHardDiskDrive -VMName *
```

Review virtual hard disk information:

```powershell
Get-VMHardDiskDrive -VMName "DC01" |
ForEach-Object {
    Get-VHD -Path $_.Path
}
```

### 8.4 Storage Considerations

- Monitor available capacity.
- Avoid unnecessary storage overcommitment.
- Protect VM configuration files.
- Maintain appropriate backups.
- Review checkpoint storage growth.
- Document disk locations.

### 8.5 Verification Checklist

- [ ] VM storage locations identified
- [ ] Virtual disk sizes recorded
- [ ] Disk types reviewed
- [ ] Available storage reviewed
- [ ] Backup locations documented

---

## 9. Hyper-V Administration

### 9.1 Administrative Tools

Hyper-V can be administered using:

- Hyper-V Manager
- PowerShell
- Windows Admin Center
- Supported remote management tools

### 9.2 Common Tasks

- Start virtual machines.
- Shut down virtual machines.
- Review VM configuration.
- Manage virtual switches.
- Adjust VM resources.
- Inspect checkpoints.
- Review virtual storage.
- Troubleshoot VM connectivity.

### 9.3 Example Commands

List virtual machines:

```powershell
Get-VM
```

Start a virtual machine:

```powershell
Start-VM -Name "CLIENT01"
```

Request a graceful guest shutdown:

```powershell
Stop-VM -Name "CLIENT01" -Shutdown
```

The shutdown command requires supported guest integration services.

### 9.4 Important

Do not force-stop domain controllers or other infrastructure VMs unless necessary and appropriate for the situation.

Use supported shutdown procedures whenever possible.

---

## 10. Virtual Machine Startup Dependencies

### 10.1 Overview

Some TTT virtual machines depend on services provided by other VMs.

### 10.2 Logical Dependencies

```text
Hyper-V Host
     |
     v
FW01 - OPNsense
     |
     v
RTR01 - VyOS
     |
     v
DC01 / DC02
     |
     v
CLIENT01 / MGMT01
```

This diagram represents logical service dependencies, not a verified automatic startup sequence.

### 10.3 Startup Considerations

- Ensure virtual networking is available.
- Ensure routing services are operational.
- Ensure domain controllers are available.
- Verify DNS.
- Start dependent workstations as needed.

### 10.4 Verification

```powershell
Get-VM |
Select-Object Name,AutomaticStartAction,AutomaticStartDelay
```

### 10.5 Important

Hyper-V startup settings do not inherently verify that an application service is ready.

A running VM may still have unavailable services.

---

## 11. Hyper-V Checkpoints

### 11.1 Overview

Hyper-V checkpoints capture VM state or data at a particular point in time.

They can be useful for controlled lab experiments.

### 11.2 Checkpoint Types

**Production Checkpoints**

Use guest-supported backup technologies to create data-consistent checkpoints when supported.

**Standard Checkpoints**

Capture VM state, including memory state, and are primarily suited to development and testing scenarios.

### 11.3 Lab Applications

Potential uses include:

- Testing configuration changes
- Practicing troubleshooting
- Testing software installation
- Reverting noncritical lab experiments

### 11.4 Checkpoint Verification

```powershell
Get-VMSnapshot -VMName *
```

### 11.5 Important

Checkpoints are not replacements for backups.

Reverting domain controllers to earlier states requires special care because Active Directory is a replicated directory service.

Use supported Active Directory recovery methods and understand the implications of VM restoration.

### 11.6 Verification Checklist

- [ ] Existing checkpoints inventoried
- [ ] Checkpoint types reviewed
- [ ] Storage impact reviewed
- [ ] Domain controller recovery considerations documented
- [ ] Unnecessary checkpoints reviewed

---

## 12. Backup and Recovery

### 12.1 Purpose

Virtual machine backups support recovery from system failure, data loss, and configuration problems.

### 12.2 Backup Considerations

- Host configuration
- Virtual machine files
- Virtual hard disks
- Guest operating system data
- Application-consistent backups
- Domain controller System State
- Firewall and router configurations

### 12.3 Recovery Planning

Potential recovery activities include:

- Restoring a VM from backup
- Rebuilding a failed VM
- Restoring guest application data
- Recovering domain services
- Reconnecting virtual networks
- Restoring firewall or router configurations

### 12.4 Verification Checklist

- [ ] Backup solution identified
- [ ] Backup schedule documented
- [ ] VM backup coverage reviewed
- [ ] Last successful backups recorded
- [ ] Recovery procedures documented
- [ ] Restore testing performed

### Important

The current TTT backup implementation and recovery test results require verification.

---

## 13. Hyper-V Security

### 13.1 Security Objectives

- Protect the virtualization host.
- Restrict administrative access.
- Protect VM storage.
- Isolate network segments appropriately.
- Maintain secure guest configurations.
- Protect backups.
- Review changes.

### 13.2 Security Recommendations

- Use authorized administrative accounts.
- Apply host updates.
- Review Hyper-V permissions.
- Restrict management access.
- Protect VM configuration files.
- Review virtual switch connections.
- Avoid exposing unnecessary services.
- Maintain supported guest operating systems.

### 13.3 Security Checklist

- [ ] Host access reviewed
- [ ] Administrative permissions reviewed
- [ ] Host update status reviewed
- [ ] VM storage permissions reviewed
- [ ] Virtual network isolation reviewed
- [ ] Backup security reviewed

---

## 14. Monitoring and Performance

### 14.1 Monitoring Objectives

Monitor:

- VM availability
- CPU utilization
- Memory consumption
- Storage capacity
- Virtual network connectivity
- Hyper-V events
- Host resource availability

### 14.2 Example Commands

Review VM status:

```powershell
Get-VM
```

Review VM resource usage:

```powershell
Get-VM |
Select-Object Name,State,CPUUsage,MemoryAssigned,Uptime
```

Review virtual switch configuration:

```powershell
Get-VMSwitch
```

### 14.3 Monitoring Matrix

| Component | Monitoring Focus | Status |
|---|---|---|
| Hyper-V Host | CPU, memory, storage | Pending |
| FW01 | VM availability | Pending |
| RTR01 | VM availability | Pending |
| DC01 | VM availability | Pending |
| DC02 | VM availability | Pending |
| CLIENT01 | VM availability | Pending |
| MGMT01 | VM availability | Pending |
| Virtual Switches | Connectivity | Pending |

---

## 15. Hyper-V Troubleshooting

### 15.1 General Workflow

1. Identify the affected VM.
2. Confirm symptoms.
3. Review VM state.
4. Review host resources.
5. Review virtual network connections.
6. Review storage.
7. Review integration services.
8. Review relevant logs.
9. Identify the cause.
10. Implement an authorized correction.
11. Verify functionality.
12. Document findings.

### 15.2 Troubleshooting Matrix

| Issue | Potential Cause | Investigation |
|---|---|---|
| VM will not start | Resource or configuration issue | Review VM and host events |
| VM has no network connectivity | Incorrect virtual switch | Review VM adapter assignment |
| VM performance is poor | Resource contention | Review CPU, memory, storage |
| VM cannot access disk | Storage issue | Review VHDX and host storage |
| Domain authentication fails | DC, DNS, or networking issue | Review infrastructure dependencies |
| Checkpoint operation fails | Storage or configuration issue | Review checkpoint and host logs |

### 15.3 Example Scenario

**Scenario:** CLIENT01 cannot communicate with DC01.

Potential investigation:

1. Verify CLIENT01 is running.
2. Verify DC01 is running.
3. Review VM network adapter connections.
4. Verify virtual switches.
5. Review IP configuration.
6. Verify RTR01 routing.
7. Verify DNS.
8. Test domain connectivity.
9. Document findings.

**Status:** Illustrative Scenario — Not Executed

---

## 16. ITIL 4 Integration

| Practice | Application |
|---|---|
| Incident Management | Restore unavailable virtual machines |
| Problem Management | Investigate recurring virtualization issues |
| Change Enablement | Control VM and network changes |
| Knowledge Management | Document Hyper-V procedures |
| Monitoring and Event Management | Review VM and host health |
| Service Configuration Management | Track virtual machines and dependencies |
| Information Security Management | Protect host and guest environments |
| Continual Improvement | Improve virtualization reliability |

### Example Incident

**Scenario:** DC01 becomes unavailable.

Potential workflow:

1. Service Desk records the incident.
2. IT verifies DC01's VM state.
3. Host resource and storage conditions are reviewed.
4. Network connectivity is checked.
5. Domain services are investigated.
6. An authorized corrective action is implemented.
7. Authentication and DNS functionality are verified.
8. The incident is documented and closed.

---

## 17. Service Configuration Management

### Configuration Items

| Configuration Item | Type |
|---|---|
| Hyper-V Host | Virtualization Host |
| FW01 | Firewall VM |
| RTR01 | Router VM |
| DC01 | Domain Controller VM |
| DC02 | Domain Controller VM |
| CLIENT01 | Workstation VM |
| MGMT01 | Management Workstation VM |

### Configuration Relationships

```text
Hyper-V Host
     |
     +-- Virtual Switches
     |
     +-- FW01
     |
     +-- RTR01
     |
     +-- DC01
     |
     +-- DC02
     |
     +-- CLIENT01
     |
     +-- MGMT01
```

### Configuration Management Requirements

- Maintain accurate VM inventory.
- Document resource assignments.
- Record virtual network connections.
- Document storage.
- Track important configuration changes.
- Maintain recovery procedures.
- Verify dependencies.

---

## 18. Change Management

Hyper-V changes may affect multiple infrastructure services.

### Examples

- Creating or deleting VMs
- Changing VM memory
- Changing virtual processors
- Modifying virtual switches
- Changing network adapters
- Expanding virtual disks
- Applying host updates
- Restoring virtual machines

### Proposed Change Workflow

1. Identify the required change.
2. Assess affected VMs and services.
3. Review dependencies.
4. Obtain applicable authorization.
5. Prepare implementation steps.
6. Prepare a recovery plan.
7. Implement the change.
8. Verify VM functionality.
9. Test network and application services.
10. Update documentation.

---

## 19. Future Improvements

Potential projects include:

- Automated VM inventory
- Hyper-V monitoring
- VM resource optimization
- Backup and recovery exercises
- PowerShell automation
- Additional virtual network segments
- Controlled troubleshooting simulations
- Automated lab deployment
- Infrastructure configuration reporting

These projects are proposed and are not documented as completed.

---

## 20. Skills Practiced

- Microsoft Hyper-V
- Virtual machine administration
- Virtual networking
- Virtual switches
- Windows Server virtualization
- Virtualized firewall deployment
- Virtualized router deployment
- VM resource allocation
- Virtual storage
- PowerShell
- Infrastructure troubleshooting
- Backup and recovery concepts
- Configuration management
- Change management
- ITIL-aligned infrastructure operations

---

## 21. What I Learned

**1. Virtualization**

Hyper-V allows multiple operating systems to run as virtual machines on shared hardware.

**2. Virtual Networking**

Virtual switches connect VMs to internal and external networks.

**3. Infrastructure Dependencies**

Domain controllers, routers, firewalls, and workstations depend on one another for different services.

**4. Resource Management**

Virtual machines require appropriate CPU, memory, storage, and networking resources.

**5. Checkpoints**

Checkpoints can support controlled testing but should not replace proper backups.

**6. Troubleshooting**

Virtualization troubleshooting requires examining both the guest operating system and the underlying Hyper-V environment.

**7. Configuration Management**

Accurate VM documentation supports maintenance, troubleshooting, recovery, and change management.

---

## 22. Final Verification Checklist

### Host

- [ ] Hyper-V host identified
- [ ] Host operating system verified
- [ ] CPU and memory documented
- [ ] Storage configuration documented

### Virtual Machines

- [ ] All VMs inventoried
- [ ] VM generations verified
- [ ] vCPU assignments documented
- [ ] Memory assignments documented
- [ ] Virtual disks documented

### Networking

- [ ] Virtual switches inventoried
- [ ] VM network adapters verified
- [ ] Network segmentation reviewed
- [ ] Routing connectivity tested

### Security and Recovery

- [ ] Administrative access reviewed
- [ ] Checkpoints inventoried
- [ ] Backup configuration verified
- [ ] Recovery procedures documented

### Documentation

- [ ] Configuration evidence collected
- [ ] Screenshots sanitized
- [ ] Dependencies documented
- [ ] Revision history updated

---

## 23. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT Hyper-V virtualization infrastructure documentation |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

The Hyper-V environment and listed virtual machines are based on previously documented TTT lab infrastructure.

Exact host specifications, VM resource assignments, virtual switch configurations, backup settings, and operational results require verification.

Proposed procedures and example scenarios do not represent completed activities.

Sensitive infrastructure information must be reviewed before publication.
