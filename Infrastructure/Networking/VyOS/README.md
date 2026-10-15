# Technical Techno Tech — VyOS Router Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Document ID:** INF-NET-003  
**Document Type:** Network Infrastructure Documentation  
**Version:** 1.0  
**Status:** Existing Lab — Verification Ongoing  
**Device:** RTR01  
**Platform:** VyOS  
**Function:** Internal IT  
**ITIL 4 Practice:** Service Configuration Management

---

## 1. Purpose

This document describes the VyOS router supporting Technical Techno Tech's internal network infrastructure.

It provides a centralized reference for:

- Router architecture
- Network interfaces
- IP addressing
- Routing
- Network segmentation
- Default gateways
- Firewall dependencies
- Router administration
- Configuration management
- Monitoring
- Troubleshooting
- Backup and recovery
- Change management

RTR01 provides connectivity between TTT's internal network segments and the OPNsense firewall.

---

## 2. Environment Overview

Technical Techno Tech operates a segmented virtual network using Hyper-V, VyOS, and OPNsense.

### Router Inventory

| Attribute | Configuration |
|---|---|
| Hostname | RTR01 |
| Platform | VyOS |
| Deployment | Virtual Machine |
| Hypervisor | Hyper-V |
| Primary Function | Internal Routing |
| Transit Address | `10.10.10.2` |
| Transit Network | `10.10.10.0/24` |
| Upstream Firewall | FW01 — OPNsense |
| Current VyOS Version | Pending Verification |
| Interface Names | Pending Verification |
| Configuration Backup Status | Pending Verification |

---

## 3. Network Architecture

### 3.1 Logical Topology

```text
                   Internet
                      |
                      v
                 FW01 - OPNsense
                 10.10.10.1
                      |
                      v
                Transit Network
                 10.10.10.0/24
                      |
                      v
                  RTR01 - VyOS
                  10.10.10.2
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
       Servers      Clients    Management
       Network      Network     Network
          |           |           |
          v           v           v
       DC01/DC02    CLIENT01     MGMT01
```

### 3.2 Network Segments

| Segment | Subnet | Router Gateway |
|---|---|---|
| Servers | `10.20.10.0/24` | `10.20.10.1` |
| Clients | `10.20.20.0/24` | `10.20.20.1` |
| Management | `10.20.30.0/24` | `10.20.30.1` |
| Transit | `10.10.10.0/24` | RTR01: `10.10.10.2` |

---

## 4. VyOS Responsibilities

RTR01 provides the internal routing functionality required for TTT's segmented network.

### Primary Responsibilities

- Route traffic between internal subnets.
- Provide default gateways.
- Forward external-bound traffic toward FW01.
- Maintain routing information.
- Support network troubleshooting.
- Provide a centralized routing point between internal segments.

### Important

Routing enables connectivity between networks.

Firewall policies and other access controls determine whether specific traffic should be permitted.

---

## 5. Interface Architecture

### 5.1 Documented IP Addressing

| Interface Role | IP Address | Network |
|---|---|---|
| Transit | `10.10.10.2` | `10.10.10.0/24` |
| Servers Gateway | `10.20.10.1` | `10.20.10.0/24` |
| Clients Gateway | `10.20.20.1` | `10.20.20.0/24` |
| Management Gateway | `10.20.30.1` | `10.20.30.0/24` |

The physical or virtual interface names require verification.

### 5.2 Interface Verification

Using the VyOS operational CLI:

```bash
show interfaces
```

Review interface addresses:

```bash
show interfaces detail
```

Review the running configuration:

```bash
show configuration commands
```

### Verification Checklist

- [ ] Transit interface identified
- [ ] Server interface identified
- [ ] Client interface identified
- [ ] Management interface identified
- [ ] IP addresses verified
- [ ] Interface status reviewed
- [ ] Hyper-V connections documented

---

## 6. Routing Architecture

### 6.1 Connected Routes

RTR01 should have directly connected routes for its configured interfaces.

Expected networks include:

```text
10.10.10.0/24
10.20.10.0/24
10.20.20.0/24
10.20.30.0/24
```

