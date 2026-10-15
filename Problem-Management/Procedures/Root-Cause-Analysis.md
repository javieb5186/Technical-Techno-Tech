# SOP — Root Cause Analysis

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Problem Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-PM-002  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Problem Management

---

## 1. Purpose

This procedure establishes a standardized method for performing Root Cause Analysis (RCA) within Technical Techno Tech.

Root Cause Analysis is a structured investigation used to identify the underlying technical, operational, or procedural conditions contributing to IT incidents and problems.

While Incident Management focuses on restoring service, Root Cause Analysis seeks to understand why a failure occurred and how similar failures can be prevented or their impact reduced.

The procedure supports:

- Identification of underlying technical causes
- Reduction of recurring incidents
- Improved infrastructure reliability
- Evidence-based troubleshooting
- Identification of contributing factors
- Development of effective workarounds
- Evaluation of permanent corrective actions
- Improved technical documentation
- Better operational decision-making
- Continual improvement

**Key Principle:** Root Cause Analysis should identify causes supported by evidence rather than assumptions. The objective is to understand system failures and improve reliability, not to assign blame.

---

## 2. Scope

This procedure applies to problems affecting Technical Techno Tech's internal IT services and supporting infrastructure.

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

Root Cause Analysis may involve:

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

Technologies should only be described as deployed or operational when supported by actual lab evidence.

---

## 3. ITIL 4 Problem Management

### Purpose

The purpose of Problem Management is to reduce the likelihood and impact of incidents by identifying actual and potential causes of incidents and managing workarounds and known errors.

### Important Definitions

**Incident:** An unplanned interruption to a service or a reduction in the quality of a service.

**Problem:** A cause, or potential cause, of one or more incidents.

**Known Error:** A problem that has been analyzed but has not been resolved.

**Workaround:** A solution that reduces or eliminates the impact of an incident or problem for which a full resolution is not yet available.

**Root Cause Analysis:** A structured investigative method used to identify the underlying causes and contributing conditions of a failure.

### Incident Investigation vs. Root Cause Analysis

| Incident Investigation | Root Cause Analysis |
|---|---|
| Focuses on restoring service | Focuses on understanding underlying causes |
| Investigates immediate symptoms | Investigates causal relationships |
| May apply temporary workarounds | Evaluates long-term corrective actions |
| Prioritizes service restoration | Prioritizes reducing recurrence and impact |
| May end without a confirmed cause | Seeks an evidence-supported causal explanation |

A confirmed root cause is not always obtainable. Unresolved uncertainty must be documented rather than replaced with an unsupported conclusion.

---

## 4. Root Cause Analysis Principles

Technical Techno Tech follows several principles during RCA.

### 4.1 Evidence-Based Investigation

Conclusions must be supported by diagnostic evidence, documented observations, or reproducible testing.

### 4.2 Separate Symptoms From Causes

A symptom describes what failed.

A cause explains why the failure occurred.

### 4.3 Consider Multiple Contributing Factors

Complex failures may involve several interacting technical or operational conditions.

### 4.4 Avoid Premature Conclusions

Do not select a root cause before evaluating reasonable alternatives.

### 4.5 Investigate System Conditions

Consider configuration, monitoring, maintenance, documentation, and process weaknesses where relevant.

### 4.6 Preserve Technical Evidence

Collect important evidence before making changes that could alter the system state.

### 4.7 Prioritize Safe Investigation

Use authorized diagnostic methods and avoid unnecessary disruption to functioning services.

### 4.8 Maintain Traceability

Link findings to incident records, monitoring events, Configuration Items, and relevant changes.

### 4.9 Support Continual Improvement

Use confirmed findings to identify actions that reduce future service disruptions.

---

## 5. Roles and Responsibilities

### Problem Manager / Coordinator

Responsible for:

- Coordinating Root Cause Analysis
- Defining investigation scope
- Assigning technical responsibilities
- Reviewing evidence
- Monitoring investigation progress
- Documenting findings
- Coordinating corrective action recommendations

### Systems Administrator

Responsible for:

- Investigating Windows Server failures
- Reviewing Active Directory health
- Analyzing DNS and directory service issues
- Reviewing Event Logs
- Evaluating server configurations
- Providing technical findings

### Network Administrator

Responsible for:

- Investigating network failures
- Analyzing routing and switching
- Reviewing firewall configurations
- Evaluating network performance
- Identifying network dependencies

### Endpoint Support Specialist

Responsible for:

- Investigating workstation failures
- Reviewing application and operating system behavior
- Analyzing endpoint configurations
- Comparing affected and unaffected devices
- Documenting technical findings

### Cloud Administrator

Responsible for:

- Investigating Microsoft 365 and Azure issues
- Reviewing cloud service health
- Analyzing cloud identity configurations
- Evaluating cloud service dependencies
- Providing relevant diagnostic evidence

### Information Security Personnel

Responsible for:

- Supporting analysis of security-related failures
- Reviewing relevant security controls
- Identifying contributing security weaknesses
- Coordinating with security incident response
- Evaluating security implications of corrective actions

### Service Desk Technician

Responsible for:

- Providing incident histories
- Documenting recurring symptoms
- Supplying initial troubleshooting records
- Identifying affected employees and services
- Supporting validation when appropriate

**Lab Note:** These responsibilities represent simulated organizational roles. One learner may perform multiple roles during a controlled lab exercise.

---

## 6. Root Cause Analysis Triggers

Root Cause Analysis may be initiated when:

- Multiple related incidents occur.
- A major incident requires further investigation.
- A critical service fails unexpectedly.
- A recurring workaround is required.
- Monitoring identifies persistent technical errors.
- A significant infrastructure weakness is discovered.
- A previous corrective action fails.
- An unresolved problem presents substantial operational risk.

### Example Triggers

| Trigger | Example |
|---|---|
| Recurring Incidents | Multiple domain authentication failures |
| Major Incident | Organization-wide DNS outage |
| Repeated Service Failure | Windows service repeatedly stops |
| Monitoring Trend | Increasing server disk usage |
| Configuration Issue | Repeated failures following a configuration change |
| Infrastructure Risk | Single point of failure affecting critical services |

Not every incident requires a formal RCA.

The depth of investigation should reflect the business impact, recurrence risk, and technical complexity.

---

## 7. Root Cause Analysis Methods

Technical Techno Tech may use several RCA techniques.

### 7.1 Five Whys Analysis

The Five Whys technique investigates a failure by repeatedly asking why it occurred.

The number of questions is not fixed. Investigation continues until a useful, evidence-supported causal explanation is established or the available evidence is exhausted.

#### Example

**Problem:** Employees cannot authenticate to the domain.

| Question | Hypothetical Finding |
|---|---|
| Why 1 | Workstations cannot locate a domain controller |
| Why 2 | Domain controller DNS records cannot be resolved |
| Why 3 | Workstations are querying an incorrect DNS server |
| Why 4 | Incorrect DNS settings were distributed through DHCP |
| Why 5 | A DHCP configuration change introduced an incorrect DNS option |

**Potential Root Cause:** Incorrect DNS server information in the DHCP configuration.

**Important:** This is an illustrative causal chain. Every step must be verified before the conclusion is accepted.

### 7.2 Fishbone Diagram

A Fishbone Diagram, also called an Ishikawa or cause-and-effect diagram, organizes possible contributing factors into categories.

#### Example Categories

- Configuration
- Infrastructure
- Software
- Network
- Processes
- Human Factors
- Monitoring
- External Dependencies

#### Example

```text id="iowrxe"
Configuration --------\
                       \
Infrastructure ---------\
                         \
Software -----------------> Recurring Authentication Failure
                         /
Network ----------------/
                       /
Processes ------------/
```

The diagram helps organize hypotheses but does not independently prove causation.

### 7.3 Timeline Analysis

Timeline analysis examines the sequence of events surrounding a failure.

#### Example

```text id="uwvrll"
09:00 — Authentication operating normally
09:30 — DHCP configuration modified
09:45 — First authentication failure reported
10:00 — Additional authentication failures
10:15 — Service Desk begins investigation
10:30 — DNS configuration discrepancy identified
```

The timeline may reveal relevant relationships between changes and failures.

A change occurring before a failure does not automatically establish causation.

### 7.4 Fault Tree Analysis

Fault Tree Analysis works backward from an undesirable event to identify combinations of conditions that could produce it.

#### Example

```text id="wtsjcf"
          Domain Authentication Failure
                       |
             +---------+---------+
             |                   |
       Client-Side Issue   Server-Side Issue
             |                   |
        +----+----+         +----+----+
        |         |         |         |
       DNS     Network    DC Down   AD Issue
```

The diagram represents potential causes for investigation.

### 7.5 Comparative Analysis

Compare affected and unaffected systems to identify relevant differences.

Potential comparisons:

- DNS configuration
- Group Policy application
- Network settings
- Operating system versions
- Software updates
- Security group membership
- Server configurations

### 7.6 Change Analysis

Review recent changes that may have contributed to the failure.

Examples:

- Group Policy modifications
- Firewall rule updates
- DHCP configuration changes
- Software installations
- Operating system updates
- Server role modifications

Changes should be evaluated as hypotheses until supporting evidence is available.

