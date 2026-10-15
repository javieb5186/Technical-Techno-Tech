# Networking Infrastructure

**Organization:** Technical Techno Tech (TTT)  
**Environment:** Virtualized Enterprise Network Lab  
**Firewall:** OPNsense  
**Router:** VyOS  
**Virtualization:** Hyper-V  
**Status:** Existing Lab — Documentation and Verification Ongoing

---

## 1. Overview

This project documents the network infrastructure supporting Technical Techno Tech's internal IT environment.

The network uses OPNsense and VyOS to provide firewall services, routing, network segmentation, and internet connectivity for virtualized Windows Server and workstation systems.

The environment is designed to simulate the infrastructure of a small business with separate networks for servers, employees, and IT administration.

## 2. Objectives

- Design a segmented business network.
- Configure virtual network interfaces.
- Deploy and administer a firewall.
- Configure routing between network segments.
- Implement outbound NAT.
- Establish internet connectivity.
- Support Active Directory and DNS traffic.
- Troubleshoot network connectivity.
- Verify routing and firewall behavior.
- Document network architecture and configuration.
- Practice enterprise networking concepts.

## 3. Network Architecture

```text
              Internet
                 |
                 v
          External Network
                 |
                 v
          FW01 - OPNsense
          WAN: 192.168.1.176
          LAN: 10.10.10.1
                 |
                 |
        Transit Network
          10.10.10.0/24
                 |
                 v
           RTR01 - VyOS
          Transit: 10.10.10.2
                 |
       +---------+---------+
       |         |         |
       v         v         v
    Servers    Clients   Management
    Network    Network    Network
       |         |         |
       v         v         v
   DC01/DC02  CLIENT01   MGMT01
```

The topology separates routing and firewall responsibilities.

## 4. Network Segmentation

| Network | Subnet | Gateway | Purpose |
|---|---|---|---|
| Transit | `10.10.10.0/24` | N/A | Firewall-to-router connectivity |
| Servers | `10.20.10.0/24` | `10.20.10.1` | Windows Server infrastructure |
| Clients | `10.20.20.0/24` | `10.20.20.1` | Employee workstations |
| Management | `10.20.30.0/24` | `10.20.30.1` | IT administrative systems |

The subnet gateways are provided by the VyOS router.

## 5. Network Device Inventory

| Device | Platform | Address | Purpose |
|---|---|---|---|
| FW01 | OPNsense | `10.10.10.1` | Firewall and outbound NAT |
| RTR01 | VyOS | `10.10.10.2` | Routing between internal networks |
| DC01 | Windows Server | `10.20.10.10` | AD DS and DNS |
| DC02 | Windows Server | `10.20.10.11` | Additional domain controller |
| CLIENT01 | Windows 11 | `10.20.20.10` | Employee workstation |
| MGMT01 | Windows 11 | `10.20.30.10` | Administrative workstation |

FW01 also has a previously documented WAN address of `192.168.1.176`.

## 6. Firewall Infrastructure — OPNsense

OPNsense provides the firewall layer between the TTT network and its external network.

### Responsibilities

- External network connectivity
- Outbound Network Address Translation
- Firewall policy enforcement
- Traffic filtering
- Network troubleshooting

### Documented Activities

Previous lab work established outbound NAT and verified internet connectivity from CLIENT01.

Additional firewall rules and security policies should be documented as they are configured and tested.

## 7. Routing Infrastructure — VyOS

VyOS provides routing between the TTT network segments.

### Responsibilities

- Internal network gateways
- Inter-subnet routing
- Routing toward OPNsense
- Connectivity between servers, clients, and management systems

### Network Interfaces

The router connects to:

- Transit network
- Server network
- Client network
- Management network

Exact virtual interface names should be recorded from the current VyOS configuration.

### Example Verification Commands

```text
show interfaces
show ip route
show configuration
```

Commands are reference examples and are not evidence of execution.

