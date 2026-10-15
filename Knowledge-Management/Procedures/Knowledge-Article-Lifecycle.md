# SOP — Knowledge Article Lifecycle Management

**Organization:** Technical Techno Tech (TTT)  
**Department:** Internal IT / Knowledge Management  
**Document Type:** Standard Operating Procedure (SOP)  
**Procedure ID:** SOP-KM-001  
**Version:** 1.0  
**Status:** Draft — Lab Procedure  
**ITIL Practice:** Knowledge Management

---

## 1. Purpose

This procedure establishes a standardized process for managing Knowledge Base (KB) articles throughout their lifecycle within Technical Techno Tech.

Knowledge articles provide reusable technical information that helps IT personnel troubleshoot incidents, fulfill service requests, perform administrative tasks, and maintain IT infrastructure.

The procedure supports:

- Consistent knowledge documentation
- Accurate technical instructions
- Faster incident resolution
- Improved first-contact resolution
- Reduced repetitive troubleshooting
- Standardized service request fulfillment
- Effective knowledge sharing
- Knowledge accuracy and reliability
- Controlled documentation updates
- Continual improvement

**Key Principle:** Knowledge should be accurate, accessible to authorized personnel, reusable, and maintained throughout its useful lifecycle.

---

## 2. Scope

This procedure applies to technical knowledge articles maintained within Technical Techno Tech's internal IT Knowledge Base.

### Supported Knowledge Categories

| Category | Description |
|---|---|
| Active Directory | Domain services, user administration, Group Policy, and authentication |
| Windows Server | Server roles, administration, maintenance, and troubleshooting |
| Microsoft 365 | Microsoft 365 applications, administration, and collaboration |
| Microsoft Entra ID | Cloud identity, authentication, and access management |
| Microsoft Intune | Endpoint enrollment, configuration, and management |
| Networking | Connectivity, DNS, DHCP, routing, switching, and firewalls |

Additional categories may be introduced as the technical environment expands.

### Applicable Knowledge Types

- Troubleshooting guides
- How-to articles
- Technical reference articles
- Known error documentation
- Workaround instructions
- Administrative guides
- Frequently asked questions
- Service support instructions

Formal organizational policies, incident records, and change records remain separate document types, although knowledge articles may reference them.

---

## 3. ITIL 4 Knowledge Management

### Purpose

The purpose of Knowledge Management is to maintain and improve the effective, efficient, and convenient use of information and knowledge across an organization.

### Knowledge vs. Information

**Information:** Organized facts or data that describe something.

**Knowledge:** Information combined with understanding and experience that can support decisions and actions.

### Knowledge Management Objectives

1. Capture useful technical knowledge.
2. Validate the accuracy of that knowledge.
3. Make approved information accessible.
4. Encourage knowledge reuse.
5. Maintain documentation as systems change.
6. Remove or archive outdated information.

---

## 4. Roles and Responsibilities

### Knowledge Author

Responsible for:

- Identifying documentation opportunities
- Drafting knowledge articles
- Recording technical procedures
- Providing supporting evidence
- Following documentation standards
- Submitting articles for review

### Technical Reviewer

Responsible for:

- Verifying technical accuracy
- Reviewing commands and procedures
- Checking prerequisites
- Evaluating potential risks
- Confirming validation instructions
- Identifying necessary corrections

### Knowledge Approver

Responsible for:

- Confirming that required reviews are complete
- Approving publication
- Verifying the intended audience
- Confirming documentation requirements
- Authorizing significant article revisions when required

### Knowledge Manager

Responsible for:

- Maintaining the Knowledge Base structure
- Coordinating article reviews
- Monitoring article quality
- Managing lifecycle statuses
- Identifying outdated content
- Supporting continual improvement

### Knowledge User

Responsible for:

- Using applicable approved documentation
- Following administrative authorization requirements
- Reporting inaccurate instructions
- Suggesting improvements
- Providing feedback on article usefulness

**Lab Note:** These roles represent simulated organizational responsibilities. A single learner may perform multiple roles during a controlled lab exercise. A simulated approval must not be represented as an independent review.

---

## 5. Knowledge Article Lifecycle

Technical Techno Tech uses the following proposed lifecycle.