---

## 8. Root Cause Analysis Workflow

```text id="yvvuwz"
Problem Record Available
          |
          v
Review Problem and Incident History
          |
          v
Define Investigation Scope
          |
          v
Collect Technical Evidence
          |
          v
Establish Event Timeline
          |
          v
Identify Potential Causes
          |
          v
Select RCA Method
          |
          v
Test Causal Hypotheses
          |
          v
Evidence Supports a Cause?
          |
     +----+----+
     |         |
    Yes        No
     |         |
     v         v
Document    Continue Analysis /
Findings    Record Uncertainty
     |         |
     +----+----+
          |
          v
Identify Contributing Factors
          |
          v
Evaluate Corrective Options
          |
          v
Document RCA Findings
          |
          v
Review and Approve Findings
          |
          v
Track Corrective Actions
```

---

## 9. Root Cause Analysis Procedure

### Step 1 — Review the Problem Record

Open the assigned Problem record.

Review:

- Problem ID
- Summary
- Description
- Affected services
- Technical category
- Priority
- Related incidents
- Existing workarounds
- Monitoring events
- Affected Configuration Items
- Previous investigation findings

**Expected Result:** The investigator understands the problem and its operational context.

### Step 2 — Define the Investigation Scope

Identify what the RCA will investigate.

Determine:

1. What failure is being analyzed?
2. Which services are affected?
3. Which systems are involved?
4. Which symptoms are confirmed?
5. What is the business impact?
6. What information remains unknown?
7. What evidence is required?

#### Example

**Problem:** Recurring Active Directory authentication failures.

**Scope:** Investigate domain controller availability, DNS resolution, client network configuration, and related infrastructure dependencies.

**Expected Result:** The investigation has a defined technical scope.

### Step 3 — Review Related Incident History

Examine incidents associated with the problem.

Review:

- Incident timelines
- Reported symptoms
- Diagnostic results
- Corrective actions
- Workarounds
- Resolution outcomes
- Recurrence patterns

#### Example

| Incident | Symptom | Restoration Method |
|---|---|---|
| INC-001 | Authentication failure | Temporary connectivity restoration |
| INC-002 | Authentication failure | DNS configuration corrected |
| INC-003 | Authentication failure | Workstation configuration corrected |

These entries are illustrative.

**Expected Result:** Historical patterns and prior findings are documented.

### Step 4 — Establish the Failure Timeline

Construct a chronological sequence of relevant events.

Include:

- Last known working state
- First observed failure
- Monitoring alerts
- Configuration changes
- Incident reports
- Restoration actions
- Recurrence events

#### Example

```text id="xehkpd"
08:00 — Service operating normally
09:00 — Configuration change performed
09:20 — First failure observed
09:35 — Additional users affected
10:00 — Temporary restoration completed
11:30 — Similar failure recurs
```

**Expected Result:** A documented timeline supports further investigation.

### Step 5 — Identify Affected Configuration Items

Determine which infrastructure components may contribute to the problem.

Examples:

- Domain controllers
- DNS servers
- DHCP servers
- Workstations
- Routers
- Switches
- Firewalls
- Virtual machines
- Cloud services

#### Example

```text id="9eowzi"
CLIENT01
   |
   v
Network Configuration
   |
   v
DNS Resolution
   |
   v
Domain Controller Discovery
   |
   v
Active Directory Authentication
```

Review relevant Configuration Item records and dependency documentation.

**Expected Result:** Potential infrastructure dependencies are identified.

### Step 6 — Collect Technical Evidence

Collect relevant diagnostic information.

Evidence may include:

- Windows Event Logs
- PowerShell output
- Service status
- DNS records
- Network configuration
- Performance data
- Monitoring alerts
- Configuration history
- Application logs
- Vendor documentation

Record the source, collection time, and interpretation of each item.

**Expected Result:** Relevant evidence is available for analysis.

### Step 7 — Identify Potential Causes

Develop a list of reasonable hypotheses.

#### Example

**Problem:** Recurring domain authentication failures.

Potential causes:

1. Incorrect DNS configuration
2. Domain controller availability issues
3. Active Directory replication failures
4. Network connectivity problems
5. Authentication policy configuration
6. Workstation domain trust issues

These are hypotheses, not confirmed root causes.

**Expected Result:** Potential causes are documented for testing.

### Step 8 — Select an RCA Method

Choose an analysis method appropriate to the problem.

| Method | Recommended Use |
|---|---|
| Five Whys | Investigating a causal chain |
| Fishbone Diagram | Organizing multiple possible causes |
| Timeline Analysis | Examining event sequences |
| Fault Tree Analysis | Investigating complex failure conditions |
| Comparative Analysis | Comparing affected and unaffected systems |
| Change Analysis | Evaluating potential change-related failures |

