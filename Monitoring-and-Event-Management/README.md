# Technical Techno Tech — Monitoring and Event Management

## Overview

Monitoring and Event Management is responsible for observing IT services and infrastructure, detecting significant events, and coordinating appropriate responses within **Technical Techno Tech (TTT)**, a fictional technology solutions company.

The practice helps maintain service availability, performance, reliability, and operational awareness by monitoring systems and identifying conditions that may require attention.

Monitoring activities may involve Windows Server, Active Directory Domain Services, Microsoft 365, Microsoft Entra ID, Microsoft Intune, Microsoft Azure, network infrastructure, virtualization, and other technologies supporting internal business operations.

Technical Techno Tech applies ITIL-aligned Monitoring and Event Management principles through simulated business scenarios, hands-on monitoring exercises, event analysis, alert configuration, and structured documentation.

---

## Purpose

The purpose of Monitoring and Event Management is to observe IT services and infrastructure, identify significant changes in state, and ensure appropriate responses are initiated.

Primary objectives include:

- Monitor the health and availability of IT services.
- Detect significant infrastructure and application events.
- Identify conditions that may affect service performance.
- Recognize potential service disruptions.
- Generate and evaluate relevant alerts.
- Reduce unnecessary or duplicate alerts.
- Support timely incident identification.
- Identify patterns that may indicate underlying problems.
- Provide operational visibility into infrastructure health.
- Maintain accurate monitoring and event records.
- Support proactive maintenance and continual improvement.

**Key Principle:** Not every event is an incident. Events must be evaluated to determine whether they require action.

---

## Scope of Monitoring and Event Management

### In Scope

Monitoring and Event Management includes:

- Server availability monitoring
- Windows service monitoring
- Active Directory health monitoring
- DNS and DHCP monitoring
- Network device monitoring
- Network connectivity monitoring
- CPU, memory, disk, and resource utilization
- Application availability monitoring
- Windows Event Log analysis
- Authentication event monitoring
- Virtual machine health monitoring
- Microsoft Azure resource monitoring
- Alert configuration and notification
- Event classification and correlation
- Threshold management
- Event response and escalation
- Monitoring documentation and reporting

### Out of Scope

Activities primarily handled through other ITIL practices include:

- Full incident investigation and service restoration
- Long-term root cause analysis
- Routine employee service requests
- Change authorization and implementation
- Configuration Item inventory management
- Security incident response investigations
- General technical knowledge documentation

Monitoring and Event Management may initiate or support these activities when appropriate.

---

## Monitoring and Event Definitions

### Monitoring

**Monitoring** is the repeated observation of a system, service, or process to detect events and understand its current condition.

Examples include:

- Checking whether a server is online.
- Monitoring CPU utilization.
- Reviewing available disk space.
- Checking Active Directory replication health.
- Monitoring network interface status.
- Checking whether critical Windows services are running.

### Event

An **event** is a change of state that has significance for the management of a service or Configuration Item.

Examples include:

- A Windows service stops.
- A server becomes unavailable.
- Disk utilization exceeds a defined threshold.
- A domain controller reports a replication failure.
- A network interface changes state.
- A backup job completes.
- A user authentication failure is recorded.

### Alert

An **alert** is a notification generated when an event or monitored condition meets defined criteria.

An alert may require investigation, escalation, or no immediate action depending on its significance.

### Event vs. Incident

| Situation | Classification |
|---|---|
| A scheduled backup completes successfully | Informational Event |
| Server disk utilization exceeds a warning threshold | Warning Event |
| A monitored service unexpectedly stops | Exception Event |
| Employees cannot access an application because its service stopped | Incident |
| Repeated service failures require root cause investigation | Problem |

An event may indicate an incident, but the two are not automatically equivalent.

---

## Event Classification

Technical Techno Tech uses three general event categories.

### 1. Informational Events

Informational events indicate normal or expected activity.

Examples include:

- Successful backup completion
- Scheduled service startup
- Successful system update
- Normal authentication activity
- Successful monitoring checks

These events may be recorded for operational visibility without requiring immediate action.

### 2. Warning Events

Warning events indicate conditions that may require attention or could develop into service disruptions.

Examples include:

- Disk utilization approaching capacity
- Elevated CPU usage
- Increasing memory consumption
- Intermittent network latency
- Repeated service restart attempts
- Active Directory replication warnings

Warning events may require further monitoring, investigation, or preventive action.

### 3. Exception Events

Exception events indicate abnormal conditions that may require prompt action.

Examples include:

- Critical Windows service failure
- Domain controller unavailable
- Network interface failure
- Application service outage
- Repeated replication failures
- Critical disk capacity condition

Exception events should be assessed to determine their actual impact and the appropriate response.

### Event Classification Summary

| Event Type | Description | Typical Response |
|---|---|---|
| Informational | Normal or expected activity | Record or review as needed |
| Warning | Potential issue or approaching threshold | Investigate or monitor |
| Exception | Abnormal condition requiring attention | Assess impact and initiate appropriate response |

Event classification does not automatically determine incident priority.

---

## Monitoring and Event Management Responsibilities

### Service Desk

The Service Desk may:

- Receive monitoring-generated tickets.
- Review alerts affecting employees.
- Record reported service disruptions.
- Coordinate incident communication.
- Escalate alerts requiring specialized investigation.
- Link monitoring evidence to incident records.

### Systems Administration

Systems Administrators may monitor:

- Windows Server availability
- Active Directory health
- DNS and DHCP services
- Server resource utilization
- Windows services
- Event Logs
- Virtual machine health
- Backup operations

### Network Administration

Network Administrators may monitor:

- Network device availability
- Interface status
- Bandwidth utilization
- Routing availability
- Firewall events
- Network latency
- Packet loss
- Connectivity between infrastructure components

### Endpoint Administration

Endpoint Administrators may monitor:

- Device health
- Microsoft Intune compliance
- Application deployment status
- Device enrollment
- Endpoint configuration
- Operating system health

### Cloud Administration

Cloud Administrators may monitor:

- Microsoft Azure resources
- Microsoft 365 service health
- Microsoft Entra ID events
- Cloud authentication activity
- Cloud resource utilization
- Cloud service availability

### Information Security

Information Security personnel may review security-relevant monitoring data, including:

- Suspicious authentication activity
- Security alerts
- Unauthorized configuration changes
- Endpoint protection events
- Unusual administrative activity

Security monitoring findings may require separate security investigation and response procedures.

**Note:** These responsibilities represent simulated IT roles within the lab environment and do not imply that separate employees or teams are operating the environment.

---

## Monitoring and Event Management Lifecycle

Technical Techno Tech follows a structured monitoring and event handling workflow.

### 1. Identify Monitoring Requirements

Determine which services and components require monitoring.

Considerations include:

- Business importance
- Service dependencies
- Availability requirements
- Security requirements
- Performance expectations
- Known technical risks

### 2. Configure Monitoring

Establish appropriate monitoring methods.

Examples include:

- Windows Event Log collection
- Service status checks
- Network connectivity tests
- Performance counters
- PowerShell monitoring scripts
- Azure Monitor alerts
- Device health monitoring

### 3. Detect Events

Monitoring tools or administrative checks identify changes in system or service conditions.

Examples include:

- Service failures
- Resource utilization thresholds
- Network connectivity changes
- Authentication errors
- Application warnings
- System health failures

### 4. Record Events

Relevant events are recorded with information such as:

- Event ID
- Detection time
- Event source
- Affected service
- Affected Configuration Item
- Event category
- Description
- Observed condition
- Supporting evidence

### 5. Filter and Correlate Events

Events are evaluated to identify:

- Duplicate alerts
- Related events
- Expected maintenance activity
- False positives
- Recurring patterns
- Potential service impact

Filtering helps reduce unnecessary operational noise.

### 6. Assess Event Significance

Determine whether the event:

- Requires no action
- Requires continued monitoring
- Requires technical investigation
- Indicates an incident
- Suggests a potential problem
- Requires security escalation

### 7. Initiate Appropriate Response

The response depends on the event's significance.

Possible actions include:

- Recording the event
- Continuing observation
- Notifying an administrator
- Creating an incident
- Escalating a security concern
- Initiating a problem investigation
- Recommending preventive maintenance

### 8. Validate the Outcome

