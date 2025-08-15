# Cloud Service Alternatives Report – CST8919

**Course:** DevOps Security and Compliance  
**Assignment:** 2 – Cloud Service Alternatives Report  
**Author:** Ajay Morla  
**Date:** August 15, 2025  

---

## 1. Introduction
This report compares the Microsoft Azure services used in CST8919 with equivalent offerings in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**. The analysis focuses on features, security and compliance capabilities, pricing models, and integration potential for DevSecOps practices.  

The goal is to understand cross-cloud capabilities and prepare for multi-cloud or cloud migration scenarios in a DevSecOps environment.

---

## 2. Quick Comparison Table

| Azure Service | AWS Equivalent | GCP Equivalent |
|---------------|---------------|----------------|
| **Azure Active Directory** (SSO, IAM) | AWS IAM + AWS IAM Identity Center (formerly AWS SSO) | Google Cloud Identity + IAM |
| **Azure Monitor & Log Analytics** | Amazon CloudWatch + AWS CloudTrail | Google Cloud Operations Suite (Stackdriver) |
| **Azure Policy** | AWS Organizations + Service Control Policies (SCP) | Google Organization Policy Service |
| **Defender for Cloud** | AWS Security Hub + AWS GuardDuty | Google Security Command Center (SCC) |
| **Azure Sentinel** (SIEM/SOAR) | Amazon Security Lake + Amazon Detective + AWS GuardDuty | Chronicle Security Operations |

---

## 3. Detailed Comparisons

### 3.1 Azure Active Directory (SSO, IAM)
**AWS Equivalent:** AWS IAM + AWS IAM Identity Center  
**GCP Equivalent:** Google Cloud Identity + IAM  

#### Overview
- **Azure Active Directory (Azure AD):** Cloud-based identity and access management service supporting SSO, MFA, conditional access, and integration with Microsoft 365 and thousands of SaaS apps.  
- **AWS IAM + IAM Identity Center:** IAM controls AWS resource permissions; Identity Center provides SSO, MFA, and access to multiple AWS accounts and apps.  
- **Google Cloud Identity + IAM:** Directory service with SSO, MFA, user lifecycle management, and granular IAM for GCP resources.

#### Core Features
- **Azure AD:** SSO, MFA, conditional access, role-based access control (RBAC), identity protection.  
- **AWS IAM & Identity Center:** Fine-grained permissions, SSO, MFA, federated access, AWS CLI/SDK integration.  
- **GCP Cloud Identity & IAM:** SSO, MFA, security keys, service accounts, hierarchical access control.

#### Security & Compliance
- **Azure AD:** ISO 27001, SOC 1/2/3, FedRAMP High, HIPAA, GDPR.  
- **AWS IAM:** SOC 1/2/3, ISO 27001, FedRAMP, HIPAA.  
- **GCP IAM:** ISO 27001, SOC 1/2/3, FedRAMP, HIPAA, GDPR.

#### Pricing Model
- **Azure AD:** Free tier; Premium P1 ($6/user/month), Premium P2 ($9/user/month).  
- **AWS IAM:** Free; pay for advanced features like MFA with SMS and linked services.  
- **GCP IAM:** Free; Cloud Identity Premium $6/user/month.

#### DevSecOps Integration
- CI/CD access control (GitHub Actions, Jenkins, Azure DevOps, etc.).  
- Automated role assignment through IaC tools (Terraform, CloudFormation, Deployment Manager).  
- Supports least privilege principles and policy enforcement in pipelines.

---

### 3.2 Azure Monitor & Log Analytics
**AWS Equivalent:** Amazon CloudWatch + AWS CloudTrail  
**GCP Equivalent:** Google Cloud Operations Suite (formerly Stackdriver)  

#### Overview
- **Azure Monitor & Log Analytics:** End-to-end observability and logging platform, queryable via Kusto Query Language (KQL).  
- **Amazon CloudWatch & CloudTrail:** CloudWatch monitors metrics/logs; CloudTrail records AWS API calls and account activity.  
- **Google Cloud Operations Suite:** Logging, monitoring, and alerting for GCP resources and workloads.

#### Core Features
- Metrics collection and dashboards.  
- Log aggregation and search.  
- Alerts and automated actions.  
- Application performance monitoring (APM).  
- API and CLI support for automation.

#### Security & Compliance
All three services comply with ISO 27001, SOC, FedRAMP, and HIPAA (when configured).

