# Technical Techno Tech — Network Topology

**Organization:** Technical Techno Tech (TTT)  
**Document Type:** Infrastructure Architecture  
**Document ID:** INF-NET-001  
**Version:** 1.0  
**Status:** Existing Lab — Configuration Verification Ongoing  
**Infrastructure Platform:** Microsoft Hyper-V  
**Firewall Platform:** OPNsense  
**Routing Platform:** VyOS  
**Network Type:** Segmented Virtual Enterprise Network  
**Last Reviewed:** Pending Verification

---

## 1. Purpose

This document describes the network architecture supporting Technical Techno Tech's internal IT infrastructure.

It establishes a central reference for:

- Network topology
- Network devices
- IP addressing
- Subnet segmentation
- Default gateways
- Routing
- Firewall services
- Network Address Translation (NAT)
- Virtual network connectivity
- Active Directory network dependencies
- Network verification and troubleshooting
- Infrastructure relationships

The document also supports future network expansion, maintenance, incident investigation, and change management.

---

## 2. Environment Overview

Technical Techno Tech operates a virtualized network environment designed to simulate a small business infrastructure.

The environment uses:

- **Microsoft Hyper-V:** Virtual machine hosting and virtual networking
- **OPNsense:** Firewall and outbound NAT
- **VyOS:** Internal network routing
- **Windows Server:** Domain services and DNS
- **Windows 11:** Administrative and employee workstations

The network separates servers, employee workstations, and IT management systems into distinct IP subnets.

### Design Objectives

1. Establish a structured internal network.
2. Separate systems according to their operational purpose.
3. Provide connectivity between authorized network segments.
4. Route external traffic through a firewall.
5. Support Active Directory authentication and DNS.
6. Enable centralized infrastructure administration.
7. Support realistic troubleshooting scenarios.
8. Maintain clear technical documentation.

---

## 3. Logical Network Topology

```text
                         INTERNET
                            |
                            |
                    External Network
                       192.168.1.0/24
                            |
                            |
                  +-------------------+
                  | FW01              |
                  | OPNsense Firewall |
                  |-------------------|
                  | WAN: 192.168.1.176|
                  | LAN: 10.10.10.1   |
                  +-------------------+
                            |
                            |
                    TRANSIT NETWORK
                      10.10.10.0/24
                            |
                            |
                  +-------------------+
                  | RTR01             |
                  | VyOS Router       |
                  |-------------------|
                  | Transit:          |
                  | 10.10.10.2        |
                  +-------------------+
                            |
             +--------------+--------------+
             |              |              |
             |              |              |
             v              v              v
       SERVER NETWORK  CLIENT NETWORK  MANAGEMENT NETWORK
       10.20.10.0/24   10.20.20.0/24    10.20.30.0/24
             |              |              |
       GW: 10.20.10.1  GW: 10.20.20.1  GW: 10.20.30.1
             |              |              |
       +-----+-----+        |              |
       |           |        |              |
       v           v        v              v
      DC01        DC02    CLIENT01        MGMT01
   10.20.10.10 10.20.10.11 10.20.20.10  10.20.30.10

      AD DS      AD DS     Windows 11      Windows 11
      DNS        Domain    Employee        IT Admin
                 Controller Workstation    Workstation
```

### Architecture Summary

Network traffic between internal subnets is routed through RTR01.

Traffic requiring external connectivity is forwarded toward FW01.

FW01 provides the firewall and outbound NAT functions used by the lab.

The virtual networking infrastructure is hosted on Hyper-V.

**Documentation Note:** This diagram represents the previously documented TTT logical design. The current running configuration should be verified against the diagram.

---

## 4. Network Addressing Plan

### 4.1 Subnet Inventory

| Network ID | Network Name | Subnet | Subnet Mask | Purpose |
|---|---|---|---|---|
| NET-001 | Transit | `10.10.10.0/24` | `255.255.255.0` | Firewall-to-router connectivity |
| NET-002 | Servers | `10.20.10.0/24` | `255.255.255.0` | Server infrastructure |
| NET-003 | Clients | `10.20.20.0/24` | `255.255.255.0` | Employee workstations |
| NET-004 | Management | `10.20.30.0/24` | `255.255.255.0` | IT administration |

