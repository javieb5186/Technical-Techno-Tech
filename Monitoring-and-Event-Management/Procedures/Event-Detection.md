# SOP — Event Detection

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Monitoring and Event Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-MEM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Monitoring and Event Management

---

## 1. Purpose

This procedure establishes a standardized method for detecting and initially evaluating events affecting Technical Techno Tech's internal IT services and supporting infrastructure.

Event Detection enables IT personnel to recognize changes in the operational state of services, infrastructure components, applications, and security-related systems.

Effective event detection helps identify abnormal conditions before they develop into significant service disruptions.

This procedure supports:

- Early identification of infrastructure failures
- Detection of abnormal system behavior
- Monitoring of service availability
- Identification of performance degradation
- Recognition of security-related events
- Consistent event documentation
- Reduced incident detection time
- Improved operational visibility
- Identification of potential problems
- Proactive infrastructure maintenance
- Continual improvement

**Key Principle:** Not every event is an incident. Events must be evaluated to determine whether they represent normal activity, a condition requiring attention, or an actual service disruption.

---

## 2. Scope

This procedure applies to monitoring activities involving Technical Techno Tech's internal IT services and supporting infrastructure.

### Supported Services

| Service ID | Service Name |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

### Technical Environments

Event detection may involve:

- Windows 11 workstations
- Windows Server
- Active Directory Domain Services
- Group Policy
- DNS and DHCP
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V virtualization
- Network routers and switches
- OPNsense
- VyOS

### Monitoring Areas

- System availability
- Service health
- Resource utilization
- Network connectivity
- Authentication activity
- Application errors
- Configuration changes
- Backup operations
- Security events
- Infrastructure performance

Only technologies actually configured in the lab should be described as actively monitored.

---

## 3. ITIL 4 Monitoring and Event Management

### Purpose

The purpose of Monitoring and Event Management is to systematically observe services and service components and record and report selected changes of state identified as events.

### Important Definitions

**Monitoring:** Repeated observation of a system, service, or process to detect events and verify operational conditions.

**Event:** Any change of state that has significance for the management of a service or other Configuration Item.

**Alert:** A notification that a threshold has been reached, something has changed, or a failure has occurred.

**Incident:** An unplanned interruption to a service or a reduction in the quality of a service.

**Configuration Item (CI):** A component that needs to be managed to deliver an IT service.

**Threshold:** A defined value or condition used to determine when monitoring should generate an alert.

**False Positive:** An alert indicating a condition that investigation determines does not represent the suspected issue.

**False Negative:** A relevant condition that the monitoring approach fails to detect or report.

### Event vs. Alert vs. Incident

| Concept | Description | Example |
|---|---|---|
| Event | Significant change of state | Windows service stops |
| Alert | Notification generated from a condition | Monitoring reports that the service is stopped |
| Incident | Actual service disruption or degradation | Employees cannot use the affected application |

An event may generate an alert.

An alert may lead to an Incident record.

However, neither relationship is automatic.

---

## 4. Event Detection Principles

Technical Techno Tech follows these principles when detecting events.

### 4.1 Monitor Relevant Services

Monitoring should focus on systems and components that support business services.

### 4.2 Establish Normal Operating Conditions

Understand expected system behavior before defining abnormal conditions.

### 4.3 Use Appropriate Monitoring Methods

Select monitoring tools and checks according to the technology and operational requirements.

### 4.4 Prioritize Actionable Events

Focus on events that provide useful information or require an operational response.

### 4.5 Reduce Alert Noise

Avoid generating unnecessary alerts for expected or insignificant activity.

### 4.6 Preserve Event Evidence

Record sufficient information to support investigation and future analysis.

### 4.7 Evaluate Business Impact

Consider whether the detected condition affects service delivery.

### 4.8 Maintain Security

Monitoring activities must follow applicable access, privacy, and security requirements.

### 4.9 Support Proactive Management

Use trends and warning conditions to identify risks before failures occur.

### 4.10 Maintain Traceability

Link significant events to relevant incidents, problems, changes, and Configuration Items.

---

## 5. Roles and Responsibilities

### Monitoring Analyst / Technician

Responsible for:

- Reviewing monitoring results
- Detecting abnormal conditions
- Evaluating alerts
- Recording significant events
- Performing initial verification
- Escalating relevant findings

### Systems Administrator

Responsible for:

- Monitoring Windows Server
- Reviewing Active Directory health
- Evaluating Windows services
- Investigating system performance
- Reviewing server-related event logs

### Network Administrator

Responsible for:

- Monitoring network connectivity
- Reviewing router and switch conditions
- Evaluating network performance
- Investigating interface and routing events
- Reviewing firewall-related alerts

### Cloud Administrator

Responsible for:

- Reviewing Microsoft 365 service health
- Evaluating Entra ID events
- Monitoring relevant Azure resources
- Reviewing available cloud diagnostic information

### Endpoint Support Specialist

Responsible for:

- Reviewing workstation-related events
- Investigating endpoint failures
- Evaluating application errors
- Identifying recurring endpoint issues

### Information Security Personnel

Responsible for:

- Reviewing security-related events
- Evaluating suspicious activity
- Coordinating applicable security investigations
- Recommending security monitoring improvements

### Service Desk

Responsible for:

- Receiving relevant monitoring notifications
- Recording associated incidents
- Communicating service disruptions
- Supporting escalation and follow-up

### Service Configuration Management

Responsible for maintaining relevant Configuration Item information and dependencies used to interpret events.

**Lab Note:** These responsibilities represent simulated organizational roles. A single learner may perform multiple roles in a controlled lab exercise.

---

## 6. Event Detection Sources

Events may originate from several technical and operational sources.

