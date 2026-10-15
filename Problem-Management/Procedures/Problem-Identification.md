# SOP — Problem Identification

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Problem Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-PM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Problem Management

---

## 1. Purpose

This procedure establishes a standardized method for identifying and recording IT problems within Technical Techno Tech.

Problem identification focuses on recognizing actual or potential underlying causes of incidents, recurring technical failures, and infrastructure conditions that could lead to future service disruptions.

The procedure supports:

- Early identification of recurring technical issues
- Reduction of repeat incidents
- Identification of infrastructure weaknesses
- Proactive risk management
- Improved service reliability
- Accurate problem classification
- Effective problem prioritization
- Evidence-based technical investigation
- Improved collaboration between IT support teams
- Continual improvement

**Key Principle:** A problem does not need to have a confirmed root cause before it can be identified and recorded. The purpose of Problem Management is to investigate actual or potential causes and reduce the likelihood and impact of incidents.

---

## 2. Scope

This procedure applies to potential problems affecting Technical Techno Tech's internal IT services and supporting infrastructure.

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

Problem identification may involve:

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

Technologies should only be described as operational when actually configured or used in the lab.

---

## 3. ITIL 4 Problem Management

### Purpose

The purpose of Problem Management is to reduce the likelihood and impact of incidents by identifying actual and potential causes of incidents and managing workarounds and known errors.

### Important Definitions

**Incident:** An unplanned interruption to a service or reduction in the quality of a service.

**Problem:** A cause, or potential cause, of one or more incidents.

**Known Error:** A problem that has been analyzed but has not been resolved.

**Workaround:** A solution that reduces or eliminates the impact of an incident or problem for which a full resolution is not yet available.

### Incident vs. Problem

| Incident Management | Problem Management |
|---|---|
| Restores disrupted services | Investigates underlying or potential causes |
| Focuses on immediate service restoration | Focuses on preventing or reducing future disruptions |
| Addresses individual incidents | May address multiple related incidents |
| May use temporary workarounds | Develops and manages workarounds and known errors |
| Prioritizes restoring service | Prioritizes reducing long-term risk |

### Example

**Incident:** A Windows Server DNS service unexpectedly stops.

**Problem:** The DNS service repeatedly stops because of an unidentified underlying condition.

Incident Management restores DNS functionality.

Problem Management investigates why the service continues to fail.

---

## 4. Reactive and Proactive Problem Identification

Technical Techno Tech uses two approaches to identify problems.

### 4.1 Reactive Problem Identification

Reactive identification occurs after one or more incidents reveal a possible underlying issue.

#### Examples

- Repeated domain authentication failures
- Multiple incidents involving the same application
- Recurring DNS service failures
- Repeated network outages
- Multiple workstations experiencing similar errors
- A significant incident with an unresolved underlying cause

**Objective:** Identify potential causes contributing to incidents that have already occurred.

### 4.2 Proactive Problem Identification

Proactive identification occurs before an incident or additional incidents happen.

#### Examples

- Monitoring identifies recurring disk capacity warnings.
- Server logs reveal repeated service failures.
- Network monitoring shows increasing packet loss.
- Infrastructure reviews identify unsupported software.
- Capacity analysis reveals insufficient resources.
- Configuration reviews identify a potential single point of failure.

**Objective:** Identify conditions that could cause future incidents.

### Comparison

| Reactive | Proactive |
|---|---|
| Triggered by existing incidents | Triggered by trends, risks, or technical observations |
| Uses incident history | Uses monitoring and analysis |
| Investigates experienced failures | Investigates potential future failures |
| Reduces recurrence | Reduces likelihood of occurrence |

Both approaches support service reliability.

---

## 5. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Recognizing repeated incident patterns
- Reviewing related incident records
- Reporting suspected problems
- Documenting recurring symptoms
- Identifying potential knowledge gaps
- Escalating problem candidates

### Technical Support Specialist

Responsible for:

- Identifying recurring technical failures
- Reviewing troubleshooting evidence
- Recognizing shared technical dependencies
- Recommending problem investigation
- Documenting relevant observations

### Problem Manager / Coordinator

Responsible for:

- Reviewing problem candidates
- Determining whether a Problem record is appropriate
- Coordinating problem identification
- Reviewing business impact
- Assigning preliminary priority
- Assigning problem ownership
- Monitoring the Problem Register