### 4.2 Default Gateways

| Network | Default Gateway | Device |
|---|---|---|
| Servers | `10.20.10.1` | RTR01 |
| Clients | `10.20.20.1` | RTR01 |
| Management | `10.20.30.1` | RTR01 |

The transit network uses the following router-facing addresses:

| Device | IP Address |
|---|---|
| FW01 | `10.10.10.1` |
| RTR01 | `10.10.10.2` |

### 4.3 Addressing Strategy

The environment uses a structured addressing plan.

- `10.10.10.0/24` — Network transit
- `10.20.10.0/24` — Servers
- `10.20.20.0/24` — Clients
- `10.20.30.0/24` — Management

This design simplifies network administration and troubleshooting.

Static IP addressing is appropriate for infrastructure systems requiring consistent network identities.

Dynamic addressing may be introduced through DHCP where appropriate.

---

## 5. Network Device Inventory

| Device | Hostname | Platform | IP Address | Function |
|---|---|---|---|---|
| Firewall | FW01 | OPNsense | `10.10.10.1` | Firewall and NAT |
| Router | RTR01 | VyOS | `10.10.10.2` | Internal routing |
| Domain Controller | DC01 | Windows Server | `10.20.10.10` | AD DS and DNS |
| Domain Controller | DC02 | Windows Server Core | `10.20.10.11` | Additional writable DC |
| Client | CLIENT01 | Windows 11 | `10.20.20.10` | Employee workstation |
| Management | MGMT01 | Windows 11 | `10.20.30.10` | Administrative workstation |

### 5.1 External Firewall Interface

| Property | Value |
|---|---|
| Device | FW01 |
| Interface | WAN |
| Previously Documented Address | `192.168.1.176` |
| Upstream Gateway | Pending Verification |
| Address Assignment Method | Pending Verification |

### 5.2 Configuration Verification

The following properties should be checked against the running infrastructure:

- Interface assignments
- Interface IP addresses
- Virtual switch connections
- Default routes
- Static routes
- Firewall rules
- NAT rules
- DNS configuration
- Current device availability

---

## 6. Firewall Architecture — FW01

### 6.1 Overview

FW01 is the OPNsense firewall used by Technical Techno Tech.

Its primary responsibilities include:

- Providing the boundary between internal and external networks
- Controlling traffic through firewall rules
- Performing outbound NAT
- Supporting external network connectivity
- Providing network diagnostic capabilities

### 6.2 Interface Configuration

| Interface | Network | Address | Purpose |
|---|---|---|---|
| WAN | External | `192.168.1.176` | Upstream connectivity |
| LAN | Transit | `10.10.10.1/24` | Connection to RTR01 |

Actual interface names and assignments should be verified in OPNsense.

### 6.3 Outbound NAT

Outbound NAT allows internal systems to communicate with external networks using the firewall's external interface.

Previously documented lab work included configuring outbound NAT and confirming internet connectivity from CLIENT01.

The specific NAT rule configuration should be captured separately.

### 6.4 Firewall Rules

Firewall rules determine which traffic is permitted or denied.

Important considerations include:

- Internal network access to external services
- Administrative access to FW01
- Required infrastructure communication
- Unnecessary service exposure
- Logging of relevant denied traffic

**Current Rule Inventory:** Pending Documentation

### 6.5 Firewall Verification

Review the following in OPNsense:

1. Interface assignments
2. Interface addresses
3. Routing configuration
4. Outbound NAT configuration
5. Firewall rules
6. Firewall logs
7. Connectivity diagnostics

Record screenshots or sanitized configuration exports as evidence.

---

## 7. Router Architecture — RTR01

### 7.1 Overview

RTR01 is the VyOS router responsible for connectivity between TTT's internal network segments.

### 7.2 Router Interface Addressing