### 6.1 Operating System Events

Examples:

- Service failures
- System startup and shutdown
- Driver errors
- Application crashes
- Disk errors
- Authentication failures

Potential tools:

- Windows Event Viewer
- PowerShell
- Windows Performance Monitor

### 6.2 Infrastructure Events

Examples:

- Server unavailable
- High CPU utilization
- Low disk capacity
- Memory pressure
- Backup failure
- Virtual machine failure

### 6.3 Network Events

Examples:

- Network interface failure
- Packet loss
- High latency
- Routing instability
- DNS resolution failure
- Firewall connectivity issue

Potential tools:

- Network device logs
- Syslog
- SNMP monitoring
- ICMP connectivity checks
- OPNsense
- VyOS

### 6.4 Cloud Events

Examples:

- Cloud service disruption
- Failed authentication
- Device compliance change
- Resource health issue
- Administrative configuration change

Potential sources:

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Azure Monitor
- Azure Activity Log

Availability depends on licensing, permissions, resource configuration, and enabled logging.

### 6.5 Security Events

Examples:

- Repeated failed sign-in attempts
- Unexpected privileged activity
- Security policy changes
- Endpoint protection detections
- Suspicious network activity

Security-related events should be evaluated under applicable Information Security Management procedures.

---

## 7. Event Categories

Technical Techno Tech uses three primary event categories for operational classification.

### 7.1 Informational Events

Events indicating normal or expected activity.

Examples:

- Successful service startup
- Completed scheduled task
- Successful backup
- Authorized configuration update
- Successful system restart

**Typical Response:** Record or retain according to monitoring requirements. No immediate intervention may be necessary.

### 7.2 Warning Events

Events indicating abnormal conditions or potential future failures.

Examples:

- Increasing disk utilization
- Repeated application warnings
- Elevated CPU usage
- Intermittent connectivity
- Approaching certificate expiration

**Typical Response:** Verify the condition, assess risk, and determine whether further action is required.

### 7.3 Exception Events

Events indicating failures or conditions requiring attention.

Examples:

- Critical service unavailable
- Disk volume inaccessible
- Repeated application crashes
- Domain controller failure
- Significant network connectivity loss

**Typical Response:** Assess service impact and initiate the appropriate operational response.

### Event Classification Table

| Category | Meaning | Example | Initial Action |
|---|---|---|---|
| Informational | Expected or noteworthy activity | Service started | Record if relevant |
| Warning | Potential risk or abnormal condition | Disk capacity approaching threshold | Investigate |
| Exception | Failure or significant abnormal condition | Critical service stopped | Verify impact and respond |

These categories support triage but do not independently determine incident priority.

---

## 8. Monitoring Methods

### 8.1 Active Monitoring

Active monitoring performs checks against systems or services.

Examples:

- Testing connectivity
- Querying service status
- Checking DNS resolution
- Measuring response time
- Reviewing available storage

#### Example

```powershell
Test-Connection -ComputerName 10.20.10.10 -Count 4
```

A successful response supports connectivity to the tested address.

A failed response does not necessarily prove the device is unavailable because ICMP may be blocked.

### 8.2 Passive Monitoring

Passive monitoring collects events generated by systems.

Examples:

- Windows Event Logs
- Syslog messages
- SNMP traps
- Application logs
- Cloud activity logs

### 8.3 Agent-Based Monitoring

A monitoring agent installed on a device collects relevant system information.

Examples of possible measurements:

- CPU usage
- Memory utilization
- Disk capacity
- Service status
- Application performance

### 8.4 Agentless Monitoring

Monitoring is performed remotely without installing a dedicated monitoring agent on the target.

Possible methods include:

- SNMP
- ICMP
- Remote PowerShell
- Supported management APIs
- Remote service checks

### Monitoring Method Selection

| Requirement | Possible Method |
|---|---|
| Server availability | Connectivity or service checks |
| Windows errors | Event Log collection |
| Network interface status | SNMP or device logs |
| Disk capacity | Performance counters or PowerShell |
| Authentication activity | Security and identity logs |
| Cloud resource health | Supported cloud monitoring tools |

The appropriate method depends on the environment and monitoring objective.

---

## 9. Event Detection Workflow

```text
Identify Service or Component
              |
              v
Determine Monitoring Requirements
              |
              v
Identify Configuration Item
              |
              v
Establish Normal Baseline
              |
              v
Select Monitoring Source
              |
              v
Define Detection Conditions
              |
              v
Configure Authorized Monitoring
              |
              v
Verify Data Collection
              |
              v
Detect Event or Alert
              |
              v
Validate Event Information
              |
              v
Classify Event
              |
              v
Assess Operational Significance
              |
              v
Record Relevant Event
              |
              v
Determine Required Response
              |
       +------+------+------+
       |             |      |
 Informational    Warning Exception
       |             |      |
       v             v      v
    Record       Evaluate  Assess Service
    / Retain      Risk       Impact
       |             |      |
       +------+------+------+
              |
              v
     Route or Escalate
       When Required
              |
              v
    Update Event Record
```

---

## 10. Event Detection Procedure

### Step 1 — Identify the Service to Monitor

Determine which internal IT service requires monitoring.

Review:

- Service name
- Service ID
- Business importance
- Supported users
- Service dependencies
- Known operational risks

#### Example

**Service:** IT-SVC-001 — Identity & Access Management

**Monitoring Objective:** Detect conditions affecting Active Directory authentication.

**Expected Result:** The monitoring activity is associated with a defined service.

### Step 2 — Identify Supporting Configuration Items

Determine which infrastructure components support the service.

#### Example

