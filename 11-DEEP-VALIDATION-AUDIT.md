# 11 — Deep Validation Audit — CLF-C02

**Validation date:** 2026-09-16  
**Objective:** verify this repository against the current AWS Certified Cloud Practitioner CLF-C02 exam guide, domain task statements, technologies/concepts list, in-scope/out-of-scope service lists, current Skill Builder preparation guidance, and current AWS Support documentation.

# Validation result

The repository is structured around the **current CLF-C02 blueprint**, not around an old course syllabus.

Official exam facts validated:
- 65 total questions
- 50 scored + 15 unscored
- 90 minutes
- multiple choice + multiple response
- scaled passing score: 700/1000
- Domain 1: 24%
- Domain 2: 30%
- Domain 3: 34%
- Domain 4: 12%

AWS explicitly lists these candidate tasks as out of scope:
- coding
- designing cloud architecture
- troubleshooting
- implementation
- load/performance testing

The repo therefore prioritizes scenario recognition, concepts and service selection rather than hands-on implementation depth.

---

# Domain-by-domain coverage audit

## Domain 1 — Cloud Concepts — 24%

### Task 1.1 Benefits of AWS Cloud
Covered:
- global reach/infrastructure benefits
- high availability
- elasticity
- agility
- scalability
- economies of scale
- fixed vs variable expenditure

Primary files:
- `02-DOMAIN-1-CLOUD-CONCEPTS.md`
- `08-LAST-MINUTE-CRAM.md`

### Task 1.2 Design principles
Covered:
- six Well-Architected pillars
- scenario trigger for each pillar
- CAF vs Well-Architected distinction

### Task 1.3 Migration benefits/strategies
Covered:
- migration business/technical reasons
- AWS CAF six perspectives
- 7 Rs concepts
- migration-service recognition
- Snow Family offline transfer

### Task 1.4 Cloud economics
Covered:
- fixed/variable cost
- on-prem cost categories
- BYOL/license included
- rightsizing
- automation
- economies of scale

**Domain 1 status: covered at CLF-C02 depth.**

---

## Domain 2 — Security & Compliance — 30%

### Task 2.1 Shared Responsibility
Covered:
- security OF vs IN the cloud
- EC2 customer responsibilities
- RDS/Lambda increased AWS management responsibility

### Task 2.2 Security, governance and compliance
Covered:
- encryption at rest/in transit
- CloudWatch / CloudTrail / Config
- Artifact / Audit Manager
- GuardDuty / Inspector / Security Hub / Shield
- compliance principle
- access/security reporting concepts

### Task 2.3 Access management
Validated and explicitly expanded during this audit:
- IAM users/groups/roles/policies
- AWS managed vs customer managed vs inline policies
- least privilege
- access keys vs passwords
- IAM password policy
- MFA
- IAM Identity Center
- federation
- cross-account roles
- root-user protection
- root-only task examples
- IAM credential report
- Secrets Manager
- Systems Manager Parameter Store / SecureString

### Task 2.4 Security resources
Covered:
- WAF / Shield / Firewall Manager
- GuardDuty / Inspector / Macie / Detective / Security Hub
- KMS / CloudHSM / ACM / Secrets Manager
- Marketplace third-party security software
- Trusted Advisor
- AWS security/support knowledge resources

**Domain 2 status: covered at CLF-C02 depth after audit patch.**

---

## Domain 3 — Cloud Technology & Services — 34%

### Task 3.1 Deploy/operate AWS
Covered:
- Console
- CLI
- APIs/SDKs
- Infrastructure as Code
- CloudFormation
- one-time/manual vs repeatable/automated operation recognition
- cloud/on-prem/hybrid deployment models

### Task 3.2 Global infrastructure
Covered:
- Regions
- Availability Zones
- edge locations
- Multi-AZ vs Multi-Region
- Region selection factors

### Task 3.3 Compute
Covered:
- EC2
- EC2 instance categories
- Auto Scaling
- Elastic Load Balancing
- ECS / EKS / Fargate / ECR
- Lambda
- Batch
- Elastic Beanstalk
- Lightsail
- Outposts

### Task 3.4 Databases
Covered:
- RDS
- Aurora
- DynamoDB
- ElastiCache
- DocumentDB
- Neptune
- DMS
- SCT
- Redshift distinction

### Task 3.5 Networking
Covered:
- VPC / subnets / gateways / route-table concept
- Security Groups vs NACLs
- Route 53
- CloudFront
- VPN / Direct Connect
- Transit Gateway
- PrivateLink
- Global Accelerator
- API Gateway

### Task 3.6 Storage
Covered:
- S3 + storage classes + lifecycle
- EBS
- Instance Store
- EFS
- FSx
- Storage Gateway
- Backup
- Elastic Disaster Recovery

### Task 3.7 AI/ML and analytics
Covered at recognition level:
- Athena
- Glue
- EMR
- Kinesis
- QuickSight
- Redshift
- OpenSearch
- SageMaker AI
- Comprehend
- Kendra
- Lex
- Polly
- Transcribe
- Translate
- Rekognition
- Textract
- Amazon Q

### Task 3.8 Other in-scope service categories
Covered at recognition level:
- SQS / SNS / EventBridge / Step Functions
- SES / Connect
- CodeBuild / CodePipeline / X-Ray
- WorkSpaces / AppStream 2.0 / Secure Browser
- Amplify / AppSync
- IoT Core
- Systems Manager / Service Catalog / Service Quotas / License Manager
- migration services

