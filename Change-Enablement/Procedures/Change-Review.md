# SOP — Change Review

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Change Enablement  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-CE-003  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Change Enablement

---

## 1. Purpose

This procedure establishes a standardized method for reviewing changes after implementation within Technical Techno Tech.

Change Review evaluates whether an implemented change achieved its intended objectives, remained within its authorized scope, introduced unexpected issues, and maintained acceptable service functionality.

The procedure also identifies opportunities to improve future change planning, authorization, implementation, validation, and recovery activities.

The procedure supports:

- Verification of change outcomes
- Evaluation of implementation effectiveness
- Identification of change-related incidents
- Review of technical and business impact
- Assessment of rollback effectiveness
- Confirmation of documentation updates
- Identification of unresolved risks
- Improved change success rates
- Accurate change closure
- Continual improvement

**Key Principle:** A completed implementation does not automatically mean a change was successful. The actual outcome must be evaluated against the approved objectives and success criteria.

---

## 2. Scope

This procedure applies to changes affecting Technical Techno Tech's internal IT services and supporting infrastructure.

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

Change reviews may involve:

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

### Applicable Change Types

This procedure may be applied to:

- Standard changes
- Normal changes
- Emergency changes

The depth of review should reflect the change's risk, complexity, business impact, and outcome.

Not every low-risk standard change requires a formal meeting or extensive Post-Implementation Review.

---

## 3. ITIL 4 Change Enablement

### Purpose

The purpose of Change Enablement is to maximize the number of successful service and product changes by ensuring that risks have been properly assessed, authorizing changes to proceed, and managing the change schedule.

### Important Definitions

**Change:** The addition, modification, or removal of anything that could have a direct or indirect effect on services.

**Change Authorization:** The decision permitting a proposed change to proceed under defined conditions.

**Change Implementation:** The controlled execution of an authorized modification.

**Post-Implementation Review (PIR):** An evaluation of a change after implementation to determine its outcome, effectiveness, impact, and lessons learned.

**Rollback / Backout:** Actions taken to return to an acceptable previous state following an unsuccessful implementation.

**Change-Related Incident:** An incident associated with a change, where the relationship may require investigation before causation is established.

### Change Implementation vs. Change Review

| Change Implementation | Change Review |
|---|---|
| Executes the authorized modification | Evaluates the implementation outcome |
| Follows technical implementation steps | Compares results with approved objectives |
| Performs immediate validation | Assesses overall effectiveness and stability |
| Documents technical actions | Identifies lessons learned |
| May initiate rollback | Evaluates rollback outcomes |
| Updates implementation status | Determines closure readiness |

A change review should consider both technical results and the effect on service delivery.

---

## 4. Change Review Principles

Technical Techno Tech follows these principles during Change Review.

### 4.1 Evidence-Based Evaluation

Review findings must be supported by implementation records, validation results, monitoring data, or other relevant evidence.

### 4.2 Compare Expected and Actual Results

Evaluate the actual outcome against the original business justification and approved success criteria.

### 4.3 Review the Entire Change Lifecycle

Consider planning, authorization, implementation, validation, recovery, and communication.

### 4.4 Identify Unintended Consequences

Review whether the change introduced unexpected service disruptions, performance issues, or security risks.

### 4.5 Maintain Accountability

Document responsibilities, decisions, findings, and required follow-up actions.

### 4.6 Support Blameless Improvement

Focus on technical, procedural, and organizational conditions rather than assigning personal blame.

### 4.7 Preserve Traceability

Link review findings to relevant incidents, problems, Configuration Items, and improvement records.

### 4.8 Validate Before Closure

Do not close a change as successful without sufficient evidence that the required objectives were achieved.

### 4.9 Record Uncertainty

If evidence is incomplete, document the limitation rather than assuming success.

---

## 5. Roles and Responsibilities

### Change Owner

Responsible for:

- Coordinating the review
- Collecting implementation evidence
- Confirming change objectives
- Evaluating the implementation outcome
- Identifying outstanding actions
- Updating the Change record

### Change Coordinator

Responsible for:

- Determining applicable review requirements
- Coordinating review activities
- Evaluating process compliance
- Tracking outstanding actions
- Confirming closure readiness
- Monitoring change performance trends

### Implementation Technician

Responsible for:

- Providing implementation records
- Explaining technical actions performed
- Presenting validation evidence
- Documenting unexpected issues
- Reporting rollback activities
- Identifying technical lessons learned

