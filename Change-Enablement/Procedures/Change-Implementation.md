# SOP — Change Implementation

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Change Enablement  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-CE-002  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Change Enablement

---

## 1. Purpose

This procedure establishes a standardized method for implementing authorized changes to Technical Techno Tech's internal IT services and infrastructure.

Change Implementation ensures that approved modifications are executed in a controlled, documented, and verifiable manner while minimizing disruption to business operations.

The procedure supports:

- Consistent implementation of authorized changes
- Reduced risk of service disruption
- Clear technical execution procedures
- Verification of implementation readiness
- Protection of existing configurations
- Effective implementation monitoring
- Early detection of unexpected behavior
- Reliable rollback and recovery
- Accurate technical documentation
- Improved change success rates
- Continual improvement

**Key Principle:** Implement only what has been authorized, validate the resulting system state, and maintain a recovery strategy if the change does not produce the expected outcome.

---

## 2. Scope

This procedure applies to authorized changes affecting Technical Techno Tech's internal IT services and supporting infrastructure.

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

Change implementation may involve:

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

### Example Changes

- Updating Group Policy settings
- Modifying DNS or DHCP configurations
- Deploying software
- Installing operating system updates
- Updating firewall rules
- Changing network routing
- Modifying server roles
- Configuring endpoint management policies
- Updating authentication settings
- Deploying additional infrastructure components

Technologies should only be described as operational when supported by actual lab evidence.

---

## 3. ITIL 4 Change Enablement

### Purpose

The purpose of Change Enablement is to maximize the number of successful service and product changes by ensuring that risks have been properly assessed, authorizing changes to proceed, and managing the change schedule.

### Important Definitions

**Change:** The addition, modification, or removal of anything that could have a direct or indirect effect on services.

**Change Authorization:** The decision permitting a proposed change to proceed under defined conditions.

**Change Implementation:** The controlled execution of an authorized modification.

**Change Schedule:** Information used to plan changes and identify potential conflicts.

**Rollback / Backout:** Actions taken to return to an acceptable previous state when implementation fails.

**Post-Implementation Review (PIR):** An evaluation of the change's outcome, including its effectiveness, impact, and lessons learned.

### Authorization vs. Implementation

| Change Authorization | Change Implementation |
|---|---|
| Determines whether a change may proceed | Executes the authorized modification |
| Reviews business and technical risk | Follows the approved technical plan |
| Establishes implementation conditions | Verifies that conditions are satisfied |
| Evaluates recovery readiness | Performs recovery when required |
| Records approval decisions | Records execution and validation results |

Authorization must precede implementation unless the activity is already covered by an applicable preauthorized standard change model.

---

## 4. Change Implementation Principles

Technical Techno Tech follows these principles during change implementation.

### 4.1 Authorization First

Do not implement changes without the required authorization.

### 4.2 Follow the Approved Scope

Implement only the modifications covered by the authorization.

### 4.3 Verify Readiness

Confirm prerequisites, access, backups, dependencies, and implementation conditions before beginning.

### 4.4 Establish a Baseline

Record the relevant system configuration before making modifications.

### 4.5 Use Controlled Execution

Follow the approved implementation sequence and avoid unnecessary simultaneous changes.

### 4.6 Validate Results

Confirm that the change achieved its intended outcome.

### 4.7 Monitor for Unexpected Impact

Review affected services and systems for unintended consequences.

### 4.8 Maintain Recovery Capability

Use the approved rollback or recovery plan when necessary.

### 4.9 Document Actual Results

Record what was performed, what succeeded, what failed, and what remains unresolved.

### 4.10 Support Continual Improvement

Use implementation findings to improve future changes.

---

## 5. Roles and Responsibilities

### Change Owner

Responsible for:

- Coordinating implementation
- Confirming authorization
- Reviewing implementation readiness
- Managing dependencies
- Tracking implementation progress
- Coordinating validation
- Maintaining the Change record

### Implementation Technician

Responsible for:

- Performing the authorized technical change
- Following the approved implementation plan
- Recording technical actions
- Monitoring immediate results
- Performing technical validation
- Initiating authorized recovery procedures when necessary

### Change Coordinator

Responsible for:

- Confirming the implementation schedule
- Coordinating affected teams
- Monitoring change progress
- Managing implementation communication
- Recording change status
- Supporting post-implementation review

### Technical Reviewer

Responsible for:

- Reviewing implementation requirements
- Evaluating technical readiness
- Supporting complex implementations
- Reviewing unexpected technical results
- Assisting with recovery decisions

### Service Owner

Responsible for:

