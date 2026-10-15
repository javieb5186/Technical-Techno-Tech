# Configuration Item (CI) Register and Documentation Standards

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Configuration Management  
**Document Type:** Configuration Item Documentation Guide  
**Document ID:** GUIDE-SCM-001  
**Version:** 1.0  
**Status:** Draft — Lab Documentation Standard  
**Function:** Internal IT  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

## 1. Purpose

This directory contains the Configuration Item (CI) records for Technical Techno Tech's simulated internal IT infrastructure.

Its purpose is to provide a consistent method for identifying, documenting, organizing, verifying, updating, and maintaining information about the components that support IT services.

The directory supports the ITIL 4 Service Configuration Management practice.

The objectives are to:

- Maintain accurate information about relevant IT infrastructure components.
- Establish consistent CI naming and identification standards.
- Document configuration attributes and technical baselines.
- Identify relationships between CIs and IT services.
- Support incident investigation and troubleshooting.
- Improve change impact assessment.
- Support problem investigation and root cause analysis.
- Provide information for monitoring and security activities.
- Maintain traceability between configuration changes and supporting records.
- Demonstrate configuration management practices through documented technical labs.

**Key Principle:** A Configuration Item record should describe a component's verified configuration and relationships, not simply identify that the component exists.

---

## 2. ITIL 4 Alignment

The purpose of the ITIL 4 Service Configuration Management practice is to ensure that accurate and reliable information about the configuration of services, and the configuration items that support them, is available when and where needed.

A **Configuration Item (CI)** is any component that needs to be managed to deliver an IT service.

Examples include:

- Servers
- Workstations
- Network devices
- Virtual machines
- Applications
- Cloud services
- Databases
- Infrastructure services
- Service configurations

### Configuration Item vs. IT Asset

Although a component can be both an IT asset and a CI, these concepts have different purposes.

| IT Asset | Configuration Item |
|---|---|
| Focuses on financial, contractual, and lifecycle value | Focuses on configuration and service relationships |
| May track cost, ownership, and procurement | May track roles, settings, dependencies, and operational status |
| Supports IT Asset Management | Supports Service Configuration Management |
| Can exist without being a CI | Can exist without being a separately tracked financial asset |

**Example:** DC01 may be tracked as a virtual machine asset while also being documented as a CI supporting Active Directory authentication and DNS services.

### Configuration Management System

In a production organization, configuration information may be managed through a Configuration Management Database (CMDB) or a broader Configuration Management System (CMS).

For this portfolio, GitHub Markdown files serve as a lightweight, manually maintained configuration documentation repository.

This repository is **not presented as an enterprise CMDB** and does not provide automatic discovery, synchronization, or configuration verification.

---

## 3. Directory Scope

This directory contains records for selected components that support Technical Techno Tech's internal IT services.

### Supported CI Categories

| Category | Directory | Examples |
|---|---|---|
| Servers | `Servers/` | Domain controllers, member servers |
| Workstations | `Workstations/` | Windows administrative and client devices |
| Network Devices | `Network-Devices/` | Routers, switches, firewalls |
| Cloud Services | `Cloud-Services/` | Microsoft 365, Entra ID, Intune, Azure resources |

### Directory Structure

```text
Configuration-Items/
├── README.md
├── Servers/
├── Workstations/
├── Network-Devices/
└── Cloud-Services/
```

Individual CI records should be created inside the appropriate category directory.

### Scope Considerations

Not every physical or virtual component must become a separate CI.

A component should be registered when its configuration, status, or relationships are important to service delivery, support, security, or change management.

---

## 4. Configuration Item Identification

Every registered CI must have a unique identifier.

### Proposed Naming Convention

```text
CI-###
```

### Examples

```text
CI-001
CI-002
CI-003
CI-004
```

### Identification Rules

1. Assign a unique CI ID when registering a component.
2. Do not reuse retired CI IDs.
3. Retain the CI ID throughout the component's documented lifecycle.
4. Use the same ID in related incidents, problems, changes, and improvement records.
5. Avoid assigning multiple CI IDs to the same component unless separate managed configuration entities are intentionally defined.
6. Distinguish the CI ID from the hostname, display name, and asset identifier.

### Example

