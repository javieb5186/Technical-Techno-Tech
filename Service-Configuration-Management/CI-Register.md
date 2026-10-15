# Configuration Item Register

**Organization:** Technical Techno Tech (TTT)  
**ITIL 4 Practice:** Service Configuration Management  
**Document Type:** Configuration Item Register  
**Document Status:** Draft — Pending Infrastructure Verification  
**Document Owner:** Internal IT  
**Last Updated:** 2026-10-14  
**Version:** 1.0

---

## 1. Purpose

The Configuration Item (CI) Register provides a centralized inventory of the configuration items documented within Technical Techno Tech's simulated enterprise environment.

The register supports the ITIL 4 Service Configuration Management practice by maintaining information about infrastructure components, their ownership, lifecycle status, and relationships.

The register is intended to support:

- Infrastructure visibility and accountability
- Incident investigation and troubleshooting
- Problem identification and root cause analysis
- Change impact assessment
- Service request fulfillment
- Security and access management
- Infrastructure recovery planning
- Configuration verification and auditing

Detailed technical information is maintained in each individual CI record.

---

## 2. Scope

This register covers the initial nine configuration items supporting TTT's on-premises virtual infrastructure.

Included configuration categories:

- Servers
- Network devices
- Workstations
- Virtualization infrastructure
- Logical infrastructure

The current scope includes Microsoft Hyper-V, Windows Server, Windows 11, OPNsense, VyOS, Active Directory Domain Services, and virtual networking.

Microsoft 365, Microsoft Entra ID, and Microsoft Intune are planned technologies and are not included as deployed configuration items in this register.

Additional CIs may be added as the infrastructure expands.

---

## 3. Configuration Item Inventory

| CI ID | Configuration Item | Classification | Criticality | Owner | Verification Status |
|---|---|---|---|---|---|
| [CI-001](Configuration-Items/Servers/CI-001-DC01.md) | DC01 | Server | Critical — Proposed | Internal IT | Pending |
| [CI-002](Configuration-Items/Servers/CI-002-DC02.md) | DC02 | Server | Critical — Proposed | Internal IT | Pending |
| [CI-003](Configuration-Items/Network-Devices/CI-003-FW01.md) | FW01 | Network Device | Critical — Proposed | Internal IT | Pending |
| [CI-004](Configuration-Items/Network-Devices/CI-004-RTR01.md) | RTR01 | Network Device | Critical — Proposed | Internal IT | Pending |
| [CI-005](Configuration-Items/Workstations/CI-005-MGMT01.md) | MGMT01 | Workstation | High — Proposed | Internal IT | Pending |
| [CI-006](Configuration-Items/Workstations/CI-006-CLIENT01.md) | CLIENT01 | Workstation | Medium — Proposed | Internal IT | Pending |
| [CI-007](Configuration-Items/Servers/CI-007-Hyper-V-Host.md) | Hyper-V Host | Virtualization Host | Critical — Proposed | Internal IT | Pending |
| [CI-008](Configuration-Items/Logical-Services/CI-008-Active-Directory-Domain.md) | Active Directory Domain | Logical Directory Service | Critical — Proposed | Internal IT | Pending |
| [CI-009](Configuration-Items/Logical-Services/CI-009-Virtual-Networks.md) | TTT Virtual Networks | Logical Network Infrastructure | Critical — Proposed | Internal IT | Pending |

**Inventory Count:** 9 configuration items

Criticality classifications are proposed and require formal review.

All nine records require current-state verification.

---

## 4. Configuration Item Categories

### 4.1 Servers

| CI ID | Name | Operating System | Documented IP Address | Primary Function |
|---|---|---|---|---|
| CI-001 | DC01 | Windows Server — Desktop Experience | `10.20.10.10` | Active Directory Domain Controller / DNS |
| CI-002 | DC02 | Windows Server Core | `10.20.10.11` | Additional Active Directory Domain Controller |

**Category Location:** [Servers](Configuration-Items/Servers/)

### 4.2 Network Devices

| CI ID | Name | Platform | Documented IP Address | Primary Function |
|---|---|---|---|---|
| CI-003 | FW01 | OPNsense | Transit: `10.10.10.1` | Firewall / NAT |
| CI-004 | RTR01 | VyOS | Transit: `10.10.10.2` | Internal Routing |

FW01's previously documented WAN address was `192.168.1.176`. Its current address requires verification.

**Category Location:** [Network Devices](Configuration-Items/Network-Devices/)

### 4.3 Workstations

