# SOP-SRM-002 — Request Assessment and Authorization

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Request Management  
**Document Type:** Standard Operating Procedure (SOP)  
**SOP ID:** SOP-SRM-002  
**Version:** 1.0  
**Status:** Draft — Proposed Operating Standard  
**Process Owner:** Internal IT  
**Primary Responsible Function:** Service Request Management  
**Effective Date:** Pending Adoption  
**Last Reviewed:** Not Yet Reviewed  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

# 1. Purpose

Establish a standardized procedure for assessing employee IT service requests and obtaining the authorization required before fulfillment.

This procedure ensures that requests are evaluated consistently against business needs, service eligibility, technical feasibility, security requirements, licensing, costs, and organizational policies.

The objectives are to:

- Confirm that a request is valid and sufficiently documented.
- Determine whether the requested service is available.
- Evaluate the business justification.
- Identify technical and operational requirements.
- Verify requester eligibility.
- Apply information security requirements.
- Determine the appropriate authorization authority.
- Obtain and document required approvals.
- Prevent unauthorized access or configuration changes.
- Communicate assessment decisions.
- Prepare authorized requests for fulfillment.

**Key Principle:** A valid service request is not necessarily an authorized service request.

Approval must be obtained when required, and fulfillment must remain within the approved scope.

---

# 2. Scope

## 2.1 In Scope

This procedure applies to employee IT service requests that have been logged and require assessment before fulfillment.

Examples include:

- New employee account requests
- User account modifications
- Security group membership requests
- Shared folder access requests
- Microsoft 365 license assignments
- Microsoft Entra ID access requests
- Microsoft Intune device enrollment requests
- Approved software installations
- Hardware provisioning requests
- Network access requests
- Privileged access requests
- Employee onboarding and role changes
- Requests involving costs or additional licensing

## 2.2 Out of Scope

This procedure does not directly perform:

- Initial request logging
- Technical fulfillment
- Incident troubleshooting
- Root cause analysis
- Change implementation
- Service request closure
- Security incident response

These activities are governed by their respective procedures.

## 2.3 Supported Environments

Assessment may involve:

- Active Directory Domain Services
- Windows Server
- Windows 11
- Microsoft 365
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Network infrastructure
- ITSM platforms

The existence, availability, and configuration of these systems must be verified before they are referenced as operational dependencies.

---

# 3. ITIL 4 Alignment

This SOP supports the ITIL 4 Service Request Management practice.

Service Request Management aims to support agreed service quality by handling predefined, user-initiated service requests effectively and efficiently.

Assessment and authorization help ensure that requests are appropriate, feasible, secure, and consistent with organizational requirements.

## 3.1 Related ITIL Practices

| Practice | Relationship |
|---|---|
| Service Desk | Communicates with the requester and coordinates request handling |
| Service Request Management | Evaluates requests and coordinates authorization |
| Knowledge Management | Provides documented service requirements and fulfillment guidance |
| Information Security Management | Defines access control and security requirements |
| Service Configuration Management | Identifies affected configuration items and dependencies |
| Change Enablement | Evaluates requests requiring formal change control |
| Continual Improvement | Reviews assessment delays, approval patterns, and process effectiveness |

## 3.2 Practice Boundaries

Service Request Management determines whether a request is eligible for fulfillment.

Information Security Management establishes relevant security requirements.

Change Enablement governs technical changes that require formal change authorization.

These practices may operate together without requiring separate organizational departments.

### Important

A service request approval does not automatically authorize a technical change that requires separate change control.

---

# 4. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Requester | Provides the request and business justification |
| Service Desk Technician | Reviews request completeness and coordinates communication |
| Request Owner | Coordinates assessment and tracks authorization |
| Service Owner | Determines service eligibility and service-specific requirements |
| Manager | May approve business need or employee eligibility |
| Resource Owner | Authorizes access to resources under their responsibility |
| Security Administrator | Evaluates security-sensitive requests |
| IT Administrator | Evaluates technical feasibility and permissions |
| Change Authority | Authorizes applicable technical changes |
| Fulfillment Technician | Performs work after required authorization is established |

## 4.1 Separation of Responsibilities

Where practical:

- The requester submits the request.
- The appropriate authority approves the request.
- An authorized technician performs fulfillment.
- The request owner maintains the record.

A single technician may perform multiple operational activities when permitted by organizational policy.

However, a technician's administrative privileges do not automatically grant authority to approve access or expenditures.

## 4.2 Approval Authority

Approval authority depends on the requested service.

For example:

- A manager may confirm business need.
- A resource owner may authorize folder access.
- A licensing authority may approve additional expenditure.
- A security authority may review privileged access.
- A change authority may approve a controlled infrastructure change.

Approval requirements must be defined by applicable organizational policies and service-specific rules.

---

# 5. Assessment and Authorization Principles

All assessments should follow these principles.

## 5.1 Business Justification

The request should have a legitimate operational purpose when justification is required.

## 5.2 Least Privilege

Grant only the access necessary to perform approved responsibilities.

