# CHG-XXX — Change Title

## Change Information

| Field | Details |
|---|---|
| **Change ID** | CHG-XXX |
| **Change Title** | [Brief description of the proposed change] |
| **Organization** | Technical Techno Tech |
| **Requested By** | [Employee / IT Administrator / Department] |
| **Assigned To** | [Systems Administrator / Network Administrator / Endpoint Administrator] |
| **Date Submitted** | YYYY-MM-DD HH:MM |
| **Scheduled Implementation** | YYYY-MM-DD HH:MM or TBD |
| **Date Completed** | YYYY-MM-DD HH:MM or Pending |
| **Status** | Proposed / Assessing / Awaiting Authorization / Scheduled / Implementing / Reviewing / Completed / Cancelled |
| **Change Type** | Standard / Normal / Emergency |
| **Risk Level** | Low / Medium / High |
| **Affected Service** | [IT-SVC-XXX — Service Name] |
| **Related Scenario** | [SCN-XXX](path-to-scenario) or N/A |
| **Ticket Reference** | [Jira Ticket ID / URL] or N/A |
| **Environment** | Simulated Enterprise |

---

## 1. Change Summary

### Change Description

[Describe the proposed modification to an IT service, system, infrastructure component, or configuration.]

Include:

- What is being changed?
- Which systems or services are affected?
- Who requested or initiated the change?
- Why is the change necessary?
- What is the expected outcome?

### Business Justification

[Explain the business requirement or operational need driving the change.]

### Change Objectives

- [Objective 1]
- [Objective 2]
- [Objective 3]

### Expected Outcome

[Describe the expected result of successfully implementing the change.]

---

## 2. Change Classification

### Change Type

**Selected Type:** [Standard / Normal / Emergency]

**Classification Justification:**

[Explain why the change falls into the selected category.]

### Change Type Definitions

- **Standard Change:** A low-risk, well-understood change that has been preauthorized and follows an established procedure.
- **Normal Change:** A change that requires assessment and authorization according to its risk, scope, and impact.
- **Emergency Change:** A change that must be implemented as soon as possible, typically to resolve a major incident or address a critical risk.

### Change Priority

**Priority:** [Low / Medium / High / Critical]

**Reason:** [Explain the business or operational urgency.]

---

## 3. Scope & Affected Services

### In Scope

- [System or configuration included]
- [Service or infrastructure component included]
- [Administrative activity included]

### Out of Scope

- [System or activity excluded]
- [System or activity excluded]

### Affected Systems

| System / Service | Identifier | Planned Modification |
|---|---|---|
| [Windows Server / AD DS / Microsoft 365 / etc.] | [Hostname / Service ID] | [Description] |
| [Workstation / Network Device / etc.] | [Hostname / Device ID] | [Description] |

### Relevant Infrastructure

- [Infrastructure Documentation](path-to-document)
- [Configuration Item](path-to-configuration-item)
- [Network or Service Documentation](path-to-document)

### Dependencies

[Identify other systems, services, or components that depend on the affected infrastructure.]

---

## 4. Risk & Impact Assessment

### Business Impact

[Describe how the change may affect employees, business operations, service availability, or security.]

### Technical Impact

[Describe the potential technical consequences of the change.]

### Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| [Risk 1] | Low / Medium / High | Low / Medium / High | [Mitigation] |
| [Risk 2] | Low / Medium / High | Low / Medium / High | [Mitigation] |
| [Risk 3] | Low / Medium / High | Low / Medium / High | [Mitigation] |

### Overall Risk Level

**Risk:** [Low / Medium / High]

**Justification:** [Explain the overall risk rating.]

### Expected Service Disruption

**Downtime Expected:** Yes / No

**Estimated Duration:** [Duration or N/A]

**Affected Users:** [Users / Departments / None]

### Security Considerations

[Describe any impact on authentication, authorization, data protection, or security controls.]

---

## 5. Change Authorization

### Authorization Requirements

**Authorization Required:** Yes / No — Preauthorized

**Change Authority:** [IT Manager / Systems Administrator / Change Authority / Emergency Change Authority]

### Authorization Record

| Field | Details |
|---|---|
| **Authorized By** | [Name / Role] |
| **Authorization Status** | Approved / Rejected / Pending / Preauthorized |
| **Authorization Date** | YYYY-MM-DD HH:MM or N/A |
| **Authorization Reference** | [Jira Approval / Simulated Approval / Standard Change Procedure] |