## 8. Network Address Translation

Outbound NAT allows internal TTT systems to communicate with external networks through OPNsense.

The documented lab previously verified internet connectivity from CLIENT01.

NAT and firewall rules should be reviewed whenever internal network addressing or routing changes.

## 9. Active Directory Network Requirements

The network supports communication between:

- Domain controllers
- Domain-joined workstations
- Administrative workstations
- DNS services

Active Directory requires reliable name resolution and connectivity to domain controllers.

Relevant protocols include:

- DNS
- Kerberos
- LDAP
- SMB
- RPC
- NTP

Firewall policies must permit required traffic without unnecessarily exposing internal services.

## 10. Connectivity Verification

### Windows

```powershell
ipconfig /all
ping 10.20.10.10
tracert 10.20.10.10
Test-NetConnection 10.20.10.10 -Port 53
Resolve-DnsName technicaltechnotech.com
```

### VyOS

```text
show interfaces
show ip route
ping 10.10.10.1
```

### OPNsense

Use the applicable firewall management and diagnostic tools to inspect:

- Interfaces
- Routing
- Firewall rules
- NAT configuration
- Connectivity logs

Actual test results should be recorded in the appropriate project documentation.

## 11. Network Security

Security considerations include:

- Network segmentation
- Firewall rule management
- Least-privilege network access
- Administrative interface protection
- Restricted management access
- DNS security
- Logging and monitoring
- Change control

Network segmentation alone does not guarantee isolation.

Effective isolation depends on routing, firewall rules, and other access controls.

## 12. Troubleshooting Scenarios

Potential exercises include:

- Incorrect default gateway
- Incorrect DNS server
- Missing route
- Firewall rule blocking traffic
- NAT misconfiguration
- Duplicate IP address
- Incorrect subnet mask
- Domain controller unreachable
- DNS resolution failure
- Client unable to access the internet

Each scenario should record:

1. Symptoms
2. Impact
3. Investigation
4. Root cause, when established
5. Corrective action
6. Verification
7. Lessons learned

## 13. ITIL 4 Integration

| Practice | Example |
|---|---|
| Incident Management | Client connectivity failure |
| Problem Management | Recurring DNS resolution issues |
| Change Enablement | Firewall or routing changes |
| Monitoring and Event Management | Interface and connectivity alerts |
| Service Configuration Management | Router, firewall, and network dependencies |
| Information Security Management | Firewall access policies |
| Knowledge Management | Network troubleshooting procedures |
| Continual Improvement | Reducing recurring network failures |

## 14. Documentation

- [Network Topology](Network-Topology.md)
- [OPNsense](OPNsense/)
- [VyOS](VyOS/)
- [Infrastructure Overview](../README.md)
- [Active Directory](../Active-Directory/README.md)
- [Windows Server](../Windows-Server/README.md)
- [Hyper-V](../Virtualization/Hyper-V/README.md)

## 15. Skills Practiced

- IP addressing
- Subnetting
- Routing
- Network segmentation
- Firewall administration
- NAT
- DNS troubleshooting
- Network diagnostics
- Virtual networking
- Connectivity verification
- Network documentation
- Network security fundamentals

## 16. What I Learned

This project demonstrates how network infrastructure supports centralized IT services.

Key learning areas include:

- The difference between routing and firewall responsibilities.
- How separate subnets organize business infrastructure.
- How clients communicate with servers on different networks.
- How NAT provides outbound connectivity.
- How DNS and routing affect Active Directory operations.
- How to isolate network connectivity problems systematically.

## 17. Future Development

Potential future activities include:

- Additional firewall policy testing
- Centralized logging
- Network monitoring
- Network redundancy
- VPN connectivity
- More advanced routing scenarios
- Security validation
- Network automation

Future activities must be distinguished from completed implementations.

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for practical IT training.

This README documents its virtualized networking environment. Technical configurations and test results should be supported by actual lab evidence.