## 5.3 Separation of Duties

Avoid unnecessary conflicts between requesting, approving, and implementing sensitive actions.

## 5.4 Service Eligibility

Confirm that the requested service is available to the requester or affected user.

## 5.5 Technical Feasibility

Verify that the request can be fulfilled using available systems, permissions, and resources.

## 5.6 Traceability

Document assessment decisions, required approvals, and authorization evidence.

## 5.7 Scope Control

Fulfillment must not exceed what was authorized.

## 5.8 Evidence-Based Decisions

Distinguish verified facts from assumptions and proposed configurations.

---

# 6. Assessment and Authorization Workflow

## 6.1 High-Level Workflow

```text
Logged Service Request
          |
          v
Review Request Record
          |
          v
Verify Request Completeness
          |
          v
Check Service Eligibility
          |
          v
Evaluate Business Justification
          |
          v
Assess Technical Feasibility
          |
          v
Evaluate Security and Cost
          |
          v
Determine Approval Requirements
          |
          v
Is Approval Required?
       /         \
      No         Yes
      |           |
      |           v
      |       Identify Approver
      |           |
      |           v
      |       Request Approval
      |           |
      |           v
      |       Review Decision
      |           |
      +-----+-----+
            |
            v
Evaluate Assessment Outcome
            |
      +-----+-----+
      |     |     |
   Approve Defer Reject
      |     |     |
      v     v     v
   Prepare Hold  Document
   Handoff       Decision
      |
      v
Request Fulfillment
```

## 6.2 Possible Outcomes

| Outcome | Meaning | Next Action |
|---|---|---|
| Authorized | Requirements satisfied and necessary approvals obtained | Prepare fulfillment |
| Authorized with Conditions | Approved within defined limitations | Document and enforce conditions |
| Pending Approval | Required authorization has not been received | Await decision |
| Awaiting Information | Assessment cannot proceed without clarification | Contact requester |
| Deferred | Decision postponed | Document reason and next review |
| Rejected | Request not approved | Document and communicate decision |
| Cancelled | Request withdrawn or no longer required | Document cancellation |
| Redirected | Another workflow is required | Transfer or link appropriate record |

### Important

The absence of a response from an approver must not be treated as approval unless an explicitly established policy authorizes that behavior for the specific request type.

---

# 7. Step 1 — Review the Logged Request

## 7.1 Objective

Confirm that the request record contains the information necessary for assessment.

## 7.2 Required Information

| Field | Requirement |
|---|---|
| Request ID | Required |
| Requester | Required |
| Affected User | When applicable |
| Requested Service | Required |
| Request Category | Required |
| Business Justification | When applicable |
| Requested Resource | When applicable |
| Initial Priority | Required |
| Request Owner | Required |
| Current Status | Required |
| Supporting Documentation | When applicable |

## 7.3 Procedure

1. Open the service request record.
2. Confirm the request identifier.
3. Review the requester information.
4. Identify the affected user or system.
5. Review the requested service.
6. Check the request category.
7. Confirm the business justification.
8. Identify missing information.
9. Verify that the request belongs in the Service Request Management workflow.

## 7.4 Incomplete Requests

If required information is missing:

1. Identify the missing fields.
2. Update the request status.
3. Contact the requester.
4. Document the clarification request.
5. Resume assessment when sufficient information is available.

**Suggested Status:** Awaiting Information

### Important

Do not approve a request whose scope cannot be determined.

---

# 8. Step 2 — Verify Service Eligibility

## 8.1 Objective

Determine whether the requested service is available and appropriate for the affected user.

## 8.2 Eligibility Considerations

- Employment or account status
- Department
- Assigned responsibilities
- Service Catalog availability
- Existing access
- Device ownership
- Applicable licensing
- Service-specific restrictions
- Organizational policies

## 8.3 Eligibility Assessment

| Requirement | Assessment | Evidence |
|---|---|---|
| Service Available | Pending | [Reference] |
| Requester Eligible | Pending | [Reference] |
| Affected User Eligible | Pending | [Reference] |
| Required Account Exists | Pending | [Reference] |
| Service Restrictions Satisfied | Pending | [Reference] |

## 8.4 Procedure

1. Identify the requested service.
2. Review the Service Catalog.
3. Determine whether the service is offered.
4. Review applicable eligibility requirements.
5. Confirm the affected user's eligibility.
6. Identify any restrictions.
7. Record the result.

## 8.5 Eligibility Outcomes

- Eligible
- Conditionally Eligible
- Not Eligible
- Unable to Determine

### Example

An employee requests Microsoft 365 Business Premium functionality.

The assessor must determine whether:

- The employee requires the requested functionality.
- The requested features are available under the intended license.
- An appropriate license is available.
- The assignment complies with organizational policy.
- Any additional cost requires authorization.

### Important

Do not assume that all Microsoft 365 or Azure services are included in a particular subscription.

Licensing and service availability must be checked against the actual environment and applicable product terms.

---

# 9. Step 3 — Evaluate Business Justification