```text
IT-SVC-001 — Identity & Access Management
                 |
                 v
        Active Directory
                 |
        +--------+--------+
        |                 |
       DC01              DC02
        |                 |
        +--------+--------+
                 |
                DNS
                 |
          Domain Clients
```

Potential Configuration Items:

- DC01
- DC02
- DNS services
- Relevant network infrastructure
- Domain-joined workstations

**Expected Result:** Relevant infrastructure dependencies are identified.

### Step 3 — Define Monitoring Objectives

Determine what conditions monitoring should detect.

Examples:

- Server becomes unavailable.
- Critical Windows service stops.
- Disk capacity approaches an unacceptable level.
- Authentication failures increase unexpectedly.
- DNS resolution fails.
- Network connectivity becomes unstable.

### Example

```text
Monitoring Objective:
Detect when the DNS Server service is not running
on a designated domain controller.

Affected Service:
IT-SVC-001 — Identity & Access Management

Affected Component:
DC01

Expected Condition:
DNS Server service is running.
```

**Expected Result:** Monitoring objectives are measurable and documented.

### Step 4 — Establish a Normal Operating Baseline

Record relevant normal operating conditions.

Potential baseline measurements:

- CPU utilization
- Memory usage
- Available disk capacity
- Service status
- Network latency
- Authentication activity
- DNS response behavior

#### Example

**Server:** DC01

**Service:** DNS

**Expected State:** Running

### Diagnostic Command

```powershell
Get-Service -Name DNS
```

The actual output should be recorded when the test is performed.

**Expected Result:** Normal operating conditions are documented.

### Step 5 — Select the Monitoring Source

Choose an appropriate source for the condition being monitored.

| Monitoring Objective | Possible Source |
|---|---|
| Windows service status | PowerShell / Service Control Manager |
| Operating system errors | Windows Event Logs |
| Disk capacity | PowerShell / Performance Monitor |
| Network connectivity | ICMP or service checks |
| DNS functionality | DNS queries |
| Active Directory replication | Replication diagnostics |
| Authentication failures | Available security or identity logs |
| Cloud resource health | Supported Azure monitoring tools |

**Expected Result:** An appropriate monitoring source is selected.

### Step 6 — Define Detection Conditions

Establish the conditions that should be considered significant.

Examples:

- Service state is not Running.
- Disk free space falls below a defined threshold.
- Repeated failures occur within a defined period.
- A monitored endpoint becomes unreachable.
- A required DNS query fails.

### Example

```text
Monitoring Rule:
DNS Service Availability

Condition:
DNS service status is not Running.

Event Category:
Exception

Affected Component:
DC01

Required Action:
Verify service condition and assess impact.
```

**Expected Result:** The event detection condition is clearly defined.

### Step 7 — Define Thresholds Where Appropriate

Thresholds establish when monitored values require attention.

### Illustrative Thresholds

| Metric | Warning | Exception |
|---|---|---|
| Disk Utilization | 80% | 90% |
| CPU Utilization | Above 85% for 10 minutes | Above 95% for 10 minutes |
| Memory Utilization | Above 85% for 10 minutes | Above 95% for 10 minutes |
| Service Status | N/A | Required service stopped |
| Connectivity | Intermittent failures | Sustained failure of required service check |

These are example values, not universal recommendations or confirmed TTT monitoring configurations.

Thresholds should be adjusted according to workload, baseline behavior, business impact, and system capacity.

**Expected Result:** Appropriate detection thresholds are documented.

### Step 8 — Verify Monitoring Permissions

Confirm that the monitoring method uses appropriate permissions.

Review:

- Required administrative access
- Remote management permissions
- Event Log access
- Network access
- Cloud administrative roles
- Monitoring account privileges

### Security Principle

Monitoring should use the least privileges necessary.

Do not use privileged credentials unnecessarily.

**Expected Result:** Monitoring access requirements are satisfied.

### Step 9 — Configure the Monitoring Check

Configure or prepare the approved monitoring method.

#### Example — Windows Service Check

```powershell
Get-Service -Name DNS
```

#### Example — Disk Capacity

```powershell
Get-Volume
```

#### Example — Network Connectivity

```powershell
Test-Connection -ComputerName 10.20.10.10 -Count 4
```

#### Example — DNS Resolution

```powershell
Resolve-DnsName dc01.homelab.local
```

These commands perform individual checks.

They do not automatically provide continuous monitoring, event storage, alerting, or notification.

Those capabilities require additional configuration.

**Expected Result:** The selected monitoring method is prepared.

### Step 10 — Verify Data Collection

Confirm that the monitoring source provides usable information.

Check:

1. Does the command or tool execute?
2. Is the correct system being monitored?
3. Is the expected data available?
4. Are timestamps recorded?
5. Can normal and abnormal states be distinguished?
6. Are monitoring permissions sufficient?

#### Example

```powershell
Get-Service -Name DNS
```

Possible service states include:

- Running
- Stopped
- Paused

The actual state must be recorded from the lab.

**Expected Result:** Monitoring data can be collected and interpreted.

### Step 11 — Detect the Event

Identify when a monitored condition matches a defined event rule.

### Example

**Monitoring Condition:** Required DNS service is not running.

**Observed Condition:** To be recorded during testing.

**Event Trigger:** Service state differs from the expected Running state.

**Expected Result:** A significant change of state is recognized.

### Step 12 — Capture Event Details

Record relevant event information.

### Required Fields

| Field | Description |
|---|---|
| Event ID | Unique event identifier |
| Detection Time | When the event was detected |
| Source | Monitoring tool or system |
| Affected CI | Relevant infrastructure component |
| Service | Related internal IT service |
| Event Description | Observed condition |
| Event Category | Informational, Warning, or Exception |
| Observed Value | Actual measurement or state |
| Expected Value | Baseline or threshold |
| Evidence | Supporting logs or diagnostic results |
| Initial Status | New, Under Review, or other defined status |