### Authorization Notes

[Document the authorization decision, conditions, or restrictions.]

**Important:** A standard change should reference its existing preauthorization rather than require a new approval for every execution.

For simulated approvals, clearly identify the approval as fictional.

---

## 6. Implementation Planning

### Prerequisites

- [Required administrative permissions]
- [Required system availability]
- [Required software, licenses, or resources]
- [Required backup or recovery capability]
- [Required coordination or notification]

### Implementation Schedule

| Field | Details |
|---|---|
| **Planned Start** | YYYY-MM-DD HH:MM |
| **Planned End** | YYYY-MM-DD HH:MM |
| **Maintenance Window** | [Scheduled Window / N/A] |
| **Implementation Owner** | [IT Role] |
| **Affected Stakeholders** | [Employees / Departments / IT Teams] |

### Implementation Plan

1. [Verify prerequisites and current system state]
2. [Prepare required configurations or resources]
3. [Perform the planned change]
4. [Verify successful implementation]
5. [Update relevant documentation]
6. [Notify affected stakeholders]

### Pre-Implementation Checks

| Check | Expected Result | Status |
|---|---|---|
| [Current configuration verified] | [Expected result] | Pass / Fail / Pending |
| [Dependencies available] | [Expected result] | Pass / Fail / Pending |
| [Recovery procedure verified] | [Expected result] | Pass / Fail / Pending |

---

## 7. Backout & Recovery Plan

### Backout Criteria

[Describe the conditions that would require reversing the change.]

Examples:

- The affected service becomes unavailable.
- Validation tests fail.
- Unexpected security or configuration issues occur.
- The change exceeds the approved impact or maintenance window.

### Backout Procedure

1. [Stop implementation safely]
2. [Restore the previous configuration or system state]
3. [Verify service functionality]
4. [Document the outcome]
5. [Notify affected stakeholders]

### Recovery Resources

- **Backup / Snapshot:** [Reference or N/A]
- **Previous Configuration:** [Location or Reference]
- **Recovery Tools:** [Tools Required]
- **Estimated Recovery Time:** [Duration or Unknown]

### Backout Limitations

[Document any irreversible actions, dependencies, or limitations.]

**Note:** A virtual machine snapshot is not always a safe recovery method for every workload. For example, domain controllers require supported Active Directory backup and recovery procedures.

---

## 8. Change Implementation

Document the technical work performed during the approved implementation.

### Implementation Log

| Date / Time | Action Performed | Result |
|---|---|---|
| YYYY-MM-DD HH:MM | [Action] | [Result] |
| YYYY-MM-DD HH:MM | [Action] | [Result] |
| YYYY-MM-DD HH:MM | [Action] | [Result] |

### Technical Implementation

[Describe the actual configuration changes, commands, administrative actions, or deployments performed.]

### Commands & Tools Used

```powershell
# Include actual commands used during implementation.
# Replace these placeholders with the commands performed.
```

### Configuration Changes

| Configuration Item | Previous State | New State |
|---|---|---|
| [Setting / Policy / Service] | [Previous value] | [New value] |
| [Setting / Policy / Service] | [Previous value] | [New value] |

### Deviations From Plan

[Document any unexpected changes to the approved implementation plan, or enter N/A.]

### Implementation Evidence

- [Before Configuration](Evidence/before-configuration.png)
- [Implementation Output](Evidence/implementation-output.txt)
- [After Configuration](Evidence/after-configuration.png)

Only include evidence collected during actual implementation.

---

## 9. Validation & Testing

### Post-Implementation Testing

| Test | Expected Result | Actual Result | Status |
|---|---|---|---|
| [Test 1] | [Expected behavior] | [Observed behavior] | Pass / Fail |
| [Test 2] | [Expected behavior] | [Observed behavior] | Pass / Fail |
| [Test 3] | [Expected behavior] | [Observed behavior] | Pass / Fail |

### Service Availability Verification

**Affected Services Operational:** Yes / No / Partially

**Unexpected Service Disruption:** Yes / No

**Details:** [Describe any unexpected behavior.]

### Security Verification

[Document any relevant access control, authentication, or security validation.]

### Business Requirement Verification

**Business Requirement Met:** Yes / No / Partially

**Validation Summary:**

[Explain how the results demonstrate whether the change achieved its objectives.]