```text
Knowledge Opportunity Identified
             |
             v
        Article Draft
             |
             v
       Technical Review
             |
       +-----+-----+
       |           |
    Approved    Revisions
       |         Required
       |           |
       |           v
       |       Update Draft
       |           |
       |           v
       |       Re-Review
       |
       v
         Publication
             |
             v
         Active Use
             |
             v
       Periodic Review
             |
       +-----+-----+
       |           |
     Current     Outdated
       |           |
       v           v
 Continue Use   Revise Article
       |           |
       |           v
       |        Re-Review
       |
       v
    Retirement
    When Needed
             |
             v
       Archive / Remove
       From Active Use
```

### Lifecycle Stages

| Stage | Description |
|---|---|
| Identification | A knowledge opportunity is recognized |
| Draft | Article content is created |
| Technical Review | Instructions and information are evaluated |
| Approval | Article is authorized for publication |
| Publication | Article becomes available to its intended audience |
| Active Use | Article supports operational activities |
| Maintenance | Article is updated when necessary |
| Periodic Review | Accuracy and relevance are reassessed |
| Retirement | Article is removed from active use when obsolete |
| Archival | Historical content is retained when appropriate |

---

## 6. Knowledge Article Statuses

Each knowledge article should have a clearly identified lifecycle status.

| Status | Description |
|---|---|
| Draft | Article is being created |
| In Review | Article is undergoing technical review |
| Changes Required | Corrections are needed before approval |
| Approved | Article has completed required approval |
| Published | Article is available for authorized use |
| Under Revision | A published article is being updated |
| Retired | Article is no longer approved for operational use |
| Archived | Article is retained for historical reference |

### Important Distinction

**Approved** means the article has met the applicable review and authorization requirements.

**Published** means the article is available to its intended audience.

An article may be approved before it is published.

In this portfolio, a Markdown file being present in GitHub does not automatically mean that its operational content has been technically validated or approved.

---

## 7. Knowledge Article Identification

Each knowledge article receives a unique identifier.

### Naming Convention

```text
KB-001
KB-002
KB-003
```

### Recommended Filename Format

```text
KB-001-Reset-AD-User-Password.md
KB-002-Troubleshoot-DNS-Resolution.md
KB-003-Verify-Group-Policy-Application.md
```

### Example Article Metadata

| Field | Example |
|---|---|
| Article ID | KB-001 |
| Title | Reset an Active Directory User Password |
| Category | Active Directory |
| Article Type | How-To |
| Version | 1.0 |
| Status | Draft |
| Intended Audience | Authorized IT Support Personnel |
| Author | Lab Administrator |
| Technical Reviewer | Pending |
| Approval Status | Not Approved |
| Last Reviewed | Not Yet Reviewed |
| Next Review | To Be Determined |

Article identifiers should remain consistent throughout revisions.

---

## 8. Knowledge Article Lifecycle Procedure

### Step 1 — Identify a Knowledge Opportunity

Identify technical information that would benefit from reusable documentation.

### Common Knowledge Sources

- Resolved incidents
- Service request fulfillment
- Problem investigations
- Change implementations
- Infrastructure deployments
- Monitoring events
- Repeated troubleshooting questions
- New administrative procedures
- Lessons learned from lab exercises

### Example

A Service Desk technician repeatedly investigates Windows workstations that cannot locate a domain controller.

A reusable troubleshooting guide could reduce repeated diagnostic work.

**Expected Result:** A documentation opportunity is identified.

### Step 2 — Determine Whether an Article Already Exists

Search the Knowledge Base for existing documentation.

Review:

- Article titles
- Categories
- Keywords
- Existing troubleshooting guides
- Known error documentation
- Related administrative procedures

#### Decision

If a suitable article exists:

- Review whether it requires an update.
- Avoid unnecessary duplication.
- Propose improvements where appropriate.

If no suitable article exists:

- Create a new article.

**Expected Result:** Duplicate documentation is minimized.

### Step 3 — Determine Article Type and Audience

Identify the purpose and intended users of the article.

### Article Types

| Type | Purpose |
|---|---|
| Troubleshooting Guide | Diagnose and resolve technical issues |
| How-To Article | Perform a specific technical task |
| Technical Reference | Explain technical settings or components |
| Known Error | Document a known issue and available workaround |
| FAQ | Answer frequently asked questions |
| Administrative Guide | Support authorized system administration |