### 6.2 Default Route

The expected upstream next hop is FW01.

```text
0.0.0.0/0 -> 10.10.10.1
```

**Status:** Expected Architecture — Verify Actual Configuration

### 6.3 Routing Table Verification

```bash
show ip route
```

Review the default route:

```bash
show ip route 0.0.0.0/0
```

### 6.4 Example Default Route Configuration

The following is a reference example and should not be executed without verifying the current configuration.

```bash
configure
set protocols static route 0.0.0.0/0 next-hop 10.10.10.1
compare
commit
save
exit
```

**Execution Status:** Reference Example — Not Executed

### 6.5 Routing Considerations

- Verify connected routes.
- Verify the default route.
- Avoid duplicate or conflicting routes.
- Review upstream routing.
- Confirm firewall policies.
- Document changes.

---

## 7. Inter-Subnet Routing

### 7.1 Overview

Inter-subnet routing allows devices on different IP networks to communicate through RTR01.

### 7.2 Example Communication

CLIENT01:

```text
10.20.20.10
```

DC01:

```text
10.20.10.10
```

### 7.3 Expected Traffic Path

```text
CLIENT01
10.20.20.10
    |
    v
RTR01
10.20.20.1
    |
    v
Server Network
10.20.10.0/24
    |
    v
DC01
10.20.10.10
```

### 7.4 Routing Verification

From CLIENT01:

```powershell
ping 10.20.20.1
```

```powershell
ping 10.20.10.10
```

```powershell
tracert 10.20.10.10
```

### 7.5 Important

Successful routing does not guarantee that an application service is available.

Firewall rules, host firewalls, DNS, and application configuration may still affect connectivity.

---

## 8. External Network Connectivity

### 8.1 Overview

RTR01 forwards traffic destined for external networks toward FW01.

### 8.2 Expected Traffic Flow

```text
Internal Client
      |
      v
RTR01 - VyOS
      |
      v
FW01 - OPNsense
      |
      v
Outbound NAT
      |
      v
External Network
```

### 8.3 Dependencies

- Correct client default gateway
- RTR01 interface connectivity
- RTR01 default route
- FW01 routing
- FW01 firewall rules
- Outbound NAT
- Upstream network connectivity

### 8.4 Verification

From RTR01:

```bash
ping 10.10.10.1
```

From CLIENT01:

```powershell
tracert 1.1.1.1
```

### Verification Checklist

- [ ] RTR01 reaches FW01
- [ ] Default route verified
- [ ] Internal clients reach RTR01
- [ ] FW01 routes verified
- [ ] NAT configuration verified
- [ ] External connectivity tested

---

## 9. Network Segmentation

### 9.1 Purpose

Network segmentation separates devices according to their operational functions.

### 9.2 TTT Segments

**Server Network**

```text
10.20.10.0/24
```

Contains:

- DC01
- DC02

**Client Network**

```text
10.20.20.0/24
```

Contains:

- CLIENT01

**Management Network**

```text
10.20.30.0/24
```

Contains:

- MGMT01

### 9.3 Segmentation Benefits

- Clear network organization
- Simplified routing
- Improved troubleshooting
- Better traffic control opportunities
- Separation of infrastructure responsibilities

### 9.4 Security Considerations

Network segmentation alone does not automatically block communication.

Additional firewall policies or access controls are required to restrict traffic between routed segments.

The current inter-subnet filtering configuration requires verification.

---

## 10. VyOS Configuration Management

### 10.1 Overview

VyOS uses a command-line configuration system.

Changes are generally prepared in configuration mode and applied through a commit process.

### 10.2 Operational Mode

Used to inspect system information and perform diagnostics.

Examples:

```bash
show interfaces
```

```bash
show ip route
```

### 10.3 Configuration Mode

Enter configuration mode:

```bash
configure
```

Review proposed changes:

```bash
compare
```

Apply changes:

```bash
commit
```

Save the running configuration:

```bash
save
```

Exit configuration mode:

```bash
exit
```

### 10.4 Important

A committed configuration change is not necessarily saved for subsequent reboots.