Verify that the monitored condition has returned to an acceptable state or is being managed appropriately.

Validation may include:

- Confirming service availability
- Checking updated performance metrics
- Reviewing event logs
- Repeating diagnostic tests
- Confirming alert clearance
- Monitoring for recurrence

### 9. Close or Transition the Event

The event record is updated with:

- Investigation findings
- Actions taken
- Related incident or problem records
- Validation results
- Final event status
- Follow-up requirements

An event may be closed while a related incident or problem remains open.

---

## Monitoring Categories

Technical Techno Tech organizes monitoring activities into several categories.

| Category | Monitoring Focus | Example |
|---|---|---|
| Availability | Service and system accessibility | Domain controller online status |
| Performance | Resource utilization and responsiveness | CPU and memory usage |
| Capacity | Available infrastructure resources | Disk space utilization |
| Network | Connectivity and network health | Packet loss and interface status |
| Application | Application and service functionality | Windows service availability |
| Identity | Authentication and directory health | AD DS replication and sign-in events |
| Security | Security-relevant activity | Repeated failed authentication attempts |
| Cloud | Cloud service and resource health | Azure VM metrics and service health |

Monitoring requirements should reflect the importance and technical characteristics of each service.

---

## Infrastructure Monitoring

### Windows Server Monitoring

Potential monitoring activities include:

- Server uptime
- CPU utilization
- Memory usage
- Disk capacity
- Windows service status
- Event Log errors
- Network connectivity
- Operating system health

### Active Directory Monitoring

Potential monitoring activities include:

- Domain controller availability
- Active Directory replication
- DNS service health
- SYSVOL availability
- Authentication failures
- Directory service events
- Time synchronization
- FSMO role availability

### Network Monitoring

Potential monitoring activities include:

- Router and switch availability
- Network interface status
- Bandwidth utilization
- Packet loss
- Latency
- DNS resolution
- DHCP availability
- Firewall events

### Endpoint Monitoring

Potential monitoring activities include:

- Device availability
- Operating system health
- Device compliance
- Application deployment status
- Disk utilization
- Endpoint protection status

### Cloud Monitoring

Potential monitoring activities include:

- Azure VM availability
- Resource utilization
- Azure service health
- Microsoft 365 service health
- Entra ID authentication events
- Intune device compliance

Monitoring capabilities depend on available tools, licenses, and configured services.

---

## Monitoring Tools

Technical Techno Tech may use the following tools.

### Windows Event Viewer

Used to review:

- System events
- Application events
- Security events
- Directory Service events
- DNS Server events
- Service failures
- Authentication activity

### Windows Performance Monitor

Used to observe performance counters such as:

- Processor utilization
- Available memory
- Disk performance
- Network activity

### PowerShell

Used for administrative monitoring and diagnostic checks.

Example commands:

```powershell
# Check running services
Get-Service

# Check a specific service
Get-Service -Name DNS

# Review recent system errors
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    Level = 2
    StartTime = (Get-Date).AddHours(-24)
}

# Test network connectivity
Test-Connection -ComputerName DC01 -Count 4

# Check Active Directory replication
repadmin /replsummary

# Check domain controller health
dcdiag /q
```

Commands should be executed only in appropriate environments with the required permissions.

### Windows Admin Center

May be used to review:

- Server health
- Resource utilization
- Windows services
- Event Logs
- Server administration information

### Microsoft Azure Monitor

May be used to:

- Monitor Azure resource metrics
- Collect diagnostic information
- Configure alerts
- Review resource health
- Analyze monitoring data

Azure monitoring features may have associated usage costs.

### Microsoft Intune

May be used to review:

- Device compliance
- Enrollment status
- Application deployment results
- Device configuration status
- Endpoint management information

### Networking Tools

Potential tools include:

- Cisco Packet Tracer
- OPNsense
- VyOS
- Ping
- Traceroute
- DNS diagnostic utilities
- SNMP-based monitoring tools
- Syslog

Tools are documented in individual monitoring exercises according to their actual use.

---

## Alert Configuration

Alerts notify IT personnel when monitored conditions meet defined criteria.

### Alert Components

An alert configuration may include:

- Alert name
- Monitored service or component
- Event source
- Trigger condition
- Threshold
- Severity
- Notification destination
- Response procedure
- Escalation criteria

