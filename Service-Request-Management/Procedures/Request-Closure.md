# SOP-SRM-004 — Request Closure

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Request Management  
**Document Type:** Standard Operating Procedure (SOP)  
**SOP ID:** SOP-SRM-004  
**Version:** 1.0  
**Status:** Draft — Proposed Operating Standard  
**Process Owner:** Internal IT  
**Primary Responsible Function:** Service Request Management  
**Effective Date:** Pending Adoption  
**Last Reviewed:** Not Yet Reviewed  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

# 1. Purpose

Establish a standardized procedure for reviewing, verifying, documenting, and formally closing employee IT service requests.

This procedure ensures that completed service requests are properly evaluated before closure and that all required technical results, authorization evidence, communications, and records are preserved.

The objectives are to:

- Confirm that the approved request has been fulfilled.
- Verify that fulfillment results meet the original requirements.
- Confirm that applicable authorization conditions were satisfied.
- Review technical verification evidence.
- Identify and document outstanding issues.
- Obtain requester confirmation when required.
- Communicate the final request outcome.
- Ensure request documentation is complete.
- Update related configuration and knowledge records where necessary.
- Assign an accurate closure classification.
- Maintain traceability for auditing and reporting.
- Support continual improvement through service request analysis.

**Key Principle:** A service request should be closed only when its final disposition has been established, required documentation is complete, and applicable closure conditions have been satisfied.

A request may be closed as successfully fulfilled, rejected, cancelled, or otherwise concluded according to the organization's approved workflow.

Closure does not always mean that the requested service was delivered.

---

# 2. Scope

## 2.1 In Scope

This procedure applies to service requests that have reached a final disposition or are ready for closure.

Examples include:

- Completed account creation requests
- Completed access permission requests
- Completed Microsoft 365 license assignments
- Completed software installation requests
- Completed device provisioning requests
- Completed employee onboarding requests
- Completed employee role changes
- Rejected service requests
- Cancelled service requests
- Requests withdrawn by employees
- Requests resolved through an approved alternative

## 2.2 Out of Scope

This procedure does not replace:

- Request logging
- Request assessment and authorization
- Technical fulfillment
- Incident resolution
- Problem investigation
- Change implementation
- Security incident response

These activities are governed by their respective procedures.

## 2.3 Supported Environments

Closure activities may reference work performed in:

- Active Directory Domain Services
- Windows Server
- Windows 11
- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Network infrastructure
- ITSM platforms

The closure procedure applies regardless of the technology used to fulfill the request.

---

# 3. ITIL 4 Alignment

This SOP supports the ITIL 4 Service Request Management practice.

Service Request Management aims to support agreed service quality by handling predefined, user-initiated service requests effectively and efficiently.

Request Closure establishes the final disposition of the request and preserves the information necessary for operational reporting and improvement.

## 3.1 Related ITIL Practices

| Practice | Relationship |
|---|---|
| Service Desk | Coordinates final communication and request closure |
| Service Request Management | Maintains request lifecycle records and closure standards |
| Knowledge Management | Uses fulfillment findings to improve technical guidance |
| Information Security Management | Supports verification of authorized access and security requirements |
| Service Configuration Management | Maintains accurate configuration information |
| Change Enablement | Confirms applicable change records are appropriately linked |
| Incident Management | Handles service interruptions identified during fulfillment |
| Problem Management | Investigates recurring fulfillment failures where appropriate |
| Continual Improvement | Analyzes closure quality, fulfillment performance, and recurring issues |

## 3.2 Practice Boundaries

Service Request Management owns the request's final disposition.

Technical verification may be performed by the fulfillment technician.

Requester communication may be coordinated through the Service Desk.

Configuration documentation may be maintained through Service Configuration Management.

These responsibilities may be performed by the same authorized IT personnel depending on organizational structure.

### Important

Closing a service request does not automatically close associated incidents, problems, or changes.

Each related record follows its own applicable lifecycle.

---

# 4. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Requester | Confirms the delivered service when required |
| Service Desk Technician | Reviews closure readiness and communicates the outcome |
| Request Owner | Ensures the request record is complete and accurately closed |
| Fulfillment Technician | Provides technical completion and verification evidence |
| IT Administrator | Confirms specialized technical results when necessary |
| Service Owner | Defines applicable service completion requirements |
| Resource Owner | Confirms resource-specific conditions where required |
| Reviewer | Performs independent verification when required |
| Security Administrator | Reviews security-sensitive fulfillment when necessary |

## 4.1 Request Owner Responsibilities

The request owner should:

1. Review the fulfillment outcome.
2. Confirm that the required work is complete.
3. Verify that evidence is available.
4. Identify outstanding issues.
5. Confirm applicable authorization conditions.
6. Review requester communication.
7. Determine the appropriate closure classification.
8. Update the request record.
9. Close the request.
10. Preserve relevant documentation.

## 4.2 Fulfillment Technician Responsibilities

The fulfillment technician should provide:

- A summary of work performed
- The affected systems or resources
- Technical verification results
- Relevant command output or screenshots
- Known limitations
- Outstanding technical issues
- Recovery actions, if applicable

## 4.3 Requester Responsibilities

When required, the requester should:

- Test the delivered service.
- Confirm whether the request meets the intended need.
- Report remaining issues.
- Provide clarification when necessary.

### Important

Requester confirmation is not mandatory for every service request.

