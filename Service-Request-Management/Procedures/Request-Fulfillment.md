# SOP-SRM-003 — Request Fulfillment

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Service Request Management  
**Document Type:** Standard Operating Procedure (SOP)  
**SOP ID:** SOP-SRM-003  
**Version:** 1.0  
**Status:** Draft — Proposed Operating Standard  
**Process Owner:** Internal IT  
**Primary Responsible Function:** Service Request Management  
**Effective Date:** Pending Adoption  
**Last Reviewed:** Not Yet Reviewed  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

# 1. Purpose

Establish a standardized procedure for fulfilling authorized employee IT service requests safely, consistently, and efficiently.

This procedure ensures that fulfillment activities follow the approved scope, applicable technical requirements, security policies, and organizational standards.

The objectives are to:

- Verify authorization before performing technical work.
- Confirm the request is ready for fulfillment.
- Identify the appropriate fulfillment technician.
- Prepare the required systems and resources.
- Execute approved service request activities.
- Apply least-privilege principles.
- Prevent unauthorized configuration changes.
- Verify successful fulfillment.
- Document technical actions and results.
- Communicate fulfillment outcomes.
- Prepare completed requests for closure.
- Support knowledge management and continual improvement.

**Key Principle:** Request fulfillment must remain within the authorized scope and must be verified before the request is considered completed.

---

# 2. Scope

## 2.1 In Scope

This procedure applies to authorized employee IT service requests, including:

- User account creation
- User account modifications
- Password reset requests
- Security group membership changes
- Shared folder access
- Microsoft 365 license assignments
- Microsoft Entra ID user administration
- Microsoft Intune device enrollment
- Approved software installations
- Device provisioning
- Hardware replacement requests
- Standard network access requests
- Employee onboarding activities
- Employee role changes
- Other approved service catalog requests

## 2.2 Out of Scope

This procedure does not replace:

- Request logging
- Request assessment and authorization
- Incident investigation
- Problem investigation
- Formal change authorization
- Security incident response
- Service request closure

These activities are governed by their respective procedures.

## 2.3 Supported Environments

Depending on the request, fulfillment may involve:

- Windows 11
- Windows Server
- Active Directory Domain Services
- Microsoft Entra ID
- Microsoft 365
- Microsoft Intune
- Microsoft Azure
- Hyper-V
- Network infrastructure
- ITSM platforms

System availability, administrative access, licensing, and current configuration must be verified before fulfillment.

---

# 3. ITIL 4 Alignment

This SOP supports the ITIL 4 Service Request Management practice.

Service Request Management handles predefined, user-initiated service requests in a controlled and user-friendly manner.

Request Fulfillment performs the approved work required to deliver the requested service.

## 3.1 Related ITIL Practices

| Practice | Relationship |
|---|---|
| Service Desk | Coordinates communication and request ownership |
| Service Request Management | Controls the request fulfillment workflow |
| Knowledge Management | Provides technical fulfillment instructions |
| Information Security Management | Defines access and security requirements |
| Service Configuration Management | Maintains relevant configuration information |
| Change Enablement | Governs technical changes requiring change control |
| Monitoring and Event Management | May provide technical verification or event evidence |
| Continual Improvement | Evaluates fulfillment performance and improvement opportunities |

## 3.2 Practice Boundaries

Service Request Management coordinates the delivery of an authorized service.

Information Security Management establishes security requirements.

Change Enablement governs changes requiring formal authorization.

Service Configuration Management maintains information about relevant configuration items and relationships.

These practices may interact during fulfillment without representing separate organizational departments.

### Important

An approved service request does not automatically authorize every technical action needed to complete it.

Additional change authorization or security review may be required.

---

# 4. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Requester | Provides information and participates in verification when required |
| Service Desk Technician | Coordinates communication and request tracking |
| Request Owner | Maintains overall responsibility for the request record |
| Fulfillment Technician | Performs approved technical activities |
| IT Administrator | Performs tasks requiring elevated permissions |
| Service Owner | Defines service requirements and fulfillment standards |
| Resource Owner | Establishes access requirements for owned resources |
| Security Administrator | Supports security-sensitive fulfillment |
| Change Authority | Authorizes applicable technical changes |
| Reviewer | Verifies fulfillment results when independent review is required |

## 4.1 Fulfillment Technician Responsibilities

The fulfillment technician should:

1. Review the request.
2. Verify authorization.
3. Confirm the approved scope.
4. Review technical prerequisites.
5. Confirm administrative permissions.
6. Identify relevant technical documentation.
7. Prepare the environment.
8. Perform the authorized work.
9. Verify the result.
10. Document the actions taken.
11. Communicate the outcome.
12. Prepare the request for closure.

## 4.2 Request Owner Responsibilities

The request owner should:

- Track request progress.
- Coordinate assignments.
- Identify delays.
- Ensure required approvals remain valid.
- Maintain the request record.
- Coordinate communication.
- Confirm that fulfillment evidence is available.