- Confirming service requirements
- Evaluating business impact
- Supporting functional validation
- Reviewing service restoration when applicable

### Information Security Personnel

Responsible for:

- Reviewing security-sensitive implementation activities
- Confirming applicable security requirements
- Supporting security validation
- Evaluating unexpected security impacts

### Service Desk

Responsible for:

- Receiving implementation-related incident reports
- Communicating relevant service information
- Supporting affected employees
- Linking change-related incidents to the Change record

**Lab Note:** These roles represent simulated organizational responsibilities. One learner may perform multiple roles during a controlled lab exercise.

---

## 6. Change Implementation Prerequisites

Before implementation, verify the following requirements.

### Authorization

- Required approval is documented.
- Authorization conditions are satisfied.
- Approved scope is understood.
- The change remains within the authorized risk level.

### Technical Preparation

- Required tools are available.
- Administrative permissions are confirmed.
- Affected systems are identified.
- Dependencies are understood.
- Relevant technical documentation is available.

### Recovery Preparation

- Required backups or exports are complete.
- Previous configuration values are recorded.
- Rollback instructions are available.
- Recovery requirements are understood.

### Scheduling

- The approved implementation window is confirmed.
- Relevant personnel are available.
- Conflicting changes have been reviewed.
- Required communications are complete.

### Validation

- Success criteria are documented.
- Validation commands are prepared.
- Expected results are understood.
- Required functional testing is identified.

**Important:** If a required prerequisite is not satisfied, implementation should not begin until the issue is resolved or the change is appropriately reassessed.

---

## 7. Change Implementation Lifecycle

```text
Authorized Change
        |
        v
Review Approved Change Record
        |
        v
Confirm Implementation Readiness
        |
        v
Notify Relevant Stakeholders
        |
        v
Capture Pre-Change Baseline
        |
        v
Verify Backup / Recovery
        |
        v
Begin Implementation
        |
        v
Execute Approved Steps
        |
        v
Perform Technical Validation
        |
        v
Change Successful?
        |
   +----+----+
   |         |
  Yes        No
   |         |
   v         v
Functional  Assess Failure
Validation      |
   |            v
   |       Recovery Required?
   |            |
   |       +----+----+
   |       |         |
   |      Yes        No
   |       |         |
   |       v         v
   |    Rollback   Authorized
   |       |       Remediation
   |       |         |
   +-------+---------+
           |
           v
   Document Results
           |
           v
   Update Change Status
           |
           v
   Post-Implementation Review
           |
           v
   Change Closure
```

Implementation, review, and closure are related activities but should remain distinguishable in the Change record.

---

## 8. Change Implementation Procedure

### Step 1 — Review the Authorized Change Record

Open the relevant Change record.

Review:

- Change ID
- Change title
- Change type
- Business justification
- Affected services
- Affected Configuration Items
- Approved implementation scope
- Risk assessment
- Implementation plan
- Validation plan
- Rollback plan
- Authorization decision
- Authorization conditions
- Approved implementation window

#### Example

```text
Change ID: CHG-001

Title:
Correct DHCP DNS Server Configuration

Change Type:
Normal

Affected Service:
IT-SVC-004 — Network Connectivity

Related Problem:
PRB-001

Authorization Status:
Pending Verification
```

**Expected Result:** The implementation technician understands the approved change and its requirements.

### Step 2 — Confirm Authorization

Verify that the change has received the authorization required for its type and risk.

Check:

1. Is the authorization decision recorded?
2. Is the approved scope clearly defined?
3. Are authorization conditions satisfied?
4. Is the implementation window valid?
5. Have any material risks changed?
6. Are additional approvals required?

#### Decision

If authorization is valid:

Proceed with preparation.

If authorization is missing or no longer applicable:

Stop and refer the change for authorization or reassessment.

**Expected Result:** The change is confirmed as authorized.

### Step 3 — Confirm Implementation Scope

Review exactly what systems and configurations may be modified.

#### Example

**Approved Scope:** Update DNS server options on a specific DHCP scope.

**Not Automatically Authorized:**

- Modifying unrelated DHCP scopes
- Changing domain controller IP addresses
- Updating firewall policies
- Reconfiguring unrelated DNS zones

If additional modifications are required, evaluate whether reauthorization is necessary.

**Expected Result:** Implementation boundaries are established.

### Step 4 — Verify Technical Prerequisites

Confirm that the required technical conditions are satisfied.

Potential prerequisites include:

- Administrative access
- Network connectivity
- Required software tools
- Available server resources
- Healthy dependent services
- Required configuration files
- Appropriate backups
- Access to recovery systems

