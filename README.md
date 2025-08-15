# Cloud Service Alternatives Report – CST8919

**Course:** DevOps Security and Compliance  
**Assignment:** 2 – Cloud Service Alternatives Report  
**Author:** Ajay Morla  
**Date:** August 15, 2025  

---

## 1. Introduction
This report compares Microsoft Azure services used in CST8919 with equivalent services in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**.  
It covers both the **core 5 services** required by the professor and **additional services we implemented in labs**, providing a broader cross-cloud mapping.

The analysis focuses on:
- Service overviews
- Core features
- Security & compliance
- Pricing models
- Integration with DevSecOps pipelines

---

## 2. Quick Comparison Table

| # | Azure Service | AWS Equivalent | GCP Equivalent |
|---|---------------|---------------|----------------|
| 1 | Azure Active Directory (SSO, IAM) | AWS IAM + IAM Identity Center (AWS SSO) | Google Cloud Identity + IAM |
| 2 | Azure Monitor & Log Analytics | Amazon CloudWatch + AWS CloudTrail | Google Cloud Operations Suite (Stackdriver) |
| 3 | Azure Policy | AWS Organizations + Service Control Policies (SCP) | Google Organization Policy Service |
| 4 | Defender for Cloud | AWS Security Hub + GuardDuty | Google Security Command Center (SCC) |
| 5 | Azure Sentinel (SIEM/SOAR) | Amazon Security Lake + Amazon Detective + GuardDuty | Chronicle Security Operations |
| 6 | Auth0 (as used in Flask App) | AWS Cognito | Google Identity Platform |
| 7 | Azure App Service | AWS Elastic Beanstalk | Google App Engine |
| 8 | Azure Alerts (Monitor + KQL) | AWS CloudWatch Alarms | Google Cloud Monitoring Alerts |
| 9 | Azure Diagnostic Settings & Activity Logs | AWS CloudTrail | Google Cloud Audit Logs |
| 10 | Azure Tagging & Resource Governance | AWS Resource Tagging + Tag Policies | GCP Labels + Organization Policy |

---

## 3. Detailed Comparisons

---

### 3.1 Azure Active Directory (SSO, IAM)
**AWS Equivalent:** AWS IAM + IAM Identity Center  
**GCP Equivalent:** Google Cloud Identity + IAM  

#### Overview
- **Azure AD:** Identity & access management, SSO, MFA, conditional access.  
- **AWS IAM + Identity Center:** Role-based access, SSO across AWS accounts and apps.  
- **GCP Cloud Identity + IAM:** Directory services with SSO and granular IAM.

#### Core Features
- User & group management  
- Role-based access control (RBAC)  
- SAML, OAuth2, OIDC support  
- MFA & conditional access

#### Security & Compliance
- ISO 27001, SOC 1/2/3, FedRAMP, HIPAA, GDPR across all three.

#### Pricing
- Azure AD Free + Premium P1/P2 per user/month  
- AWS IAM free; Identity Center free, pay for linked services  
- GCP Cloud Identity free tier + premium per user/month

#### DevSecOps Integration
- Access control in CI/CD  
- Automatable via Terraform, CloudFormation, Deployment Manager

---

### 3.2 Azure Monitor & Log Analytics
**AWS Equivalent:** Amazon CloudWatch + AWS CloudTrail  
**GCP Equivalent:** Google Cloud Operations Suite  

#### Overview
- Azure Monitor collects metrics, Log Analytics queries logs with KQL.  
- AWS CloudWatch for metrics/logs, CloudTrail for API audit logs.  
- GCP Operations Suite integrates monitoring/logging/alerting.

#### Core Features
- Metrics dashboards  
- Log aggregation & search  
- Alerts & automated actions  
- APM integration

#### Security & Compliance
- SOC, ISO, FedRAMP, HIPAA on all three.

#### Pricing
- Pay-per-GB ingested and retention period.

#### DevSecOps Integration
- Trigger workflows from alerts  
- Integrated with SIEM/SOAR like Sentinel or Splunk

---

### 3.3 Azure Policy
**AWS Equivalent:** AWS Organizations + SCP  
**GCP Equivalent:** Organization Policy Service  

#### Overview
- Azure Policy enforces compliance (e.g., restrict regions, require tags).  
- AWS SCP sets guardrails for accounts.  
- GCP Org Policy defines constraints.

#### Core Features
- Policy-as-code  
- Deny/modify non-compliant resources  
- Compliance dashboards

#### Security & Compliance
- Supports CIS, ISO, SOC, FedRAMP baselines.

#### Pricing
- No direct charge; costs may arise from remediation actions.

#### DevSecOps Integration
- Compliance checks in pipelines  
- Automated policy deployment via IaC

---

### 3.4 Defender for Cloud
**AWS Equivalent:** AWS Security Hub + GuardDuty  
**GCP Equivalent:** Security Command Center  

