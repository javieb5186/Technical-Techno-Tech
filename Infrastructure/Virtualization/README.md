# Hyper-V Virtualization Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Platform:** Microsoft Hyper-V  
**Environment:** Virtualized Business Infrastructure  
**Status:** Existing Lab — Documentation and Verification Ongoing

---

## 1. Overview

This project documents the Hyper-V virtualization environment supporting Technical Techno Tech's internal IT infrastructure.

Hyper-V hosts the virtual machines used to simulate business networking, Windows Server administration, Active Directory, and employee workstation operations.

The virtualized environment allows infrastructure changes, troubleshooting exercises, and controlled testing without requiring separate physical servers for every component.

## 2. Objectives

- Deploy and manage virtual machines.
- Configure virtual networking.
- Allocate virtual hardware resources.
- Deploy Windows Server and Windows 11 systems.
- Run virtualized networking appliances.
- Support isolated network segments.
- Manage VM startup and shutdown.
- Practice virtual infrastructure troubleshooting.
- Understand virtualization dependencies.
- Document VM configurations and maintenance.

## 3. Virtual Machine Inventory

| VM | Operating System / Platform | Function |
|---|---|---|
| FW01 | OPNsense | Firewall and outbound NAT |
| RTR01 | VyOS | Internal routing |
| DC01 | Windows Server | Primary domain controller |
| DC02 | Windows Server Core | Additional domain controller |
| MGMT01 | Windows 11 | IT administration |
| CLIENT01 | Windows 11 | Employee workstation |

The VM names and roles reflect the documented TTT lab.

Actual VM generation, CPU, RAM, storage, and checkpoint settings should be verified from Hyper-V before recording them.

## 4. Virtual Infrastructure Architecture

```text
                  Hyper-V Host
                       |
       +---------------+---------------+
       |               |               |
       v               v               v
     FW01            RTR01          Windows VMs
   OPNsense           VyOS               |
       |               |          +------+------+
       +-------+-------+          |      |      |
               |                  v      v      v
         Virtual Networks        DCs   MGMT01 CLIENT01
```

Hyper-V provides the virtual hardware and network connectivity used by these systems.

## 5. Virtual Networking

The project uses separate virtual network segments to support routing and network isolation.

| Network | Subnet | Purpose |
|---|---|---|
| Transit | `10.10.10.0/24` | OPNsense-to-VyOS connectivity |
| Servers | `10.20.10.0/24` | Domain controllers and servers |
| Clients | `10.20.20.0/24` | Employee workstations |
| Management | `10.20.30.0/24` | Administrative workstations |

### Virtual Networking Objectives

- Separate server and workstation traffic.
- Connect internal networks through VyOS.
- Route outbound traffic through OPNsense.
- Support Active Directory communication.
- Allow controlled troubleshooting of network faults.

The exact Hyper-V virtual switch names and types should be documented from the current host configuration.

## 6. Virtual Machine Configuration

Each VM should have a documented configuration record.

### Recommended VM Record

| Attribute | Value |
|---|---|
| VM Name | [Name] |
| Operating System | [OS] |
| VM Generation | [Generation] |
| Virtual Processors | [Count] |
| Assigned Memory | [Amount] |
| Virtual Disk | [Size and Location] |
| Network Adapters | [Adapters] |
| Virtual Switches | [Switch Names] |
| IP Address | [Address] |
| Operational Role | [Purpose] |
| Current State | [State] |

Do not populate unknown values from assumptions.

## 7. VM Deployment Workflow

A standard VM deployment process may include:

1. Define the business or technical requirement.
2. Determine the required operating system.
3. Select appropriate virtual hardware.
4. Create the virtual machine.
5. Attach the required virtual network.
6. Install the operating system.
7. Configure networking.
8. Install required roles or applications.
9. Apply security settings.
10. Verify connectivity.
11. Document the VM configuration.
12. Record the implementation evidence.

## 8. Hyper-V Administration

Relevant administrative activities include:

- Creating virtual machines
- Modifying virtual hardware
- Configuring virtual switches
- Managing virtual disks
- Connecting installation media
- Starting and stopping VMs
- Reviewing VM health
- Managing integration services
- Inspecting VM networking
- Troubleshooting startup failures