### Audience Examples

- Tier 1 Service Desk
- Tier 2 Technical Support
- Systems Administrators
- Network Administrators
- Cloud Administrators
- General Employees

Articles intended for general employees should not expose privileged administrative procedures or sensitive infrastructure details.

**Expected Result:** The article's purpose and audience are defined.

### Step 4 — Create the Article Record

Assign the next available knowledge article ID.

Create the article in the appropriate Knowledge Base category.

### Example

```text
Knowledge-Management/
└── Knowledge-Base/
    └── Active-Directory/
        └── KB-001-Reset-AD-User-Password.md
```

Use the standardized template:

[Knowledge Article Template](../../Templates/Knowledge-Article-Template.md)

**Expected Result:** A new article record is created.

### Step 5 — Document Article Metadata

Record:

- Article ID
- Title
- Category
- Article type
- Version
- Status
- Author
- Intended audience
- Date created
- Review information
- Related services
- Related records

### Example

```text
Article ID: KB-001
Title: Reset an Active Directory User Password
Category: Active Directory
Type: How-To
Version: 1.0
Status: Draft
Audience: Authorized IT Support Personnel
Related Service: IT-SVC-001
```

**Expected Result:** The article is identifiable and traceable.

### Step 6 — Write the Article

Develop the technical content using the approved template.

### Recommended Article Sections

1. Purpose
2. Scope
3. Prerequisites
4. Required permissions
5. Tools and technologies
6. Procedure
7. Validation
8. Common errors
9. Troubleshooting
10. Escalation
11. Recovery or rollback, when applicable
12. Related documentation
13. Review history

### Writing Standards

Articles should be:

- Clear
- Accurate
- Consistent
- Task-focused
- Technically relevant
- Easy to follow
- Appropriate for the intended audience

Avoid unnecessary explanations that make procedures difficult to use.

**Expected Result:** A complete draft is available for review.

### Step 7 — Validate Technical Instructions

Verify technical procedures in an authorized environment when practical.

### Validation Activities

- Confirm prerequisites.
- Verify required permissions.
- Test commands.
- Review expected output.
- Confirm administrative interfaces.
- Validate troubleshooting logic.
- Check potential side effects.
- Confirm recovery instructions.

### Example

An article documents how to verify Active Directory replication.

Example commands:

```powershell
repadmin /replsummary
```

```powershell
repadmin /showrepl
```

The author should verify that:

- The commands are appropriate.
- Required permissions are documented.
- The tools are available.
- The output is interpreted correctly.
- The article explains relevant limitations.

**Expected Result:** Technical instructions are supported by testing or clearly identified authoritative references.

If testing is incomplete, the article must remain appropriately labeled as unverified or draft.

### Step 8 — Submit for Technical Review

Change the article status to:

**In Review**

The reviewer evaluates:

- Technical accuracy
- Completeness
- Clarity
- Security considerations
- Prerequisites
- Command correctness
- Validation instructions
- Related documentation
- Intended audience

### Review Outcomes

| Outcome | Action |
|---|---|
| Approved | Proceed to approval or publication |
| Changes Required | Return to author for revision |
| Rejected | Document reason and discontinue the proposed article |
| Additional Testing Required | Retain review status until testing is completed |

**Expected Result:** The article receives a documented technical review outcome.

### Step 9 — Correct Identified Issues

If changes are required:

1. Review feedback.
2. Correct inaccurate information.
3. Clarify confusing instructions.
4. Update commands or screenshots.
5. Repeat technical testing when necessary.
6. Resubmit the article.

### Example

**Review Finding:** The article does not specify that Active Directory administrative permissions are required.

**Correction:** Add a prerequisites section describing the required delegated permissions.

**Expected Result:** Identified deficiencies are addressed.

### Step 10 — Approve the Article

After successful review, an authorized approver determines whether the article is ready for publication.

Approval should consider:

- Technical accuracy
- Intended audience
- Security
- Documentation standards
- Operational relevance
- Review completeness

Record:

- Approval status
- Approver or simulated approver role
- Approval date
- Relevant review notes

### Lab Consideration