## 9.1 Objective

Determine whether the request supports a legitimate business requirement.

## 9.2 Assessment Questions

- Why is the service needed?
- What responsibilities require the service?
- Is the request related to an employee's assigned role?
- Is the requested level of access appropriate?
- Is there an existing alternative?
- Is the request time-sensitive?
- Does the request create additional cost or risk?

## 9.3 Business Justification Record

**Request ID:** SR-###

**Requested Service:** [Service]

**Business Need:**

[Describe.]

**Expected Operational Benefit:**

[Describe.]

**Alternative Available:** [Yes / No / Unknown]

**Assessment Result:** Pending

## 9.4 Procedure

1. Review the justification.
2. Compare the request with the user's responsibilities.
3. Identify the expected benefit.
4. Consider available alternatives.
5. Determine whether further clarification is required.
6. Record the assessment.

### Important

A convincing business justification does not override security policies or access restrictions.

---

# 10. Step 4 — Assess Technical Feasibility

## 10.1 Objective

Determine whether the request can be fulfilled safely using available technology and resources.

## 10.2 Technical Assessment

| Requirement | Available? | Notes |
|---|---|---|
| Required System | Pending | [Details] |
| Administrative Tools | Pending | [Details] |
| Required Permissions | Pending | [Details] |
| Required License | Pending | [Details] |
| Network Connectivity | Pending | [Details] |
| Device Compatibility | Pending | [Details] |
| Technical Documentation | Pending | [Details] |
| Fulfillment Resources | Pending | [Details] |

## 10.3 Procedure

1. Identify the systems involved.
2. Review technical prerequisites.
3. Determine whether the required resources exist.
4. Confirm necessary administrative permissions.
5. Check compatibility requirements.
6. Identify potential dependencies.
7. Determine whether additional technical review is needed.
8. Document findings.

## 10.4 Technical Assessment Outcomes

- Feasible
- Feasible with Conditions
- Not Feasible
- Further Investigation Required

## 10.5 Example

**Request:** Add an employee to an Active Directory security group.

**Technical Considerations:**

- Does the user account exist?
- Does the group exist?
- Is the group appropriate for the requested access?
- Does the technician have permission to modify membership?
- Are there applicable restrictions?
- Does the request require a separate approval?

### Important

This stage evaluates feasibility.

It does not authorize the technician to modify Active Directory.

---

# 11. Step 5 — Evaluate Security Requirements

## 11.1 Objective

Identify security requirements and risks associated with the request.

## 11.2 Security Considerations

- Identity verification
- Least privilege
- Access classification
- Privileged permissions
- Sensitive data
- Separation of duties
- Account lifecycle
- MFA requirements
- Conditional Access requirements
- Security group membership
- Auditability
- Temporary access expiration

## 11.3 Security Assessment

| Security Requirement | Applicable? | Status |
|---|---|---|
| Identity Verification | Pending | Not Evaluated |
| Least-Privilege Review | Pending | Not Evaluated |
| Resource Owner Approval | Pending | Not Evaluated |
| Privileged Access Review | Pending | Not Evaluated |
| MFA Requirement | Pending | Not Evaluated |
| Temporary Access Expiration | Pending | Not Evaluated |
| Audit Documentation | Pending | Not Evaluated |

## 11.4 Procedure

1. Identify the requested permissions or capabilities.
2. Determine whether sensitive resources are involved.
3. Evaluate the requested access level.
4. Identify applicable security policies.
5. Determine whether security review is required.
6. Identify any necessary restrictions.
7. Document the assessment.

## 11.5 Least-Privilege Assessment

**Requested Access:** [Specify]

**Minimum Required Access:** [Specify]

**Excessive Permissions Identified:** [Yes / No / Pending]

**Recommended Access Scope:** [Specify]

## 11.6 Privileged Access

Requests involving elevated privileges may require:

- Additional approval
- Security review
- Time-limited access
- Separate administrative accounts
- Additional authentication controls
- Enhanced logging
- Periodic access review

### Important

Administrative access must not be granted merely because the requester has technical knowledge or a business need.

Privileged access requires appropriate authorization and security controls.

---

# 12. Step 6 — Evaluate Cost and Licensing

## 12.1 Objective

Identify financial, licensing, and resource implications.

## 12.2 Cost Considerations

- Software subscriptions
- Microsoft 365 licenses
- Intune licensing
- Azure resource consumption
- Hardware purchases
- Storage costs
- Network equipment
- Support costs
- Ongoing maintenance

## 12.3 Cost Assessment

| Cost Item | Estimated Cost | Frequency | Authorization Required |
|---|---|---|---|
| [Item] | TBD | [Monthly/One-Time] | Pending |

## 12.4 Procedure

1. Determine whether the request introduces costs.
2. Identify the required product or service.
3. Verify licensing requirements.
4. Check available licenses or resources.
5. Estimate additional costs where applicable.
6. Identify the appropriate financial authority.
7. Record the assessment.

## 12.5 Cost Assessment Outcome