**Domain 3 status: covered at CLF-C02 recognition depth.**

---

## Domain 4 — Billing, Pricing & Support — 12%

### Task 4.1 Pricing models
Validated and explicitly expanded during this audit:
- On-Demand
- Reserved Instances
- Savings Plans
- Spot
- Dedicated Hosts
- Dedicated Instances
- Capacity Reservations
- Standard vs Convertible RIs
- Regional vs Zonal RIs
- RI Availability Zone / instance-size flexibility concept
- RI/Savings Plans discount sharing in AWS Organizations
- storage-tier cost logic
- inbound/outbound/cross-Region transfer concept

### Task 4.2 Billing and cost management
Covered:
- Pricing Calculator
- Cost Explorer
- Budgets
- Cost and Usage Report
- Organizations consolidated billing
- AWS-generated vs user-defined cost allocation tags
- tag activation for cost analysis/reporting
- Marketplace billing/procurement concept

### Task 4.3 Technical resources and support
Validated and explicitly expanded during this audit:
- Documentation
- Whitepapers
- Prescriptive Guidance
- Knowledge Center / re:Post
- Support Center
- Trusted Advisor
- Health Dashboard / AWS Health API
- Trust & Safety
- Professional Services
- Solutions Architects
- AWS Partner Network
- ISVs vs consulting/system-integration partners
- Marketplace
- current and legacy/transitional Support plan terminology

**Domain 4 status: covered after audit patch.**

---

# In-scope service-list audit

The current official in-scope list was cross-checked category by category against this repo.

High-level categories confirmed:
- Analytics
- Application Integration
- Business Applications
- Cloud Financial Management
- Compute
- Containers
- Customer Enablement
- Database
- Developer Tools
- End User Computing
- Frontend Web and Mobile
- Internet of Things
- Machine Learning
- Management and Governance
- Migration and Transfer
- Networking and Content Delivery
- Security, Identity, and Compliance
- Serverless
- Storage

The repo teaches high-frequency/core services in detail and lower-frequency in-scope services primarily at **recognition level**, which matches the foundational exam target.

---

# Out-of-scope audit

`10-OUT-OF-SCOPE-SKIP.md` was cross-checked against the current AWS out-of-scope page.

Examples intentionally excluded from deep study include:
- Amazon MSK
- Amazon Timestream for LiveAnalytics
- AWS App Runner
- AWS Billing Conductor
- Amazon Keyspaces
- Amazon MemoryDB
- AWS CodeArtifact
- AWS CodeDeploy
- AWS CloudShell
- IoT Greengrass
- Amazon Personalize
- VPC Lattice
- AWS Network Firewall
- Amazon FSx for Lustre

Important: AWS says the out-of-scope list is **non-exhaustive and subject to change**, so official task statements remain the primary scope authority.

---

# Skill Builder validation

Current AWS preparation guidance was re-checked.

AWS recommends:
1. Review exam guide.
2. Use Official Practice Question Set.
3. Use Official Pretest to identify gaps.
4. Refresh weak topics.
5. Review/practice exam-style questions.
6. Use Official Practice Exam if subscription access is available.

Current Cloud Practitioner Essentials listing was validated as a long foundational course, about **12h45m** and last updated May 15, 2026. With a 48-hour deadline, the repo recommends targeted use rather than mandatory full-course completion.

The old direct Skill Builder URL for the Official Practice Question Set was found to be stale and was removed. The repo now points to the current certification page/exam-prep hub as the durable entry point.

---

# AWS Support 2026 transition validation

This was a stale-material risk and received special validation.

Current AWS Support documentation lists:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

AWS states these legacy plans retire January 1, 2027:
- Developer Support
- Business Support
- Enterprise On-Ramp

However, the current CLF-C02 Domain 4 task page still names legacy plans as examples. The repository therefore teaches:
- current live plan names
- recognition of the legacy/transitional names that can still appear in exam-guide wording
- support-level concepts rather than fragile price-table memorization

---

# Practice coverage validation

## `practice/QUESTIONS.md`
50 scored-style original questions with exact domain weighting:
- 12 Domain 1 = 24%
- 15 Domain 2 = 30%
- 17 Domain 3 = 34%
- 6 Domain 4 = 12%

Plus six extra Domain 3 service drills.

## `practice/TARGETED-GAPS-QUESTIONS.md`
30 additional original questions added after this audit to cover underrepresented explicit task-statement details, including:
- IAM policy types
- IAM credential report
- root-only tasks
- Parameter Store vs Secrets Manager
- one-time vs repeatable operations
- Systems Manager / Service Catalog / License Manager / X-Ray / AppStream / AppSync
- RI flexibility and Organizations sharing
- cost allocation tag types
- data transfer
- APN / Marketplace / Health / Trust & Safety

## Score warning
Practice percentages in this repository are readiness heuristics only. They must **not** be interpreted as direct conversions to the AWS scaled 700/1000 passing score.

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

For every topic in the repo, ask:

> Can AWS plausibly test recognition, differentiation, responsibility, use case, cost/support choice, or business value from this concept?

If yes, learn it at foundational level.

If the learning activity is mainly implementation, debugging, coding, tuning, or advanced architecture configuration, postpone it until after CLF-C02.