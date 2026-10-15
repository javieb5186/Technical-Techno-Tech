# SOP — Incident Investigation and Diagnosis

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Incident Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-IM-002  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practices:** Incident Management, Service Desk, Problem Management

---

## 1. Purpose

This procedure establishes a standardized method for investigating and diagnosing IT incidents within Technical Techno Tech.

Incident investigation focuses on understanding the reported symptoms, identifying affected services, evaluating potential causes, and determining appropriate actions to restore normal service operation.

The procedure supports:

- Consistent technical troubleshooting
- Accurate incident diagnosis
- Efficient service restoration
- Evidence-based decision-making
- Reduced unnecessary troubleshooting
- Appropriate technical escalation
- Identification of recurring incidents
- Accurate technical documentation
- Improved knowledge sharing
- Continual improvement

**Key Principle:** Investigate incidents systematically, validate assumptions with evidence, and prioritize restoring service over identifying a permanent root cause when immediate restoration is necessary.

---

## 2. Scope

This procedure applies to incidents affecting Technical Techno Tech's internal IT services.

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

Incident investigations may involve:

- Windows 11 workstations
- Windows Server
- Active Directory Domain Services
- Group Policy
- DNS and DHCP
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V virtual machines
- Network routers and switches
- OPNsense
- VyOS

Only technologies actually deployed or configured during a lab exercise should be represented as operational.

---

## 3. ITIL 4 Incident Management

### Definition

An **incident** is an unplanned interruption to a service or a reduction in the quality of a service.

### Purpose

The purpose of Incident Management is to minimize the negative impact of incidents by restoring normal service operation as quickly as possible.

### Investigation Objectives

Incident investigation should answer:

1. What service is affected?
2. What symptoms are occurring?
3. Who or what is affected?
4. When did the issue begin?
5. What changed before the issue occurred?
6. What evidence is available?
7. What potential causes should be investigated?
8. What action can safely restore service?
9. Is escalation necessary?
10. How will restoration be verified?

### Incident Investigation vs. Problem Management

| Incident Investigation | Problem Management |
|---|---|
| Focuses on restoring service | Focuses on actual or potential underlying causes |
| Investigates current symptoms | Investigates causes and recurring patterns |
| May use temporary workarounds | Develops workarounds and permanent resolution options |
| Prioritizes service restoration | Prioritizes reducing the likelihood and impact of incidents |
| Does not always require root cause confirmation | Uses root cause analysis when appropriate |

An incident may be resolved before its underlying cause is fully understood.

---

## 4. Roles and Responsibilities

### Service Desk Technician

Responsible for:

- Reviewing incident information
- Confirming reported symptoms
- Performing initial troubleshooting
- Collecting diagnostic evidence
- Searching existing knowledge articles
- Documenting findings
- Escalating when necessary
- Communicating with affected employees

### Technical Support Specialist

Responsible for:

- Performing advanced troubleshooting
- Investigating operating system and application issues
- Reviewing diagnostic information
- Identifying potential causes
- Applying authorized corrective actions
- Documenting technical findings

### Systems Administrator

Responsible for:

- Investigating Windows Server incidents
- Troubleshooting Active Directory
- Diagnosing DNS and infrastructure services
- Reviewing server health
- Performing authorized administrative actions
- Supporting infrastructure recovery

### Network Administrator

Responsible for:

- Investigating network connectivity issues
- Reviewing routing and switching
- Diagnosing network segmentation
- Evaluating firewall configurations
- Reviewing network performance
- Restoring network services

### Cloud Administrator

Responsible for:

- Investigating Microsoft 365 and Azure issues
- Reviewing cloud identity and service health
- Troubleshooting cloud resources
- Evaluating cloud configuration
- Supporting cloud service restoration

### Incident Coordinator

Responsible for:

- Monitoring incident progress
- Coordinating technical resources
- Supporting escalation
- Maintaining incident ownership
- Coordinating communication for significant incidents