#### Example — Active Directory

Before modifying a domain-related configuration, relevant health checks may include:

```powershell
dcdiag /q
```

```powershell
repadmin /replsummary
```

Results should be interpreted before proceeding.

**Expected Result:** Technical readiness is verified.

### Step 5 — Confirm the Implementation Window

Review the approved schedule.

Consider:

- Business operating hours
- Expected service disruption
- Required downtime
- Personnel availability
- Related infrastructure activities
- Recovery time

#### Example

A DNS infrastructure modification may be scheduled during a period of reduced service demand.

A lab exercise may use a simulated maintenance window.

**Expected Result:** The implementation schedule is confirmed.

### Step 6 — Notify Relevant Stakeholders

Communicate the planned implementation when required.

Potential recipients include:

- Change owner
- Service owner
- Service Desk
- Systems Administration
- Network Administration
- Information Security
- Affected employees

### Recommended Communication Information

```text
Change ID:
Change Summary:
Affected Services:
Implementation Window:
Expected Impact:
Responsible Team:
Support Contact:
```

**Expected Result:** Relevant participants understand the planned change.

### Step 7 — Capture the Pre-Change Baseline

Document the relevant system state before modification.

Baseline information may include:

- Current configuration
- Service status
- Network settings
- Software versions
- Existing policy settings
- Resource usage
- Relevant event logs

#### Example — Network Configuration

```powershell
ipconfig /all
```

#### Example — Windows Services

```powershell
Get-Service
```

#### Example — DNS Client Configuration

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

#### Example — Group Policy

```powershell
gpresult /r
```

**Expected Result:** Relevant pre-change conditions are documented for comparison.

### Step 8 — Verify Backup and Recovery Readiness

Confirm that required recovery resources are available.

Potential recovery resources include:

- Configuration exports
- System backups
- Approved VM snapshots for suitable lab scenarios
- Previous policy settings
- Documented configuration values
- Recovery scripts

### Backup Verification

Check:

1. Was the backup or export completed?
2. Does it cover the affected configuration?
3. Is the recovery method appropriate?
4. Can the backup be accessed?
5. Are restoration limitations understood?

**Important:** A VM snapshot is not a substitute for a supported backup strategy, particularly for systems such as Active Directory domain controllers.

**Expected Result:** Recovery readiness is verified.

### Step 9 — Begin the Implementation

Record the actual implementation start time.

Update the Change record to an appropriate status.

**Proposed Status:** In Progress

Confirm that:

- The correct system is selected.
- The correct administrative account is used.
- The approved procedure is available.
- Required personnel are ready.

**Expected Result:** The authorized implementation begins.

### Step 10 — Execute the Approved Technical Steps

Perform the implementation according to the approved plan.

### Execution Standards

- Follow the documented sequence.
- Avoid unrelated modifications.
- Record deviations.
- Confirm expected results at checkpoints.
- Stop when unexpected risks emerge.
- Preserve relevant technical evidence.

#### Example

**Change:** Modify an approved DNS client configuration.

An authorized technician may use:

```powershell
Set-DnsClientServerAddress -InterfaceAlias "Ethernet0" -ServerAddresses 10.20.10.10,10.20.10.11
```

This command changes DNS settings on the specified network interface.

It is not a command for changing DHCP scope options.

The interface alias, addresses, and authorization must be verified before execution.

**Expected Result:** The approved technical modification is performed.

### Step 11 — Record Implementation Activities

Document each significant action.

### Implementation Log

| Field | Description |
|---|---|
| Timestamp | When the action occurred |
| Technician | Who performed the action |
| System | Affected device or service |
| Action | Modification performed |
| Result | Success, failure, or partial completion |
| Evidence | Supporting output or screenshot |

#### Example

```text
IMPLEMENTATION LOG

Change ID:
Date:
Technician:

Time:
System:
Action:
Expected Result:
Actual Result:
Evidence:
Notes:
```

**Expected Result:** Implementation activities are traceable.

### Step 12 — Perform Immediate Technical Validation

Verify that the intended configuration or functionality is present.

### Validation Examples

**DNS Configuration**

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

**DNS Resolution**

```powershell
nslookup dc01.homelab.local
```

**Domain Controller Discovery**

```powershell
nltest /dsgetdc:homelab.local
```

**Windows Service Status**

```powershell
Get-Service -Name DNS
```

### Validation Requirements

Compare:

- Expected results
- Actual results
- Pre-change baseline
- Approved success criteria

**Expected Result:** The technical outcome is documented.

### Step 13 — Perform Functional Validation

