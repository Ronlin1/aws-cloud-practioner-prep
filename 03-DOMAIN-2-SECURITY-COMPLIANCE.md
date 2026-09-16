# Domain 2 — Security & Compliance (30%)

This is the second-largest domain and one of the highest-return areas if you know the responsibility and service distinctions.

# 1. Shared Responsibility Model

The core statement:

- **AWS is responsible for security OF the cloud.**
- **The customer is responsible for security IN the cloud.**

## AWS generally manages
- physical data centers
- physical servers and storage hardware
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
- guest OS and patching
- installed software/application
- data
- security groups/network configuration
- IAM

### RDS
AWS manages more:
- database infrastructure
- host OS
- much of patching/maintenance depending on configuration

Customer still manages:
- data
- DB users/access
- schema/application logic
- security/configuration choices

### Lambda
AWS manages underlying servers and much of the runtime infrastructure.
Customer still manages:
- application code
- data
- IAM permissions
- application configuration

**Exam pattern:** as the service becomes more managed/serverless, AWS manages more of the underlying operational layers. The customer still owns data, identities, access decisions and application-level configuration.

---

# 2. IAM fundamentals

IAM = Identity and Access Management.

Think:
> WHO can perform WHAT ACTION on WHICH RESOURCE under WHICH CONDITIONS?

## IAM User
Long-term identity that can have console credentials and/or access keys.

## IAM Group
Collection of IAM users. Permissions can be attached to a group to simplify management.

## IAM Role
Assumable identity with permissions. Commonly provides **temporary credentials**.

Typical exam scenario:
> EC2 needs access to S3.

Correct approach:
> Attach/assign an appropriate IAM role rather than hard-code access keys.

## IAM Policy
JSON permission document defining allowed/denied actions/resources/conditions.

You do not need advanced JSON authoring for CLF-C02.

### AWS managed vs customer managed vs inline policies
Know at recognition level:

- **AWS managed policy**: standalone policy created and maintained by AWS; reusable across identities.
- **Customer managed policy**: standalone reusable policy you create/manage in your account; allows more precise organization-specific control.
- **Inline policy**: embedded directly into one user, group, or role; one-to-one relationship and not independently reusable.

Exam clue:
> “Who maintains the policy?” or “Which reusable policy can the customer edit?”

## Least privilege
Grant only the permissions required for the task.

## Authentication vs authorization
- **Authentication** = who are you?
- **Authorization** = what are you allowed to do?

Credentials, MFA and federation are authentication concepts; policies/roles determine authorization.

---

# 3. Root user, passwords and credentials

## AWS account root user
The root user has complete account access and should **not** be used for routine administration.

Best practice:
- protect root credentials
- register/use MFA
- do not use root for daily tasks
- avoid root access keys
- use IAM Identity Center/federated/admin identities for routine work

### Root-only task examples worth recognizing
AWS explicitly expects the exam candidate to identify tasks that require root credentials. You do not need the full long list. Know common examples:

For a standalone AWS account, root credentials can be required to:
- change the root email/password/access keys
- close the standalone AWS account
- restore IAM administrator permissions if the only admin locked themselves out
- activate IAM access to Billing and Cost Management
- perform certain tax/billing/account-level tasks
- register as a seller in the EC2 Reserved Instance Marketplace
- repair certain S3/SQS resource policies that deny all principals

**2026 nuance:** AWS Organizations can centrally perform some privileged/root operations for member accounts. Do not overgeneralize “only root can ever do X” across Organizations-managed member accounts.

## MFA
Adds another authentication factor. Root MFA is especially important.

## IAM password policy
An account can define password requirements for IAM users, such as:
- minimum length
- character requirements
- expiration/rotation settings
- password reuse prevention
- whether users can change their own passwords

Important: IAM user password policy does **not** control the root-user password or access keys.

## Access keys vs console password
- console password -> interactive sign-in for IAM user
- access key ID + secret access key -> long-term programmatic credentials for an IAM user
- temporary role/federated credentials -> preferred where practical over long-term keys

---

# 4. IAM Identity Center, federation and cross-account access

## IAM Identity Center
Centralized workforce access to multiple AWS accounts and applications.

Think:
> employees/workforce + many AWS accounts.

## Federation
Use identities from an external identity provider to obtain temporary/federated AWS access.

## Cross-account role
A role in one account can be assumed by an authorized principal from another account.

---

# 5. Access reporting and credential auditing

## IAM credential report
A downloadable account-level report listing IAM users and credential status, including items such as:
- password status/use
- access keys and rotation/use status
- MFA status
- signing certificates

Trigger:
> “Audit whether IAM users have MFA, stale passwords or old access keys.”

## Access reports / access analysis concept
AWS can provide information that helps identify which services/actions identities have accessed and support least-privilege reviews. At CLF-C02 level, recognize that IAM/access-analysis reporting helps audit and refine access rather than being an application-monitoring tool.

Do not confuse:
- credential report -> identity credential status
- CloudTrail -> API activity/event history
- Config -> resource configuration state/history

---

# 6. Encryption and secret/configuration storage

## Encryption at rest
Protect stored data, for example S3 objects, EBS/RDS data and backups.

## Encryption in transit
Protect data moving across networks, commonly with TLS/HTTPS.

## AWS KMS
Managed key-management service integrated with many AWS services.