| Attribute | Value |
|---|---|
| CI ID | CI-001 |
| CI Name | DC01 |
| CI Type | Server |
| Hostname | DC01 |
| Domain | homelab.local |

**Important:** These values identify an illustrative lab CI. The complete CI record must be verified against the actual environment.

---

## 5. CI Naming Standards

CI names should be consistent, recognizable, and suitable for cross-referencing.

### Naming Principles

- Use the actual hostname or service name where appropriate.
- Maintain consistent capitalization.
- Avoid ambiguous names.
- Avoid unnecessary special characters.
- Distinguish physical devices from logical services.
- Keep names stable when possible.

### Example Naming Patterns

| CI Type | Example |
|---|---|
| Domain Controller | DC01 |
| Domain Controller | DC02 |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Router | RTR01 |
| Switch | SW01 |
| Firewall | FW01 |
| Cloud Service | Microsoft-Entra-ID |

Names such as RTR01, SW01, and FW01 are illustrative conventions, not claims that those devices currently exist in the lab.

---

## 6. CI Record File Naming

Use a predictable filename for each CI.

### Recommended Format

```text
CI-###-CI-Name.md
```

### Examples

```text
CI-001-DC01.md
CI-002-DC02.md
CI-003-MGMT01.md
CI-004-CLIENT01.md
```

### Example Directory Organization

```text
Configuration-Items/
├── README.md
├── Servers/
│   ├── CI-001-DC01.md
│   └── CI-002-DC02.md
├── Workstations/
│   ├── CI-003-MGMT01.md
│   └── CI-004-CLIENT01.md
├── Network-Devices/
└── Cloud-Services/
```

This is a proposed structure.

Files should be added only when their corresponding CI records are created.

---

## 7. Required CI Attributes

Each Configuration Item record should contain sufficient information to identify, understand, and manage the component.

### Core Attributes

| Attribute | Description | Required |
|---|---|---|
| CI ID | Unique identifier | Yes |
| CI Name | Recognizable component name | Yes |
| CI Type | Server, workstation, network device, cloud service, etc. | Yes |
| Description | Purpose of the component | Yes |
| Environment | Lab, test, production, etc. | Yes |
| Lifecycle Status | Current lifecycle state | Yes |
| Operational Status | Current observed operating condition | Yes |
| Owner | Responsible role or function | Yes |
| Location | Physical, virtual, or cloud environment | When applicable |
| Hostname | Device hostname | When applicable |
| Operating System | OS and version | When applicable |
| IP Address | Verified addressing information | When applicable |
| Domain/Tenant | Associated identity environment | When applicable |
| Installed Roles | Relevant server or service roles | When applicable |
| Dependencies | Related CIs and services | Yes, or explicitly none/unknown |
| Last Verified | Date of last configuration verification | Yes, if verified |
| Evidence | Supporting technical evidence | When available |

### Optional Attributes

- Asset identifier
- Hardware specifications
- VM resource allocation
- Installed applications
- Software versions
- Patch status
- Backup requirements
- Monitoring coverage
- Security classification
- Administrative access model
- Recovery requirements
- Related changes
- Related incidents
- Related problems
- Related improvements
- Maintenance requirements

### Unknown Information

If an attribute has not been verified, use an explicit value such as:

- `Not Yet Verified`
- `Not Yet Documented`
- `Not Applicable`
- `Pending Assessment`

Do not invent technical specifications to complete a record.

---

## 8. CI Lifecycle Statuses

Each CI should have a documented lifecycle status.

### Proposed Lifecycle Model

| Status | Description |
|---|---|
| Proposed | Component identified for potential deployment |
| Planned | Deployment or registration planned |
| Under Configuration | Component being configured |
| Testing | Component undergoing technical validation |
| Active | Component is in operational use |
| Under Maintenance | Component undergoing maintenance |
| Suspended | Component temporarily removed from service |
| Retired | Component permanently removed from service |
| Archived | Historical record retained for reference |

### Lifecycle Flow

```text
Proposed
   |
   v
Planned
   |
   v
Under Configuration
   |
   v
Testing
   |
   v
Active
   |
   +------> Under Maintenance
   |               |
   |               v
   |             Active
   |
   +------> Suspended
   |             |
   |             v
   |           Active
   |
   v
Retired
   |
   v
Archived
```