### Example

```text
Event ID: EVT-001

Event Title:
DNS Service Not Running

Affected Service:
IT-SVC-001

Affected CI:
DC01

Event Category:
Exception

Detection Method:
PowerShell Service Status Check

Observed Result:
Pending Lab Validation

Event Status:
Draft
```

**Expected Result:** Event information is documented.

### Step 13 — Validate the Detected Condition

Confirm whether the detected event represents a real and relevant condition.

Possible validation methods:

- Repeat the diagnostic check.
- Review another monitoring source.
- Examine related Event Logs.
- Compare with the baseline.
- Check relevant service dependencies.
- Review recent authorized changes.

#### Example

If monitoring indicates the DNS service is stopped:

```powershell
Get-Service -Name DNS
```

Review relevant service-related system events:

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    StartTime = (Get-Date).AddHours(-1)
} -MaxEvents 50
```

The returned events require interpretation.

**Expected Result:** The detected condition is verified or identified as uncertain.

### Step 14 — Classify the Event

Assign the appropriate category.

### Informational

Expected or noteworthy operational activity.

### Warning

Potential risk or abnormal behavior.

### Exception

Failure or significant abnormal condition requiring attention.

#### Example

**Event:** DNS Server service stops unexpectedly.

**Proposed Classification:** Exception.

Actual impact must still be assessed.

**Expected Result:** The event is classified consistently.

### Step 15 — Assess Service Impact

Determine whether the event affects service delivery.

Questions:

1. Is the affected service unavailable?
2. Are employees experiencing disruption?
3. Is redundancy maintaining functionality?
4. Are dependent services affected?
5. Is performance degraded?
6. Is the condition likely to worsen?

### Example

DC01 experiences a DNS service failure.

If DC02 continues providing required DNS functionality, the immediate business impact may be limited.

However, the event may still represent an infrastructure risk.

**Expected Result:** Operational impact is evaluated.

### Step 16 — Check for Related Events

Review whether similar events have occurred.

Look for:

- Repeated service failures
- Related authentication errors
- Network connectivity warnings
- Disk capacity alerts
- Recent configuration changes
- Events affecting shared infrastructure

### Example

```text
EVT-001 — DNS Service Failure
EVT-002 — Domain Controller Discovery Warning
EVT-003 — Authentication Failure
```

These are illustrative identifiers.

Related events may indicate a shared technical condition, but causation must be investigated.

**Expected Result:** Potential event relationships are identified.

### Step 17 — Determine Whether an Incident Exists

Assess whether the detected condition constitutes an incident.

### Incident Indicators

- Unplanned service interruption
- Reduced service quality
- Employee inability to use a required service
- Significant application failure
- Loss of required connectivity

### Example

**Event:** DNS service stops on DC01.

**Possible Incident:** Employees cannot authenticate because required DNS functionality is unavailable.

If no service interruption or degradation exists, an Incident record may not be necessary.

The event may still require preventive investigation.

**Expected Result:** Incident creation is based on actual service impact.

### Step 18 — Determine Whether Problem Management Is Required

Consider whether the event indicates an actual or potential underlying cause that warrants investigation.

Potential triggers:

- Recurring service failures
- Repeated abnormal warnings
- Persistent resource exhaustion
- Unexplained infrastructure instability
- Recurring configuration defects

### Example

Repeated DNS service failures occur despite temporary restoration.

Problem Management may investigate the underlying cause.

**Expected Result:** Relevant problems are identified for further assessment.

### Step 19 — Route or Escalate the Event

Direct the event to the appropriate technical responsibility.

| Event Type | Potential Responsible Role |
|---|---|
| Windows Server failure | Systems Administrator |
| Active Directory replication issue | Systems Administrator |
| Network interface failure | Network Administrator |
| Firewall alert | Network Administrator / Information Security |
| Endpoint application failure | Endpoint Support Specialist |
| Cloud service issue | Cloud Administrator |
| Suspicious authentication activity | Information Security |

### Escalation Considerations

- Business impact
- Service criticality
- Technical complexity
- Security implications
- Required permissions
- Recurrence

**Expected Result:** Significant events receive appropriate attention.

### Step 20 — Update the Event Record

Record:

- Detection method
- Actual observations
- Validation results
- Event category
- Impact assessment
- Related events
- Escalation decision
- Related Incident or Problem records
- Next required action

### Proposed Event Statuses

- New
- Under Review
- Validated
- Monitoring
- Escalated
- Resolved
- Closed

These are proposed internal workflow statuses.

**Expected Result:** The Event record reflects the current state of evaluation.

---

## 11. Technical Event Detection — Windows Server

Windows Server monitoring may include:

- Service availability
- Operating system errors
- CPU utilization
- Memory utilization
- Disk capacity
- Scheduled task failures
- Application errors
- Backup status

### Example — Service Status

```powershell
Get-Service
```

### Example — Specific Service

```powershell
Get-Service -Name DNS
```

### Example — Recent System Errors

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    Level = 2
    StartTime = (Get-Date).AddDays(-1)
} -MaxEvents 50
```

### Example — Disk Capacity

```powershell
Get-Volume
```

### Example — CPU Utilization

```powershell
Get-Counter '\Processor(_Total)\% Processor Time'
```

### Monitoring Considerations

- Are required services running?
- Are system errors recurring?
- Is disk capacity sufficient?
- Is resource utilization abnormal?
- Are scheduled operations completing?
- Are dependent services functioning?

