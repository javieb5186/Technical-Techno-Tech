# Technical Techno Tech — Problem Management

## Overview

Problem Management is responsible for identifying, investigating, and managing the actual or potential causes of IT incidents within **Technical Techno Tech (TTT)**, a fictional technology solutions company.

The practice focuses on reducing recurring incidents, preventing future service disruptions, and minimizing the impact of unresolved technical problems.

Problems may involve Windows Server, Active Directory Domain Services, Microsoft 365, Microsoft Entra ID, Microsoft Intune, network infrastructure, cloud services, or other components supporting the organization's internal IT operations.

Technical Techno Tech applies ITIL-aligned Problem Management principles through simulated business scenarios, hands-on root cause investigations, documented workarounds, and corrective action planning.

---

## Purpose

The purpose of Problem Management is to reduce the likelihood and impact of incidents by identifying and managing their underlying causes.

Primary objectives include:

- Identify recurring and significant technical issues.
- Investigate actual or potential causes of incidents.
- Perform structured root cause analysis.
- Document confirmed findings and unresolved hypotheses.
- Identify and maintain effective workarounds.
- Document known errors.
- Recommend permanent corrective actions.
- Coordinate infrastructure changes when necessary.
- Reduce recurring service interruptions.
- Improve service reliability and stability.
- Share troubleshooting knowledge with IT personnel.
- Support continual improvement.

**Key Principle:** Incident Management restores service. Problem Management investigates and manages the causes of incidents to reduce their recurrence and impact.

---

## Scope of Problem Management

### In Scope

Problem Management includes:

- Recurring incident investigations
- Root cause analysis
- Proactive identification of potential service failures
- Investigation of infrastructure weaknesses
- Known error documentation
- Workaround identification and management
- Analysis of incident patterns
- Investigation of recurring authentication failures
- DNS and DHCP reliability investigations
- Active Directory replication issues
- Repeated Group Policy failures
- Network performance and stability issues
- Recurring application or endpoint failures
- Recommendations for permanent corrective actions

### Out of Scope

Activities primarily handled through other ITIL practices include:

- Initial employee support interactions
- Routine service request fulfillment
- Immediate service restoration without further cause investigation
- Change authorization and implementation management
- General infrastructure inventory maintenance
- Routine system monitoring
- Standard administrative procedures

Problem Management may work alongside these practices when necessary.

---

## Problem Definition

A **problem** is a cause, or potential cause, of one or more incidents.

A problem may be identified after incidents occur or proactively before a service interruption happens.

### Examples

| Situation | Classification |
|---|---|
| Employee cannot sign in to a domain workstation | Incident |
| IT investigates recurring authentication failures across multiple workstations | Problem |
| Employees repeatedly lose access to a shared folder | Incidents that may indicate a problem |
| IT identifies a DNS configuration weakness that could cause future outages | Potential Problem |
| IT implements an authorized DNS configuration correction | Change |
| IT documents a verified workaround for recurring DNS failures | Knowledge Article / Known Error Information |

### Incident vs. Problem

**Incident Management:**

- Focuses on restoring normal service.
- Minimizes immediate business disruption.
- May implement a temporary workaround.
- Does not always require complete root cause identification.

**Problem Management:**

- Focuses on identifying and managing underlying causes.
- Investigates recurring or significant technical issues.
- Documents known errors and workarounds.
- Recommends actions to prevent or reduce future incidents.

An incident may be resolved while the related problem remains open.

---

## Problem Management Responsibilities

### Service Desk

The Service Desk supports Problem Management by:

- Identifying recurring employee complaints.
- Recognizing repeated incident patterns.
- Documenting incident symptoms.
- Reporting ineffective workarounds.
- Linking related incident records.
- Sharing troubleshooting observations.
- Using known error information during incident resolution.

### Systems Administration

Systems Administrators investigate problems involving:

- Windows Server
- Active Directory Domain Services
- DNS and DHCP
- Group Policy
- Server configuration
- Virtualization
- Authentication services
- Infrastructure dependencies

### Network Administration

Network Administrators investigate problems involving:

- Network connectivity
- Routing and switching
- VLAN configuration
- DNS and DHCP
- Firewall configuration
- Network performance
- OPNsense
- VyOS

### Endpoint Administration

Endpoint Administrators investigate problems involving:

- Windows workstation stability
- Microsoft Intune
- Application deployment
- Device enrollment
- Endpoint configuration
- Recurring software failures

### Cloud Administration

Cloud Administrators investigate problems involving:

- Microsoft 365
- Microsoft Entra ID
- Microsoft Azure
- Cloud authentication
- Cloud service configuration
- Identity synchronization, where applicable

### Problem Owner

The assigned problem owner is responsible for:

- Coordinating the investigation.
- Maintaining the problem record.
- Reviewing related incidents.
- Documenting findings.
- Identifying workarounds.
- Recommending corrective actions.
- Coordinating with Change Enablement when appropriate.
- Reviewing problem status and closure requirements.

**Note:** These responsibilities represent simulated IT roles within the lab environment and do not imply that separate employees or teams are operating the environment.

---

## Reactive & Proactive Problem Management

Technical Techno Tech recognizes two approaches to Problem Management.

### Reactive Problem Management

Reactive Problem Management investigates problems identified after incidents have occurred.

Examples include:

- Repeated Active Directory authentication failures
- Recurring DNS resolution issues
- Multiple workstation application crashes
- Repeated network connectivity failures
- Recurring Group Policy processing errors

### Proactive Problem Management

Proactive Problem Management identifies potential problems before they result in incidents.

Examples include:

- Detecting insufficient server storage capacity
- Identifying inconsistent DNS configurations
- Discovering unsupported software versions
- Detecting recurring warning events
- Identifying infrastructure dependencies without sufficient redundancy
- Reviewing configuration weaknesses that may affect service availability

### Comparison

| Approach | Focus | Example |
|---|---|---|
| Reactive | Investigates causes of incidents that have occurred | Repeated domain authentication failures |
| Proactive | Identifies potential causes before incidents occur | Detecting a misconfigured DNS dependency during an infrastructure review |

Both approaches support improved service reliability.

---

## Problem Management Lifecycle

Technical Techno Tech follows a structured problem investigation workflow.

### 1. Problem Identification

A potential problem is identified through:

- Recurring incidents
- Major incident reviews
- Service Desk observations
- Monitoring alerts
- Infrastructure assessments
- Technical investigations
- Configuration reviews
- Performance analysis

### 2. Problem Logging

A problem record is created to document the investigation.

Information may include:

- Problem ID
- Problem title
- Date identified
- Reporting source
- Affected IT service
- Related incidents
- Affected systems
- Business impact
- Assigned problem owner
- Current investigation status

### 3. Categorization & Prioritization

The problem is categorized according to the affected service or technology.

Priority may be based on:

- Business impact
- Frequency of related incidents
- Severity of service disruptions
- Number of affected users
- Likelihood of recurrence
- Security implications
- Availability of workarounds

### 4. Investigation & Diagnosis

The assigned technician investigates the potential causes.

Activities may include:

- Reviewing incident history
- Examining system logs
- Analyzing configuration settings
- Testing network connectivity
- Reviewing infrastructure dependencies
- Comparing expected and actual behavior
- Testing technical hypotheses
- Reproducing the issue in a controlled environment

### 5. Root Cause Analysis

Root cause analysis attempts to identify the underlying technical or operational factors contributing to the problem.

Methods may include:

- Five Whys analysis
- Fault tree analysis
- Timeline analysis
- Configuration comparison
- Event correlation
- Dependency analysis
- Controlled testing

Findings should distinguish confirmed causes from suspected causes.

### 6. Workaround Identification

When a permanent resolution is not immediately available, IT may identify a workaround.

A workaround should:

- Reduce or eliminate the immediate impact.
- Be technically validated where possible.
- Document applicable limitations.
- Identify potential risks.
- Be accessible to relevant support personnel.

### 7. Known Error Management

A problem may be recorded as a known error when it has been analyzed but remains unresolved.

Known error information may include:

- Recognizable symptoms
- Confirmed technical findings
- Available workarounds
- Affected services
- Known limitations
- Related incidents
- Recommended corrective actions

A known error does not necessarily require a completed permanent fix.

### 8. Resolution Planning

When corrective actions are identified, IT evaluates the available options.

Considerations include:

- Technical feasibility
- Business impact
- Implementation risk
- Required resources
- Security implications
- Service dependencies
- Change authorization requirements

### 9. Corrective Action & Validation

Approved corrective actions are implemented through the appropriate operational process.

Validation may include:

- Testing affected services
- Verifying corrected configurations
- Monitoring for recurrence
- Reviewing relevant event logs
- Confirming expected system behavior
- Comparing results with previous failures

### 10. Problem Closure

A problem may be closed when its applicable investigation and management objectives have been satisfied.

Closure should document:

- Confirmed or unresolved cause
- Corrective action or accepted risk
- Workaround status
- Validation results
- Related changes
- Related knowledge articles
- Outstanding follow-up work
- Final outcome

Problems should not be marked permanently resolved without sufficient supporting evidence.

---

## Problem Prioritization

Problem priority is determined according to business impact, risk, and likelihood of future disruption.

### Impact

| Impact Level | Description |
|---|---|
| High | Critical services or multiple departments may be affected |
| Medium | Important service or department may experience disruption |
| Low | Limited business impact or noncritical service affected |

### Likelihood / Recurrence

| Level | Description |
|---|---|
| High | Frequent incidents or strong evidence of likely failure |
| Medium | Occasional incidents or moderate likelihood of recurrence |
| Low | Infrequent incidents or low likelihood of disruption |

### Example Priority Matrix

| Impact / Likelihood | High Likelihood | Medium Likelihood | Low Likelihood |
|---|---|---|---|
| High Impact | P1 | P2 | P3 |
| Medium Impact | P2 | P3 | P4 |
| Low Impact | P3 | P4 | P4 |

### Priority Definitions

| Priority | Description |
|---|---|
| P1 — Critical | Significant risk to critical business services |
| P2 — High | High-impact or frequently recurring problem |
| P3 — Medium | Moderate business impact or recurrence risk |
| P4 — Low | Limited impact or low likelihood of recurrence |

This matrix is a proposed prioritization model for the simulated environment.

---

## Root Cause Analysis

Root cause analysis is a central activity within Problem Management.

### Investigation Objectives

The investigation should attempt to determine:

1. What technical behavior is occurring?
2. When and under what conditions does it occur?
3. Which systems or services are affected?
4. What evidence supports the investigation?
5. Which potential causes can be confirmed or eliminated?
6. What underlying factors contribute to the issue?
7. What actions could reduce recurrence?

### Root Cause Analysis Methods

| Method | Purpose |
|---|---|
| Five Whys | Investigates contributing causes through repeated questioning |
| Fault Tree Analysis | Examines possible combinations of failures |
| Timeline Analysis | Identifies relationships between events and failures |
| Configuration Comparison | Identifies differences between expected and actual configurations |
| Event Correlation | Connects related logs, alerts, and system events |
| Dependency Analysis | Examines relationships between infrastructure components |

### Root Cause Documentation

Investigation records should include:

- Initial hypotheses
- Diagnostic tests
- Evidence collected
- Confirmed findings
- Eliminated causes
- Remaining uncertainties
- Final root cause, when identified

**Important:** Root cause analysis should be evidence-based. Do not present assumptions as confirmed findings.

---

## Workaround Management

A workaround is a solution that reduces or eliminates the impact of an incident or problem when a full resolution is not yet available.

### Workaround Requirements