**Lab Note:** These responsibilities represent simulated organizational roles. One learner may perform multiple roles during a controlled lab exercise.

---

## 5. Investigation Principles

Technical Techno Tech follows several principles during incident investigation.

### 5.1 Verify Before Assuming

Do not treat reported symptoms as confirmed root causes.

**Example:**

An employee reports that the internet is unavailable.

Possible causes include:

- Incorrect IP configuration
- DNS resolution failure
- Default gateway failure
- Firewall restrictions
- Network infrastructure outage

The cause must be investigated rather than assumed.

### 5.2 Start With the Reported Symptoms

Identify what is actually failing before changing configurations.

### 5.3 Investigate From Simple to Complex

Begin with safe, low-risk diagnostic checks before advanced troubleshooting.

### 5.4 Change One Variable at a Time

When practical, isolate individual potential causes to understand the effect of each diagnostic or corrective action.

### 5.5 Preserve Evidence

Record important diagnostic information before making changes that could remove or alter it.

### 5.6 Follow Administrative Boundaries

Do not perform actions requiring permissions or authorization beyond the technician's assigned responsibilities.

### 5.7 Prioritize Service Restoration

A safe workaround may restore service while further investigation continues through Problem Management.

### 5.8 Maintain Communication

Keep the requester and relevant stakeholders informed according to the incident's impact and priority.

---

## 6. Incident Investigation Lifecycle

```text
Incident Assigned
        |
        v
Review Incident Record
        |
        v
Confirm Symptoms and Scope
        |
        v
Review Existing Knowledge
        |
        v
Collect Diagnostic Evidence
        |
        v
Develop Potential Causes
        |
        v
Perform Controlled Testing
        |
        v
Identify Restoration Options
        |
        v
Authorization / Escalation
        |
        v
Implement Approved Action
        |
        v
Validate Service Restoration
        |
        v
Document Findings
        |
        v
Resolve or Escalate Incident
```

Investigation activities may occur concurrently during significant incidents.

Critical incidents should not be delayed by unnecessary diagnostic steps.

---

## 7. Incident Investigation Procedure

### Step 1 — Review the Incident Record

Open the assigned incident and review all available information.

Verify:

- Incident ID
- Summary
- Description
- Affected service
- Technical category
- Priority
- Business impact
- Requester
- Assigned technician
- Existing troubleshooting history
- Related incidents
- Available evidence

**Expected Result:** The technician understands the incident and its current status.

### Step 2 — Confirm the Symptoms

Verify the reported behavior when it is safe and practical to do so.

Determine:

- What action fails?
- What result was expected?
- What result actually occurred?
- Is an error message displayed?
- Is the failure consistent or intermittent?
- Can the issue be reproduced safely?

#### Example

**Reported Issue:** Employee cannot access a shared folder.

**Expected Behavior:** The employee can open the authorized folder.

**Actual Behavior:** Windows displays an access-denied message.

**Expected Result:** The symptoms are clearly understood and documented.

### Step 3 — Determine the Scope

Identify the extent of the incident.

#### Scope Questions

1. Is one employee affected?
2. Are multiple employees affected?
3. Is one workstation affected?
4. Is an entire department affected?
5. Is the issue limited to one application?
6. Are multiple services affected?
7. Is the issue isolated to one network segment?

#### Example

If one employee cannot access a shared folder, investigate:

- User permissions
- Group membership
- Authentication
- Workstation configuration

If all employees cannot access the same folder, investigate:

- File server availability
- Network connectivity
- Shared folder configuration
- Server-side permissions

**Expected Result:** The investigation scope is established.

### Step 4 — Establish the Timeline

Determine when the incident began and whether relevant changes occurred.

Record:

- Last known working time
- First observed failure
- Time reported
- Recent configuration changes
- Recent software installations
- Recent updates
- Related monitoring alerts

#### Example

```text
09:00 — Employee successfully accessed the application.
10:15 — Application update completed.
10:30 — Employee reported application failure.
10:45 — Service Desk began investigation.
```

