# Technical Techno Tech — OPNsense Firewall Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Document ID:** INF-NET-002  
**Document Type:** Network Infrastructure Documentation  
**Version:** 1.0  
**Status:** Existing Lab — Verification Ongoing  
**Device:** FW01  
**Platform:** OPNsense  
**Function:** Internal IT  
**ITIL 4 Practice:** Service Configuration Management

---

## 1. Purpose

This document describes the OPNsense firewall infrastructure supporting Technical Techno Tech.

It provides a centralized reference for:

- Firewall architecture
- Network interfaces
- WAN and internal connectivity
- Firewall rules
- Network Address Translation (NAT)
- Routing dependencies
- Security controls
- Firewall administration
- Monitoring and logging
- Troubleshooting
- Configuration backup and recovery
- Change management

The goal is to document how FW01 supports network connectivity and security within the TTT environment.

---

## 2. Environment Overview

Technical Techno Tech operates a segmented virtual network using Hyper-V, OPNsense, and VyOS.

OPNsense functions as the firewall between the external network and TTT's internal infrastructure.

### Firewall Inventory

| Attribute | Configuration |
|---|---|
| Hostname | FW01 |
| Platform | OPNsense |
| Deployment | Virtual Machine |
| Hypervisor | Hyper-V |
| Function | Firewall and Network Security |
| WAN Address | `192.168.1.176` — Last Documented |
| Transit Address | `10.10.10.1` |
| Transit Network | `10.10.10.0/24` |
| Internal Router | RTR01 — VyOS |
| Current OPNsense Version | Pending Verification |
| Management Address | Pending Verification |
| Configuration Backup Status | Pending Verification |

The last documented WAN address may change if assigned dynamically.

---

## 3. Network Architecture

### 3.1 Logical Topology

```text
                  Internet
                     |
                     v
             External Network
                     |
                     v
              FW01 - OPNsense
              WAN: 192.168.1.176
              Transit: 10.10.10.1
                     |
                     v
              10.10.10.0/24
                     |
                     v
                RTR01 - VyOS
                10.10.10.2
                     |
          +----------+----------+
          |          |          |
          v          v          v
       Servers     Clients   Management
       Network     Network    Network
          |          |          |
          v          v          v
      DC01/DC02    CLIENT01    MGMT01
```

### 3.2 Network Segments

| Network | Subnet | Gateway |
|---|---|---|
| Transit | `10.10.10.0/24` | Not Applicable — Transit Link |
| Servers | `10.20.10.0/24` | `10.20.10.1` |
| Clients | `10.20.20.0/24` | `10.20.20.1` |
| Management | `10.20.30.0/24` | `10.20.30.1` |

RTR01 provides routing between the internal network segments.

FW01 provides the external firewall boundary.

---

## 4. OPNsense Responsibilities

FW01 is responsible for supporting the following network functions.

### Firewall Enforcement

Control permitted and denied network traffic according to configured policies.

### Network Address Translation

Translate applicable internal source addresses when traffic exits toward the external network.

### External Connectivity

Provide the firewall boundary between TTT's internal infrastructure and the upstream network.

### Network Security

Reduce unnecessary exposure of internal systems to external networks.

### Logging

Provide firewall and network activity logs for investigation and troubleshooting.

### Configuration Management

Maintain documented and recoverable firewall configurations.

---

## 5. Interface Configuration

### 5.1 Documented Interfaces

| Interface Role | IP Address | Network | Status |
|---|---|---|---|
| WAN | `192.168.1.176` | Upstream Network | Last Documented |
| Transit | `10.10.10.1` | `10.10.10.0/24` | Previously Configured |

Actual OPNsense interface names and assignments require verification.

### 5.2 Interface Verification

Using the OPNsense web interface:

1. Sign in with an authorized administrative account.
2. Navigate to **Interfaces > Overview**.
3. Review interface assignments.
4. Verify IP addresses.
5. Review interface status.
6. Confirm the expected virtual network connections.
7. Record the results.

### Verification Checklist

- [ ] WAN interface identified
- [ ] Transit interface identified
- [ ] Interface names recorded
- [ ] IP addresses verified
- [ ] Interface status verified
- [ ] Hyper-V virtual switch connections documented