### Example PowerShell Commands

List virtual machines:

```powershell
Get-VM
```

Review VM configuration:

```powershell
Get-VM -Name "DC01" |
Select-Object Name,State,Generation,ProcessorCount,MemoryAssigned
```

Review virtual switches:

```powershell
Get-VMSwitch
```

Review network adapters:

```powershell
Get-VMNetworkAdapter -VMName "DC01"
```

Review virtual disks:

```powershell
Get-VMHardDiskDrive -VMName "DC01"
```

These commands are examples for inspecting an authorized Hyper-V environment.

## 9. Resource Management

Virtual machine resource allocation affects overall infrastructure performance.

Important resources include:

- CPU
- RAM
- Storage
- Network connectivity
- Host capacity

Resource planning should consider:

- Domain controller availability
- Network appliance requirements
- Workstation performance
- Concurrent VM usage
- Available host resources

## 10. Time Synchronization

Time synchronization is particularly important for domain controllers.

Previous TTT lab work included troubleshooting DC01 time synchronization and reviewing Hyper-V Time Synchronization settings.

Domain controller time configuration should be managed consistently with Active Directory's time hierarchy.

Hyper-V integration settings should be documented and verified rather than changed indiscriminately across every VM.

## 11. Checkpoints and Recovery

Hyper-V checkpoints can be useful during controlled lab exercises.

However, checkpoints are not a replacement for proper backups.

Special care is required with:

- Domain controllers
- Replicated services
- Databases
- Stateful applications

Recovery procedures should use supported methods and be tested separately.

## 12. VM Lifecycle Management

### Deployment

Create and configure new VMs.

### Operation

Monitor availability and resource consumption.

### Maintenance

Apply approved updates and configuration changes.

### Recovery

Restore service using supported recovery procedures.

### Decommissioning

Remove VMs only after reviewing:

- Service dependencies
- Required backups
- Configuration records
- Data retention requirements
- Change authorization

## 13. Troubleshooting Scenarios

Potential exercises include:

- VM fails to start
- Incorrect virtual switch assignment
- Missing network connectivity
- Incorrect memory allocation
- Virtual disk capacity issue
- Guest operating system boot failure
- Integration service issue
- Domain controller time synchronization issue

Each exercise should record the actual symptoms, corrective actions, and verification results.

## 14. ITIL 4 Integration

| Practice | Example |
|---|---|
| Incident Management | Virtual machine unavailable |
| Problem Management | Recurring virtual networking failures |
| Change Enablement | VM resource or network changes |
| Monitoring and Event Management | VM availability and resource alerts |
| Service Configuration Management | VM configuration item records |
| Information Security Management | Hypervisor and guest access control |
| Continual Improvement | VM resource optimization |

## 15. Documentation

- [Virtualization Overview](../README.md)
- [Infrastructure Overview](../../README.md)
- [Networking](../../Networking/README.md)
- [Active Directory](../../Active-Directory/README.md)
- [Windows Server](../../Windows-Server/README.md)
- [Configuration Item Standards](../../../Service-Configuration-Management/Configuration-Items/README.md)

## 16. Skills Practiced

- Hyper-V administration
- Virtual machine deployment
- Virtual networking
- Resource allocation
- Virtual disk management
- Windows Server virtualization
- Virtual firewall deployment
- Virtual router deployment
- PowerShell administration
- Infrastructure troubleshooting
- Recovery planning
- Technical documentation

## 17. What I Learned

This project provides practical experience understanding how virtualization supports business IT infrastructure.

Key learning areas include:

- How virtual machines share physical host resources.
- How virtual switches connect isolated network segments.
- How virtualized firewalls and routers support network services.
- How Windows Server and workstations operate within virtual environments.
- How host and guest configurations affect service availability.
- Why recovery planning and resource management are important.

## 18. Future Development

Potential future activities include:

- More detailed VM inventory
- Resource monitoring
- Automated VM deployment
- PowerShell-based administration
- Additional recovery exercises
- Improved infrastructure documentation
- Advanced Hyper-V networking

Future activities are not represented as completed implementations.

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization used for hands-on IT training.

This README documents the Hyper-V virtualization environment and its associated learning objectives. VM specifications and operational results must be supported by actual configuration and verification evidence.