Multiple methods may be combined.

**Expected Result:** An appropriate analysis approach is selected.

### Step 9 — Test Potential Causes

Perform controlled diagnostic tests.

For each hypothesis:

1. Identify the proposed cause.
2. Determine what evidence would support it.
3. Determine what evidence would contradict it.
4. Select appropriate diagnostic tools.
5. Perform authorized testing.
6. Record the results.
7. Update the hypothesis status.

#### Example

**Hypothesis:** Incorrect DNS configuration prevents domain controller discovery.

**Test:**

```powershell id="nbrrzu"
Get-DnsClientServerAddress -AddressFamily IPv4
```

**Additional Test:**

```powershell id="vaykzf"
nslookup dc01.homelab.local
```

**Additional Test:**

```powershell id="btmd4c"
nltest /dsgetdc:homelab.local
```

Compare the results with the documented network configuration.

**Expected Result:** Potential causes are evaluated using observable evidence.

### Step 10 — Review Contradictory Evidence

Do not ignore evidence that conflicts with the leading hypothesis.

#### Example

**Hypothesis:** The domain controller is unavailable.

**Evidence:**

- Domain controller responds to authorized management connections.
- Other workstations authenticate successfully.
- Only one subnet is affected.

These findings may suggest that the issue is more localized than originally assumed.

**Expected Result:** Unsupported explanations are challenged.

### Step 11 — Identify Contributing Factors

Determine whether additional conditions contributed to the failure.

Potential factors include:

- Inadequate monitoring
- Missing configuration validation
- Incomplete documentation
- Insufficient testing
- Uncontrolled configuration changes
- Single points of failure
- Resource limitations
- Missing recovery procedures

#### Example

**Primary Technical Cause:** Incorrect DNS settings distributed to clients.

**Potential Contributing Factors:**

- Configuration change was not adequately validated.
- Monitoring did not identify incorrect DNS settings.
- A recovery procedure was unavailable.

Each contributing factor must be supported by evidence or explicitly identified as a hypothesis.

**Expected Result:** Relevant contributing conditions are documented.

### Step 12 — Determine Root Cause Status

Classify the investigation outcome.

| Status | Description |
|---|---|
| Confirmed | Sufficient evidence supports the causal explanation |
| Probable | Evidence strongly suggests a cause, but confirmation is incomplete |
| Inconclusive | Available evidence does not establish a reliable cause |
| Multiple Causes | More than one supported cause contributed to the failure |
| Investigation Ongoing | Additional analysis is required |

Do not classify a cause as confirmed solely because a corrective action appears successful.

**Expected Result:** The certainty of the RCA findings is accurately represented.

### Step 13 — Identify Workarounds

Determine whether an approved workaround can reduce service impact while corrective actions are evaluated.

Examples:

- Using an alternative authorized service
- Restoring a previous approved configuration
- Redirecting users to an available system
- Applying an approved temporary operational procedure

Document:

- Workaround description
- Conditions for use
- Required authorization
- Known limitations
- Validation method
- Associated risks

**Expected Result:** Available mitigation options are documented.

### Step 14 — Evaluate Corrective Action Options

Identify actions that could eliminate or reduce the identified causes.

Examples:

- Correcting configuration errors
- Updating software
- Replacing faulty hardware
- Improving monitoring
- Modifying infrastructure design
- Implementing redundancy
- Updating operational procedures
- Improving change validation

#### Evaluation Criteria

| Criterion | Consideration |
|---|---|
| Effectiveness | Does the action address the supported cause? |
| Risk | Could it disrupt other services? |
| Cost | What resources are required? |
| Complexity | How difficult is implementation? |
| Security | Does it preserve required controls? |
| Reversibility | Can the change be rolled back? |
| Validation | How will success be measured? |

**Expected Result:** Corrective action options are evaluated.

### Step 15 — Determine Change Enablement Requirements

Some corrective actions require controlled infrastructure changes.

Examples:

- Modifying DHCP settings
- Updating firewall rules
- Changing Group Policy
- Updating domain controller configuration
- Deploying patches
- Modifying routing settings

Before implementation:

1. Review the proposed action.
2. Identify affected services.
3. Assess technical risk.
4. Determine the applicable change type.
5. Obtain required authorization.
6. Document implementation requirements.
7. Define validation and rollback procedures.

**Expected Result:** Applicable corrective changes are directed through Change Enablement.

### Step 16 — Document RCA Findings

Update the Problem record with:

- Investigation scope
- Related incidents
- Technical evidence
- Event timeline
- RCA method
- Hypotheses tested
- Confirmed findings
- Root cause status
- Contributing factors
- Workarounds
- Corrective action recommendations
- Remaining uncertainties

**Expected Result:** The RCA is documented and traceable.

### Step 17 — Review Findings

Submit the RCA findings for an appropriate technical review.

Reviewers should evaluate:

- Evidence quality
- Logical consistency
- Technical accuracy
- Alternative explanations
- Root cause certainty
- Proposed corrective actions
- Security implications
- Documentation completeness

### Lab Consideration

If the investigation is self-reviewed, record:

**Review Method:** Self-Review / Lab Validation

Do not represent the review as independent organizational approval.

**Expected Result:** Findings receive an accurately documented review.

### Step 18 — Track Corrective Actions

Record approved or proposed corrective actions in the appropriate operational records.

Potential records include:

- Change records
- Problem records
- Knowledge articles
- Configuration Item updates
- Continual improvement records

Assign ownership and identify validation requirements.

**Expected Result:** RCA findings lead to traceable follow-up activities.

### Step 19 — Monitor for Recurrence

After corrective actions are implemented, evaluate whether the problem recurs.

Monitoring may include:

- Related incident frequency
- Windows Event Logs
- Service availability
- Network performance
- Authentication success
- Application stability
- Relevant monitoring alerts

An observation period should be appropriate to the failure pattern.

**Expected Result:** The effectiveness of corrective actions can be evaluated.

---

## 10. Technical RCA — Active Directory

Active Directory problems may involve:

- Authentication failures
- DNS configuration
- Replication failures
- Group Policy processing
- Domain controller availability
- Account configuration
- Trust relationships

### Diagnostic Tools

- Active Directory Administrative Center
- Active Directory Users and Computers
- Event Viewer
- PowerShell
- `dcdiag`
- `repadmin`
- `nltest`

### Example Commands

**Domain Controller Discovery**

```powershell id="pqopzy"
nltest /dsgetdc:homelab.local
```

**Domain Controller Diagnostics**

```powershell id="xmb54h"
dcdiag /q
```

**Replication Summary**

```powershell id="5spbdq"
repadmin /replsummary
```

**Replication Details**

```powershell id="itjqah"
repadmin /showrepl
```

**DNS Resolution**

```powershell id="wudkjy"
nslookup dc01.homelab.local
```

### Investigation Considerations

- Are failures isolated to one domain controller?
- Are multiple workstations affected?
- Are DNS records resolving correctly?
- Are replication errors present?
- Did relevant configurations recently change?
- Is the failure consistent or intermittent?

**Expected Documentation:** Record diagnostic output and explain how each finding supports or contradicts a hypothesis.

---

## 11. Technical RCA — Windows Server

Windows Server problems may involve:

- Repeated service failures
- Performance degradation
- Storage exhaustion
- Application crashes
- Update failures
- Backup failures
- Resource limitations

### Diagnostic Tools

- Event Viewer
- Performance Monitor
- Windows Admin Center
- Server Manager
- PowerShell

### Example Commands

**Service Status**

```powershell id="xkhh1s"
Get-Service
```

**Specific Service**

```powershell id="lnf1be"
Get-Service -Name DNS
```

**Recent System Errors**

```powershell id="9xbr7s"
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    Level = 2
    StartTime = (Get-Date).AddDays(-7)
} -MaxEvents 50
```

**Storage Information**

```powershell id="ypbvyn"
Get-Volume
```

### Investigation Considerations

- Does the failure occur at predictable intervals?
- Are resource limitations involved?
- Do Event Logs identify recurring errors?
- Did the issue begin after an update?
- Are dependent services affected?
- Does the problem recur after a service restart?

---

## 12. Technical RCA — Networking

Network problems may involve:

- Incorrect IP configuration
- DNS failures
- DHCP misconfiguration
- Routing errors
- VLAN configuration
- Firewall restrictions
- Network congestion
- Packet loss

### Diagnostic Tools

| Tool | Purpose |
|---|---|
| `ipconfig` | Review IP configuration |
| `ping` | Test IP connectivity |
| `tracert` | Examine network paths |
| `nslookup` | Test DNS resolution |
| `arp` | Review local ARP information |
| `route print` | Review local routing information |
| OPNsense | Review firewall and network settings |
| VyOS | Review routing and interface configurations |
| Packet Tracer | Investigate simulated network behavior |

### Example Commands

```powershell id="c2x3nz"
ipconfig /all
```

```powershell id="vv98yl"
route print
```

```powershell id="qnphb5"
nslookup dc01.homelab.local
```