#### Overview
- CSPM + threat protection for Azure, hybrid, and multi-cloud.  
- AWS Security Hub aggregates findings; GuardDuty detects threats.  
- GCP SCC scans for misconfigurations and threats.

#### Core Features
- Compliance posture  
- Threat alerts  
- Remediation recommendations

#### Security & Compliance
- PCI DSS, HIPAA, ISO, SOC, FedRAMP.

#### Pricing
- Defender for Cloud: Free CSPM tier; paid per-resource protection.

#### DevSecOps Integration
- Continuous scans & alerts integrated into workflows

---

### 3.5 Azure Sentinel (SIEM/SOAR)
**AWS Equivalent:** Security Lake + Detective + GuardDuty  
**GCP Equivalent:** Chronicle Security Ops  

#### Overview
- Azure Sentinel ingests logs, detects threats, and automates response.  
- AWS Security Lake centralizes logs; Detective investigates; GuardDuty detects.  
- Chronicle provides Google-scale SIEM & SOAR.

#### Core Features
- Real-time threat detection  
- Playbook automation  
- Multi-source log ingestion

#### Pricing
- Pay-as-you-go per GB ingested.

#### DevSecOps Integration
- Automated incident response playbooks  
- Integration with ServiceNow, Jira

---

### 3.6 Auth0 (SSO for Flask App)
**AWS Equivalent:** AWS Cognito  
**GCP Equivalent:** Google Identity Platform  

#### Overview
- **Auth0** used in Flask lab for secure login with OIDC.  
- AWS Cognito handles auth & federation.  
- GCP Identity Platform offers similar auth services.

#### Core Features
- OIDC, OAuth2, SAML support  
- MFA, social logins  
- JWT token-based sessions

#### Pricing
- Auth0: Free tier + paid per active user  
- AWS Cognito: Monthly active users + data storage  
- GCP: Pay per MAU

#### DevSecOps Integration
- Secures access to app pipelines  
- Integration with CI/CD auth flows

---

### 3.7 Azure App Service
**AWS Equivalent:** AWS Elastic Beanstalk  
**GCP Equivalent:** Google App Engine  

#### Overview
- Azure App Service hosts Flask web app in lab.  
- AWS Beanstalk deploys apps without managing servers.  
- GCP App Engine provides serverless app hosting.

#### Core Features
- Auto-scaling  
- CI/CD integration  
- Language/runtime support

#### Pricing
- Pay for compute instance size + usage.

#### DevSecOps Integration
- Deploy from GitHub Actions  
- Integration with monitoring & alerts

---

### 3.8 Azure Alerts (Monitor + KQL)
**AWS Equivalent:** CloudWatch Alarms  
**GCP Equivalent:** Cloud Monitoring Alerts  

#### Overview
- Azure Alerts trigger actions based on KQL queries in Monitor.  
- AWS CloudWatch Alarms monitor metrics & logs.  
- GCP Alerts work within Monitoring.

#### Core Features
- Metric & log-based triggers  
- Multi-channel notifications  
- Auto-remediation hooks

#### Pricing
- Pay per alert rule & notifications beyond free tier.

#### DevSecOps Integration
- Automated incident tickets  
- Trigger Lambda/Functions for remediation

---

### 3.9 Azure Diagnostic Settings & Activity Logs
**AWS Equivalent:** AWS CloudTrail  
**GCP Equivalent:** Cloud Audit Logs  

#### Overview
- Diagnostic Settings forward logs to Log Analytics, Event Hub, or Storage.  
- AWS CloudTrail records account activity.  
- GCP Cloud Audit Logs track admin & data access events.

#### Core Features
- Governance & auditing  
- Long-term storage  
- Query & alerting integration

#### Security & Compliance
- Essential for compliance audits.

#### Pricing
- Pay for log storage & queries.

#### DevSecOps Integration
- Used in security investigations  
- Integrated with SIEM/SOAR

---

### 3.10 Azure Tagging & Resource Governance
**AWS Equivalent:** Resource Tagging + Tag Policies  
**GCP Equivalent:** Labels + Org Policy  

#### Overview
- Lab enforced ProjectName tag using Azure Policy.  
- AWS Tag Policies enforce consistent tagging.  
- GCP Labels used for cost tracking & governance.

#### Core Features
- Metadata for resources  
- Cost allocation  
- Policy enforcement

#### Pricing
- Free; cost only for enforcement tooling.

#### DevSecOps Integration
- Automate tagging in IaC  
- Tag-based cost & compliance reports

---

## 4. Conclusion
This expanded comparison covers **10 services** instead of the base 5, reflecting both course material and additional lab work.  
Across Azure, AWS, and GCP, equivalent capabilities exist for:
- Identity & access management  
- Monitoring & logging  
- Policy enforcement & governance  
- Threat detection & response  
- Application hosting & alerting  

For DevSecOps, all platforms provide:
- API access for automation  
- CI/CD integration  
- Compliance frameworks

However, differences in pricing, naming conventions, and integration depth mean that **choosing a provider** depends on existing infrastructure, team expertise, and compliance needs.

---