The requirement depends on the service, organizational policy, and applicable fulfillment model.

---

# 5. Request Closure Principles

All closure activities should follow these principles.

## 5.1 Verified Outcomes

Successful fulfillment should be supported by appropriate technical or functional verification.

## 5.2 Accurate Classification

The closure reason must reflect the actual outcome.

## 5.3 Complete Documentation

Required request details, approvals, fulfillment actions, and verification results should be retained.

## 5.4 Traceability

The request should remain linked to relevant incidents, changes, configuration items, and knowledge articles.

## 5.5 Requester Communication

The requester should receive appropriate notification of the final disposition.

## 5.6 Security

Sensitive information must be protected throughout closure and record retention.

## 5.7 No Premature Closure

Requests should not be closed merely to reduce the number of open tickets.

## 5.8 Continual Improvement

Closure findings should inform improvements to request forms, technical instructions, and service delivery.

---

# 6. Request Closure Workflow

## 6.1 High-Level Workflow

```text
Fulfillment Completed
or Final Disposition Reached
            |
            v
Review Request Record
            |
            v
Confirm Final Outcome
            |
            v
Review Technical Verification
            |
            v
Are Outstanding Issues Present?
        /           \
       Yes           No
        |             |
        v             v
Assess Issues     Review Authorization
and Next Steps    and Documentation
        |             |
        v             v
Resolve, Escalate, Check Requester
or Document        Confirmation
Disposition           |
        |             v
        +----------> Update Related
                     Records
                        |
                        v
                  Assign Closure
                  Classification
                        |
                        v
                  Notify Requester
                        |
                        v
                  Complete Closure
                  Quality Review
                        |
                        v
                  Close Request
                        |
                        v
                  Retain Evidence
                        |
                        v
                  Review Improvement
                  Opportunities
```

## 6.2 Possible Closure Outcomes

| Outcome | Description |
|---|---|
| Fulfilled | Requested service successfully delivered |
| Fulfilled with Approved Alternative | An authorized alternative satisfied the business requirement |
| Rejected | Request was not authorized |
| Cancelled | Request was withdrawn or cancelled |
| Duplicate | Request was confirmed as a duplicate of another record |
| Not Fulfilled | Request concluded without successful delivery under an approved disposition |
| Other | An approved closure reason not covered above |

## 6.3 Closure Requirements

Before closure:

- The final disposition must be known.
- Required evidence must be documented.
- Outstanding work must be resolved or appropriately transferred.
- Relevant stakeholders must be informed.
- The request record must accurately reflect the outcome.

### Important

A request that remains blocked or partially fulfilled should generally remain open unless an approved process establishes a valid final disposition.

---

# 7. Step 1 — Review the Request Record

## 7.1 Objective

Confirm that the request contains sufficient information to evaluate its final outcome.

## 7.2 Required Information

| Field | Requirement |
|---|---|
| Request ID | Required |
| Requester | Required |
| Requested Service | Required |
| Service Category | Required |
| Request Owner | Required |
| Authorization Status | When applicable |
| Approved Scope | When applicable |
| Fulfillment Outcome | Required for fulfilled requests |
| Verification Results | Required for fulfilled requests |
| Outstanding Issues | When applicable |
| Current Status | Required |

## 7.3 Procedure

1. Open the service request record.
2. Confirm the request identifier.
3. Review the original request.
4. Review the approved fulfillment scope.
5. Review authorization records.
6. Review fulfillment notes.
7. Identify the final outcome.
8. Identify missing documentation.
9. Determine whether closure review can continue.

## 7.4 Incomplete Records

If required information is missing:

1. Identify the missing information.
2. Contact the responsible technician or request owner.
3. Obtain available supporting evidence.
4. Update the request record.
5. Document any unresolved evidence limitations.
6. Determine whether closure requirements are satisfied.

### Important

Do not invent missing technical results or approval evidence to complete a request record.

---

# 8. Step 2 — Confirm the Fulfillment Outcome

## 8.1 Objective

Determine whether the requested service was delivered within the approved scope.

## 8.2 Fulfillment Review

| Assessment Item | Status | Notes |
|---|---|---|
| Approved Work Completed | Pending | [Details] |
| Correct User or Resource | Pending | [Details] |
| Approved Permissions Applied | Pending | [Details] |
| Required Service Available | Pending | [Details] |
| Fulfillment Conditions Satisfied | Pending | [Details] |
| Unintended Changes Identified | Pending | [Details] |

## 8.3 Procedure

1. Identify the original request.
2. Review the authorized scope.
3. Compare the approved work with the documented actions.
4. Determine whether all required tasks were completed.
5. Identify any deviations.
6. Confirm the final fulfillment status.
7. Document the outcome.

## 8.4 Completion Criteria

A successfully fulfilled request should meet the applicable criteria:

- Correct service delivered
- Correct user or resource affected
- Approved scope followed
- Required technical work completed
- Applicable security requirements satisfied
- Technical verification completed
- No unresolved issues preventing the intended service

### Important

A request should not be classified as successfully fulfilled when essential approved work remains incomplete.

---

# 9. Step 3 — Review Technical Verification

## 9.1 Objective

Confirm that fulfillment results were verified using appropriate methods.

## 9.2 Verification Methods