## 4.3 Separation of Duties

For sensitive activities, the organization may require separate individuals to:

- Request the service.
- Approve the service.
- Implement the service.
- Verify the result.

A technician's administrative privileges do not automatically grant authority to approve their own access request.

---

# 5. Fulfillment Principles

All fulfillment activities should follow these principles.

## 5.1 Authorization First

Perform only actions supported by valid authorization or an established preauthorized request model.

## 5.2 Least Privilege

Use only the permissions necessary to complete the approved task.

## 5.3 Approved Scope

Do not expand the request beyond the approved service, user, resource, or permission level.

## 5.4 Technical Accuracy

Verify target systems, accounts, and configuration details before making changes.

## 5.5 Change Control

Follow applicable Change Enablement requirements.

## 5.6 Security

Protect credentials, sensitive information, and privileged access.

## 5.7 Verification

Confirm that the requested service was delivered correctly.

## 5.8 Traceability

Document actions, outcomes, and supporting evidence.

## 5.9 Communication

Keep the requester informed when appropriate.

## 5.10 Continuous Learning

Use fulfillment experience to improve technical documentation and operational procedures.

---

# 6. Request Fulfillment Workflow

## 6.1 High-Level Workflow

```text
Authorized Service Request
          |
          v
Review Request and Approval
          |
          v
Confirm Fulfillment Readiness
          |
          v
Assign Fulfillment Technician
          |
          v
Review Technical Documentation
          |
          v
Prepare Environment
          |
          v
Verify Target and Scope
          |
          v
Perform Authorized Work
          |
          v
Verify Technical Result
          |
          v
Was Fulfillment Successful?
       /             \
      No             Yes
      |               |
      v               v
Investigate       Document Results
or Escalate            |
      |               v
      v           Notify Requester
Resolve or            |
Record Blocker        v
      |           Prepare Closure
      +---------------+
```

## 6.2 Fulfillment Outcomes

| Outcome | Description | Next Action |
|---|---|---|
| Successful | Approved service delivered and verified | Prepare closure |
| Partially Successful | Some approved activities completed | Document outstanding work |
| Blocked | Fulfillment cannot proceed | Resolve blocker or escalate |
| Failed | Technical action did not achieve the intended result | Troubleshoot and assess recovery |
| Deferred | Fulfillment postponed | Record reason and next action |
| Cancelled | Request withdrawn before completion | Document cancellation |
| Unauthorized Scope | Required authorization missing or insufficient | Stop and obtain authorization |

### Important

A technical command completing without an error does not necessarily prove successful service delivery.

Verification must evaluate the intended outcome.

---

# 7. Step 1 — Review the Authorized Request

## 7.1 Objective

Confirm that the request has completed the necessary assessment and authorization activities.

## 7.2 Required Information

| Field | Requirement |
|---|---|
| Request ID | Required |
| Requester | Required |
| Affected User | When applicable |
| Requested Service | Required |
| Approved Scope | Required |
| Authorization Status | Required |
| Approval Evidence | When required |
| Fulfillment Owner | Required |
| Technical Requirements | Required |
| Related Change ID | When applicable |
| Current Request Status | Required |

## 7.3 Procedure

1. Open the service request record.
2. Confirm the request identifier.
3. Review the requested service.
4. Identify the affected user or resource.
5. Review the approved fulfillment scope.
6. Verify authorization requirements.
7. Review approval conditions.
8. Identify any outstanding prerequisites.
9. Confirm the request is ready for implementation.

## 7.4 Authorization Verification

- [ ] Correct request identified
- [ ] Approval requirements satisfied
- [ ] Approver authority established
- [ ] Approved resource identified
- [ ] Approved permissions documented
- [ ] Approval conditions reviewed
- [ ] Approval remains applicable
- [ ] Required change authorization obtained

### Important

Do not begin fulfillment when authorization is missing, expired, ambiguous, or inconsistent with the requested action.

---

# 8. Step 2 — Confirm Fulfillment Readiness

## 8.1 Objective

Determine whether the necessary resources, permissions, and technical prerequisites are available.

## 8.2 Readiness Assessment

| Requirement | Status | Notes |
|---|---|---|
| Request Authorized | Pending | [Details] |
| Target System Available | Pending | [Details] |
| Required Permissions Available | Pending | [Details] |
| Technical Prerequisites Met | Pending | [Details] |
| Required License Available | Pending | [Details] |
| Change Control Satisfied | Pending | [Details] |
| Fulfillment Documentation Available | Pending | [Details] |
| Recovery Requirements Reviewed | Pending | [Details] |

## 8.3 Procedure

1. Review the technical requirements.
2. Confirm the target environment.
3. Verify system availability.
4. Confirm administrative permissions.
5. Check required licenses or resources.
6. Identify dependencies.
7. Review implementation risks.
8. Confirm whether additional change control applies.
9. Record readiness findings.