This is a proposed model, not a mandatory ITIL 4 lifecycle.

Actual transitions may differ based on the component and operating environment.

### Important

A CI lifecycle status is different from its operational health.

For example:

- Lifecycle Status: Active
- Operational Status: Degraded

Both attributes can be true simultaneously.

---

## 9. CI Operational Status

Operational status describes the component's observed operating condition.

### Proposed Status Values

| Status | Description |
|---|---|
| Operational | Required functions verified as working |
| Degraded | Some functions are impaired |
| Unavailable | Component or required service is unavailable |
| Maintenance | Component is intentionally undergoing maintenance |
| Unknown | Current operational condition has not been verified |

### Evidence Requirements

An operational status should be based on actual observations.

Examples include:

- Service checks
- Connectivity tests
- Event logs
- Administrative console observations
- Application health checks
- Monitoring information

**Important:** A successful ping does not prove that every service hosted by a system is operational.

---

## 10. Configuration Baselines

A configuration baseline documents an agreed or recorded configuration state used for comparison.

Baselines help identify unexpected or unauthorized changes.

### Potential Baseline Attributes

**Servers**

- Operating system version
- Installed roles
- IP configuration
- DNS settings
- Domain membership
- Relevant services
- Security configuration

**Workstations**

- Operating system version
- Domain or Entra join state
- Management enrollment
- Security settings
- Installed software

**Network Devices**

- Interface configuration
- VLAN assignments
- Routing settings
- Firewall policies
- Management configuration

**Cloud Services**

- Tenant configuration
- Applicable licensing
- Identity settings
- Administrative role assignments
- Management policies
- Relevant service configuration

### Baseline Requirements

1. Identify the component.
2. Document relevant configuration attributes.
3. Record the source of the information.
4. Identify the collection date.
5. Distinguish observed configuration from an approved target baseline.
6. Preserve evidence where appropriate.
7. Review changes against the applicable baseline.

### Important

A snapshot of current settings is not automatically an approved configuration baseline.

A formally approved baseline requires an appropriate authorization process.

---

## 11. CI Relationships and Dependencies

Configuration Items often depend on other components to deliver an IT service.

### Relationship Types

| Relationship | Meaning |
|---|---|
| Depends On | CI requires another component or service |
| Hosts | CI provides a platform for another component |
| Hosted On | CI operates on another platform |
| Connects To | CI communicates with another component |
| Authenticates Through | CI relies on an identity service |
| Resolves Through | CI relies on DNS resolution |
| Managed By | CI is administered through another system |
| Monitored By | CI is observed by a monitoring system |
| Supports | CI contributes to delivery of an IT service |

### Example

```text
CLIENT01
   |
   | Authenticates Through
   v
Active Directory Domain Services
   |
   | Provided By
   v
DC01 / DC02
```

This diagram represents a conceptual service dependency. Actual authentication behavior and domain controller selection depend on the configured environment.

### Dependency Documentation Requirements

- Identify the source CI.
- Identify the target CI or service.
- Define the relationship.
- Record the dependency's purpose.
- Identify service impact.
- Verify the relationship where practical.
- Link the applicable dependency map.

### Related Directory

[Dependency Maps](../Dependency-Maps/)

---

## 12. CI Relationship to IT Services

Each CI should identify the internal IT services it supports.

### Service Mapping

| Service ID | Service | Example Supporting CIs |
|---|---|---|
| IT-SVC-001 | Identity & Access Management | Domain controllers, Entra ID |
| IT-SVC-002 | Endpoint Management | Workstations, Intune |
| IT-SVC-003 | Microsoft 365 & Collaboration | Microsoft 365 services |
| IT-SVC-004 | Network Connectivity | Routers, switches, firewalls |
| IT-SVC-005 | Server & Infrastructure Services | Windows servers, Hyper-V infrastructure |
| IT-SVC-006 | Information Security | Security controls, identity systems |
| IT-SVC-007 | Employee IT Lifecycle | Identity, endpoint, and collaboration systems |

These are conceptual examples.

Actual service-to-CI relationships should be documented only after verification.

### Why Service Mapping Matters

Service mapping helps determine:

- Which services may be affected by a failed CI.
- Which components are relevant to incident investigation.
- Which dependencies must be considered during changes.
- Which technical risks could affect business operations.
- Which components should be included in monitoring.

---

# 13. CI Registration Procedure

Use the following workflow when creating a new Configuration Item record.

### Step 1 — Identify the Component

Determine which component requires configuration management.

Examples:

- Windows Server domain controller
- Windows workstation
- Router
- Firewall
- Microsoft cloud service

### Step 2 — Confirm CI Scope

Determine whether the component's configuration or relationships are important to service delivery.

### Step 3 — Check for Existing Records

Search the repository to prevent duplicate CI registration.

### Step 4 — Assign a CI Identifier

Use the next available identifier following the `CI-###` convention.

### Step 5 — Select the CI Category

Choose:

- `Servers/`
- `Workstations/`
- `Network-Devices/`
- `Cloud-Services/`

### Step 6 — Create the Record

Use the existing template:

[Configuration Item Template](../../Templates/Configuration-Item-Template.md)

### Step 7 — Record Core Attributes

Document identification, ownership, environment, and relevant technical information.

### Step 8 — Collect Configuration Evidence

Gather actual configuration information from the lab.

### Step 9 — Document Dependencies

Identify related CIs and supported services.

### Step 10 — Verify the Record

Compare recorded information with the observed configuration.

### Step 11 — Record Verification Status

Identify which attributes were verified and which remain unknown.

### Step 12 — Link Related Documentation

Connect the CI to applicable infrastructure documentation, dependency maps, and operational records.

### Step 13 — Maintain the Record

Update the CI when relevant configuration or lifecycle changes occur.

**Expected Result:** A consistent, traceable CI record supported by available evidence.

---

# 14. CI Verification Procedure

Configuration records should be periodically checked against the actual environment.

### Verification Activities

1. Identify the CI to review.
2. Confirm access to the relevant system.
3. Review its current configuration.
4. Compare observed settings with the CI record.
5. Identify missing or outdated information.
6. Determine whether discrepancies are expected.
7. Check for related authorized changes.
8. Correct documentation errors.
9. Escalate unexplained configuration discrepancies when appropriate.
10. Record the verification date and evidence.

### Verification Outcomes

| Outcome | Description |
|---|---|
| Verified | Required recorded attributes match observations |
| Partially Verified | Some attributes confirmed; others remain unresolved |
| Discrepancy Identified | Recorded and observed values differ |
| Unable to Verify | Required access or evidence unavailable |
| Not Yet Verified | Verification has not been performed |

### Important

Verification does not mean that the configuration is secure or meets every operational requirement.

Configuration accuracy, policy compliance, and operational health may require separate assessments.

---

# 15. Hands-On Lab — Server CI Documentation

## Example: DC01

**Proposed CI ID:** CI-001  
**CI Name:** DC01  
**CI Category:** Server  
**Environment:** Hyper-V Lab  
**Domain:** `homelab.local`  
**Known Lab IP Address:** `10.20.10.10`

### Example Attributes

| Attribute | Example Value |
|---|---|
| CI ID | CI-001 |
| CI Name | DC01 |
| CI Type | Windows Server |
| Domain | homelab.local |
| IP Address | 10.20.10.10 |
| Server Role | Domain Controller |
| Additional Roles | Verify installed roles |
| Lifecycle Status | Verify current status |
| Operational Status | Not Yet Verified |
| Configuration Baseline | Not Yet Established |
| Last Verified | Pending |

### Suggested PowerShell Checks

**Identify the computer and operating system:**

```powershell
Get-ComputerInfo |
Select-Object CsName, WindowsProductName, WindowsVersion, OsBuildNumber
```

**Inspect network configuration:**

```powershell
Get-NetIPConfiguration
```

**Inspect installed server roles:**

```powershell
Get-WindowsFeature |
Where-Object InstallState -eq 'Installed'
```

**Inspect domain controller information:**

```powershell
Get-ADDomainController -Identity DC01
```

**Inspect relevant services:**

```powershell
Get-Service -Name NTDS, DNS -ErrorAction SilentlyContinue
```

### Verification Notes