#### Pricing Model
- **Azure Monitor:** Pay-per-GB ingested and retention; custom metrics billed separately.  
- **AWS CloudWatch:** Pay per metric, dashboard, and GB of logs; CloudTrail basic is free (90-day history).  
- **GCP Operations Suite:** Pay per GB of logs and metrics beyond free tier.

#### DevSecOps Integration
- Trigger security workflows based on alerts.  
- Integrates with SIEM/SOAR tools (e.g., Sentinel, Splunk).  
- API hooks for automated incident response.

---

### 3.3 Azure Policy
**AWS Equivalent:** AWS Organizations + Service Control Policies (SCP)  
**GCP Equivalent:** Google Organization Policy Service  

#### Overview
- **Azure Policy:** Enforces compliance by defining rules (policy definitions) applied to subscriptions/resource groups.  
- **AWS Organizations + SCP:** Central management of multiple AWS accounts with guardrails to limit allowed actions.  
- **Google Organization Policy Service:** Sets constraints at the organization, folder, or project level to enforce security and compliance.

#### Core Features
- Policy-as-code.  
- Deny/modify non-compliant resources.  
- Compliance dashboard and remediation.  
- Scope-based application (Org → Project/RG → Resource).

#### Security & Compliance
Supports CIS Benchmarks, ISO, SOC, FedRAMP, HIPAA across all clouds when policies match compliance baselines.

#### Pricing Model
- All three services: No direct charge; costs may apply for remediation actions or linked services.

#### DevSecOps Integration
- Automate policy deployment with Terraform/ARM/CloudFormation.  
- Integrate compliance checks into CI/CD pipelines.  
- Enable auto-remediation scripts.

---

### 3.4 Defender for Cloud
**AWS Equivalent:** AWS Security Hub + AWS GuardDuty  
**GCP Equivalent:** Google Security Command Center (SCC)  

#### Overview
- **Defender for Cloud:** CSPM and workload protection platform for Azure, hybrid, and multi-cloud environments.  
- **AWS Security Hub + GuardDuty:** Security Hub aggregates findings from AWS and partner tools; GuardDuty detects threats using ML and threat intelligence.  
- **GCP SCC:** Centralized security risk assessment and threat detection across GCP.

#### Core Features
- Posture management and compliance reporting.  
- Threat detection and alerting.  
- Integration with SIEM/SOAR tools.  
- Recommendations for remediation.

#### Security & Compliance
Covers CIS, PCI DSS, HIPAA, ISO 27001, SOC, and FedRAMP standards.

#### Pricing Model
- **Defender for Cloud:** Free tier for CSPM; per-resource pricing for advanced protection.  
- **AWS Security Hub:** Charged per finding and compliance check; GuardDuty billed per GB analyzed.  
- **GCP SCC:** Tiered pricing; per-asset and per-event charges.

#### DevSecOps Integration
- Continuous compliance checks in pipelines.  
- API-based integration for automated remediation.  
- Alerts to messaging platforms (Slack, Teams).

---

### 3.5 Azure Sentinel (SIEM/SOAR)
**AWS Equivalent:** Amazon Security Lake + Amazon Detective + AWS GuardDuty  
**GCP Equivalent:** Chronicle Security Operations  

#### Overview
- **Azure Sentinel:** Cloud-native SIEM/SOAR for threat detection, investigation, and automated response.  
- **Amazon Security Lake + Detective + GuardDuty:** Aggregates and analyzes security data; provides investigation tools and threat detection.  
- **GCP Chronicle Security Ops:** SIEM and SOAR platform with Google-scale analytics.

#### Core Features
- Ingest data from multiple sources.  
- Real-time threat detection.  
- Playbooks for automated response.  
- AI-driven investigation.

#### Security & Compliance
All comply with ISO 27001, SOC, FedRAMP, HIPAA when configured.

#### Pricing Model
- **Sentinel:** Pay-as-you-go for ingested data; commitment tiers for discount.  
- **AWS:** Pay per GB stored/processed; Detective and GuardDuty billed separately.  
- **GCP Chronicle:** Per GB/month pricing; tiered based on retention.

#### DevSecOps Integration
- Automated incident response workflows.  
- Integration with ticketing systems (Jira, ServiceNow).  
- Supports custom SOAR playbooks.

---

## 4. Conclusion
This comparison highlights that while Azure, AWS, and GCP offer similar core security and compliance capabilities, naming conventions, integration depth, and pricing models differ. For DevSecOps workflows, each platform supports automation, CI/CD integration, and compliance enforcement, but the choice often depends on existing ecosystem investments and organizational expertise.