When no independent reviewer is available, record:

**Review Method:** Self-review / Lab Validation

**Approval Status:** Not Independently Approved

Do not imply that an actual IT manager or technical review board approved the article.

**Expected Result:** The article's approval status is accurately documented.

### Step 11 — Publish the Article

Make the article available to its intended audience after the applicable publication requirements have been satisfied.

### Publication Activities

1. Confirm article metadata.
2. Confirm final version.
3. Verify Markdown formatting.
4. Check relative links.
5. Verify screenshots and evidence.
6. Confirm sensitive information is removed.
7. Update the article status.
8. Add the article to the appropriate Knowledge Base index.

### GitHub Publication

For the portfolio, articles may be committed to the repository using Git.

Example:

```bash
git add .
git commit -m "docs: add Active Directory knowledge article"
git push
```

GitHub publication demonstrates documentation management but does not, by itself, establish operational approval.

**Expected Result:** The article is accessible to its intended audience with an accurate status.

### Step 12 — Use the Article

Knowledge users may reference published articles during:

- Incident investigation
- Incident resolution
- Service request fulfillment
- Administrative maintenance
- Infrastructure troubleshooting
- Training exercises

### Example

An employee reports an authentication failure.

The Service Desk technician consults an approved Active Directory troubleshooting article.

The technician follows the documented diagnostic steps and records relevant results in the incident ticket.

**Expected Result:** Knowledge supports consistent operational activities.

### Step 13 — Collect Feedback

Knowledge users should report issues such as:

- Incorrect instructions
- Outdated screenshots
- Missing prerequisites
- Broken links
- Unclear steps
- Commands that no longer apply
- Missing validation guidance

### Feedback Record

```text
Article ID:
Feedback Date:
Reported By:
Issue Description:
Suggested Improvement:
Review Status:
```

**Expected Result:** Knowledge quality issues are identified.

### Step 14 — Review the Article Periodically

Review published articles according to their risk, technical volatility, and operational importance.

### Suggested Review Frequency

| Article Type | Proposed Review Frequency |
|---|---|
| Security-sensitive procedures | Every 3–6 months |
| Cloud administration procedures | Every 6 months |
| Active Directory procedures | Every 6–12 months |
| Windows Server procedures | Every 6–12 months |
| Networking procedures | Every 6–12 months |
| General technical references | Annually |

These are proposed internal review intervals, not mandatory ITIL requirements.

### Review Questions

1. Is the article still accurate?
2. Are the commands valid?
3. Have administrative interfaces changed?
4. Are screenshots current?
5. Are permissions still appropriate?
6. Are linked documents available?
7. Is the article still useful?
8. Does it contain sensitive information?
9. Does the article require revision or retirement?

**Expected Result:** The article's continued relevance is assessed.

### Step 15 — Revise the Article

When changes are necessary:

1. Change the status to **Under Revision**.
2. Record the reason for revision.
3. Update the affected content.
4. Repeat appropriate technical validation.
5. Obtain the required review.
6. Update the version number.
7. Publish the revised article.

### Versioning Examples

| Version | Change |
|---|---|
| 1.0 | Initial article |
| 1.1 | Minor clarification or correction |
| 1.2 | Updated screenshots or commands |
| 2.0 | Major procedure revision |

The existing published version should not be silently replaced with unverified instructions.

**Expected Result:** The article remains accurate and traceable.

### Step 16 — Retire Outdated Articles

An article should be considered for retirement when:

- The technology is no longer supported.
- The procedure is obsolete.
- A replacement article exists.
- The service has been retired.
- The information is no longer relevant.
- The instructions cannot be maintained safely.

### Retirement Procedure

1. Identify the retirement reason.
2. Review related articles and references.
3. Identify replacement documentation.
4. Record the retirement decision.
5. Change status to **Retired**.
6. Remove the article from active operational indexes.
7. Archive the article when appropriate.

**Expected Result:** Obsolete instructions are no longer presented as approved operational guidance.

### Step 17 — Archive or Remove the Article

Retired articles may be archived when historical reference is useful.

### Archival Requirements

- Clearly mark the article as archived.
- Record the retirement reason.
- Preserve relevant revision history.
- Identify replacement documentation.
- Prevent accidental operational use.