- Commands must be executed in an appropriate environment.
- Some commands require administrative permissions or installed modules.
- Missing command output does not automatically indicate a configuration failure.
- Verify role information before adding it to the CI record.
- Do not publish sensitive configuration details.

### Expected Documentation

After verification, the corresponding CI record should identify:

- Actual operating system
- Actual installed roles
- Verified IP configuration
- Domain membership
- Service relationships
- Operational status
- Evidence references

No command execution or verification is claimed by this example.

---

# 16. Hands-On Lab — Workstation CI Documentation

## Example: MGMT01

**Proposed CI ID:** CI-003  
**CI Name:** MGMT01  
**CI Category:** Workstation  
**Known Lab IP Address:** `10.20.30.10`

### Suggested PowerShell Checks

**Computer information:**

```powershell
Get-ComputerInfo |
Select-Object CsName, WindowsProductName, WindowsVersion
```

**Network configuration:**

```powershell
Get-NetIPConfiguration
```

**Domain membership:**

```powershell
Get-CimInstance Win32_ComputerSystem |
Select-Object Name, Domain, PartOfDomain
```

**Local administrators:**

```powershell
Get-LocalGroupMember -Group Administrators
```

### Documentation Considerations

- Operating system
- Domain membership
- Management role
- IP configuration
- Installed administrative tools
- Local administrative access
- Relevant dependencies

### Important

Local administrator membership can contain sensitive identity information.

Sanitize output before publication.

---

# 17. Hands-On Lab — Network Device CI Documentation

Network device records should describe verified network configuration and service dependencies.

### Potential CI Types

- Router
- Switch
- Firewall
- Wireless access point
- Virtual network appliance

### Required Network Attributes

- Device name
- Device type
- Platform
- Management method
- Interface information
- IP addressing
- Relevant VLANs
- Routing role
- Security function
- Connected devices
- Supported services

### Example Cisco Verification Commands

```text
show version
show ip interface brief
show interfaces
show vlan brief
show ip route
```

Command availability depends on device platform and supported features.

### Example OPNsense Documentation

Record applicable:

- Interface assignments
- IP addressing
- Firewall zones
- Routing
- DHCP configuration
- DNS configuration
- VPN services
- Relevant security policies

### Example VyOS Documentation

Record applicable:

- Interface configuration
- Routing configuration
- Firewall rules
- NAT configuration
- Relevant services

### Important

Do not publish:

- Passwords
- Private keys
- API tokens
- Sensitive management access details
- Confidential network configurations

---

# 18. Hands-On Lab — Cloud Service CI Documentation

Cloud service CIs may represent logical services rather than individual physical devices.

### Potential Cloud CIs

- Microsoft Entra ID tenant
- Microsoft 365 tenant
- Microsoft Intune service
- Azure virtual machine
- Azure virtual network
- Azure storage service

### Suggested Attributes

| Attribute | Description |
|---|---|
| CI Name | Cloud service or resource name |
| Provider | Microsoft or other provider |
| Service Type | Identity, endpoint, compute, storage, etc. |
| Environment | Lab or test |
| Administrative Owner | Responsible role |
| Service Dependencies | Required related services |
| Licensing | Applicable licensing requirements |
| Security Controls | Relevant access and protection settings |
| Operational Status | Verified service condition |
| Last Verified | Verification date |

### Microsoft Entra ID Example

A tenant-level CI might document:

- Tenant display name
- Identity service purpose
- Relevant administrative roles
- Authentication requirements
- Relationship to Microsoft 365
- Relationship to device management

### Important

Cloud service availability, licensing, and configuration can change.

Records should distinguish verified settings from planned capabilities.

---

# 19. CI Changes and Change Enablement

Configuration changes may affect registered CIs.

### Examples

- Server IP address changes
- DNS configuration changes
- Installed role changes
- Firewall rule changes
- Domain controller promotion or demotion
- Network routing changes
- Cloud policy changes
- Virtual machine resource changes

### Documentation Procedure

1. Identify the affected CI.
2. Review the planned change.
3. Determine authorization requirements.
4. Record the relevant Change ID where applicable.
5. Capture necessary baseline information.
6. Implement the authorized change.
7. Verify the actual configuration.
8. Update the CI record.
9. Update affected dependencies.
10. Record the verification date.