## 8.4 Readiness Outcomes

- Ready
- Ready with Conditions
- Not Ready
- Additional Assessment Required

### Important

Do not treat a proposed system, license, or integration as available until its actual status has been verified.

---

# 9. Step 3 — Assign the Fulfillment Technician

## 9.1 Objective

Assign the work to an individual or group with the appropriate technical capabilities and permissions.

## 9.2 Assignment Considerations

- Requested service
- Required technical skills
- Administrative privileges
- Service ownership
- Security restrictions
- Workload
- Availability
- Change control requirements

## 9.3 Example Assignments

| Request Type | Potential Responsible Role |
|---|---|
| Standard Account Creation | Service Desk or Identity Administrator |
| AD Security Group Membership | Authorized Identity Administrator |
| Shared Folder Permissions | Authorized Systems Administrator |
| Microsoft 365 License Assignment | Microsoft 365 Administrator |
| Intune Device Enrollment | Endpoint Administrator |
| Software Installation | Endpoint Support |
| Network Access Configuration | Network Administrator |
| Server Resource Provisioning | Systems Administrator |

These assignments are illustrative.

## 9.4 Procedure

1. Identify the required technical role.
2. Confirm that the technician is authorized.
3. Assign the fulfillment task.
4. Record ownership.
5. Identify any required escalation.
6. Confirm the next action.

---

# 10. Step 4 — Review Technical Documentation

## 10.1 Objective

Identify existing technical guidance that supports consistent and accurate fulfillment.

## 10.2 Documentation Sources

Potential sources include:

- Knowledge articles
- Technical runbooks
- Vendor documentation
- Service Catalog entries
- Configuration Item records
- Dependency maps
- Change records
- Security policies
- Previous verified lab procedures

## 10.3 Procedure

1. Identify the requested technical activity.
2. Search for an applicable knowledge article.
3. Confirm that the documentation applies to the current environment.
4. Review prerequisites.
5. Review security requirements.
6. Identify verification steps.
7. Identify recovery or rollback requirements where relevant.
8. Document the guidance used.

## 10.4 Knowledge Article Assessment

| Field | Value |
|---|---|
| Knowledge Article | [Reference] |
| Article Status | [Draft / Verified / Retired] |
| Applicable Environment | [Environment] |
| Last Verified | [Date] |
| Additional Validation Required | [Yes / No] |

### Important

A knowledge article may describe how to perform a technical task.

It does not independently authorize the task.

If no verified article exists, use approved technical documentation and document the actual steps taken.

---

# 11. Step 5 — Prepare the Environment

## 11.1 Objective

Ensure that fulfillment can be performed without unnecessary disruption or security risk.

## 11.2 Preparation Activities

Depending on the request:

- Verify administrative connectivity.
- Confirm target device availability.
- Check service health.
- Confirm required licenses.
- Verify account and group existence.
- Review relevant dependencies.
- Check available storage or capacity.
- Identify active maintenance restrictions.
- Confirm backups or recovery options where necessary.
- Notify affected users when required.

## 11.3 Preparation Record

**Request ID:** SR-###

**Target System:** [System]

**Target Resource:** [Resource]

**Administrative Tool:** [Tool]

**Prerequisites:** [List]

**Potential Impact:** [Description]

**Recovery Requirements:** [Description]

**Preparation Status:** Pending

## 11.4 Procedure

1. Identify the target environment.
2. Verify access to required tools.
3. Confirm the target system is available.
4. Check relevant service dependencies.
5. Verify technical prerequisites.
6. Identify implementation risks.
7. Review recovery requirements.
8. Record preparation results.

### Important

For higher-risk work, confirm applicable backup, rollback, maintenance-window, and change-control requirements before implementation.

---

# 12. Step 6 — Verify the Target and Approved Scope

## 12.1 Objective

Prevent changes to incorrect users, devices, resources, or permissions.

## 12.2 Target Verification

| Item | Expected Value | Verified Value | Status |
|---|---|---|---|
| User Account | [Expected] | [Observed] | Pending |
| Target Device | [Expected] | [Observed] | Pending |
| Target Resource | [Expected] | [Observed] | Pending |
| Requested Permission | [Expected] | [Observed] | Pending |
| Approved Scope | [Expected] | [Observed] | Pending |

## 12.3 Procedure

1. Confirm the affected user.
2. Confirm the target system.
3. Confirm the requested resource.
4. Review the approved permissions.
5. Compare the intended action against the authorization.
6. Resolve discrepancies before proceeding.

## 12.4 Scope Restrictions

Do not:

- Grant additional permissions without authorization.
- Modify unrelated accounts.
- Change unrelated configurations.
- Assign unapproved licenses.
- Provision additional cloud resources.
- Remove existing access without justification.
- Expand a request beyond its approved boundaries.