Technical success does not always guarantee successful service delivery.

Functional validation should confirm that the affected service works as intended.

#### Examples

| Change | Functional Validation |
|---|---|
| DNS Configuration | Workstation resolves required internal resources |
| Active Directory | Authorized user authenticates successfully |
| Group Policy | Intended policy applies to target computers |
| Software Deployment | Application launches and performs required functions |
| Firewall Rule | Authorized traffic works and unintended access remains restricted |
| Network Routing | Required destinations are reachable |
| Microsoft 365 Configuration | Intended user workflow functions correctly |

**Expected Result:** Relevant service functionality is verified.

### Step 14 — Perform Security Validation

Determine whether the change affected applicable security controls.

Review:

- Authentication
- Authorization
- Administrative access
- Firewall restrictions
- Audit logging
- Endpoint protection
- Network segmentation
- Data access permissions

#### Example

After modifying a firewall rule:

1. Confirm authorized traffic is permitted.
2. Verify that unrelated traffic remains restricted.
3. Review relevant logging.
4. Confirm the rule matches the approved scope.

**Expected Result:** Required security controls remain effective.

### Step 15 — Monitor for Unexpected Impact

Observe affected services after implementation.

Potential monitoring sources:

- Windows Event Logs
- Service status
- Network diagnostics
- Performance Monitor
- Microsoft service health information
- Relevant cloud logs
- User-reported incidents
- Infrastructure monitoring tools

### Monitoring Questions

1. Are the affected services operational?
2. Have new errors appeared?
3. Are users reporting failures?
4. Has system performance changed?
5. Are related dependencies healthy?
6. Is the change producing the expected benefit?

**Expected Result:** Unexpected consequences are identified.

### Step 16 — Evaluate Implementation Success

Compare actual results against the approved success criteria.

### Possible Outcomes

| Outcome | Description |
|---|---|
| Successful | Approved objectives achieved and required validation passed |
| Successful With Issues | Objectives achieved, but minor issues or follow-up work remain |
| Partially Successful | Some objectives achieved, others remain incomplete |
| Failed | Required objectives were not achieved |
| Rolled Back | Recovery actions returned the environment to an acceptable state |
| Inconclusive | Available evidence is insufficient to determine success |

### Example

**Change:** Correct DNS configuration.

**Success Criteria:**

- Approved DNS settings are present.
- Required internal names resolve.
- Domain controller discovery succeeds.
- Authorized authentication works.
- No unacceptable service impact is observed.

**Expected Result:** Implementation outcome is accurately classified.

### Step 17 — Determine Whether Rollback Is Required

Evaluate whether the change must be reversed.

### Potential Rollback Triggers

- Critical validation failure
- Unexpected service outage
- Security control failure
- Significant performance degradation
- Incorrect configuration
- Unacceptable business impact
- Exceeded implementation window
- Inability to complete the approved change safely

### Decision

If the change is successful:

Proceed to documentation and review.

If the change fails:

Follow the approved recovery decision process.

**Expected Result:** The need for rollback is assessed.

### Step 18 — Execute Authorized Rollback When Necessary

Follow the approved rollback plan.

### General Rollback Procedure

1. Stop further implementation.
2. Notify the responsible change authority or coordinator.
3. Confirm the rollback decision.
4. Record the current system state.
5. Execute the approved recovery steps.
6. Restore relevant previous configurations.
7. Validate recovered functionality.
8. Document the outcome.
9. Escalate unresolved failures.

### Example

**Change:** Modify DNS client configuration.

**Rollback:** Restore the previously recorded DNS server addresses or approved automatic configuration, as applicable.

#### Illustrative Command

```powershell
Set-DnsClientServerAddress -InterfaceAlias "Ethernet0" -ResetServerAddresses
```

This command resets the interface to its default DNS configuration behavior. It does not necessarily restore previously configured static DNS addresses.

If the original configuration used static DNS servers, restore the documented original values instead.

**Expected Result:** The environment is returned to an acceptable state when recovery is possible.

### Step 19 — Handle Unexpected Implementation Issues

If an unexpected condition occurs:

1. Stop potentially harmful actions.
2. Record the observed issue.
3. Assess the impact.
4. Determine whether service restoration is required.
5. Escalate to the appropriate technical personnel.
6. Follow applicable Incident Management procedures.
7. Evaluate whether a new change authorization is required.
8. Preserve diagnostic evidence.

### Example

A firewall change unexpectedly blocks authentication traffic.

The implementation technician should not introduce unrelated firewall modifications without appropriate assessment and authorization.