**Additional Cost:** [Yes / No / Unknown]

**Estimated Cost:** Not Yet Determined

**Funding Approval Required:** [Yes / No / Pending]

**Approval Authority:** [Role]

### Important

Technical feasibility does not automatically establish financial authorization.

Do not assign paid licenses or provision billable cloud resources before the required approvals are obtained.

---

# 13. Step 7 — Determine Authorization Requirements

## 13.1 Objective

Identify the approvals necessary before fulfillment.

## 13.2 Proposed Authorization Matrix

| Request Type | Potential Approval Authority | Additional Review |
|---|---|---|
| Standard Low-Risk Request | Preauthorized through documented policy | Service eligibility |
| Departmental Folder Access | Resource Owner | Security requirements |
| Security Group Membership | Resource Owner or Designated Authority | Least-privilege review |
| Privileged Access | Authorized Security or Identity Authority | Enhanced security review |
| Software Installation | Software or Service Owner | Licensing and compatibility |
| Paid License Assignment | Licensing or Budget Authority | Cost review |
| Hardware Purchase | Budget Authority | Procurement requirements |
| Network Configuration Request | Network Service Owner | Change assessment |
| Infrastructure Modification | Applicable Change Authority | Technical risk assessment |

This matrix is a proposed governance model.

Actual approval authority must be established through organizational policies.

## 13.3 Authorization Classification

Classify the request as:

- Preauthorized Standard Request
- Single Approval Required
- Multiple Approvals Required
- Additional Security Review Required
- Change Authorization Required
- Authorization Requirements Undetermined

## 13.4 Preauthorized Requests

Some low-risk, predefined requests may be fulfilled without obtaining a separate approval for each submission.

However, the organization must establish:

- The eligible request types
- Required requester qualifications
- Approved fulfillment scope
- Applicable security controls
- Responsible service owner
- Conditions for using preauthorization

### Important

A request is not preauthorized simply because it is common or easy to perform.

Preauthorization must be supported by an established policy or approved service request model.

---

# 14. Step 8 — Identify the Approver

## 14.1 Objective

Determine who has authority to approve the request.

## 14.2 Procedure

1. Review the request type.
2. Identify the affected service or resource.
3. Review applicable authorization rules.
4. Determine the responsible approval authority.
5. Confirm that the approver has authority for the requested action.
6. Record the approver's role.
7. Identify any additional required approvals.

## 14.3 Approval Authority Record

| Field | Value |
|---|---|
| Request ID | SR-### |
| Approval Type | [Business / Resource / Security / Financial / Change] |
| Approver Role | [Role] |
| Approver Identity | [Authorized Individual] |
| Approval Scope | [Scope] |
| Approval Status | Pending |

## 14.4 Multiple Approvals

Some requests require more than one authorization.

For example, a paid software request may require:

1. Business approval.
2. Financial approval.
3. Licensing or technical assessment.

A privileged access request may require both resource-owner and security approval.

### Important

Do not substitute an unrelated manager's approval for authorization from the actual resource owner or designated authority.

---

# 15. Step 9 — Submit the Authorization Request

## 15.1 Objective

Provide the approver with sufficient information to make an informed decision.

## 15.2 Required Authorization Information

- Request ID
- Requester
- Affected user
- Requested service
- Requested resource
- Business justification
- Requested access level
- Relevant risks
- Estimated cost, if applicable
- Duration of access, if applicable
- Technical assessment
- Required decision

## 15.3 Procedure

1. Confirm the correct approver.
2. Prepare the authorization request.
3. Include the necessary context.
4. Submit through an approved channel.
5. Record the submission date and time.
6. Update the request status.
7. Await the decision.

**Suggested Status:** Pending Approval

## 15.4 Example Authorization Message

**Subject:** Approval Required — SR-001 — HR Shared Folder Access

Hello,

Service Request SR-001 requires authorization for an employee to access the HR departmental shared folder.

**Requested Access:** [Access Level]  
**Business Justification:** [Justification]  
**Affected User:** [Employee]  
**Requested Duration:** [Permanent or Temporary]

Please review the request and confirm whether the specified access should be approved, rejected, or modified.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 15.5 Approval Tracking

| Event | Date/Time | Status | Evidence |
|---|---|---|---|
| Approval Requested | Pending | Not Submitted | None |
| Approver Response | Pending | Awaiting Decision | None |
| Decision Recorded | Pending | Not Recorded | None |

---

# 16. Step 10 — Evaluate the Authorization Decision

## 16.1 Possible Decisions

| Decision | Meaning | Required Action |
|---|---|---|
| Approved | Request authorized within stated scope | Prepare fulfillment |
| Approved with Conditions | Authorization includes restrictions | Document conditions |
| Rejected | Request not authorized | Document and communicate |
| Deferred | Decision postponed | Record reason and follow-up |
| More Information Required | Approver needs clarification | Obtain information |
| No Response | Decision not received | Follow up or escalate |

## 16.2 Procedure