| Method | Example |
|---|---|
| Configuration Inspection | Review Active Directory group membership |
| Functional Testing | Confirm shared folder access |
| Administrative Portal | Verify Microsoft 365 license assignment |
| PowerShell | Query the resulting configuration |
| Endpoint Verification | Confirm software installation |
| Network Testing | Verify approved connectivity |
| Requester Confirmation | Confirm the service works for the employee |
| Independent Review | Validate sensitive or higher-risk fulfillment |

## 9.3 Procedure

1. Review the expected result.
2. Identify the verification method used.
3. Review the recorded observations.
4. Confirm that the correct target was evaluated.
5. Determine whether the result satisfies the request.
6. Identify verification limitations.
7. Record the conclusion.

## 9.4 Verification Record

**Request ID:** SR-###

**Expected Result:** [Description]

**Verification Method:** [Method]

**Actual Result:** Not Yet Verified

**Verification Date:** Pending

**Verified By:** [Role]

**Evidence Reference:** Not Available

**Verification Status:** Pending

## 9.5 Verification Checklist

- [ ] Expected result identified
- [ ] Appropriate verification method used
- [ ] Correct target verified
- [ ] Actual result documented
- [ ] Approved scope confirmed
- [ ] Errors or limitations recorded
- [ ] Evidence retained

### Important

A command completing successfully does not necessarily demonstrate that the requested service works.

Where appropriate, functional verification should supplement configuration inspection.

---

# 10. Step 4 — Review Outstanding Issues

## 10.1 Objective

Identify unresolved problems, incomplete tasks, or unexpected results that may prevent closure.

## 10.2 Potential Outstanding Issues

- Incomplete fulfillment
- Failed verification
- Missing authorization evidence
- Incorrect permissions
- Unavailable licenses
- Unresolved technical errors
- Missing requester information
- Incomplete configuration documentation
- Unexpected service disruption
- Unresolved security concerns

## 10.3 Procedure

1. Review fulfillment notes.
2. Review verification findings.
3. Identify outstanding work.
4. Determine the operational impact.
5. Identify the responsible technician.
6. Determine whether further fulfillment is required.
7. Escalate or create related records when appropriate.
8. Update the request status.

## 10.4 Outstanding Issue Register

| Issue ID | Description | Impact | Owner | Status |
|---|---|---|---|---|
| ISSUE-001 | [Description] | [Impact] | [Role] | Open |

## 10.5 Handling Outcomes

| Condition | Action |
|---|---|
| Minor documentation gap | Obtain or document missing information |
| Incomplete fulfillment | Return to fulfillment |
| Incorrect implementation | Assess correction or recovery |
| Service interruption | Follow Incident Management |
| Recurring technical failure | Consider Problem Management |
| Unauthorized change identified | Escalate under applicable security and change procedures |
| Request no longer required | Evaluate cancellation |
| Approved alternative delivered | Verify and document the alternative |

### Important

Do not close a request as fulfilled simply because the technician cannot complete the work.

Use an accurate final disposition and preserve relevant evidence.

---

# 11. Step 5 — Confirm Authorization Conditions

## 11.1 Objective

Ensure that the final result complies with the authorization granted during assessment.

## 11.2 Authorization Review

| Item | Requirement |
|---|---|
| Authorization Evidence | Available when required |
| Approved Resource | Matches implementation |
| Approved User | Matches implementation |
| Approved Permission Level | Matches implementation |
| Approval Conditions | Satisfied |
| Temporary Access Expiration | Recorded when applicable |
| Change Authorization | Completed when required |

## 11.3 Procedure

1. Review the original authorization.
2. Identify the approved scope.
3. Compare the scope with the implemented configuration.
4. Confirm that conditions were followed.
5. Identify unauthorized deviations.
6. Record the review outcome.

## 11.4 Temporary Access

For time-limited access, verify that:

- The approved expiration is documented.
- The responsible owner is identified.
- A removal or review mechanism is established.
- The request record references the follow-up requirement.

### Important

Closing the initial access request does not eliminate the responsibility to remove temporary access when its authorization expires.

A separate tracked task or control may be required.

---

# 12. Step 6 — Obtain Requester Confirmation

## 12.1 Objective

Confirm that the delivered service meets the requester's needs when confirmation is required.

## 12.2 Confirmation Requirements

Requester confirmation may be appropriate for:

- Shared folder access
- Software installations
- Device provisioning
- Collaboration access
- Application configuration
- Other services requiring user interaction

Confirmation may be unnecessary when objective technical verification sufficiently demonstrates fulfillment under an approved service model.

## 12.3 Procedure

1. Determine whether requester confirmation is required.
2. Review the fulfillment result.
3. Contact the requester through an approved channel.
4. Provide relevant verification instructions.
5. Request confirmation where appropriate.
6. Record the response.
7. Address reported issues before closure.

## 12.4 Example Confirmation Message

**Subject:** Service Request SR-001 — Verification Requested

Hello,

The requested IT service has been implemented.

**Request:** [Description]  
**Service Delivered:** [Description]

Please confirm whether the service works as expected.

If you experience any issues, reply with a description so the IT Service Desk can investigate.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 12.5 Confirmation Record

**Request ID:** SR-###

**Confirmation Required:** [Yes / No]

**Confirmation Requested:** [Date or Not Applicable]

**Requester Response:** Pending

**Confirmation Status:** [Confirmed / Issue Reported / No Response / Not Required]

**Evidence:** [Reference]

## 12.6 No Response Handling