### Systems Administrator

Responsible for:

- Identifying server and directory service problems
- Reviewing Windows Server logs
- Evaluating Active Directory health
- Identifying infrastructure risks
- Providing technical evidence

### Network Administrator

Responsible for:

- Identifying recurring network failures
- Reviewing routing and switching behavior
- Evaluating network performance
- Identifying configuration risks
- Providing network diagnostic evidence

### Cloud Administrator

Responsible for:

- Identifying Microsoft 365 and Azure service patterns
- Reviewing relevant cloud service health
- Evaluating cloud configuration risks
- Documenting recurring cloud issues

### Information Security Personnel

Responsible for:

- Identifying security-related technical risks
- Reviewing repeated security events
- Coordinating with security incident handling
- Recommending investigation of underlying security weaknesses

**Lab Note:** These roles are simulated organizational responsibilities. One learner may perform multiple roles during a controlled lab exercise.

---

## 6. Problem Identification Sources

Problems may be identified through several operational sources.

| Source | Potential Problem Indicator |
|---|---|
| Incident Records | Repeated or related service disruptions |
| Service Desk Reports | Similar complaints from multiple employees |
| Monitoring Events | Repeated alerts or abnormal conditions |
| Event Logs | Recurring technical errors |
| Problem Reviews | Previously unresolved issues |
| Change Records | Repeated failures following configuration changes |
| Configuration Reviews | Weaknesses or inconsistencies |
| Capacity Monitoring | Resource exhaustion trends |
| Security Reviews | Recurring vulnerabilities or control failures |
| Vendor Advisories | Known defects affecting deployed technology |
| Technical Assessments | Potential infrastructure failure points |

A single significant incident may justify problem investigation even without a recurring pattern.

---

## 7. Problem Identification Criteria

A potential problem should be evaluated when one or more of the following conditions exist.

### Criterion 1 — Recurring Incidents

Multiple incidents share similar symptoms, affected services, or infrastructure dependencies.

### Criterion 2 — Significant Incident

A major or high-impact incident occurs and the underlying cause remains unknown or requires further analysis.

### Criterion 3 — Repeated Technical Errors

System logs or monitoring tools identify recurring failures.

### Criterion 4 — Unknown Underlying Cause

Service is restored, but evidence suggests an unresolved condition that may cause future incidents.

### Criterion 5 — Infrastructure Risk

A technical weakness could reasonably cause future service disruption.

### Criterion 6 — Repeated Workaround Usage

A service repeatedly depends on a temporary workaround.

### Criterion 7 — Known Vendor Defect

A documented software or hardware defect may affect an existing service.

### Criterion 8 — Related Incident Trend

Different symptoms may share a common infrastructure dependency.

**Important:** These criteria identify candidates for assessment. They do not automatically prove that the incidents have the same underlying cause.

---

## 8. Problem Identification Workflow

```text
Incident / Monitoring / Risk Observation
                  |
                  v
       Identify Potential Pattern
                  |
                  v
       Review Available Evidence
                  |
                  v
       Check Existing Problems
                  |
                  v
       Assess Business Relevance
                  |
                  v
       Problem Candidate Valid?
                  |
             +----+----+
             |         |
            Yes        No
             |         |
             v         v
       Create Problem   Document
           Record       Assessment
             |         |
             v         v
       Classify and     Continue
         Prioritize     Monitoring
             |
             v
       Assign Ownership
             |
             v
       Link Related Records
             |
             v
       Begin Problem Analysis
```

Problem identification may occur while Incident Management continues restoring affected services.

---

## 9. Problem Identification Procedure

### Step 1 — Identify a Potential Problem

Recognize a recurring failure, significant incident, technical trend, or infrastructure risk.

Potential indicators include:

- Multiple incidents with similar symptoms
- Repeated service restarts
- Frequent authentication failures
- Recurring network disconnections
- Persistent performance degradation
- Repeated application crashes
- Monitoring trends indicating possible service failure

#### Example

Several incidents report that employees cannot authenticate to the domain.

The Service Desk identifies a possible recurring authentication issue.

**Expected Result:** A potential problem is identified for assessment.

### Step 2 — Collect Initial Information

Gather relevant information about the suspected problem.