| Network | Router Address | Purpose |
|---|---|---|
| Transit | `10.10.10.2/24` | Connection to FW01 |
| Servers | `10.20.10.1/24` | Server gateway |
| Clients | `10.20.20.1/24` | Client gateway |
| Management | `10.20.30.1/24` | Management gateway |

### 7.3 Routing Responsibilities

RTR01 provides:

- Routing between internal subnets
- Default gateway services for internal systems
- Forwarding toward FW01 for external connectivity

### 7.4 Default Route

The intended external forwarding path is:

```text
Internal Networks
       |
       v
RTR01
       |
       v
10.10.10.1
       |
       v
FW01
       |
       v
External Network
```

The configured default route should be verified in VyOS.

### 7.5 Example VyOS Verification Commands

Inspect interfaces:

```text
show interfaces
```

Inspect the IPv4 routing table:

```text
show ip route
```

Inspect configuration:

```text
show configuration
```

Test transit connectivity:

```text
ping 10.10.10.1
```

**Execution Status:** Reference Commands — Results Not Included

### 7.6 Routing Verification Checklist

- [ ] Transit interface configured
- [ ] Server gateway configured
- [ ] Client gateway configured
- [ ] Management gateway configured
- [ ] Connected routes present
- [ ] Default route verified
- [ ] Firewall transit connectivity tested
- [ ] Server network reachable
- [ ] Client network reachable
- [ ] Management network reachable

---

## 8. Server Network

### 8.1 Network Information

| Property | Value |
|---|---|
| Network | Servers |
| Subnet | `10.20.10.0/24` |
| Gateway | `10.20.10.1` |
| Router | RTR01 |
| Purpose | Centralized server infrastructure |

### 8.2 Connected Systems

| Hostname | IP Address | Function |
|---|---|---|
| DC01 | `10.20.10.10` | Domain controller and DNS |
| DC02 | `10.20.10.11` | Additional domain controller |

### 8.3 Network Requirements

The server network must support authorized communication for:

- DNS
- Kerberos authentication
- LDAP
- SMB
- RPC
- Active Directory replication
- Administrative management

Firewall policies should permit required traffic while restricting unnecessary access.

---

## 9. Client Network

### 9.1 Network Information

| Property | Value |
|---|---|
| Network | Clients |
| Subnet | `10.20.20.0/24` |
| Gateway | `10.20.20.1` |
| Router | RTR01 |
| Purpose | Employee workstation connectivity |

### 9.2 Connected Systems

| Hostname | IP Address | Function |
|---|---|---|
| CLIENT01 | `10.20.20.10` | Windows 11 employee workstation |

### 9.3 Network Requirements

CLIENT01 requires connectivity to:

- Domain controllers
- DNS
- Approved internal services
- External services when authorized

### 9.4 Previously Documented Verification

Previous lab work established outbound internet connectivity from CLIENT01 after NAT configuration.

Current connectivity should be retested before presenting it as an up-to-date operational result.

---

## 10. Management Network

### 10.1 Network Information

| Property | Value |
|---|---|
| Network | Management |
| Subnet | `10.20.30.0/24` |
| Gateway | `10.20.30.1` |
| Router | RTR01 |
| Purpose | IT infrastructure administration |

### 10.2 Connected Systems

| Hostname | IP Address | Function |
|---|---|---|
| MGMT01 | `10.20.30.10` | IT administrative workstation |

### 10.3 Administrative Responsibilities

MGMT01 supports administrative tasks involving:

- Active Directory
- Windows Server
- DNS
- Group Policy
- Remote administration
- Infrastructure troubleshooting

### 10.4 Security Considerations

Management systems should have access appropriate to their administrative responsibilities.

Recommended controls include:

- Restricted administrative access
- Least privilege
- Strong authentication
- Logging
- Appropriate firewall restrictions
- Separation of administrative and standard user activities

The presence of a dedicated management subnet does not by itself prove that access restrictions are enforced.

---

## 11. Hyper-V Virtual Networking

### 11.1 Overview