If the requester does not respond:

1. Follow the applicable communication policy.
2. Review available technical verification.
3. Determine whether requester confirmation is mandatory.
4. Document contact attempts.
5. Escalate unresolved concerns when necessary.
6. Apply any established administrative closure rules.

### Important

Do not invent requester confirmation.

A request may be administratively closed without a response only when the applicable service model permits it and required verification and communication steps have been completed.

---

# 13. Step 7 — Review Related Configuration Records

## 13.1 Objective

Confirm that relevant configuration documentation reflects the fulfilled request.

## 13.2 Potentially Affected Records

- Server configuration items
- Workstation configuration items
- Network device configuration items
- Cloud service configuration items
- Software inventory
- Device ownership
- Service dependencies
- Configuration baselines

## 13.3 Procedure

1. Determine whether fulfillment changed a tracked configuration item.
2. Identify the affected CI record.
3. Review the documented configuration.
4. Compare it with the verified result.
5. Update the record when required.
6. Confirm the update is traceable to the request.
7. Review relevant dependency maps.
8. Record completion.

## 13.4 Configuration Review

**Related CI:** CI-###

**CI Update Required:** [Yes / No]

**CI Update Completed:** [Yes / No / Not Applicable]

**Dependency Map Update Required:** [Yes / No]

**Dependency Map Updated:** [Yes / No / Not Applicable]

**Evidence:** [Reference]

### Important

Not every service request requires a configuration item update.

Apply the organization's configuration management scope.

---

# 14. Step 8 — Review Knowledge Documentation

## 14.1 Objective

Determine whether the completed request revealed information that should be captured or improved in the Knowledge Base.

## 14.2 Knowledge Review Triggers

- A new technical procedure was developed.
- Existing instructions were inaccurate.
- Troubleshooting was required.
- A recurring fulfillment issue was identified.
- A more efficient method was discovered.
- Verification requirements changed.
- A common employee question was identified.

## 14.3 Procedure

1. Review the technical work performed.
2. Identify the knowledge article used.
3. Determine whether the article remains accurate.
4. Identify missing or outdated instructions.
5. Propose a new or updated article when appropriate.
6. Record the knowledge reference.
7. Follow the Knowledge Article Lifecycle procedure.

## 14.4 Knowledge Review Record

**Knowledge Article Used:** [Reference or None]

**Article Update Required:** [Yes / No]

**New Article Recommended:** [Yes / No]

**Knowledge Improvement Description:** [Description]

**Knowledge Status:** [Pending / Completed / Not Applicable]

### Important

A service request does not need a new knowledge article simply because it was completed.

Knowledge articles should provide reusable value.

---

# 15. Step 9 — Review Related Records

## 15.1 Objective

Ensure the service request remains traceable to relevant operational records.

## 15.2 Potential Relationships

| Record Type | Example Relationship |
|---|---|
| Incident | Fulfillment caused or identified a service interruption |
| Problem | Repeated fulfillment failures require investigation |
| Change | Fulfillment involved a controlled technical change |
| Configuration Item | Request modified a tracked resource |
| Dependency Map | Request affected a documented service dependency |
| Knowledge Article | Technical guidance used or updated |
| Scenario | Request forms part of a simulated business scenario |
| Improvement | Closure revealed an improvement opportunity |

## 15.3 Procedure

1. Review related activity.
2. Identify applicable records.
3. Confirm identifiers.
4. Link records where supported.
5. Document relationships in GitHub when appropriate.
6. Verify that references are accurate.

## 15.4 Related Record Register

| Record Type | Record ID | Relationship |
|---|---|---|
| Incident | INC-### | [If applicable] |
| Problem | PRB-### | [If applicable] |
| Change | CHG-### | [If applicable] |
| Configuration Item | CI-### | [If applicable] |
| Dependency Map | DM-### | [If applicable] |
| Knowledge Article | [Reference] | [If applicable] |
| Scenario | SCN-### | [If applicable] |
| Improvement | IMP-### | [If applicable] |

### Important

Do not create unnecessary records solely to populate the relationship table.

Only reference records that exist or clearly identify proposed relationships.

---

# 16. Step 10 — Assign the Closure Classification

## 16.1 Objective

Record the final disposition of the service request accurately.

## 16.2 Proposed Closure Classifications

| Classification | Definition |
|---|---|
| Fulfilled | Requested service successfully delivered and verified |
| Fulfilled with Approved Alternative | Authorized alternative delivered and verified |
| Rejected | Request was not authorized |
| Cancelled by Requester | Requester withdrew the request |
| Cancelled by IT | Request cancelled under an applicable policy |
| Duplicate | Existing request already covers the same work |
| Not Fulfilled | Request concluded without successful delivery under an approved disposition |
| Other | Approved closure classification with documented explanation |

## 16.3 Classification Procedure

1. Review the request history.
2. Confirm the final disposition.
3. Select the appropriate classification.
4. Record the reason.
5. Link related records when applicable.
6. Verify that the classification matches the evidence.

## 16.4 Closure Classification Record

**Request ID:** SR-###

**Closure Classification:** Pending

**Closure Reason:** [Description]

**Fulfillment Successful:** [Yes / No / Not Applicable]

**Verification Completed:** [Yes / No / Not Applicable]

**Closure Authority:** [Role]

### Important

Do not use the "Fulfilled" classification for rejected, cancelled, or unsuccessful requests.