Historical records may be retained in Git history or a designated archive.

Sensitive or unsafe content should not be retained publicly merely for historical purposes.

**Expected Result:** Retired knowledge is handled appropriately.

---

## 9. Knowledge Article Structure

Each article should follow a consistent format.

### Standard Article Layout

```text
Article ID
Title
Category
Version
Status
Audience
Author
Review Information

1. Purpose
2. Scope
3. Prerequisites
4. Required Permissions
5. Tools and Technologies
6. Procedure
7. Validation
8. Troubleshooting
9. Escalation
10. Recovery / Rollback
11. Related Documentation
12. Revision History
```

Sections may be omitted when they do not apply.

### Documentation Principles

- Use descriptive headings.
- Number procedural steps.
- Include commands in code blocks.
- Explain expected results.
- Identify administrative permissions.
- Include validation steps.
- Avoid unnecessary duplication.
- Link related documentation.

---

## 10. Knowledge Base Repository Structure

Technical Techno Tech organizes knowledge articles by technical category.

```text
Knowledge-Management/
├── README.md
├── Procedures/
│   └── Knowledge-Article-Lifecycle.md
└── Knowledge-Base/
    ├── Active-Directory/
    ├── Windows-Server/
    ├── Microsoft-365/
    ├── Entra-ID/
    ├── Intune/
    └── Networking/
```

### Example Articles

```text
Knowledge-Base/
├── Active-Directory/
│   ├── KB-001-Reset-AD-User-Password.md
│   └── KB-002-Troubleshoot-AD-Authentication.md
├── Windows-Server/
│   └── KB-003-Check-Windows-Service-Status.md
├── Microsoft-365/
│   └── KB-004-Troubleshoot-Outlook-Sign-In.md
├── Entra-ID/
│   └── KB-005-Review-Entra-Sign-In-Logs.md
├── Intune/
│   └── KB-006-Verify-Device-Enrollment.md
└── Networking/
    └── KB-007-Troubleshoot-DNS-Resolution.md
```

These filenames are examples of proposed articles and do not indicate that the documents already exist.

---

## 11. Knowledge Article Security

Knowledge articles must follow applicable information security requirements.

### Sensitive Information

Do not publish:

- Passwords
- Authentication tokens
- Private keys
- Recovery secrets
- Confidential employee information
- Unredacted personal data
- Sensitive production configurations

### Administrative Procedures

Articles involving privileged operations should identify:

- Required permissions
- Authorized audience
- Administrative tools
- Potential risks
- Approval requirements
- Validation steps

### Public Portfolio Considerations

Because the GitHub repository may be publicly accessible:

1. Use fictional employee information.
2. Redact sensitive screenshots.
3. Avoid exposing live credentials.
4. Distinguish lab infrastructure from production systems.
5. Identify simulated approvals.
6. Do not publish confidential third-party information.

**Key Principle:** Public availability does not make a document suitable for unrestricted operational use.

---

## 12. Knowledge Article Review Checklist

### Technical Accuracy

- [ ] Purpose is clear
- [ ] Scope is defined
- [ ] Technical instructions are accurate
- [ ] Commands have been tested or clearly identified as unverified
- [ ] Prerequisites are documented
- [ ] Required permissions are identified
- [ ] Expected results are explained
- [ ] Validation instructions are included
- [ ] Known limitations are documented

### Documentation Quality

- [ ] Article ID is unique
- [ ] Title is descriptive
- [ ] Category is correct
- [ ] Version is recorded
- [ ] Status is accurate
- [ ] Audience is identified
- [ ] Formatting is consistent
- [ ] Links work
- [ ] Screenshots are relevant
- [ ] Related documentation is linked

### Security

- [ ] No credentials are exposed
- [ ] No authentication tokens are included
- [ ] Sensitive information is redacted
- [ ] Administrative boundaries are documented
- [ ] Risky actions include appropriate warnings
- [ ] Recovery or rollback guidance is included when applicable

### Lifecycle

- [ ] Author is recorded
- [ ] Review method is documented
- [ ] Approval status is accurate
- [ ] Publication status is accurate
- [ ] Revision history is maintained
- [ ] Next review is identified when applicable

---

## 13. Example Knowledge Article Lifecycle