Use the appropriate save procedure after verifying an approved change.

For potentially disruptive remote changes, use the supported confirmed-commit or rollback capabilities appropriate to the installed VyOS version.

---

## 11. Router Administration

### 11.1 Administrative Tasks

- Review interfaces.
- Review routing.
- Configure network addresses.
- Manage static routes.
- Review system logs.
- Troubleshoot connectivity.
- Maintain configuration backups.
- Apply approved updates.

### 11.2 Security Recommendations

- Restrict administrative access.
- Use secure remote management.
- Protect administrative credentials.
- Review configured services.
- Document changes.
- Maintain supported software.

### 11.3 Verification Checklist

- [ ] Administrative accounts reviewed
- [ ] SSH configuration reviewed
- [ ] Management access restrictions verified
- [ ] VyOS version documented
- [ ] Configuration backup status recorded

---

## 12. Monitoring and Logging

### 12.1 Monitoring Objectives

Monitor:

- Interface availability
- Routing changes
- Connectivity
- CPU utilization
- Memory utilization
- System logs
- Administrative activity

### 12.2 Example Commands

Review system information:

```bash
show version
```

Review interfaces:

```bash
show interfaces
```

Review routing:

```bash
show ip route
```

Review logs using commands supported by the installed VyOS version.

### 12.3 Monitoring Matrix

| Component | Monitoring Focus | Status |
|---|---|---|
| Transit Interface | FW01 connectivity | Pending |
| Server Interface | Server network connectivity | Pending |
| Client Interface | Client network connectivity | Pending |
| Management Interface | Management connectivity | Pending |
| Routing Table | Correct routes | Pending |
| System | Performance and errors | Pending |

---

## 13. Router Troubleshooting

### 13.1 General Workflow

1. Identify the affected network.
2. Confirm the symptoms.
3. Review interface status.
4. Verify IP addresses.
5. Review connected routes.
6. Review the default route.
7. Test next-hop connectivity.
8. Review firewall dependencies.
9. Identify the cause.
10. Implement an authorized correction.
11. Verify connectivity.
12. Document findings.

### 13.2 Troubleshooting Matrix

| Issue | Potential Cause | Investigation |
|---|---|---|
| Client cannot reach server | Routing or firewall issue | Review interfaces and routes |
| No internet access | Missing default route | Review upstream route |
| Management network unreachable | Interface or policy issue | Review management interface |
| Transit connection unavailable | Virtual network issue | Review Hyper-V and interface status |
| Incorrect next hop | Static route configuration | Review routing table |
| Intermittent connectivity | Interface or upstream issue | Review logs and network health |

### 13.3 Example Scenario

**Scenario:** CLIENT01 can reach its gateway but cannot reach DC01.

Potential investigation:

1. Verify CLIENT01 IP configuration.
2. Verify the client gateway.
3. Review RTR01 interfaces.
4. Review routing.
5. Verify DC01's gateway.
6. Review host and network firewall rules.
7. Test connectivity.
8. Document the findings.

**Status:** Illustrative Scenario — Not Executed

---

## 14. Configuration Backup and Recovery

### 14.1 Purpose

VyOS configuration backups support restoration after configuration errors or infrastructure failures.

### 14.2 Backup Considerations

- Maintain protected configuration backups.
- Record VyOS version compatibility.
- Document interface assignments.
- Document routing configuration.
- Protect credentials and keys.
- Test recovery procedures.

### 14.3 Recovery Planning

Potential recovery activities include:

- Restoring a known-good configuration
- Correcting routing changes
- Recovering management access
- Rebuilding the router VM
- Reconnecting virtual interfaces

### Verification Checklist

- [ ] Backup method documented
- [ ] Backup destination identified
- [ ] Last successful backup recorded
- [ ] Recovery procedure documented
- [ ] Restore testing performed

### Important

VyOS configuration files may contain sensitive information.

Do not publish unredacted configurations in a public GitHub repository.

---

## 15. ITIL 4 Integration

