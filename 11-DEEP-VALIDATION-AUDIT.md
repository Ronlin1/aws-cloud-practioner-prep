# 11 — Deep Validation Audit — CLF-C02

**Validation date:** 2026-09-17  
**Objective:** verify this repository against the current AWS Certified Cloud Practitioner CLF-C02 exam guide, task statements, technologies/concepts list, in-scope/out-of-scope service lists, current Skill Builder preparation guidance, AWS Support documentation, and the current AWS AI/GenAI ecosystem.

---

# Validation result

The repository is aligned to the **current CLF-C02 blueprint** and keeps broader modern AWS material separate from exam requirements.

Validated exam facts:
- 65 total questions
- 50 scored + 15 unscored
- 90 minutes
- multiple choice + multiple response
- scaled passing score: 700/1000
- Domain 1: 24%
- Domain 2: 30%
- Domain 3: 34%
- Domain 4: 12%

AWS explicitly says the target candidate is not expected to perform deep:
- coding
- cloud architecture design
- troubleshooting
- implementation
- load/performance testing

The repository therefore prioritizes **recognition, differentiation, responsibility, service selection, business value, pricing, and support choices** rather than implementation depth.

---

# Domain 1 — Cloud Concepts — 24%

Covered:
- AWS Cloud value proposition
- global infrastructure benefits
- scalability vs elasticity
- agility
- high availability / fault tolerance / DR
- fixed vs variable expenditure
- Well-Architected six pillars
- AWS CAF six perspectives
- CAF business-outcome examples
- migration strategies
- cloud economics
- rightsizing
- automation
- BYOL / license-included concepts

**Status:** covered at CLF-C02 depth.

---

# Domain 2 — Security & Compliance — 30%

Covered:
- Shared Responsibility Model
- EC2 vs managed-service responsibility differences
- IAM users, groups, roles, policies
- AWS-managed vs customer-managed vs inline policies
- least privilege
- MFA
- password/access-key concepts
- IAM Identity Center
- federation and cross-account roles
- root-user protection and root-only task examples
- IAM credential reports
- encryption at rest / in transit
- KMS / CloudHSM / ACM
- Secrets Manager / Parameter Store recognition
- CloudWatch / CloudTrail / Config
- Artifact / Audit Manager
- GuardDuty / Inspector / Macie / Detective / Security Hub
- WAF / Shield / Firewall Manager
- Cognito / Directory Service / RAM
- Organizations / SCPs / Control Tower

**Status:** covered at CLF-C02 depth.

---

# Domain 3 — Cloud Technology & Services — 34%

Covered at the appropriate foundational recognition level:

## Compute and containers
- EC2
- Auto Scaling
- ELB
- Lambda
- Batch
- Elastic Beanstalk
- Lightsail
- Outposts
- ECR / ECS / EKS / Fargate

## Storage
- S3 and storage classes
- EBS
- Instance Store
- EFS
- FSx
- Storage Gateway
- Backup
- Elastic Disaster Recovery

## Databases
- RDS
- Aurora
- DynamoDB
- ElastiCache
- DocumentDB
- Neptune
- Redshift distinction
- DMS / SCT

## Networking
- VPC
- subnets / gateway / route concepts
- security groups vs NACLs
- Route 53
- CloudFront
- Direct Connect / VPN
- Transit Gateway
- PrivateLink
- Global Accelerator
- API Gateway

## Analytics
- Athena
- Glue
- EMR
- Kinesis
- QuickSight
- Redshift
- OpenSearch

## Current explicit CLF-C02 Machine Learning list
The current official in-scope page explicitly lists:
- Amazon Comprehend
- Amazon Kendra
- Amazon Lex
- Amazon Polly
- Amazon Q
- Amazon Rekognition
- Amazon SageMaker AI
- Amazon Textract
- Amazon Transcribe
- Amazon Translate

These are taught at recognition/use-case level.

## Other in-scope categories
- SQS / SNS / EventBridge / Step Functions
- Connect / SES
- CodeBuild / CodePipeline / X-Ray
- WorkSpaces / AppStream 2.0 / Secure Browser
- Amplify / AppSync
- IoT Core
- Systems Manager
- Service Catalog
- Service Quotas
- License Manager
- migration services

**Status:** covered at CLF-C02 recognition depth.

---

# Domain 4 — Billing, Pricing & Support — 12%

