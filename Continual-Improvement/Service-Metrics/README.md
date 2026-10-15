# IT Service Metrics and Performance Measurement

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Continual Improvement  
**Document Type:** Service Metrics Documentation Guide  
**Document ID:** GUIDE-CI-001  
**Version:** 1.0  
**Status:** Draft — Lab Documentation Standard  
**Function:** Internal IT  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

## 1. Purpose

This directory contains the service performance metrics, measurement definitions, and supporting reports used to evaluate Technical Techno Tech's internal IT operations.

The purpose is to establish a consistent method for defining, collecting, calculating, analyzing, documenting, and reviewing IT service performance data.

Service metrics support evidence-based decisions and help identify opportunities for continual improvement.

This documentation framework supports:

- IT service performance measurement
- Incident management effectiveness
- Service request fulfillment performance
- Service Desk operational efficiency
- Infrastructure reliability
- Monitoring and alert quality
- Configuration management accuracy
- Information security effectiveness
- Knowledge management quality
- Change implementation performance
- Cost optimization
- Continual improvement initiatives

**Key Principle:** A metric should provide meaningful information about service performance or an improvement objective. Collecting data without a clear purpose does not necessarily create value.

---

## 2. ITIL 4 Alignment

Service measurement supports the ITIL 4 Continual Improvement practice and provides useful information to other ITIL practices.

### Continual Improvement Practice

The purpose of Continual Improvement is to align the organization's practices and services with changing business needs through the ongoing improvement of products, services, and practices.

Measurement supports this objective by helping answer:

1. Where are we now?
2. Where do we want to be?
3. Did we get there?
4. How do we keep the momentum going?

### Relationship to the Continual Improvement Model

| ITIL 4 Model Activity | Measurement Application |
|---|---|
| What is the vision? | Identify organizational and service objectives |
| Where are we now? | Establish performance baselines |
| Where do we want to be? | Define targets and success criteria |
| How do we get there? | Select improvement actions and measurement methods |
| Take action | Implement improvements and collect relevant observations |
| Did we get there? | Compare actual performance with targets |
| How do we keep the momentum going? | Continue monitoring performance and identifying improvements |

### Important

ITIL 4 does not require every organization to use the same metrics.

Measurements should reflect the services, risks, objectives, and capabilities of the organization.

This directory defines a proposed measurement framework for a simulated corporate IT environment.

---

## 3. Scope

This directory covers metrics related to Technical Techno Tech's internal IT services.

### Supported Services

| Service ID | Service |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

### Supported ITIL Practices

- Service Desk
- Incident Management
- Service Request Management
- Knowledge Management
- Problem Management
- Change Enablement
- Monitoring and Event Management
- Service Configuration Management
- Information Security Management
- Continual Improvement

### Supported Technical Environments

- Active Directory Domain Services
- Windows Server
- Windows 11
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Network infrastructure
- OPNsense
- VyOS
- Cisco Packet Tracer
- PowerShell

### Scope Limitations

Metrics may be based on actual lab observations, simulated scenarios, or illustrative examples.

These categories must remain clearly distinguished.

Only measurements supported by actual evidence should be reported as observed results.

---

# 4. Key Terminology

| Term | Definition |
|---|---|
| Metric | A defined measurement used to evaluate performance or outcomes |
| KPI | Key Performance Indicator used to assess progress toward an important objective |
| Baseline | Recorded current or previous performance used for comparison |
| Target | Desired performance level |
| Actual Result | Performance observed during a defined measurement period |
| Measurement Period | Time interval covered by the data |
| Data Source | System, record, or observation from which data originates |
| Measurement Method | Procedure used to collect or calculate data |
| Service Level Agreement (SLA) | Documented agreement between a service provider and customer identifying required services and expected service levels |
| Service Level Objective (SLO) | Defined target for a particular service performance measure |
| Threshold | Value used to identify a condition requiring attention |
| Trend | Pattern of change over time |
| Variance | Difference between a target or baseline and actual performance |
| Availability | Degree to which a service or component is available when required |
| Reliability | Ability to perform required functions under stated conditions |
| Effectiveness | Extent to which intended results are achieved |
| Efficiency | Relationship between results achieved and resources used |
| Evidence | Information supporting a reported measurement or conclusion |
| Data Quality | Accuracy, completeness, consistency, and suitability of measurement data |

---

# 5. Directory Structure

## Proposed Structure

```text
Service-Metrics/
├── README.md
├── MET-001-Incident-Resolution-Time.md
├── MET-002-Service-Request-Fulfillment-Time.md
├── MET-003-Change-Success-Rate.md
├── MET-004-Service-Availability.md
├── MET-005-Alert-Quality.md
└── Reports/
    ├── Monthly/
    └── Quarterly/
```

These are proposed files and directories.

Individual metric definitions should be created when a measurement is selected for use.

Reports should be created only when actual observations or explicitly labeled simulated datasets are available.

### Directory Responsibilities

| Location | Purpose |
|---|---|
| `README.md` | Defines measurement and reporting standards |
| `MET-###-Name.md` | Defines an individual metric |
| `Reports/Monthly/` | Stores monthly performance reports |
| `Reports/Quarterly/` | Stores quarterly performance reports |

### Important

Git does not track empty directories.

Create directories when they contain documentation or another tracked file.

---

# 6. Metric Identification Standards

Each metric should receive a unique identifier.

### Proposed Identifier

```text
MET-###
```

### Examples

```text
MET-001
MET-002
MET-003
MET-004
```

### File Naming Convention

```text
MET-###-Metric-Name.md
```

### Example

```text
MET-001-Incident-Resolution-Time.md
```

### Identification Rules

1. Assign a unique identifier.
2. Do not reuse identifiers.
3. Use descriptive metric names.
4. Maintain consistent calculation methods.
5. Link the metric to relevant services and practices.
6. Retain historical definitions when methods change materially.
7. Document revisions that affect comparisons.

### Important

Changing a metric's definition may make historical results incomparable.

Significant calculation changes should be documented rather than silently applied.

---

# 7. Types of IT Service Metrics

Technical Techno Tech uses the following proposed metric categories.

## 7.1 Service Performance Metrics

Evaluate the performance of an IT service.

Examples:

- Service availability
- Service response time
- Service reliability
- Service restoration time

## 7.2 Operational Process Metrics

Evaluate the performance of operational workflows.

Examples:

- Incident resolution time
- Service request fulfillment time
- Change implementation success
- Ticket reassignment frequency

## 7.3 Infrastructure Metrics

Evaluate technical infrastructure performance.

Examples:

- CPU utilization
- Memory utilization
- Disk capacity
- Network latency
- Server availability

## 7.4 Security Metrics

Evaluate selected security controls and activities.

Examples:

- Privileged access review completion
- Security configuration compliance
- Remediation time
- Unresolved security findings

## 7.5 Knowledge Management Metrics

Evaluate knowledge documentation and its usefulness.

Examples:

- Article review completion
- Article verification coverage
- Documentation completeness
- Knowledge article usage

## 7.6 Continual Improvement Metrics

Evaluate improvement activities and outcomes.

Examples:

- Improvements completed
- Improvement success rate
- Verified benefits
- Improvement backlog age
- Improvement review completion

## 7.7 Cost Metrics

Evaluate resource consumption and spending.

Examples:

- Monthly Azure spending
- Virtual machine compute cost
- Storage cost
- Software licensing cost

### Important

A single metric may support more than one category.

---

# 8. Required Metric Attributes

Every individual metric definition should contain the following information.

| Attribute | Description | Required |
|---|---|---|
| Metric ID | Unique identifier | Yes |
| Metric Name | Descriptive title | Yes |
| Purpose | Why the metric is measured | Yes |
| Related Service | Applicable IT service | Yes |
| Related Practice | Applicable ITIL practice | Yes |
| Metric Owner | Responsible role | Yes |
| Definition | Exactly what is measured | Yes |
| Data Source | Where the data originates | Yes |
| Calculation Method | Formula or measurement procedure | Yes |
| Unit | Minutes, hours, percentage, count, etc. | Yes |
| Measurement Period | Reporting interval | Yes |
| Inclusion Criteria | Records or events included | Yes |
| Exclusion Criteria | Records or events excluded | Yes |
| Baseline | Current or previous performance | When available |
| Target | Desired performance | When established |
| Actual Result | Observed measurement | When collected |
| Evidence | Supporting records | When available |
| Last Reviewed | Most recent review date | When reviewed |
| Limitations | Known measurement restrictions | Yes |

### Optional Attributes

- Alert thresholds
- Service level objectives
- Related SLAs
- Related improvement initiatives
- Related incident records
- Related problem records
- Related changes
- Trend analysis
- Data collection tools
- Automation details
- Review findings

### Unknown Information

Use explicit values such as:

- `Not Yet Measured`
- `Not Yet Established`
- `Pending Verification`
- `Not Applicable`
- `Insufficient Data`

Do not invent measurements to complete a metric record.

---

# 9. Metric Selection Principles

Metrics should be selected according to their usefulness.

### 9.1 Align With Service Objectives

The metric should help evaluate an important service or operational objective.

### 9.2 Define a Clear Purpose

Explain why the metric is needed.

### 9.3 Use Reliable Data

Prefer measurements that can be collected consistently.

### 9.4 Define the Calculation

The metric should produce comparable results when the same method is used.

### 9.5 Avoid Unnecessary Complexity

A simple, useful metric is preferable to a complex metric that cannot be maintained.

### 9.6 Consider Unintended Consequences

Metrics can encourage undesirable behavior when interpreted incorrectly.

### Example

Measuring only the number of tickets closed may encourage premature closure.

A better evaluation may consider:

- Resolution quality
- Reopened tickets
- Requester confirmation
- Resolution time

### 9.7 Maintain Context

Performance results should be interpreted alongside relevant operational conditions.

### Important

A metric should support decision-making, not simply generate a number.

---

# 10. Service Measurement Lifecycle

```text
Identify Measurement Need
           |
           v
Define Metric
           |
           v
Identify Data Source
           |
           v
Establish Collection Method
           |
           v
Collect Baseline
           |
           v
Define Target
           |
           v
Collect Performance Data
           |
           v
Validate Data
           |
           v
Calculate Results
           |
           v
Analyze Performance
           |
           v
Report Findings
           |
           v
Identify Improvements
           |
           v
Review Measurement Method
```

The lifecycle is iterative.

Metric definitions, targets, and collection methods may require revision as services change.

---

# 11. Service Measurement Procedure

## Step 1 — Identify the Measurement Objective

Determine what needs to be evaluated.

### Questions

1. Which service or process is being measured?
2. What operational objective matters?
3. What decision will the measurement support?
4. Who will use the results?
5. What improvement opportunity might the metric reveal?

### Example

**Objective:** Evaluate how long it takes to resolve incidents.

**Expected Result:** A clear measurement objective is established.

---

## Step 2 — Select the Metric

Choose a metric aligned with the objective.

### Example

**Metric:** Incident Resolution Time

**Related Practice:** Incident Management

**Purpose:** Evaluate the elapsed time between incident logging and restoration or resolution, according to the defined measurement method.

### Important

The metric definition must specify its start and end events.

Different organizations may measure incident resolution time differently.

**Expected Result:** The metric is selected.

---

## Step 3 — Define the Metric

Document exactly what is being measured.

### Example

```text
Metric ID:
MET-001

Metric Name:
Incident Resolution Time

Definition:
Elapsed time between the recorded incident
start point and the defined resolution event.

Unit:
Minutes

Related Practice:
Incident Management

Status:
Proposed
```

### Required Decisions

- Start event
- End event
- Time unit
- Included records
- Excluded records
- Treatment of paused time
- Treatment of reopened incidents

**Expected Result:** The metric has an unambiguous definition.

---

## Step 4 — Identify the Data Source

Determine where the required information can be obtained.

### Potential Sources

- ITSM ticket records
- Incident logs
- Service request records
- Change records
- Windows Event Logs
- PowerShell output
- Azure Cost Management
- Microsoft administrative reports
- Monitoring systems
- Configuration verification records
- Manual lab observations

### Example

Incident timestamps may be obtained from a ticketing platform or a documented incident record.

### Important

Jira Service Management integration is a proposed future capability.

Do not claim that automated Jira reporting is configured unless it has actually been implemented and verified.