A change occurring before an incident does not automatically establish causation.

**Expected Result:** A preliminary incident timeline is documented.

### Step 5 — Review Existing Knowledge

Search available documentation for relevant information.

Potential sources include:

- Internal Knowledge Base
- Previous incident records
- Known errors
- Approved troubleshooting procedures
- Infrastructure documentation
- Vendor documentation

Determine whether:

- The issue has occurred before.
- An approved workaround exists.
- A known error has been documented.
- A standard troubleshooting procedure applies.

**Expected Result:** Existing knowledge is considered before repeating unnecessary investigation.

### Step 6 — Identify Affected Configuration Items

Determine which infrastructure components may be involved.

Examples:

- Domain controllers
- Workstations
- DNS servers
- Network switches
- Routers
- Firewalls
- Virtual machines
- Cloud services

#### Example

**Incident:** CLIENT01 cannot authenticate to the domain.

Potential dependencies:

```text
CLIENT01
   |
   v
Network Connectivity
   |
   v
DNS Resolution
   |
   v
Domain Controller
   |
   v
Active Directory Authentication
```

Review relevant infrastructure documentation and Configuration Item records.

**Expected Result:** Relevant technical dependencies are identified.

### Step 7 — Collect Diagnostic Evidence

Collect evidence appropriate to the affected technology.

Evidence may include:

- Error messages
- Screenshots
- Event Logs
- PowerShell output
- Service status
- Network diagnostic results
- Application logs
- Monitoring alerts
- Configuration information

Record:

- Command or tool used
- Target system
- Date and time
- Observed result
- Interpretation
- Evidence reference

Do not collect or publish authentication secrets or unnecessary personal information.

**Expected Result:** Relevant diagnostic evidence is preserved.

### Step 8 — Develop Potential Causes

Use the available evidence to identify reasonable explanations.

#### Example

**Incident:** Workstation cannot authenticate to the domain.

Potential causes:

1. Incorrect DNS configuration
2. Domain controller unavailable
3. Network connectivity failure
4. Account disabled or locked
5. Workstation trust relationship issue

These are hypotheses, not confirmed findings.

**Expected Result:** A focused list of potential causes is established.

### Step 9 — Perform Controlled Diagnostic Testing

Test potential causes using safe, appropriate diagnostic methods.

For each test:

1. Identify the hypothesis.
2. Select the diagnostic tool.
3. Perform the test.
4. Record the result.
5. Determine whether the evidence supports or contradicts the hypothesis.
6. Select the next diagnostic step.

#### Example

**Hypothesis:** DNS configuration is preventing domain controller discovery.

**Test:**

```powershell
nslookup dc01.homelab.local
```

**Possible Finding:** The workstation cannot resolve the domain controller's hostname.

**Next Action:** Review DNS client configuration and DNS server availability.

A failed DNS lookup supports further DNS investigation but does not independently prove the underlying cause.

**Expected Result:** Potential causes are evaluated using observable evidence.

### Step 10 — Determine Restoration Options

Based on the investigation, identify possible ways to restore service.

Options may include:

- Correcting a configuration
- Restarting a failed service
- Restoring connectivity
- Applying an approved workaround
- Reverting an authorized change
- Restoring a system from backup
- Escalating to specialized support

Consider:

- Business impact
- Security implications
- Technical risk
- Required permissions
- Service dependencies
- Reversibility
- Required approvals

**Expected Result:** An appropriate restoration approach is identified.

### Step 11 — Confirm Authorization

Before implementing a corrective action, determine whether the action is authorized.

Examples of actions that may require Change Enablement assessment include:

- Modifying production-like network configurations
- Changing domain controller settings
- Updating firewall rules
- Modifying critical server configurations
- Deploying infrastructure changes

Routine, preauthorized restoration activities may proceed under approved operational procedures.

**Expected Result:** Corrective actions are performed within established authority.