---

## 6. Firewall Rules

### 6.1 Overview

Firewall rules determine whether network traffic is permitted or denied.

OPNsense uses a stateful firewall.

Rules can evaluate characteristics such as:

- Source address
- Destination address
- Protocol
- Port
- Interface
- Direction
- Connection state

### 6.2 TTT Firewall Policy

The exact deployed rules require verification.

The intended security design should:

- Permit authorized outbound traffic.
- Restrict unnecessary inbound connections.
- Protect internal infrastructure.
- Allow required routing and service communication.
- Log relevant denied traffic.
- Avoid overly permissive rules.

### 6.3 Rule Inventory

| Rule ID | Interface | Source | Destination | Action | Status |
|---|---|---|---|---|---|
| FW-RULE-001 | Pending | Pending | Pending | Pending | Verification Required |
| FW-RULE-002 | Pending | Pending | Pending | Pending | Verification Required |
| FW-RULE-003 | Pending | Pending | Pending | Pending | Verification Required |

### 6.4 Rule Verification

In the OPNsense web interface:

1. Navigate to **Firewall > Rules**.
2. Select each relevant interface.
3. Review enabled rules.
4. Record source and destination conditions.
5. Review protocols and ports.
6. Identify unnecessary permissions.
7. Review rule descriptions.
8. Capture sanitized evidence.

### 6.5 Security Considerations

- Follow least privilege.
- Avoid unnecessary any-to-any rules.
- Restrict management access.
- Document rule purposes.
- Review rules after infrastructure changes.
- Remove obsolete rules through approved change procedures.

---

## 7. Network Address Translation

### 7.1 Overview

Network Address Translation allows private internal networks to communicate with external networks through translated addresses.

### 7.2 TTT NAT Design

Previous lab work included troubleshooting OPNsense outbound NAT and internal client internet connectivity.

The current NAT configuration must be verified.

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
FW01
10.10.10.1
    |
    v
Outbound NAT
    |
    v