```powershell id="gnon5c"
tracert 10.20.10.10
```

### Investigation Considerations

- Are failures isolated to one subnet?
- Are multiple services affected?
- Does the problem involve name resolution?
- Are routing paths correct?
- Are firewall rules relevant?
- Did a network configuration change occur?
- Is packet loss consistent or intermittent?

A failed ping or traceroute does not necessarily prove a device is unavailable because network security controls may restrict diagnostic traffic.

---

## 13. Technical RCA — Microsoft 365 and Entra ID

Cloud-related problems may involve:

- Repeated authentication failures
- Licensing issues
- Device registration failures
- Conditional Access configuration
- Microsoft 365 application disruptions
- Cloud service availability
- Administrative permission problems

### Investigation Sources

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Microsoft service health information
- Available sign-in logs
- Relevant audit records

### Investigation Considerations

1. Are multiple users affected?
2. Is the issue limited to one application?
3. Are licensing requirements satisfied?
4. Are relevant cloud services available?
5. Are access policies contributing to the failure?
6. Did a configuration change occur?
7. Are device compliance requirements involved?

Diagnostic capabilities depend on licensing, assigned administrative roles, and configured services.

---

## 14. Technical RCA — Virtualization

Virtualization problems may involve:

- Virtual machine startup failures
- Resource exhaustion
- Virtual network configuration
- Storage performance
- Guest operating system failures
- Hypervisor configuration

### Investigation Considerations

- Are multiple virtual machines affected?
- Is the host experiencing resource pressure?
- Are virtual network adapters configured correctly?
- Is storage capacity sufficient?
- Did the problem begin after a VM configuration change?
- Is the issue isolated to one guest operating system?

### Example

**Problem:** Multiple virtual machines experience intermittent network connectivity.

Potential investigation:

1. Compare affected virtual machines.
2. Review virtual network configurations.
3. Verify guest network settings.
4. Examine host networking.
5. Review recent virtualization changes.
6. Identify shared dependencies.

Do not assume the hypervisor is responsible merely because multiple virtual machines are affected.

---

## 15. Root Cause Analysis Evidence Standards

Each RCA should preserve sufficient evidence to support its findings.

### Evidence Types

- Incident histories
- Event Logs
- Diagnostic command output
- Configuration comparisons
- Monitoring data
- Screenshots
- Performance reports
- Change histories
- Technical diagrams
- Validation results

### Example Directory

```text id="fhc0ve"
Problem-Management/
└── Records/
    └── PRB-001-Recurring-Authentication-Failures/
        ├── README.md
        └── Evidence/
            ├── 01-Incident-Timeline.md
            ├── 02-Event-Log-Findings.txt
            ├── 03-DNS-Configuration.txt
            ├── 04-RCA-Five-Whys.md
            ├── 05-Root-Cause-Findings.md
            └── 06-Corrective-Action-Validation.md
```

### Evidence Requirements

Each item should identify:

- Evidence source
- System involved
- Collection date and time
- Diagnostic method
- Observed result
- Interpretation
- Related hypothesis

### Security Requirements

Before publishing:

- Remove credentials.
- Redact authentication tokens.
- Remove unnecessary personal information.
- Protect sensitive configuration details.
- Avoid exposing private keys.
- Verify screenshots contain no confidential information.

---

## 16. RCA Documentation Template

Use the following structure within a Problem record.

```text id="wccwxd"
ROOT CAUSE ANALYSIS RECORD

Problem ID:
Problem Summary:
Affected Service:
Affected Systems:
Investigator:
Investigation Date:
RCA Status:

1. Problem Statement

2. Business Impact

3. Related Incidents

4. Investigation Scope

5. Event Timeline

6. Technical Evidence

7. Potential Causes

8. RCA Method Used

9. Hypotheses Tested

10. Confirmed Findings

11. Root Cause Status
    Confirmed / Probable / Inconclusive /
    Multiple Causes / Investigation Ongoing

12. Root Cause Explanation

13. Contributing Factors

14. Existing Workarounds

15. Corrective Action Options

16. Recommended Corrective Action

17. Required Change Authorization

18. Validation Requirements

19. Remaining Risks

20. Related Records

21. Review Method and Outcome

22. Lessons Learned
```

---

## 17. Example Root Cause Analysis Scenario

### Scenario — Recurring Domain Authentication Failures

**Problem ID:** PRB-001  
**Problem Summary:** Recurring Active Directory Authentication Failures  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Technical Category:** Active Directory / DNS  
**Environment:** homelab.local

### Business Context

Employees rely on domain authentication to access internal systems.

Several simulated incidents involve domain-joined workstations failing to locate a domain controller.

### Problem Statement