### Example Alert Definitions

| Alert | Trigger | Classification |
|---|---|---|
| High CPU Usage | CPU utilization exceeds a defined threshold | Warning |
| Low Disk Space | Available storage falls below a defined threshold | Warning |
| Critical Service Stopped | Required Windows service stops unexpectedly | Exception |
| Domain Controller Unavailable | Domain controller fails availability checks | Exception |
| Backup Completed | Scheduled backup completes successfully | Informational |

Thresholds should be established through testing, operational requirements, and observed system behavior.

These are example definitions, not claims that alerts have already been configured.

---

## Alert Threshold Management

Thresholds help determine when monitored conditions require attention.

### Threshold Considerations

- Normal operating behavior
- Expected workload
- Business requirements
- System capacity
- Service criticality
- Frequency of temporary spikes
- Risk of false positives
- Available response resources

### Example

A server may temporarily experience high CPU utilization during an expected maintenance task.

An alert based on a brief CPU spike may generate unnecessary notifications.

A threshold that considers sustained utilization may provide more useful information.

Thresholds should be reviewed and adjusted when monitoring results indicate excessive noise or missed issues.

---

## Event Correlation & Alert Noise Reduction

Multiple events may be related to the same underlying condition.

### Example

A domain controller becomes unavailable.

Monitoring may generate:

- Domain controller availability alert
- DNS service availability alert
- Authentication failure alerts
- Application connectivity alerts

These events may originate from one underlying service disruption.

### Correlation Objectives

- Identify related events.
- Reduce duplicate notifications.
- Determine potential dependencies.
- Improve investigation efficiency.
- Avoid unnecessary ticket creation.
- Support accurate incident classification.

### Alert Noise Reduction

Potential methods include:

- Appropriate thresholds
- Duplicate alert suppression
- Maintenance window handling
- Event correlation
- Alert severity tuning
- Periodic review of false positives

Alert suppression must not hide significant service or security failures.

---

## Event Response & Escalation

Events should be evaluated before determining the appropriate response.

### Informational Event

Typical response:

1. Record or review the event as needed.
2. Confirm expected behavior when appropriate.
3. Take no further action unless additional findings require it.

### Warning Event

Typical response:

1. Review the event details.
2. Check affected system health.
3. Assess whether the condition is expected.
4. Investigate potential risks.
5. Continue monitoring or initiate preventive action.

### Exception Event

Typical response:

1. Review the event and affected service.
2. Determine whether service disruption has occurred.
3. Assess business impact.
4. Notify appropriate technical personnel.
5. Create or link an incident when applicable.
6. Coordinate investigation and response.
7. Verify recovery or appropriate follow-up.

### Escalation Criteria

Escalation may be required when:

- Critical infrastructure becomes unavailable.
- An event indicates significant service disruption.
- A monitored condition exceeds acceptable limits.
- Specialized expertise is required.
- A security concern is identified.
- Repeated events suggest an underlying problem.
- The monitoring system itself becomes unreliable.

---

## Monitoring and Event Records

The `Records/` directory contains individual monitoring exercises, event investigations, and alert response documentation.

Each record should include:

- Event or monitoring record ID
- Event title
- Date and time
- Event source
- Affected service
- Affected Configuration Item
- Event classification
- Trigger condition
- Observed symptoms
- Technical investigation
- Commands and evidence
- Actions taken
- Validation results
- Related records
- Lessons learned
- Final status

### Directory Structure

```text
Monitoring-and-Event-Management/
├── README.md
├── Procedures/
└── Records/
    └── EVT-001-Event-Title/
        ├── README.md
        └── Evidence/
```

### Event Identification

**Format: EVT-XXX — Descriptive Event Title**

Examples:

- EVT-001 — Domain Controller Availability Alert
- EVT-002 — High CPU Utilization Warning
- EVT-003 — DNS Service Failure Detection
- EVT-004 — Active Directory Replication Warning
- EVT-005 — Low Disk Space Alert

These are examples of potential monitoring records, not completed exercises.

### Event Register

| Event ID | Event Title | Classification | Status |
|---|---|---|---|
| EVT-XXX | [Event Title] | [Informational / Warning / Exception] | [Status] |