Record:

- Affected service
- Reported symptoms
- Date first observed
- Frequency of occurrence
- Known affected systems
- Number of related incidents
- Business impact
- Existing workarounds
- Relevant technical evidence

#### Example

```text
Potential Problem: Recurring Domain Authentication Failures

Affected Service: IT-SVC-001
Technical Category: Active Directory
Affected Systems: CLIENT01, DC01
Observed Pattern: Multiple authentication incidents
Suspected Cause: Not yet determined
```

**Expected Result:** Initial evidence is available for evaluation.

### Step 3 — Review Related Incident Records

Examine incident history for common characteristics.

Compare:

1. Reported symptoms
2. Affected services
3. Affected users
4. Affected systems
5. Time of occurrence
6. Error messages
7. Resolution methods
8. Recurrence frequency

#### Example

| Incident | Reported Issue | Potential Relationship |
|---|---|---|
| INC-001 | Domain authentication failure | Identity service |
| INC-002 | Domain authentication failure | Identity service |
| INC-003 | Group Policy processing failure | Possible directory or DNS dependency |

The table is illustrative.

The incidents may be related, but the relationship must be evaluated.

**Expected Result:** Relevant incident patterns are documented.

### Step 4 — Identify Shared Dependencies

Determine whether affected incidents share infrastructure components.

Potential shared dependencies include:

- Domain controllers
- DNS servers
- DHCP servers
- Network switches
- Routers
- Firewalls
- File servers
- Authentication services
- Cloud identity services

#### Example

```text
CLIENT01 ----+
             |
CLIENT02 ----+---- DNS / Active Directory
             |           |
CLIENT03 ----+           v
                        DC01
```

Multiple authentication incidents may involve a shared domain controller or DNS service.

However, shared infrastructure does not automatically establish causation.

**Expected Result:** Potential common dependencies are identified.

### Step 5 — Review Monitoring and Technical Evidence

Review relevant diagnostic information.

Examples:

- Windows Event Logs
- Server monitoring alerts
- Active Directory diagnostics
- DNS service status
- Network performance data
- Disk capacity trends
- Application logs
- Virtualization alerts

#### Example — Windows Server

Review recent system errors:

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    Level = 2
    StartTime = (Get-Date).AddDays(-7)
} -MaxEvents 50
```

#### Example — Active Directory

Review replication health:

```powershell
repadmin /replsummary
```

#### Example — Domain Controller Diagnostics

```powershell
dcdiag /q
```

These commands provide diagnostic information. They do not independently confirm the underlying cause of a problem.

**Expected Result:** Technical evidence supports further problem assessment.

### Step 6 — Check for Existing Problem Records

Search the Problem Register and existing Problem records.

Review:

- Problem summaries
- Affected services
- Technical categories
- Related incidents
- Known errors
- Existing workarounds
- Investigation status

#### Decision

If an existing Problem record covers the suspected issue:

- Link relevant incidents.
- Add new evidence.
- Update the problem record as appropriate.
- Avoid unnecessary duplication.

If no relevant Problem record exists:

- Continue the identification process.

**Expected Result:** Duplicate Problem records are minimized.

### Step 7 — Assess Business Impact

Determine the actual or potential impact of the suspected problem.

Consider:

- Number of affected employees
- Frequency of incidents
- Criticality of affected services
- Duration of disruptions
- Availability of workarounds
- Operational consequences
- Security implications
- Potential future impact

#### Impact Levels

| Impact | Description |
|---|---|
| High | Critical services or significant business operations may be affected |
| Medium | Departmental operations or multiple users may be affected |
| Low | Limited service or individual-user impact |

**Expected Result:** Business impact is documented.

### Step 8 — Assess Likelihood and Recurrence

Evaluate the likelihood of future incidents.

Consider:

- Historical incident frequency
- Recurring monitoring alerts
- Known technical weaknesses
- Recent configuration changes
- Vendor advisories
- Capacity trends
- Existing mitigation measures

#### Likelihood Levels

| Likelihood | Description |
|---|---|
| High | Repeated failures or strong evidence of likely recurrence |
| Medium | Some evidence of recurrence or a plausible future failure |
| Low | Limited evidence of recurrence or future failure |

Likelihood assessments should be supported by available evidence.

**Expected Result:** Recurrence risk is assessed.

### Step 9 — Determine Whether a Problem Record Is Required

Review the available information.

A Problem record may be appropriate when:

- Related incidents suggest a common cause.
- A significant incident requires further analysis.
- An unresolved technical condition presents a meaningful risk.
- A recurring workaround indicates an unresolved issue.
- Proactive monitoring identifies a potential future failure.

A Problem record is not automatically required for every incident.

#### Example

**Incident:** A single employee enters an incorrect password.

**Assessment:** This may be an isolated support issue without evidence of an underlying technical problem.

**Alternative Example:** Multiple employees repeatedly experience authentication failures associated with a shared service.

**Assessment:** Further Problem Management investigation may be appropriate.

**Expected Result:** A documented decision is made.

### Step 10 — Create the Problem Record

Assign a unique Problem identifier.

#### Naming Convention

```text
PRB-001
PRB-002
PRB-003
```

#### Example Record Location

```text
Problem-Management/
└── Records/
    └── PRB-001-Recurring-Authentication-Failures/
        ├── README.md
        └── Evidence/