1. Receive the decision.
2. Confirm the decision came from an authorized source.
3. Verify that the decision identifies the relevant request.
4. Review any conditions or restrictions.
5. Record the decision.
6. Preserve supporting evidence.
7. Update the request status.
8. Communicate the result as appropriate.

## 16.3 Approval Conditions

Conditions may include:

- Limited access duration
- Reduced permissions
- Specific resource restrictions
- Additional MFA requirements
- Additional training
- Completion of another approval
- Restricted installation scope

## 16.4 Approval Verification

Before accepting an approval, verify:

- [ ] Correct Request ID
- [ ] Authorized Approver
- [ ] Requested Resource Identified
- [ ] Approved Access Scope Clear
- [ ] Conditions Documented
- [ ] Decision Date Recorded
- [ ] Evidence Retained

### Important

An approval must be sufficiently specific to support controlled fulfillment.

Ambiguous approvals should be clarified before implementation.

---

# 17. Step 11 — Record the Authorization

## 17.1 Objective

Maintain traceable evidence of the authorization decision.

## 17.2 Required Authorization Fields

| Field | Requirement |
|---|---|
| Request ID | Required |
| Approval Type | Required |
| Approver | Required |
| Decision | Required |
| Decision Date/Time | Required |
| Approved Scope | Required for approval |
| Conditions | When applicable |
| Expiration Date | When applicable |
| Evidence Reference | Required where approval is necessary |
| Request Status | Required |

## 17.3 Authorization Record

**Request ID:** SR-###

**Approval Authority:** [Role]

**Decision:** Pending

**Decision Date:** Not Applicable

**Approved Resource:** [Resource]

**Approved Permissions:** [Permissions]

**Conditions:** [Conditions or None]

**Expiration:** [Date or Not Applicable]

**Evidence:** Not Yet Available

## 17.4 Recordkeeping Procedure

1. Open the service request record.
2. Record the authorization decision.
3. Identify the approver.
4. Record the decision date and time.
5. Document the approved scope.
6. Record conditions.
7. Attach or reference supporting evidence.
8. Update the request status.
9. Confirm the record was saved.

### Important

Do not record approval as granted unless a valid approval or established preauthorization exists.

---

# 18. Step 12 — Handle Rejected or Deferred Requests

## 18.1 Rejected Requests

If a request is rejected:

1. Confirm the decision.
2. Record the approving authority.
3. Document the rejection reason.
4. Update the request status.
5. Notify the requester.
6. Identify an alternative when appropriate.
7. Route the record for closure.

## 18.2 Deferred Requests

If a request is deferred:

1. Record the reason.
2. Identify outstanding requirements.
3. Assign responsibility for follow-up.
4. Establish a review date when appropriate.
5. Update the status.
6. Communicate the delay.

## 18.3 Example Rejection Reasons

- Requester not eligible
- Insufficient business justification
- Security policy conflict
- Licensing unavailable
- Budget not approved
- Technical incompatibility
- Requested permissions excessive
- Required authorization denied

## 18.4 Example Rejection Message

**Subject:** Service Request SR-001 — Authorization Decision

Hello,

Your request has been reviewed and cannot be approved in its current form.

**Request:** [Description]  
**Decision:** Rejected  
**Reason:** [Approved explanation]

If your requirements change or additional information becomes available, please contact the IT Service Desk.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

### Important

Do not disclose confidential security details or unnecessary internal approval information when communicating a rejection.

---

# 19. Step 13 — Assess Change Enablement Requirements

## 19.1 Objective

Determine whether the requested action requires a separately controlled technical change.

## 19.2 Potential Change-Control Triggers

- Modification of shared infrastructure
- Network routing changes
- Firewall configuration changes
- Domain-wide policy changes
- Production server configuration changes
- Changes affecting multiple services
- Significant security configuration changes
- High-risk or nonstandard implementation

## 19.3 Change Assessment

| Field | Value |
|---|---|
| Technical Change Required | Pending |
| Change Control Applicable | Pending |
| Change Type | To Be Determined |
| Related Change ID | Not Applicable |
| Change Authorization | Pending if Required |

## 19.4 Procedure

1. Review the technical fulfillment requirements.
2. Determine whether an existing standard change model applies.
3. Identify nonstandard or higher-risk modifications.
4. Consult applicable Change Enablement requirements.
5. Create or link a change record when required.
6. Confirm the necessary change authorization before implementation.

## 19.5 Example

**Request:** Configure a new network segment for an employee group.

The service request may establish the business requirement.

The technical implementation may require a separate change record because it could affect network infrastructure.

### Important

Not every service request requires a separate change record.

The requirement depends on the organization's change policies and the nature of the technical activity.

---

# 20. Step 14 — Final Assessment Decision

## 20.1 Objective

Determine whether the request is ready for fulfillment.

## 20.2 Final Assessment Checklist