The TTT network is hosted in Microsoft Hyper-V.

Hyper-V virtual switches provide connectivity between virtual machines and their assigned network segments.

### 11.2 Required Logical Segments

| Segment | Connected Systems |
|---|---|
| External | FW01 WAN |
| Transit | FW01 LAN, RTR01 transit |
| Servers | RTR01, DC01, DC02 |
| Clients | RTR01, CLIENT01 |
| Management | RTR01, MGMT01 |

### 11.3 Virtual Switch Inventory

| Logical Segment | Hyper-V Switch Name | Switch Type | Verified |
|---|---|---|---|
| External | Pending | Pending | No |
| Transit | Pending | Pending | No |
| Servers | Pending | Pending | No |
| Clients | Pending | Pending | No |
| Management | Pending | Pending | No |

The logical segments are documented, but exact Hyper-V switch names and types must be obtained from the current configuration.

### 11.4 Hyper-V Verification Commands

List virtual switches:

```powershell
Get-VMSwitch
```

List virtual machine network adapters:

```powershell
Get-VMNetworkAdapter -VMName "FW01"
Get-VMNetworkAdapter -VMName "RTR01"
Get-VMNetworkAdapter -VMName "DC01"
Get-VMNetworkAdapter -VMName "DC02"
Get-VMNetworkAdapter -VMName "CLIENT01"
Get-VMNetworkAdapter -VMName "MGMT01"
```

Review switch assignments:

```powershell
Get-VMNetworkAdapter -VMName "RTR01" |
Select-Object VMName,Name,SwitchName,MacAddress
```

**Execution Status:** Reference Commands — Results Not Included

### 11.5 Virtual Networking Verification

- [ ] Hyper-V switches inventoried
- [ ] Switch types documented
- [ ] FW01 interfaces mapped
- [ ] RTR01 interfaces mapped
- [ ] DC01 connected to server segment
- [ ] DC02 connected to server segment
- [ ] CLIENT01 connected to client segment
- [ ] MGMT01 connected to management segment
- [ ] Network connectivity tested

---

## 12. DNS Architecture

### 12.1 Overview

DNS supports name resolution and Active Directory domain controller discovery.

### 12.2 Active Directory Domain

**Domain:** `technicaltechnotech.com`

### 12.3 DNS Infrastructure

| Server | Address | DNS Responsibility |
|---|---|---|
| DC01 | `10.20.10.10` | DNS server |
| DC02 | `10.20.10.11` | DNS configuration to be verified |

### 12.4 DNS Client Configuration

The intended DNS configuration for domain-joined systems should use DNS servers capable of resolving the Active Directory domain.

Actual preferred and alternate DNS settings should be documented from each system.

### 12.5 Example DNS Verification

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

```powershell
Resolve-DnsName technicaltechnotech.com
```

```powershell
Resolve-DnsName -Type SRV _ldap._tcp.dc._msdcs.technicaltechnotech.com
```

### 12.6 DNS Verification Checklist

- [ ] DNS servers identified
- [ ] DNS client addresses verified
- [ ] Domain records resolve
- [ ] Domain controller SRV records resolve
- [ ] Domain controller discovery succeeds
- [ ] External DNS resolution tested where required

---

## 13. Active Directory Network Dependencies

Active Directory requires several network services to function properly.

### 13.1 Key Protocols

| Protocol | Common Port | Purpose |
|---|---|---|
| DNS | TCP/UDP 53 | Name resolution |
| Kerberos | TCP/UDP 88 | Authentication |
| LDAP | TCP/UDP 389 | Directory access |
| LDAPS | TCP 636 | LDAP over TLS, when configured |
| SMB | TCP 445 | File and domain services |
| RPC Endpoint Mapper | TCP 135 | RPC service discovery |
| NTP | UDP 123 | Time synchronization |
| Global Catalog | TCP 3268 | Global Catalog queries |
| Global Catalog over TLS | TCP 3269 | Encrypted Global Catalog queries, when configured |

Additional ports, including dynamic RPC ports, may be required depending on the operation.