```

Use the standardized template:

[Problem Template](../../Templates/Problem-Template.md)

**Expected Result:** The identified problem has a traceable record.

### Step 11 — Document the Problem Description

Describe the observed condition without assuming an unverified cause.

#### Recommended Format

```text
Problem Summary:
Affected Service:
Observed Symptoms:
Related Incidents:
Affected Systems:
Frequency:
Business Impact:
Known Workarounds:
Potential Causes:
Evidence:
```

#### Example

**Problem Summary:** Recurring Active Directory Authentication Failures

**Description:**

Multiple simulated incidents involve employees experiencing intermittent domain authentication failures.

The incidents may share infrastructure dependencies involving DNS or domain controller availability.

The underlying cause has not yet been confirmed.

**Expected Result:** The Problem record accurately describes the observed issue.

### Step 12 — Categorize the Problem

Assign an appropriate technical category.

| Category | Example Subcategory |
|---|---|
| Active Directory | Authentication |
| Windows Server | Service Availability |
| Networking | DNS Resolution |
| Networking | Routing |
| Microsoft 365 | Application Availability |
| Microsoft Entra ID | Sign-In |
| Endpoint Management | Application Stability |
| Virtualization | Resource Availability |

Categories should reflect available evidence.

They may be updated during subsequent investigation.

**Expected Result:** The problem is classified for analysis and reporting.

### Step 13 — Prioritize the Problem

Problem priority should reflect business impact, risk, likelihood of recurrence, and the need for investigation.

Problem priority is not necessarily identical to the priority of an associated incident.

#### Proposed Problem Priority Levels

| Priority | Description |
|---|---|
| P1 — Critical | Significant ongoing or imminent risk to critical services |
| P2 — High | Substantial business impact or high recurrence risk |
| P3 — Medium | Moderate operational impact requiring planned investigation |
| P4 — Low | Limited impact or low-risk investigation |

#### Example

A recurring domain controller failure affecting multiple departments may justify high problem priority.

A low-impact application issue with an effective workaround may receive a lower priority.

Document the rationale.

**Expected Result:** The problem receives an appropriate preliminary priority.

### Step 14 — Assign Problem Ownership

Assign responsibility for further analysis.

Potential owners include:

- Systems Administration
- Network Administration
- Endpoint Support
- Microsoft 365 Administration
- Cloud Administration
- Information Security

Ownership should reflect the suspected technical area and required expertise.

#### Example

```text
Problem ID: PRB-001
Category: Active Directory
Assigned Group: Systems Administration
Status: New
```

**Expected Result:** A responsible owner is identified.

### Step 15 — Link Related Records

Associate the Problem record with relevant operational documentation.

Potential related records include:

- Incident records
- Monitoring events
- Change records
- Configuration Items
- Knowledge articles
- Continual improvement records

#### Example

```text
Problem: PRB-001

Related Incidents:
- INC-001
- INC-002
- INC-003

Affected Configuration Items:
- DC01
- DC02

Related Monitoring Events:
- To Be Determined