A documented workaround should include:

- Applicable symptoms
- Affected systems
- Required permissions
- Step-by-step instructions
- Expected results
- Limitations
- Risks
- Validation steps
- Escalation guidance

### Example

**Problem:** Recurring failure of an application service.

**Workaround:** Restarting the affected service temporarily restores application availability.

**Limitation:** The underlying cause remains unresolved, and the failure may recur.

**Follow-Up:** Continue investigating service dependencies, event logs, and configuration issues.

Workarounds should be documented in the appropriate problem record and may be shared through Knowledge Management.

---

## Known Error Management

A known error is a problem that has been analyzed but has not been resolved.

### Known Error Information

Known error records may contain:

- Problem reference
- Affected services
- Recognizable symptoms
- Investigation findings
- Confirmed or suspected causes
- Available workarounds
- Known limitations
- Resolution status

### Known Error Lifecycle

1. Identify and investigate the problem.
2. Document analysis findings.
3. Identify available workarounds.
4. Share relevant information with support personnel.
5. Continue evaluating permanent corrective actions.
6. Update the record as new information becomes available.
7. Review or close the problem when appropriate.

Known error information should remain accessible while it is operationally relevant.

---

## Problem Escalation

Problems may require additional technical expertise or organizational coordination.

### Functional Escalation

Examples include:

- Service Desk to Systems Administration
- Systems Administration to Network Administration
- Endpoint Administration to Cloud Administration
- Infrastructure Administration to Information Security

### Escalation Criteria

Escalation may be necessary when:

- The underlying cause cannot be identified.
- Specialized technical expertise is required.
- Critical infrastructure is affected.
- Investigation requires additional permissions.
- Multiple systems or services are involved.
- Corrective actions present significant risk.
- Vendor assistance is necessary.

### Escalation Documentation

Escalated problems should include:

- Problem description
- Related incidents
- Affected services
- Business impact
- Investigation history
- Diagnostic evidence
- Current hypotheses
- Known workarounds
- Outstanding questions

---

## Supported Technologies

Problem Management investigations may involve the following technologies.

### Windows & Active Directory

- Windows Server
- Active Directory Domain Services
- Group Policy
- DNS and DHCP
- Windows Event Viewer
- PowerShell
- Active Directory diagnostic utilities

### Microsoft Cloud Services

- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure

### Networking

- Cisco Networking
- Cisco Packet Tracer
- OPNsense
- VyOS
- Routing and Switching
- TCP/IP
- DNS and DHCP

### Virtualization

- VMware
- Virtual Machines
- Virtual Networking

### IT Service Management

- Jira Service Management
- Spiceworks
- Knowledge Base Documentation

Technologies are included in individual problem records according to their actual use.

---

## Problem Management Procedures

The `Procedures/` directory contains repeatable operational instructions.

| Procedure | Purpose | Status |
|---|---|---|
| Problem Identification | Defines how potential problems are recognized | Planned |
| Problem Logging | Defines required problem record information | Planned |
| Problem Prioritization | Defines risk and impact assessment | Planned |
| Root Cause Analysis | Defines investigation and evidence requirements | Planned |
| Workaround Management | Defines how workarounds are documented and maintained | Planned |
| Known Error Management | Defines known error documentation and review | Planned |
| Problem Closure | Defines closure and validation requirements | Planned |

Procedures will be developed and refined as the simulated environment evolves.

---

## Problem Records

The `Records/` directory contains individual problem investigations.

Each record should document:

- Problem identification
- Related incidents
- Business impact
- Affected systems
- Investigation objectives
- Initial hypotheses
- Diagnostic testing
- Root cause analysis
- Supporting evidence
- Workarounds
- Known error information
- Recommended corrective actions
- Validation results
- Related changes
- Lessons learned
- Final problem status

### Directory Structure

```text
Problem-Management/
├── README.md
├── Procedures/
└── Records/
    └── PRB-001-Problem-Title/
        ├── README.md
        └── Evidence/
```