### 13.2 Domain Controller Connectivity

Domain controllers must be able to communicate for:

- Directory replication
- DNS
- Authentication
- Time synchronization
- Administrative operations

### 13.3 Workstation Connectivity

Domain-joined workstations must be able to locate and communicate with appropriate domain controllers.

### 13.4 Example Verification

```powershell
nltest /dsgetdc:technicaltechnotech.com
```

```powershell
Test-NetConnection 10.20.10.10 -Port 53
```

```powershell
Test-NetConnection 10.20.10.10 -Port 389
```

```powershell
Test-NetConnection 10.20.10.10 -Port 445
```

These commands test selected connectivity paths and do not replace complete Active Directory health verification.

---

## 14. Routing and Traffic Flow

### 14.1 Client-to-Server Communication

Example: CLIENT01 contacting DC01.

```text
CLIENT01
10.20.20.10
     |
     v
Client Gateway
10.20.20.1
     |
     v
RTR01
     |
     v
Server Network
10.20.10.0/24
     |
     v
DC01
10.20.10.10
```

### 14.2 Management-to-Server Communication

```text
MGMT01
10.20.30.10
     |
     v
Management Gateway
10.20.30.1
     |
     v
RTR01
     |
     v
DC01 / DC02
```

### 14.3 Outbound Internet Communication

```text
CLIENT01
     |
     v
RTR01
     |
     v
FW01
     |
     v
Outbound NAT
     |
     v
External Network
     |
     v
Internet
```

### 14.4 Return Traffic

Successful communication requires a valid return path.

Routing and firewall configuration must support both outbound traffic and the associated responses.

---

## 15. Firewall and Network Security

### 15.1 Security Objectives

- Protect internal infrastructure.
- Restrict unauthorized access.
- Separate management and employee networks.
- Control external connectivity.
- Limit unnecessary services.
- Maintain relevant security logs.
- Support investigation of network incidents.

### 15.2 Proposed Security Controls

| Control | Purpose | Implementation Status |
|---|---|---|
| Network Segmentation | Separate systems by function | Logical Segments Documented |
| Firewall Rules | Restrict traffic | Detailed Rules Pending Review |
| Outbound NAT | Provide external connectivity | Previously Configured |
| Management Access Restrictions | Protect administrative systems | Pending Verification |
| Logging | Support troubleshooting | Pending Verification |
| DNS Security | Protect name resolution | Pending Review |
| Network Monitoring | Detect service issues | Planned |

### 15.3 Security Verification

- [ ] Review firewall rules
- [ ] Review NAT configuration
- [ ] Confirm administrative access restrictions
- [ ] Test permitted communication
- [ ] Test intended denied communication
- [ ] Review relevant logs
- [ ] Document actual results

### Important

Network segmentation and network isolation are different concepts.

Separate IP subnets provide segmentation. Isolation requires appropriate routing and access controls.

---

## 16. Network Verification Plan

### 16.1 Verification Objectives

Confirm that:

1. Devices have the correct addresses.
2. Default gateways are configured.
3. Routing works between required segments.
4. DNS resolves internal resources.
5. Active Directory services are reachable.
6. Outbound NAT works.
7. Firewall policies behave as intended.
8. Administrative connectivity is available.

### 16.2 Verification Matrix

| Test ID | Source | Destination | Test | Result |
|---|---|---|---|---|
| NET-TST-001 | CLIENT01 | `10.20.20.1` | Gateway connectivity | Pending |
| NET-TST-002 | CLIENT01 | DC01 | Server connectivity | Pending |
| NET-TST-003 | CLIENT01 | Domain DNS | Name resolution | Pending |
| NET-TST-004 | MGMT01 | DC01 | Management connectivity | Pending |
| NET-TST-005 | MGMT01 | DC02 | Management connectivity | Pending |
| NET-TST-006 | RTR01 | FW01 | Transit connectivity | Pending |
| NET-TST-007 | CLIENT01 | External network | Internet connectivity | Retest Required |
| NET-TST-008 | CLIENT01 | Domain Controller | DC discovery | Pending |
| NET-TST-009 | DC01 | DC02 | AD replication health | Pending |
| NET-TST-010 | Management Network | Restricted Resource | Firewall policy validation | Pending |