### Technical Reviewer

Responsible for:

- Evaluating technical results
- Reviewing configuration accuracy
- Assessing unresolved technical risks
- Confirming relevant validation requirements
- Recommending additional testing when necessary

### Service Owner

Responsible for:

- Evaluating service functionality
- Reviewing business impact
- Confirming relevant operational requirements
- Identifying unresolved service issues

### Information Security Personnel

Responsible for:

- Reviewing security-sensitive changes
- Evaluating security validation results
- Identifying new or remaining security risks
- Recommending corrective actions

### Service Desk

Responsible for:

- Providing related incident information
- Reporting employee feedback
- Identifying recurring issues following changes
- Supporting communication and follow-up

### Change Authority

Responsible for:

- Reviewing significant outcomes when required
- Evaluating deviations from approved conditions
- Determining whether further authorization is needed
- Supporting decisions involving unresolved high-risk issues

**Lab Note:** These roles represent simulated organizational responsibilities. A single learner may perform multiple roles during a controlled lab exercise.

---

## 6. Change Review Requirements

A Change Review should evaluate the following information.

| Requirement | Description |
|---|---|
| Change ID | Unique change identifier |
| Change Type | Standard, Normal, or Emergency |
| Business Justification | Original reason for the change |
| Approved Objectives | Intended outcomes |
| Authorization | Applicable approval decision |
| Approved Scope | Authorized modification boundaries |
| Implementation Results | Actual technical actions and outcomes |
| Validation Evidence | Results of technical and functional testing |
| Service Impact | Actual operational consequences |
| Security Impact | Relevant security findings |
| Schedule Performance | Planned versus actual timing |
| Rollback Results | Recovery actions, if applicable |
| Related Incidents | Issues potentially associated with the change |
| Outstanding Risks | Unresolved technical or business concerns |
| Lessons Learned | Opportunities for improvement |
| Closure Recommendation | Whether the change is ready for closure |

---

## 7. Change Review Types

Technical Techno Tech uses a proposed risk-based review approach.

### 7.1 Routine Review

Appropriate for successful, low-risk standard changes.

May involve:

- Automated or manual validation checks
- Implementation record review
- Confirmation of expected results
- Exception tracking
- Documentation completion

### 7.2 Formal Post-Implementation Review

Appropriate for changes involving:

- Moderate or high risk
- Significant infrastructure modifications
- Multiple affected services
- Complex implementation activities
- Important business dependencies

May involve a documented review with relevant technical and service stakeholders.

### 7.3 Failed Change Review

Required when an implementation:

- Fails to achieve required objectives
- Introduces significant service disruption
- Requires rollback
- Produces unacceptable security or operational consequences

### 7.4 Emergency Change Review

Evaluates:

- Whether emergency classification was justified
- Whether appropriate authorization was obtained
- Whether the response addressed the urgent condition
- Whether additional risks were introduced
- Whether retrospective documentation is complete
- Whether permanent corrective actions remain necessary

### Proposed Review Matrix

| Change Type / Outcome | Suggested Review |
|---|---|
| Successful Standard Change | Routine review |
| Successful Low-Risk Normal Change | Documented outcome review |
| Medium- or High-Risk Normal Change | Formal PIR |
| Failed Change | Formal PIR |
| Rolled-Back Change | Formal PIR |
| Emergency Change | Formal retrospective review |

These are proposed internal standards, not mandatory ITIL 4 requirements.

---

## 8. Change Review Lifecycle

```text
Change Implementation Completed
              |
              v
    Collect Change Evidence
              |
              v
    Review Approved Objectives
              |
              v
    Evaluate Actual Results
              |
              v
    Review Service and Security
             Impact
              |
              v
    Evaluate Incidents / Rollback
              |
              v
    Identify Outstanding Issues
              |
              v
    Document Lessons Learned
              |
              v
    Determine Follow-Up Actions
              |
              v
      Closure Criteria Met?
              |
         +----+----+
         |         |
        Yes        No
         |         |
         v         v
    Complete     Assign and
     Review      Track Actions
         |         |
         v         v
    Close Change  Continue Review
                   or Escalate
```

A change may remain open while required follow-up actions or validation activities are incomplete.

---

## 9. Change Review Procedure

### Step 1 — Open the Change Record

Locate the implemented Change record.

Review:

- Change ID
- Change title
- Change type
- Requester
- Change owner
- Approved scope
- Business justification
- Authorization decision
- Implementation plan
- Validation plan
- Rollback plan
- Implementation status

**Expected Result:** The reviewer understands the original change requirements.

### Step 2 — Confirm Implementation Status

Determine the actual implementation outcome.

Possible statuses include:

- Successful
- Successful With Issues
- Partially Successful
- Failed
- Rolled Back
- Inconclusive

#### Example

```text
Change ID: CHG-001

Implementation Status:
Successful With Issues

Outstanding Issue:
Additional workstation validation required
```

Do not assume success solely because implementation steps were completed.

**Expected Result:** The actual implementation status is identified.

### Step 3 — Review Original Change Objectives

Identify the intended outcomes.

Questions:

1. Why was the change requested?
2. What business requirement did it address?
3. What technical condition was expected to change?
4. What success criteria were approved?
5. What services were expected to benefit?

#### Example

**Change:** Correct DHCP DNS configuration.

**Objective:** Ensure affected workstations receive approved internal DNS server addresses.

**Expected Benefit:** Improve domain controller discovery and reduce authentication failures.

**Expected Result:** Original objectives are documented for comparison.

### Step 4 — Review Authorization and Scope Compliance

Verify that the implementation remained within the authorized scope.

Review:

- Approved systems
- Approved configuration modifications
- Authorization conditions
- Implementation window
- Required technical reviews
- Security requirements

#### Example

**Approved Scope:** Modify DNS options for one DHCP scope.

**Actual Implementation:** Confirm which scopes were modified using implementation evidence.

If additional scopes were modified without authorization, record the deviation and assess its consequences.

**Expected Result:** Authorization and scope compliance are evaluated.

### Step 5 — Review Implementation Documentation

Examine the implementation log.

Verify:

- Actual start time
- Actual completion time
- Systems modified
- Technical actions performed
- Unexpected issues
- Implementation deviations
- Recovery activities
- Supporting evidence

### Example

```text
IMPLEMENTATION REVIEW

Change ID:

Approved Implementation Steps:

Actual Steps Performed:

Deviations:

Unexpected Issues:

Implementation Outcome:

Evidence References:
```

**Expected Result:** The review is supported by documented implementation activities.

### Step 6 — Compare Expected and Actual Results

Evaluate whether the change achieved its approved objectives.

| Evaluation Area | Expected Result | Actual Result |
|---|---|---|
| Configuration | Approved settings applied | Record observed settings |
| Functionality | Required service works | Record functional test result |
| Security | Required controls remain effective | Record security validation |
| Stability | No unacceptable degradation | Record monitoring findings |
| Business Outcome | Intended requirement satisfied | Record service owner feedback |

Do not complete the Actual Result column without evidence.

**Expected Result:** Differences between planned and actual outcomes are identified.

### Step 7 — Review Technical Validation

Review the diagnostic evidence collected after implementation.

### Example — DNS Configuration

```powershell
Get-DnsClientServerAddress -AddressFamily IPv4
```

### Example — DNS Resolution

```powershell
nslookup dc01.homelab.local
```

### Example — Domain Controller Discovery

```powershell
nltest /dsgetdc:homelab.local
```

### Example — Active Directory Health

```powershell
dcdiag /q
```

### Example — Replication Health

```powershell
repadmin /replsummary
```

Only use tests relevant to the affected systems and approved objectives.

**Expected Result:** Technical success criteria are evaluated using actual diagnostic evidence.

### Step 8 — Review Functional Validation

Confirm that the affected service works as intended.

#### Examples

| Change | Functional Validation |
|---|---|
| DNS Configuration | Required internal names resolve |
| Active Directory | Authorized users authenticate |
| Group Policy | Intended policy applies correctly |
| Software Deployment | Application launches and functions |
| Firewall Rule | Required traffic is permitted without unintended access |
| Network Routing | Required network destinations are reachable |
| Microsoft 365 | Intended user workflow functions |

Technical configuration accuracy does not automatically establish functional success.

**Expected Result:** Relevant service functionality is evaluated.

### Step 9 — Review Security Impact

Determine whether the change affected applicable security controls.

Review:

- Authentication requirements
- Authorization permissions
- Administrative access
- Firewall rules
- Endpoint protection
- Audit logging
- Data access
- Network segmentation

#### Example

A firewall change successfully permits an approved application connection.

However, the review should also confirm that the rule does not unintentionally permit unrelated traffic.