### Important

When the actual environment differs from the approved request, stop and reassess rather than improvising an unauthorized change.

---

# 13. Step 7 — Perform the Authorized Work

## 13.1 Objective

Execute the approved service request using appropriate administrative tools and documented procedures.

## 13.2 General Fulfillment Procedure

1. Confirm readiness.
2. Verify the target.
3. Confirm authorization.
4. Open the required administrative tool.
5. Perform the approved technical action.
6. Observe system responses.
7. Record errors or warnings.
8. Avoid unrelated changes.
9. Preserve relevant execution evidence.
10. Proceed to verification.

## 13.3 Supported Fulfillment Methods

| Method | Example |
|---|---|
| Graphical Administration | ADUC, ADAC, Microsoft 365 Admin Center |
| Command-Line Administration | PowerShell, Windows CLI |
| Remote Administration | RSAT, Windows Admin Center |
| Endpoint Administration | Microsoft Intune |
| Network Administration | Device CLI or management interface |
| ITSM-Guided Workflow | Manual or configured request tasks |

## 13.4 Execution Record

**Request ID:** SR-###

**Technician:** [Role]

**Execution Date:** Pending

**Target System:** [System]

**Approved Action:** [Action]

**Tool Used:** [Tool]

**Execution Result:** Not Yet Performed

**Evidence Reference:** Not Available

### Important

Document the actual commands, settings, or administrative actions performed.

Do not record proposed commands as executed actions.

---

# 14. Step 8 — Verify Fulfillment

## 14.1 Objective

Confirm that the authorized service was delivered correctly.

## 14.2 Verification Principles

Verification should establish:

- The intended technical change occurred.
- The correct user or resource was affected.
- The resulting configuration matches the authorization.
- The requested service is functional.
- No known unintended changes occurred.
- Applicable security requirements remain satisfied.

## 14.3 Verification Methods

| Method | Example |
|---|---|
| Configuration Inspection | Review account or group membership |
| Functional Testing | Confirm the requested service works |
| Command Output | Query the resulting configuration |
| Administrative Portal | Review license or device status |
| Event Logs | Check relevant system events |
| Requester Confirmation | Confirm the employee can use the service |
| Independent Review | Another authorized technician validates the result |

## 14.4 Verification Procedure

1. Review the expected outcome.
2. Select an appropriate verification method.
3. Inspect the resulting configuration.
4. Perform functional testing where applicable.
5. Confirm that the result matches the approved scope.
6. Review unexpected behavior.
7. Record actual findings.
8. Preserve supporting evidence.

## 14.5 Verification Record

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| Approved Action Applied | [Expected] | Not Tested | Pending |
| Correct Target Modified | [Expected] | Not Tested | Pending |
| Requested Service Functional | [Expected] | Not Tested | Pending |
| Security Requirements Satisfied | [Expected] | Not Tested | Pending |
| Unintended Changes Identified | None Expected | Not Evaluated | Pending |

### Important

Verification should be based on actual observations.

Do not mark fulfillment successful solely because the implementation command returned without an error.

---

# 15. Step 9 — Handle Fulfillment Failures

## 15.1 Objective

Respond consistently when fulfillment fails, produces unexpected results, or cannot be completed.

## 15.2 Failure Categories

| Category | Example |
|---|---|
| Permission Failure | Technician lacks required administrative rights |
| Missing Resource | Requested account or group does not exist |
| Licensing Failure | Required license unavailable |
| Connectivity Failure | Target system unreachable |
| Configuration Conflict | Existing settings prevent fulfillment |
| Technical Error | Administrative command fails |
| Authorization Conflict | Required action exceeds approved scope |
| Service Disruption | Implementation affects an existing service |

## 15.3 Failure Response Procedure

1. Stop the affected activity when appropriate.
2. Record the error or unexpected result.
3. Determine whether the system remains in a safe state.
4. Assess operational impact.
5. Review applicable recovery instructions.
6. Restore the previous state when necessary and authorized.
7. Identify whether troubleshooting or escalation is required.
8. Update the request record.
9. Communicate relevant delays.
10. Resume only when prerequisites and authorization are satisfied.

## 15.4 Recovery and Rollback

Recovery requirements depend on the technical activity.

Examples include:

- Removing an incorrectly assigned group membership
- Reversing an unauthorized configuration
- Restoring a previous application configuration
- Reverting an approved change using its rollback plan
- Restoring a service affected by an implementation error

### Important

Rollback actions can themselves introduce risk.

Follow applicable change-control and security requirements.

## 15.5 Incident Creation

If fulfillment causes an unplanned service interruption or degradation:

1. Assess the impact.
2. Record the incident through the appropriate process.
3. Link the incident to the original service request.
4. Coordinate service restoration.
5. Preserve relevant technical evidence.

A failed service request does not automatically become an incident unless an actual service interruption or degradation has occurred.

---