Multiple workstations experience recurring authentication failures.

The underlying cause has not yet been confirmed.

### Hypothetical Evidence

For this example, assume diagnostic testing establishes that:

1. Affected workstations have incorrect DNS server addresses.
2. Domain controller DNS queries fail using the configured DNS servers.
3. The incorrect settings originate from a DHCP configuration.
4. The DHCP configuration was modified before the failures began.
5. Correcting the DNS settings restores domain controller discovery.

These findings are hypothetical and must not be represented as completed lab results.

### Five Whys Analysis

| Question | Hypothetical Answer |
|---|---|
| Why did authentication fail? | Workstations could not discover a domain controller |
| Why could they not discover a domain controller? | Required DNS queries failed |
| Why did DNS queries fail? | Workstations were using incorrect DNS servers |
| Why were incorrect DNS servers configured? | DHCP distributed incorrect DNS settings |
| Why did DHCP distribute incorrect settings? | A configuration change introduced incorrect DNS options |

### Hypothetical Root Cause

Incorrect DNS server settings were introduced into the DHCP configuration and distributed to affected workstations.

### Potential Contributing Factors

- Inadequate post-change validation
- Missing DNS configuration checks
- Insufficient monitoring of client DNS settings

These factors would require separate supporting evidence before being confirmed.

### Proposed Corrective Actions

1. Correct the DHCP DNS server options.
2. Validate DNS configuration on affected clients.
3. Verify domain controller discovery.
4. Review change validation procedures.
5. Consider additional monitoring or configuration checks.

### Proposed Validation

**Client DNS Configuration**

```powershell id="epozqk"
Get-DnsClientServerAddress -AddressFamily IPv4
```

**DNS Resolution**

```powershell id="zggwjq"
nslookup dc01.homelab.local
```

**Domain Controller Discovery**

```powershell id="xgdifj"
nltest /dsgetdc:homelab.local
```

**Domain Authentication**

Confirm that an authorized test account can authenticate successfully.

### Follow-Up

- Record corrective changes.
- Update relevant configuration documentation.
- Consider creating a Knowledge Base article.
- Monitor for recurrence.
- Review whether the Problem record can be resolved.

**Scenario Status:** Illustrative RCA example. No diagnostic commands, corrective actions, or root cause confirmation are claimed as completed.

---

## 18. Root Cause Analysis vs. Corrective Action

Root Cause Analysis identifies why a problem occurred.

Corrective action addresses the identified cause or contributing conditions.

### Example

**Problem:** DNS service repeatedly stops.

**RCA Finding:** A specific configuration defect causes the service to fail.

**Corrective Action:** Apply an authorized configuration correction.

**Validation:** Confirm the service remains operational and the failure does not recur during an appropriate observation period.

### Important Distinction

A successful service restart does not necessarily eliminate the underlying cause.

A corrective action should address the supported causal explanation rather than only the immediate symptom.

---

## 19. RCA and Known Error Management

A problem may be documented as a known error after analysis when it remains unresolved.

### Example

**Problem:** Application crashes under a specific configuration.

**Analysis:** Investigation identifies a reproducible software defect.

**Workaround:** Use an approved alternative configuration.

**Permanent Resolution:** Awaiting vendor correction.

### Known Error Documentation

Record:

- Problem ID
- Known error description
- Affected services
- Confirmed or sufficiently analyzed conditions
- Available workaround
- Known limitations
- Corrective action status
- Related knowledge articles

A known error does not necessarily require an immediately available permanent fix.

---

## 20. RCA and Change Enablement

Permanent corrective actions may require controlled changes.

### Examples

- Updating DHCP configuration
- Modifying Group Policy
- Changing firewall rules
- Updating Windows Server
- Reconfiguring network infrastructure
- Implementing redundancy
- Deploying application fixes

### Change Coordination

1. Document the supported root cause.
2. Identify corrective options.
3. Assess implementation risks.
4. Determine applicable change requirements.
5. Obtain required authorization.
6. Implement the approved change.
7. Validate the result.
8. Monitor for recurrence.

### Example Record Relationship

```text id="nac8he"
Problem: PRB-001
Related Change: CHG-001
Related Knowledge Article: KB-001
```

These identifiers are illustrative.

---

## 21. Common Root Cause Analysis Errors

### Error 1 — Confusing Symptoms With Causes

**Incorrect:** Identifying "authentication failure" as the root cause.

**Correct:** Investigate the underlying condition responsible for the authentication failure.

### Error 2 — Assuming the First Hypothesis Is Correct

**Incorrect:** Concluding that DNS is responsible before reviewing diagnostic evidence.

**Correct:** Evaluate reasonable alternative explanations.