### 16.3 Evidence Requirements

Each completed test should record:

- Test identifier
- Date
- Source device
- Destination
- Test method
- Expected result
- Actual result
- Pass/fail status
- Supporting evidence
- Troubleshooting notes

---

## 17. Troubleshooting Procedures

### 17.1 Initial Investigation

When a network issue occurs:

1. Identify the affected device.
2. Determine the affected service.
3. Confirm the reported symptoms.
4. Review IP addressing.
5. Review the subnet mask.
6. Verify the default gateway.
7. Verify DNS settings.
8. Test local connectivity.
9. Test routing.
10. Review firewall policies.
11. Identify the probable failure point.
12. Document findings.

### 17.2 Windows Troubleshooting Commands

Review IP configuration:

```powershell
ipconfig /all
```

Test gateway:

```powershell
ping 10.20.20.1
```

Trace a route:

```powershell
tracert 10.20.10.10
```

Test DNS:

```powershell
nslookup technicaltechnotech.com
```

Test a TCP service:

```powershell
Test-NetConnection 10.20.10.10 -Port 389
```

Review routing:

```powershell
route print
```

### 17.3 VyOS Troubleshooting

```text
show interfaces
show ip route
ping 10.10.10.1
```

### 17.4 OPNsense Troubleshooting

Review:

- Interface status
- Routing table
- Firewall logs
- NAT rules
- Packet captures where appropriate
- Diagnostic ping and traceroute results

### 17.5 Troubleshooting Documentation

Record:

**Issue:** [Description]

**Affected Systems:** [Systems]

**Symptoms:** [Observed Behavior]

**Investigation:** [Actions Taken]

**Findings:** [Actual Results]

**Root Cause:** [Established Cause or Undetermined]

**Corrective Action:** [Action]

**Verification:** [Actual Result]

**Status:** [Open / Resolved / Escalated]

---

## 18. Common Network Failure Scenarios

| Scenario | Possible Cause | Investigation |
|---|---|---|
| CLIENT01 cannot reach DC01 | Routing or firewall issue | Check gateway, routes, connectivity |
| Domain login fails | DNS or authentication issue | Check DNS and domain controller discovery |
| Internet unavailable | NAT or default route issue | Inspect RTR01 and FW01 |
| MGMT01 cannot manage DC01 | Firewall, DNS, or permissions | Verify network and administrative access |
| DC01 and DC02 cannot replicate | DNS, routing, or RPC issue | Review replication and network connectivity |
| One subnet unreachable | Interface or route failure | Inspect VyOS |
| Incorrect DNS resolution | DNS client configuration | Review configured DNS servers |
| VM loses connectivity | Virtual switch issue | Inspect Hyper-V adapters |
| Intermittent connectivity | Interface, resource, or network issue | Review logs and connectivity tests |

These are potential troubleshooting scenarios, not claims of observed failures.

---

## 19. Network Dependencies

### 19.1 Dependency Overview

| Service | Depends On |
|---|---|
| Active Directory Authentication | DNS, routing, domain controllers |
| Domain Controller Replication | DNS, network connectivity, AD DS |
| Employee Workstation Connectivity | Virtual networking, routing |
| Administrative Access | Management network, routing, authentication |
| Internet Access | Routing, firewall, NAT, upstream connectivity |
| Windows Server Administration | Network connectivity, credentials, management services |

### 19.2 Critical Infrastructure Dependencies

```text
Hyper-V
   |
   +-- Virtual Networking
           |
           +-- FW01
           |     |
           |     +-- External Connectivity
           |
           +-- RTR01
                 |
                 +-- Server Network
                 |     |
                 |     +-- DC01 / DC02
                 |           |
                 |           +-- AD DS
                 |           +-- DNS
                 |
                 +-- Client Network
                 |     |
                 |     +-- CLIENT01
                 |
                 +-- Management Network
                       |
                       +-- MGMT01
```