**Expected Result:** Relevant security implications are documented.

### Step 10 — Evaluate Service Impact

Compare anticipated and actual service impact.

Review:

1. Number of affected users
2. Actual downtime
3. Service degradation
4. Unexpected interruptions
5. Availability of alternatives
6. Employee feedback
7. Business process impact

### Example

| Impact Area | Planned | Actual |
|---|---|---|
| Downtime | No planned outage | To Be Determined |
| Affected Users | Test workstation only | To Be Determined |
| Service Degradation | None expected | To Be Determined |
| Business Disruption | Minimal | To Be Determined |

**Expected Result:** Actual service impact is documented.

### Step 11 — Review Change-Related Incidents

Determine whether incidents occurred during or after implementation.

Review:

- Incident timestamps
- Affected services
- Reported symptoms
- Configuration changes
- Diagnostic evidence
- Resolution methods

### Important Distinction

An incident occurring after a change does not automatically prove that the change caused it.

Investigate the relationship before recording a confirmed causal connection.

#### Example

A workstation experiences authentication failures shortly after a DNS configuration change.

The review should determine whether the change contributed to the failure.

**Expected Result:** Relevant incidents are documented and appropriately linked.

### Step 12 — Review Rollback Activities

If rollback occurred, evaluate:

- Why rollback was initiated
- Whether the approved procedure was followed
- Whether recovery succeeded
- Whether services returned to an acceptable state
- Whether additional incidents occurred
- Whether the rollback plan requires improvement

### Example

```text
ROLLBACK REVIEW

Rollback Required:
Reason:
Decision Authority:
Actions Performed:
Recovery Outcome:
Validation Results:
Outstanding Issues:
```

**Expected Result:** Recovery effectiveness is assessed.

### Step 13 — Review Implementation Schedule

Compare planned and actual timing.

Review:

- Planned start time
- Actual start time
- Planned completion time
- Actual completion time
- Maintenance window adherence
- Delays
- Scheduling conflicts

#### Example

**Planned Duration:** 30 minutes

**Actual Duration:** 45 minutes

**Variance:** 15 minutes

The reviewer should determine whether the difference created an operational issue.

**Expected Result:** Schedule performance is documented.

### Step 14 — Review Communication Effectiveness

Determine whether relevant stakeholders received appropriate information.

Review:

- Pre-change notification
- Implementation start communication
- Service disruption updates
- Rollback communication
- Completion notification
- Outstanding issue communication

### Review Questions

1. Were affected stakeholders informed?
2. Were communications accurate?
3. Were unexpected issues communicated promptly?
4. Were support teams prepared?
5. Were communication responsibilities clear?

**Expected Result:** Communication effectiveness is evaluated.

### Step 15 — Identify Outstanding Issues

Document unresolved conditions.

Examples:

- Incomplete validation
- Remaining configuration inconsistencies
- Recurring service errors
- Pending documentation updates
- Unresolved security concerns
- Follow-up monitoring requirements

### Example

```text
OUTSTANDING ISSUES

Issue ID:
Description:
Business Impact:
Technical Risk:
Responsible Owner:
Required Action:
Target Review Date:
```

**Expected Result:** Outstanding issues are traceable.

### Step 16 — Identify Lessons Learned

Review what worked and what should improve.

### Review Categories

**Planning**

- Were prerequisites identified?
- Was the implementation scope accurate?
- Were dependencies understood?

**Authorization**

- Was the risk assessment appropriate?
- Were required conditions identified?
- Was the correct change authority used?

**Implementation**

- Were instructions clear?
- Were technical steps accurate?
- Were unexpected issues handled appropriately?

**Validation**

- Were success criteria sufficient?
- Were tests performed correctly?
- Were service dependencies checked?

**Recovery**

- Was the rollback plan practical?
- Were recovery resources available?
- Were recovery steps documented?

**Communication**

- Were stakeholders informed?
- Were updates timely and accurate?

**Expected Result:** Actionable lessons learned are documented.

### Step 17 — Recommend Corrective or Improvement Actions

Identify actions necessary to address review findings.

Examples:

- Update implementation procedures
- Improve pre-change validation
- Revise rollback instructions
- Add monitoring checks
- Update technical documentation
- Improve authorization criteria
- Create a Problem record
- Submit a new Change request
- Register a continual improvement opportunity

### Example

**Finding:** The implementation plan did not include verification of a dependent DNS server.