### Important

Updating a CI record does not authorize the underlying technical change.

Technical changes must follow the applicable Change Enablement requirements.

### Related Procedures

- [Change Authorization](../../Change-Enablement/Procedures/Change-Authorization.md)
- [Change Implementation](../../Change-Enablement/Procedures/Change-Implementation.md)
- [Change Review](../../Change-Enablement/Procedures/Change-Review.md)

---

# 20. CI Relationships With Other ITIL Practices

| Practice | How CI Records Are Used |
|---|---|
| Service Desk | Identify affected components during ticket intake |
| Incident Management | Support troubleshooting and service impact assessment |
| Service Request Management | Identify resources affected by requests |
| Knowledge Management | Link technical procedures to relevant components |
| Problem Management | Support root cause and dependency analysis |
| Change Enablement | Support impact assessment and configuration updates |
| Monitoring and Event Management | Associate events and alerts with affected components |
| Service Configuration Management | Maintain accurate configuration information |
| Information Security Management | Identify critical systems and relevant security controls |
| Continual Improvement | Identify configuration documentation and reliability improvements |

### Important

CI records are shared information resources.

They do not require a separate approval or sequential handoff through every ITIL practice.

---

# 21. CI Evidence Standards

Every completed CI record should contain or reference evidence appropriate to the component.

### Acceptable Evidence

- PowerShell command output
- Windows Server administrative console screenshots
- Active Directory administrative information
- Network device command output
- Azure resource configuration screenshots
- Microsoft 365 configuration information
- Hyper-V virtual machine settings
- Configuration exports with sensitive information removed

### Evidence Requirements

Each evidence item should identify:

1. CI ID
2. Component name
3. Date collected
4. Source system
5. Configuration attribute verified
6. Actual observed value
7. Verification result

### Evidence Integrity

Do not fabricate:

- Installed roles
- IP addresses
- Operating system versions
- Device configurations
- Service relationships
- Successful tests
- Change approvals
- Verification dates

### Sanitization

Remove or redact:

- Credentials
- Tokens
- Secrets
- Private keys
- Sensitive personal information
- Confidential tenant identifiers
- Information that could expose real systems

---

# 22. CI Review and Maintenance

Configuration records should be reviewed when relevant changes occur.

### Review Triggers

- New CI deployment
- Configuration change
- Incident investigation
- Problem investigation
- Security finding
- Monitoring discrepancy
- Infrastructure migration
- Service dependency change
- CI retirement
- Scheduled configuration review

### Proposed Review Frequency

| CI Criticality | Suggested Review |
|---|---|
| High | Quarterly or after significant changes |
| Medium | Semiannually or after significant changes |
| Low | Annually or when changes occur |

These intervals are proposed lab documentation standards, not mandatory ITIL requirements.

### Review Checklist

- [ ] CI still exists
- [ ] CI name is accurate
- [ ] CI type is accurate
- [ ] Owner is identified
- [ ] Lifecycle status is current
- [ ] Operational status is supported by evidence
- [ ] Relevant configuration attributes are accurate
- [ ] Supported services are documented
- [ ] Dependencies are current
- [ ] Related changes are linked
- [ ] Evidence is appropriately sanitized
- [ ] Last verification date is updated

---

# 23. CI Retirement and Archiving

When a component is permanently removed from service, its CI record should be updated.

### Retirement Procedure

1. Identify the CI.
2. Confirm the retirement decision.
3. Determine applicable authorization requirements.
4. Review supported services.
5. Identify dependent CIs.
6. Verify replacement arrangements where applicable.
7. Record the actual retirement activity.
8. Update the lifecycle status.
9. Update dependency maps.
10. Retain historical information according to applicable documentation requirements.

### Important

Deleting a virtual machine does not automatically mean every related service dependency has been removed.

Dependencies and supporting records must be reviewed separately.

### Archived Records

Retired CI records may be retained to support:

- Historical troubleshooting
- Change analysis
- Incident investigation
- Security review
- Infrastructure documentation
- Portfolio evidence

Do not delete useful historical information solely because the component is no longer active.

---

# 24. Common Configuration Documentation Errors

### Error 1 — Recording Unverified Information

**Incorrect:** Assuming a server runs a particular operating system version.