This dependency representation is logical and does not imply that every dependency has been formally validated.

---

## 20. ITIL 4 Integration

The network infrastructure supports several ITIL 4 practices.

| Practice | Network Application |
|---|---|
| Service Desk | Receives network connectivity reports |
| Incident Management | Restores interrupted network services |
| Problem Management | Investigates recurring network failures |
| Change Enablement | Controls routing and firewall modifications |
| Monitoring and Event Management | Detects network failures and alerts |
| Service Configuration Management | Documents network devices and dependencies |
| Information Security Management | Manages network access controls |
| Knowledge Management | Maintains network troubleshooting articles |
| Continual Improvement | Improves reliability and troubleshooting procedures |

### Example Scenario

**Scenario:** CLIENT01 cannot access the domain controller.

Potential operational workflow:

1. Service Desk logs the issue.
2. Incident Management investigates connectivity.
3. Network diagnostics identify the affected layer.
4. Authorized corrective action restores connectivity.
5. Technical verification confirms service restoration.
6. Knowledge documentation is updated if appropriate.
7. Related configuration records are reviewed.

This is an example workflow, not a completed incident record.

---

## 21. Configuration Management

The network infrastructure should be represented through configuration item records.

### Proposed CI Records

| CI ID | Configuration Item | Type |
|---|---|---|
| CI-001 | FW01 | Firewall |
| CI-002 | RTR01 | Router |
| CI-003 | DC01 | Server |
| CI-004 | DC02 | Server |
| CI-005 | CLIENT01 | Workstation |
| CI-006 | MGMT01 | Workstation |

These IDs are proposed placeholders and must be reconciled with the actual CI register before use.

### Configuration Item Documentation

Each record should include:

- CI identifier
- Name
- Type
- Operational purpose
- Network configuration
- Dependencies
- Relationships
- Current status
- Evidence
- Change history

---

## 22. Change Management

Changes to network infrastructure may affect multiple services.

Examples include:

- Modifying firewall rules
- Changing subnet addresses
- Updating routing configuration
- Changing virtual switch assignments
- Reconfiguring NAT
- Modifying DNS settings
- Introducing new network segments

### Proposed Change Workflow

1. Identify the required change.
2. Assess business and technical impact.
3. Identify affected configuration items.
4. Evaluate risks and dependencies.
5. Obtain applicable authorization.
6. Prepare implementation and recovery plans.
7. Implement the change.
8. Verify the result.
9. Update infrastructure documentation.
10. Review the outcome.

---

## 23. Monitoring and Maintenance

### 23.1 Monitoring Objectives

Potential monitoring activities include:

- Interface availability
- Router reachability
- Firewall availability
- Network latency
- DNS availability
- Domain controller connectivity
- Packet loss
- Network service failures

### 23.2 Proposed Monitoring Matrix

| Component | Metric | Status |
|---|---|---|
| FW01 | Firewall availability | Monitoring Not Verified |
| RTR01 | Router availability | Monitoring Not Verified |
| DC01 | DNS reachability | Monitoring Not Verified |
| DC02 | Domain controller reachability | Monitoring Not Verified |
| CLIENT01 | Network connectivity | Monitoring Not Verified |
| MGMT01 | Administrative connectivity | Monitoring Not Verified |

### 23.3 Maintenance Activities

Potential maintenance includes:

- Reviewing firewall policies
- Reviewing routing configuration
- Checking interface status
- Reviewing relevant logs
- Verifying DNS
- Validating network documentation
- Reviewing configuration changes

Monitoring automation is not claimed as implemented.

---

## 24. Evidence and Documentation Standards

Technical evidence should support actual configuration and verification claims.

### Recommended Evidence

- Hyper-V virtual switch inventory
- Hyper-V network adapter assignments
- OPNsense interface configuration
- OPNsense NAT configuration
- OPNsense firewall rules
- VyOS interface configuration
- VyOS routing table
- Windows IP configuration
- DNS test results
- Domain controller discovery
- Connectivity test results