- [ ] Request record complete
- [ ] Requester identified
- [ ] Requested service available
- [ ] Eligibility verified
- [ ] Business justification evaluated
- [ ] Technical feasibility assessed
- [ ] Security requirements reviewed
- [ ] Cost and licensing evaluated
- [ ] Approval requirements identified
- [ ] Required approvals obtained
- [ ] Approval conditions documented
- [ ] Change requirements assessed
- [ ] Request ownership confirmed
- [ ] Fulfillment scope clearly defined

## 20.3 Final Decision Record

**Request ID:** SR-###

**Assessment Outcome:** Pending

**Authorization Status:** Pending

**Technical Feasibility:** Pending

**Security Review:** Pending

**Cost Review:** Pending

**Change Requirements:** Pending

**Approved Fulfillment Scope:** Not Yet Established

**Next Action:** Pending

## 20.4 Readiness Criteria

A request is ready for fulfillment when:

1. The request is sufficiently documented.
2. The service is available.
3. The affected user is eligible.
4. Technical prerequisites are understood.
5. Security requirements are satisfied.
6. Required approvals are valid.
7. Any applicable change controls are addressed.
8. The authorized scope is clear.
9. A responsible fulfillment role is identified.

### Important

A request must not be marked ready for fulfillment solely because an approval message was received.

All applicable prerequisites must be satisfied.

---

# 21. Handoff to Request Fulfillment

## 21.1 Handoff Objective

Transfer the authorized request to the responsible fulfillment technician with complete and accurate instructions.

## 21.2 Required Handoff Information

| Field | Requirement |
|---|---|
| Request ID | Required |
| Requester | Required |
| Affected User | When applicable |
| Requested Service | Required |
| Approved Resource | When applicable |
| Approved Permissions | When applicable |
| Business Justification | When applicable |
| Authorization Evidence | When required |
| Approval Conditions | When applicable |
| Technical Requirements | Required |
| Related Change ID | When applicable |
| Fulfillment Owner | Required |
| Request Status | Required |

## 21.3 Handoff Procedure

1. Confirm the final assessment outcome.
2. Verify authorization evidence.
3. Document the approved fulfillment scope.
4. Identify implementation restrictions.
5. Confirm the fulfillment technician or group.
6. Link applicable technical documentation.
7. Update the request status.
8. Transfer the request for fulfillment.

**Suggested Status:** Approved or Ready for Fulfillment

### Next Procedure

`Request-Fulfillment.md`

**Status:** Planned Procedure

### Important

The fulfillment technician should verify the authorization scope before making technical changes.

---

# 22. Practical Lab Example — Active Directory Folder Access

## 22.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-001  
**Scenario Type:** Service Request  
**Service:** IT-SVC-001 — Identity & Access Management  
**Request Type:** Shared Folder Access  
**Environment:** Active Directory Lab  
**Classification:** Proposed Simulation

### Business Context

An HR employee requests access to a departmental shared folder.

The Service Desk must determine whether the employee is eligible, whether the requested access is technically feasible, and whether the appropriate resource owner has authorized the permissions.

## 22.2 Example Lab Infrastructure

| Component | Example Configuration |
|---|---|
| Domain | homelab.local |
| Primary Domain Controller | DC01 |
| Secondary Domain Controller | DC02 |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Identity Platform | Active Directory Domain Services |

Current configurations must be verified before performing the scenario.

## 22.3 Example Assessment

| Assessment Area | Example Finding |
|---|---|
| Request Type | Shared Folder Access |
| Requested Service | IT-SVC-001 |
| Business Justification | Departmental responsibilities |
| User Eligibility | Pending Verification |
| Requested Resource | HR Shared Folder |
| Technical Feasibility | Pending Verification |
| Resource Owner Approval | Required Under Proposed Policy |
| Security Review | Least-Privilege Assessment |
| Final Authorization | Pending |

These findings are illustrative, not completed assessment results.

## 22.4 Lab Tasks

1. Open the simulated service request.
2. Review the request information.
3. Identify the affected employee.
4. Determine the requested folder permissions.
5. Review the business justification.
6. Inspect the applicable Active Directory environment.
7. Identify the relevant security group.
8. Determine whether the requested access is appropriate.
9. Identify the resource owner.
10. Simulate the authorization workflow.
11. Record the simulated approval decision.
12. Document the approved scope.
13. Prepare the request for fulfillment.

## 22.5 Technical Assessment Examples

The following commands may assist with verifying technical prerequisites.

They are examples and do not constitute execution evidence.

### Verify the User Account

```powershell
Get-ADUser -Identity "username" -Properties Enabled,Department |
Select-Object Name,SamAccountName,Enabled,Department
```

### Verify the Security Group

```powershell
Get-ADGroup -Identity "HR_Security_Group"
```

### Review Existing Group Membership

```powershell
Get-ADGroupMember -Identity "HR_Security_Group"
```

### Important

Replace placeholder account and group names with actual lab objects.

Read-only inspection does not authorize modifying group membership.

Do not execute access changes during the assessment stage.

## 22.6 Simulated Authorization

**Approver Role:** HR Resource Owner

**Approval Type:** Resource Access

**Decision:** To Be Simulated