**Improvement:** Add dependency validation to future DNS-related change procedures.

**Expected Result:** Review findings produce actionable recommendations.

### Step 18 — Assign Follow-Up Ownership

Each required follow-up action should identify:

- Action description
- Responsible owner
- Priority
- Target completion date
- Related record
- Completion criteria

#### Example

| Action | Owner | Status |
|---|---|---|
| Update DNS change checklist | Systems Administration | Proposed |
| Review monitoring requirements | Infrastructure Team | Proposed |
| Update Knowledge Base article | Knowledge Management | Proposed |

These assignments are illustrative.

**Expected Result:** Required follow-up activities have clear ownership.

### Step 19 — Determine Closure Readiness

Review whether the change can be closed.

### Proposed Closure Criteria

- Implementation outcome documented
- Required validation completed
- Actual service impact assessed
- Security requirements reviewed
- Relevant incidents linked
- Rollback outcome documented when applicable
- Required documentation updated
- Outstanding actions assigned or resolved
- Required review completed
- Closure decision recorded

### Closure Decision

| Decision | Description |
|---|---|
| Ready for Closure | Required review and documentation are complete |
| Closure With Follow-Up | Closure permitted under policy with separately tracked outstanding actions |
| Further Validation Required | Additional evidence is needed |
| Additional Remediation Required | Technical issues remain unresolved |
| Escalation Required | Significant risk or unresolved service impact requires further action |

A failed or rolled-back change may still be administratively closed after its outcome is accurately recorded and required follow-up work is assigned.

**Expected Result:** Closure readiness is determined.

### Step 20 — Complete the Review Record

Document:

- Change ID
- Review date
- Review participants or method
- Implementation outcome
- Objective achievement
- Service impact
- Security impact
- Related incidents
- Rollback outcome
- Lessons learned
- Follow-up actions
- Closure recommendation

**Expected Result:** The review is complete and traceable.

### Step 21 — Update the Change Status

Update the Change record according to the review outcome.

### Proposed Statuses

- Implemented — Pending Review
- Review in Progress
- Pending Additional Validation
- Follow-Up Required
- Closed — Successful
- Closed — Successful With Issues
- Closed — Failed
- Closed — Rolled Back
- Closed — Inconclusive

The status must reflect the actual outcome.

**Expected Result:** The Change record accurately represents its lifecycle state.

---

## 10. Standard Change Review

Standard changes are preauthorized and follow established procedures.

### Review Objectives

- Confirm the standard change model was followed.
- Verify required validation.
- Identify exceptions.
- Detect recurring implementation issues.
- Confirm documentation completeness.

### Example

An approved routine software deployment completes successfully.

The review may consist of:

1. Confirming deployment completion.
2. Reviewing application functionality.
3. Checking for unexpected incidents.
4. Recording the outcome.
5. Escalating exceptions.

A formal meeting is not necessarily required.

---

## 11. Normal Change Review

Normal changes should be reviewed according to their risk and impact.

### Review Considerations

- Business justification
- Technical objectives
- Authorization conditions
- Implementation accuracy
- Service impact
- Security impact
- Validation results
- Rollback effectiveness
- Lessons learned

### Example

A domain-wide Group Policy change may require additional review because it can affect multiple systems and users.

The review should confirm that the intended policy applies correctly and that unintended systems were not affected.

---

## 12. Emergency Change Review

Emergency changes should receive retrospective evaluation.

### Review Objectives

1. Confirm the emergency condition.
2. Evaluate whether expedited authorization was appropriate.
3. Review the technical response.
4. Confirm service restoration or risk reduction.
5. Assess unexpected consequences.
6. Review recovery readiness.
7. Confirm required documentation.
8. Identify remaining corrective actions.

### Example

An urgent firewall change is implemented to reduce exposure to a critical security threat.

The review should determine:

- Whether the immediate risk was addressed
- Whether the rule matched the approved emergency scope
- Whether legitimate services were affected
- Whether additional permanent remediation is necessary

Emergency changes should not be exempt from accountability or review.

---

## 13. Failed Change Review

A failed change requires investigation of the unsuccessful outcome.

### Potential Causes

- Incomplete prerequisites
- Incorrect configuration
- Missing dependencies
- Inadequate testing
- Implementation errors
- Insufficient permissions
- Unexpected infrastructure behavior
- Incomplete rollback planning

These are potential causes, not automatic conclusions.

