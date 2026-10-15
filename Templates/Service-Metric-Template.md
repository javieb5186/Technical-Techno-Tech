# MET-### — Service Metric Title

**Organization:** Technical Techno Tech (TTT)  
**Practice:** Continual Improvement  
**Document Type:** Service Metric Record  
**Metric ID:** MET-###  
**Version:** 1.0  
**Status:** Proposed — Not Yet Measured  
**Metric Owner:** To Be Assigned  
**Function:** Internal IT  
**Related Service:** IT-SVC-###  
**Related ITIL Practice:** [Practice Name]  
**Environment:** To Be Defined  
**Date Created:** YYYY-MM-DD  
**Last Reviewed:** Not Yet Reviewed  
**Next Review Date:** Not Yet Established  
**Classification:** Public Portfolio — Sanitized Lab Documentation

---

# 1. Metric Overview

## 1.1 Purpose

[Describe why this metric is being established and what it is intended to measure.]

This metric provides a consistent method for evaluating a defined aspect of IT service performance.

Its purpose is to support:

- Evidence-based decision-making
- IT service performance evaluation
- Operational effectiveness
- Service quality assessment
- Identification of performance gaps
- Continual improvement
- Technical and operational reporting

**Key Principle:** A service metric should measure something meaningful, use a consistent calculation method, and support an identifiable operational or improvement objective.

## 1.2 Metric Summary

| Attribute | Value |
|---|---|
| Metric ID | MET-### |
| Metric Name | [Name] |
| Metric Category | [Category] |
| Related Service | IT-SVC-### |
| Related Practice | [Practice] |
| Metric Owner | [Role] |
| Measurement Unit | [Unit] |
| Measurement Frequency | [Frequency] |
| Reporting Frequency | [Frequency] |
| Baseline Status | Not Yet Measured |
| Target Status | Not Yet Established |
| Collection Method | To Be Determined |
| Current Status | Proposed |

## 1.3 Metric Category

Select the primary category.

- [ ] Service Performance
- [ ] Service Desk Operations
- [ ] Incident Management
- [ ] Service Request Management
- [ ] Problem Management
- [ ] Change Enablement
- [ ] Monitoring and Event Management
- [ ] Service Configuration Management
- [ ] Information Security Management
- [ ] Knowledge Management
- [ ] Continual Improvement
- [ ] Infrastructure Performance
- [ ] Cost Optimization
- [ ] Other: [Specify]

## 1.4 Measurement Objective

**Objective:**

[Explain what the organization wants to understand or improve.]

**Decision Supported:**

[Describe the decision that will be informed by this metric.]

**Expected Value:**

[Describe how the measurement may support service improvement.]

---

# 2. ITIL 4 Alignment

This metric supports the ITIL 4 Continual Improvement practice and the relevant operational practice identified in this record.

### Continual Improvement Relationship

| ITIL 4 Continual Improvement Activity | Metric Contribution |
|---|---|
| What is the vision? | Align measurement with service objectives |
| Where are we now? | Establish the baseline |
| Where do we want to be? | Define the target |
| How do we get there? | Select improvement activities |
| Take action | Implement and monitor improvements |
| Did we get there? | Compare actual results with success criteria |
| How do we keep the momentum going? | Continue measurement and review |

### Related ITIL Practices

- [ ] Service Desk
- [ ] Incident Management
- [ ] Service Request Management
- [ ] Knowledge Management
- [ ] Problem Management
- [ ] Change Enablement
- [ ] Monitoring and Event Management
- [ ] Service Configuration Management
- [ ] Information Security Management
- [x] Continual Improvement

**Practice Relationship:**

[Explain how this metric supports the selected practices.]

### Important

ITIL 4 does not prescribe one universal set of service metrics.

Metrics should reflect the services, objectives, risks, and capabilities of the organization.

---

# 3. Related IT Services

Identify the services evaluated by this metric.

| Service ID | Service Name | Measurement Relationship |
|---|---|---|
| IT-SVC-### | [Service Name] | [Description] |