Add events to this register as they are documented. Remove placeholder entries until actual records exist.

---

## Event Status Definitions

| Status | Description |
|---|---|
| Detected | Event has been identified |
| Under Review | Event significance is being assessed |
| Investigating | Technical investigation is in progress |
| Escalated | Event requires additional technical or operational response |
| Monitoring | Condition is being observed for changes or recurrence |
| Resolved | The relevant condition has returned to an acceptable state |
| Closed | Required documentation and follow-up are complete |

An event record may reference an open incident, problem, or change.

---

## Monitoring and Event Management Procedures

The `Procedures/` directory contains repeatable monitoring and event handling instructions.

| Procedure | Purpose | Status |
|---|---|---|
| Monitoring Configuration | Defines monitoring setup and requirements | Planned |
| Event Classification | Defines informational, warning, and exception categories | Planned |
| Alert Configuration | Defines alert triggers, thresholds, and notifications | Planned |
| Event Investigation | Defines event analysis and evidence requirements | Planned |
| Event Escalation | Defines escalation criteria and responsibilities | Planned |
| Event Closure | Defines validation and documentation requirements | Planned |

Procedures will be developed and refined as monitoring capabilities are introduced.

---

## Integration With Incident Management

Monitoring may detect conditions that indicate an unplanned service interruption.

### Example

**Event:** Monitoring detects that the DNS service on DC01 has unexpectedly stopped.

**Monitoring and Event Management:**

1. Detects the service failure.
2. Records the event.
3. Assesses the affected service.
4. Generates an alert.
5. Initiates an incident when a service interruption is confirmed.

**Incident Management:**

1. Investigates the DNS service interruption.
2. Determines the immediate impact.
3. Performs troubleshooting.
4. Restores the affected service.
5. Validates recovery.
6. Documents the incident outcome.

### Documentation Relationship

- **Event Record:** Documents detection, alerting, and initial event assessment.
- **Incident Record:** Documents the specific service disruption and restoration.

**Reference:** [Incident Management](../Incident-Management/)

---

## Integration With Problem Management

Repeated monitoring events may indicate an underlying technical problem.

### Example

**Monitoring Finding:** A Windows service repeatedly stops and restarts.

**Problem Management:**

1. Reviews recurring service failure events.
2. Investigates possible underlying causes.
3. Analyzes relevant logs and configurations.
4. Identifies workarounds when available.
5. Recommends corrective action.

Monitoring may continue after corrective action to determine whether the failures recur.

**Reference:** [Problem Management](../Problem-Management/)

---

## Integration With Change Enablement

Monitoring supports change planning, implementation, and post-change validation.

### Example

**Change:** Deploy a new domain controller.

Monitoring may be used to:

- Establish baseline service health.
- Confirm existing domain controller availability.
- Observe replication status.
- Detect unexpected errors.
- Validate post-deployment service health.
- Identify issues requiring corrective action.

**Reference:** [Change Enablement](../Change-Enablement/)

---

## Integration With Service Configuration Management

Monitoring targets should be associated with relevant Configuration Items when practical.

### Example

**Configuration Item:** DC01 — Domain Controller

Potential monitored attributes include:

- Server availability
- DNS service status
- Active Directory replication
- CPU utilization
- Memory utilization
- Disk capacity
- Time synchronization

Configuration records help identify infrastructure relationships and determine the potential impact of monitored failures.

**Reference:** [Service Configuration Management](../Service-Configuration-Management/)

---

## Integration With Information Security Management

Monitoring may identify events relevant to information security.

Examples include:

- Repeated failed authentication attempts
- Unexpected privileged account activity
- Unauthorized configuration changes
- Endpoint protection alerts
- Suspicious network connections
- Security policy violations

Security-relevant events should be assessed and escalated according to established security procedures.

Not every failed authentication event indicates a security incident.

**Reference:** [Information Security Management](../Information-Security-Management/)

---

## Integration With Knowledge Management

Monitoring investigations may produce reusable technical knowledge.

Examples include:

- Interpreting Windows Event IDs
- Investigating DNS service failures
- Diagnosing Active Directory replication errors
- Configuring monitoring thresholds
- Troubleshooting monitoring agents
- Responding to common infrastructure alerts