---

## 10. Backout Execution

**Backout Required:** Yes / No

### Backout Actions

[Document the recovery actions performed, or enter N/A.]

### Backout Results

| Test | Expected Result | Actual Result | Status |
|---|---|---|---|
| [Recovery Test] | [Expected behavior] | [Observed behavior] | Pass / Fail / N/A |

### Final System State

[Describe the final system configuration following implementation or recovery.]

---

## 11. Communication & Coordination

### Stakeholder Communication

| Date / Time | Recipient | Communication | Method |
|---|---|---|---|
| YYYY-MM-DD HH:MM | [Affected Department] | [Planned change notification] | [Jira / Email / Chat] |
| YYYY-MM-DD HH:MM | [IT Team] | [Implementation update] | [Jira / Email / Chat] |
| YYYY-MM-DD HH:MM | [Stakeholders] | [Completion notification] | [Jira / Email / Chat] |

### Coordination Notes

[Document any technical coordination, scheduling decisions, or stakeholder concerns.]

---

## 12. Post-Implementation Review

### Implementation Outcome

**Outcome:** Successful / Partially Successful / Failed / Rolled Back

### Objectives Achieved

| Objective | Achieved | Evidence |
|---|---|---|
| [Objective 1] | Yes / No / Partially | [Reference] |
| [Objective 2] | Yes / No / Partially | [Reference] |

### Actual vs. Planned Results

| Item | Planned | Actual |
|---|---|---|
| Implementation Duration | [Duration] | [Duration] |
| Service Downtime | [Duration] | [Duration] |
| Configuration Outcome | [Expected State] | [Actual State] |

### Unexpected Issues

- [Unexpected issue or complication]
- [Enter None if applicable]

### Review Findings

[Summarize the effectiveness of the change, whether its objectives were achieved, and any follow-up work required.]

---

## 13. Related Records & Documentation

### Related Operational Records

- **Scenario:** [SCN-XXX](path-to-scenario) or N/A
- **Incident:** [INC-XXX](path-to-incident) or N/A
- **Problem:** [PRB-XXX](path-to-problem) or N/A
- **Service Request:** [SR-XXX](path-to-request) or N/A

### Knowledge Articles

- [KB-XXX — Knowledge Article](path-to-article)

### Infrastructure Documentation

- [Configuration Item](path-to-configuration-item)
- [Infrastructure Documentation](path-to-document)

### Documentation Updates

[Describe any configuration records, procedures, knowledge articles, or infrastructure documentation updated after implementation.]

---

## 14. Lessons Learned

### What Went Well

- [Successful technical implementation or planning activity]

### Challenges Encountered

- [Technical difficulty or unexpected behavior]

### What I Learned

- [Technical concept reinforced]
- [Change planning or risk assessment insight]
- [IT service management principle applied]

### Skills Practiced

- [Windows Server / Active Directory / Microsoft 365 / Networking / etc.]
- [PowerShell / Group Policy / Intune / Azure / etc.]
- [Change risk assessment]
- [Implementation planning and validation]
- [Change documentation and review]

### Improvement Opportunities

- [Potential procedure improvement]
- [Potential automation]
- [Potential monitoring enhancement]
- [Potential risk reduction]

---

## 15. Change Closure

| Field | Details |
|---|---|
| **Final Status** | Completed / Failed / Rolled Back / Cancelled |
| **Change Authorized** | Yes / No / Preauthorized |
| **Implementation Completed** | Yes / No / Partially |
| **Validation Completed** | Yes / No |
| **Business Objectives Met** | Yes / No / Partially |
| **Backout Required** | Yes / No |
| **Post-Implementation Review Completed** | Yes / No / Not Required |
| **Related Records Updated** | Yes / No / N/A |
| **Closure Date** | YYYY-MM-DD HH:MM |

### Final Change Summary

[Provide a concise summary of the change, its business justification, implementation results, validation, and final outcome.]

### Outstanding Actions

- [Remaining follow-up task]
- [Enter None if applicable]

---

## Simulation Disclaimer

This change record represents simulated IT operations within Technical Techno Tech, a fictional technology solutions company.

Technical implementation, configuration changes, testing, and validation are documented based on hands-on work performed in controlled lab environments.

Business requirements, change authorities, approvals, maintenance windows, and stakeholder communications may be simulated for educational and portfolio purposes.
