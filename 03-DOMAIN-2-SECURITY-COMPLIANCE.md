# Domain 2 — Security & Compliance (30%)

This is the second-largest domain and one of the easiest places to gain marks if you know the service distinctions.

# 1. Shared Responsibility Model

The core statement:

- **AWS is responsible for security OF the cloud.**
- **The customer is responsible for security IN the cloud.**

## AWS generally manages
- physical data centers
- physical servers
- storage hardware
- physical network
- underlying managed infrastructure
- virtualization/hypervisor layer for EC2

## Customer generally manages
- data
- identities and permissions
- application code/configuration
- encryption choices
- network/security configuration
- guest operating systems on EC2

## Responsibility changes by service

### EC2
Customer manages more:
- guest OS
- OS patching
- installed software
- application
- data
- security groups/network configuration
- IAM

### RDS
AWS manages more:
- database infrastructure
- host OS
- much of patching/maintenance/backups depending on configuration

Customer still manages:
- data
- DB users/access
- schema/application logic
- security choices

### Lambda
AWS manages underlying servers and much of runtime infrastructure.
Customer still manages:
- application code
- data
- IAM permissions
- configuration

**Exam pattern:** the more managed/serverless the service, the more underlying operational work AWS handles. The customer still owns data and access decisions.

---

# 2. IAM fundamentals

IAM = Identity and Access Management.

Think:
> WHO can perform WHAT ACTION on WHICH RESOURCE under WHICH CONDITIONS?

## IAM User
Long-term identity that can have credentials.

## IAM Group
Collection of users. Permissions can be assigned to a group to simplify management.

## IAM Role
Assumable identity with permissions. Commonly provides **temporary credentials**.

Typical exam scenario:
> EC2 needs access to S3.

Correct approach:
> Attach/assign an appropriate IAM role rather than hard-code access keys.

## IAM Policy
JSON permission document defining allowed/denied actions/resources/conditions.

You do not need advanced policy-authoring syntax for CLF-C02.

## Least privilege
Grant only the permissions required for the task.

## MFA
Requires an additional authentication factor. Very important for privileged/root access.

## Root user
Root has extremely powerful account-level privileges.

Best practice:
- protect credentials
- enable MFA
- do not use root for daily work
- avoid root access keys
- use appropriately privileged IAM/federated identities instead

## IAM Identity Center
Centralized workforce access to multiple AWS accounts and applications.

Think:
> employees/workforce + many AWS accounts.

## Federation
Use identities from an external identity provider to access AWS through temporary/federated access.

## Cross-account role
A role in one account can be assumed by an authorized principal from another account.

---

# 3. Authentication vs authorization

- **Authentication** = who are you?
- **Authorization** = what are you allowed to do?

IAM credentials/MFA/federation relate to authentication; policies/roles define authorization.

---

# 4. Encryption

## Encryption at rest
Protect stored data.

Examples:
- S3 objects
- EBS volumes
- RDS data
- backups

## Encryption in transit
Protect data moving across networks, commonly using TLS/HTTPS.

## AWS KMS
Managed key-management service integrated with many AWS services.

**Trigger:** create/manage encryption keys.

## AWS CloudHSM
Dedicated hardware security module capability.

**Trigger:** dedicated HSM / more direct control over cryptographic hardware.

## AWS Secrets Manager
Store and manage secrets such as:
- database credentials
- API keys/tokens
- application secrets

Can support rotation.

## AWS Certificate Manager (ACM)
Provision/manage SSL/TLS certificates for supported AWS integrations.

### High-value comparison
- KMS -> encryption keys
- CloudHSM -> dedicated HSM cryptographic hardware
- Secrets Manager -> credentials/secrets
- ACM -> TLS certificates

---

# 5. Monitoring, auditing, governance

## Amazon CloudWatch
Operational monitoring.

Think:
- metrics
- logs
- alarms
- dashboards

Trigger:
> “Alert when EC2 CPU exceeds 80%.”

## AWS CloudTrail
Records AWS API/account activity.

Think:
- who did it?
- what API action?
- when?

Trigger:
> “Which identity deleted this S3 bucket?”

## AWS Config
Tracks resource configurations/configuration changes and can evaluate against rules.

Trigger:
> “Was this security group compliant?” / “How did resource configuration change?”

## AWS Audit Manager
Helps automate collection of evidence for audits/compliance assessments.

## AWS Artifact
Self-service access to AWS compliance reports and certain agreements.

Trigger:
> “Download AWS SOC/compliance documentation.”

### Remember
- performance/metrics -> CloudWatch
- API audit -> CloudTrail
- configuration history/compliance -> Config
- audit evidence -> Audit Manager
- AWS compliance reports -> Artifact

---

# 6. Threat/vulnerability/security services

## Amazon GuardDuty
Managed threat-detection service.