| CI ID | Name | Operating System | Documented IP Address | Primary Function |
|---|---|---|---|---|
| CI-005 | MGMT01 | Windows 11 | `10.20.30.10` | Infrastructure Administration |
| CI-006 | CLIENT01 | Windows 11 | `10.20.20.10` | Employee Workstation |

**Category Location:** [Workstations](Configuration-Items/Workstations/)

### 4.4 Virtualization Infrastructure

| CI ID | Name | Platform | Primary Function |
|---|---|---|---|
| CI-007 | Hyper-V Host | Microsoft Hyper-V | Hosts TTT Virtual Machines |

The host operating system, hardware specifications, and management address remain pending verification.

**CI Record:** [CI-007 — Hyper-V Host](Configuration-Items/Servers/CI-007-Hyper-V-Host.md)

### 4.5 Logical Infrastructure

| CI ID | Name | Technology | Primary Function |
|---|---|---|---|
| CI-008 | Active Directory Domain | AD DS | Identity, Authentication, Authorization |
| CI-009 | TTT Virtual Networks | Hyper-V / IPv4 Networking | Virtual Network Connectivity |

**Category Location:** [Logical Services](Configuration-Items/Logical-Services/)

---

## 5. Network Configuration Summary

The following table represents the previously documented TTT network architecture.

| Network Segment | Subnet | Gateway / Interface | Purpose |
|---|---|---|---|
| WAN | Pending Verification | FW01 WAN Interface | External Connectivity |
| Transit | `10.10.10.0/24` | FW01: `10.10.10.1`; RTR01: `10.10.10.2` | Firewall-to-Router Connectivity |
| Servers | `10.20.10.0/24` | `10.20.10.1` | Server Infrastructure |
| Clients | `10.20.20.0/24` | `10.20.20.1` | Employee Workstations |
| Management | `10.20.30.0/24` | `10.20.30.1` | Administrative Systems |

**Related CI:** [CI-009 — TTT Virtual Networks](Configuration-Items/Logical-Services/CI-009-Virtual-Networks.md)

**Technical Documentation:** [Network Topology](../Infrastructure/Networking/Network-Topology.md)

---

## 6. Configuration Item Relationships

Configuration items may depend on, host, connect to, or provide services to other configuration items.

The following relationships represent the documented logical architecture and require current-state verification.

| Source CI | Relationship | Related CI |
|---|---|---|
| CI-007 — Hyper-V Host | Hosts | CI-001 — DC01 |
| CI-007 — Hyper-V Host | Hosts | CI-002 — DC02 |
| CI-007 — Hyper-V Host | Hosts | CI-003 — FW01 |
| CI-007 — Hyper-V Host | Hosts | CI-004 — RTR01 |
| CI-007 — Hyper-V Host | Hosts | CI-005 — MGMT01 |
| CI-007 — Hyper-V Host | Hosts | CI-006 — CLIENT01 |
| CI-001 — DC01 | Provides Directory Services For | CI-008 — Active Directory Domain |
| CI-002 — DC02 | Provides Directory Services For | CI-008 — Active Directory Domain |
| CI-003 — FW01 | Provides Firewall Connectivity For | CI-009 — TTT Virtual Networks |
| CI-004 — RTR01 | Provides Internal Routing For | CI-009 — TTT Virtual Networks |
| CI-009 — TTT Virtual Networks | Connects | CI-001 through CI-006 |
| CI-005 — MGMT01 | Used to Administer | TTT Infrastructure |
| CI-006 — CLIENT01 | Uses | CI-008 — Active Directory Domain |

### Simplified Dependency Diagram

```text
                      CI-007
                    Hyper-V Host
                         |
       +-----------------+-----------------+
       |                 |                 |
       v                 v                 v
   Servers           Network Devices   Workstations
       |                 |                 |
   +---+---+         +---+---+         +---+---+
   |       |         |       |         |       |
 CI-001  CI-002    CI-003  CI-004    CI-005  CI-006
  DC01    DC02      FW01    RTR01     MGMT01  CLIENT01
   |       |         |       |
   +---+---+         +---+---+
       |                 |
       v                 v
    CI-008             CI-009
 Active Directory    Virtual Networks
     Domain
```

This diagram summarizes major CI relationships rather than every network connection or service dependency.

**Dependency Documentation:** [Dependency Maps](Dependency-Maps/README.md)

---

## 7. Ownership and Responsibilities

| Responsibility | Assigned Role |
|---|---|
| Configuration Register Owner | Internal IT |
| Configuration Management Coordinator | Systems Administrator |
| Server Configuration Management | Systems Administrator |
| Network Configuration Management | Network Administrator |
| Identity Configuration Management | Identity & Systems Administrator |
| Workstation Configuration Management | Endpoint Administrator |
| Configuration Verification | Assigned Technical Owner |
| Configuration Change Authorization | Authorized Change Authority |