**Expected Result:** The data source is identified.

---

## Step 5 — Establish the Collection Method

Define how the data will be gathered.

### Collection Methods

- Manual observation
- Manual record review
- PowerShell
- Administrative reporting
- Monitoring tools
- ITSM reporting
- Scheduled automation

### Required Information

- Collection method
- Responsible role
- Required permissions
- Frequency
- Data format
- Storage location
- Validation method

**Expected Result:** The measurement can be collected consistently.

---

## Step 6 — Define the Measurement Period

Select the reporting interval.

### Potential Periods

- Per event
- Daily
- Weekly
- Monthly
- Quarterly
- Per lab exercise
- Before and after an improvement

### Example

**Measurement Period:** Calendar month

### Important

Measurements should use consistent periods when making comparisons.

A seven-day incident count should not be directly compared with a thirty-day count without accounting for the different periods.

**Expected Result:** The reporting interval is defined.

---

## Step 7 — Establish the Baseline

Collect or identify the current performance level.

### Example

```text
Metric:
Incident Resolution Time

Baseline Period:
Not Yet Defined

Baseline Value:
Not Yet Measured

Data Source:
Pending

Evidence:
Pending
```

### Important

A baseline should be based on actual observations.

If no historical information exists, collect an initial baseline before claiming improvement.

**Expected Result:** A baseline is established or the limitation is recorded.

---

## Step 8 — Define the Target

Establish the desired performance level.

### Example

**Metric:** Incident Resolution Time

**Target:** To Be Established After Baseline Review

### Target Considerations

- Business requirements
- Service criticality
- Available resources
- Historical performance
- Technical constraints
- User expectations
- Risk

### Important

A target is not automatically an SLA.

An SLA requires an actual agreement between the relevant parties.

**Expected Result:** A justified target is documented.

---

## Step 9 — Collect Measurement Data

Gather observations according to the defined method.

### Requirements

1. Record the source.
2. Record the collection date.
3. Record the measurement period.
4. Preserve relevant raw values.
5. Identify missing information.
6. Avoid duplicate counting.
7. Protect sensitive data.

### Example

```text
Metric ID:
MET-001

Measurement Period:
Pending

Records Evaluated:
Pending

Raw Observations:
Not Yet Collected

Collection Status:
Pending
```

**Expected Result:** Measurement data is available for evaluation.

---

## Step 10 — Validate Data Quality

Review the collected information.

### Validation Questions

- Is the data complete?
- Are timestamps accurate?
- Are units consistent?
- Are duplicate records present?
- Are exclusions documented?
- Are there missing values?
- Does the data match the metric definition?

### Important

A mathematically correct calculation can still produce a misleading result if the underlying data is inaccurate.

**Expected Result:** Data quality is evaluated.

---

## Step 11 — Calculate the Metric

Apply the documented formula or measurement procedure.

### Calculation Requirements

- Use consistent units.
- Use the defined record population.
- Preserve the calculation method.
- Identify missing data.
- Handle zero denominators appropriately.
- Record the actual result.

### Important

If required data is unavailable, report the result as unavailable rather than estimating without disclosure.

**Expected Result:** A reproducible measurement is calculated.

---

## Step 12 — Compare Results

Compare actual performance against the baseline or target.

### Example

| Measurement | Value |
|---|---|
| Baseline | Not Yet Measured |
| Target | Not Yet Established |
| Actual | Not Yet Measured |
| Variance | Not Available |
| Outcome | Pending |

### Questions

1. Is performance improving?
2. Is performance declining?
3. Was the target achieved?
4. Are there unusual results?
5. Did the operating environment change?

**Expected Result:** Performance differences are identified.

---

## Step 13 — Analyze the Results

Determine what the measurement indicates.

### Analysis Considerations

- Operational trends
- Service demand
- Technical changes
- Incident severity
- Resource availability
- Configuration changes
- Security events
- Measurement limitations

### Example

A higher average incident resolution time could reflect:

- More complex incidents
- Insufficient support resources
- Poor escalation
- Missing knowledge documentation
- Inaccurate ticket timestamps

### Important

A metric identifies a pattern.

It does not necessarily identify the underlying cause.

**Expected Result:** Results are interpreted in context.

---

## Step 14 — Document Findings

Create a metric report or update the individual metric record.

### Required Information

- Metric ID
- Reporting period
- Data source
- Calculation
- Actual result
- Baseline or target
- Interpretation
- Limitations
- Evidence references
- Recommended actions

**Expected Result:** Findings are documented.

---

## Step 15 — Identify Improvement Opportunities

Determine whether the results indicate a need for improvement.

### Examples

- Increasing incident resolution time
- Repeated service request delays
- High alert false-positive rates
- Incomplete CI records
- Repeated change failures
- Increasing infrastructure costs

### Improvement Workflow

1. Identify the performance gap.
2. Review the supporting evidence.
3. Determine whether further investigation is required.
4. Document the opportunity.
5. Register an improvement initiative where appropriate.
6. Define success criteria.
7. Track the initiative separately.

### Related Register

[Continual Improvement Register](../Improvement-Register.md)

**Expected Result:** Relevant improvement opportunities are identified.

---

## Step 16 — Review the Metric

Periodically assess whether the metric remains useful.

### Review Questions

1. Does the metric still support a meaningful objective?
2. Is the data source reliable?
3. Is the collection method practical?
4. Is the calculation appropriate?
5. Is the target still relevant?
6. Are results being used to make decisions?
7. Should the metric be revised or retired?

**Expected Result:** The measurement framework remains relevant.

---

# 12. Incident Management Metrics

Incident Management metrics evaluate the effectiveness of restoring disrupted services.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Incident Volume | Number of incidents during a defined period |
| Incident Resolution Time | Time required to reach the defined resolution event |
| Mean Time to Restore Service (MTRS) | Average time required to restore service |
| Incident Reopen Rate | Percentage of resolved incidents subsequently reopened |
| Incident Escalation Rate | Percentage of incidents requiring escalation |
| Recurring Incident Count | Number of incidents meeting defined recurrence criteria |

## 12.1 Incident Resolution Time

### Example Formula

```text
Incident Resolution Time =
Resolution Timestamp - Start Timestamp
```

### Important

