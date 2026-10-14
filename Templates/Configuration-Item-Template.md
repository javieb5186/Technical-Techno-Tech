# CI-XXX — Configuration Item Name

## Configuration Item Information

| Field | Details |
|---|---|
| **CI ID** | CI-XXX |
| **CI Name** | [Hostname / Device Name / Service Name] |
| **Organization** | Technical Techno Tech |
| **CI Type** | [Server / Workstation / Network Device / Application / Cloud Service / etc.] |
| **CI Category** | [Compute / Network / Storage / Software / Identity / etc.] |
| **Environment** | Simulated Enterprise |
| **Status** | Planned / Active / Under Maintenance / Retired |
| **Owner** | [Responsible Department / Service Owner] |
| **Managed By** | [Systems Administrator / Network Administrator / Endpoint Administrator] |
| **Date Created** | YYYY-MM-DD |
| **Last Updated** | YYYY-MM-DD |
| **Last Verified** | YYYY-MM-DD |
| **Related IT Service** | [IT-SVC-XXX — Service Name] |

---

## 1. Configuration Item Overview

### Description

[Describe the Configuration Item and its role within Technical Techno Tech's IT environment.]

### Business Purpose

[Explain why this CI exists and what business or operational requirement it supports.]

### Supported IT Services

| Service ID | Service Name | Relationship |
|---|---|---|
| IT-SVC-XXX | [Service Name] | [How this CI supports the service] |

**Reference:** [IT Service Catalog](../../../Service-Catalog.md)

---

## 2. Classification & Ownership

### Configuration Item Classification

- **CI Type:** [Server / Workstation / Network Device / Cloud Service / Application]
- **CI Category:** [Compute / Networking / Storage / Software / Identity]
- **Criticality:** [Low / Medium / High / Critical]
- **Lifecycle Status:** [Planned / Active / Under Maintenance / Retired]

### Ownership

| Responsibility | Assigned Role |
|---|---|
| **Service Owner** | [Role / Department] |
| **Technical Owner** | [Role / Department] |
| **Primary Administrator** | [IT Role] |
| **Support Team** | [IT Team] |

### Business Criticality

[Explain how the unavailability or failure of this CI could affect business operations.]

---

## 3. Technical Specifications

Complete the fields relevant to this Configuration Item.

### General Information

| Attribute | Value |
|---|---|
| **Hostname / Device Name** | [Name] |
| **Operating System / Platform** | [OS / Platform] |
| **Version / Build** | [Version] |
| **Manufacturer / Vendor** | [Vendor or N/A] |
| **Model / Instance Type** | [Model or VM Size] |
| **Asset Identifier** | [Asset Tag / Inventory ID / N/A] |
| **Location** | [Virtual Environment / Cloud Region / Simulated Office] |
| **Domain / Tenant** | [Domain or Tenant] |

### Hardware / Virtual Resources

| Resource | Configuration |
|---|---|
| **CPU / vCPU** | [Specification] |
| **Memory** | [RAM] |
| **Storage** | [Disk Capacity / Type] |
| **Network Adapters** | [Quantity / Type] |
| **Virtualization Platform** | [VMware / Hyper-V / Azure / N/A] |

### Network Configuration

| Attribute | Value |
|---|---|
| **IP Address** | [IP Address] |
| **Subnet Mask / Prefix** | [Subnet] |
| **Default Gateway** | [Gateway] |
| **DNS Servers** | [DNS Addresses] |
| **VLAN / Network Segment** | [VLAN / Segment] |
| **FQDN** | [Fully Qualified Domain Name] |

### Cloud Configuration

For cloud-based Configuration Items:

| Attribute | Value |
|---|---|
| **Cloud Provider** | [Microsoft Azure / Microsoft 365 / Other] |
| **Service / Resource Type** | [VM / Storage / Entra ID / etc.] |
| **Region** | [Region or N/A] |
| **Resource Group** | [Resource Group or N/A] |
| **Subscription / Tenant Reference** | [Non-sensitive Identifier] |
| **Service Tier / License** | [Tier or License] |

Remove sections that do not apply.

---

## 4. Installed Roles, Services & Software

### Server Roles / Features

- [Active Directory Domain Services]
- [DNS Server]
- [DHCP Server]
- [File Services]
- [Other installed roles]

### Installed Applications

| Application | Version | Purpose |
|---|---|---|
| [Application] | [Version] | [Purpose] |
| [Application] | [Version] | [Purpose] |

### Running Services

| Service | Purpose | Expected State |
|---|---|---|
| [Service Name] | [Purpose] | Running / Stopped / Automatic |

Include only components relevant to the CI.

---

## 5. Configuration Baseline

### Approved Configuration

[Describe the intended or approved configuration of this CI.]

### Key Configuration Settings

| Setting | Expected Value | Current Value | Status |
|---|---|---|---|
| [Setting 1] | [Expected] | [Actual] | Compliant / Noncompliant |
| [Setting 2] | [Expected] | [Actual] | Compliant / Noncompliant |
| [Setting 3] | [Expected] | [Actual] | Compliant / Noncompliant |

### Configuration Policies

- [Applicable Group Policy Object]
- [Intune Configuration Profile]
- [Security Baseline]
- [Firewall Policy]
- [Other relevant configuration]

### Configuration Verification

**Last Verified:** YYYY-MM-DD

**Verification Method:** [PowerShell / Administrative Console / Monitoring Tool / Manual Review]

**Verification Result:** Compliant / Noncompliant / Partially Compliant / Not Assessed

**Notes:**

[Document relevant findings.]

---

## 6. Relationships & Dependencies

Identify the other Configuration Items and services connected to this CI.

### CI Relationships

| Related CI | Relationship Type | Description |
|---|---|---|
| [CI-XXX](path-to-ci) | Depends On | [Dependency] |
| [CI-XXX](path-to-ci) | Provides Service To | [Description] |
| [CI-XXX](path-to-ci) | Hosted On | [Description] |
| [CI-XXX](path-to-ci) | Connected To | [Description] |

### Upstream Dependencies

[Identify systems or services required for this CI to operate.]

### Downstream Dependencies

[Identify systems, users, or services that rely on this CI.]

### Dependency Diagram

[Link to a network topology, infrastructure diagram, or service dependency map.]

### Impact of CI Failure

[Describe which services or infrastructure components would be affected if this CI became unavailable.]

---

## 7. Security Configuration

### Access Control

| Access Type | Authorized Role / Group | Permission Level |
|---|---|---|
| Administrative Access | [Role / Group] | [Permissions] |
| Remote Management | [Role / Group] | [Permissions] |
| Standard Access | [Role / Group] | [Permissions] |

### Security Controls

- [Firewall Configuration]
- [Endpoint Protection]
- [MFA / Conditional Access]
- [Group Policy Security Settings]
- [Encryption]
- [Logging and Auditing]

### Security Review

**Last Security Review:** YYYY-MM-DD or N/A

**Security Status:** Compliant / Noncompliant / Not Assessed

### Security Notes

[Document relevant security considerations without exposing credentials or other sensitive information.]

---

## 8. Monitoring & Maintenance

### Monitoring Configuration

| Monitoring Item | Tool / Method | Expected Condition |
|---|---|---|
| [CPU / Memory / Disk] | [Monitoring Tool] | [Threshold] |
| [Service Availability] | [Monitoring Tool] | [Expected State] |
| [Event Logs] | [Event Viewer / SIEM] | [Expected Condition] |
| [Network Connectivity] | [Ping / SNMP / Monitoring] | [Expected Condition] |

### Maintenance Activities

- [Operating system updates]
- [Application updates]
- [Security patching]
- [Backup verification]
- [Configuration review]
- [Performance review]

### Maintenance Schedule

**Frequency:** [Daily / Weekly / Monthly / As Required]

**Responsible Role:** [IT Role]

**Last Maintenance:** YYYY-MM-DD or N/A

**Next Planned Maintenance:** YYYY-MM-DD or N/A

---

## 9. Backup & Recovery

### Backup Configuration

**Backup Required:** Yes / No

**Backup Method:** [Windows Server Backup / Azure Backup / Other / N/A]

**Backup Frequency:** [Schedule or N/A]

**Backup Destination:** [Non-sensitive Location or Reference]

**Last Successful Backup:** YYYY-MM-DD or N/A

### Recovery Information

**Recovery Procedure:** [Knowledge Article / Procedure Link]

**Recovery Dependencies:** [Required Systems / Services]

**Recovery Testing:** [Last Test Date / Not Tested]

### Recovery Considerations

[Describe any special requirements or limitations.]

**Note:** Backup and recovery methods must be appropriate for the workload. For example, Active Directory Domain Services requires supported domain controller backup and recovery procedures.

---

## 10. Configuration History

Track significant configuration changes affecting this CI.

| Date | Change ID | Description | Result |
|---|---|---|---|
| YYYY-MM-DD | [CHG-XXX](path-to-change) | [Configuration Change] | [Result] |
| YYYY-MM-DD | [CHG-XXX](path-to-change) | [Configuration Change] | [Result] |

### Current Configuration Summary

[Summarize the current configuration following the most recent verified changes.]

**Note:** Detailed implementation steps, approvals, and testing evidence should remain in the associated Change Enablement records rather than being duplicated here.

---

## 11. Related Operational Records

### Incidents

- [INC-XXX — Incident Title](path-to-incident)

### Problems

- [PRB-XXX — Problem Title](path-to-problem)

### Changes

- [CHG-XXX — Change Title](path-to-change)

### Service Requests

- [SR-XXX — Service Request Title](path-to-request)

### Knowledge Articles

- [KB-XXX — Knowledge Article Title](path-to-article)

### Infrastructure Documentation

- [Relevant Infrastructure Document](path-to-document)

Use N/A when no related records exist.

---

## 12. Verification & Evidence

### Configuration Verification

| Verification Item | Expected Result | Actual Result | Status |
|---|---|---|---|
| [Hostname / Identity] | [Expected] | [Observed] | Pass / Fail |
| [Network Configuration] | [Expected] | [Observed] | Pass / Fail |
| [Required Services] | [Expected] | [Observed] | Pass / Fail |
| [Security Configuration] | [Expected] | [Observed] | Pass / Fail |

### Supporting Evidence

- [System Information](Evidence/system-information.png)
- [Network Configuration](Evidence/network-configuration.txt)
- [Service Configuration](Evidence/services.png)
- [Configuration Verification](Evidence/verification.png)

Include only evidence actually collected.

### Verification Summary

[Explain whether the CI matches its documented configuration.]

---

## 13. Lifecycle Management

### Lifecycle Information

| Field | Details |
|---|---|
| **Deployment Date** | YYYY-MM-DD or Planned |
| **Current Lifecycle Stage** | Planned / Active / Maintenance / Retired |
| **Last Major Update** | YYYY-MM-DD or N/A |
| **Planned Replacement / Retirement** | YYYY-MM-DD or N/A |
| **Retirement Date** | YYYY-MM-DD or N/A |

### Retirement Considerations

If the CI is being retired:

- [Identify dependent services]
- [Migrate or remove workloads]
- [Revoke unnecessary access]
- [Securely remove or archive data]
- [Update related configuration records]
- [Verify retirement completion]

### Lifecycle Notes

[Document any relevant lifecycle decisions or planned changes.]

---

## 14. Lessons Learned

### What I Learned

- [Technical concept learned or reinforced]
- [Infrastructure relationship or dependency understood]
- [Configuration management principle applied]

### Skills Practiced

- [Windows Server / Active Directory / Networking / Azure / etc.]
- [PowerShell / Administrative Tools]
- [Configuration verification]
- [Infrastructure documentation]
- [Service Configuration Management]

### Improvement Opportunities

- [Potential configuration improvement]
- [Monitoring enhancement]
- [Automation opportunity]
- [Documentation improvement]

---

## 15. Configuration Item Review

| Field | Details |
|---|---|
| **CI Status** | Planned / Active / Under Maintenance / Retired |
| **Configuration Verified** | Yes / No / Partially |
| **Documentation Current** | Yes / No |
| **Dependencies Documented** | Yes / No / Partially |
| **Security Reviewed** | Yes / No / Not Applicable |
| **Last Review Date** | YYYY-MM-DD |
| **Next Review Date** | YYYY-MM-DD |

### Review Summary

[Summarize the current state of the Configuration Item, any discrepancies, and required follow-up actions.]

---

## Simulation Disclaimer

This Configuration Item represents simulated IT infrastructure within Technical Techno Tech, a fictional technology solutions company.

Technical configurations, infrastructure relationships, and verification results are documented based on hands-on work performed in controlled lab environments.

Business ownership, administrative responsibilities, and operational processes may be simulated for educational and portfolio purposes.
