# Validation Notes

## Latest deep validation

**Date:** 2026-09-17

This repository was rechecked against current official AWS sources before the public refresh.

## What was validated

### Exam structure
Confirmed against the current CLF-C02 guide:
- 65 total questions
- 50 scored
- 15 unscored
- 90 minutes
- multiple choice and multiple response
- 700/1000 scaled passing score
- Domain 1: 24%
- Domain 2: 30%
- Domain 3: 34%
- Domain 4: 12%

### Domain task statements
All four official domain pages were rechecked for explicit knowledge and skill statements.

### In-scope service list
The current official in-scope list was checked category by category.

Important AI/ML entries currently include:
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

Other explicitly listed services rechecked include AWS AppSync, Amazon API Gateway, AWS Fargate, AWS Audit Manager, AWS IAM Identity Center, AWS Secrets Manager, AWS Security Hub, and the current management/governance services.

### Out-of-scope service list
The current official out-of-scope page was rechecked so the repository does not tell learners to deep-study explicitly excluded services.

### AWS Skill Builder / Certification Prep
The current AWS certification page still recommends:
1. exam guide
2. Official Practice Question Set
3. Official Pretest
4. targeted knowledge refresh
5. exam-style review/practice
6. Official Practice Exam where available

### AWS Support transition
The 2026 Support-plan transition remains important because the CLF-C02 Domain 4 wording can contain legacy plan names while current live AWS Support documentation reflects the newer portfolio.

The notes therefore preserve both:
- current live terminology
- recognition of legacy/transitional terminology that remains visible in the exam guide

### Modern AWS AI
Amazon Bedrock and AgentCore were researched separately from CLF-C02.

Important finding:
- Amazon Bedrock is useful modern AWS GenAI knowledge but is **not currently listed as a CLF-C02 in-scope service**.
- Amazon Bedrock Agents is now **Agents Classic**.
- AWS says Agents Classic is no longer open to new customers from July 30, 2026 and recommends Amazon Bedrock AgentCore for new agentic workloads.

That material is therefore kept in `MODERN-AWS-AI.md` as supplemental learning.

## Validation methodology

For scope-sensitive claims, this repository uses this order:

1. current CLF-C02 Exam Guide
2. current Domain 1–4 pages
3. current Technologies and Concepts page
4. current In-Scope / Out-of-Scope pages
5. current AWS service documentation
6. AWS Skill Builder / Certification Prep
7. community material only as supplementary evidence

## Privacy validation

The public refresh also scans the current branch for:
- personal names
- personal projects
- employer/school/location references
- emails
- phone-like strings
- obvious ID-like values
- unfinished `TODO` / `TBD` markers

Generic examples are preferred throughout.

## Important limitations

AWS explicitly says the in-scope and out-of-scope service lists are **non-exhaustive and subject to change**.

This means:
- the task statements remain more important than memorizing a static service list
- a service list can change after this repository's validation date
- learners should recheck the official guide if preparing much later than the validation date

Git history can also preserve content that was removed from the latest branch. See `../DISCLAIMER.md`.

## Official sources

- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
- https://aws.amazon.com/certification/certified-cloud-practitioner/

**Validation status:** current branch content revalidated for the 2026-09-17 public refresh.