Each problem record follows the standardized [Problem Template](../Templates/Problem-Template.md).

### Problem Register

| Problem ID | Problem Title | Priority | Status |
|---|---|---|---|
| PRB-XXX | [Problem Title] | [P1–P4] | [Status] |

Add problems to this register as they are documented. Remove placeholder entries until actual records exist.

---

## Problem Status Definitions

| Status | Description |
|---|---|
| Identified | Potential problem has been recognized and recorded |
| Under Investigation | Root cause investigation is in progress |
| Known Error | Problem has been analyzed but remains unresolved |
| Pending Change | Corrective action requires an associated change |
| Monitoring | Corrective action has been implemented and recurrence is being evaluated |
| Resolved | Applicable corrective action has been validated |
| Closed | Investigation and required follow-up activities are complete |

A problem may remain open even when related incidents have been resolved.

---

## Integration With Incident Management

Incident Management and Problem Management are closely related but have different objectives.

### Example: Recurring Authentication Failures

**Incident Management:**

1. Receives a report that an employee cannot authenticate.
2. Investigates the immediate failure.
3. Applies an appropriate workaround.
4. Restores employee access.
5. Documents the incident resolution.

**Problem Management:**

1. Reviews repeated authentication incidents.
2. Identifies patterns across affected systems.
3. Investigates DNS, replication, and time synchronization.
4. Performs root cause analysis.
5. Documents findings and workarounds.
6. Recommends corrective action.
7. Evaluates whether failures recur.

### Documentation Relationship

- **Incident Record:** Documents an individual service interruption and restoration.
- **Problem Record:** Documents the investigation and management of an underlying cause.

Multiple incident records may link to a single problem record.

**Reference:** [Incident Management](../Incident-Management/)

---

## Integration With Change Enablement

Permanent corrective actions may require modifications to infrastructure or service configurations.

### Example

**Problem:** Recurring Active Directory authentication failures caused by an incorrect DNS configuration.

**Proposed Corrective Action:** Update the affected server's DNS settings.

**Change Enablement:**

- Assess the proposed modification.
- Evaluate potential risks.
- Obtain appropriate authorization.
- Plan implementation and recovery.
- Implement and validate the correction.
- Document the change outcome.

**Problem Management:**

- Links to the associated change.
- Reviews the implementation results.
- Monitors for recurrence.
- Updates the problem status.

Not every problem requires a separate change record.

**Reference:** [Change Enablement](../Change-Enablement/)

---

## Integration With Knowledge Management

Problem investigations may produce information useful for future troubleshooting.

Examples include:

- Known error symptoms
- Diagnostic commands
- Confirmed workarounds
- Technical dependencies
- Root cause findings
- Escalation guidance

Reusable information should be maintained in Knowledge Management.

### Documentation Relationship

- **Problem Record:** Contains the detailed investigation and current problem status.
- **Knowledge Article:** Provides reusable diagnostic instructions or workaround guidance.

**Reference:** [Knowledge Management](../Knowledge-Management/)

---

## Integration With Monitoring and Event Management

Monitoring may help identify recurring failures and potential problems.

Examples include:

- Repeated service restart events
- Frequent authentication errors
- Persistent DNS warnings
- Increasing disk utilization
- Recurring network interface failures
- Repeated application crashes

Problem Management may use monitoring information to:

- Identify trends
- Correlate events
- Develop hypotheses
- Validate corrective actions
- Detect recurrence

**Reference:** [Monitoring and Event Management](../Monitoring-and-Event-Management/)

---

## Integration With Service Configuration Management

Configuration Item records help identify affected infrastructure and dependencies.

### Example

A recurring authentication issue may involve:

- Domain controllers
- DNS servers
- Client workstations
- Network devices
- Identity services

Configuration relationships can help determine how a failure in one component affects other systems.

Relevant Configuration Items should be linked to the problem record.