Define whether the start timestamp represents incident detection, occurrence, or logging.

Also define how reopened incidents and paused time are handled.

---

## 12.2 Mean Time to Restore Service

```text
Mean Time to Restore Service =

Total Restoration Duration
--------------------------
Number of Restored Incidents
```

### Important

Restoration time and ticket closure time may differ.

A service may be restored before all administrative documentation is completed.

---

## 12.3 Incident Reopen Rate

```text
Incident Reopen Rate (%) =

Number of Reopened Incidents
---------------------------- x 100
Number of Resolved Incidents
```

The numerator and denominator must refer to a consistently defined population and reporting period.

---

# 13. Service Desk Metrics

Service Desk metrics evaluate support activities and ticket handling.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Ticket Volume | Measures support demand |
| First Response Time | Measures time to initial response |
| Ticket Categorization Accuracy | Evaluates correct ticket classification |
| Ticket Reassignment Rate | Tracks reassignment frequency |
| First Contact Resolution Rate | Measures eligible tickets resolved during first contact |
| Ticket Backlog | Tracks unresolved tickets |
| Ticket Age | Measures how long tickets remain unresolved |

### Example: First Response Time

```text
First Response Time =

First Qualifying Response Timestamp
-
Ticket Receipt Timestamp
```

### Important

An automated acknowledgment should not automatically count as a meaningful first response.

The metric definition must specify qualifying response events.

---

# 14. Service Request Management Metrics

Service Request Management metrics evaluate request fulfillment.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Request Volume | Measures request demand |
| Fulfillment Time | Measures time required to fulfill requests |
| Request Backlog | Tracks outstanding requests |
| Request Rework Rate | Identifies requests requiring repeated work |
| Fulfillment Accuracy | Evaluates whether requests were completed correctly |
| Request Authorization Delay | Measures time spent awaiting authorization |

### Example: Fulfillment Time

```text
Request Fulfillment Time =

Fulfillment Completion Timestamp
-
Defined Request Start Timestamp
```

### Important

The measurement method should define whether waiting for approval or requester information is included.

---

# 15. Problem Management Metrics

Problem Management metrics evaluate recurring issues and underlying causes.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Open Problem Count | Tracks unresolved problems |
| Problem Backlog Age | Measures age of unresolved problem records |
| Root Cause Identification Rate | Measures problems with documented root causes |
| Known Error Documentation Rate | Tracks documented known errors |
| Recurring Incident Trend | Evaluates recurrence associated with known problems |
| Permanent Remediation Verification | Tracks verified corrective outcomes |

### Important

A documented root cause does not automatically mean the underlying problem has been permanently resolved.

Problem investigation and remediation should be evaluated separately.

---

# 16. Change Enablement Metrics

Change Enablement metrics evaluate the effectiveness of changes.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Change Volume | Number of changes during a period |
| Change Success Rate | Percentage meeting defined success criteria |
| Failed Change Rate | Percentage failing defined criteria |
| Emergency Change Rate | Proportion classified as emergency changes |
| Change Rollback Rate | Percentage requiring rollback |
| Change Review Completion | Percentage of required reviews completed |

## 16.1 Change Success Rate

```text
Change Success Rate (%) =

Successful Implemented Changes
------------------------------ x 100
Total Evaluated Implemented Changes
```

### Definition Requirements

Define:

- What constitutes success
- Which changes are included
- How partially successful changes are handled
- How cancelled changes are treated
- Whether success requires an observation period

### Important

A change that completes without an immediate error is not necessarily successful.

Success should be evaluated against its approved objectives and validation criteria.

---

# 17. Monitoring and Event Management Metrics

Monitoring metrics evaluate detection effectiveness and alert quality.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Event Volume | Number of recorded events |
| Alert Volume | Number of generated alerts |
| False-Positive Rate | Proportion of evaluated alerts that were false positives |
| Alert Acknowledgment Time | Time before an alert is acknowledged |
| Detection Time | Time between defined event occurrence and detection |
| Duplicate Alert Rate | Proportion of duplicate alerts |
| Monitoring Coverage | Proportion of in-scope components monitored |

## 17.1 False-Positive Rate

```text
False-Positive Rate (%) =

Alerts Classified as False Positives
------------------------------------ x 100
Total Evaluated Alerts
```

### Important

A low alert volume does not automatically indicate effective monitoring.

Important events may be missed.

---

# 18. Service Configuration Management Metrics

Configuration metrics evaluate the quality of CI records and dependency documentation.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| CI Record Completeness | Measures required fields populated |
| CI Verification Coverage | Tracks CIs verified during a period |
| Configuration Discrepancy Rate | Measures verified CIs with discrepancies |
| Dependency Map Coverage | Tracks services with dependency maps |
| Verified Dependency Rate | Measures relationships supported by evidence |
| Overdue CI Reviews | Tracks records requiring review |

## 18.1 CI Verification Coverage

```text
CI Verification Coverage (%) =

In-Scope CIs Verified During Period
----------------------------------- x 100
Total CIs Requiring Verification
```

### Important

A complete CI record is not necessarily an accurate CI record.

Field completeness and technical verification should be measured separately.

---

# 19. Information Security Management Metrics

Security metrics evaluate selected controls and risk management activities.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Privileged Access Review Completion | Tracks completion of scheduled access reviews |
| Security Configuration Compliance | Measures systems meeting defined controls |
| Unnecessary Privilege Findings | Tracks identified excessive permissions |
| Security Remediation Time | Measures time to remediate defined findings |
| Overdue Security Reviews | Tracks missed review requirements |
| Security Policy Exception Count | Tracks approved or pending exceptions |

## 19.1 Privileged Access Review Completion

```text
Access Review Completion (%) =

Completed Required Access Reviews
--------------------------------- x 100
Total Scheduled Access Reviews
```

### Important

Completing an access review does not automatically prove that every permission is appropriate.

Review quality and corrective actions may require separate evaluation.

---

# 20. Knowledge Management Metrics

Knowledge metrics evaluate documentation quality and usefulness.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Knowledge Article Count | Tracks published articles |
| Article Review Completion | Measures scheduled reviews completed |
| Verified Article Rate | Measures articles with documented technical verification |
| Outdated Article Count | Tracks articles requiring updates |
| Knowledge Article Usage | Measures documented article use |
| Documentation Gap Count | Tracks identified missing knowledge |