# 16. Step 10 — Document Fulfillment Results

## 16.1 Objective

Maintain an accurate record of what was performed and verified.

## 16.2 Required Documentation

| Field | Requirement |
|---|---|
| Request ID | Required |
| Fulfillment Technician | Required |
| Execution Date/Time | Required |
| Target System | When applicable |
| Target Resource | When applicable |
| Technical Actions | Required |
| Tools Used | When applicable |
| Configuration Changes | When applicable |
| Verification Method | Required |
| Verification Results | Required |
| Errors or Warnings | When applicable |
| Recovery Actions | When applicable |
| Related Records | When applicable |
| Evidence References | When available |
| Final Fulfillment Status | Required |

## 16.3 Documentation Procedure

1. Open the request record.
2. Record the actions performed.
3. Identify the affected systems.
4. Record significant configuration changes.
5. Document verification results.
6. Record errors and recovery actions.
7. Attach or reference supporting evidence.
8. Update the fulfillment status.
9. Confirm the record is accurate.

## 16.4 Example Fulfillment Summary

**Request ID:** SR-###

**Requested Service:** [Service]

**Approved Action:** [Action]

**Technical Work Performed:** [Actual Work]

**Verification Method:** [Method]

**Verification Result:** [Result]

**Outstanding Issues:** [Issues or None]

**Fulfillment Status:** [Status]

**Evidence:** [Reference]

### Important

A request record should explain what actually happened, not merely repeat the intended work.

---

# 17. Step 11 — Update Configuration Documentation

## 17.1 Objective

Maintain accurate configuration information when fulfillment changes a tracked configuration item or service dependency.

## 17.2 Potential Updates

- Server configuration
- Workstation configuration
- Installed software
- Device ownership
- Assigned licenses
- Network configuration
- Service dependencies
- Resource relationships
- Configuration baselines

## 17.3 Procedure

1. Determine whether the fulfilled request affected a tracked configuration item.
2. Identify the relevant CI record.
3. Compare the documented configuration with the verified result.
4. Update the CI record when required.
5. Record the related request or change reference.
6. Update dependency information when necessary.
7. Preserve supporting evidence.

## 17.4 Configuration Record

**Related CI:** CI-###

**Configuration Changed:** [Yes / No]

**Baseline Update Required:** [Yes / No]

**Dependency Map Update Required:** [Yes / No]

**Documentation Status:** Pending

### Important

Not every service request requires a configuration record update.

Apply the organization's configuration management scope and documentation requirements.

---

# 18. Step 12 — Communicate the Fulfillment Outcome

## 18.1 Objective

Inform the requester of the fulfillment result and any required next steps.

## 18.2 Communication Requirements

The communication should include:

- Request reference
- Service delivered
- Fulfillment status
- Relevant instructions
- Required user actions
- Known limitations
- Verification or confirmation requirements

## 18.3 Example Completion Message

**Subject:** Service Request SR-001 — Fulfillment Update

Hello,

The requested service has been implemented.

**Request:** [Description]  
**Service Delivered:** [Description]  
**Status:** Pending Final Verification

Please verify that the service works as expected and report any remaining issues.

Thank you,  
Technical Techno Tech  
IT Service Desk

**Example Classification:** Illustrative Communication — Not Actually Sent

## 18.4 Procedure

1. Review the fulfillment result.
2. Confirm that the message accurately describes the work performed.
3. Identify any required user verification.
4. Communicate through an approved channel.
5. Record the communication.
6. Update the request status.

### Important

Do not state that fulfillment is complete if technical verification remains outstanding.

---

# 19. Step 13 — Prepare the Request for Closure

## 19.1 Objective

Ensure that fulfillment documentation and verification are sufficient for final request closure.

## 19.2 Closure Readiness Checklist

- [ ] Approved scope fulfilled
- [ ] Technical work documented
- [ ] Verification completed
- [ ] Errors addressed or documented
- [ ] Relevant configuration records updated
- [ ] Required evidence retained
- [ ] Requester notified
- [ ] Outstanding actions identified
- [ ] Request status accurate
- [ ] Request owner informed

## 19.3 Closure Readiness Outcomes

| Outcome | Next Action |
|---|---|
| Ready for Closure | Transfer to closure procedure |
| Pending User Verification | Await applicable confirmation |
| Partially Fulfilled | Continue or reassess outstanding work |
| Blocked | Resolve blocker or escalate |
| Failed | Troubleshoot or follow recovery procedure |
| Cancelled | Document cancellation and proceed to appropriate closure handling |

## 19.4 Handoff Procedure

1. Confirm the final fulfillment status.
2. Review verification evidence.
3. Confirm that the requester was informed.
4. Identify outstanding actions.
5. Update the request record.
6. Transfer the request to closure.

### Next Procedure

`Request-Closure.md`

**Status:** Planned Procedure

---

# 20. Practical Lab Example — Active Directory Group Membership

