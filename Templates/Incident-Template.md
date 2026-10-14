# INC-XXX — Incident Title

## Incident Information

| Field | Details |
|---|---|
| **Incident ID** | INC-XXX |
| **Incident Title** | [Brief description of the issue] |
| **Organization** | Technical Techno Tech |
| **Reported By** | [Employee / Department / Monitoring System] |
| **Assigned To** | [Service Desk / Systems Administrator / Network Administrator] |
| **Date Reported** | YYYY-MM-DD HH:MM |
| **Date Resolved** | YYYY-MM-DD HH:MM or Pending |
| **Status** | New / In Progress / Pending / Resolved / Closed |
| **Category** | [Hardware / Software / Network / Identity / Security / etc.] |
| **Priority** | P1 / P2 / P3 / P4 |
| **Affected Service** | [IT-SVC-XXX — Service Name] |
| **Related Scenario** | [SCN-XXX](path-to-scenario) or N/A |
| **Ticket Reference** | [Jira Ticket ID / URL] or N/A |
| **Environment** | Simulated Enterprise |

---

## 1. Incident Summary

### Issue Description

[Describe the unexpected interruption or degradation of an IT service.]

Include:

- What is not functioning correctly?
- Who or what is affected?
- When was the issue first observed?
- What symptoms were reported?
- What is the impact on business operations?

### Reported Symptoms

- [Symptom 1]
- [Symptom 2]
- [Symptom 3]

### Expected Behavior

[Describe how the affected service or system should normally function.]

### Actual Behavior

[Describe what is occurring instead.]

---

## 2. Impact & Priority Assessment

### Business Impact

[Explain how the incident affects employees, departments, applications, or business operations.]

### Impact Level

- **High:** Widespread disruption or critical business service unavailable.
- **Medium:** Multiple users or an important business function affected.
- **Low:** Limited disruption affecting a small number of users.

### Urgency Level

- **High:** Immediate action required to avoid significant business consequences.
- **Medium:** Timely resolution required, but limited temporary operation is possible.
- **Low:** Resolution can follow the normal support schedule.

### Assigned Priority

**Priority:** [P1 / P2 / P3 / P4]

**Justification:** [Explain why this priority was selected based on impact and urgency.]

*Note: Priority definitions and response targets should follow Technical Techno Tech's established incident procedures.*

---

## 3. Affected Systems & Services

| System / Service | Identifier | Impact |
|---|---|---|
| [Windows Server / AD DS / Microsoft 365 / etc.] | [Hostname / Service ID] | [Description] |
| [Workstation / Network Device / etc.] | [Hostname / Device ID] | [Description] |

### Relevant Infrastructure

- [Link to server or workstation documentation]
- [Link to configuration item]
- [Link to network or service documentation]

---

## 4. Initial Assessment

### Information Gathered

- [User statements or observed symptoms]
- [Recent changes or relevant events]
- [Error messages]
- [Scope of affected users or devices]

### Initial Hypotheses

1. [Possible cause]
2. [Possible cause]
3. [Possible cause]

### Initial Diagnostic Actions

| Action | Result |
|---|---|
| [Diagnostic action] | [Observation] |
| [Diagnostic action] | [Observation] |

---

## 5. Troubleshooting & Investigation

Document the troubleshooting process chronologically.

### Investigation Log

| Time | Action Performed | Result / Observation |
|---|---|---|
| HH:MM | [Diagnostic command or action] | [Result] |
| HH:MM | [Configuration or connectivity check] | [Result] |
| HH:MM | [Additional investigation] | [Result] |

### Commands & Tools Used

```powershell
# Include relevant commands used during investigation.
# Replace this placeholder with actual commands.
```

### Technical Findings

[Summarize what the investigation revealed.]

### Evidence

- [Screenshot or diagnostic output](Evidence/example-01.png)
- [Event log or command output](Evidence/example-02.txt)

Only include evidence that was actually collected.

---

## 6. Escalation & Collaboration

**Escalation Required:** Yes / No

### Escalation Details