### Error 3 — Ignoring Contributing Factors

**Incorrect:** Investigating only the immediate technical defect when additional conditions contributed.

**Correct:** Review relevant configuration, monitoring, maintenance, and process factors.

### Error 4 — Treating Correlation as Causation

**Incorrect:** Assuming an update caused a failure solely because it occurred first.

**Correct:** Establish a causal relationship using technical evidence.

### Error 5 — Performing Uncontrolled Testing

**Incorrect:** Modifying multiple critical settings without authorization or documentation.

**Correct:** Use controlled diagnostic methods and applicable change procedures.

### Error 6 — Declaring a Cause Confirmed Without Evidence

**Incorrect:** Recording a suspected cause as verified.

**Correct:** Document the level of certainty and remaining uncertainty.

### Error 7 — Failing to Validate Corrective Actions

**Incorrect:** Assuming a problem is eliminated immediately after applying a fix.

**Correct:** Verify functionality and monitor for recurrence when appropriate.

### Error 8 — Assigning Individual Blame

**Incorrect:** Ending an investigation with "technician error" without examining the system conditions that allowed the failure.

**Correct:** Identify actionable technical and procedural contributing factors.

---

## 22. Root Cause Analysis Quality Checklist

Before completing an RCA, verify:

- [ ] Problem record reviewed
- [ ] Investigation scope defined
- [ ] Related incidents examined
- [ ] Failure timeline documented
- [ ] Affected services identified
- [ ] Relevant Configuration Items identified
- [ ] Technical evidence collected
- [ ] Potential causes documented
- [ ] RCA method selected
- [ ] Hypotheses tested
- [ ] Contradictory evidence reviewed
- [ ] Findings supported by evidence
- [ ] Root cause certainty documented
- [ ] Contributing factors considered
- [ ] Workarounds evaluated
- [ ] Corrective action options identified
- [ ] Implementation risks assessed
- [ ] Change Enablement requirements considered
- [ ] RCA findings documented
- [ ] Review method recorded
- [ ] Related records linked
- [ ] Corrective actions tracked
- [ ] Validation requirements defined
- [ ] Recurrence monitoring considered

---

## 23. Root Cause Analysis Performance Metrics

RCA effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| RCA Completion Rate | Tracks investigations completed |
| Average RCA Duration | Measures time required to complete analysis |
| Confirmed Root Cause Rate | Measures investigations producing supported causal findings |
| Inconclusive RCA Rate | Tracks investigations without sufficient evidence |
| Repeat Incident Rate | Evaluates recurring failures |
| Corrective Action Implementation Rate | Tracks recommended actions implemented |
| Corrective Action Effectiveness | Evaluates whether actions reduce recurrence |
| Known Error Documentation Rate | Tracks analyzed unresolved problems |
| Problem Reopen Rate | Identifies ineffective or incomplete problem resolution |
| RCA Documentation Completeness | Measures quality of investigation records |

Metrics should be based on actual records or clearly labeled simulated datasets.

---

## 24. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Supplies incident histories and recurring support observations |
| Incident Management | Restores services and provides investigation evidence |
| Service Request Management | May reveal recurring fulfillment or process failures |
| Knowledge Management | Stores known errors, workarounds, and reusable findings |
| Problem Management | Coordinates RCA and corrective action recommendations |
| Change Enablement | Controls applicable permanent corrective changes |
| Monitoring and Event Management | Supplies technical alerts, trends, and validation evidence |
| Service Configuration Management | Identifies affected infrastructure and dependencies |
| Information Security Management | Supports analysis of security-related weaknesses |
| Continual Improvement | Uses RCA findings to improve services and processes |

---

## 25. Related Procedures and Documentation

### Problem Management

- [Problem Management Overview](../README.md)
- [Problem Identification](Problem-Identification.md)
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

## 26. Procedure Review

This procedure should be reviewed when:

- RCA methodologies change.
- New infrastructure technologies are introduced.
- Problem Management responsibilities change.
- Diagnostic tools are updated.
- Corrective action procedures change.
- Documentation quality issues are identified.
- Security requirements change.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Root Cause Analysis procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee reports, incident histories, organizational roles, business impact assessments, and RCA scenarios may be simulated.

Technical investigations, diagnostic commands, infrastructure configurations, root cause findings, corrective actions, and validation results are documented based on hands-on lab activities where indicated.

Hypothetical findings must not be represented as confirmed technical evidence.

This procedure demonstrates ITIL-aligned Problem Management, Root Cause Analysis, technical troubleshooting, evidence-based investigation, corrective action planning, and continual improvement practices rather than employment experience within an actual production organization.