Upstream Network
```

### 7.4 Outbound NAT Verification

Using the OPNsense web interface:

1. Navigate to **Firewall > NAT > Outbound**.
2. Identify the current NAT mode.
3. Review outbound NAT rules.
4. Confirm relevant internal networks are covered.
5. Verify the translation interface.
6. Review rule ordering and conditions.
7. Test connectivity.
8. Document the results.

### 7.5 NAT Inventory

| Source Network | Translation Interface | Status |
|---|---|---|
| `10.20.10.0/24` | WAN — Verify | Pending |
| `10.20.20.0/24` | WAN — Verify | Pending |
| `10.20.30.0/24` | WAN — Verify | Pending |

These entries represent expected network coverage, not confirmed NAT rules.

### 7.6 Verification Checklist

- [ ] Outbound NAT mode recorded
- [ ] NAT rules inventoried
- [ ] Internal networks reviewed
- [ ] Translation addresses verified
- [ ] External connectivity tested
- [ ] Results documented

---

## 8. Routing Configuration

### 8.1 Overview

FW01 must be able to forward traffic toward the appropriate networks.

RTR01 provides routing for the internal server, client, and management networks.

### 8.2 Internal Routes

The following internal networks are reachable through RTR01 when routing is correctly configured.

| Destination Network | Expected Next Hop |
|---|---|
| `10.20.10.0/24` | `10.10.10.2` |
| `10.20.20.0/24` | `10.10.10.2` |
| `10.20.30.0/24` | `10.10.10.2` |

**Status:** Expected Architecture — Verify Actual Routing Table

### 8.3 Route Verification

In OPNsense:

1. Open the routing diagnostics or route status page available in the installed version.
2. Review the routing table.
3. Verify routes to internal networks.
4. Verify the default route.
5. Confirm the next-hop addresses.
6. Test connectivity.

### 8.4 Routing Dependencies

- RTR01 availability
- Transit network connectivity
- Correct static or dynamic routes
- Firewall policies
- NAT configuration
- Hyper-V virtual networking

---

## 9. Firewall Administration

### 9.1 Administrative Access

FW01 should be administered only by authorized IT personnel.

### 9.2 Administrative Tasks

- Review firewall rules.
- Manage network interfaces.
- Review NAT configuration.
- Inspect routing.
- Review logs.
- Apply approved updates.
- Back up configuration.
- Troubleshoot connectivity.

### 9.3 Security Recommendations

- Use strong administrative authentication.
- Restrict management access.
- Use HTTPS for web administration.
- Avoid exposing the management interface unnecessarily.
- Review administrator accounts.
- Maintain current supported software.

### 9.4 Verification Checklist

- [ ] Management interface identified
- [ ] Administrative accounts reviewed
- [ ] Management access restrictions reviewed
- [ ] HTTPS configuration reviewed
- [ ] Software version recorded

---

## 10. Logging and Monitoring

### 10.1 Purpose

Firewall logs provide information about network activity and security events.

### 10.2 Relevant Logs

- Allowed connections
- Blocked connections
- Firewall rule matches
- System events
- Interface events
- Administrative activity

### 10.3 Monitoring Objectives

| Component | Monitoring Focus | Status |
|---|---|---|
| WAN Interface | Connectivity | Pending |
| Transit Interface | Connectivity | Pending |
| Firewall Rules | Blocked and allowed traffic | Pending |
| NAT | Translation behavior | Pending |
| Routing | Internal network reachability | Pending |
| System | Resource utilization and errors | Pending |

### 10.4 Verification

Using the OPNsense interface:

1. Open **Firewall > Log Files**.
2. Review relevant entries.
3. Identify the source and destination.
4. Review the matching firewall rule.
5. Correlate events with reported issues.
6. Record findings.

Menu names may differ by OPNsense version.

---

## 11. Firewall Troubleshooting

### 11.1 Troubleshooting Workflow

1. Identify the affected system.
2. Confirm the reported symptoms.
3. Verify the source IP configuration.
4. Verify the default gateway.
5. Test connectivity to RTR01.
6. Test connectivity to FW01.
7. Review routing.
8. Review firewall rules.
9. Review NAT.
10. Review logs.
11. Implement an authorized correction.
12. Retest connectivity.
13. Document findings.

### 11.2 Example Troubleshooting Matrix

| Issue | Potential Cause | Investigation |
|---|---|---|
| Client cannot access internet | NAT or routing issue | Review outbound NAT and routes |
| Server cannot reach external network | Firewall policy | Review applicable rules |
| Internal network unreachable | Missing route | Review routing table |
| Firewall management unavailable | Interface or access restriction | Review management connectivity |
| Traffic unexpectedly blocked | Rule mismatch | Review firewall logs |
| Intermittent connectivity | Interface or upstream issue | Review interface status and logs |

### 11.3 Windows Client Tests

```powershell
ipconfig /all
```

```powershell
ping 10.20.20.1
```

```powershell
ping 10.10.10.1
```

```powershell
tracert 1.1.1.1
```

The ability to ping an interface depends on routing and firewall policy.

A failed ICMP test does not always indicate that the target service is unavailable.

---

## 12. Configuration Backup and Recovery

### 12.1 Purpose

Firewall configuration backups support recovery after configuration errors or system failures.

### 12.2 Backup Considerations

- Export firewall configuration using supported OPNsense tools.
- Protect configuration files.
- Restrict access to backup copies.
- Record backup dates.
- Review recovery procedures.
- Test restoration in an appropriate environment.

### 12.3 Verification Checklist

- [ ] Backup method documented
- [ ] Backup location recorded
- [ ] Last backup date recorded
- [ ] Configuration file protected
- [ ] Recovery procedure documented
- [ ] Restore test completed

### Important

Configuration exports may contain sensitive network and authentication information.

Do not publish unredacted configuration backups in a public GitHub repository.

---

## 13. ITIL 4 Integration

| Practice | Application |
|---|---|
| Incident Management | Restore interrupted connectivity |
| Problem Management | Investigate recurring firewall issues |
| Change Enablement | Control firewall rule and NAT changes |
| Knowledge Management | Document troubleshooting procedures |
| Monitoring and Event Management | Review firewall events |
| Service Configuration Management | Track FW01 configuration and dependencies |
| Information Security Management | Enforce network access controls |
| Continual Improvement | Improve firewall configuration and reliability |

### Example Incident

**Scenario:** CLIENT01 cannot access the internet.

Potential workflow:

1. Service Desk records the incident.
2. IT confirms local connectivity.
3. RTR01 routing is reviewed.
4. FW01 firewall and NAT configuration is inspected.
5. An authorized correction is implemented.
6. Internet connectivity is tested.
7. The incident is documented and closed.

**Status:** Illustrative Scenario — Not Executed

---

## 14. Service Configuration Management

### Configuration Item

| Attribute | Value |
|---|---|
| CI Name | FW01 |
| CI Type | Firewall |
| Platform | OPNsense |
| Virtualization | Hyper-V |
| Related Device | RTR01 |
| Configuration Status | Verification Ongoing |

### Dependencies

```text
Hyper-V
   |
   v