### Important

Publishing more knowledge articles does not automatically improve service quality.

Accuracy, relevance, usability, and maintenance are also important.

---

# 21. Continual Improvement Metrics

Continual Improvement metrics evaluate improvement initiatives and outcomes.

### Proposed Metrics

| Metric | Purpose |
|---|---|
| Improvements Identified | Tracks new opportunities |
| Improvements Completed | Tracks initiatives reaching documented completion |
| Improvement Success Rate | Measures achievement of defined success criteria |
| Improvement Cycle Time | Measures elapsed time from defined start to completion |
| Improvement Backlog Age | Measures unresolved opportunity age |
| Verified Benefit Rate | Tracks improvements with evidence-supported benefits |
| Improvement Review Completion | Measures required reviews completed |

## 21.1 Improvement Success Rate

```text
Improvement Success Rate (%) =

Improvements Meeting Success Criteria
------------------------------------- x 100
Improvements With Evaluated Outcomes
```

### Important

A completed improvement is not necessarily a successful improvement.

Lifecycle status and measured outcome should be recorded separately.

---

# 22. Infrastructure Performance Metrics

Infrastructure metrics evaluate technical resource conditions.

### Potential Measurements

- CPU utilization
- Memory utilization
- Disk capacity
- Network latency
- Packet loss
- Service availability
- Virtual machine resource usage

### Windows Server Examples

**CPU utilization:**

```powershell
Get-Counter '\Processor(_Total)\% Processor Time'
```

**Available memory:**

```powershell
Get-Counter '\Memory\Available MBytes'
```

**Disk information:**

```powershell
Get-Volume
```

**Relevant service status:**

```powershell
Get-Service -Name DNS
```

### Important

A single measurement is a snapshot.

Meaningful performance analysis often requires repeated observations over a defined period.

Counter availability and naming can vary by Windows installation and configuration.

---

# 23. Service Availability Metrics

Availability measures whether a service is available during a defined period.

### Example Formula

```text
Service Availability (%) =

Agreed Service Time - Unavailable Time
-------------------------------------- x 100
          Agreed Service Time
```

### Required Definitions

- Service being measured
- Agreed service hours
- Measurement period
- Definition of unavailability
- Treatment of planned maintenance
- Treatment of partial degradation
- Monitoring method

### Illustrative Example

A service has:

- Agreed service time: 100 hours
- Unavailable time: 2 hours

```text
Availability =

(100 - 2) / 100 × 100

Availability = 98%
```

This is an illustrative calculation, not an observed lab result.

### Important

A server being powered on does not necessarily mean the service it supports is available.

Availability should be measured at the appropriate service level.

---

# 24. Network Performance Metrics

Network metrics help evaluate connectivity and performance.

### Potential Metrics

- Round-trip latency
- Packet loss
- Interface utilization
- Network availability
- Error counts
- Throughput
- Jitter

### Windows Examples

**Connectivity:**

```powershell
Test-NetConnection 10.20.10.10
```

**Repeated ICMP testing:**

```powershell
Test-Connection 10.20.10.10 -Count 10
```

**Network adapter statistics:**

```powershell
Get-NetAdapterStatistics
```

### Important

ICMP measurements may be affected by firewall policies, device configuration, and network conditions.

A successful ping does not prove that every application or network service is functioning correctly.

---

# 25. Azure Cost Metrics

Cost metrics can help identify opportunities to reduce unnecessary infrastructure spending.

### Potential Measurements

- Monthly compute charges
- Storage charges
- Network-related charges
- Resource utilization
- Virtual machine operating hours
- Cost per lab environment

### Potential Data Sources

- Azure Cost Management
- Azure billing reports
- Azure resource inventory
- Resource usage information

### Example Measurement Record

```text
Metric:
Monthly Azure Lab Cost

Baseline:
Not Yet Measured

Measurement Period:
Calendar Month

Data Source:
Azure Cost Management

Target:
To Be Established

Actual:
Not Yet Measured
```

### Important

Deallocating an Azure virtual machine generally stops its compute charges, but storage and other resources may continue generating charges.

Cost comparisons should use equivalent periods and account for changes in usage.

---

# 26. Baseline and Target Management

Baselines and targets should be maintained separately.

### Baseline

Represents the measured current or historical state.

### Target

Represents the desired future state.

### Actual

Represents observed performance during a measurement period.

### Example

| Metric | Baseline | Target | Actual |
|---|---|---|---|
| Incident Resolution Time | Pending | Pending | Pending |
| Change Success Rate | Pending | Pending | Pending |
| Service Availability | Pending | Pending | Pending |
| CI Verification Coverage | Pending | Pending | Pending |
| Azure Lab Cost | Pending | Pending | Pending |

### Baseline Rules

1. Record the measurement period.
2. Identify the source.
3. Use consistent calculation methods.
4. Preserve supporting evidence.
5. Identify missing data.
6. Document significant environmental changes.

### Target Rules

1. Define the desired outcome.
2. Consider feasibility.
3. Align with service objectives.
4. Record the rationale.
5. Review targets periodically.

### Important

Targets should not be represented as achieved results.

---

# 27. Data Collection Methods

## 27.1 Manual Collection

Suitable for:

- Small lab environments
- Individual scenarios
- Procedure verification
- Initial baseline measurements

### Advantages

- Low cost
- Simple implementation
- Direct observation

### Limitations

- Time-consuming
- Potentially inconsistent
- Requires manual verification

---

## 27.2 PowerShell Collection

Suitable for:

- Windows Server metrics
- Active Directory information
- Workstation configuration
- Event log analysis
- Repeated diagnostic checks

### Advantages

- Repeatable
- Scriptable
- Supports structured output
- Can reduce manual effort

### Limitations

- Requires suitable permissions
- May require modules
- Requires error handling
- Must be tested

---

## 27.3 ITSM Reporting

Potentially suitable for:

- Ticket volumes
- Incident response times
- Request fulfillment times
- Change outcomes
- Escalation patterns

### Tools

- Jira Service Management, if configured in the future
- Other suitable ITSM platforms

### Important

Do not claim automated reporting or live integrations unless they are actually configured and verified.

