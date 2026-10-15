# CI-009 — TTT Virtual Networks

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-009 |
| **CI Name** | TTT Virtual Networks |
| **Organization** | Technical Techno Tech |
| **CI Type** | Logical Infrastructure — Virtual Networking |
| **CI Category** | Networking / Virtualization |
| **Environment** | Simulated Enterprise — Hyper-V |
| **Status** | Active — Previously Documented; Current State Pending Verification |
| **Owner** | Internal IT |
| **Managed By** | Network Administrator |
| **Date Created** | Not Recorded |
| **Last Updated** | 2026-10-14 |
| **Last Verified** | Not Yet Verified for This Record |
| **Related IT Service** | IT-SVC-004 — Network Connectivity |

---

## 1. Configuration Item Overview

### Description

TTT Virtual Networks represents the logical network infrastructure supporting Technical Techno Tech's simulated enterprise environment.

The network architecture uses Microsoft Hyper-V virtual networking, an OPNsense firewall, and a VyOS router to connect servers, employee workstations, and administrative systems.

The documented architecture consists of five network segments:

- WAN
- Transit
- Servers
- Clients
- Management

FW01 provides the external firewall boundary, while RTR01 provides routing between the internal network segments.

CI-009 represents the combined virtual networking configuration rather than an individual network device.

### Business Purpose

TTT Virtual Networks provides the connectivity required for enterprise IT services.

Its primary purposes include:

- Connecting virtual infrastructure components
- Separating systems into logical network segments
- Supporting communication between servers and workstations
- Providing internal routing through RTR01
- Providing external connectivity through FW01
- Supporting Active Directory authentication and DNS
- Enabling remote administration
- Supporting network troubleshooting and security exercises

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Provides connectivity to directory services |
| IT-SVC-002 | Endpoint Management | Connects employee and management workstations |
| IT-SVC-004 | Network Connectivity | Primary virtual network infrastructure |
| IT-SVC-005 | Server & Infrastructure Services | Provides connectivity between infrastructure components |
| IT-SVC-006 | Information Security | Supports network segmentation and traffic control |