### Available Internal IT Services

| Service ID | Service |
|---|---|
| IT-SVC-001 | Identity & Access Management |
| IT-SVC-002 | Endpoint Management |
| IT-SVC-003 | Microsoft 365 & Collaboration |
| IT-SVC-004 | Network Connectivity |
| IT-SVC-005 | Server & Infrastructure Services |
| IT-SVC-006 | Information Security |
| IT-SVC-007 | Employee IT Lifecycle |

### Service Scope

**Primary Service:** [IT-SVC-###]

**Additional Services:** [List or Not Applicable]

**Service Owner:** [Role or To Be Assigned]

**Service Criticality:** [High / Medium / Low / Not Yet Assessed]

---

# 4. Metric Definition

## 4.1 Formal Definition

**Metric Name:** [Name]

**Definition:**

[Provide an exact definition of what is measured.]

**Measurement Type:** [Count / Percentage / Duration / Rate / Utilization / Cost / Other]

**Measurement Unit:** [Minutes / Hours / Percentage / Count / Dollars / Other]

**Desired Direction:**

- [ ] Higher Is Better
- [ ] Lower Is Better
- [ ] Within a Defined Range
- [ ] Context Dependent

## 4.2 Measurement Boundaries

**Start Condition:**

[Define when measurement begins.]

**End Condition:**

[Define when measurement ends.]

**Included Records or Events:**

- [Criterion]
- [Criterion]

**Excluded Records or Events:**

- [Criterion]
- [Criterion]

## 4.3 Special Conditions

Document how the metric handles:

- Missing information
- Duplicate records
- Cancelled activities
- Reopened records
- Paused time
- Planned maintenance
- Partial service degradation
- Incomplete measurements
- Zero denominators
- Outliers

**Handling Rules:**

[Describe applicable rules.]

### Important

A metric must have a consistent definition before meaningful comparisons can be made.

For example, incident resolution time may be measured from ticket logging to resolution, while service restoration time may use different start and end events.

These measurements should not be treated as interchangeable.

---

# 5. Data Source

## 5.1 Primary Data Source

**Source Name:** [Name]

**Source Type:** [ITSM / Monitoring / PowerShell / Administrative Portal / Manual Observation / Other]

**Source System:** [Specify]

**Data Owner:** [Role]

**Access Requirements:** [Specify]

**Source Status:** [Available / Planned / Not Yet Verified]

## 5.2 Potential Data Sources

Select applicable sources.

- [ ] Jira Service Management
- [ ] Windows Event Logs
- [ ] PowerShell
- [ ] Active Directory
- [ ] Microsoft Entra ID
- [ ] Microsoft Intune
- [ ] Microsoft 365
- [ ] Microsoft Azure
- [ ] Azure Cost Management
- [ ] Hyper-V
- [ ] Network device CLI
- [ ] Monitoring platform
- [ ] Configuration Item records
- [ ] Change records
- [ ] Incident records
- [ ] Service request records
- [ ] Manual lab observations
- [ ] Other: [Specify]

### Important

Selecting a data source does not establish that it is connected or configured.

Jira Service Management reporting and integrations must be identified as planned until implemented and verified.

## 5.3 Required Data Fields

| Field | Description | Required |
|---|---|---|
| [Field] | [Description] | Yes |
| [Field] | [Description] | Yes |
| [Field] | [Description] | No |

## 5.4 Data Availability

**Required Data Available:** Not Yet Verified

**Historical Data Available:** Not Yet Determined

**Known Limitations:**

[Document missing fields, access restrictions, or other limitations.]

---

# 6. Measurement Method

## 6.1 Collection Method

**Method:** [Manual / Automated / Scripted / Report Export]

**Description:**

[Explain how measurements will be collected.]

## 6.2 Collection Procedure

1. Identify the reporting period.
2. Access the approved data source.
3. Apply the defined inclusion criteria.
4. Apply the defined exclusion criteria.
5. Collect the required fields.
6. Review missing or duplicate records.
7. Preserve relevant raw observations.
8. Calculate the metric.
9. Validate the result.
10. Document findings and evidence.

## 6.3 Collection Frequency

**Collection Frequency:** [Daily / Weekly / Monthly / Quarterly / Per Event]

**Reporting Frequency:** [Frequency]

**Collection Owner:** [Role]

**Collection Schedule:** [Specify]

## 6.4 Collection Tools

| Tool | Purpose | Status |
|---|---|---|
| [Tool] | [Purpose] | Planned |

## 6.5 Automation

**Automated Collection:** No

**Automation Planned:** [Yes / No]

**Automation Method:** [Specify or Not Applicable]

**Script Location:** [Relative path or Not Applicable]

**Automation Verification:** Not Applicable

### Important

Do not claim automated data collection unless the automation has actually been implemented and tested.

---

# 7. Calculation Method

## 7.1 Formula

**Metric Formula:**

```text
[Insert the metric formula]
```

## 7.2 Calculation Variables

| Variable | Description | Unit | Source |
|---|---|---|---|
| A | [Description] | [Unit] | [Source] |
| B | [Description] | [Unit] | [Source] |

## 7.3 Calculation Procedure

1. Identify valid observations.
2. Confirm the reporting period.
3. Validate required fields.
4. Apply the documented formula.
5. Confirm units.
6. Review the result.
7. Record calculation evidence.

## 7.4 Example Calculation

**Example Type:** Illustrative — Not Actual Performance Data

**Example Inputs:**

```text
Variable A = [Illustrative Value]
Variable B = [Illustrative Value]
```

**Example Formula:**

```text
Result = [Calculation]
```

**Example Result:** [Illustrative Result]

### Important

Remove this illustrative example or label it clearly when publishing the completed metric record.

Example calculations must not be represented as observed service performance.

---

# 8. Measurement Period

## 8.1 Reporting Interval

**Measurement Period Type:** [Daily / Weekly / Monthly / Quarterly / Custom]

**Start Date:** YYYY-MM-DD

**End Date:** YYYY-MM-DD

**Time Zone:** [Specify]

## 8.2 Measurement Population

**Population Description:**

[Describe the records, events, systems, or users included.]

**Population Size:** Not Yet Determined

**Sample Size:** Not Yet Determined

## 8.3 Comparison Period

**Baseline Period:** Not Yet Established

**Comparison Period:** Not Yet Established

### Comparison Requirements

- Use consistent definitions.
- Use consistent time units.
- Compare equivalent populations where practical.
- Account for differences in reporting periods.
- Document environmental changes.
- Identify small sample sizes.

### Important

A metric calculated from a small number of observations may not represent typical service performance.

---

# 9. Baseline Measurement

## 9.1 Current Performance

**Baseline Status:** Not Yet Measured

**Baseline Value:** Not Available

**Baseline Unit:** [Unit]

**Baseline Period:** Not Yet Established

**Collection Date:** Pending

**Data Source:** [Specify]

**Evidence Reference:** Not Available

## 9.2 Baseline Collection Procedure

1. Define the baseline period.
2. Identify the required observations.
3. Collect actual data.
4. Validate the observations.
5. Calculate the baseline.
6. Document the result.
7. Preserve evidence.

## 9.3 Baseline Results

| Measurement | Value |
|---|---|
| Baseline Value | Not Yet Measured |
| Measurement Period | Pending |
| Valid Observations | Pending |
| Data Quality | Not Yet Evaluated |
| Verification Status | Pending |

## 9.4 Baseline Limitations

[Document limitations.]

### Important

Do not claim improvement without a suitable comparison.

If no baseline exists, the first valid measurement may establish the initial baseline.

---

# 10. Target and Performance Thresholds

## 10.1 Target Definition

**Target Status:** Not Yet Established

**Target Value:** To Be Determined

**Target Unit:** [Unit]

**Target Period:** [Period]

**Target Owner:** [Role]

## 10.2 Target Rationale

[Explain why the target is appropriate.]

Consider:

- Service requirements
- Historical performance
- Technical constraints
- Available resources
- Business impact
- Risk
- User expectations
- Improvement objectives

## 10.3 Performance Thresholds

| Threshold | Value | Meaning | Required Action |
|---|---|---|---|
| Acceptable | TBD | [Definition] | [Action] |
| Warning | TBD | [Definition] | [Action] |
| Critical | TBD | [Definition] | [Action] |

## 10.4 SLA and SLO Relationship

**Related SLA:** [Reference or Not Applicable]

**Related SLO:** [Reference or Not Applicable]

**Internal Performance Target:** [Reference or Not Yet Established]

### Important

An internal performance target is not automatically a Service Level Agreement.

An SLA requires an actual agreement between the relevant parties.

Do not claim SLA compliance unless the agreement, measurement method, and supporting results are documented.

---

# 11. Data Collection Record

Complete this section when actual observations are collected.

## 11.1 Collection Information

**Collection ID:** COL-###

**Metric ID:** MET-###

**Collection Date:** Pending

**Measurement Period:** Pending

**Collected By:** Not Applicable

**Source System:** [Specify]

**Collection Method:** [Specify]

## 11.2 Raw Observations

| Observation ID | Date/Time | Source | Observed Value | Unit | Validation |
|---|---|---|---|---|---|
| OBS-001 | [Date/Time] | [Source] | Not Collected | [Unit] | Pending |

## 11.3 Collection Notes

[Document relevant observations.]

## 11.4 Missing Data

**Missing Records Identified:** Not Yet Evaluated

**Description:**

[Document missing information.]

**Handling Method:**

[Explain how missing data was treated.]

## 11.5 Collection Evidence

**Evidence ID:** EVD-###

**Evidence Location:** [Relative path]

**Verification Status:** Pending

### Important

Do not replace unknown measurements with zero unless zero is the actual observed value.

---

# 12. Data Quality Validation

## 12.1 Validation Checklist

- [ ] Correct measurement period
- [ ] Correct data source
- [ ] Required fields available
- [ ] Duplicate records reviewed
- [ ] Missing values identified
- [ ] Consistent units
- [ ] Inclusion criteria followed
- [ ] Exclusion criteria followed
- [ ] Calculation inputs verified
- [ ] Supporting evidence retained

## 12.2 Data Quality Assessment

| Dimension | Assessment | Notes |
|---|---|---|
| Accuracy | Pending | [Notes] |
| Completeness | Pending | [Notes] |
| Consistency | Pending | [Notes] |
| Timeliness | Pending | [Notes] |
| Validity | Pending | [Notes] |
| Traceability | Pending | [Notes] |

## 12.3 Validation Outcome

**Data Quality Status:** Not Yet Evaluated

**Valid Observations:** Not Yet Determined

**Excluded Observations:** Not Yet Determined

**Outstanding Issues:**

[Document.]

## 12.4 Corrective Actions

[Document actions needed to improve data quality.]

### Important

A correct mathematical formula cannot compensate for inaccurate or incomplete source data.

---

# 13. Actual Performance Measurement

## 13.1 Measurement Summary

**Metric ID:** MET-###

**Reporting Period:** Pending

**Actual Result:** Not Yet Measured

**Measurement Unit:** [Unit]

**Data Source:** [Source]

**Calculation Method:** [Formula]

**Evidence Reference:** Not Available

## 13.2 Calculation Inputs

| Variable | Actual Value | Source | Verification |
|---|---|---|---|
| A | Pending | [Source] | Pending |
| B | Pending | [Source] | Pending |

## 13.3 Calculation

```text
[Insert actual calculation using verified values]
```

## 13.4 Calculation Result

**Calculated Value:** Not Yet Available

**Calculation Date:** Pending

**Verified By:** Not Applicable

**Verification Status:** Not Yet Verified

## 13.5 Measurement Limitations

[Document limitations affecting interpretation.]

### Important

Only report an actual result after the required observations have been collected and evaluated.

---

# 14. Performance Comparison

## 14.1 Baseline vs. Target vs. Actual

| Measurement | Value | Unit |
|---|---|---|
| Baseline | Not Yet Measured | [Unit] |
| Target | Not Yet Established | [Unit] |
| Actual | Not Yet Measured | [Unit] |
| Variance From Baseline | Not Available | [Unit] |
| Variance From Target | Not Available | [Unit] |

## 14.2 Variance Calculation

**Formula:**

```text
Absolute Variance = Actual Value - Comparison Value
```

**Percentage Change:**

```text
Percentage Change (%) =

(Actual Value - Baseline Value)
------------------------------- x 100
        Baseline Value
```

### Important

Percentage change is undefined when the baseline is zero.

Also, an increase is not always desirable.

For example:

- Higher service availability may be positive.
- Higher incident recurrence may be negative.

## 14.3 Target Achievement

**Target Achieved:** Not Yet Evaluated

**Evaluation:**

[Explain the result.]

## 14.4 Comparison Limitations

[Document differences in reporting periods, data populations, or collection methods.]

---

# 15. Trend Analysis

## 15.1 Historical Measurements

| Period | Actual Result | Target | Data Quality | Notes |
|---|---|---|---|---|
| [Period 1] | Pending | TBD | Pending | [Notes] |
| [Period 2] | Pending | TBD | Pending | [Notes] |
| [Period 3] | Pending | TBD | Pending | [Notes] |

## 15.2 Trend Direction

Select the observed trend.

- [ ] Improving
- [ ] Declining
- [ ] Stable
- [ ] Inconsistent
- [x] Insufficient Data

## 15.3 Trend Findings

[Describe observed patterns.]

## 15.4 Potential Contributing Factors

- [ ] Changes in service demand
- [ ] Changes in infrastructure
- [ ] Changes in staffing or resources
- [ ] Changes in ticket complexity
- [ ] Configuration changes
- [ ] Security events
- [ ] Monitoring changes
- [ ] Measurement definition changes
- [ ] Other: [Specify]

## 15.5 Trend Limitations

[Document limitations.]

### Important

A trend does not automatically establish causation.

Further investigation may be required to explain performance changes.

---

# 16. Performance Visualization

## 16.1 Visualization Type

Select an appropriate format.

- [ ] Line Chart
- [ ] Bar Chart
- [ ] Table
- [ ] Percentage Summary
- [ ] Trend Summary
- [ ] Not Applicable

## 16.2 Visualization Purpose

[Describe what the visualization communicates.]

## 16.3 Visualization Reference

**File:** [Relative path or Not Yet Created]

**Data Source:** [Source]

**Measurement Period:** [Period]

## 16.4 Visualization Requirements

- [ ] Uses verified or clearly labeled simulated data
- [ ] Measurement period identified
- [ ] Units labeled
- [ ] Target distinguished from actual results
- [ ] Data source documented
- [ ] Appropriate scale used
- [ ] Limitations identified

### Important

Charts should not imply greater precision or certainty than the underlying data supports.

---

# 17. Performance Analysis

## 17.1 Summary of Findings

[Summarize the measurement results.]

## 17.2 Positive Findings

[Document favorable results.]

## 17.3 Negative Findings

[Document unfavorable results.]

## 17.4 Unexpected Findings

[Document unexpected results.]

## 17.5 Potential Causes

[Identify possible contributing factors.]

**Root Cause Established:** [Yes / No / Not Applicable]

**Related Problem ID:** [PRB-### or Not Applicable]

## 17.6 Operational Impact

[Explain what the findings may mean for service delivery.]

## 17.7 Security Impact

[Document relevant security considerations.]

## 17.8 Analysis Limitations

[Describe uncertainty or missing information.]

### Important

Metric analysis should distinguish verified findings from hypotheses.

A metric may reveal a performance problem without identifying its root cause.

---

# 18. Continual Improvement Opportunities

## 18.1 Improvement Assessment

**Improvement Opportunity Identified:** [Yes / No / Pending]

**Description:**

[Describe the opportunity.]

## 18.2 Improvement Register Reference

**Improvement ID:** [IMP-### or Not Applicable]

**Improvement Status:** [Proposed / Under Assessment / Planned / In Progress / Completed]

[Continual Improvement Register](../Continual-Improvement/Improvement-Register.md)

## 18.3 Recommended Actions

| Action ID | Recommended Action | Expected Benefit | Priority | Status |
|---|---|---|---|---|
| ACT-001 | [Action] | [Benefit] | [Priority] | Proposed |

## 18.4 Success Criteria

| Criterion ID | Success Criterion | Measurement Method |
|---|---|---|
| SC-001 | [Criterion] | [Method] |

## 18.5 Follow-Up Measurement

**Follow-Up Required:** [Yes / No / Pending]

**Next Measurement Period:** [Period]

**Expected Evaluation Date:** [Date]

### Important

Identifying an improvement opportunity does not mean the improvement has been authorized, implemented, or successful.

---

# 19. Service Performance Reporting

## 19.1 Reporting Requirements

**Reporting Frequency:** [Monthly / Quarterly / Other]

**Report Owner:** [Role]

**Intended Audience:** [Roles]

**Reporting Format:** [Markdown / CSV / Dashboard / Other]

## 19.2 Reporting Summary

| Field | Value |
|---|---|
| Metric ID | MET-### |
| Metric Name | [Name] |
| Reporting Period | [Period] |
| Baseline | Pending |
| Target | Pending |
| Actual | Pending |
| Performance Status | Not Yet Evaluated |
| Improvement Required | Pending |

## 19.3 Report Findings

**Summary:**

[Document.]

**Risks:**

[Document.]

**Recommendations:**

[Document.]

## 19.4 Report Location

**Report File:** [Relative path or Not Yet Created]

### Proposed Reporting Structure

```text
Continual-Improvement/
└── Service-Metrics/
    ├── README.md
    ├── MET-###-Metric-Name.md
    └── Reports/
        ├── Monthly/
        └── Quarterly/
```

### Important

Reports should distinguish actual measurements from illustrative or simulated datasets.

---

# 20. Metric Review and Maintenance

## 20.1 Review Information

**Review Frequency:** [Monthly / Quarterly / Annual / Event-Driven]

**Last Review Date:** Not Yet Reviewed

**Next Review Date:** Not Yet Established

**Review Owner:** [Role]

## 20.2 Review Triggers

Review this metric when:

- Service objectives change.
- Measurement requirements change.
- The data source changes.
- Collection automation changes.
- Calculation methods change.
- Reporting requirements change.
- Performance targets change.
- Data quality issues are identified.
- A relevant improvement is completed.
- The metric no longer provides useful information.

## 20.3 Review Checklist

- [ ] Metric remains relevant
- [ ] Definition remains accurate
- [ ] Related service remains correct
- [ ] Data source remains available
- [ ] Calculation remains appropriate
- [ ] Collection method remains consistent
- [ ] Baseline remains relevant
- [ ] Target remains appropriate
- [ ] Data quality reviewed
- [ ] Evidence references valid
- [ ] Improvement opportunities considered
- [ ] Revision history updated

## 20.4 Review Outcome

**Review Status:** Pending

**Findings:**

[Document.]

**Required Changes:**

[Document.]

---

# 21. Metric Lifecycle

## 21.1 Lifecycle Status

Select the current status.

- [x] Proposed
- [ ] Under Development
- [ ] Ready for Measurement
- [ ] Active
- [ ] Under Review
- [ ] Suspended
- [ ] Retired

## 21.2 Status Definitions

| Status | Description |
|---|---|
| Proposed | Metric identified for potential use |
| Under Development | Definition and collection method being established |
| Ready for Measurement | Metric defined and collection requirements prepared |
| Active | Metric being collected and evaluated |
| Under Review | Metric undergoing formal reassessment |
| Suspended | Measurement temporarily paused |
| Retired | Metric no longer used for active reporting |

## 21.3 Retirement Assessment

**Retirement Required:** [Yes / No / Pending]

**Reason:** [Specify]

**Replacement Metric:** [MET-### or Not Applicable]

**Historical Data Retained:** [Yes / No / Not Applicable]

### Important

Retiring a metric should not automatically remove historical performance evidence.

---

# 22. Metric Definition Changes

Changes to a metric's calculation or scope may affect historical comparisons.

## 22.1 Change Record

| Version | Change | Reason | Effective Date | Historical Comparability |
|---|---|---|---|---|
| 1.0 | Initial definition | New metric | [Date] | Not Applicable |

## 22.2 Definition Change Assessment

**Definition Changed:** [Yes / No]

**Affected Fields:**

[Specify.]

**Affected Reporting Periods:**

[Specify.]

**Historical Results Comparable:** [Yes / No / Partially / Not Yet Evaluated]

## 22.3 Required Actions

- [ ] Update the metric definition
- [ ] Update calculation documentation
- [ ] Update collection procedures
- [ ] Review historical comparisons
- [ ] Notify relevant stakeholders where applicable
- [ ] Update reporting documentation

### Important

Do not silently recalculate historical results using a new method without documenting the change.

---

# 23. Evidence Register

Maintain evidence supporting the metric's collection, calculation, and analysis.

| Evidence ID | Evidence Type | Description | Collection Date | Source | File |
|---|---|---|---|---|---|
| EVD-001 | [Type] | [Description] | [Date] | [Source] | [Path] |

## 23.1 Acceptable Evidence

- Ticket records
- Incident logs
- Service request records
- Change records
- PowerShell output
- Windows Event Logs
- Monitoring data
- Azure Cost Management reports
- Configuration verification records
- Calculation worksheets
- Sanitized screenshots
- Technical test results

## 23.2 Evidence Requirements

Each evidence item should identify:

1. Metric ID
2. Measurement period
3. Data source
4. Collection date
5. Relevant observations
6. Calculation method
7. Verification status

## 23.3 Evidence Integrity

Do not fabricate:

- Ticket volumes
- Incident resolution times
- Service availability
- Change success rates
- Security compliance results
- Cost savings
- Performance improvements
- Automated reporting capabilities

## 23.4 Evidence Security

Before publishing:

- Remove credentials.
- Remove API keys and tokens.
- Remove sensitive user information.
- Sanitize tenant identifiers where necessary.
- Exclude confidential operational data.
- Review screenshots and exported reports.

---

# 24. Related Records

| Record Type | Reference | Relationship |
|---|---|---|
| Service Metric | MET-### | Current metric |
| Improvement | IMP-### | [If applicable] |
| Incident | INC-### | [If applicable] |
| Problem | PRB-### | [If applicable] |
| Change | CHG-### | [If applicable] |
| Configuration Item | CI-### | [If applicable] |
| Dependency Map | DM-### | [If applicable] |
| Knowledge Article | [Reference] | [If applicable] |
| Scenario | SCN-### | [If applicable] |
| Performance Report | [Reference] | [If applicable] |

Remove unused placeholders or mark them `Not Applicable`.

### Record Relationship Notes

[Explain relevant relationships.]

---

# 25. Service Metric Quality Checklist

## Identification

- [ ] Unique Metric ID assigned
- [ ] Descriptive metric name
- [ ] Related service identified
- [ ] Related ITIL practice identified
- [ ] Metric owner identified
- [ ] Lifecycle status accurate

## Definition

- [ ] Measurement objective defined
- [ ] Formal definition documented
- [ ] Unit specified
- [ ] Desired direction identified
- [ ] Start and end conditions defined where applicable
- [ ] Inclusion criteria documented
- [ ] Exclusion criteria documented
- [ ] Special conditions addressed

## Data Collection

- [ ] Data source identified
- [ ] Data availability verified
- [ ] Collection method documented
- [ ] Measurement frequency established
- [ ] Reporting frequency established
- [ ] Required permissions considered
- [ ] Automation status accurate

## Calculation

- [ ] Formula documented
- [ ] Variables defined
- [ ] Units consistent
- [ ] Zero denominators addressed
- [ ] Missing values handled appropriately
- [ ] Calculation reproducible

## Baseline and Target

- [ ] Baseline measured or marked unavailable
- [ ] Baseline period documented
- [ ] Target established or marked pending
- [ ] Target rationale recorded
- [ ] SLA and SLO distinctions maintained

## Validation

- [ ] Data quality reviewed
- [ ] Duplicate records checked
- [ ] Missing values identified
- [ ] Actual observations supported by evidence
- [ ] Calculation verified
- [ ] Limitations documented

## Reporting

- [ ] Actual results recorded
- [ ] Reporting period identified
- [ ] Baseline comparison included where available
- [ ] Target comparison included where available
- [ ] Trends evaluated
- [ ] Findings documented
- [ ] Recommendations supported by evidence

## Continual Improvement

- [ ] Performance gaps assessed
- [ ] Improvement opportunities considered
- [ ] Related Improvement IDs linked
- [ ] Follow-up measurements planned where appropriate
- [ ] Review requirements documented

## Portfolio Accuracy

- [ ] Fictional organization identified
- [ ] Simulated data clearly labeled
- [ ] Actual measurements distinguished from examples
- [ ] No fabricated results
- [ ] No unsupported integration claims
- [ ] No unverified improvement claims
- [ ] Sensitive information removed
- [ ] Relative links verified

---

# 26. Record Creation Instructions

Store individual metric records under:

`Continual-Improvement/Service-Metrics/`

## Recommended Naming Convention

```text
MET-###-Descriptive-Metric-Name.md
```

### Example

```text
Continual-Improvement/
├── README.md
├── Improvement-Register.md
└── Service-Metrics/
    ├── README.md
    ├── MET-001-Incident-Resolution-Time.md
    ├── MET-002-Service-Request-Fulfillment-Time.md
    └── Reports/
```

These filenames are illustrative.

## Creation Procedure

1. Identify the measurement objective.
2. Assign the next available Metric ID.
3. Copy this template.
4. Save it using the naming convention.
5. Replace placeholders.
6. Remove irrelevant example content.
7. Define the measurement scope.
8. Identify the data source.
9. Document the calculation method.
10. Establish the collection procedure.
11. Collect baseline data when available.
12. Define an appropriate target.
13. Begin actual measurement.
14. Preserve supporting evidence.
15. Review and update the metric regularly.

### Important

Creating a metric definition does not mean performance data has been collected.

A proposed metric should remain clearly identified as proposed until the collection method and actual measurements are established.

---

# 27. Document Review and Revision History

## Review Triggers

Review this template when:

- Metric documentation standards change.
- New reporting requirements are introduced.
- Data collection methods change.
- Calculation standards change.
- New ITSM or monitoring tools are introduced.
- Service performance objectives change.
- Continual Improvement procedures are revised.
- Data quality reviews identify documentation gaps.

## Revision History

| Version | Description |
|---|---|
| 1.0 | Initial reusable Service Metric Template aligned with ITIL 4 Continual Improvement |

---

## Portfolio Disclaimer

Technical Techno Tech is a fictional organization developed for hands-on IT training and professional portfolio development.

This template provides a standardized method for defining, collecting, calculating, validating, analyzing, and reporting IT service performance metrics within a simulated corporate IT environment.

Organizational roles, metric definitions, targets, reporting schedules, and operational scenarios may be proposed or simulated.

Actual service performance results must be supported by verifiable lab observations, technical output, or documented operational records.

Illustrative datasets and example calculations must not be presented as actual operational performance.

No automated ITSM reporting, SLA compliance, cost savings, service improvement, or monitoring integration is claimed unless supported by documented implementation and verification evidence.

GitHub Markdown files provide a lightweight documentation framework and are not represented as a production analytics or enterprise service reporting platform.

The purpose of this template is to demonstrate metric definition, measurement planning, data collection, calculation, baseline establishment, target setting, data quality validation, performance reporting, and evidence-based continual improvement.