**Documentation Requirement:** Record actual output and explain the operational significance of relevant findings.

---

## 12. Technical Event Detection — Active Directory

Active Directory monitoring may include:

- Domain controller availability
- Replication health
- DNS functionality
- Authentication activity
- Directory service errors
- Time synchronization
- Group Policy processing

### Example — Domain Controller Diagnostics

```powershell
dcdiag /q
```

### Example — Replication Summary

```powershell
repadmin /replsummary
```

### Example — Replication Details

```powershell
repadmin /showrepl
```

### Example — Domain Controller Discovery

```powershell
nltest /dsgetdc:homelab.local
```

### Example — DNS Resolution

```powershell
Resolve-DnsName dc01.homelab.local
```

### Monitoring Considerations

1. Are domain controllers available?
2. Are replication errors present?
3. Are required DNS records resolving?
4. Are authentication failures increasing?
5. Are time synchronization issues present?
6. Are directory service errors recurring?

### Important

A single successful diagnostic test does not establish continuous Active Directory health.

Monitoring should consider recurring checks, historical data, and relevant service dependencies.

---

## 13. Technical Event Detection — Networking

Network monitoring may include:

- Device availability
- Interface status
- Packet loss
- Latency
- Routing changes
- DNS resolution
- Firewall events
- Network congestion

### Example — Connectivity

```powershell
Test-Connection -ComputerName 10.20.10.10 -Count 4
```

### Example — Network Configuration

```powershell
ipconfig /all
```

### Example — Routing Table

```powershell
route print
```

### Example — DNS Resolution

```powershell
nslookup dc01.homelab.local
```

### Potential Monitoring Technologies

**SNMP**

May provide information about network device interfaces, status, and performance.

**Syslog**

Can collect event messages from supported network devices.

**ICMP**

Can support connectivity and response-time checks.

**OPNsense**

May provide firewall logs and network diagnostic information.

**VyOS**

May provide routing, interface, and system log information.

**Packet Tracer**

Can simulate network conditions and protocol behavior for training.

### Important

Packet Tracer simulation results must not be represented as measurements from physical production infrastructure.

---

## 14. Technical Event Detection — Microsoft 365 and Azure

Cloud monitoring may include:

- Microsoft 365 service health
- Entra ID sign-in activity
- Device compliance
- Cloud resource health
- Administrative changes
- Application availability
- Resource utilization

### Potential Monitoring Sources

| Source | Monitoring Purpose |
|---|---|
| Microsoft 365 Admin Center | Service health and administrative information |
| Microsoft Entra Admin Center | Identity-related events and available logs |
| Microsoft Intune Admin Center | Device and policy status |
| Azure Monitor | Supported resource metrics, logs, and alerts |
| Azure Activity Log | Subscription-level management events |
| Azure Resource Health | Health information for supported Azure resources |

### Monitoring Considerations

- Are required services available?
- Are authentication failures increasing?
- Are managed devices reporting compliance issues?
- Are cloud resources operating as expected?
- Have administrative configurations changed?
- Are monitoring alerts configured appropriately?

### Licensing Considerations

Monitoring features may require specific licenses, permissions, resource configurations, or usage-based charges.

Azure logging, data ingestion, retention, and alerting may incur costs depending on the configuration.

**Lab Note:** Proposed monitoring capabilities should not be described as configured until verified.

---

## 15. Technical Event Detection — Virtualization

Virtualization monitoring may include:

- Virtual machine availability
- Host resource utilization
- Virtual disk capacity
- Virtual network connectivity
- Guest operating system status
- VM startup failures
- Hypervisor errors

### Example

**Monitoring Objective:** Detect when DC01 becomes unavailable.

Potential checks:

1. Verify virtual machine power state.
2. Test guest connectivity.
3. Review guest operating system status.
4. Examine relevant host or guest logs.
5. Evaluate dependent service availability.

### Important

A powered-on virtual machine does not necessarily mean that its guest operating system or hosted services are functioning correctly.

Monitoring should distinguish between:

- Hypervisor state
- Guest operating system state
- Application or service state

---

## 16. Event Detection and Security Monitoring

Security monitoring may identify events requiring specialized investigation.

### Examples

- Repeated failed authentication attempts
- Unexpected privileged account activity
- Security policy changes
- Suspicious network connections
- Endpoint protection alerts
- Unauthorized configuration attempts

### Example — Windows Security Events

Where access and audit configuration permit:

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'Security'
    Id = 4625
    StartTime = (Get-Date).AddHours(-24)
} -MaxEvents 50
```

Windows Security Event ID 4625 records failed logon events.

### Important Considerations

- Audit policy must be configured appropriately.
- The relevant events must exist in the selected log.
- Administrative permissions may be required.
- Failed logons do not automatically indicate malicious activity.
- Investigation should consider normal operational explanations.

Security-sensitive events should be evaluated through Information Security Management and applicable incident response procedures.

---

## 17. Event Detection and Alert Thresholds

Thresholds should be designed to identify meaningful conditions without generating excessive alert noise.

### Static Thresholds

A fixed value triggers an alert.

**Example:** Disk utilization exceeds 90%.

### Duration-Based Thresholds

A condition must persist for a defined period.

**Example:** CPU utilization remains above 90% for 10 minutes.

### Frequency-Based Thresholds

An event occurs repeatedly within a period.

**Example:** A service stops three times within one hour.

### Baseline-Based Detection

Current behavior is compared with established normal conditions.

**Example:** Authentication failures increase significantly above the usual level.

### Threshold Review

Thresholds should be reviewed when:

- Workloads change
- Infrastructure capacity changes
- False positives increase
- Important events are missed
- New services are introduced
- Business requirements change

---

## 18. Event Noise and False Positives

Monitoring systems may generate alerts that do not require intervention.

### Common Causes

- Overly sensitive thresholds
- Expected maintenance activity
- Temporary network interruptions
- Duplicate alerts
- Incorrect monitoring configuration
- Normal workload fluctuations

### Noise Reduction Techniques

- Review thresholds.
- Use duration-based conditions where appropriate.
- Suppress or annotate expected maintenance events.
- Correlate related alerts.
- Remove obsolete monitoring rules.
- Review recurring false positives.

### Important

Alert suppression should not conceal significant service or security failures.

Changes to monitoring rules should follow applicable configuration and change controls.

---

## 19. Event Correlation

Event correlation identifies relationships among multiple events.

### Example

```text
EVT-001 — DNS Service Failure
             |
             v