### Scenario — Troubleshooting Domain Authentication

**Proposed Article ID:** KB-002  
**Title:** Troubleshoot Active Directory Authentication Failures  
**Category:** Active Directory  
**Type:** Troubleshooting Guide  
**Related Service:** IT-SVC-001 — Identity & Access Management

### Stage 1 — Identification

A simulated incident involves an employee unable to authenticate to the domain.

The investigation requires several diagnostic checks.

### Stage 2 — Draft

The author prepares a guide covering:

- Network connectivity
- DNS configuration
- Domain controller discovery
- Account status
- Authentication errors

### Stage 3 — Technical Validation

The author tests relevant commands in the lab.

Example:

```powershell
ipconfig /all
```

```powershell
nslookup dc01.homelab.local
```

```powershell
nltest /dsgetdc:homelab.local
```

Actual results must be recorded separately.

### Stage 4 — Review

The article is checked for:

- Technical accuracy
- Required permissions
- Correct troubleshooting order
- Validation instructions
- Security considerations

### Stage 5 — Publication

After applicable review requirements are met, the article is made available in the Active Directory Knowledge Base.

### Stage 6 — Reuse

The article may be referenced by future incident records involving similar authentication symptoms.

### Stage 7 — Maintenance

The article is reviewed when:

- Domain architecture changes
- Administrative tools change
- Troubleshooting findings reveal inaccuracies
- The scheduled review date is reached

### Stage 8 — Retirement

The article is retired if its procedures become obsolete or are replaced.

**Scenario Status:** Illustrative lifecycle example. It does not represent a completed review, approval, or publication.

---

## 14. Knowledge Article Revision Control

Changes to published articles should be traceable.

### Revision History Format

| Version | Date | Description | Review Status |
|---|---|---|---|
| 1.0 | TBD | Initial article | Pending |
| 1.1 | TBD | Minor procedural update | Pending |
| 2.0 | TBD | Major technical revision | Pending |

### Git Version Control

Git may be used to track:

- Article creation
- Content changes
- Revision history
- Documentation corrections
- Retirement updates

### Example Git Workflow

```bash
git status
git add .
git commit -m "docs: update Active Directory troubleshooting article"
git push
```

Git commits provide a technical change history.

They do not automatically establish that an article was reviewed, approved, or validated.

---

## 15. Knowledge Management Metrics

Knowledge Management effectiveness may be evaluated using:

| Metric | Purpose |
|---|---|
| Knowledge Article Creation Rate | Measures new articles created |
| Knowledge Article Reuse | Tracks articles referenced during support work |
| Article Review Compliance | Measures completion of scheduled reviews |
| Outdated Article Rate | Identifies content requiring maintenance |
| Article Accuracy | Evaluates correctness of technical instructions |
| Knowledge Feedback Rate | Measures user feedback and improvement suggestions |
| Article Revision Rate | Tracks documentation updates |
| Knowledge-Related First Contact Resolution | Evaluates support resolutions assisted by knowledge |
| Article Retirement Rate | Tracks removal of obsolete knowledge |
| Documentation Coverage | Identifies services or procedures lacking reusable guidance |

Metrics should be calculated using actual records or clearly labeled simulated datasets.

---

## 16. Integration With ITIL Practices

| ITIL Practice | Relationship |
|---|---|
| Service Desk | Uses knowledge articles during employee support |
| Incident Management | Produces and reuses troubleshooting and resolution knowledge |
| Service Request Management | Uses standardized fulfillment instructions |
| Knowledge Management | Manages knowledge creation, publication, maintenance, and retirement |
| Problem Management | Produces known error and workaround documentation |
| Change Enablement | Identifies documentation requiring updates after changes |
| Monitoring and Event Management | Provides technical findings and diagnostic procedures |
| Service Configuration Management | Supplies infrastructure configuration and dependency information |
| Information Security Management | Establishes appropriate knowledge access and protection |
| Continual Improvement | Identifies opportunities to improve knowledge quality and availability |

---

## 17. Common Knowledge Management Errors

### Error 1 — Publishing Unverified Instructions

**Incorrect:** Presenting an untested command as a confirmed solution.

**Correct:** Validate instructions or clearly identify unverified steps.

### Error 2 — Missing Prerequisites