### Failed Change Review Procedure

1. Review the original change objectives.
2. Examine the implementation log.
3. Identify the point of failure.
4. Review technical evidence.
5. Assess business impact.
6. Review rollback actions.
7. Identify contributing factors.
8. Determine whether Problem Management investigation is required.
9. Document corrective recommendations.
10. Record the final outcome.

### Important

A failed change should not automatically be classified as a Problem record.

Problem Management is appropriate when further analysis of an actual or potential underlying cause is warranted.

---

## 14. Change Review Evidence

Review findings should be supported by appropriate evidence.

### Evidence Types

- Approved Change record
- Authorization documentation
- Implementation log
- Pre-change configuration
- Post-change configuration
- Diagnostic command output
- Functional validation results
- Security validation results
- Monitoring data
- Related incident records
- Rollback results
- Stakeholder feedback

### Example Directory

```text
Change-Enablement/
└── Records/
    └── CHG-001-DNS-Configuration-Update/
        ├── README.md
        └── Evidence/
            ├── 01-Pre-Change-Configuration.txt
            ├── 02-Implementation-Log.md
            ├── 03-Post-Change-Configuration.txt
            ├── 04-Validation-Results.md
            ├── 05-Service-Impact-Review.md
            └── 06-Post-Implementation-Review.md
```

These filenames represent a proposed structure.

### Evidence Standards

Each item should identify:

- Affected system
- Collection date and time
- Tool or method used
- Actual observed result
- Interpretation
- Related Change ID

Do not fabricate diagnostic output or validation results.

---

## 15. Post-Implementation Review Template

Use the following structure within the Change record or a supporting review document.

```text
POST-IMPLEMENTATION REVIEW

Change ID:
Change Title:
Change Type:
Change Owner:
Implementation Date:
Review Date:
Review Method:
Review Participants:

1. Original Business Justification

2. Approved Objectives

3. Approved Scope

4. Authorization Conditions

5. Implementation Summary

6. Planned vs. Actual Results

7. Technical Validation

8. Functional Validation

9. Security Validation

10. Stability Assessment

11. Actual Service Impact

12. Change-Related Incidents

13. Rollback / Recovery Review

14. Schedule Performance

15. Communication Review

16. Outstanding Issues

17. Lessons Learned

18. Corrective Actions

19. Improvement Recommendations

20. Follow-Up Ownership

21. Closure Recommendation

22. Final Change Status

23. Evidence References
```

---

## 16. Example Change Review Scenario

### Scenario — DHCP DNS Configuration Correction

**Change ID:** CHG-001  
**Change Type:** Normal  
**Affected Service:** IT-SVC-004 — Network Connectivity  
**Related Problem:** PRB-001  
**Environment:** homelab.local

### Business Context

Domain-joined workstations rely on internal DNS services for domain controller discovery.

A simulated Problem Management investigation identifies incorrect DNS server settings distributed through DHCP.

A change is proposed to correct the DHCP DNS options.

### Original Change Objective

Configure the affected DHCP scope to distribute the approved internal DNS server addresses.

### Approved DNS Server Design

| Server | IP Address |
|---|---|
| DC01 | 10.20.10.10 |
| DC02 | 10.20.10.11 |

Actual server availability and configuration must be verified.

### Proposed Review Requirements

The reviewer should confirm:

1. The correct DHCP scope was modified.
2. The approved DNS server addresses were configured.
3. A test workstation received the intended settings.
4. Internal DNS resolution succeeded.
5. Domain controller discovery succeeded.
6. Authorized domain authentication worked.
7. No unacceptable service impact occurred.
8. Implementation documentation was completed.

### Proposed Technical Validation

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

**Functional Validation**

Confirm successful authorized domain authentication.

### Proposed Review Matrix

| Review Area | Expected Result | Actual Result |
|---|---|---|
| Authorization | Appropriate authorization recorded | Pending |
| Scope Compliance | Correct DHCP scope modified | Not Verified |
| DNS Configuration | Approved DNS addresses distributed | Not Tested |
| DNS Resolution | Required internal records resolve | Not Tested |
| Domain Discovery | Domain controller located successfully | Not Tested |
| Authentication | Authorized sign-in succeeds | Not Tested |
| Service Impact | No unacceptable disruption | Not Assessed |
| Documentation | Change record completed | Pending |

### Potential Lessons Learned

The following are examples of possible findings, not actual conclusions:

- Improve pre-change DNS configuration validation.
- Add DHCP scope verification to the implementation checklist.
- Confirm both domain controller dependencies before implementation.
- Expand post-change authentication testing.
- Improve rollback documentation.

### Review Status

**Pending — Implementation and Validation Not Confirmed**

### Closure Recommendation

**Not Ready for Closure**

The review cannot establish success until actual implementation evidence and validation results are available.

**Scenario Status:** Illustrative Post-Implementation Review exercise. No implementation, approval, diagnostic result, or successful outcome is claimed.

---

## 17. Change Review and Problem Management

Change reviews may identify conditions requiring Problem Management.

### Examples

- Repeated change failures
- Recurring service disruptions
- Unexplained infrastructure behavior
- Persistent configuration defects
- Repeated rollback requirements

### Example Relationship

```text
Change: CHG-001

Review Finding:
Recurring DNS configuration failure

Potential Related Problem:
PRB-001
```

The relationship should be supported by evidence.

### Important Distinction

Change Review evaluates the change outcome.

Problem Management investigates actual or potential underlying causes of incidents.

A review finding may initiate or contribute to a Problem investigation without replacing it.

---

## 18. Change Review and Continual Improvement

Change Review provides information for improving future change activities.

### Improvement Opportunities

- More accurate risk assessments
- Better implementation checklists
- Improved technical validation
- Stronger rollback procedures
- Better scheduling coordination
- More effective communication
- Improved dependency documentation
- Reduced change-related incidents

### Example Improvement Record

```text
Improvement ID: IMP-001

Source:
Change Review

Finding:
Pre-change validation did not include all
relevant DNS dependencies.

Proposed Improvement:
Update the DNS change checklist to include
dependency validation.

Owner:
To Be Assigned

Status:
Proposed
```

Improvement records should be maintained through Continual Improvement when the finding warrants formal tracking.

---

## 19. Change Review Documentation Standards

Review records must distinguish:

### Planned Outcomes

What the change was intended to accomplish.

### Actual Outcomes

What was observed after implementation.

### Verified Findings

Conclusions supported by technical or operational evidence.

### Unverified Findings

Potential explanations or outcomes that have not been confirmed.

### Proposed Improvements

Recommended actions that have not yet been implemented.

### Completed Improvements

Actions that were actually performed and validated.

### Example

**Expected Result:** Domain controller discovery succeeds after correcting DNS configuration.

**Actual Result:** Not yet tested.

**Review Conclusion:** Insufficient evidence to confirm success.

Do not describe a change as successful without supporting validation.

---

## 20. Common Change Review Errors

### Error 1 — Closing Immediately After Implementation

**Incorrect:** Closing the change because the technical steps were completed.

**Correct:** Confirm the required validation and review criteria.

### Error 2 — Ignoring Business Outcomes

**Incorrect:** Evaluating only whether the configuration changed.

**Correct:** Determine whether the intended service improvement occurred.

### Error 3 — Missing Security Validation

**Incorrect:** Assuming the change preserved security controls.

**Correct:** Review relevant authentication, authorization, and security requirements.

### Error 4 — Ignoring Change-Related Incidents

**Incorrect:** Excluding incidents that occurred during implementation.

**Correct:** Review potentially related incidents and investigate causal relationships where necessary.

### Error 5 — Treating Rollback as Successful Implementation

**Incorrect:** Marking a rolled-back change as successfully implemented.

**Correct:** Record the actual implementation and recovery outcomes separately.

### Error 6 — Failing to Document Lessons Learned

**Incorrect:** Recording only that a change succeeded or failed.

**Correct:** Identify actionable improvements when relevant.

### Error 7 — Leaving Follow-Up Actions Unassigned

**Incorrect:** Documenting unresolved issues without ownership.

**Correct:** Assign and track required actions.

### Error 8 — Assuming Correlation Proves Causation

**Incorrect:** Concluding that every incident after implementation was caused by the change.

**Correct:** Evaluate evidence before confirming a causal relationship.

### Error 9 — Fabricating Review Results

**Incorrect:** Recording successful validation that was not performed.

**Correct:** Distinguish actual results from expected or hypothetical outcomes.

### Error 10 — Treating a Simulated Review as Independent Approval

**Incorrect:** Claiming a fictional Change Advisory Board completed a formal review.

**Correct:** Label simulated reviews and self-assessments accurately.

---