| Field | Details |
|---|---|
| **Escalated To** | [Team / Role] |
| **Reason** | [Why escalation was required] |
| **Escalation Time** | HH:MM or N/A |
| **Outcome** | [Result of escalation] |

### Collaboration Notes

[Document relevant assistance, handoffs, or technical discussions.]

If escalation was unnecessary, indicate N/A.

---

## 7. Resolution & Service Restoration

### Resolution Actions

1. [Action performed]
2. [Action performed]
3. [Action performed]

### Resolution Commands

```powershell
# Include commands used to restore service, if applicable.
```

### Workaround

[Describe any temporary workaround provided, or enter N/A.]

### Resolution Summary

[Explain what restored the affected service and why the action was effective.]

### Service Restoration Time

**Date / Time:** YYYY-MM-DD HH:MM

---

## 8. Validation & Testing

Describe how normal service operation was verified.

| Test | Expected Result | Actual Result | Status |
|---|---|---|---|
| [Test 1] | [Expected behavior] | [Observed behavior] | Pass / Fail |
| [Test 2] | [Expected behavior] | [Observed behavior] | Pass / Fail |
| [Test 3] | [Expected behavior] | [Observed behavior] | Pass / Fail |

### User Confirmation

**Confirmation Received:** Yes / No / Not Applicable

**Details:** [Document employee confirmation or explain how restoration was independently verified.]

### Final Service Status

[Operational / Partially Restored / Unavailable]

---

## 9. Cause & Related Problem Records

### Identified Cause

[Describe the known cause, if established.]

**Cause Status:** Confirmed / Suspected / Unknown

### Further Investigation Required

**Problem Management Required:** Yes / No / To Be Determined

**Related Problem Record:** [PRB-XXX](path-to-problem) or N/A

An incident can be resolved when normal service is restored, even if the underlying cause remains unknown.

Recurring incidents, unknown underlying causes, or significant risks may justify a separate Problem Management investigation.

---

## 10. Related Changes & Knowledge Articles

### Related Changes

- [CHG-XXX — Change Title](path-to-change)

### Knowledge Articles

- [KB-XXX — Knowledge Article](path-to-article)

### Documentation Updates

- [Procedure or infrastructure documentation updated]
- [Enter N/A if no updates were required]

Changes should be documented through Change Enablement when required by the organization's change procedures.

---

## 11. Communication Log

| Time | Recipient | Communication | Method |
|---|---|---|---|
| HH:MM | [Employee / Department] | [Initial acknowledgment] | [Jira / Email / Chat] |
| HH:MM | [Employee / Department] | [Progress update] | [Jira / Email / Chat] |
| HH:MM | [Employee / Department] | [Resolution notification] | [Jira / Email / Chat] |

---

## 12. Lessons Learned

### What Went Well

- [Successful troubleshooting technique or process]

### Challenges Encountered

- [Technical or operational difficulty]

### What I Learned

- [Technical concept reinforced]
- [Troubleshooting insight gained]
- [IT service management principle applied]

### Skills Practiced

- [Windows Server / AD DS / Networking / Microsoft 365 / etc.]
- [PowerShell / Event Viewer / Diagnostic Tools]
- [Incident prioritization and documentation]
- [Technical communication and escalation]

### Improvement Opportunities

- [Potential monitoring improvement]
- [Potential procedure or knowledge base improvement]
- [Potential preventive action]

---

## 13. Incident Closure

| Field | Details |
|---|---|
| **Final Status** | Resolved / Closed / Pending |
| **Service Restored** | Yes / No / Partially |
| **Resolution Verified** | Yes / No |
| **User Notified** | Yes / No / N/A |
| **Related Records Updated** | Yes / No / N/A |
| **Closure Date** | YYYY-MM-DD HH:MM |

### Final Incident Summary

[Provide a concise summary of the reported issue, troubleshooting findings, resolution, and final service status.]

---

## Simulation Disclaimer

This incident represents a simulated IT service disruption within Technical Techno Tech, a fictional technology solutions company.

Technical troubleshooting, configuration changes, and validation results are documented based on hands-on work performed in a controlled lab environment.

Employee interactions, ticket records, escalations, and operational approvals may be simulated for educational and portfolio purposes.