---

## 27.4 Monitoring Platforms

Potentially suitable for:

- Infrastructure availability
- Resource utilization
- Event detection
- Alert volumes
- Network performance

### Important

Monitoring coverage and measurement accuracy depend on the configured platform and data sources.

---

# 28. Metric Calculation Standards

Calculations should follow consistent rules.

### General Requirements

- Define the numerator.
- Define the denominator.
- Define the unit.
- Define the reporting period.
- Define included records.
- Define excluded records.
- Address missing data.
- Address zero denominators.
- Preserve the calculation method.

### Percentage Calculation

```text
Percentage =

Qualifying Observations
----------------------- x 100
 Total Observations
```

### Average Calculation

```text
Average =

Sum of Measured Values
----------------------
Number of Valid Measurements
```

### Percentage Change

```text
Percentage Change =

New Value - Baseline Value
-------------------------- x 100
      Baseline Value
```

### Important

Percentage change is undefined when the baseline is zero.

Also, an increase is not always desirable.

For example:

- Increased service availability may be positive.
- Increased incident recurrence may be negative.

Interpret the direction of change according to the metric's purpose.

---

# 29. Data Quality Standards

Reliable metrics require reliable data.

### Quality Dimensions

| Dimension | Description |
|---|---|
| Accuracy | Data reflects actual observations |
| Completeness | Required data is available |
| Consistency | Measurements follow the same rules |
| Timeliness | Data is collected when relevant |
| Validity | Values meet defined requirements |
| Traceability | Results can be linked to supporting evidence |

### Validation Checklist

- [ ] Correct reporting period
- [ ] Correct data source
- [ ] Consistent units
- [ ] Duplicate records reviewed
- [ ] Missing values identified
- [ ] Calculation verified
- [ ] Inclusion criteria followed
- [ ] Exclusion criteria followed
- [ ] Evidence available
- [ ] Limitations documented

### Important

Do not silently replace missing data with zero.

Zero and unknown have different meanings.

---

# 30. Metric Reporting Standards

Metric reports should communicate performance clearly.

### Required Report Information

- Report title
- Reporting period
- Preparing role
- Related service
- Metrics included
- Data sources
- Actual results
- Baselines
- Targets
- Variances
- Significant findings
- Data limitations
- Recommended actions

### Proposed Report Naming

```text
Service-Metrics/
└── Reports/
    ├── Monthly/
    │   └── YYYY-MM-Service-Performance.md
    └── Quarterly/
        └── YYYY-Q#-Service-Performance.md
```

### Example

```text
2026-10-Service-Performance.md
```

The filename is illustrative.

### Important

Do not create performance reports implying operational measurements were collected when no supporting data exists.

---

# 31. Service Performance Report Template

```text
SERVICE PERFORMANCE REPORT

Organization:
Technical Techno Tech

Report ID:
Reporting Period:
Prepared By:
Report Status:

Services Evaluated:
ITIL Practices Evaluated:

Metric Summary:

Metric ID:
Metric Name:
Data Source:
Measurement Period:
Baseline:
Target:
Actual Result:
Variance:
Measurement Status:

Performance Findings:

Positive Trends:

Negative Trends:

Data Quality Issues:

Service Risks:

Improvement Opportunities:

Related Improvement IDs:

Recommended Actions:

Evidence References:

Limitations:

Review Outcome:

Next Reporting Period:
```

A dedicated reusable metric template is planned at:

`Templates/Service-Metric-Template.md`

This section provides an interim reporting structure until that template is created.

---

# 32. Metric Visualization Standards

Visualizations can help communicate performance trends.

### Suitable Visualizations

| Visualization | Suitable Use |
|---|---|
| Line Chart | Performance over time |
| Bar Chart | Comparing categories |
| Table | Detailed metric values |
| Percentage Summary | Compliance or completion rates |
| Trend Summary | Direction of performance changes |

### Example

A line chart may display incident resolution time over several reporting periods.

### Visualization Rules

1. Use actual or clearly labeled simulated data.
2. Identify the measurement period.
3. Label units.
4. Include relevant context.
5. Avoid misleading axis scales.
6. Distinguish targets from actual values.
7. Document data sources.

### Important

A visually attractive chart is not evidence of accurate performance measurement.

---

# 33. Metric Interpretation and Limitations

Metrics should be interpreted alongside operational context.

### Example: Incident Resolution Time

An increase in average resolution time may result from:

- More complex incidents
- Different incident priorities
- Changes in ticket volume
- Incomplete documentation
- Resource limitations
- Changes in the measurement method

### Example: Change Success Rate

A high change success rate may indicate effective change management.

However, it may also reflect:

- Limited change complexity
- Inconsistent success definitions
- Incomplete reporting
- Small sample size

### Example: Service Availability

A high server uptime percentage may not reflect application availability or user experience.

### Important

Metrics provide information for investigation and decision-making.

They should not be treated as complete explanations of service performance.

---

# 34. Service Metrics and Continual Improvement

Metrics provide a foundation for identifying and evaluating improvement opportunities.

### Example Workflow

```text
Collect Performance Data
          |
          v
Identify Performance Gap
          |
          v
Investigate Contributing Factors
          |
          v
Register Improvement Opportunity
          |
          v
Define Baseline and Target
          |
          v
Implement Authorized Improvement
          |
          v
Measure New Performance
          |
          v
Evaluate Results
          |
          v
Update Improvement Register
```

### Example

**Observation:** Incident resolution times are increasing.

**Potential Investigation:**

- Review incident categories.
- Review incident complexity.
- Review escalation patterns.
- Review knowledge documentation.
- Review staffing or resource constraints.

**Potential Improvement:** Standardize troubleshooting documentation.

### Important

The improvement should be based on the findings of the investigation, not merely the existence of an unfavorable metric.

### Related Documents

- [Continual Improvement Overview](../README.md)
- [Improvement Management SOP](../Procedures/Improvement-Management.md)
- [Improvement Register](../Improvement-Register.md)

---

# 35. Example Lab — Measuring Active Directory Health-Check Efficiency

## Scenario Overview

Technical Techno Tech evaluates whether a standardized diagnostic script improves the efficiency of Active Directory health checks.