## 21. Change Review Quality Checklist

Before completing a Change Review, verify:

- [ ] Change record reviewed
- [ ] Change ID confirmed
- [ ] Change type identified
- [ ] Business justification reviewed
- [ ] Approved objectives documented
- [ ] Authorization conditions reviewed
- [ ] Approved scope compared with actual implementation
- [ ] Implementation log examined
- [ ] Actual implementation outcome recorded
- [ ] Technical validation reviewed
- [ ] Functional validation reviewed
- [ ] Security validation reviewed when applicable
- [ ] Stability assessed
- [ ] Business impact documented
- [ ] Change-related incidents reviewed
- [ ] Rollback results evaluated when applicable
- [ ] Planned and actual timing compared
- [ ] Communication effectiveness assessed
- [ ] Outstanding issues identified
- [ ] Lessons learned documented
- [ ] Corrective actions recommended when necessary
- [ ] Follow-up ownership assigned
- [ ] Configuration documentation reviewed
- [ ] Knowledge Base updates considered
- [ ] Problem Management requirements evaluated
- [ ] Continual Improvement opportunities identified
- [ ] Closure readiness determined
- [ ] Review method recorded
- [ ] Final status accurately documented

---

## 22. Change Review Performance Metrics

Change Review effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Change Success Rate | Measures changes achieving approved objectives |
| Failed Change Rate | Tracks unsuccessful changes |
| Rollback Rate | Measures changes requiring recovery |
| Change-Related Incident Rate | Tracks incidents associated with changes |
| PIR Completion Rate | Measures completion of required reviews |
| Average Review Completion Time | Tracks time needed to complete reviews |
| Change Schedule Adherence | Evaluates planned versus actual implementation timing |
| Authorization Compliance Rate | Measures adherence to approval requirements |
| Validation Completion Rate | Tracks required post-change testing |
| Repeat Change Failure Rate | Identifies recurring implementation weaknesses |
| Improvement Action Completion Rate | Tracks closure of identified improvements |
| Change Documentation Completeness | Measures quality of change records |

Metrics should be based on actual records or clearly labeled simulated datasets.

---

## 23. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Provides employee feedback and reports change-related incidents |
| Incident Management | Investigates and restores services disrupted by changes |
| Service Request Management | Provides feedback on changes affecting request fulfillment |
| Knowledge Management | Updates technical procedures and recovery guidance |
| Problem Management | Investigates recurring failures or underlying conditions identified during review |
| Change Enablement | Evaluates implementation outcomes and determines closure readiness |
| Monitoring and Event Management | Provides technical evidence and stability monitoring |
| Service Configuration Management | Confirms Configuration Item records reflect implemented changes |
| Information Security Management | Reviews security implications and unresolved risks |
| Continual Improvement | Tracks improvements identified through change reviews |

---

## 24. Related Procedures and Documentation

### Change Enablement

- [Change Enablement Overview](../README.md)
- [Change Authorization](Change-Authorization.md)
- [Change Implementation](Change-Implementation.md)
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
- [Incident Closure](../../Incident-Management/Procedures/Incident-Closure.md)

### Knowledge Management

- [Knowledge Management Overview](../../Knowledge-Management/)
- [Knowledge Article Lifecycle](../../Knowledge-Management/Procedures/Knowledge-Article-Lifecycle.md)

### ITIL Practices

- [Service Desk](../../01-Service-Desk/)
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

## 25. Procedure Review

This procedure should be reviewed when:

- Change review responsibilities change.
- New infrastructure technologies are introduced.
- Change authorization or implementation procedures are updated.
- Validation requirements change.
- Recovery procedures are modified.
- Change-related incidents increase.
- Security review requirements change.
- Review documentation issues are identified.
- Continual improvement activities identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Change Review procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Employee requests, organizational roles, business impact assessments, Change Advisory Board activities, review decisions, and operational scenarios may be simulated.

Technical implementations, diagnostic commands, infrastructure configurations, validation results, rollback activities, and review findings are documented based on hands-on lab work where indicated.

Expected results and hypothetical findings must not be represented as completed technical activities.

Simulated approvals and reviews do not constitute independent organizational authorization or validation.

GitHub publication does not imply production deployment, independent technical approval, or employment experience.

This procedure demonstrates ITIL-aligned Change Enablement, Post-Implementation Review, change outcome evaluation, operational risk assessment, technical documentation, and continual improvement practices.