Accurate classification is essential for reliable reporting.

---

# 17. Step 11 — Complete the Closure Summary

## 17.1 Objective

Create a concise final record explaining how the request concluded.

## 17.2 Required Closure Summary

The summary should identify:

- Original request
- Final disposition
- Work performed, if applicable
- Verification method
- Verification result
- Requester confirmation status
- Relevant authorization
- Outstanding issues
- Related records
- Closure reason

## 17.3 Closure Summary Template

**Request ID:** SR-###

**Requested Service:** [Service]

**Requester:** [Employee]

**Final Disposition:** [Disposition]

**Work Performed:**

[Describe actual work or state Not Applicable.]

**Verification Method:**

[Describe or state Not Applicable.]

**Verification Result:**

[Actual result or Not Applicable.]

**Requester Confirmation:**

[Status]

**Outstanding Issues:**

[None or Description]

**Related Records:**

[References]

**Closure Reason:**

[Explanation]

## 17.4 Documentation Procedure

1. Review the request history.
2. Summarize the final outcome.
3. Document the actual work performed.
4. Include verification results.
5. Identify relevant limitations.
6. Record requester confirmation status.
7. Include related record references.
8. Save the summary.

### Important

The closure summary should describe the actual outcome, not merely repeat the original request.

---

# 18. Step 12 — Notify the Requester

## 18.1 Objective

Communicate the final disposition of the request.

## 18.2 Communication Requirements

The closure notification should include:

- Request reference
- Requested service
- Final disposition
- Brief summary of the outcome
- Relevant next steps
- Instructions for reporting remaining issues

## 18.3 Example Successful Closure Message

**Subject:** Service Request SR-001 — Completed

Hello,

Your IT service request has been completed.

**Request:** [Description]  
**Service Delivered:** [Description]  
**Status:** Fulfilled

The requested service has been implemented and verified.

If you experience any issues, please contact the IT Service Desk and reference SR-001.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 18.4 Example Cancellation Message

**Subject:** Service Request SR-001 — Cancelled

Hello,

Your service request has been cancelled.

**Request:** [Description]  
**Status:** Cancelled  
**Reason:** [Reason]

If the service is still required, please contact the IT Service Desk.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 18.5 Procedure

1. Confirm the closure classification.
2. Prepare the notification.
3. Verify the information is accurate.
4. Communicate through an approved channel.
5. Record the communication.
6. Update the request history.

### Important

Do not claim that the requester was notified unless communication actually occurred.

---

# 19. Step 13 — Perform the Closure Quality Review

## 19.1 Objective

Confirm that the request meets the organization's closure requirements.

## 19.2 Closure Quality Checklist

### Request Information

- [ ] Request ID recorded
- [ ] Requester identified
- [ ] Requested service documented
- [ ] Service category correct
- [ ] Request owner recorded

### Authorization

- [ ] Authorization requirements evaluated
- [ ] Required approval evidence available
- [ ] Approved scope documented
- [ ] Authorization conditions reviewed

### Fulfillment

- [ ] Final fulfillment outcome documented
- [ ] Actual technical work recorded
- [ ] Verification completed where required
- [ ] Relevant errors documented
- [ ] Recovery actions recorded where applicable

### Communication

- [ ] Requester confirmation addressed
- [ ] Final communication prepared
- [ ] Required notification completed
- [ ] Communication evidence recorded where applicable

### Documentation

- [ ] Closure classification accurate
- [ ] Closure summary complete
- [ ] Related records linked
- [ ] CI updates completed where required
- [ ] Knowledge updates considered
- [ ] Evidence retained
- [ ] Sensitive information protected

## 19.3 Quality Review Outcome

**Request ID:** SR-###

**Quality Review Status:** Pending

**Reviewed By:** [Role]

**Review Date:** Pending

**Outstanding Documentation:** [None or Description]

**Closure Authorized:** [Yes / No / Pending]

### Important

The level of review may vary by request type and risk.

Routine low-risk requests may use automated or checklist-based validation where an approved workflow exists.

Sensitive requests may require independent review.

---

# 20. Step 14 — Close the Request

## 20.1 Objective

Formally record the final disposition and transition the request to its closed state.

## 20.2 Closure Prerequisites

Before closing the request:

1. Confirm the final disposition.
2. Complete the closure summary.
3. Verify required documentation.
4. Confirm applicable communications.
5. Review outstanding issues.
6. Confirm related records are appropriately referenced.
7. Select the correct closure classification.

## 20.3 Closure Procedure

1. Open the request record.
2. Review the final summary.
3. Confirm the closure classification.
4. Enter the closure reason.
5. Record the closure date and time.
6. Identify the person performing closure.
7. Update the request status to Closed.
8. Save the record.
9. Confirm the status change was retained.

## 20.4 Closure Record

| Field | Value |
|---|---|
| Request ID | SR-### |
| Final Status | Closed |
| Closure Classification | [Classification] |
| Closure Reason | [Reason] |
| Closed By | [Role] |
| Closure Date | Pending |
| Closure Time | Pending |
| Verification Reference | [Reference] |
| Communication Reference | [Reference] |

## 20.5 Closure Verification

After saving:

- [ ] Status displays Closed
- [ ] Closure classification retained
- [ ] Closure reason retained
- [ ] Closure date/time recorded
- [ ] Final summary available
- [ ] Supporting evidence accessible
- [ ] Related record references retained