EVT-002 — DNS Resolution Failure
             |
             v
EVT-003 — Domain Controller Discovery Failure
             |
             v
INC-001 — Employee Authentication Disruption
```

This sequence illustrates a possible relationship.

The actual causal connection must be established through investigation.

### Correlation Factors

- Event timestamps
- Shared Configuration Items
- Common dependencies
- Similar error messages
- Recent changes
- Affected services
- Repeated failure patterns

### Expected Benefit

Event correlation can help technicians identify shared infrastructure conditions and reduce duplicate investigation.

---

## 20. Event Detection Records

Event records are maintained under the Monitoring and Event Management practice.

### Example Directory

```text
Monitoring-and-Event-Management/
├── README.md
├── Procedures/
│   └── Event-Detection.md
└── Records/
    └── EVT-001-DNS-Service-Failure/
        ├── README.md
        └── Evidence/
            ├── 01-Initial-Detection.md
            ├── 02-Service-Status.txt
            ├── 03-System-Event-Logs.txt
            ├── 04-Validation-Results.md
            └── 05-Event-Assessment.md
```

These filenames represent a proposed record structure.

### Event Record Requirements

- Event ID
- Event title
- Detection timestamp
- Monitoring source
- Affected service
- Affected Configuration Item
- Observed condition
- Expected condition
- Event classification
- Initial impact assessment
- Validation results
- Related records
- Escalation decision
- Current status

---

## 21. Event Detection Record Template

Use the following structure for an individual event.

```text
EVENT DETECTION RECORD

Event ID:
Event Title:
Detection Date/Time:
Monitoring Source:
Monitoring Method:

Affected Service:
Affected Configuration Item:
Technical Category:

1. Monitoring Objective

2. Expected Operating Condition

3. Detection Rule / Threshold

4. Observed Condition

5. Event Category

6. Technical Evidence

7. Validation Performed

8. Validation Results

9. Service Impact Assessment

10. Related Events

11. Related Incidents

12. Related Problems

13. Recent Relevant Changes

14. Initial Response

15. Escalation Decision

16. Assigned Responsibility

17. Current Event Status

18. Outstanding Questions

19. Follow-Up Actions

20. Lessons Learned

21. Evidence References
```

---

## 22. Example Event Detection Scenario

### Scenario — DNS Service Failure on DC01

**Event ID:** EVT-001  
**Event Title:** DNS Service Not Running  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Affected CI:** DC01  
**Environment:** homelab.local

### Business Context

Technical Techno Tech uses Active Directory Domain Services for internal identity management.

Domain-joined workstations rely on DNS to locate domain controllers and related services.

### Monitoring Objective

Detect when the DNS Server service on DC01 is not running.

### Expected Condition

```text
System: DC01
Service: DNS
Expected Status: Running
```

### Proposed Detection Method

Run an authorized service status check on DC01:

```powershell
Get-Service -Name DNS
```

### Proposed Detection Rule

```text
Condition:
DNS service status is not Running.

Event Category:
Exception

Initial Action:
Verify service state and assess impact.
```

### Proposed Validation

1. Repeat the service status check.
2. Review relevant Windows Event Logs.
3. Verify DNS resolution.
4. Review the status of DC02.
5. Determine whether affected clients can locate a domain controller.
6. Assess actual service impact.

### Example Diagnostic Commands

**DNS Service Status**

```powershell
Get-Service -Name DNS
```

**DNS Resolution**

```powershell
Resolve-DnsName dc01.homelab.local
```

**Domain Controller Discovery**

```powershell
nltest /dsgetdc:homelab.local
```

**Active Directory Replication Summary**

```powershell
repadmin /replsummary
```

### Potential Event Relationships

```text
EVT-001 — DNS Service Failure
             |
             v
Potential DNS Resolution Problems
             |
             v