### Step 12 — Implement the Restoration Action

Perform the approved corrective action.

Record:

- Action performed
- System affected
- Command or administrative tool
- Date and time
- Technician
- Observed result

If the action does not work, reassess the evidence rather than repeatedly applying unverified changes.

**Expected Result:** A restoration action is completed and documented.

### Step 13 — Validate Service Restoration

Confirm that the affected service is functioning as expected.

Validation may include:

- Successful authentication
- Restored network connectivity
- Successful application launch
- Successful DNS resolution
- Restored shared folder access
- Normal service status
- Requester confirmation

Validation should address the original reported symptoms.

**Expected Result:** Service restoration is verified.

### Step 14 — Document the Investigation

Update the incident record with:

- Confirmed symptoms
- Scope
- Timeline
- Diagnostic tests
- Evidence
- Findings
- Corrective actions
- Workarounds
- Validation results
- Remaining concerns
- Related records

Distinguish between confirmed findings and suspected causes.

**Expected Result:** Another technician can understand the investigation and outcome.

### Step 15 — Resolve or Escalate

If service is restored:

- Record the resolution.
- Document validation.
- Update incident status.
- Notify the requester when appropriate.
- Follow incident resolution and closure requirements.

If service is not restored:

- Document outstanding findings.
- Identify the escalation reason.
- Transfer responsibility to the appropriate support function.
- Maintain clear ticket ownership.

**Expected Result:** The incident progresses toward documented resolution or appropriate escalation.

---

## 8. Technical Troubleshooting Methods

Technical Techno Tech uses structured troubleshooting methods appropriate to the affected system.

### Method 1 — Bottom-Up Troubleshooting

Begin with foundational components and progress toward higher-level services.

**Networking Example:**

1. Physical or virtual network connection
2. Network adapter status
3. IP configuration
4. Default gateway connectivity
5. DNS resolution
6. Application connectivity

**Best Used For:** Connectivity and infrastructure dependency issues.

### Method 2 — Top-Down Troubleshooting

Begin with the affected application or service and work toward underlying components.

**Example:**

1. Application error
2. Application service
3. Authentication
4. Network connectivity
5. Infrastructure dependencies

**Best Used For:** Application-specific failures.

### Method 3 — Divide-and-Conquer

Test an intermediate component to narrow the affected area.

**Example:**

A workstation cannot access a website.

Test gateway connectivity first.

- Gateway reachable: Investigate upstream connectivity, DNS, or application behavior.
- Gateway unreachable: Investigate local addressing, switching, and gateway availability.

**Best Used For:** Complex issues involving multiple potential failure points.

### Method 4 — Comparison Testing

Compare a failing system with a known-working system.

Potential comparisons:

- IP configuration
- DNS settings
- Group membership
- Operating system configuration
- Application versions
- Security policies

**Best Used For:** Issues affecting one user or device while similar systems function normally.

### Method 5 — Change Correlation

Review recent changes that may be related to the failure.

Examples:

- Group Policy update
- Software installation
- Network configuration change
- Firewall modification
- Operating system update

**Important:** Temporal correlation alone does not prove causation.

---

## 9. Windows Workstation Investigation

Windows workstation incidents may involve:

- Operating system errors
- Application failures
- Network connectivity
- Authentication
- Group Policy
- Device configuration
- Software installation
- Windows updates

### Common Diagnostic Tools

| Tool | Purpose |
|---|---|
| Event Viewer | Review Windows event logs |
| Task Manager | Review processes and resource usage |
| Device Manager | Review device status |
| Services | Review Windows services |
| PowerShell | Perform diagnostics and administration |
| `ipconfig` | Review IP configuration |
| `ping` | Test IP connectivity |
| `nslookup` | Test DNS resolution |
| `gpresult` | Review applied Group Policy |

### Example Commands

**IP Configuration**

```powershell
ipconfig /all
```

**Connectivity**

```powershell
ping 10.20.10.10
```