Covered:
- On-Demand
- Reserved Instances
- Savings Plans
- Spot
- Dedicated Hosts / Dedicated Instances
- Capacity Reservations
- Standard vs Convertible RI
- Regional vs Zonal RI
- RI flexibility concepts
- Organizations discount sharing
- data-transfer cost concepts
- S3 storage-tier cost logic
- Pricing Calculator
- Cost Explorer
- Budgets
- Cost and Usage Report
- cost allocation tag types
- Marketplace
- consolidated billing
- documentation / whitepapers / Prescriptive Guidance
- re:Post / Knowledge Center
- Trusted Advisor
- AWS Health
- Trust & Safety
- Professional Services
- Solutions Architects
- AWS Partner Network
- partner-benefit examples
- current-vs-legacy Support terminology

**Status:** covered at CLF-C02 depth.

---

# In-scope / out-of-scope audit

The current official service lists were rechecked during the public refresh.

Important rule from AWS:

> The in-scope and out-of-scope lists are non-exhaustive and subject to change.

Therefore:
- the task statements remain the primary authority
- explicit service lists are important but not the only source
- the repository avoids deep study of services explicitly listed out of scope

See:
- `10-OUT-OF-SCOPE-SKIP.md`
- `resources/OFFICIAL-AWS.md`

---

# Skill Builder validation

Current AWS Cloud Practitioner preparation guidance still recommends:
1. review the exam guide
2. use the Official Practice Question Set
3. use the Official Pretest to identify gaps
4. refresh weak topics
5. review/practice exam-style questions
6. use the Official Practice Exam where available

The repository links to durable exam-prep hubs rather than depending on stale direct course IDs.

See `resources/SKILL-BUILDER.md`.

---

# AWS Support transition validation

This remains a stale-material risk in 2026.

Current AWS Support documentation lists:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

The current CLF-C02 Domain 4 material still contains some legacy/transitional plan terminology.

The repository therefore teaches:
- current plan names
- recognition of legacy guide terminology
- support-selection concepts rather than fragile price-table memorization

---

# Modern AWS AI / GenAI validation

A separate research pass checked modern AI services so the repository is current without confusing the exam scope.

## Important findings

- **Amazon Q** and **Amazon SageMaker AI** remain explicitly listed in the current CLF-C02 Machine Learning service list.
- **Amazon Bedrock is not currently on the explicit CLF-C02 in-scope service list.**
- Bedrock, RAG, Knowledge Bases, Guardrails, and AgentCore are therefore treated as **supplemental modern AWS learning**, not CLF-C02 requirements.
- AWS states that **Amazon Bedrock Agents** is now **Amazon Bedrock Agents Classic** and is no longer open to new customers from **July 30, 2026**.
- AWS recommends **Amazon Bedrock AgentCore** for new agentic workloads.

See `resources/MODERN-AWS-AI.md`.

---

# Practice validation

## `practice/QUESTIONS.md`
50 scored-style original questions with exact official domain weighting:
- 12 Domain 1 = 24%
- 15 Domain 2 = 30%
- 17 Domain 3 = 34%
- 6 Domain 4 = 12%

Plus six extra Domain 3 service drills.

## `practice/TARGETED-GAPS-QUESTIONS.md`
30 original questions targeting explicit but easy-to-miss task-statement details.

Practice percentages are readiness heuristics only and must not be interpreted as direct conversions to AWS's 700/1000 scaled passing score.

---

# Privacy/public-repo audit

The public refresh removes personalized examples and uses generic labels instead.

Known personalized cost-tag examples were replaced with generic examples such as:
- `Project=WebApp`
- `Department=Engineering`
- `Environment=Production`

The current branch is also scanned for names, personal projects, employer/school/location references, email patterns, phone-like strings, IDs, and unfinished placeholders before merge.

Historical Git commits can retain removed text. See `DISCLAIMER.md`.

---

# Public resource library

The repository now includes:
- `resources/OFFICIAL-AWS.md`
- `resources/SKILL-BUILDER.md`
- `resources/MODERN-AWS-AI.md`
- `resources/COMMUNITY-RESOURCES.md`
- `resources/VALIDATION-NOTES.md`

This separates authoritative exam material from useful but non-exam modern AWS learning.

---

# Sources of truth

- Exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Technologies/concepts: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html
- In-scope list: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Out-of-scope list: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- AWS certification prep: https://aws.amazon.com/certification/certification-prep/
- Current Support plans: https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

---

# Final scope rule

For each topic, ask:

> Can AWS plausibly test recognition, differentiation, responsibility, use case, cost/support choice, or business value from this public CLF-C02 task statement?

If yes, learn it at foundational level.

If the learning activity is mainly implementation, debugging, coding, tuning, or advanced architecture configuration, postpone it until after CLF-C02.