| Practice | Application |
|---|---|
| Incident Management | Restore interrupted routing |
| Problem Management | Investigate recurring connectivity failures |
| Change Enablement | Control route and interface changes |
| Knowledge Management | Document router procedures |
| Monitoring and Event Management | Review router health |
| Service Configuration Management | Track RTR01 and dependencies |
| Information Security Management | Protect management access |
| Continual Improvement | Improve network reliability |

### Example Incident

**Scenario:** The management network cannot communicate with the server network.

Potential workflow:

1. Service Desk records the incident.
2. IT identifies affected networks.
3. RTR01 interfaces and routes are inspected.
4. Firewall and host policies are reviewed.
5. An authorized correction is implemented.
6. Connectivity is tested.
7. The incident is documented and closed.

---

## 16. Service Configuration Management

### Configuration Item

| Attribute | Value |
|---|---|
| CI Name | RTR01 |
| CI Type | Router |
| Platform | VyOS |
| Virtualization | Hyper-V |
| Related Firewall | FW01 |
| Configuration Status | Verification Ongoing |

### Dependencies

```text
Hyper-V
   |
   v
RTR01 - VyOS
   |
   +-- Server Network
   |
   +-- Client Network
   |
   +-- Management Network
   |
   v
FW01 - OPNsense
```

### Configuration Requirements

- Document interfaces.
- Record IP addresses.
- Maintain routing information.
- Document dependencies.
- Record configuration changes.
- Maintain backup information.

---

## 17. Change Management

Changes to RTR01 can affect connectivity across multiple networks.

### Examples

- Interface address changes
- Route additions
- Route removals
- Default gateway changes
- Management service changes
- Software upgrades

### Proposed Workflow

1. Identify the required change.
2. Assess affected networks.
3. Review dependencies.
4. Obtain applicable authorization.
5. Prepare configuration commands.
6. Prepare rollback steps.
7. Implement the change.
8. Verify routing.
9. Test connectivity.
10. Save the verified configuration.
11. Update documentation.

---

## 18. Future Improvements

Potential projects include:

- Static routing exercises
- Dynamic routing protocol labs
- Routing troubleshooting simulations
- Network monitoring
- Configuration backup automation
- Access control policy improvements
- Additional routed networks
- High-availability design exercises

These improvements are proposed and not documented as completed.

---

## 19. Skills Practiced

- VyOS administration
- Linux-based network appliance concepts
- IPv4 addressing
- Subnetting
- Static routing
- Default routes
- Inter-subnet routing
- Network segmentation
- Routing table analysis
- Command-line administration
- Network troubleshooting
- Configuration management
- Change management
- ITIL-aligned network operations

---

## 20. What I Learned

**1. Routing**

Routers forward packets between different IP networks.

**2. Default Gateways**

Devices use their default gateway to reach destinations outside their local subnet.

**3. Static Routes**

Static routes define specific network destinations and next hops.

**4. Network Segmentation**

Separate networks improve organization and provide opportunities for security controls.

**5. Firewall Dependencies**

Routing and firewall policies work together to provide authorized connectivity.

**6. Configuration Management**

Router changes should be reviewed, verified, saved, and documented.

---

## 21. Final Verification Checklist

### Network Configuration

- [ ] VyOS version verified
- [ ] Interfaces inventoried
- [ ] IP addresses verified
- [ ] Connected routes verified
- [ ] Default route verified

### Connectivity

- [ ] Server network reachable
- [ ] Client network reachable
- [ ] Management network reachable
- [ ] FW01 reachable
- [ ] External connectivity tested

### Administration

- [ ] Management access reviewed
- [ ] Configuration backup verified
- [ ] Recovery procedure documented

### Documentation

- [ ] Configuration evidence collected
- [ ] Screenshots sanitized
- [ ] Routing dependencies documented
- [ ] Revision history updated

---

## 22. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT VyOS routing infrastructure documentation |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

RTR01 is part of the documented TTT infrastructure. Network addresses and architecture are based on previously recorded lab information.

Actual interface assignments, software versions, routes, and operational results require verification.

Example configurations and troubleshooting scenarios do not represent completed activities.

Sensitive configuration data and credentials must not be published.