**Proposed Improvement:** IMP-001 — Standardize Active Directory Health Checks

**Related Service:** IT-SVC-005 — Server & Infrastructure Services

### Lab Environment

| System | Role | IP Address |
|---|---|---|
| DC01 | Domain Controller | 10.20.10.10 |
| DC02 | Domain Controller | 10.20.10.11 |
| MGMT01 | Administrative Workstation | 10.20.30.10 |

### Measurement Objective

Compare the time required to perform a defined set of manual health checks against a standardized script performing equivalent checks.

### Proposed Measurements

- Execution duration
- Number of manual actions
- Output completeness
- Diagnostic accuracy
- Error visibility

---

## 35.1 Establish the Manual Baseline

Define the manual diagnostic procedure.

### Example Commands

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

```powershell
Get-ADDomainController -Filter *
```

### Measurement Requirements

1. Define the exact task.
2. Record the starting time.
3. Execute the required commands.
4. Review the results.
5. Record the ending time.
6. Calculate elapsed time.
7. Preserve relevant observations.

### Baseline Status

Not Yet Measured.

---

## 35.2 Measure the Script Method

Execute the proposed standardized health-check script in an authorized lab environment.

### Example Timing Method

```powershell
$StartTime = Get-Date

# Execute the verified health-check script here.

$EndTime = Get-Date

$Duration = $EndTime - $StartTime

$Duration.TotalSeconds
```

### Important

The timing method must include equivalent work for a fair comparison.

If the manual method includes interpreting and documenting results, the scripted method should be evaluated against comparable requirements.

---

## 35.3 Compare Results

| Measurement | Manual Method | Script Method |
|---|---|---|
| Execution duration | Pending | Pending |
| Manual actions | Pending | Pending |
| Diagnostic completeness | Pending | Pending |
| Error visibility | Pending | Pending |
| Documentation consistency | Pending | Pending |

### Success Criteria

To be defined before implementation.

### Lab Status

This is a proposed measurement exercise.

No timing results, performance gains, or successful script execution are claimed.

---

# 36. Example Lab — Measuring Incident Resolution Time

## Scenario Overview

Technical Techno Tech evaluates incident resolution time using documented incident records.

### Measurement Definition

**Start:** Incident logging timestamp.

**End:** Recorded resolution timestamp.

**Unit:** Minutes.

This is one possible definition and should be applied consistently.

### Illustrative Dataset

| Incident | Logged | Resolved | Duration |
|---|---|---|---|
| INC-001 | 09:00 | 09:30 | 30 minutes |
| INC-002 | 10:00 | 11:00 | 60 minutes |
| INC-003 | 13:00 | 13:45 | 45 minutes |

### Calculation

```text
Average Resolution Time =

(30 + 60 + 45) / 3

Average Resolution Time = 45 minutes
```

### Important

These are fictional example values.

They do not represent actual incidents, ticket records, or operational performance.

### Actual Lab Procedure

1. Select real lab incident records.
2. Verify the timestamps.
3. Apply the metric definition.
4. Calculate elapsed time.
5. Identify exclusions.
6. Calculate the average.
7. Document limitations.
8. Preserve evidence.

---

# 37. Example Lab — Measuring Configuration Accuracy

## Scenario Overview

Technical Techno Tech evaluates the accuracy of documented Configuration Item records.

### Measurement Objective

Determine how many reviewed CIs match their recorded configuration attributes.

### Proposed Procedure

1. Identify the in-scope CI records.
2. Define required attributes.
3. Select verification methods.
4. Inspect the actual systems.
5. Compare observed and documented values.
6. Record discrepancies.
7. Calculate the result.
8. Document corrective actions.

### Example Metric

```text
Verified CI Accuracy (%) =

Reviewed CIs Without Defined Discrepancies
----------------------------------------- x 100
Total CIs Reviewed
```

### Important

Define what constitutes a discrepancy.

A missing optional attribute should not necessarily be treated the same as an incorrect critical configuration value.

### Measurement Status

Not Yet Measured.

---

# 38. Example Lab — Measuring Azure Cost Optimization

## Scenario Overview

Technical Techno Tech evaluates whether Azure lab resource scheduling reduces unnecessary spending.

### Measurement Objective

Compare Azure costs before and after implementing an authorized resource management improvement.

### Proposed Measurements

- Monthly compute cost
- Monthly storage cost
- Total monthly cost
- VM operating hours
- Lab availability

### Example Table

| Metric | Before | After |
|---|---|---|
| Compute cost | Pending | Pending |
| Storage cost | Pending | Pending |
| Total cost | Pending | Pending |
| VM operating hours | Pending | Pending |
| Lab availability | Pending | Pending |

### Evaluation Requirements

- Compare equivalent billing periods.
- Review resource changes.
- Account for storage and other continuing charges.
- Verify that required lab functionality remains available.
- Distinguish cost savings from changes in usage.

### Measurement Status

Not Yet Measured.

---

# 39. Metric Review and Maintenance

Metrics should be reviewed when service objectives, processes, or data sources change.

### Review Triggers

- New IT services
- Service retirement
- Process changes
- New ITSM tools
- Monitoring changes
- Configuration changes
- New security requirements
- Continual improvement initiatives
- Unreliable data
- Outdated targets
- Reporting requirements

### Proposed Review Frequency

| Metric Category | Suggested Review |
|---|---|
| Critical Service Performance | Monthly |
| Operational Process Performance | Monthly or Quarterly |
| Security Controls | Based on risk and control requirements |
| Configuration Accuracy | Quarterly or after significant changes |
| Continual Improvement | Monthly or Quarterly |
| Infrastructure Cost | Monthly |

These are proposed review intervals, not mandatory ITIL requirements.

### Review Checklist

- [ ] Metric remains relevant
- [ ] Owner identified
- [ ] Definition accurate
- [ ] Data source available
- [ ] Calculation valid
- [ ] Measurement period appropriate
- [ ] Baseline reviewed
- [ ] Target reviewed
- [ ] Evidence available
- [ ] Limitations documented
- [ ] Improvement opportunities considered

---

# 40. Metric Retirement

A metric may be retired when it no longer provides useful information.

### Potential Reasons