**Approved Permissions:** To Be Determined

**Conditions:** To Be Determined

**Evidence:** Pending

### Important

Simulated approval demonstrates the workflow but is not independent authorization.

## 22.7 Expected Learning Outcomes

- Evaluate request eligibility.
- Apply business justification requirements.
- Assess technical feasibility.
- Identify access control requirements.
- Apply least-privilege principles.
- Determine the appropriate approver.
- Document authorization decisions.
- Separate assessment from technical fulfillment.
- Prepare an authorized fulfillment handoff.

## 22.8 Evidence to Capture

- Service request record
- Eligibility assessment
- Technical prerequisite checks
- Security assessment
- Approval requirement
- Simulated authorization decision
- Approved fulfillment scope
- Handoff documentation

---

# 23. Practical Lab Example — Microsoft 365 License Request

## 23.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-###  
**Service:** IT-SVC-003 — Microsoft 365 & Collaboration  
**Request Type:** License Assignment  
**Classification:** Proposed Simulation

### Business Context

An employee requests Microsoft 365 functionality requiring a license.

The Service Desk must assess the request before an administrator assigns the license.

## 23.2 Assessment Requirements

1. Identify the requested functionality.
2. Verify the employee's account.
3. Determine the required license.
4. Check license availability.
5. Identify any additional cost.
6. Evaluate the business justification.
7. Determine approval requirements.
8. Record the authorization decision.
9. Prepare the request for fulfillment.

## 23.3 Example Assessment Record

| Field | Example |
|---|---|
| Requested Service | Microsoft 365 |
| Required License | To Be Determined |
| License Available | Pending Verification |
| Additional Cost | Pending Assessment |
| Business Approval | Pending |
| Financial Approval | If Required |
| Authorization Status | Pending |
| Fulfillment Status | Not Started |

### Important

This example does not claim that a license has been purchased, assigned, or verified.

---

# 24. Common Assessment and Authorization Errors

| Error | Potential Consequence | Prevention |
|---|---|---|
| Approving incomplete requests | Incorrect fulfillment | Verify required information |
| Assuming eligibility | Unauthorized service access | Check service requirements |
| Missing business justification | Unsupported expenditure or access | Review business need |
| Ignoring technical prerequisites | Failed implementation | Assess feasibility |
| Granting excessive access | Security exposure | Apply least privilege |
| Accepting approval from the wrong person | Unauthorized access | Verify approval authority |
| Treating silence as approval | Unauthorized fulfillment | Require valid authorization |
| Ignoring licensing requirements | Compliance or cost issues | Verify license terms |
| Missing change assessment | Uncontrolled infrastructure changes | Evaluate change requirements |
| Failing to record approval conditions | Scope violations | Document restrictions |
| Modifying systems during assessment | Unauthorized changes | Separate assessment and fulfillment |
| Recording simulated approval as real | Misleading evidence | Label simulations clearly |

---

# 25. Metrics and Performance Measurement

Assessment and authorization activities may be evaluated using service metrics.

## 25.1 Proposed Metrics

| Metric | Description | Measurement |
|---|---|---|
| Request Assessment Time | Time spent assessing requests | Duration |
| Approval Turnaround Time | Time from approval request to decision | Duration |
| Requests Awaiting Approval | Number of requests pending authorization | Count |
| First-Pass Assessment Completeness | Requests assessed without additional clarification | Percentage |
| Authorization Documentation Completeness | Requests with required approval evidence | Percentage |
| Request Rejection Rate | Percentage of assessed requests rejected | Percentage |
| Approval Rework Rate | Requests requiring corrected or repeated authorization | Percentage |

## 25.2 Example Metric

**Metric:** Authorization Documentation Completeness

**Formula:**

```text
Authorization Documentation Completeness (%) =

Requests with Complete Required Authorization Evidence
------------------------------------------------------- x 100
       Requests Requiring Authorization
```

**Baseline:** Not Yet Established

**Target:** Not Yet Established

**Actual Result:** Not Yet Measured

## 25.3 Measurement Requirements

1. Define the reporting period.
2. Identify applicable request records.
3. Define complete authorization evidence.
4. Review actual records.
5. Calculate the result.
6. Document data quality.
7. Preserve evidence.
8. Identify improvement opportunities.

### Related Documentation

[Service Metrics Documentation Standards](../../Continual-Improvement/Service-Metrics/README.md)

[Service Metric Template](../../Templates/Service-Metric-Template.md)

### Important

No measured approval performance, established SLA, or automated reporting capability is claimed by this SOP.

---

# 26. Security and Compliance Considerations

## 26.1 Access Control

Authorization must consider:

- Identity verification
- Role-based access requirements
- Least privilege
- Resource ownership
- Privileged access
- Temporary access
- Sensitive information
- Separation of duties

## 26.2 Approval Evidence

Approval records should identify:

- The authorized decision-maker
- The affected user
- The requested resource
- The approved permissions
- Any conditions
- The decision date
- The related request

## 26.3 Sensitive Information

Do not record:

- Passwords
- MFA recovery codes
- Authentication tokens
- Private keys
- Unnecessary sensitive personal information

## 26.4 Publication Requirements

Before publishing lab documentation:

- Use fictional employee information.
- Sanitize sensitive configuration details.
- Distinguish simulated decisions from real authorization.
- Remove credentials and secrets.
- Avoid publishing confidential organizational information.

---

# 27. Records and Evidence

## 27.1 Required Records

Assessment and authorization should produce:

- Assessment findings
- Eligibility determination
- Business justification review
- Technical feasibility assessment
- Security assessment
- Cost and licensing assessment where applicable
- Authorization requirements
- Approval decision
- Approved fulfillment scope
- Request status update
- Fulfillment handoff information

## 27.2 Supporting Evidence

| Evidence Type | Purpose |
|---|---|
| Service Request Record | Establish request identity and scope |
| Eligibility Assessment | Document service eligibility |
| Technical Verification | Support feasibility findings |
| Approval Record | Document authorization |
| Security Review | Record security requirements |
| Licensing Review | Document license availability and cost |
| Change Record | Support applicable change control |
| Handoff Record | Establish fulfillment readiness |

## 27.3 Evidence Integrity

Do not fabricate:

- Approval decisions
- Authorization timestamps
- Technical verification
- License availability
- Security findings
- Change authorization
- Fulfillment readiness
- Requester communication

All simulated evidence must be labeled.

---

# 28. Continual Improvement

## 28.1 Potential Improvements

- Standardized approval matrices
- Predefined request models
- Clearer eligibility requirements
- Improved request forms
- Automated approval routing
- Reduced unnecessary approval steps
- Better licensing visibility
- Improved authorization evidence
- Standardized security reviews
- Better handoff documentation

## 28.2 Improvement Procedure

1. Identify an assessment inefficiency.
2. Collect supporting observations.
3. Evaluate the operational impact.
4. Propose an improvement.
5. Record the opportunity.
6. Assess risk and feasibility.
7. Obtain necessary authorization.
8. Implement the improvement.
9. Measure the outcome.
10. Update this SOP when appropriate.

## 28.3 Related Documentation

[Improvement Management SOP](../../Continual-Improvement/Procedures/Improvement-Management.md)

[Improvement Register](../../Continual-Improvement/Improvement-Register.md)

[Improvement Template](../../Templates/Improvement-Template.md)

---

# 29. Procedure Quality Checklist

## Process Definition

- [ ] Purpose documented
- [ ] Scope established
- [ ] Roles defined
- [ ] Assessment workflow documented
- [ ] Authorization requirements explained
- [ ] Decision outcomes defined
- [ ] Fulfillment handoff requirements established

## Assessment

- [ ] Request completeness reviewed
- [ ] Service eligibility assessed
- [ ] Business justification evaluated
- [ ] Technical feasibility reviewed
- [ ] Security requirements considered
- [ ] Cost and licensing evaluated
- [ ] Change requirements assessed

## Authorization

- [ ] Approval authority identified
- [ ] Approval scope defined
- [ ] Approval request documented
- [ ] Decision recorded
- [ ] Conditions documented
- [ ] Evidence retained
- [ ] Rejections and deferrals addressed

## Security

- [ ] Least privilege considered
- [ ] Privileged access reviewed where applicable
- [ ] Separation of duties considered
- [ ] Sensitive information protected
- [ ] Unauthorized fulfillment prevented

## Lab Readiness

- [ ] Example scenarios included
- [ ] Technical assessment methods identified
- [ ] Simulated approvals clearly labeled
- [ ] No fabricated execution results
- [ ] Evidence requirements documented

## Documentation

- [ ] SOP identifier correct
- [ ] Version recorded
- [ ] Related procedures referenced
- [ ] Relative links verified
- [ ] Revision history maintained

---

# 30. Document Review and Revision History

## 30.1 Review Triggers

Review this SOP when:

- Service eligibility requirements change.
- Approval authorities change.
- New services are introduced.
- Security policies are updated.
- Licensing requirements change.
- ITSM approval workflows change.
- Change control requirements change.
- Assessment quality reviews identify issues.
- Continual improvement initiatives introduce process changes.

## 30.2 Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Request Assessment and Authorization SOP aligned with ITIL 4 Service Request Management |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This SOP establishes a proposed standard for evaluating employee IT service requests, determining eligibility, assessing technical and security requirements, obtaining authorization, and preparing requests for fulfillment.

Organizational roles, approval authorities, authorization matrices, employee requests, and operational scenarios may be fictional or proposed.

Actual technical assessments, licensing checks, approval decisions, and request processing activities must be supported by documented lab evidence.

Simulated approvals are instructional examples and do not constitute independent authorization or professional employment experience.

Jira Service Management and associated automation capabilities are planned unless implementation and verification are explicitly documented.

This procedure demonstrates service eligibility assessment, business justification review, technical feasibility evaluation, access control awareness, authorization governance, and controlled fulfillment preparation.