## 20.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-001  
**Scenario Type:** Service Request  
**Service:** IT-SVC-001 — Identity & Access Management  
**Request Type:** Shared Folder Access  
**Environment:** Active Directory Lab  
**Classification:** Proposed Simulation

### Business Context

An HR employee requests access to a departmental shared folder.

The request has completed a simulated assessment and authorization process.

An authorized technician must implement the approved access and verify the result.

## 20.2 Example Lab Infrastructure

| Component | Example Configuration |
|---|---|
| Domain | homelab.local |
| Primary Domain Controller | DC01 |
| Secondary Domain Controller | DC02 |
| Management Workstation | MGMT01 |
| Client Workstation | CLIENT01 |
| Identity Platform | Active Directory Domain Services |

Current configurations must be verified before performing the scenario.

## 20.3 Proposed Fulfillment Requirements

- The target user account exists.
- The appropriate security group exists.
- The approved permissions are documented.
- The technician has sufficient administrative rights.
- The group grants the intended resource access.
- The change does not exceed the approved scope.

## 20.4 Step 1 — Verify the User

Run from an authorized management environment with the Active Directory PowerShell module available.

```powershell
Get-ADUser -Identity "username" -Properties Enabled,Department |
Select-Object Name,SamAccountName,Enabled,Department
```

**Expected Result:** The intended account is found and its relevant attributes can be reviewed.

**Actual Result:** Not Yet Tested

## 20.5 Step 2 — Verify the Security Group

```powershell
Get-ADGroup -Identity "HR_Security_Group" |
Select-Object Name,GroupScope,GroupCategory
```

**Expected Result:** The intended security group exists.

**Actual Result:** Not Yet Tested

## 20.6 Step 3 — Review Existing Membership

```powershell
Get-ADGroupMember -Identity "HR_Security_Group"
```

**Expected Result:** Existing group membership is displayed.

**Actual Result:** Not Yet Tested

## 20.7 Step 4 — Add the Approved User

Perform this step only after authorization and target verification.

```powershell
Add-ADGroupMember -Identity "HR_Security_Group" -Members "username"
```

**Expected Result:** The approved account is added to the intended security group.

**Actual Result:** Not Yet Executed

### Important

The example group name is a placeholder.

Confirm that the selected group provides the approved access and does not grant unintended permissions.

## 20.8 Step 5 — Verify Membership

```powershell
Get-ADGroupMember -Identity "HR_Security_Group" |
Where-Object SamAccountName -eq "username"
```

**Expected Result:** The target user appears in the group's membership.

**Actual Result:** Not Yet Tested

## 20.9 Step 6 — Verify Resource Access

Group membership alone does not prove that the employee can access the requested folder.

Additional verification may include:

1. Confirming the group has the intended resource permissions.
2. Confirming the employee's effective access.
3. Testing access from an authorized workstation.
4. Verifying that access is limited to the approved scope.
5. Documenting any replication or sign-in refresh requirements.

**Functional Verification:** Pending

## 20.10 Lab Evidence

Capture:

- Request authorization record
- User account verification
- Group verification
- Membership before the change
- Actual implementation output
- Membership after the change
- Functional access verification
- Final request record

### Important

This example is instructional.

Commands, expected results, and simulated approvals are not evidence that the activity has been completed.

---

# 21. Practical Lab Example — Microsoft 365 License Assignment

## 21.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-###  
**Service:** IT-SVC-003 — Microsoft 365 & Collaboration  
**Request Type:** License Assignment  
**Classification:** Proposed Simulation

### Business Context

An employee requires Microsoft 365 functionality for an approved business purpose.

The fulfillment technician must verify the authorized license assignment and confirm that the intended license is available.

## 21.2 Fulfillment Prerequisites

- Valid service request
- Appropriate authorization
- Existing user account
- Available license
- Required administrative permissions
- Applicable usage location and licensing requirements
- Confirmed assignment scope

## 21.3 Proposed Fulfillment Procedure

1. Open the Microsoft 365 Admin Center.
2. Locate the intended user.
3. Verify the user identity.
4. Review existing license assignments.
5. Confirm the requested license is available.
6. Verify that the assignment is authorized.
7. Assign the approved license.
8. Save the changes.
9. Review the resulting assignment.
10. Confirm the required service is available.
11. Document the result.

## 21.4 Verification

| Verification Item | Expected Result | Actual Result |
|---|---|---|
| Correct User | Intended account selected | Pending |
| Correct License | Approved product assigned | Pending |
| Assignment Status | License successfully assigned | Pending |
| Service Availability | Required functionality available | Pending |
| Additional Cost | Matches authorization | Pending |

### Important

This example does not claim that a license has been purchased, assigned, or verified.

Microsoft 365 and Azure licensing requirements must be checked against the actual environment.

---

# 22. Practical Lab Example — Approved Software Installation