**DNS Resolution**

```powershell
nslookup dc01.homelab.local
```

**Group Policy Results**

```powershell
gpresult /r
```

**Expected Documentation:** Record relevant output, observed errors, and conclusions.

---

## 10. Active Directory Investigation

Active Directory incidents may involve:

- Authentication failures
- Account lockouts
- Security group membership
- Group Policy
- Domain controller availability
- Replication
- DNS dependencies
- Administrative permissions

### Diagnostic Tools

- Active Directory Users and Computers
- Active Directory Administrative Center
- PowerShell Active Directory module
- Event Viewer
- `dcdiag`
- `repadmin`
- `nltest`

### Example Commands

**Domain Controller Discovery**

```powershell
nltest /dsgetdc:homelab.local
```

**Domain Controller Diagnostics**

```powershell
dcdiag /q
```

**Replication Summary**

```powershell
repadmin /replsummary
```

**Replication Status**

```powershell
repadmin /showrepl
```

**User Account Information**

```powershell
Get-ADUser -Identity "sconnor" -Properties Enabled,LockedOut,MemberOf
```

The example user must exist in the environment for the command to succeed.

**Expected Documentation:** Record observed directory health, errors, and relevant diagnostic findings.

---

## 11. Windows Server Investigation

Windows Server incidents may involve:

- Server unavailability
- Failed services
- DNS failures
- Storage issues
- Performance degradation
- Authentication infrastructure
- Backup failures

### Diagnostic Tools

- Server Manager
- Windows Admin Center
- Event Viewer
- Performance Monitor
- PowerShell
- Windows Server Backup

### Example Commands

**Service Status**

```powershell
Get-Service
```

**Specific Service**

```powershell
Get-Service -Name DNS
```

**Disk Information**

```powershell
Get-Volume
```

**Recent System Errors**

```powershell
Get-WinEvent -FilterHashtable @{
    LogName = 'System'
    Level = 2
    StartTime = (Get-Date).AddHours(-24)
} -MaxEvents 20
```

**Expected Documentation:** Identify affected services, observed failures, and relevant system conditions.

---

## 12. Network Investigation

Network incidents may involve:

- IP addressing
- DNS
- DHCP
- Routing
- Switching
- VLAN configuration
- Firewall restrictions
- Wireless connectivity
- Network performance

### Diagnostic Tools

| Tool | Purpose |
|---|---|
| `ipconfig` | Review network configuration |
| `ping` | Test reachability |
| `tracert` | Examine network path |
| `nslookup` | Test DNS resolution |
| `arp` | Review ARP information |
| `route print` | Review local routing table |
| Packet Tracer | Investigate simulated networks |
| OPNsense | Review firewall and network configuration |
| VyOS | Review routing and network configuration |

### Example Commands

**Network Configuration**

```powershell
ipconfig /all
```

**Default Gateway Test**

```powershell
ping 10.20.20.1
```

**Routing Table**

```powershell
route print
```

**Route Tracing**

```powershell
tracert 10.20.10.10
```

**DNS Test**

```powershell
nslookup homelab.local
```

The gateway address is illustrative and must be replaced with the actual configured gateway.

A failed ping does not always indicate that a device is unavailable because ICMP traffic may be blocked.

---

## 13. Microsoft 365 and Entra ID Investigation

Cloud-related incidents may involve:

- Sign-in failures
- Multifactor authentication
- Licensing
- Microsoft 365 application access
- Cloud service availability
- Administrative permissions
- Device registration

### Investigation Areas

1. Confirm the affected user and service.
2. Review the reported error.
3. Check relevant Microsoft service health information.
4. Review user account status.
5. Verify applicable licensing.
6. Review sign-in information when authorized.
7. Identify access or configuration restrictions.
8. Document findings.

### Administrative Tools

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Microsoft service health dashboards

Access to diagnostic information depends on assigned roles, licensing, and configured features.