### Important

Do not record a request as closed until the actual status change has been performed and verified.

---

# 21. Step 15 — Retain Records and Evidence

## 21.1 Objective

Preserve the documentation required for traceability, reporting, review, and continual improvement.

## 21.2 Records to Retain

Depending on the request:

- Original request details
- Requester information
- Assessment findings
- Authorization evidence
- Fulfillment documentation
- Technical verification results
- Requester communications
- Closure summary
- Closure classification
- Related record references
- Relevant screenshots or command output

## 21.3 Evidence Register

| Evidence ID | Evidence Type | Description | File |
|---|---|---|---|
| EVD-001 | Request Record | Original request | [Path] |
| EVD-002 | Authorization | Approval evidence | [Path] |
| EVD-003 | Technical Verification | Verification results | [Path] |
| EVD-004 | Communication | Closure notification | [Path] |

These entries are placeholders, not actual collected evidence.

## 21.4 Record Retention

**Retention Period:** To Be Established

**Retention Authority:** Internal IT / Applicable Organizational Policy

**Storage Location:** Approved ITSM Platform or Documentation Repository

**Access Restrictions:** Based on record sensitivity

## 21.5 Portfolio Evidence

For GitHub documentation:

- Use fictional employee identities.
- Sanitize screenshots.
- Remove credentials.
- Avoid publishing sensitive account information.
- Distinguish simulated activities from verified lab results.
- Preserve relevant technical evidence without exposing secrets.

### Important

GitHub should not be treated as the primary repository for confidential production service request records.

---

# 22. Reopened Requests and Follow-Up Issues

## 22.1 Objective

Establish a consistent response when a requester reports that a previously closed request was not successfully fulfilled.

## 22.2 Reopening Considerations

- Was the original fulfillment incorrect?
- Was verification incomplete?
- Did the requested service never become available?
- Has a new technical issue occurred?
- Is the new request materially different?
- Does the ITSM platform support reopening?
- Does organizational policy permit reopening?

## 22.3 Procedure

1. Review the original request.
2. Confirm the reported issue.
3. Determine whether it relates to the original fulfillment.
4. Review technical evidence.
5. Apply the configured reopening policy.
6. Reopen the original record or create a linked record as appropriate.
7. Assign responsibility.
8. Continue the applicable workflow.

## 22.4 Reopen vs. New Record

| Situation | Potential Action |
|---|---|
| Original request was incorrectly fulfilled | Reopen or create linked corrective request |
| Original work was incomplete | Continue fulfillment |
| Previously working service is now unavailable | Create an incident |
| Employee requests additional functionality | Create a new service request |
| Repeated failures indicate an underlying issue | Consider a problem record |

### Important

Do not automatically classify every post-closure issue as a new service request.

Determine whether the issue is incomplete fulfillment, a new request, or an incident.

---

# 23. Practical Lab Example — Active Directory Folder Access Closure

## 23.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-001  
**Scenario Type:** Service Request  
**Service:** IT-SVC-001 — Identity & Access Management  
**Request Type:** Shared Folder Access  
**Environment:** Active Directory Lab  
**Classification:** Proposed Simulation

### Business Context

An HR employee requested access to a departmental shared folder.

The request has completed a simulated authorization and fulfillment workflow.

The Service Desk must review the technical results, confirm that the approved permissions were applied, and determine whether the request is ready for closure.

## 23.2 Example Lab Infrastructure

| Component | Example Configuration |
|---|---|
| Domain | homelab.local |
| Primary Domain Controller | DC01 |
| Secondary Domain Controller | DC02 |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Identity Platform | Active Directory Domain Services |

Current configurations must be verified before performing the scenario.

## 23.3 Proposed Closure Tasks

1. Open the simulated service request.
2. Review the authorization record.
3. Confirm the approved access level.
4. Review the fulfillment documentation.
5. Verify the user's security group membership.
6. Confirm the group provides the intended resource access.
7. Review functional access testing.
8. Check for outstanding issues.
9. Determine whether requester confirmation is required.
10. Document the final outcome.
11. Assign the closure classification.
12. Complete the closure record.

## 23.4 Technical Verification — User Account

Run from an authorized management environment with the Active Directory PowerShell module available.

```powershell
Get-ADUser -Identity "username" -Properties Enabled,Department |
Select-Object Name,SamAccountName,Enabled,Department
```

**Expected Result:** The intended user account is found.

**Actual Result:** Not Yet Tested

## 23.5 Technical Verification — Group Membership

```powershell
Get-ADGroupMember -Identity "HR_Security_Group" |
Where-Object SamAccountName -eq "username"
```

**Expected Result:** The approved user appears in the intended security group.

**Actual Result:** Not Yet Tested

## 23.6 Functional Verification

Group membership alone does not establish successful folder access.

Additional verification should include:

1. Confirming the group has the intended folder permissions.
2. Testing access using an authorized employee session.
3. Confirming the requested level of access.
4. Checking for unintended permissions.
5. Documenting the observed result.

**Functional Verification Status:** Pending

## 23.7 Example Closure Review

| Requirement | Status |
|---|---|
| Request Authorized | Pending Verification |
| Correct User Modified | Pending Verification |
| Correct Group Membership | Pending Verification |
| Folder Access Functional | Not Yet Tested |
| Security Requirements Satisfied | Pending |
| Requester Confirmation | Pending |
| Documentation Complete | Pending |
| Ready for Closure | Not Yet Determined |