FW01 - OPNsense
   |
   v
RTR01 - VyOS
   |
   v
Internal Networks
```

### Configuration Management Requirements

- Maintain accurate interface information.
- Document firewall rules.
- Document NAT.
- Document routing.
- Record significant changes.
- Maintain recovery information.
- Verify configuration after changes.

---

## 15. Change Management

Changes to FW01 may affect network availability and security.

### Examples

- Adding firewall rules
- Removing firewall rules
- Changing NAT configuration
- Changing interface addresses
- Updating routes
- Changing management access
- Applying software updates

### Proposed Change Workflow

1. Identify the required change.
2. Document the justification.
3. Assess security and connectivity impact.
4. Obtain applicable authorization.
5. Prepare implementation steps.
6. Prepare a recovery plan.
7. Implement the change.
8. Test connectivity.
9. Review firewall logs.
10. Update documentation.

---

## 16. Future Improvements

Potential projects include:

- Firewall rule auditing
- Network segmentation policy refinement
- Centralized logging
- Firewall configuration backup automation
- VPN configuration
- Additional network monitoring
- Firewall security hardening
- Incident simulation
- NAT troubleshooting exercises

These improvements are proposed and are not documented as completed.

---

## 17. Skills Practiced

- OPNsense administration
- Firewall architecture
- Network security
- Stateful firewall concepts
- Network Address Translation
- Routing
- Network segmentation
- Interface configuration
- Firewall logging
- Connectivity troubleshooting
- Configuration management
- Change management
- ITIL-aligned network operations

---

## 18. What I Learned

**1. Firewall Architecture**

A firewall controls traffic between networks according to defined security policies.

**2. NAT**

Network Address Translation allows internal private networks to communicate through translated addresses.

**3. Routing Dependencies**

Firewall connectivity depends on correct routing between internal and external networks.

**4. Network Segmentation**

Separate networks allow traffic to be organized and controlled according to business requirements.

**5. Firewall Logging**

Logs provide evidence for troubleshooting and security investigations.

**6. Change Management**

Firewall changes require careful planning because incorrect rules can interrupt services or expose resources.

---

## 19. Final Verification Checklist

### Configuration

- [ ] OPNsense version verified
- [ ] Interfaces inventoried
- [ ] IP addresses verified
- [ ] Firewall rules documented
- [ ] NAT configuration documented
- [ ] Routing table verified

### Security

- [ ] Administrative access reviewed
- [ ] Management restrictions reviewed
- [ ] Unnecessary firewall rules reviewed
- [ ] Logging configuration reviewed

### Operations

- [ ] External connectivity tested
- [ ] Internal network reachability tested
- [ ] Configuration backup verified
- [ ] Recovery procedure documented

### Documentation

- [ ] Screenshots sanitized
- [ ] Test results recorded
- [ ] Configuration dependencies documented
- [ ] Revision history updated


---

## 20. Revision History

| Version | Description |
|---|---|
| 1.0 | Initial TTT OPNsense firewall infrastructure documentation |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

FW01 is part of the documented TTT infrastructure. Configuration values are based on previously recorded lab information and must be verified against the current environment.

Proposed procedures and example scenarios are not represented as completed activities.

Sensitive firewall configurations, credentials, and authentication information must not be published in the public repository.