Potential Domain Authentication Impact
```

These are possible consequences, not confirmed results.

### Proposed Event Assessment

| Requirement | Status |
|---|---|
| Monitoring Objective | Defined |
| Detection Method | Documented |
| Detection Rule | Proposed |
| Monitoring Configuration | Not Verified |
| Event Observed | Not Confirmed |
| Technical Validation | Not Performed |
| Service Impact | Not Assessed |
| Incident Required | Undetermined |
| Escalation | Pending Assessment |

### Expected Outcome

The monitoring process should detect a relevant DNS service state change, preserve supporting evidence, and support an appropriate operational response.

**Scenario Status:** Illustrative event detection exercise. No monitoring deployment, service failure, alert generation, or successful diagnostic result is claimed.

---

## 23. Event Detection Evidence Standards

Evidence should support the actual event observations.

### Evidence Types

- Monitoring output
- Event Logs
- PowerShell results
- Network diagnostic output
- Service status information
- Performance measurements
- Configuration records
- Screenshots
- Alert details
- Cloud monitoring data

### Evidence Requirements

Each item should identify:

1. Source system
2. Collection date and time
3. Monitoring method
4. Observed result
5. Relevant threshold or baseline
6. Interpretation
7. Related Event ID

### Documentation Principle

Separate:

**Expected Result:** What monitoring is intended to detect.

**Actual Result:** What was observed during testing.

**Interpretation:** What the observed result may indicate.

**Confirmed Finding:** A conclusion supported by sufficient evidence.

Do not invent event logs, alerts, measurements, or monitoring results.

---

## 24. Event Detection and Incident Management

Event Detection supports Incident Management by identifying conditions that may disrupt services.

### Example

**Event:** A required DNS service stops.

**Impact Assessment:** Domain authentication is unavailable to affected employees.

**Potential Action:** Create an Incident record.

### Incident Handoff Information

- Event ID
- Detection timestamp
- Affected service
- Affected Configuration Item
- Observed symptoms
- Technical evidence
- Impact assessment
- Initial troubleshooting
- Related alerts

### Important

An exception event does not automatically require an Incident record.

The decision should consider whether a service interruption or degradation has occurred.

---

## 25. Event Detection and Problem Management

Recurring events may indicate underlying technical problems.

### Examples

- Repeated DNS service failures
- Recurring authentication errors
- Persistent disk capacity warnings
- Intermittent network instability
- Repeated application crashes

### Potential Problem Identification Criteria

- Significant recurrence
- Shared infrastructure dependencies
- Unknown underlying cause
- Repeated temporary restoration
- Increasing operational risk

### Example

```text
EVT-001 — DNS Service Failure
EVT-004 — DNS Service Failure
EVT-009 — DNS Service Failure
             |
             v
Potential Problem Investigation
             |
             v
PRB-001 — Recurring DNS Service Failure
```

These identifiers are illustrative.

Problem Management determines whether further investigation is warranted.

---

## 26. Event Detection and Change Enablement

Monitoring may identify conditions requiring infrastructure modifications.

### Examples

- Increasing storage capacity
- Updating service configurations
- Adjusting network settings
- Modifying monitoring thresholds
- Implementing additional redundancy

### Change Control Requirements

Changes to infrastructure or monitoring configurations should follow applicable Change Enablement procedures.

### Example

**Detected Event:** Disk capacity repeatedly exceeds the defined warning threshold.

**Potential Corrective Action:** Increase storage capacity.

The proposed modification should be assessed and authorized according to its risk and impact.

Monitoring evidence can support the business justification for the change.

---

## 27. Event Detection and Service Configuration Management

Monitoring results should be associated with relevant Configuration Items.

### Example

```text
Configuration Item:
CI-001 — DC01

Related Service:
IT-SVC-001

Monitoring Objective:
DNS Service Availability

Related Event:
EVT-001
```

### Benefits

- Identifies affected infrastructure
- Supports dependency analysis
- Improves incident investigation
- Enables event correlation
- Supports service impact assessment
- Improves operational documentation

Configuration Item identifiers should match actual repository records when those records exist.

---

## 28. Event Detection and Continual Improvement

Event Detection can identify opportunities to improve monitoring and infrastructure reliability.

### Potential Improvements

- Add missing monitoring checks.
- Adjust ineffective thresholds.
- Reduce duplicate alerts.
- Improve event documentation.
- Expand dependency monitoring.
- Improve escalation criteria.
- Review recurring false positives.
- Improve monitoring coverage.

### Example Improvement Record

```text
Improvement ID: IMP-001

Source:
Monitoring and Event Management

Finding:
DNS service failures are not consistently
detected through the current monitoring method.

Proposed Improvement:
Implement a recurring DNS service health check.

Owner:
To Be Assigned