**Expected Documentation:** Record relevant service status, account conditions, and diagnostic findings without exposing sensitive identity information.

---

## 14. Virtualization Investigation

Virtualization incidents may involve:

- Virtual machine startup failures
- Virtual networking
- Resource allocation
- Virtual storage
- Operating system boot failures
- Hypervisor configuration

### Investigation Questions

1. Is the virtual machine powered on?
2. Does the guest operating system start?
3. Is the virtual network adapter connected?
4. Is the correct virtual network selected?
5. Are CPU and memory resources sufficient?
6. Is virtual storage available?
7. Are other virtual machines affected?

### Example

**Incident:** CLIENT01 cannot communicate with DC01.

Potential investigation:

1. Verify both virtual machines are powered on.
2. Confirm virtual network adapter connectivity.
3. Review virtual networking configuration.
4. Verify IP addressing.
5. Test connectivity.
6. Test DNS resolution.
7. Test domain controller discovery.

**Expected Documentation:** Record the virtual infrastructure configuration and diagnostic results.

---

## 15. Evidence Collection Standards

Evidence should support the investigation without exposing unnecessary sensitive information.

### Evidence Types

- Screenshots
- Command output
- Event Logs
- Monitoring alerts
- Configuration exports
- Diagnostic reports
- Validation results

### Evidence Directory

```text
Incident-Management/
└── Records/
    └── INC-001-Incident-Title/
        ├── README.md
        └── Evidence/
            ├── 01-Initial-Error.png
            ├── 02-Diagnostic-Output.txt
            ├── 03-Event-Logs.png
            └── 04-Validation-Results.txt
```

### Evidence Requirements

Each evidence item should identify:

- What was tested or observed
- Which system was involved
- When the evidence was collected
- What the result demonstrates

### Security Requirements

Before publishing evidence:

- Remove credentials.
- Remove authentication tokens.
- Redact sensitive account information.
- Avoid exposing private keys.
- Remove confidential network or organizational information where applicable.
- Verify screenshots do not reveal sensitive data.

---

## 16. Investigation Log Format

Every significant troubleshooting action should be documented.

### Recommended Investigation Log

| Time | Action | Tool / Command | Result | Next Step |
|---|---|---|---|---|
| 10:00 | Reviewed incident | Ticketing system | Authentication failure reported | Verify connectivity |
| 10:05 | Tested DC connectivity | `ping` | Result recorded | Review DNS |
| 10:10 | Tested DNS resolution | `nslookup` | Result recorded | Review DC discovery |
| 10:15 | Checked DC discovery | `nltest` | Result recorded | Evaluate findings |

The table is illustrative and does not represent completed lab testing.

### Documentation Rules

- Record actions chronologically.
- Preserve significant error messages.
- Separate observations from interpretations.
- Identify unsuccessful troubleshooting attempts.
- Document configuration changes.
- Record validation results.
- Avoid inventing command output.

---

## 17. Escalation During Investigation

Escalation may be required when:

- Specialized technical knowledge is necessary.
- Administrative permissions are insufficient.
- Critical infrastructure is affected.
- Security risks are identified.
- Initial troubleshooting is unsuccessful.
- The incident exceeds the assigned support function's responsibilities.
- Business impact increases.

### Escalation Handoff Requirements

Include:

1. Incident ID
2. Current priority
3. Affected service
4. Confirmed symptoms
5. Investigation scope
6. Diagnostic tests performed
7. Findings
8. Evidence
9. Suspected causes
10. Requested next action

### Important

Do not delay urgent escalation to complete every troubleshooting step.

**Related Procedure:** [Ticket Escalation](../../Service-Desk/Procedures/Ticket-Escalation.md)

---

## 18. Investigation and Change Enablement

Some restoration activities involve changes to infrastructure or services.

Examples:

- Modifying DNS configuration
- Updating firewall rules
- Changing Group Policy
- Modifying server settings
- Restoring a configuration backup

Before implementation:

1. Determine whether the action is already authorized.
2. Evaluate the operational risk.
3. Identify affected systems.
4. Determine whether Change Enablement applies.
5. Obtain required authorization.
6. Document implementation.
7. Validate results.

Emergency changes may use expedited authorization procedures when applicable.

**Key Principle:** Incident urgency does not automatically eliminate change control requirements.

---

## 19. Workarounds and Temporary Restoration

A workaround reduces or eliminates the impact of an incident without necessarily removing the underlying cause.

### Example

An employee cannot access an application on their assigned workstation.

An approved alternative workstation allows the employee to continue working.

The immediate service impact may be reduced even though the original workstation issue remains unresolved.

### Workaround Documentation

Record:

- Workaround description
- Affected users
- Implementation steps
- Required authorization
- Known limitations
- Validation results
- Whether additional investigation is required

A workaround may support incident resolution when service has been restored to an acceptable level under the organization's criteria.

Unresolved underlying causes may be investigated through Problem Management.

---

## 20. Example Incident Investigation

### Scenario — Domain Authentication Failure

**Incident ID:** INC-001  
**Affected Service:** IT-SVC-001 — Identity & Access Management  
**Category:** Active Directory  
**Subcategory:** Authentication Failure  
**Affected Workstation:** CLIENT01  
**Domain:** homelab.local

### Reported Symptoms

An employee reports being unable to authenticate to a domain-joined Windows workstation.

Authentication previously worked.

### Investigation Objective

Determine whether the failure is related to:

- Network connectivity
- DNS resolution
- Domain controller availability
- User account status
- Workstation domain trust

### Investigation Plan

#### Test 1 — Review IP Configuration

```powershell
ipconfig /all
```

Verify:

- IP address
- Subnet mask
- Default gateway
- DNS server

#### Test 2 — Test Domain Controller Connectivity

```powershell
ping 10.20.10.10
```

Record the result.

#### Test 3 — Test DNS Resolution

```powershell
nslookup dc01.homelab.local
```

Record the result.

#### Test 4 — Test Domain Controller Discovery

```powershell
nltest /dsgetdc:homelab.local
```

Record the result.

#### Test 5 — Review Account Status

Using an authorized administrative account:

```powershell
Get-ADUser -Identity "sconnor" -Properties Enabled,LockedOut
```

Record whether the account is enabled or locked.

### Findings

To be completed after hands-on investigation.

### Confirmed Cause

To be completed only when supported by diagnostic evidence.

### Restoration Action

To be documented after selecting and performing an authorized action.

### Validation

Confirm the employee can authenticate successfully.

### Lessons Learned

Document findings after completing the exercise.

**Scenario Status:** Illustrative investigation plan — no diagnostic results or successful resolution are claimed.

---

## 21. Common Investigation Errors

### Error 1 — Assuming the Root Cause

**Incorrect:** Concluding that DNS is responsible before testing.

**Correct:** Treat DNS as a hypothesis until evidence supports it.

### Error 2 — Making Uncontrolled Changes

**Incorrect:** Changing several configurations simultaneously without documenting them.

**Correct:** Use controlled, authorized changes and record results.

### Error 3 — Ignoring Existing Knowledge

**Incorrect:** Repeating lengthy troubleshooting when an approved workaround already exists.

**Correct:** Review relevant knowledge articles and known errors.

### Error 4 — Failing to Record Unsuccessful Tests

**Incorrect:** Documenting only the successful corrective action.

**Correct:** Record significant diagnostic attempts and their results.

### Error 5 — Confusing Symptoms With Causes

**Incorrect:** Recording "network outage" as the confirmed cause because an application cannot connect.

**Correct:** Investigate whether the failure involves DNS, routing, authentication, or another dependency.

### Error 6 — Delaying Escalation

**Incorrect:** Continuing unauthorized or ineffective troubleshooting during a critical outage.

**Correct:** Escalate according to technical complexity, business impact, and security requirements.