**Reference:** [IT Service Catalog](../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** Logical Infrastructure — Virtual Networking
- **CI Category:** Networking / Virtualization
- **Criticality:** Critical — Proposed Classification
- **Lifecycle Status:** Active — Pending Current-State Verification

### Ownership

| Responsibility | Assigned Role |
|---|---|
| **Service Owner** | Internal IT |
| **Technical Owner** | Network Administrator |
| **Primary Administrator** | Network Administrator |
| **Support Team** | Internal IT |

These responsibilities are simulated for the TTT environment.

### Business Criticality

The virtual networking infrastructure connects TTT's servers, workstations, firewall, and router.

A failure could affect:

- Active Directory connectivity
- DNS resolution
- Employee workstation access
- Administrative access
- Inter-subnet routing
- Internet connectivity
- Infrastructure troubleshooting
- Security policy enforcement

The scope of an outage depends on which network segment or supporting component fails.

---

## 3. Technical Specifications

### General Information

| Attribute | Value |
|---|---|
| **Network Infrastructure Name** | TTT Virtual Networks |
| **Virtualization Platform** | Microsoft Hyper-V |
| **Network Firewall** | FW01 — OPNsense |
| **Internal Router** | RTR01 — VyOS |
| **Documented Network Segments** | Five |
| **IP Protocol** | IPv4 |
| **Internal Addressing** | Private IPv4 |
| **Routing Architecture** | VyOS Internal Routing / OPNsense External Firewall |
| **Virtual Switch Names** | Pending Verification |
| **VLAN Configuration** | Pending Verification |
| **DHCP Configuration** | Pending Verification |
| **DNS Infrastructure** | Active Directory DNS — Configuration Pending Verification |

### Network Segment Inventory

| Network | Subnet | Gateway / Interface | Purpose |
|---|---|---|---|
| WAN | Pending Verification | FW01 WAN: Last Documented `192.168.1.176` | External connectivity |
| Transit | `10.10.10.0/24` | FW01: `10.10.10.1`; RTR01: `10.10.10.2` | Firewall-to-router connectivity |
| Servers | `10.20.10.0/24` | RTR01: `10.20.10.1` | Server infrastructure |
| Clients | `10.20.20.0/24` | RTR01: `10.20.20.1` | Employee workstations |
| Management | `10.20.30.0/24` | RTR01: `10.20.30.1` | Administrative systems |

The WAN address is a previously documented value and may have changed.

### Network Device Inventory

| Device | Platform | Documented Addresses | Function |
|---|---|---|---|
| FW01 | OPNsense | WAN: `192.168.1.176` (historical); Transit: `10.10.10.1` | Firewall / External Connectivity |
| RTR01 | VyOS | `10.10.10.2`, `10.20.10.1`, `10.20.20.1`, `10.20.30.1` | Internal Routing |

### Connected System Inventory

| System | Network | IP Address | Purpose |
|---|---|---|---|
| DC01 | Servers | `10.20.10.10` | Domain Controller / DNS |
| DC02 | Servers | `10.20.10.11` | Additional Domain Controller |
| CLIENT01 | Clients | `10.20.20.10` | Employee Workstation |
| MGMT01 | Management | `10.20.30.10` | Administrative Workstation |

### Hardware / Virtual Resources

| Resource | Configuration |
|---|---|
| **Virtualization Host** | Microsoft Hyper-V |
| **Virtual Switch Count** | Pending Verification |
| **Virtual Switch Types** | Pending Verification |
| **Physical Network Adapters** | Pending Verification |
| **Virtual Network Adapters** | Pending Inventory |
| **VLAN IDs** | Pending Verification |
| **Network Redundancy** | Not Documented |

### Virtual Switch Architecture

The documented logical network design requires connectivity for the following segments:

- WAN
- Transit
- Servers
- Clients
- Management

The actual Hyper-V virtual switch names, switch types, and adapter assignments must be collected from the host.

A logical network segment does not necessarily correspond to a dedicated virtual switch. The implementation may use separate switches, VLANs, or other supported networking arrangements.

### Configuration Verification

Run on the Hyper-V host:

```powershell
Get-VMSwitch |
Select-Object Name,SwitchType,NetAdapterInterfaceDescription
```

Review virtual machine network adapters:

```powershell
Get-VMNetworkAdapter -All |
Select-Object VMName,Name,SwitchName,MacAddress
```

Review configured VLAN information:

```powershell
Get-VM | Get-VMNetworkAdapterVlan
```

**Verification Status:** Not Yet Completed

---

## 4. Installed Roles, Services & Software

### Network Infrastructure Components

| Component | Purpose | Configuration Status |
|---|---|---|
| Hyper-V Virtual Switches | Virtual network connectivity | Previously Configured |
| OPNsense | Firewall and NAT | Previously Configured |
| VyOS | Internal routing | Previously Configured |
| Active Directory DNS | Domain name resolution | Previously Practiced |
| IPv4 Routing | Inter-subnet communication | Previously Documented |
| Outbound NAT | External network connectivity | Previously Practiced |

### Network Services

| Service | Purpose | Status |
|---|---|---|
| Internal Routing | Communication between TTT subnets | Pending Verification |
| External Routing | Communication with upstream network | Pending Verification |
| Network Address Translation | Translates authorized outbound traffic | Pending Verification |
| DNS | Resolves required host and domain names | Pending Verification |
| DHCP | Assigns IP configurations where implemented | Not Documented |
| Firewall Filtering | Enforces network access policies | Pending Verification |

### Administrative Tools

| Tool | Purpose |
|---|---|
| Hyper-V Manager | Virtual switch and VM adapter administration |
| PowerShell | Hyper-V network configuration and diagnostics |
| OPNsense Web Interface | Firewall, NAT, and interface management |
| VyOS CLI | Router configuration and diagnostics |
| Windows Network Utilities | Connectivity and DNS troubleshooting |

---

## 5. Configuration Baseline

### Approved Configuration

The intended virtual network baseline includes:

- WAN connectivity to the upstream network
- Transit network `10.10.10.0/24`
- Server network `10.20.10.0/24`
- Client network `10.20.20.0/24`
- Management network `10.20.30.0/24`
- FW01 connected to WAN and transit networks
- RTR01 connected to transit and internal networks
- Appropriate routes between internal networks
- Appropriate default routing toward FW01
- Approved outbound NAT
- Appropriate firewall access controls
- DNS connectivity to domain controllers
- Restricted management access

This is the proposed configuration baseline. Formal approval has not been recorded.

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| WAN Connectivity | Operational | Previously Configured | Pending Verification |
| Transit Network | `10.10.10.0/24` | Previously Documented | Pending Verification |
| Server Network | `10.20.10.0/24` | Previously Documented | Pending Verification |
| Client Network | `10.20.20.0/24` | Previously Documented | Pending Verification |
| Management Network | `10.20.30.0/24` | Previously Documented | Pending Verification |
| FW01 Transit Address | `10.10.10.1` | Previously Documented | Pending Verification |
| RTR01 Transit Address | `10.10.10.2` | Previously Documented | Pending Verification |
| Server Gateway | `10.20.10.1` | Previously Documented | Pending Verification |
| Client Gateway | `10.20.20.1` | Previously Documented | Pending Verification |
| Management Gateway | `10.20.30.1` | Previously Documented | Pending Verification |
| Default Routing | Appropriate upstream route | Unknown | Pending Verification |
| Internal Routing | Required subnets reachable | Previously Practiced | Pending Verification |
| Outbound NAT | Approved traffic translated | Previously Practiced | Pending Verification |
| Firewall Rules | Match approved access policy | Unknown | Pending Verification |
| Virtual Switch Assignments | Match documented topology | Unknown | Pending Verification |
| DNS Connectivity | Domain services resolve | Unknown | Pending Verification |

### Configuration Policies

Potentially applicable policies include:

- IP addressing standards
- Network segmentation standards
- Firewall access policies
- Router configuration standards
- Virtual switch change management
- Administrative access restrictions
- Network logging
- Network backup and recovery
- Infrastructure change authorization

### Configuration Verification

**Last Verified:** Not Yet Verified

**Verification Method:** Hyper-V PowerShell, OPNsense, VyOS CLI, Windows Network Diagnostics

**Verification Result:** Not Assessed

**Notes:**

Previous TTT networking activities included configuring virtual networks, routing, firewall connectivity, and outbound NAT.

The current configuration must be verified against the live environment.

---

## 6. Relationships & Dependencies

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| CI-001 — DC01 | Provides Connectivity To | Domain controller |
| CI-002 — DC02 | Provides Connectivity To | Additional domain controller |
| CI-003 — FW01 | Implemented By | External firewall infrastructure |
| CI-004 — RTR01 | Implemented By | Internal routing infrastructure |
| CI-005 — MGMT01 | Provides Connectivity To | Management workstation |
| CI-006 — CLIENT01 | Provides Connectivity To | Employee workstation |
| CI-007 — Hyper-V Host | Hosted On | Virtual networking platform |
| CI-008 — Active Directory Domain | Supports | Domain communication and DNS |

### Upstream Dependencies

TTT Virtual Networks depends on:

- Hyper-V host availability
- Hyper-V virtual switch configuration
- Virtual network adapter assignments
- FW01 availability
- RTR01 availability
- Correct IP addressing
- Routing configuration
- Physical or upstream network connectivity for WAN access

### Downstream Dependencies

Services and systems relying on the virtual networks include:

- Active Directory authentication
- DNS
- Domain controller replication
- Employee workstation connectivity
- Remote server administration
- Internet access
- IT support troubleshooting
- Infrastructure monitoring

### Dependency Diagram

```text
                         Internet
                            |
                            v
                    Upstream Network
                            |
                            v
                     FW01 (OPNsense)
                   WAN: 192.168.1.176*
                   Transit: 10.10.10.1
                            |
                     TRANSIT NETWORK
                      10.10.10.0/24
                            |
                            v
                       RTR01 (VyOS)
                       10.10.10.2
                            |
              +-------------+-------------+
              |             |             |
              v             v             v
          SERVERS         CLIENTS      MANAGEMENT
       10.20.10.0/24  10.20.20.0/24  10.20.30.0/24
              |             |             |
         +----+----+        |             |
         |         |        |             |
         v         v        v             v
        DC01      DC02   CLIENT01       MGMT01
      10.20.10.10       10.20.20.10    10.20.30.10
                 10.20.10.11

* Last documented WAN address; current value unverified.
```

All depicted virtual machines are documented as running within the TTT Hyper-V environment.

**Reference:** [Network Topology](../../../Infrastructure/Networking/Network-Topology.md)

### Impact of CI Failure

The impact depends on the affected component.

**WAN Failure**

- External connectivity may be interrupted.
- Internal routing may remain available.

**Transit Network Failure**

- Communication between FW01 and RTR01 may stop.
- Internal systems may lose external connectivity.

**Server Network Failure**

- Workstations may lose access to domain controllers.
- DNS and authentication services may become unreachable from other networks.

**Client Network Failure**

- Employee workstations may lose network connectivity.

**Management Network Failure**

- Administrators may lose remote access to infrastructure.

**Hyper-V Networking Failure**

- Multiple virtual network segments and connected systems may be affected.

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Hyper-V Network Administration | Authorized Virtualization Administrators | Administrative |
| Firewall Administration | Network Administrator | Administrative |
| Router Administration | Network Administrator | Administrative |
| Standard Employee Access | Domain Users | Approved Network Services |
| Management Network Access | Authorized IT Personnel | Restricted Administrative Access |

Actual access permissions require verification.

### Security Controls

Recommended controls include:

- Network segmentation
- Firewall filtering
- Restricted management access
- Least-privilege administration
- Secure router administration
- Secure firewall administration
- Controlled virtual switch changes
- Logging of relevant network events
- Protected network configuration backups
- Review of inter-subnet access policies

### Network Segmentation Policy

| Source Network | Destination Network | Intended Access |
|---|---|---|
| Clients | Servers | Required domain and business services |
| Management | Servers | Authorized administration |
| Clients | Management | Restricted unless explicitly approved |
| Servers | External Network | Approved outbound services |
| Clients | External Network | Approved outbound services |
| Management | Network Devices | Authorized administration |

These are proposed policy objectives, not confirmed firewall rules.

Network separation by subnet does not automatically prevent traffic between those subnets. Enforcement requires appropriate firewall or access-control configuration.

### Security Review

**Last Security Review:** Not Recorded

**Security Status:** Not Assessed

### Security Notes

The management network should be treated as a privileged administrative segment.

Changes to virtual switches, routing, NAT, and firewall rules should be documented and reviewed.

---

## 8. Monitoring & Maintenance

### Monitoring Configuration

| Monitoring Item | Tool / Method | Expected Condition |
|---|---|---|
| Virtual Switches | Hyper-V PowerShell | Correctly Configured |
| VM Network Adapters | Hyper-V PowerShell | Connected to Intended Networks |
| WAN Interface | OPNsense | Operational |
| Transit Network | Ping / OPNsense / VyOS | Operational |
| Internal Routing | VyOS CLI | Required Routes Present |
| Firewall Rules | OPNsense | Match Approved Policy |
| NAT | OPNsense | Approved Traffic Translated |
| DNS | Windows Network Diagnostics | Required Records Resolve |
| Network Connectivity | Ping / Traceroute | Required Destinations Reachable |
| Network Logs | OPNsense / VyOS | Reviewed |

No automated monitoring deployment is confirmed.

### Maintenance Activities

- Review virtual switch assignments.
- Verify interface addressing.
- Verify routing tables.
- Review firewall rules.
- Review NAT configuration.
- Test required connectivity.
- Review DNS functionality.
- Review network logs.
- Back up network device configurations.
- Update network diagrams after approved changes.

### Maintenance Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Network Administrator

**Last Maintenance:** Not Recorded

**Next Planned Maintenance:** Not Scheduled

### Diagnostic Procedures

**Hyper-V Virtual Switch Inventory**

```powershell
Get-VMSwitch
```

**Virtual Network Adapter Inventory**

```powershell
Get-VMNetworkAdapter -All
```

**Windows Network Configuration**

Run from CLIENT01 or MGMT01:

```powershell
Get-NetIPConfiguration
```

**Test Client Gateway**

From CLIENT01:

```powershell
Test-Connection 10.20.20.1 -Count 4
```

**Test Server Connectivity**

From CLIENT01:

```powershell
Test-Connection 10.20.10.10 -Count 4
```

**Test Management Connectivity**

From an authorized system:

```powershell
Test-Connection 10.20.30.10 -Count 4
```

**DNS Verification**

```powershell
Resolve-DnsName technicaltechnotech.com
```

**VyOS Routing Verification**

From RTR01 operational mode:

```bash
show ip route
```

**OPNsense Firewall Verification**

Review:

- Interfaces
- Routing
- Firewall Rules
- Outbound NAT
- Gateway Status
- Firewall Logs

A failed ping does not always indicate a routing failure; ICMP may be blocked by firewall policy.

**Execution Status:** Procedures Provided — Results Not Yet Recorded

---

## 9. Backup & Recovery

### Backup Configuration

**Backup Required:** Yes — Recommended

**Backup Method:** Network Configuration Exports and Infrastructure Documentation

**Backup Frequency:** Not Yet Established

**Backup Destination:** Pending Verification

**Last Successful Backup:** Not Recorded

### Recovery Information

**Recovery Procedure:** Pending Documentation

**Recovery Dependencies:**

- Hyper-V host
- Virtual switch configuration
- Virtual machine network adapter assignments
- FW01 configuration
- RTR01 configuration
- IP addressing documentation
- Network topology documentation
- Authorized administrative access

**Recovery Testing:** Not Recorded

### Recovery Considerations

A network recovery procedure should account for:

1. Identifying the failed component or network segment.
2. Verifying Hyper-V host availability.
3. Restoring required virtual switches.
4. Restoring virtual machine network adapter assignments.
5. Restoring FW01 configuration if necessary.
6. Restoring RTR01 configuration if necessary.
7. Verifying IP addressing.
8. Verifying connected and default routes.
9. Verifying firewall and NAT behavior.
10. Testing connectivity between required networks.
11. Verifying DNS and Active Directory access.
12. Updating the CI record.

Recovery procedures should distinguish between network connectivity failures and failures of the services hosted on connected systems.

---

## 10. Configuration History

Track significant changes affecting TTT Virtual Networks.

| Date | Change ID | Description | Result |
|---|---|---|---|
| Not Recorded | N/A | Initial virtual networking deployment | Previously Documented |
| Not Recorded | N/A | WAN and transit network configuration | Previously Documented |
| Not Recorded | N/A | Server network configuration | Previously Documented |
| Not Recorded | N/A | Client network configuration | Previously Documented |
| Not Recorded | N/A | Management network configuration | Previously Documented |
| Not Recorded | N/A | VyOS routing configuration | Previously Practiced |
| Not Recorded | N/A | OPNsense outbound NAT configuration | Previously Practiced |

### Current Configuration Summary

TTT Virtual Networks is documented as a segmented virtual network environment hosted on Microsoft Hyper-V.

The architecture includes:

- WAN connectivity through FW01
- Transit connectivity between FW01 and RTR01
- Server network `10.20.10.0/24`
- Client network `10.20.20.0/24`
- Management network `10.20.30.0/24`

RTR01 provides internal routing, while FW01 provides the external firewall boundary.

The current virtual switch assignments, routing, NAT, firewall policies, and network health require verification.

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

- [Network Topology](../../../Infrastructure/Networking/Network-Topology.md)
- [Networking Overview](../../../Infrastructure/Networking/README.md)
- [OPNsense Infrastructure](../../../Infrastructure/Networking/OPNsense/README.md)
- [VyOS Infrastructure](../../../Infrastructure/Networking/VyOS/README.md)
- [Hyper-V Infrastructure](../../../Infrastructure/Virtualization/Hyper-V/README.md)
- [Domain Architecture](../../../Infrastructure/Active-Directory/Domain-Architecture.md)
- [FW01 Configuration Item](CI-003-FW01.md)
- [RTR01 Configuration Item](CI-004-RTR01.md)
- [Hyper-V Host Configuration Item](../Servers/CI-007-Hyper-V-Host.md)

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Virtual Switch Inventory | Documented | Not Yet Collected | Pending |
| VM Adapter Assignments | Match Network Architecture | Not Yet Collected | Pending |
| WAN Connectivity | Operational | Not Yet Collected | Pending |
| Transit Network | `10.10.10.0/24` | Not Yet Collected | Pending |
| Server Network | `10.20.10.0/24` | Not Yet Collected | Pending |
| Client Network | `10.20.20.0/24` | Not Yet Collected | Pending |
| Management Network | `10.20.30.0/24` | Not Yet Collected | Pending |
| FW01 Transit Address | `10.10.10.1` | Not Yet Collected | Pending |
| RTR01 Transit Address | `10.10.10.2` | Not Yet Collected | Pending |
| Server Gateway | `10.20.10.1` | Not Yet Collected | Pending |
| Client Gateway | `10.20.20.1` | Not Yet Collected | Pending |
| Management Gateway | `10.20.30.1` | Not Yet Collected | Pending |
| Inter-Subnet Routing | Required Traffic Reachable | Not Yet Collected | Pending |
| Outbound NAT | Approved Traffic Translated | Not Yet Collected | Pending |
| Firewall Rules | Match Approved Policy | Not Yet Collected | Pending |
| DNS Connectivity | Required Records Resolve | Not Yet Collected | Pending |
| External Connectivity | Approved Connections Succeed | Not Yet Collected | Pending |

### Supporting Evidence

No evidence files have been attached to this record.

Recommended evidence:

- Hyper-V virtual switch inventory
- Virtual machine network adapter assignments
- OPNsense interface configuration
- OPNsense routing table
- OPNsense firewall rules
- OPNsense outbound NAT configuration
- VyOS interface configuration
- VyOS routing table
- Windows IP configuration
- DNS test results
- Connectivity test results
- Updated network topology diagram

Only verified, sanitized evidence should be added to the repository.

Do not publish passwords, private keys, API credentials, or other sensitive information.

### Verification Summary

**Verification Status:** Not Yet Completed

The documented virtual network architecture must be compared against the live Hyper-V, OPNsense, and VyOS configurations.

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

Before retiring or redesigning the virtual networking infrastructure:

1. Identify all connected systems.
2. Review service dependencies.
3. Document current network addressing.
4. Export firewall and router configurations.
5. Document virtual switch assignments.
6. Identify replacement network infrastructure.
7. Plan and authorize the migration.
8. Update network device configurations.
9. Migrate connected systems.
10. Verify required connectivity.
11. Update CI relationships.
12. Decommission unused network components.

### Lifecycle Notes

No retirement activity is currently documented.

---

## 14. Lessons Learned

### What I Learned

**1. Virtual Networking**

Hyper-V virtual switches provide connectivity between virtual machines and other networks.

**2. Network Segmentation**

Separating servers, clients, and management systems into different subnets improves organization and creates opportunities for access control.

**3. Routing**

RTR01 enables communication between internal network segments.

**4. Firewall Security**

FW01 provides the external security boundary and supports traffic filtering.

**5. Network Address Translation**

NAT allows authorized internal systems to communicate with external networks through translated addressing.

**6. Infrastructure Dependencies**

Network infrastructure supports many other IT services, including authentication, DNS, endpoint administration, and remote management.

**7. Service Configuration Management**

Documenting the virtual network architecture helps identify relationships between infrastructure components and supports troubleshooting, change planning, and recovery.

### Skills Practiced

- ITIL 4 Service Configuration Management
- Microsoft Hyper-V Virtual Networking
- IPv4 Addressing
- Subnetting
- Network Segmentation
- VyOS Routing
- OPNsense Firewall Administration
- Network Address Translation
- DNS Troubleshooting
- Network Connectivity Testing
- Infrastructure Dependency Mapping
- Configuration Baseline Design
- Technical Documentation

### Improvement Opportunities

- Verify all virtual switch names.
- Document switch types.
- Verify virtual network adapter assignments.
- Record VLAN configuration, if applicable.
- Verify routing tables.
- Verify outbound NAT.
- Review firewall policies.
- Test connectivity between required networks.
- Document network monitoring.
- Establish network configuration backups.
- Update the topology diagram.
- Link future Jira records to CI-009.

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

CI-009 has been documented using the Technical Techno Tech Configuration Item Template.

The record identifies the logical virtual network infrastructure, network segments, addressing, routing relationships, dependencies, security requirements, and intended configuration baseline.

Outstanding activities include:

- Verify Hyper-V virtual networking.
- Confirm all network segments.
- Verify firewall and router interfaces.
- Verify routing and NAT.
- Review network access controls.
- Test required connectivity.
- Document backup and recovery procedures.
- Collect technical evidence.
- Complete the formal CI review.

**Overall Record Status:** Draft — Awaiting Configuration Verification

---

## 16. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial TTT Virtual Networks configuration item record aligned with the TTT CI template |

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations and infrastructure relationships are based on previously documented lab activities. Current verification results are not assumed.

Business ownership, administrative responsibilities, and operational processes are simulated for educational and portfolio purposes.