**Incorrect:** Providing an administrative procedure without identifying required permissions.

**Correct:** Document tools, access requirements, and prerequisites.

### Error 3 — Duplicating Existing Articles

**Incorrect:** Creating multiple conflicting guides for the same procedure.

**Correct:** Review existing knowledge and update it when appropriate.

### Error 4 — Failing to Maintain Articles

**Incorrect:** Leaving outdated screenshots and commands in active articles.

**Correct:** Review and revise articles when technology or procedures change.

### Error 5 — Confusing Publication With Approval

**Incorrect:** Assuming that a GitHub commit means a document has been formally approved.

**Correct:** Track technical review and approval separately.

### Error 6 — Exposing Sensitive Information

**Incorrect:** Publishing credentials or unredacted administrative screenshots.

**Correct:** Review and sanitize all public documentation.

### Error 7 — Retaining Obsolete Articles as Active

**Incorrect:** Allowing technicians to use unsupported instructions without warning.

**Correct:** Retire outdated articles and identify replacements.

---

## 18. Knowledge Article Lifecycle Quality Checklist

Before considering an article ready for active use, verify:

- [ ] Knowledge opportunity identified
- [ ] Existing articles reviewed
- [ ] Article type selected
- [ ] Intended audience identified
- [ ] Unique article ID assigned
- [ ] Appropriate category selected
- [ ] Metadata completed
- [ ] Technical content drafted
- [ ] Prerequisites documented
- [ ] Required permissions documented
- [ ] Commands validated where applicable
- [ ] Expected results documented
- [ ] Security considerations reviewed
- [ ] Technical review completed or limitations disclosed
- [ ] Required approval obtained or status accurately labeled
- [ ] Version number recorded
- [ ] Publication status updated
- [ ] Knowledge Base index updated
- [ ] Related records linked
- [ ] Review requirements identified
- [ ] Revision history maintained

---

## 19. Related Procedures and Documentation

### Knowledge Management

- [Knowledge Management Overview](../README.md)
- [Knowledge Article Template](../../Templates/Knowledge-Article-Template.md)

### ITIL Practices

- [Service Desk](../../Service-Desk/)
- [Incident Management](../../Incident-Management/)
- [Service Request Management](../../Service-Request-Management/)
- [Problem Management](../../Problem-Management/)
- [Change Enablement](../../Change-Enablement/)
- [Monitoring and Event Management](../../Monitoring-and-Event-Management/)
- [Service Configuration Management](../../Service-Configuration-Management/)
- [Information Security Management](../../Information-Security-Management/)
- [Continual Improvement](../../Continual-Improvement/)

### Knowledge Base Categories

- [Active Directory](../Knowledge-Base/Active-Directory/)
- [Windows Server](../Knowledge-Base/Windows-Server/)
- [Microsoft 365](../Knowledge-Base/Microsoft-365/)
- [Microsoft Entra ID](../Knowledge-Base/Entra-ID/)
- [Microsoft Intune](../Knowledge-Base/Intune/)
- [Networking](../Knowledge-Base/Networking/)

### Organization Documentation

- [Company Overview](../../Company-Overview.md)
- [IT Service Catalog](../../Service-Catalog.md)
- [Infrastructure Overview](../../Infrastructure/)
- [Operational Scenarios](../../Scenarios/)

---

## 20. Procedure Review

This procedure should be reviewed when:

- Knowledge Management responsibilities change.
- Documentation standards are updated.
- New technical categories are introduced.
- Article review requirements change.
- Knowledge Base platforms are modified.
- Security requirements are updated.
- Article quality issues increase.
- Continual improvement reviews identify opportunities.

### Revision History

| Version | Description |
|---|---|
| 1.0 | Initial knowledge article lifecycle management procedure |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

Organizational roles, knowledge approval workflows, article review decisions, and operational scenarios may be simulated.

Technical instructions, administrative procedures, diagnostic commands, and validation results are documented based on hands-on lab activities where indicated.

GitHub publication does not imply independent technical approval, production deployment, or organizational authorization.

This procedure demonstrates ITIL-aligned Knowledge Management, technical documentation, knowledge lifecycle control, version management, and continual improvement practices rather than employment experience within an actual production organization.