### Error 7 — Failing to Validate Restoration

**Incorrect:** Closing an incident immediately after changing a setting.

**Correct:** Verify that the original service failure has been resolved.

---

## 22. Incident Investigation Quality Checklist

Before completing an investigation, verify:

- [ ] Incident record reviewed
- [ ] Reported symptoms confirmed
- [ ] Investigation scope established
- [ ] Timeline documented
- [ ] Relevant knowledge reviewed
- [ ] Affected services identified
- [ ] Related Configuration Items identified when applicable
- [ ] Diagnostic evidence collected
- [ ] Potential causes documented
- [ ] Diagnostic tests performed
- [ ] Test results recorded
- [ ] Findings supported by evidence
- [ ] Restoration options evaluated
- [ ] Required authorization obtained
- [ ] Corrective actions documented
- [ ] Service restoration validated
- [ ] Workaround documented when applicable
- [ ] Escalation completed when necessary
- [ ] Requester updated when appropriate
- [ ] Incident record updated
- [ ] Problem investigation considered when warranted

---

## 23. Investigation Performance Metrics

Incident investigation effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Mean Time to Restore Service (MTRS) | Measures average time required to restore service |
| First Contact Resolution Rate | Measures incidents resolved during initial support contact |
| Escalation Rate | Tracks incidents requiring additional support |
| Repeat Incident Rate | Identifies recurring service disruptions |
| Investigation Documentation Completeness | Measures quality of recorded technical findings |
| Workaround Effectiveness | Evaluates whether workarounds reduce service impact |
| Incident Reopen Rate | Identifies incidents requiring further investigation |
| Knowledge Article Reuse | Measures use of existing troubleshooting guidance |
| Service Restoration Validation Rate | Tracks documented verification of restoration |

Metrics should be calculated using actual incident records or clearly labeled simulated datasets.

---

## 24. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Performs initial investigation and coordinates communication |
| Incident Management | Investigates incidents and restores services |
| Service Request Management | Handles predefined requests identified during assessment |
| Knowledge Management | Provides troubleshooting instructions and known errors |
| Problem Management | Investigates underlying causes when warranted |
| Change Enablement | Controls applicable corrective modifications |
| Monitoring and Event Management | Provides alerts and diagnostic information |
| Service Configuration Management | Identifies affected infrastructure and dependencies |
| Information Security Management | Supports investigation of security-related incidents |
| Continual Improvement | Uses investigation findings to improve services |

---

## 25. Related Procedures and Documentation

### Incident Management

- [Incident Management Overview](../README.md)
- [Incident Logging Procedure](Incident-Logging.md)

### Service Desk Procedures

- [Ticket Intake](../../Service-Desk/Procedures/Ticket-Intake.md)
- [Ticket Categorization](../../Service-Desk/Procedures/Ticket-Categorization.md)
- [Ticket Prioritization](../../Service-Desk/Procedures/Ticket-Prioritization.md)
- [Ticket Escalation](../../Service-Desk/Procedures/Ticket-Escalation.md)

### ITIL Practices

- [Knowledge Management](../../Knowledge-Management/)
- [Problem Management](../../Problem-Management/)
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

### Templates

- [Incident Template](../../Templates/Incident-Template.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Operational Scenarios](../../Scenarios/)

---

## 26. Procedure Review

This procedure should be reviewed when:

- New technologies are introduced.
- Troubleshooting standards change.
- Administrative tools are updated.
- Incident investigations reveal documentation gaps.
- Escalation responsibilities change.
- Security requirements are modified.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial incident investigation and diagnosis procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee reports, organizational roles, business requirements, and incident scenarios may be simulated.

Technical investigations, diagnostic commands, infrastructure configurations, corrective actions, and validation results are documented based on hands-on lab work where indicated.

This procedure demonstrates ITIL-aligned Incident Management, structured troubleshooting, technical diagnosis, service restoration, and operational documentation rather than employment experience within an actual production organization.