Trigger:
> suspicious/malicious activity, threat detection.

## Amazon Inspector
Vulnerability management for supported workloads.

Trigger:
> software vulnerabilities / exposure.

## Amazon Macie
Discover/protect sensitive data in S3.

Trigger:
> PII/sensitive information in S3.

## Amazon Detective
Security investigation/analysis.

Trigger:
> investigate root cause/context around suspicious security findings.

## AWS Security Hub
Central security posture/findings aggregation across supported AWS services/accounts.

Trigger:
> centralized security findings/posture.

### Memorize
- GuardDuty -> threats
- Inspector -> vulnerabilities
- Macie -> sensitive S3 data
- Detective -> investigate
- Security Hub -> centralize findings/posture

---

# 7. Network/web protection

## AWS WAF
Web Application Firewall.

Protects/filter HTTP(S) web requests using rules.

Triggers:
- SQL injection patterns
- XSS patterns
- block IPs
- malicious HTTP requests

## AWS Shield
DDoS protection.

Trigger:
> distributed denial-of-service attack.

## AWS Firewall Manager
Centrally manage firewall/security policies across multiple accounts/resources.

### Memorize
- WAF -> malicious web requests
- Shield -> DDoS
- Firewall Manager -> centrally manage firewall policies

---

# 8. Amazon Cognito vs IAM

## IAM
Controls identities/permissions for AWS resources and workforce/service access.

## Cognito
Identity for **application end users**.

Trigger:
> users signing up/signing in to your mobile/web application.

---

# 9. AWS Directory Service

Managed directory capabilities for workloads requiring directory integration such as Microsoft Active Directory use cases.

Recognition-level knowledge is enough for CLF-C02.

---

# 10. AWS Resource Access Manager (RAM)

Share supported AWS resources across AWS accounts/within an organization.

Trigger:
> centrally share supported resources across accounts.

---

# 11. AWS Organizations + Control Tower security/governance

## AWS Organizations
Central management of multiple AWS accounts.

Know:
- organizational units (OUs)
- consolidated billing
- Service Control Policies (SCPs)

### SCP exam rule
An SCP is a **permission guardrail**. It does **not itself grant IAM permissions**.

## AWS Control Tower
Helps set up and govern a multi-account AWS environment/landing zone using controls/guardrails.

Trigger:
> standardized governed multi-account environment.

---

# 12. Compliance concepts

Important principle:
> AWS being compliant does NOT automatically make your workload compliant.

Customers still need to configure/use services in accordance with their legal/regulatory/industry obligations.

Compliance requirements can vary by:
- industry
- geography
- data type
- service

Common exam resources:
- Artifact -> reports/agreements
- AWS compliance pages/trust resources -> current certifications/compliance information
- Config/Audit Manager/CloudTrail -> support governance/audit processes

---

# 13. AWS Marketplace security

Third-party security products can be purchased/deployed through AWS Marketplace.

Exam wording:
> “Where can customer find third-party security software for AWS?”

Answer:
> AWS Marketplace.

---

# 14. Trusted Advisor

Trusted Advisor provides best-practice checks/recommendations. Categories/features depend on support entitlement, but exam associations include:
- cost optimization
- security
- performance
- fault tolerance/reliability
- service quotas

Do not confuse Trusted Advisor with GuardDuty or Inspector.

---

# 15. Credential exam traps

Bad patterns:
- embedding access keys in source code
- sharing root credentials
- giving administrator permissions to everyone
- using long-term user credentials when a role is appropriate

Better patterns:
- roles and temporary credentials
- least privilege
- MFA
- centralized identity/federation
- Secrets Manager for secrets

---

# Domain 2 instant recall

1. AWS physical infrastructure? -> **AWS responsibility**
2. EC2 guest OS patching? -> **Customer**
3. RDS underlying DB host OS? -> **AWS**
4. Who deleted bucket? -> **CloudTrail**
5. CPU alarm? -> **CloudWatch**
6. Resource configuration history? -> **Config**
7. Compliance reports? -> **Artifact**
8. Audit evidence? -> **Audit Manager**
9. Threat detection? -> **GuardDuty**
10. Vulnerability scanning? -> **Inspector**
11. Sensitive data in S3? -> **Macie**
12. Investigate security findings? -> **Detective**
13. Aggregate findings? -> **Security Hub**
14. DDoS? -> **Shield**
15. HTTP/web filtering? -> **WAF**
16. Encryption key management? -> **KMS**
17. Dedicated HSM? -> **CloudHSM**
18. Password/API secret? -> **Secrets Manager**
19. TLS certificate? -> **ACM**
20. Application customer sign-in? -> **Cognito**
21. Workforce centralized access? -> **IAM Identity Center**
22. Guardrails across AWS accounts? -> **Organizations SCP**
23. Governed multi-account landing zone? -> **Control Tower**

# Official reference

https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