Related Changes:
- None Identified
```

Only link records that actually exist or clearly identify references as illustrative.

**Expected Result:** Relevant relationships are documented.

### Step 16 — Record Initial Investigation Requirements

Identify what additional analysis is necessary.

#### Example

**Problem:** Recurring domain authentication failures

**Initial Investigation Plan:**

1. Review related incident timelines.
2. Examine domain controller health.
3. Review DNS configuration.
4. Analyze relevant Event Logs.
5. Check Active Directory replication.
6. Compare affected and unaffected systems.
7. Evaluate recent infrastructure changes.
8. Identify potential underlying causes.

Do not record a root cause before sufficient evidence exists.

**Expected Result:** The problem is ready for further analysis.

### Step 17 — Update the Problem Register

Record the new problem in the organization's Problem Register.

#### Example

| Problem ID | Summary | Priority | Status | Owner |
|---|---|---|---|---|
| PRB-001 | Recurring Authentication Failures | P2 | New | Systems Administration |
| PRB-002 | Repeated DNS Service Failure | P3 | New | Systems Administration |

These entries are illustrative.

**Expected Result:** The problem is available for tracking and reporting.

---

## 10. Problem Identification Decision Matrix

The following matrix provides examples of when further Problem Management assessment may be appropriate.

| Observation | Problem Assessment |
|---|---|
| One isolated user error | Usually not necessary without additional risk |
| Multiple incidents with similar symptoms | Recommended |
| Repeated service failure | Recommended |
| Major incident with unknown cause | Strongly recommended |
| Repeated use of a workaround | Recommended |
| Monitoring indicates possible future outage | Recommended |
| Single resolved incident with confirmed isolated cause | May not be necessary |
| Significant infrastructure vulnerability | Assess through Information Security and Problem Management as appropriate |
| Repeated failures after configuration changes | Recommended |

These are proposed guidelines rather than mandatory ITIL rules.

---

## 11. Problem Identification Through Incident Trends

Incident trend analysis helps identify recurring technical patterns.

### Example Dataset

| Incident ID | Date | Category | Affected Service |
|---|---|---|---|
| INC-001 | Day 1 | Authentication | Identity & Access |
| INC-002 | Day 3 | Authentication | Identity & Access |
| INC-003 | Day 5 | Authentication | Identity & Access |
| INC-004 | Day 6 | DNS Resolution | Network Connectivity |

### Potential Findings

- Authentication incidents occur repeatedly.
- The incidents may share a DNS dependency.
- A common infrastructure condition may exist.
- Further investigation may be justified.

### Trend Analysis Questions

1. Are incidents increasing?
2. Are similar systems affected?
3. Do incidents occur at similar times?
4. Do incidents follow configuration changes?
5. Are the same workarounds repeatedly used?
6. Is there a common technical dependency?

**Important:** Trend analysis identifies possible relationships, not confirmed root causes.

---

## 12. Proactive Problem Identification

Proactive Problem Management identifies risks before they cause additional service disruption.

### Example 1 — Disk Capacity

Monitoring shows that a Windows Server is approaching its storage capacity.

Potential problem:

**Insufficient available storage may cause future service disruption.**

Possible next steps:

- Review storage usage trends.
- Identify affected services.
- Evaluate capacity requirements.
- Determine whether corrective planning is needed.

### Example 2 — Domain Controller Health

Periodic diagnostics identify repeated Active Directory replication warnings.

Potential problem:

**An unresolved replication condition may affect directory service reliability.**

Possible next steps:

- Review replication errors.
- Check connectivity and DNS dependencies.
- Evaluate the scope of the issue.
- Create a Problem record when warranted.

### Example 3 — Network Performance

Monitoring identifies recurring packet loss affecting a network segment.

Potential problem:

**A network infrastructure condition may be degrading connectivity.**

Possible next steps:

- Review interface statistics.
- Examine network topology.
- Compare affected systems.
- Investigate relevant routing and switching components.

### Example 4 — Unsupported Software

An infrastructure review identifies software approaching the end of vendor support.

Potential problem:

**The unsupported software may introduce future service reliability or security risks.**

Possible next steps:

- Identify affected services.
- Review vendor support timelines.
- Assess operational impact.
- Coordinate with Change Enablement and Information Security Management.

---

## 13. Problem Identification Evidence

Evidence should support the decision to create or investigate a Problem record.

### Evidence Types

- Related incident records
- Monitoring alerts
- Windows Event Logs
- Diagnostic command output
- Performance data
- Configuration information
- Vendor advisories
- Screenshots
- Incident trend summaries

### Example Directory

```text
Problem-Management/
└── Records/
    └── PRB-001-Recurring-Authentication-Failures/
        ├── README.md
        └── Evidence/
            ├── 01-Incident-Trend-Summary.md
            ├── 02-Event-Log-Findings.txt
            ├── 03-AD-Replication-Results.txt
            └── 04-Initial-Risk-Assessment.md