## 22.1 Scenario Overview

**Scenario ID:** SCN-###  
**Request ID:** SR-###  
**Service:** IT-SVC-002 — Endpoint Management  
**Request Type:** Software Installation  
**Classification:** Proposed Simulation

### Business Context

An employee requests installation of an approved application on a company-managed workstation.

## 22.2 Fulfillment Prerequisites

- Software approved for use
- Valid license where required
- Compatible operating system
- Appropriate installation permissions
- Approved target device
- Required security review completed
- Installation source verified

## 22.3 Proposed Fulfillment Procedure

1. Review the authorized request.
2. Identify the approved software.
3. Verify the target workstation.
4. Confirm compatibility.
5. Confirm licensing.
6. Obtain the software from an approved source.
7. Install using the approved method.
8. Verify successful installation.
9. Launch or test the application where appropriate.
10. Document the installation and verification.

## 22.4 Potential Tools

- Windows Settings
- Approved installation packages
- PowerShell
- Microsoft Intune
- Endpoint management tools

## 22.5 Verification

- Application appears installed.
- Installed version matches requirements.
- Application launches successfully.
- Required functionality works.
- No known security or compatibility issues are introduced.

### Important

Do not claim that an Intune application deployment has been configured unless it has actually been created and tested.

---

# 23. Common Fulfillment Errors

| Error | Potential Consequence | Prevention |
|---|---|---|
| Missing authorization | Unauthorized service delivery | Verify approval before work |
| Incorrect target account | Access granted to wrong user | Confirm identity |
| Incorrect security group | Excessive or incorrect access | Verify group purpose |
| Unapproved license assignment | Unexpected cost or compliance issue | Check authorization |
| Missing technical prerequisites | Failed implementation | Perform readiness checks |
| Outdated knowledge article | Incorrect procedure | Verify documentation |
| Uncontrolled configuration change | Service disruption | Apply change requirements |
| No functional verification | Undetected fulfillment failure | Test intended outcome |
| Incomplete documentation | Poor traceability | Record actual actions |
| Missing requester communication | Confusion about service status | Provide updates |
| Missing CI update | Inaccurate configuration records | Review configuration impact |
| Premature closure | Unresolved request | Confirm closure readiness |

---

# 24. Metrics and Performance Measurement

Request Fulfillment may be evaluated using service metrics.

## 24.1 Proposed Metrics

| Metric | Description | Measurement |
|---|---|---|
| Request Fulfillment Time | Time spent completing fulfillment | Duration |
| End-to-End Request Completion Time | Time from request receipt to completion | Duration |
| First-Time Fulfillment Success Rate | Requests fulfilled successfully without rework | Percentage |
| Fulfillment Rework Rate | Requests requiring corrective work | Percentage |
| Fulfillment Verification Rate | Requests with documented verification | Percentage |
| Request Backlog | Outstanding requests awaiting fulfillment | Count |
| Fulfillment Failure Rate | Requests with unsuccessful implementation | Percentage |
| Fulfillment Documentation Completeness | Requests with required evidence | Percentage |

## 24.2 Example Metric

**Metric:** Fulfillment Verification Rate

**Formula:**

```text
Fulfillment Verification Rate (%) =

Fulfilled Requests with Documented Verification
----------------------------------------------- x 100
          Total Fulfilled Requests
```

**Baseline:** Not Yet Established

**Target:** Not Yet Established

**Actual Result:** Not Yet Measured

## 24.3 Measurement Requirements

1. Define the reporting period.
2. Identify applicable request records.
3. Define acceptable verification evidence.
4. Collect actual fulfillment results.
5. Calculate the metric.
6. Validate data quality.
7. Document limitations.
8. Identify improvement opportunities.

## 24.4 Related Documentation

[Service Metrics Documentation Standards](../../Continual-Improvement/Service-Metrics/README.md)

[Service Metric Template](../../Templates/Service-Metric-Template.md)

### Important

No fulfillment performance targets, achieved results, or automated reporting capabilities are claimed by this SOP.

---

# 25. Security and Compliance Considerations

## 25.1 Least Privilege

Fulfillment technicians should use only the permissions necessary for the approved task.

## 25.2 Privileged Access

Sensitive activities may require:

- Dedicated administrative accounts
- Additional authorization
- MFA
- Time-limited privileges
- Audit logging
- Independent verification

## 25.3 Credential Protection

Do not record:

- Passwords
- MFA recovery codes
- Authentication tokens
- API secrets
- Private keys

## 25.4 Sensitive Resources

Additional controls may apply to:

- HR data
- Financial data
- Administrative systems
- Identity infrastructure
- Security configurations
- Confidential organizational information

## 25.5 Change Control

Requests that require controlled technical changes must follow applicable Change Enablement procedures.

## 25.6 Evidence Security

Before publishing portfolio documentation:

- Remove credentials.
- Sanitize sensitive user information.
- Review screenshots.
- Remove confidential configuration details.
- Clearly label simulated activities.

---

# 26. Records and Evidence

## 26.1 Required Records

A completed fulfillment activity should produce:

- Authorized service request
- Fulfillment assignment
- Technical preparation record
- Implementation details
- Verification results
- Error or recovery documentation where applicable
- Requester communication
- Updated request status
- Relevant configuration updates

## 26.2 Supporting Evidence

| Evidence Type | Purpose |
|---|---|
| Service Request Record | Establish approved work |
| Authorization Record | Demonstrate fulfillment authority |
| PowerShell Output | Document technical actions or verification |
| Administrative Screenshot | Show relevant configuration |
| Functional Test Result | Demonstrate service availability |
| Change Record | Document applicable controlled changes |
| CI Record | Maintain configuration traceability |
| Communication Record | Document requester notification |

## 26.3 Evidence Integrity

Do not fabricate:

- Technical execution
- Command output
- Successful verification
- Administrative access
- License assignments
- Configuration changes
- Requester confirmation
- Fulfillment timestamps
- Service restoration
- ITSM integrations

Simulated results must be clearly labeled.

---

# 27. Continual Improvement

## 27.1 Potential Improvement Opportunities

- Standardized fulfillment runbooks
- Improved technical knowledge articles
- Better request forms
- Automated fulfillment for approved standard requests
- Improved authorization checks
- Reduced manual rework
- Better verification procedures
- Automated evidence collection
- Improved configuration documentation
- More accurate fulfillment metrics

## 27.2 Improvement Procedure

1. Identify a fulfillment inefficiency.
2. Collect supporting observations.
3. Evaluate the operational impact.
4. Propose an improvement.
5. Record the opportunity.
6. Assess feasibility and risk.
7. Obtain necessary authorization.
8. Implement the improvement.
9. Measure the outcome.
10. Update this SOP or related knowledge articles.

## 27.3 Related Documentation

[Improvement Management SOP](../../Continual-Improvement/Procedures/Improvement-Management.md)

[Improvement Register](../../Continual-Improvement/Improvement-Register.md)

[Improvement Template](../../Templates/Improvement-Template.md)

---

# 28. Procedure Quality Checklist

## Process Definition

- [ ] Purpose documented
- [ ] Scope established
- [ ] Roles defined
- [ ] Fulfillment workflow documented
- [ ] Authorization requirements included
- [ ] Verification requirements established
- [ ] Closure handoff defined

## Fulfillment Preparation

- [ ] Approved request reviewed
- [ ] Technical prerequisites verified
- [ ] Fulfillment technician assigned
- [ ] Technical documentation reviewed
- [ ] Target system confirmed
- [ ] Approved scope verified
- [ ] Applicable change requirements satisfied

## Technical Execution

- [ ] Authorized work performed
- [ ] Actual actions documented
- [ ] Errors and warnings recorded
- [ ] Unrelated changes avoided
- [ ] Security requirements followed

## Verification

- [ ] Expected outcome defined
- [ ] Actual result observed
- [ ] Functional testing completed where applicable
- [ ] Approved scope confirmed
- [ ] Supporting evidence retained
- [ ] Outstanding issues documented

## Documentation

- [ ] Request record updated
- [ ] Relevant configuration records updated
- [ ] Requester notified
- [ ] Closure readiness evaluated
- [ ] Related records linked

## Portfolio Accuracy

- [ ] Fictional organization identified
- [ ] Simulated activities clearly labeled
- [ ] Actual execution distinguished from examples
- [ ] No fabricated technical results
- [ ] No unsupported automation claims
- [ ] Sensitive information removed
- [ ] Relative links verified

---

# 29. Document Review and Revision History

## 29.1 Review Triggers

Review this SOP when:

- Fulfillment methods change.
- New services are introduced.
- Administrative tools change.
- Security requirements are updated.
- Licensing requirements change.
- Change control requirements change.
- Verification procedures change.
- ITSM workflows change.
- Technical failures reveal procedural gaps.
- Continual improvement initiatives introduce new methods.

## 29.2 Revision History

| Version | Description |
|---|---|
| 1.0 | Initial Request Fulfillment SOP aligned with ITIL 4 Service Request Management |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This SOP establishes a proposed standard for performing authorized employee IT service requests, verifying technical results, documenting implementation evidence, and preparing requests for closure.

Organizational roles, employee requests, approval decisions, and operational scenarios may be fictional or proposed.

Actual technical execution, administrative actions, configuration changes, verification results, and requester communications must be supported by documented lab evidence.

Simulated approvals and expected technical outcomes must not be represented as actual production activity or professional employment experience.

Jira Service Management and associated automation capabilities are planned unless implementation and verification are explicitly documented.

This procedure demonstrates controlled service fulfillment, authorization verification, technical administration, least-privilege access, functional testing, documentation, and operational accountability.