## 23.8 Expected Learning Outcomes

- Review completed service requests.
- Verify Active Directory changes.
- Distinguish technical verification from functional verification.
- Confirm authorization compliance.
- Document fulfillment results.
- Evaluate closure readiness.
- Apply accurate closure classifications.
- Preserve supporting evidence.

## 23.9 Evidence to Capture

- Original service request
- Authorization record
- Fulfillment documentation
- User account verification
- Group membership verification
- Folder access test results
- Requester confirmation when applicable
- Closure summary
- Final request status

### Important

This scenario is instructional.

Expected results, simulated approvals, and example records do not demonstrate completed technical activity.

---

# 24. Practical Lab Example — Microsoft 365 License Request Closure

## 24.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-###  
**Service:** IT-SVC-003 — Microsoft 365 & Collaboration  
**Request Type:** License Assignment  
**Classification:** Proposed Simulation

### Business Context

An employee requested Microsoft 365 functionality requiring a license.

The Service Desk must confirm that the approved license was assigned to the correct user and that the intended functionality is available.

## 24.2 Proposed Closure Procedure

1. Open the request record.
2. Review the approved license assignment.
3. Confirm the affected user.
4. Review the administrator's fulfillment notes.
5. Verify the assigned license in the appropriate administrative portal.
6. Confirm that the required service is available.
7. Review any licensing errors.
8. Check for outstanding issues.
9. Document the verification results.
10. Notify the requester.
11. Complete the closure record.

## 24.3 Verification Record

| Verification Item | Expected Result | Actual Result |
|---|---|---|
| Correct User | Intended employee | Pending |
| Correct License | Approved license | Pending |
| License Assignment | Successfully assigned | Pending |
| Service Availability | Required functionality available | Pending |
| Authorization Scope | No unauthorized assignment | Pending |
| Closure Readiness | Requirements satisfied | Pending |

## 24.4 Evidence

Potential evidence includes:

- Sanitized license assignment screenshot
- Administrative portal verification
- Request authorization record
- Fulfillment notes
- Requester confirmation where required
- Final closure record

### Important

This example does not claim that any license has been assigned or that Microsoft 365 services have been verified.

---

# 25. Common Request Closure Errors

| Error | Potential Consequence | Prevention |
|---|---|---|
| Premature closure | Incomplete service delivery | Verify completion |
| Incorrect closure classification | Inaccurate reporting | Match classification to outcome |
| Missing verification | Undetected fulfillment failure | Review technical evidence |
| Missing requester communication | Poor service experience | Follow communication requirements |
| Assuming requester confirmation | Misleading documentation | Record actual responses |
| Missing authorization review | Unauthorized access remains | Compare approved and implemented scope |
| Incomplete closure summary | Poor traceability | Document final outcome |
| Unresolved technical issues | Request incorrectly marked complete | Review outstanding work |
| Missing CI updates | Inaccurate configuration information | Review configuration impact |
| Missing related record links | Reduced operational traceability | Link applicable records |
| Fabricated evidence | Misleading portfolio documentation | Use verified observations |
| Closing to improve metrics | Distorted performance reporting | Follow objective closure criteria |

---

# 26. Metrics and Performance Measurement

Request Closure may be evaluated using service metrics.

## 26.1 Proposed Metrics

| Metric | Description | Measurement |
|---|---|---|
| Request Closure Time | Time from closure readiness to formal closure | Duration |
| End-to-End Request Completion Time | Time from request receipt to final completion | Duration |
| Closure Documentation Completeness | Requests containing required closure information | Percentage |
| Fulfillment Verification Rate | Fulfilled requests with documented verification | Percentage |
| Request Reopen Rate | Closed requests subsequently reopened | Percentage |
| Requester Confirmation Rate | Applicable requests with documented confirmation | Percentage |
| Closure Classification Accuracy | Requests assigned the correct closure reason | Percentage |
| Requests Awaiting Closure | Requests ready for closure but not yet closed | Count |

## 26.2 Example Metric — Closure Documentation Completeness

**Metric Name:** Closure Documentation Completeness

**Definition:** Percentage of evaluated closed service requests containing all required closure documentation.

**Formula:**

```text
Closure Documentation Completeness (%) =

Closed Requests with Complete Required Documentation
----------------------------------------------------- x 100
             Total Evaluated Closed Requests
```

**Baseline:** Not Yet Established

**Target:** Not Yet Established

**Actual Result:** Not Yet Measured

## 26.3 Example Metric — Request Reopen Rate

**Definition:** Percentage of requests closed during a defined period that are reopened within a specified follow-up window.

**Formula:**

```text
Request Reopen Rate (%) =

Requests Closed During Period and Reopened Within Follow-Up Window
------------------------------------------------------------------ x 100
                Total Requests Closed During Period
```

**Follow-Up Window:** To Be Defined

**Baseline:** Not Yet Established

**Target:** Not Yet Established

**Actual Result:** Not Yet Measured

## 26.4 Measurement Requirements

1. Define the metric.
2. Establish the reporting period.
3. Identify the data source.
4. Define inclusion and exclusion criteria.
5. Collect actual request records.
6. Validate data quality.
7. Calculate the result.
8. Preserve supporting evidence.
9. Identify trends and improvement opportunities.

## 26.5 Related Documentation

