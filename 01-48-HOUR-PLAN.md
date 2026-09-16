# 01 — 48-Hour CLF-C02 Study Plan

You do **not** have time for broad AWS learning. The objective is to build exam recognition quickly, validate gaps with official questions, and spend the remaining time only on weak areas.

## Strategy

Prioritize by official weight:

1. **Domain 3: Technology & Services — 34%**
2. **Domain 2: Security & Compliance — 30%**
3. **Domain 1: Cloud Concepts — 24%**
4. **Domain 4: Billing/Pricing/Support — 12%**

That means **64% of scored content comes from Domains 2 and 3**.

## Before the main study blocks — 30 to 45 min

Use the current AWS prep flow:
1. Skim the official exam guide.
2. Take the **AWS Certification Official Pretest** if available in your Skill Builder account.
3. Record the domains where you are weak.

Do not spend equal time everywhere after this. The point of the pretest is to make the next 48 hours targeted.

Official certification page:
https://aws.amazon.com/certification/certified-cloud-practitioner/

Skill Builder exam prep hub:
https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

---

# Day 1 — Build the exam map

## Block 1 — 60–90 min: Blueprint + cloud concepts
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

## Block 2 — 2.5–3 h: Security
Read:
- `03-DOMAIN-2-SECURITY-COMPLIANCE.md`
- security comparisons in `07-CONFUSING-SERVICES-EXAM-TRAPS.md`

Master first:
- Shared Responsibility: EC2 vs RDS vs Lambda
- IAM user/group/role/policy
- managed vs customer-managed policies at recognition level
- least privilege, MFA, root user
- root-only task examples
- CloudWatch vs CloudTrail vs Config
- GuardDuty vs Inspector vs Macie vs Security Hub vs Detective
- WAF vs Shield
- KMS vs CloudHSM vs Secrets Manager vs ACM
- Artifact and Audit Manager
- Secrets Manager vs Systems Manager Parameter Store at recognition level

## Block 3 — 3–4 h: Core services
Read the core half of `04-DOMAIN-3-TECHNOLOGY-SERVICES.md`.

Master:
- EC2, Lambda, ECS, EKS, Fargate, ECR
- Auto Scaling + ELB
- S3, EBS, EFS, FSx, Glacier, Backup
- RDS, Aurora, DynamoDB, ElastiCache, Redshift
- VPC, Route 53, CloudFront, Direct Connect, VPN, API Gateway

## Block 4 — 90 min: Service recognition
Read `06-SERVICE-CHEAT-SHEET.md` twice.

Method:
- Cover the answer column.
- Read the requirement.
- Say the service aloud within 3 seconds.
- If you cannot, mark it weak.

## Block 5 — 45–60 min: Official question set
Take the **AWS Certification Official Practice Question Set** through the current Cloud Practitioner certification page or Skill Builder exam-prep hub.

AWS currently describes the free Official Practice Question Set as **20 exam-style questions with detailed feedback**.

Do NOT merely record score. For every miss, classify it:
- didn't know service
- confused two services
- misread keyword
- pricing/support knowledge gap
- security-responsibility gap
- framework/migration gap

### End of Day 1 target
You should confidently identify the correct service for at least **80% of basic use-case prompts** and know exactly which task statements remain weak.

---

# Day 2 — Convert knowledge into exam performance

## Block 1 — 90–120 min: Official free Exam Prep course
AWS's current certification-prep page says the free Exam Prep digital course is about **2 hours** and reviews exam topic areas plus sample questions.

Use it as a targeted revision layer, especially for weak domains identified by the pretest/question set.

Official prep page:
https://aws.amazon.com/certification/certification-prep/

Do **not** replace this with the full 12h45m Cloud Practitioner Essentials course unless you truly have time.

## Block 2 — 2 h: Finish Domain 3 recognition services
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

## Block 3 — 75–90 min: Domain 4
Read `05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`.

Master:
- On-Demand vs Reserved vs Savings Plans vs Spot
- Standard vs Convertible RI concept
- Regional vs Zonal RI concept
- Dedicated Host vs Dedicated Instance vs Capacity Reservation
- Pricing Calculator vs Cost Explorer vs Budgets vs CUR
- cost allocation tag types
- Organizations/consolidated billing
- AWS Support resources and current-vs-legacy support terminology
- Trusted Advisor, Health Dashboard/Health API
- APN, Marketplace, Professional Services, Solutions Architects

## Block 4 — 60–90 min: Traps
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

## Block 5 — 2–3 h: Timed practice
Do:
1. `practice/QUESTIONS.md`
2. `practice/TARGETED-GAPS-QUESTIONS.md`
3. If you have Skill Builder subscription access, take the **AWS Certification Official Practice Exam**.

Suggested readiness margin:
- **80%+** repeatedly = reasonable practice performance
- **85%+** = stronger margin

These percentages are **study targets only**, not conversions to AWS's 700/1000 scaled score.

For every wrong answer, write ONE sentence explaining:
1. why the correct answer is correct, and
2. why your chosen answer is wrong.

## Block 6 — 60 min: Weak-area patching
Only study material tied to your errors.

Examples:
- Missed CAF question -> study CAF only.
- Confused WAF/Shield -> fix that pair only.
- Missed support-plan question -> review support section only.
- Missed root-user task -> review the root-user subsection only.

Do not restart a long course.

## Final 2–3 hours before sleep/exam
Read only:
- `08-LAST-MINUTE-CRAM.md`
- `06-SERVICE-CHEAT-SHEET.md`
- `07-CONFUSING-SERVICES-EXAM-TRAPS.md`
- your personal wrong-answer list

Then stop cramming and sleep properly.

---

# AWS Cloud Practitioner Essentials: use selectively

Current AWS Skill Builder listing:
https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7

AWS currently lists the course as **12h45m**, free, Fundamental level, last updated May 15, 2026.

With only two days, use selected sections to repair gaps rather than consuming every lesson sequentially.

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