Reusable instructions should be documented in Knowledge Management rather than duplicated across event records.

**Reference:** [Knowledge Management](../Knowledge-Management/)

---

## Integration With Other ITIL Practices

| Management Practice | Relationship to Monitoring and Event Management |
|---|---|
| Service Desk | Receives and coordinates relevant monitoring-generated support tickets |
| Incident Management | Investigates confirmed service interruptions |
| Service Request Management | May fulfill approved requests for monitoring access or configuration |
| Knowledge Management | Maintains reusable monitoring and troubleshooting instructions |
| Problem Management | Investigates recurring events and underlying causes |
| Change Enablement | Controls changes to monitoring configurations and affected services |
| Service Configuration Management | Identifies monitored infrastructure components and dependencies |
| Information Security Management | Evaluates security-relevant events |
| Continual Improvement | Uses monitoring data to improve service performance and reliability |

Monitoring and Event Management supports multiple ITIL-aligned practices without requiring every event to become a separate ticket.

---

## Monitoring Performance Metrics

Monitoring and Event Management effectiveness may be evaluated using operational metrics.

| Metric | Purpose |
|---|---|
| Event Volume | Tracks the number of detected events |
| Alert Volume | Measures generated notifications |
| Alert Accuracy | Evaluates the relevance of alerts |
| False Positive Rate | Measures alerts that do not represent actionable conditions |
| Mean Time to Detect (MTTD) | Measures average time required to detect relevant conditions |
| Mean Time to Acknowledge (MTTA) | Measures average time required to acknowledge alerts |
| Monitoring Coverage | Measures monitored services and components |
| Repeated Event Count | Identifies recurring conditions |
| Unmonitored Critical Components | Identifies monitoring gaps |
| Alert-to-Incident Conversion | Tracks alerts that lead to incident records |

Metrics will be introduced when sufficient monitoring data becomes available.

Findings may support improvement initiatives under [Continual Improvement](../Continual-Improvement/).

---

## Continual Improvement

Monitoring and Event Management contributes to continual improvement by identifying operational weaknesses and opportunities to improve visibility.

Potential improvements include:

- Expanding monitoring coverage
- Improving alert accuracy
- Reducing duplicate notifications
- Adjusting monitoring thresholds
- Identifying recurring infrastructure warnings
- Improving event correlation
- Automating appropriate alert responses
- Improving monitoring documentation
- Strengthening infrastructure health checks
- Improving integration with Incident and Problem Management

Improvements should be based on observed monitoring results and documented operational needs.

---

## Documentation Standards

Monitoring and event records should:

1. Clearly identify the monitored service or component.
2. Document the event source and detection time.
3. Identify the observed condition.
4. Record event classification and alert severity.
5. Document relevant thresholds or trigger conditions.
6. Include technical evidence and diagnostic outputs.
7. Distinguish confirmed service failures from potential risks.
8. Record investigation and response activities.
9. Document escalation when applicable.
10. Verify recovery or continued monitoring requirements.
11. Link related incidents, problems, changes, and Configuration Items.
12. Protect sensitive monitoring and security information.
13. Distinguish simulated alerts from actual lab-generated events.
14. Record actual test results without inventing monitoring data.

---

## Related Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Operational Scenarios](../Scenarios/)
- [Service Desk](../Service-Desk/)
- [Incident Management](../Incident-Management/)
- [Service Request Management](../Service-Request-Management/)
- [Knowledge Management](../Knowledge-Management/)
- [Problem Management](../Problem-Management/)
- [Change Enablement](../Change-Enablement/)
- [Service Configuration Management](../Service-Configuration-Management/)
- [Information Security Management](../Information-Security-Management/)
- [Continual Improvement](../Continual-Improvement/)
- [Infrastructure Documentation](../Infrastructure/)

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Monitoring requirements, business impact, alert routing, escalation activities, and operational responsibilities may be simulated.

Monitoring configurations, detected events, diagnostic testing, technical investigations, and validation are documented based on hands-on work performed in controlled lab environments where indicated.

This documentation demonstrates practical infrastructure monitoring, event analysis, troubleshooting, and IT service management knowledge rather than employment experience within an actual production organization.