**Reference:** [Service Configuration Management](../Service-Configuration-Management/)

---

## Integration With Other ITIL Practices

| Management Practice | Relationship to Problem Management |
|---|---|
| Service Desk | Identifies recurring employee issues and provides support history |
| Incident Management | Provides incident records and restoration findings |
| Service Request Management | Provides information about relevant service fulfillment activities |
| Knowledge Management | Maintains reusable workarounds and troubleshooting guidance |
| Change Enablement | Manages changes needed for corrective action |
| Monitoring and Event Management | Identifies patterns, alerts, and potential problems |
| Service Configuration Management | Provides infrastructure and dependency information |
| Information Security Management | Supports investigation of security-related weaknesses |
| Continual Improvement | Uses problem trends and findings to improve service reliability |

Problem Management supports multiple ITIL-aligned practices and is not a mandatory stage for every incident.

---

## Problem Management Performance Metrics

Problem Management effectiveness may be evaluated using operational metrics.

| Metric | Purpose |
|---|---|
| Open Problem Count | Tracks unresolved problems |
| Recurring Incident Count | Measures repeated service disruptions |
| Root Cause Identification Rate | Tracks problems with identified causes |
| Average Investigation Time | Measures time required to investigate problems |
| Known Error Count | Tracks analyzed but unresolved problems |
| Workaround Availability | Measures availability of documented workarounds |
| Problem Resolution Rate | Tracks successfully resolved problems |
| Incident Recurrence After Resolution | Evaluates the effectiveness of corrective actions |

Metrics will be introduced when sufficient problem and incident data become available.

Findings may support improvement initiatives under [Continual Improvement](../Continual-Improvement/).

---

## Continual Improvement

Problem Management contributes to continual improvement by identifying recurring weaknesses and opportunities to improve service reliability.

Potential improvements include:

- Eliminating recurring technical failures
- Improving monitoring coverage
- Standardizing infrastructure configurations
- Improving troubleshooting procedures
- Automating preventive maintenance
- Strengthening documentation
- Reducing single points of failure
- Improving incident-to-problem identification
- Enhancing infrastructure resilience

Improvement opportunities should be documented and tracked when appropriate.

---

## Documentation Standards

Problem records should:

1. Clearly identify the problem and affected services.
2. Link relevant incidents when available.
3. Document business impact and recurrence patterns.
4. Record investigation activities chronologically.
5. Distinguish confirmed findings from hypotheses.
6. Include diagnostic commands, outputs, and evidence.
7. Document workarounds and their limitations.
8. Record known error information when applicable.
9. Identify corrective action options.
10. Link related Change Enablement records when required.
11. Validate corrective actions before claiming permanent resolution.
12. Document remaining risks and uncertainties.
13. Protect sensitive information.
14. Distinguish simulated operational activities from actual lab investigations.

---

## Related Documentation

- [Company Overview](../Company-Overview.md)
- [IT Service Catalog](../Service-Catalog.md)
- [Operational Scenarios](../Scenarios/)
- [Service Desk](../Service-Desk/)
- [Incident Management](../Incident-Management/)
- [Service Request Management](../Service-Request-Management/)
- [Knowledge Management](../Knowledge-Management/)
- [Change Enablement](../Change-Enablement/)
- [Monitoring and Event Management](../Monitoring-and-Event-Management/)
- [Service Configuration Management](../Service-Configuration-Management/)
- [Information Security Management](../Information-Security-Management/)
- [Continual Improvement](../Continual-Improvement/)
- [Infrastructure Documentation](../Infrastructure/)
- [Problem Template](../Templates/Problem-Template.md)

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Problem reports, business impact, support roles, escalation activities, and operational workflows may be simulated.

Technical investigations, root cause analysis, configuration testing, workarounds, and validation are documented based on hands-on work performed in controlled lab environments.

This documentation demonstrates practical troubleshooting, root cause analysis, and IT service management knowledge rather than employment experience within an actual production organization.