**Correct:** Verify the version before documenting it as fact.

### Error 2 — Missing Dependencies

**Incorrect:** Documenting DC01 without identifying its relationship to Active Directory and DNS services.

**Correct:** Record relevant service dependencies.

### Error 3 — Confusing Assets With CIs

**Incorrect:** Treating every purchased item as automatically requiring a CI record.

**Correct:** Register components according to their configuration management relevance.

### Error 4 — Outdated Configuration

**Incorrect:** Leaving an old IP address in a CI record after a verified change.

**Correct:** Update the record when the configuration changes.

### Error 5 — Missing Change References

**Incorrect:** Recording a significant configuration change without linking its applicable change documentation.

**Correct:** Maintain traceability where appropriate.

### Error 6 — Unsupported Operational Status

**Incorrect:** Marking a server operational without performing relevant checks.

**Correct:** Record the observed condition or mark it unknown.

### Error 7 — Duplicated CI Records

**Incorrect:** Creating multiple records for the same managed component without justification.

**Correct:** Search existing records before registration.

### Error 8 — Sensitive Information Exposure

**Incorrect:** Publishing administrative credentials or confidential configuration details.

**Correct:** Sanitize evidence before committing it to GitHub.

### Error 9 — Confusing Current Configuration With Approved Baseline

**Incorrect:** Treating an observed setting as an approved organizational standard.

**Correct:** Distinguish actual configuration from approved target configuration.

### Error 10 — Treating GitHub as an Automated CMDB

**Incorrect:** Assuming Markdown records automatically reflect live infrastructure.

**Correct:** Verify and maintain records manually or through explicitly documented automation.

---

# 25. CI Documentation Quality Checklist

## Identification

- [ ] Unique CI ID assigned
- [ ] CI name recorded
- [ ] CI type identified
- [ ] Correct category directory selected
- [ ] Duplicate records checked

## Configuration

- [ ] Environment identified
- [ ] Owner documented
- [ ] Relevant operating system or platform recorded
- [ ] Network configuration documented where applicable
- [ ] Installed roles or functions recorded
- [ ] Lifecycle status identified
- [ ] Operational status identified
- [ ] Unknown values clearly marked

## Relationships

- [ ] Supported services identified
- [ ] Related CIs identified
- [ ] Dependencies documented
- [ ] Relevant dependency maps linked

## Verification

- [ ] Configuration information checked
- [ ] Evidence collected where appropriate
- [ ] Verification outcome documented
- [ ] Last verification date recorded
- [ ] Discrepancies identified

## Security

- [ ] Sensitive information removed
- [ ] Credentials excluded
- [ ] Access-related information sanitized
- [ ] Relevant security requirements considered

## Maintenance

- [ ] Related changes linked where applicable
- [ ] Record reflects current known configuration
- [ ] Review requirements identified
- [ ] Historical changes retained where relevant

## Portfolio Accuracy

- [ ] Proposed configurations distinguished from implemented configurations
- [ ] Actual lab results supported by evidence
- [ ] No fabricated technical results
- [ ] No simulated approval represented as independent authorization

---

# 26. Document Review

Review this guide when:

- CI categories change.
- Naming conventions change.
- New infrastructure platforms are introduced.
- Configuration attributes change.
- Dependency documentation requirements change.
- New verification methods are adopted.
- Configuration management procedures are revised.
- Significant documentation inconsistencies are identified.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Configuration Item documentation standards and directory guide |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This directory and documentation guide demonstrate the application of ITIL 4 Service Configuration Management principles to a simulated corporate IT environment.

Configuration Item identifiers, lifecycle models, documentation standards, and organizational responsibilities are proposed for portfolio purposes.

Technical configuration information should be treated as verified only when supported by actual lab observations and evidence.

Example device names, commands, relationships, and directory structures do not establish that a component has been deployed, configured, tested, or registered.

Simulated approvals and organizational responsibilities do not constitute independent authorization or professional employment experience.

GitHub Markdown files are used as a lightweight configuration documentation system and are not represented as an automatically synchronized enterprise CMDB.

The purpose of this documentation is to demonstrate configuration identification, configuration record management, technical verification, service dependency mapping, change traceability, and lifecycle management.