- Service retired
- Metric duplicated
- Data source unavailable
- Measurement no longer relevant
- Better metric adopted
- Collection cost exceeds value
- Business objective changed

### Retirement Procedure

1. Identify the metric.
2. Document the reason.
3. Review reporting dependencies.
4. Identify replacement measurements where appropriate.
5. Preserve historical results.
6. Update related documentation.
7. Mark the metric retired.

### Important

Retiring a metric should not erase historical performance evidence.

---

# 41. Common Service Measurement Errors

### Error 1 — Measuring Without a Purpose

**Incorrect:** Collecting large amounts of data without knowing how it will be used.

**Correct:** Define the measurement objective first.

### Error 2 — No Baseline

**Incorrect:** Claiming improvement without knowing previous performance.

**Correct:** Establish a baseline when practical.

### Error 3 — Undefined Calculation

**Incorrect:** Reporting average resolution time without defining its start and end points.

**Correct:** Document the calculation method.

### Error 4 — Comparing Different Periods

**Incorrect:** Comparing one week of incidents with one month of incidents without adjustment.

**Correct:** Use comparable periods or normalize the data.

### Error 5 — Confusing Targets With SLAs

**Incorrect:** Calling an internal performance target an SLA without an agreement.

**Correct:** Distinguish internal targets, SLOs, and actual SLAs.

### Error 6 — Missing Data Treated as Zero

**Incorrect:** Recording an unknown value as zero.

**Correct:** Mark missing information explicitly.

### Error 7 — Ignoring Data Quality

**Incorrect:** Calculating results from duplicate or incomplete records without review.

**Correct:** Validate the data first.

### Error 8 — Misleading Averages

**Incorrect:** Assuming an average represents every incident.

**Correct:** Consider distribution, outliers, and severity.

### Error 9 — Activity Confused With Outcome

**Incorrect:** Treating the number of completed checks as proof of better security.

**Correct:** Evaluate whether the checks produce the intended results.

### Error 10 — Fabricated Performance Data

**Incorrect:** Publishing fictional measurements as real operational performance.

**Correct:** Clearly label examples and report actual observations separately.

### Error 11 — Changing Definitions Without Documentation

**Incorrect:** Revising a calculation and comparing the new result directly with old values.

**Correct:** Record definition changes and assess comparability.

### Error 12 — Overemphasizing a Single Metric

**Incorrect:** Optimizing ticket closure speed while ignoring resolution quality.

**Correct:** Use complementary measures where appropriate.

---

# 42. Service Metrics Quality Checklist

## Metric Definition

- [ ] Unique metric ID assigned
- [ ] Descriptive metric name selected
- [ ] Measurement purpose defined
- [ ] Related service identified
- [ ] Related ITIL practice identified
- [ ] Metric owner assigned
- [ ] Unit defined
- [ ] Calculation documented

## Data Collection

- [ ] Data source identified
- [ ] Collection method defined
- [ ] Measurement period established
- [ ] Inclusion criteria defined
- [ ] Exclusion criteria defined
- [ ] Missing data handling documented
- [ ] Evidence requirements established

## Baseline and Targets

- [ ] Baseline measured or marked unavailable
- [ ] Target defined or marked pending
- [ ] Target rationale documented
- [ ] Measurement methods comparable

## Validation

- [ ] Data quality reviewed
- [ ] Duplicate records checked
- [ ] Units consistent
- [ ] Calculations verified
- [ ] Limitations documented
- [ ] Results supported by evidence

## Reporting

- [ ] Reporting period identified
- [ ] Actual results recorded
- [ ] Baseline comparison included
- [ ] Target comparison included
- [ ] Trends interpreted
- [ ] Findings documented
- [ ] Recommended actions identified

## Continual Improvement

- [ ] Performance gaps reviewed
- [ ] Improvement opportunities considered
- [ ] Related Improvement IDs linked
- [ ] Follow-up actions documented
- [ ] Metric review date recorded

## Portfolio Accuracy

- [ ] Simulated data clearly labeled
- [ ] Actual measurements distinguished from examples
- [ ] No fabricated service performance
- [ ] No unverified integrations claimed
- [ ] Sensitive information removed
- [ ] Relative links verified

---

# 43. Integration With ITIL Practices

| ITIL Practice | Measurement Relationship |
|---|---|
| Service Desk | Ticket response, categorization, escalation, and backlog metrics |
| Incident Management | Resolution, restoration, recurrence, and reopening metrics |
| Service Request Management | Fulfillment time, accuracy, and request volume |
| Knowledge Management | Article accuracy, review completion, and usage |
| Problem Management | Problem backlog, root cause identification, and recurrence |
| Change Enablement | Change success, rollback, and review completion |
| Monitoring and Event Management | Detection, alert quality, and monitoring coverage |
| Service Configuration Management | CI accuracy, verification, and dependency coverage |
| Information Security Management | Access reviews, compliance, and remediation |
| Continual Improvement | Improvement outcomes, verified benefits, and backlog management |

### Important

Service measurement is a shared capability supporting multiple ITIL practices.

It does not require a sequential workflow through every practice.

---

# 44. Document Review

Review this guide when:

- New services are introduced.
- Measurement objectives change.
- ITSM reporting capabilities change.
- Monitoring tools are introduced.
- New data sources become available.
- Metric calculations change.
- Reporting requirements evolve.
- Significant data quality issues are identified.
- Continual improvement reviews identify weaknesses.
- Related ITIL procedures are revised.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial IT Service Metrics documentation standards, measurement procedures, and lab examples |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This directory and documentation guide demonstrate the application of ITIL 4 Continual Improvement principles to service performance measurement and reporting.

Metric definitions, organizational responsibilities, reporting intervals, targets, and service performance examples may be proposed or simulated.

Actual performance measurements must be supported by verifiable lab observations, technical output, or documented operational records.

Illustrative calculations and fictional datasets must not be represented as actual service performance.

No automated ITSM reporting, monitoring integration, SLA achievement, cost savings, or operational improvement is claimed unless independently supported by documented lab evidence.

GitHub Markdown files provide a lightweight reporting and documentation framework and are not represented as a production service analytics platform.

This documentation demonstrates metric definition, data collection, baseline establishment, target setting, calculation, data validation, performance analysis, reporting, and evidence-based continual improvement.