### Evidence Status

**Configuration Screenshots:** Pending Collection

**Command Output:** Pending Collection

**Network Verification:** Pending

**Firewall Rule Review:** Pending

**Virtual Switch Inventory:** Pending

### Documentation Requirements

Evidence should:

- Reflect the actual environment.
- Include the relevant device or service.
- Be dated where practical.
- Exclude passwords and secrets.
- Avoid exposing unnecessary sensitive information.
- Clearly distinguish successful and failed tests.
- Remain traceable to the documented configuration.

---

## 25. Planned Improvements

Potential future improvements include:

- Formal firewall rule documentation
- Centralized network monitoring
- Syslog collection
- Network configuration backups
- Network security validation
- Automated network health checks
- Additional subnet segmentation
- Expanded network troubleshooting scenarios
- More detailed dependency mapping
- Configuration management automation

These are proposed improvements, not completed changes.

---

## 26. Skills Practiced

This project demonstrates practical exposure to:

- Network architecture
- IP addressing
- Subnetting
- Routing
- Firewall administration
- Network Address Translation
- Network segmentation
- Hyper-V virtual networking
- Windows network administration
- DNS troubleshooting
- Active Directory connectivity
- Network diagnostics
- Network security fundamentals
- Infrastructure documentation
- Service dependency analysis
- ITIL-aligned operational processes

---

## 28. What I Learned

The Technical Techno Tech networking project demonstrates how multiple technologies work together to support business IT infrastructure.

### Key Learning Areas

**1. Network Segmentation**

Separating servers, workstations, and management systems improves network organization and supports more granular access controls.

**2. Routing**

VyOS connects separate IP networks and provides default gateways for internal systems.

**3. Firewall and NAT**

OPNsense controls traffic at the external network boundary and provides outbound NAT.

**4. Virtual Networking**

Hyper-V virtual switches connect virtual machines to their appropriate network segments.

**5. Active Directory Dependencies**

Domain authentication depends on reliable DNS and network communication.

**6. Troubleshooting**

Systematic investigation helps identify whether a failure involves addressing, routing, DNS, firewall policy, or virtual networking.

**7. Documentation**

Accurate network documentation supports maintenance, troubleshooting, change management, and future infrastructure expansion.

---

## 29. Verification Checklist

### Network Architecture

- [ ] Network diagram matches current configuration
- [ ] All network segments documented
- [ ] All network devices identified
- [ ] IP addresses verified
- [ ] Default gateways verified

### Firewall

- [ ] WAN configuration verified
- [ ] LAN configuration verified
- [ ] NAT rules documented
- [ ] Firewall rules reviewed
- [ ] External connectivity tested

### Routing

- [ ] VyOS interfaces verified
- [ ] Connected routes verified
- [ ] Default route verified
- [ ] Internal connectivity tested

### Virtualization

- [ ] Hyper-V switches documented
- [ ] Virtual adapters mapped
- [ ] Network assignments verified

### Windows Infrastructure

- [ ] DC01 network settings verified
- [ ] DC02 network settings verified
- [ ] CLIENT01 network settings verified
- [ ] MGMT01 network settings verified
- [ ] DNS configuration verified
- [ ] Domain controller discovery tested

### Documentation

- [ ] Actual command results captured
- [ ] Screenshots sanitized
- [ ] CI records reviewed
- [ ] Dependencies documented
- [ ] Unverified information identified
- [ ] Change history updated

---

## 30. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial documentation of the TTT network topology, addressing, routing, firewall, virtual networking, and infrastructure dependencies |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This document describes the network architecture associated with the TTT lab.

Previously documented configurations are included for continuity, but their current operational state must be confirmed through actual configuration inspection and testing.

Proposed procedures, verification checklists, future improvements, and illustrative scenarios are not evidence of completed activities.

All published evidence should be obtained from authorized lab systems and sanitized before inclusion in the public GitHub repository.