**Expected Result:** Unexpected issues are managed through controlled procedures.

### Step 20 — Update Configuration Documentation

After a successful implementation, update applicable infrastructure and Configuration Item records.

Potential updates include:

- Server configurations
- Network topology
- DNS and DHCP settings
- Group Policy documentation
- Software versions
- Firewall rules
- Cloud service configurations
- Configuration Item relationships

### Example

A DHCP configuration change may require updates to:

- DHCP server documentation
- Relevant network configuration records
- Affected Configuration Items
- Technical Knowledge Base articles

**Expected Result:** Documentation reflects the implemented configuration.

### Step 21 — Update Related Knowledge Articles

Determine whether technical procedures require revision.

Examples:

- Troubleshooting instructions
- Administrative guides
- Known error workarounds
- Configuration procedures
- Recovery documentation

### Example

A permanent correction eliminates a known error workaround.

The associated Knowledge Base article should be reviewed to prevent technicians from applying obsolete instructions.

**Expected Result:** Operational knowledge remains accurate.

### Step 22 — Communicate Implementation Results

Notify relevant stakeholders of the implementation outcome.

### Recommended Information

- Change ID
- Implementation status
- Actual service impact
- Validation outcome
- Remaining issues
- Rollback status
- Follow-up requirements

#### Example

```text
CHANGE IMPLEMENTATION UPDATE

Change ID:
Change Summary:
Implementation Date:
Outcome:
Affected Services:
Validation Results:
Outstanding Issues:
Next Steps:
```

**Expected Result:** Relevant participants receive accurate implementation information.

### Step 23 — Update the Change Record

Document:

- Actual start and completion times
- Actions performed
- Systems modified
- Implementation results
- Validation evidence
- Unexpected issues
- Rollback actions
- Remaining risks
- Related incidents
- Documentation updates
- Follow-up requirements

### Proposed Status

**Implemented — Pending Review**

If the implementation failed, use an appropriate status reflecting the actual outcome.

**Expected Result:** The Change record accurately reflects implementation activities.

### Step 24 — Prepare for Post-Implementation Review

Provide the information required to evaluate the change.

### Review Questions

1. Was the change implemented as authorized?
2. Were the expected objectives achieved?
3. Did implementation remain within the approved scope?
4. Were there unexpected incidents?
5. Was rollback necessary?
6. Were security controls preserved?
7. Was the implementation completed within the planned window?
8. Were documentation updates completed?
9. What improvements are needed?

**Expected Result:** The change is ready for post-implementation evaluation.

---

## 9. Standard Change Implementation

Standard changes follow approved, repeatable procedures.

### Requirements

- An approved standard change model exists.
- The proposed activity meets the model's conditions.
- Required prerequisites are satisfied.
- The procedure is documented.
- Validation requirements are defined.
- Recovery instructions are available.

### Procedure

1. Confirm the standard change model.
2. Verify eligibility.
3. Record the planned activity.
4. Complete required preparation.
5. Execute the approved steps.
6. Perform validation.
7. Document the outcome.
8. Escalate exceptions.

### Important

If the activity falls outside the approved standard change model, reassessment may be required.

A routine activity is not automatically a standard change.

---

## 10. Normal Change Implementation

Normal changes follow the risk-based authorization and implementation process.

### Typical Activities

- Infrastructure configuration updates
- New server role deployments
- Network routing changes
- Firewall policy modifications
- Group Policy changes
- Cloud service configuration changes

### Requirements

- Applicable authorization
- Documented implementation plan
- Risk and impact assessment
- Appropriate scheduling
- Technical validation
- Recovery planning
- Implementation documentation

Higher-risk normal changes may require additional coordination, testing, and monitoring.

---

## 11. Emergency Change Implementation

Emergency changes use expedited procedures when urgent action is necessary.

### Examples

- Critical service restoration
- Urgent security remediation
- Prevention of imminent infrastructure failure

### Emergency Implementation Procedure

1. Confirm the emergency condition.
2. Review the minimum necessary corrective action.
3. Obtain emergency authorization.
4. Record essential implementation information.
5. Verify critical prerequisites.
6. Perform the authorized change.
7. Validate immediate results.
8. Monitor affected services.
9. Document the actual implementation.
10. Complete required retrospective review.

### Important Requirements

Emergency implementation must still consider:

- Authorization
- Technical risk
- Service impact
- Security
- Recovery
- Documentation

Emergency classification should not be used to bypass normal planning when no genuine urgency exists.

---

## 12. Implementation Validation Standards

Validation should confirm that the change meets its intended objectives.

### Technical Validation