These roles represent simulated organizational responsibilities.

### Responsibilities

The assigned technical owner should:

1. Maintain accurate CI information.
2. Verify relevant technical configurations.
3. Document relationships and dependencies.
4. Update CI records after authorized changes.
5. Identify configuration discrepancies.
6. Attach or reference supporting evidence.
7. Participate in periodic configuration reviews.

The configuration management coordinator maintains the central register and checks consistency across CI records.

---

## 8. Configuration Item Lifecycle

Each configuration item follows a defined lifecycle.

| Lifecycle Stage | Description |
|---|---|
| Planned | CI has been identified but not yet deployed |
| Active | CI is deployed and intended to provide a function |
| Under Maintenance | CI is undergoing authorized maintenance |
| Retired | CI is no longer operational or required |

Lifecycle status and documentation verification status are tracked separately.

A CI may be documented as active while its current technical configuration remains unverified.

### Lifecycle Activities

**Identification**

Assign a unique CI ID and determine its category.

**Documentation**

Create the CI record using the approved configuration item template.

**Verification**

Compare documented information with the actual configuration.

**Maintenance**

Update the CI record following relevant infrastructure changes.

**Review**

Periodically assess accuracy, ownership, dependencies, and lifecycle status.

**Retirement**

Document the removal or replacement of the CI and update related records.

**Procedure:** [Configuration Item Management](Procedures/Configuration-Item-Management.md)

---

## 9. Configuration Verification Status

### Verification Definitions

| Status | Meaning |
|---|---|
| Pending | Verification has not yet been completed |
| Verified | Current configuration matches the documented baseline |
| Discrepancy | A difference between actual and documented configuration has been identified |
| Review Required | Documentation or evidence requires additional review |

### Verification Register

| CI ID | Last Verified | Verification Status | Next Action |
|---|---|---|---|
| CI-001 | Not Recorded | Pending | Verify DC01 configuration |
| CI-002 | Not Recorded | Pending | Verify DC02 configuration |
| CI-003 | Not Recorded | Pending | Verify FW01 configuration |
| CI-004 | Not Recorded | Pending | Verify RTR01 configuration |
| CI-005 | Not Recorded | Pending | Verify MGMT01 configuration |
| CI-006 | Not Recorded | Pending | Verify CLIENT01 configuration |
| CI-007 | Not Recorded | Pending | Verify Hyper-V host configuration |
| CI-008 | Not Recorded | Pending | Verify Active Directory domain |
| CI-009 | Not Recorded | Pending | Verify virtual network architecture |

### Verification Summary

| Metric | Count |
|---|---|
| Total Configuration Items | 9 |
| Verified | 0 |
| Pending Verification | 9 |
| Documented Discrepancies | 0 |
| Retired | 0 |

These figures represent the initial documentation state, not the operational health of the environment.

---

## 10. Configuration Baseline Management

A configuration baseline represents the documented and approved configuration of a CI.

Each individual CI record contains its intended configuration baseline.

Baseline information may include:

- Operating system and version
- Hostname
- IP addressing
- Installed roles and services
- Security settings
- Network configuration
- Administrative access
- Dependencies
- Backup requirements

### Baseline Review Process

1. Identify the CI requiring verification.
2. Review its documented baseline.
3. Inspect the actual configuration.
4. Compare actual settings against expected settings.
5. Record verification evidence.
6. Document any discrepancies.
7. Resolve discrepancies through the appropriate operational process.
8. Update the CI record and register.

A baseline should not be marked as verified without supporting evidence.

---

## 11. Integration With ITIL 4 Practices

The Configuration Item Register supports several TTT ITIL 4 practices.

| Practice | How the Register Is Used |
|---|---|
| Incident Management | Identify affected infrastructure and dependencies |
| Problem Management | Investigate recurring failures and shared causes |
| Change Enablement | Assess the potential impact of proposed changes |
| Service Request Management | Identify systems involved in request fulfillment |
| Information Security Management | Identify security-sensitive infrastructure |
| Monitoring and Event Management | Associate events with affected configuration items |
| Knowledge Management | Link troubleshooting articles to relevant CIs |
| Continual Improvement | Identify configuration and documentation improvement opportunities |

### Operational Record Linking

Where relevant, operational records should reference the affected CI ID.

Examples:

- Incident affecting DC01 → `CI-001`
- Change to FW01 firewall rules → `CI-003`
- Problem involving routing failures → `CI-004`
- Service request involving CLIENT01 → `CI-006`
- Domain-wide authentication issue → `CI-008`
- Virtual switch configuration change → `CI-007` and `CI-009`

These are examples of record relationships, not completed operational records.

---

## 12. Configuration Change Management

Configuration changes may affect one or more CIs.

Examples include:

- Operating system updates
- Server role changes
- Firewall rule modifications
- Routing changes
- IP address changes
- Virtual machine resource changes
- Group Policy modifications
- Security configuration changes
- Network topology changes

### Change Documentation Requirements

For relevant changes:

1. Identify the affected CI IDs.
2. Assess dependencies and potential service impact.
3. Follow the appropriate Change Enablement procedure.
4. Record the implementation outcome.
5. Verify the resulting configuration.
6. Update affected CI records.
7. Update the central CI Register where necessary.

**Related Practice:** [Change Enablement](../Change-Enablement/README.md)

---

## 13. Configuration Auditing

Configuration auditing helps determine whether documented CIs accurately represent the current environment.

### Audit Objectives

- Confirm that documented CIs exist.
- Confirm technical specifications.
- Verify ownership.
- Verify lifecycle status.
- Verify configuration baselines.
- Review relationships.
- Identify missing CIs.
- Identify outdated records.
- Identify undocumented changes.

### Audit Schedule

**Frequency:** Not Yet Established

**Responsible Role:** Configuration Management Coordinator

**Last Audit:** Not Conducted

**Next Audit:** Not Scheduled

### Audit Findings

No formal configuration audit has been completed for this register.

Findings should be recorded through the appropriate operational or continual improvement process.

---

## 14. Configuration Register Maintenance

The Configuration Item Register should be updated when:

- A new CI is introduced.
- An existing CI is retired.
- A CI changes ownership.
- A CI changes classification.
- A CI changes lifecycle status.
- A CI relationship changes.
- A configuration verification is completed.
- A significant discrepancy is identified or resolved.

### Maintenance Rules

- Every CI must have a unique identifier.
- CI IDs should not be reused after retirement.
- CI names should remain consistent across records.
- Technical details should be maintained in individual CI records.
- The register should provide a concise centralized inventory.
- Verification status should reflect actual evidence.
- Changes should be traceable to relevant operational records.

---

## 15. Related Documentation

### Service Configuration Management

- [Service Configuration Management Overview](README.md)
- [Configuration Item Management Procedure](Procedures/Configuration-Item-Management.md)
- [Configuration Items Overview](Configuration-Items/README.md)
- [Dependency Maps](Dependency-Maps/README.md)

### Templates

- [Configuration Item Template](../Templates/Configuration-Item-Template.md)
- [Dependency Map Template](../Templates/Dependency-Map-Template.md)

### Infrastructure

- [Infrastructure Overview](../Infrastructure/README.md)
- [Active Directory](../Infrastructure/Active-Directory/README.md)
- [Networking](../Infrastructure/Networking/README.md)
- [Virtualization](../Infrastructure/Virtualization/README.md)
- [Windows Server](../Infrastructure/Windows-Server/README.md)

### Service Management

- [Service Catalog](../Service-Catalog.md)
- [Incident Management](../Incident-Management/README.md)
- [Problem Management](../Problem-Management/README.md)
- [Change Enablement](../Change-Enablement/README.md)
- [Continual Improvement](../Continual-Improvement/README.md)

---

## 16. Review and Approval

| Field | Details |
|---|---|
| Document Status | Draft |
| Inventory Completeness | Nine Initial CIs Documented |
| Technical Verification | Pending |
| Ownership Review | Pending |
| Relationship Review | Pending |
| Formal Approval | Not Recorded |
| Last Review Date | Not Yet Reviewed |
| Next Review Date | Not Scheduled |

### Outstanding Actions

- Verify all nine configuration items.
- Review proposed criticality classifications.
- Confirm technical ownership.
- Verify CI relationships.
- Establish configuration review intervals.
- Establish configuration audit procedures.
- Update the register as new infrastructure is introduced.

---

## 17. Revision History

| Version | Date | Description |
|---|---|---|
| 1.0 | 2026-10-14 | Initial Configuration Item Register covering CI-001 through CI-009 |

---

## Simulation Disclaimer

This Configuration Item Register represents simulated enterprise infrastructure and IT service management activities within Technical Techno Tech, a fictional technology solutions company.

The register is maintained for hands-on IT administration, ITIL 4 practice, technical documentation, and professional portfolio development.

Previously documented configurations are not considered currently verified until supporting evidence is collected.
