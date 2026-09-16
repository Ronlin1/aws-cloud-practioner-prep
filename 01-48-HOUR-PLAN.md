# 01 — 48-Hour CLF-C02 Study Plan

You do **not** have time for broad AWS learning. The objective is to build exam recognition quickly, then spend a large fraction of time on questions.

## Strategy

Prioritize by weight:

1. **Domain 3: Technology & Services — 34%**
2. **Domain 2: Security & Compliance — 30%**
3. **Domain 1: Cloud Concepts — 24%**
4. **Domain 4: Billing/Pricing/Support — 12%**

That means 64% of scored content comes from Domains 2 and 3.

## Day 1 — Build the map

### Block 1 — 60–90 min: Blueprint + cloud concepts
Read:
- `00-EXAM-BLUEPRINT.md`
- `02-DOMAIN-1-CLOUD-CONCEPTS.md`

Master:
- scalability vs elasticity
- high availability vs fault tolerance vs DR
- Regions vs AZs vs edge locations
- Well-Architected six pillars
- CAF six perspectives
- fixed vs variable costs
- rightsizing, economies of scale, automation

### Block 2 — 2.5–3 h: Security
Read:
- `03-DOMAIN-2-SECURITY-COMPLIANCE.md`
- security comparisons in `07-CONFUSING-SERVICES-EXAM-TRAPS.md`

Master first:
- Shared Responsibility: EC2 vs RDS vs Lambda
- IAM user/group/role/policy
- least privilege, MFA, root user
- CloudWatch vs CloudTrail vs Config
- GuardDuty vs Inspector vs Macie vs Security Hub vs Detective
- WAF vs Shield
- KMS vs CloudHSM vs Secrets Manager vs ACM
- Artifact and compliance

### Block 3 — 3–4 h: Core services
Read the core half of `04-DOMAIN-3-TECHNOLOGY-SERVICES.md`.

Master:
- EC2, Lambda, ECS, EKS, Fargate, ECR
- Auto Scaling + ELB
- S3, EBS, EFS, FSx, Glacier, Backup
- RDS, Aurora, DynamoDB, ElastiCache, Redshift
- VPC, Route 53, CloudFront, Direct Connect, VPN, API Gateway

### Block 4 — 90 min: Service recognition
Read `06-SERVICE-CHEAT-SHEET.md` twice.

Method:
- Cover the answer column.
- Read the requirement.
- Say the service aloud within 3 seconds.
- If you cannot, mark it weak.

### Block 5 — 45–60 min: Official question set
Take the AWS Official Practice Question Set.

Do NOT merely record score. For every miss, classify it:
- didn't know service
- confused two services
- misread keyword
- pricing/support knowledge gap
- security-responsibility gap

### End of Day 1 target
You should confidently identify the correct service for at least **80% of basic use-case prompts**.

---

# Day 2 — Convert knowledge into exam performance

## Block 1 — 2 h: Finish Domain 3 recognition services
Learn recognition-level use cases for:
- Athena, Glue, EMR, Kinesis, QuickSight, OpenSearch
- SageMaker AI, Comprehend, Kendra, Lex, Polly, Transcribe, Translate, Rekognition, Textract, Amazon Q
- SQS, SNS, EventBridge, Step Functions
- Connect, SES
- CodeBuild, CodePipeline, X-Ray
- WorkSpaces, AppStream, Secure Browser
- Amplify, AppSync, IoT Core
- migration services
- management/governance services

Do not go deep. One-line purpose + contrast is enough for lower-frequency services.

## Block 2 — 75 min: Domain 4
Read `05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`.

Master:
- On-Demand vs Reserved vs Savings Plans vs Spot
- Dedicated Host vs Dedicated Instance vs Capacity Reservation
- Pricing Calculator vs Cost Explorer vs Budgets vs CUR
- Organizations/consolidated billing/tags
- AWS support resources

## Block 3 — 60–90 min: Traps
Read `07-CONFUSING-SERVICES-EXAM-TRAPS.md` until the comparisons are instant.

You should be able to answer without hesitation:
- CloudWatch / CloudTrail / Config
- S3 / EBS / EFS
- RDS / DynamoDB / Redshift / ElastiCache
- SQS / SNS / EventBridge / Step Functions
- GuardDuty / Inspector / Macie / Detective / Security Hub
- WAF / Shield
- Route 53 / CloudFront / Global Accelerator
- Direct Connect / VPN
- IAM / Cognito / IAM Identity Center
- KMS / Secrets Manager / CloudHSM / ACM
- Pricing Calculator / Cost Explorer / Budgets / CUR

## Block 4 — 2–3 h: Timed practice
Take at least one full timed practice exam, preferably two if energy permits.

Target:
- **80% minimum** before being comfortable
- **85%+ preferred**

For every wrong answer, write ONE sentence explaining:
1. why the correct answer is correct, and
2. why your chosen answer is wrong.

This is higher value than doing endless new questions.

## Block 5 — 60 min: Weak-area patching
Only study material tied to your errors.

Examples:
- Missed CAF question -> study CAF only.
- Confused WAF/Shield -> fix that pair only.
- Missed support plan -> review support section only.

Do not restart a 12-hour course.

## Final 2–3 hours before sleep/exam
Read only:
- `08-LAST-MINUTE-CRAM.md`
- `06-SERVICE-CHEAT-SHEET.md`
- `07-CONFUSING-SERVICES-EXAM-TRAPS.md`

Then stop cramming and sleep properly.

---

# Best use of AWS Skill Builder with only 48 hours

## Must do
1. Official Exam Guide
2. Official Practice Question Set (20 questions)
3. CLF-C02 Exam Prep material for weak domains

## Useful if time allows
- Official Practice Exam (subscription)
- selected sections of AWS Cloud Practitioner Essentials

## Do NOT attempt to finish everything merely for completion
AWS Cloud Practitioner Essentials is now a long course. With two days, use it selectively to fill gaps rather than consuming every lesson sequentially.

Official Skill Builder prep hub:
https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

Cloud Practitioner Essentials:
https://explore.skillbuilder.aws/learn/courses/134/aws-cloud-practitioner-essentials

Official Practice Question Set (link may redirect as Skill Builder evolves):
https://explore.skillbuilder.aws/learn/course/external/view/elearning/14050/aws-certified-cloud-practitioner-official-practice-question-set-clf-c02-english

---

# Practice-test rule

Do not memorize answer letters.

For each question, extract the trigger:

> “SQL query directly over files in S3” -> **Athena**

> “Who deleted the bucket?” -> **CloudTrail**

> “Alert at $500 monthly spend” -> **Budgets**

> “Sensitive PII in S3” -> **Macie**

> “Interruptible batch workload” -> **Spot Instances**

This trigger-based recall is the fastest way to improve in 48 hours.

# Exam-day strategy

- Read the final sentence first when a scenario is long.
- Identify the requirement keywords.
- Eliminate services from the wrong category first.
- Watch for **MOST cost-effective**, **LEAST operational overhead**, **high availability**, **serverless**, **managed**, **audit**, **monitor**, **notify**, **queue**, **relational**, **NoSQL**, and **archive**.
- Multiple-response questions: verify every selected option independently.
- Never leave a question unanswered; AWS states there is no penalty for guessing.
- Flag uncertain questions and return later.