Confirms that the intended configuration or technical state is present.

### Functional Validation

Confirms that the affected service works as intended.

### Security Validation

Confirms that applicable security controls remain effective.

### Stability Validation

Confirms that the environment does not exhibit unacceptable errors or degradation after implementation.

### Example

**Change:** Update domain-related DNS configuration.

| Validation Type | Example |
|---|---|
| Technical | Correct DNS addresses are configured |
| Functional | Domain controller discovery succeeds |
| Security | Authentication requirements remain enforced |
| Stability | No unacceptable recurring connectivity errors appear |

The required observation period depends on the nature and risk of the change.

---

## 13. Change Implementation Evidence

Implementation evidence should demonstrate what was actually performed.

### Evidence Types

- Pre-change configuration
- Configuration backups
- PowerShell output
- Screenshots
- Event Logs
- Monitoring results
- Post-change configuration
- Functional test results
- Rollback results
- Implementation notes

### Example Directory

```text
Change-Enablement/
└── Records/
    └── CHG-001-DNS-Configuration-Update/
        ├── README.md
        └── Evidence/
            ├── 01-Pre-Change-Configuration.txt
            ├── 02-Backup-Verification.md
            ├── 03-Implementation-Log.md
            ├── 04-Post-Change-Configuration.txt
            ├── 05-Validation-Results.md
            └── 06-Post-Implementation-Review.md
```

These filenames represent a proposed record structure.

### Evidence Requirements

Each evidence item should identify:

- Affected system
- Collection date and time
- Tool or method used
- Actual observed result
- Interpretation
- Related change

Do not fabricate command output, screenshots, or validation results.

---

## 14. Implementation Log Template

Use the following structure within the Change record.

```text
CHANGE IMPLEMENTATION LOG

Change ID:
Change Title:
Change Type:
Change Owner:
Implementation Technician:
Implementation Date:

Authorization Reference:

Approved Scope:

Pre-Change Baseline:

Backup / Recovery Verification:

Implementation Start Time:

IMPLEMENTATION ACTIONS

Step 1:
Timestamp:
System:
Action:
Expected Result:
Actual Result:
Evidence:

Step 2:
Timestamp:
System:
Action:
Expected Result:
Actual Result:
Evidence:

Step 3:
Timestamp:
System:
Action:
Expected Result:
Actual Result:
Evidence:

VALIDATION

Technical Validation:

Functional Validation:

Security Validation:

Stability Validation:

ISSUES

Unexpected Issues:

Related Incidents:

ROLLBACK

Rollback Required:
Rollback Actions:
Rollback Validation:

OUTCOME

Implementation Status:
Actual Completion Time:
Outstanding Risks:
Follow-Up Actions:
Documentation Updates:

Review Status:
```

---

## 15. Example Change Implementation Scenario

### Scenario — Correcting DHCP DNS Server Configuration

**Change ID:** CHG-001  
**Change Type:** Normal  
**Affected Service:** IT-SVC-004 — Network Connectivity  
**Related Problem:** PRB-001  
**Environment:** homelab.local

### Business Context

Domain-joined workstations depend on internal DNS services to locate domain controllers.

A simulated Problem Management investigation identifies incorrect DNS server options distributed through DHCP.

### Proposed Change

Update the affected DHCP scope options to distribute the approved internal DNS servers.

### Proposed DNS Servers

| Server | IP Address |
|---|---|
| DC01 | 10.20.10.10 |
| DC02 | 10.20.10.11 |

The current availability and DNS configuration of both servers must be verified before implementation.

### Implementation Prerequisites

- Appropriate change authorization
- Administrative access to the DHCP server
- Identification of the correct DHCP scope
- Verification of approved DNS addresses
- Configuration backup or export
- Documented rollback plan
- Available test workstation

### Proposed Pre-Change Validation

On the DHCP server, if the Windows DHCP Server PowerShell module is available:

```powershell
Get-DhcpServerv4Scope
```

Review the DNS options for the applicable scope:

```powershell
Get-DhcpServerv4OptionValue -ScopeId <ScopeNetworkAddress>
```

Replace `<ScopeNetworkAddress>` with the actual DHCP scope network address.

### Proposed Implementation

After confirming the correct scope, approved values, and authorization:

```powershell
Set-DhcpServerv4OptionValue -ScopeId <ScopeNetworkAddress> -DnsServer 10.20.10.10,10.20.10.11
```

This command updates the DNS server option for the specified DHCP scope.

It must not be executed until the DHCP server, scope, and intended configuration have been verified.

### Proposed Client Validation