Status:
Proposed
```

This is an illustrative improvement opportunity.

---

## 29. Common Event Detection Errors

### Error 1 — Treating Every Event as an Incident

**Incorrect:** Creating an Incident record for every informational event.

**Correct:** Evaluate whether the event represents a service interruption or degradation.

### Error 2 — Monitoring Without a Baseline

**Incorrect:** Defining abnormal CPU utilization without understanding normal workload behavior.

**Correct:** Establish relevant baseline measurements.

### Error 3 — Using Excessively Sensitive Thresholds

**Incorrect:** Generating alerts for every brief resource fluctuation.

**Correct:** Use appropriate thresholds, durations, and operational context.

### Error 4 — Ignoring Service Dependencies

**Incorrect:** Monitoring only whether a server responds to ping.

**Correct:** Monitor relevant hosted services and dependencies.

### Error 5 — Assuming a Failed Ping Proves an Outage

**Incorrect:** Declaring a server unavailable based solely on failed ICMP traffic.

**Correct:** Consider firewall restrictions and additional validation methods.

### Error 6 — Failing to Validate Alerts

**Incorrect:** Treating every alert as a confirmed failure.

**Correct:** Verify the condition using appropriate evidence.

### Error 7 — Ignoring Recurring Warnings

**Incorrect:** Dismissing repeated disk capacity warnings because the service remains operational.

**Correct:** Assess whether recurring warnings indicate future risk.

### Error 8 — Failing to Record Evidence

**Incorrect:** Recording an event without relevant observations or timestamps.

**Correct:** Preserve sufficient information for investigation.

### Error 9 — Confusing Monitoring With Automatic Remediation

**Incorrect:** Assuming a diagnostic command automatically repairs a detected problem.

**Correct:** Distinguish detection, alerting, investigation, and remediation.

### Error 10 — Claiming Unconfigured Monitoring Is Operational

**Incorrect:** Describing a proposed Azure Monitor alert as deployed without evidence.

**Correct:** Identify monitoring rules as planned until configuration and testing are verified.

---

## 30. Event Detection Quality Checklist

Before implementing monitoring:

- [ ] Monitoring objective defined
- [ ] Affected service identified
- [ ] Relevant Configuration Items identified
- [ ] Dependencies reviewed
- [ ] Normal operating conditions understood
- [ ] Monitoring source selected
- [ ] Detection condition documented
- [ ] Thresholds defined when appropriate
- [ ] Required permissions reviewed
- [ ] Security requirements considered
- [ ] Monitoring method prepared
- [ ] Data collection tested

When detecting an event:

- [ ] Event timestamp recorded
- [ ] Monitoring source identified
- [ ] Observed condition documented
- [ ] Expected condition recorded
- [ ] Supporting evidence collected
- [ ] Event validated
- [ ] Event category assigned
- [ ] Service impact assessed
- [ ] Related events reviewed
- [ ] Incident requirements evaluated
- [ ] Problem Management requirements considered
- [ ] Escalation requirements evaluated
- [ ] Responsible role identified
- [ ] Event record updated
- [ ] Follow-up actions documented

For ongoing monitoring improvement:

- [ ] False positives reviewed
- [ ] Missed events considered
- [ ] Threshold effectiveness evaluated
- [ ] Monitoring coverage reviewed
- [ ] Relevant Configuration Items updated
- [ ] Continual Improvement opportunities identified

---

## 31. Event Detection Performance Metrics

Event Detection effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Mean Time to Detect (MTTD) | Measures time between a condition beginning and its detection |
| Monitoring Coverage | Measures relevant services or components monitored |
| Event Detection Rate | Tracks significant events detected |
| Alert Volume | Measures generated alert activity |
| False Positive Rate | Evaluates unnecessary alerts |
| False Negative Rate | Evaluates relevant conditions missed by monitoring |
| Event Validation Time | Measures time required to verify detected conditions |
| Event-to-Incident Conversion Rate | Tracks events associated with recorded incidents |
| Recurring Event Rate | Identifies repeated abnormal conditions |
| Alert Escalation Rate | Tracks events requiring additional attention |
| Monitoring Availability | Measures availability of monitoring capabilities |
| Documentation Completeness | Evaluates event record quality |

### Measurement Considerations

Some metrics require additional data.

For example:

**MTTD = Detection Time − Actual Condition Start Time**

If the actual condition start time is unknown, an exact MTTD cannot be calculated.

False negative rates generally require independent evidence of missed conditions.

Metrics should be based on actual records or clearly labeled simulated datasets.

---

## 32. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Receives relevant event information and supports communication |
| Incident Management | Responds to detected service interruptions or degradation |
| Service Request Management | May identify monitoring needs through predefined requests |
| Knowledge Management | Maintains monitoring and troubleshooting guidance |
| Problem Management | Investigates recurring events and potential underlying causes |
| Change Enablement | Controls applicable monitoring and infrastructure modifications |
| Monitoring and Event Management | Detects, records, classifies, and evaluates events |
| Service Configuration Management | Identifies monitored Configuration Items and dependencies |
| Information Security Management | Evaluates security-related events |
| Continual Improvement | Uses monitoring results to improve services and processes |

---

## 33. Related Procedures and Documentation

### Monitoring and Event Management

- [Monitoring and Event Management Overview](../README.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Logging](../../Incident-Management/Procedures/Incident-Logging.md)
- [Incident Investigation](../../Incident-Management/Procedures/Incident-Investigation.md)
- [Incident Resolution](../../Incident-Management/Procedures/Incident-Resolution.md)

### Problem Management

- [Problem Management Overview](../../Problem-Management/)
- [Problem Identification](../../Problem-Management/Procedures/Problem-Identification.md)
- [Root Cause Analysis](../../Problem-Management/Procedures/Root-Cause-Analysis.md)

### Change Enablement

- [Change Enablement Overview](../../Change-Enablement/)
- [Change Authorization](../../Change-Enablement/Procedures/Change-Authorization.md)
- [Change Implementation](../../Change-Enablement/Procedures/Change-Implementation.md)
- [Change Review](../../Change-Enablement/Procedures/Change-Review.md)

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Service Configuration Management](../../Service-Configuration-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

### Infrastructure Documentation

- [Infrastructure Overview](../../Infrastructure/)
- [Active Directory](../../Infrastructure/Active-Directory/)
- [Windows Server](../../Infrastructure/Windows-Server/)
- [Microsoft 365](../../Infrastructure/Microsoft-365/)
- [Networking](../../Infrastructure/Networking/)
- [Virtualization](../../Infrastructure/Virtualization/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

---

## 34. Procedure Review

This procedure should be reviewed when:

- Monitoring responsibilities change.
- New infrastructure technologies are introduced.
- Monitoring tools are added or replaced.
- Event classification requirements change.
- Alert thresholds are revised.
- Monitoring coverage changes.
- Security requirements are updated.
- Significant events are missed.
- False positives increase.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Event Detection procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee reports, organizational roles, business impact assessments, monitoring requirements, event scenarios, and escalation workflows may be simulated.

Monitoring configurations, diagnostic commands, infrastructure measurements, event logs, alerts, validation results, and technical findings are documented based on hands-on lab activities where indicated.

Proposed monitoring rules must not be represented as deployed or operational until their configuration and testing have been verified.

Expected results and hypothetical events must not be represented as actual technical observations.

GitHub publication does not imply production monitoring, independent technical approval, or employment experience.

This procedure demonstrates ITIL-aligned Monitoring and Event Management, event detection, infrastructure monitoring, technical validation, operational documentation, service impact assessment, and continual improvement practices.