[Service Metrics Documentation Standards](../../Continual-Improvement/Service-Metrics/README.md)

[Service Metric Template](../../Templates/Service-Metric-Template.md)

### Important

No service performance targets, achieved results, or automated reporting capabilities are claimed by this SOP.

---

# 27. Security and Compliance Considerations

## 27.1 Sensitive Information

Service request records may contain:

- Employee identities
- Department information
- Account details
- Resource names
- Access permissions
- Device information
- Business justifications
- Authorization records

## 27.2 Security Requirements

- Restrict access to sensitive records.
- Preserve authorization evidence.
- Avoid unnecessary personal information.
- Do not store credentials.
- Review privileged access changes.
- Confirm temporary access requirements.
- Apply organizational retention policies.
- Sanitize records before publication.

## 27.3 Privileged Access Closure

Requests involving privileged access may require additional verification:

1. Confirm the correct account received access.
2. Confirm the approved privilege level.
3. Verify the access duration.
4. Confirm relevant security controls.
5. Record independent review when required.
6. Establish a follow-up mechanism for temporary access.

## 27.4 Record Retention

**Retention Period:** To Be Established

**Retention Requirements:** Applicable Organizational Policy

**Storage Method:** Approved ITSM Platform or Secure Documentation System

### Important

Do not publish production authorization records, credentials, or sensitive employee information in a public GitHub repository.

---

# 28. Continual Improvement

## 28.1 Improvement Opportunities

Request Closure may reveal opportunities to improve:

- Fulfillment verification
- Requester communication
- Technical documentation
- Closure classifications
- Request forms
- Approval workflows
- Service request automation
- Configuration record updates
- Knowledge article quality
- Request lifecycle reporting

## 28.2 Improvement Procedure

1. Identify a closure-related inefficiency.
2. Collect supporting observations.
3. Determine the operational impact.
4. Propose an improvement.
5. Record the improvement opportunity.
6. Evaluate feasibility and risk.
7. Obtain applicable authorization.
8. Implement the improvement.
9. Measure the results.
10. Update this SOP when necessary.

## 28.3 Example Improvement Opportunity

**Observation:** Multiple service requests are delayed because fulfillment technicians do not consistently document verification results.

**Potential Improvement:** Introduce standardized verification fields in service request records.

**Expected Benefit:** Improved closure readiness and more consistent documentation.

**Status:** Illustrative Proposal — Not Implemented

## 28.4 Related Documentation

[Improvement Management SOP](../../Continual-Improvement/Procedures/Improvement-Management.md)

[Improvement Register](../../Continual-Improvement/Improvement-Register.md)

[Improvement Template](../../Templates/Improvement-Template.md)

---

# 29. Procedure Quality Checklist

## Process Definition

- [ ] Purpose documented
- [ ] Scope established
- [ ] Roles defined
- [ ] Closure workflow documented
- [ ] Closure classifications established
- [ ] Closure criteria defined
- [ ] Record retention addressed

## Fulfillment Review

- [ ] Original request reviewed
- [ ] Final disposition established
- [ ] Approved scope compared with actual work
- [ ] Technical verification reviewed
- [ ] Outstanding issues identified
- [ ] Authorization conditions evaluated

## Requester Communication

- [ ] Requester confirmation requirements evaluated
- [ ] Actual requester response documented where applicable
- [ ] Final notification completed
- [ ] Communication evidence retained where required

## Documentation

- [ ] Closure summary completed
- [ ] Closure classification accurate
- [ ] Closure reason recorded
- [ ] Related records linked
- [ ] Configuration updates reviewed
- [ ] Knowledge improvements considered
- [ ] Supporting evidence retained

## Final Closure

- [ ] Closure quality review completed
- [ ] Request status updated
- [ ] Closure date/time recorded
- [ ] Closure owner identified
- [ ] Final status verified
- [ ] Evidence retained appropriately

## Portfolio Accuracy

- [ ] Fictional organization identified
- [ ] Simulated activities clearly labeled
- [ ] Actual verification distinguished from expected results
- [ ] No fabricated requester confirmations
- [ ] No fabricated ticket closures
- [ ] No unsupported automation claims
- [ ] Sensitive information removed
- [ ] Relative links verified

---

# 30. Document Review and Revision History

## 30.1 Review Triggers

Review this SOP when:

- Closure requirements change.
- Service request workflows change.
- ITSM platform configurations change.
- Requester confirmation requirements change.
- Verification standards change.
- Security policies are updated.
- Record retention requirements change.
- New services are introduced.
- Closure quality reviews identify issues.
- Continual improvement initiatives introduce new processes.

## 30.2 Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Request Closure SOP aligned with ITIL 4 Service Request Management |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This SOP establishes a proposed standard for verifying, documenting, communicating, and formally closing employee IT service requests within a simulated corporate environment.

Organizational roles, employee requests, approval decisions, communications, and operational scenarios may be fictional or proposed.

Actual fulfillment results, technical verification, requester confirmation, ticket closure, and performance measurements must be supported by documented lab evidence.

Simulated approvals, example communications, and expected outcomes must not be represented as actual production activity or professional employment experience.

Jira Service Management and associated automation capabilities are planned unless implementation and verification are explicitly documented.

This procedure demonstrates service request lifecycle management, fulfillment verification, closure classification, documentation quality, operational traceability, requester communication, and continual improvement.