On an appropriate DHCP-configured test workstation:

```powershell
ipconfig /renew
```

Review the resulting configuration:

```powershell
ipconfig /all
```

Verify DNS resolution:

```powershell
nslookup dc01.homelab.local
```

Verify domain controller discovery:

```powershell
nltest /dsgetdc:homelab.local
```

Confirm successful authorized domain authentication.

### Proposed Rollback

If validation fails:

1. Stop further implementation.
2. Review the observed failure.
3. Confirm the rollback decision.
4. Restore the previously documented DHCP DNS options.
5. Renew the test workstation's DHCP configuration.
6. Verify DNS resolution.
7. Confirm domain controller discovery.
8. Document the results.

### Proposed Success Criteria

- Approved DNS settings are distributed.
- The test workstation receives the expected configuration.
- Internal DNS resolution succeeds.
- Domain controller discovery succeeds.
- Domain authentication functions correctly.
- No unacceptable service impact is observed.

### Implementation Record

| Requirement | Status |
|---|---|
| Authorization | Pending |
| Configuration Backup | Not Performed |
| Pre-Change Baseline | Not Collected |
| Implementation | Not Started |
| Technical Validation | Not Performed |
| Functional Validation | Not Performed |
| Rollback | Not Required — Change Not Started |
| Post-Implementation Review | Pending |

### Expected Outcome

The change is implemented only after the required authorization and readiness checks are completed.

Actual results should be recorded in the Change record.

**Scenario Status:** Illustrative implementation plan. No change execution, validation, or approval is claimed as completed.

---

## 16. Failed Change Management

A failed change requires controlled handling.

### Potential Failure Conditions

- Implementation cannot be completed.
- Required validation fails.
- An unexpected service outage occurs.
- Security requirements are violated.
- The change introduces unacceptable performance degradation.
- Recovery procedures are required.

### Failed Change Procedure

1. Stop further potentially harmful modifications.
2. Assess the current service state.
3. Notify the appropriate change authority.
4. Determine whether rollback is required.
5. Execute authorized recovery actions.
6. Validate recovered services.
7. Record the failure.
8. Create related Incident records when appropriate.
9. Identify follow-up Problem Management requirements.
10. Review lessons learned.

### Important Distinction

A failed change does not automatically mean the entire service is unavailable.

The actual technical and business impact must be documented.

---

## 17. Rollback and Recovery Management

Rollback planning is an essential part of controlled change implementation.

### Rollback Objectives

- Reduce service disruption
- Restore acceptable functionality
- Recover approved configurations
- Preserve relevant evidence
- Limit additional operational risk

### Rollback Requirements

| Requirement | Description |
|---|---|
| Trigger | Condition requiring recovery |
| Decision Authority | Person or role responsible for the decision |
| Recovery Method | Approved restoration approach |
| Previous State | Documented baseline |
| Dependencies | Required services and tools |
| Validation | How recovery will be confirmed |
| Communication | Who must be informed |
| Evidence | Recovery actions and results |

### Important Considerations

Not every change is fully reversible.

For irreversible or difficult-to-reverse changes, the approved plan should identify an alternative recovery strategy.

---

## 18. Change Implementation Security

Implementation activities must follow applicable security requirements.

### Security Controls

- Use authorized administrative accounts.
- Apply least-privilege principles.
- Protect credentials.
- Avoid unnecessary privilege escalation.
- Preserve audit logging.
- Review firewall and access changes.
- Protect configuration backups.
- Validate security-sensitive modifications.

### Public Portfolio Considerations

Do not publish:

- Passwords
- Authentication tokens
- Private keys
- Sensitive production configurations
- Confidential employee information
- Unredacted personal data

Screenshots and command output should be reviewed before publication.

---

## 19. Change Implementation Documentation Standards

Implementation records should distinguish between:

### Planned Actions

Actions intended to be performed.

### Completed Actions

Actions actually executed.

### Observed Results

Technical output or behavior directly observed.

### Expected Results

Outcomes anticipated before testing.

### Unverified Results

Outcomes that have not been confirmed.

### Example

**Planned Action:** Update DNS configuration.

**Expected Result:** Workstations receive approved DNS server addresses.

**Actual Result:** Not yet tested.

**Status:** Implementation Pending.

Do not represent expected outcomes as completed results.

---

## 20. Change Implementation Quality Checklist

Before implementation:

- [ ] Change record exists
- [ ] Change ID verified
- [ ] Change type confirmed
- [ ] Authorization verified
- [ ] Authorization conditions satisfied
- [ ] Approved scope reviewed
- [ ] Affected services identified
- [ ] Configuration Items identified
- [ ] Technical prerequisites confirmed
- [ ] Required permissions available
- [ ] Implementation window confirmed
- [ ] Stakeholders notified when required
- [ ] Pre-change baseline captured
- [ ] Backup requirements satisfied
- [ ] Recovery plan reviewed
- [ ] Validation plan available

During implementation:

- [ ] Correct system selected
- [ ] Approved procedure followed
- [ ] Actions recorded
- [ ] Unexpected issues documented
- [ ] Implementation checkpoints verified
- [ ] Unapproved scope changes avoided
- [ ] Security requirements maintained

After implementation:

- [ ] Technical validation completed
- [ ] Functional validation completed
- [ ] Security validation completed when applicable
- [ ] Stability assessed
- [ ] Rollback decision documented
- [ ] Recovery validated if performed
- [ ] Actual outcome recorded
- [ ] Configuration documentation updated
- [ ] Related knowledge articles reviewed
- [ ] Relevant stakeholders informed
- [ ] Change status updated
- [ ] Post-implementation review prepared

---

## 21. Change Implementation Performance Metrics

Change implementation effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Change Success Rate | Measures changes achieving approved objectives |
| Failed Change Rate | Tracks unsuccessful implementations |
| Rollback Rate | Measures changes requiring recovery |
| Change-Related Incident Rate | Tracks incidents associated with changes |
| Implementation Duration | Measures actual execution time |
| Schedule Adherence | Evaluates completion within planned windows |
| Validation Completion Rate | Tracks required testing |
| Documentation Completeness | Measures implementation record quality |
| Unauthorized Deviation Rate | Identifies actions outside approved scope |
| Post-Implementation Review Completion | Tracks completion of required reviews |
| Repeat Change Failure Rate | Identifies recurring implementation weaknesses |

Metrics should be calculated using actual records or clearly labeled simulated datasets.

---

## 22. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Supports communication and receives change-related incidents |
| Incident Management | Restores services affected by unsuccessful changes |
| Service Request Management | May initiate approved fulfillment-related changes |
| Knowledge Management | Maintains implementation and troubleshooting documentation |
| Problem Management | Recommends corrective changes based on investigation findings |
| Change Enablement | Controls authorization, implementation, and review |
| Monitoring and Event Management | Supports implementation monitoring and validation |
| Service Configuration Management | Maintains updated Configuration Item information |
| Information Security Management | Evaluates security implications of changes |
| Continual Improvement | Uses change outcomes to improve implementation practices |

---

## 23. Related Procedures and Documentation

### Change Enablement

- [Change Enablement Overview](../README.md)
- [Change Authorization](Change-Authorization.md)
- [Change Template](../../Templates/Change-Template.md)

### Problem Management

- [Problem Management Overview](../../Problem-Management/)
- [Problem Identification](../../Problem-Management/Procedures/Problem-Identification.md)
- [Root Cause Analysis](../../Problem-Management/Procedures/Root-Cause-Analysis.md)
- [Known Error Management](../../Problem-Management/Procedures/Known-Error-Management.md)

### Incident Management

- [Incident Management Overview](../../Incident-Management/)
- [Incident Investigation](../../Incident-Management/Procedures/Incident-Investigation.md)
- [Incident Resolution](../../Incident-Management/Procedures/Incident-Resolution.md)

### Knowledge Management

- [Knowledge Management Overview](../../Knowledge-Management/)
- [Knowledge Article Lifecycle](../../Knowledge-Management/Procedures/Knowledge-Article-Lifecycle.md)

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Service Request Management](../../Service-Request-Management/)
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

## 24. Procedure Review

This procedure should be reviewed when:

- Change implementation responsibilities change.
- New infrastructure technologies are introduced.
- Authorization requirements are updated.
- Implementation tools change.
- Recovery procedures are modified.
- Security requirements change.
- Change-related incidents increase.
- Validation requirements are updated.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Change Implementation procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee requests, organizational roles, business impact assessments, change schedules, approvals, and implementation scenarios may be simulated.

Technical modifications, diagnostic commands, infrastructure configurations, validation results, and rollback activities are documented based on hands-on lab work where indicated.

Planned implementation steps must not be represented as completed technical actions.

Simulated approvals do not constitute authorization to modify systems outside the learner's controlled environment.

GitHub publication does not imply independent technical approval, production deployment, or organizational authorization.

This procedure demonstrates ITIL-aligned Change Enablement, controlled implementation, technical validation, rollback planning, operational documentation, and continual improvement practices rather than employment experience within an actual production organization.