Trigger:
> create/manage encryption keys.

## AWS CloudHSM
Dedicated hardware security module capability.

Trigger:
> dedicated HSM / direct cryptographic hardware control.

## AWS Secrets Manager
Purpose-built for secrets such as:
- database credentials
- API keys/tokens
- application secrets

Supports capabilities such as secret rotation and cross-account patterns.

## Systems Manager Parameter Store
Central store for configuration/key-value data. Supports:
- String
- StringList
- SecureString encrypted with KMS

Exam distinction:
- **Parameter Store** -> application/configuration parameters, including encrypted SecureString configuration
- **Secrets Manager** -> purpose-built secrets/credentials, especially when rotation or dedicated secret-management features are required

AWS currently recommends Secrets Manager for usernames/passwords/API keys/tokens.

## AWS Certificate Manager (ACM)
Provision/manage SSL/TLS certificates for supported AWS integrations.

### High-value comparison
- KMS -> encryption keys
- CloudHSM -> dedicated HSM hardware
- Secrets Manager -> credentials/secrets
- Parameter Store -> configuration parameters / SecureString
- ACM -> TLS certificates

---

# 7. Monitoring, auditing and governance

## Amazon CloudWatch
Operational monitoring:
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
- identity credential status -> IAM credential report

---

# 8. Threat/vulnerability/security services

## Amazon GuardDuty
Managed threat detection.

Trigger:
> suspicious/malicious activity, threat detection.

## Amazon Inspector
Vulnerability management for supported workloads.

Trigger:
> software vulnerabilities / exposure.

## Amazon Macie
Discover/classify sensitive data in S3.

Trigger:
> PII/sensitive information in S3.

## Amazon Detective
Security investigation/analysis.

Trigger:
> investigate context/root cause around suspicious findings.

## AWS Security Hub
Central security posture/findings aggregation across supported services/accounts.

Trigger:
> centralized security findings/posture.

### Memorize
- GuardDuty -> threats
- Inspector -> vulnerabilities
- Macie -> sensitive S3 data
- Detective -> investigate
- Security Hub -> centralize findings/posture

---

# 9. Network/web protection

## AWS WAF
Web Application Firewall. Filters HTTP(S) requests using rules.

Triggers:
- SQL injection patterns
- XSS patterns
- block IPs
- malicious HTTP requests

## AWS Shield
DDoS protection.

## AWS Firewall Manager
Centrally manage firewall/security policies across multiple accounts/resources.

### Memorize
- WAF -> malicious web requests
- Shield -> DDoS
- Firewall Manager -> centrally manage firewall policies

---

# 10. Cognito, Directory Service and RAM

## Amazon Cognito
Identity for **application end users**.

Trigger:
> users signing up/signing in to your mobile/web application.

## AWS Directory Service
Managed directory capabilities for workloads requiring directory integration such as Microsoft Active Directory scenarios.

## AWS Resource Access Manager (RAM)
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
- AWS compliance/security pages -> certifications/compliance information
- Config/Audit Manager/CloudTrail -> support governance/audit processes

---

# 13. Security support/resources

## AWS Marketplace
Third-party security software/products can be found and procured through AWS Marketplace.

## AWS Knowledge Center / re:Post Knowledge Center
Troubleshooting and curated support answers.

## AWS Security Center / security documentation / Security Blog
Official AWS security guidance and information.

## AWS Trusted Advisor
Best-practice checks/recommendations. Categories/features depend on support entitlement; associations include:
- cost optimization
- security
- performance
- resilience/fault tolerance
- service quotas

Do not confuse Trusted Advisor with GuardDuty or Inspector.

---

# 14. Credential exam traps

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
- credential/access reporting for audit

---

# Domain 2 instant recall

1. AWS physical infrastructure? -> **AWS responsibility**
2. EC2 guest OS patching? -> **Customer**
3. RDS underlying host/platform? -> **AWS**
4. Who deleted bucket? -> **CloudTrail**
5. CPU alarm? -> **CloudWatch**
6. Resource configuration history? -> **Config**
7. Compliance reports? -> **Artifact**
8. Audit evidence? -> **Audit Manager**
9. IAM password/MFA/access-key status across users? -> **IAM credential report**
10. Threat detection? -> **GuardDuty**
11. Vulnerability scanning? -> **Inspector**
12. Sensitive data in S3? -> **Macie**
13. Investigate security findings? -> **Detective**
14. Aggregate findings? -> **Security Hub**
15. DDoS? -> **Shield**
16. HTTP/web filtering? -> **WAF**
17. Encryption key management? -> **KMS**
18. Dedicated HSM? -> **CloudHSM**
19. Password/API secret needing secret management/rotation? -> **Secrets Manager**
20. Configuration parameter / SecureString? -> **Systems Manager Parameter Store**
21. TLS certificate? -> **ACM**
22. Application customer sign-in? -> **Cognito**
23. Workforce centralized access? -> **IAM Identity Center**
24. Guardrails across AWS accounts? -> **Organizations SCP**
25. Governed multi-account landing zone? -> **Control Tower**
26. Customer-created reusable IAM policy? -> **Customer managed policy**

# Official references

- CLF-C02 Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- IAM policies: https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- Root user: https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html
- IAM credential report: https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_getting-report.html
- Parameter Store: https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html