```

### Evidence Standards

Each item should identify:

- What was observed
- Which system was involved
- When the evidence was collected
- Which tool or method was used
- What the evidence supports
- Any limitations or uncertainties

Do not fabricate diagnostic results.

---

## 14. Problem Identification Documentation Standards

Problem records should clearly distinguish observations from hypotheses.

### Observed Condition

A fact supported by incident reports, logs, monitoring, or diagnostic evidence.

**Example:**

"Three incident records report domain authentication failures."

### Suspected Cause

A possible explanation that has not yet been confirmed.

**Example:**

"DNS configuration may be contributing to the authentication failures."

### Confirmed Cause

An explanation supported by sufficient technical investigation.

**Example:**

"Diagnostic evidence confirmed that affected clients were configured to use an incorrect DNS server."

### Documentation Rule

Do not label a suspected cause as confirmed merely because it appears plausible.

---

## 15. Example Problem Identification Scenario

### Scenario — Recurring Active Directory Authentication Failures

**Scenario Type:** Reactive Problem Identification  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Technical Category:** Active Directory  
**Potential Problem ID:** PRB-001

### Business Context

Technical Techno Tech employees use domain-joined Windows workstations to access internal resources.

Several simulated incident reports describe authentication failures.

### Related Incident Reports

| Incident | Description |
|---|---|
| INC-001 | Employee cannot authenticate to domain |
| INC-002 | Another employee reports intermittent sign-in failure |
| INC-003 | Domain authentication fails after workstation restart |

### Initial Observation

The reports involve similar authentication symptoms.

### Potential Shared Dependencies

- Domain controllers
- DNS services
- Network connectivity
- Active Directory authentication
- Workstation configuration

### Preliminary Assessment

**Impact:** Medium  
**Likelihood:** Medium  
**Proposed Priority:** P3 — Medium

These values are illustrative and should be reassessed using actual evidence.

### Problem Description

Multiple simulated incidents involve domain authentication failures.

The incidents may share an underlying infrastructure dependency.

The cause has not yet been established.

### Initial Investigation Plan

1. Review incident records.
2. Compare affected workstations.
3. Review DNS configuration.
4. Test domain controller discovery.
5. Examine domain controller health.
6. Review Active Directory replication.
7. Analyze relevant event logs.
8. Determine whether a common cause exists.

### Expected Outcome

A Problem record is created for further analysis if the available evidence supports the need for investigation.

**Scenario Status:** Illustrative problem identification exercise. No actual incidents, diagnostic findings, or confirmed root cause are claimed.

---

## 16. Common Problem Identification Errors

### Error 1 — Treating Every Incident as a Problem

**Incorrect:** Creating a separate Problem record for every routine incident.

**Correct:** Evaluate recurrence, impact, risk, and the need for underlying cause analysis.

### Error 2 — Waiting for a Confirmed Root Cause

**Incorrect:** Refusing to create a Problem record until the cause is known.

**Correct:** Record potential causes requiring investigation.

### Error 3 — Assuming Similar Symptoms Have the Same Cause

**Incorrect:** Concluding that all authentication failures originate from DNS.

**Correct:** Review evidence and shared dependencies before determining relationships.

### Error 4 — Ignoring Proactive Risks

**Incorrect:** Identifying problems only after incidents occur.

**Correct:** Review monitoring trends, capacity risks, and infrastructure weaknesses.

### Error 5 — Creating Duplicate Problems

**Incorrect:** Opening multiple Problem records for the same established investigation.

**Correct:** Search existing records and link new evidence when appropriate.

### Error 6 — Assigning Priority Without Business Context

**Incorrect:** Prioritizing solely based on technical complexity.

**Correct:** Consider business impact, recurrence risk, and affected services.

### Error 7 — Confusing Problem Identification With Root Cause Analysis

**Incorrect:** Attempting to prove the root cause before recording the problem.

**Correct:** Identify and document the problem candidate, then perform structured analysis.

### Error 8 — Missing Supporting Evidence

**Incorrect:** Recording "server keeps failing" without supporting information.

**Correct:** Include incident references, monitoring data, or diagnostic observations.

---

## 17. Problem Identification Quality Checklist

Before completing problem identification, verify:

- [ ] Potential problem identified
- [ ] Identification source documented
- [ ] Reactive or proactive classification selected
- [ ] Initial symptoms recorded
- [ ] Affected service identified
- [ ] Related incidents reviewed
- [ ] Shared dependencies considered
- [ ] Relevant technical evidence collected
- [ ] Existing Problem records checked
- [ ] Business impact assessed
- [ ] Likelihood or recurrence risk assessed
- [ ] Decision to create a Problem record documented
- [ ] Unique Problem ID assigned when applicable
- [ ] Problem description completed
- [ ] Technical category assigned
- [ ] Preliminary priority established
- [ ] Problem owner assigned
- [ ] Related records linked
- [ ] Initial investigation requirements documented
- [ ] Problem Register updated
- [ ] Suspected causes distinguished from confirmed findings

---

## 18. Problem Identification Performance Metrics

Problem identification effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Problems Identified | Measures new Problem records created |
| Reactive Problem Identification Rate | Tracks problems identified from existing incidents |
| Proactive Problem Identification Rate | Tracks problems identified before service disruption |
| Recurring Incident Detection Rate | Evaluates recognition of incident patterns |
| Problem Identification Time | Measures time between qualifying evidence and problem identification |
| Duplicate Problem Rate | Identifies unnecessary duplicate records |
| Problem Record Completeness | Measures required documentation quality |
| Problem Assignment Accuracy | Evaluates initial ownership decisions |
| Related Incident Linkage Rate | Measures traceability between incidents and problems |
| Proactive Risk Detection | Tracks infrastructure risks identified for investigation |

Metrics should be based on actual records or clearly labeled simulated datasets.

---

## 19. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Identifies recurring support issues and reports problem candidates |
| Incident Management | Supplies incident history and technical evidence |
| Service Request Management | May reveal recurring fulfillment failures or process weaknesses |
| Knowledge Management | Provides known errors, workarounds, and previous findings |
| Problem Management | Identifies and investigates actual or potential causes |
| Change Enablement | Tracks changes associated with recurring failures or future remediation |
| Monitoring and Event Management | Provides alerts, trends, and proactive indicators |
| Service Configuration Management | Identifies shared dependencies and affected Configuration Items |
| Information Security Management | Identifies security risks and recurring control failures |
| Continual Improvement | Uses problem trends to improve services and operational practices |

---

## 20. Related Procedures and Documentation

### Problem Management

- [Problem Management Overview](../README.md)
- [Problem Template](../../Templates/Problem-Template.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Logging](../../Incident-Management/Procedures/Incident-Logging.md)
- [Incident Investigation](../../Incident-Management/Procedures/Incident-Investigation.md)
- [Incident Resolution](../../Incident-Management/Procedures/Incident-Resolution.md)
- [Incident Closure](../../Incident-Management/Procedures/Incident-Closure.md)

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Service Request Management](../../Service-Request-Management/)
- [Knowledge Management](../../Knowledge-Management/)
- [Change Enablement](../../Change-Enablement/)
- [Monitoring and Event Management](../../Monitoring-and-Event-Management/)
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

## 21. Procedure Review

This procedure should be reviewed when:

- Problem identification criteria change.
- Monitoring capabilities are expanded.
- Incident trend analysis methods are updated.
- New infrastructure technologies are introduced.
- Problem prioritization standards change.
- Documentation quality issues are identified.
- Organizational responsibilities change.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial problem identification procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee reports, incident histories, organizational roles, problem assessments, and business impact evaluations may be simulated.

Technical investigations, diagnostic commands, infrastructure configurations, monitoring observations, and validation results are documented based on hands-on lab activities where indicated.

This procedure demonstrates ITIL-aligned Problem Management, reactive and proactive problem identification, incident trend analysis, infrastructure risk assessment, and operational documentation rather than employment experience within an actual production organization.
