# Validation Notes

## Latest full validation

**Date:** 2026-09-26

This repository was rechecked against current official AWS and Pearson VUE sources after the public exam-experience material was added.

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

Other explicitly listed services rechecked include AWS AppSync, Amazon API Gateway, AWS Fargate, AWS Audit Manager, AWS IAM Identity Center, AWS Secrets Manager, AWS Security Hub, and current management/governance services.

### Out-of-scope service list
The current official out-of-scope page was rechecked so the repository does not tell learners to deep-study explicitly excluded services.

### AWS Skill Builder / Certification Prep
Current AWS Certification Prep guidance distinguishes free and subscription resources.

Free resources currently include:
- AWS Certification Official Practice Question Sets — 20 questions
- Exam Prep digital courses — about 2 hours
- selected Cloud Quest content

Subscription resources currently include:
- AWS Certification Official Practice Exams
- enhanced Exam Prep content with additional practice questions/labs
- additional Cloud Quest content

The repository now states this distinction explicitly instead of implying every official preparation resource is free.

### EC2 purchasing options
Current EC2 documentation now distinguishes:
- **immediate-use Capacity Reservations** — no term commitment
- **future-dated Capacity Reservations** — include a commitment duration after delivery

The practice explanation and Domain 4 comparisons were updated accordingly. Capacity Reservations still do not inherently provide a billing discount.

### AWS Support transition
Current live AWS Support documentation lists:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

AWS states Developer Support, legacy Business Support and Enterprise On-Ramp will be discontinued January 1, 2027.

The notes preserve both current live terminology and recognition of legacy/transitional terminology still visible in CLF-C02 material.

### Modern AWS AI
Amazon Bedrock and AgentCore remain separated from CLF-C02 exam scope.

Important finding:
- Amazon Bedrock is useful modern AWS GenAI knowledge but is **not currently listed as a CLF-C02 in-scope service**.
- Amazon Bedrock Agents is now **Agents Classic**.
- AWS says Agents Classic is no longer open to new customers from July 30, 2026 and recommends Amazon Bedrock AgentCore for new agentic workloads.

That material remains in `MODERN-AWS-AI.md` as supplemental learning.

### Practice bank
The practice bank was rechecked for:
- exact 50-question domain weighting
- answer-key correctness
- ambiguity
- targeted-gap breadth
- current terminology

The targeted-gap drill contains **40 questions**. Older references saying 30 were corrected.

### Pearson VUE online testing guidance
The AWS OnVUE requirements were rechecked.

Current published requirements include:
- begin check-in 30 minutes before the appointment
- one display only
- working webcam, microphone and speaker; no headphones/headsets
- at least 6 Mbps download and 2 Mbps upload
- use the same device and network for the system test and exam
- no VPNs, corporate networks, or public/shared networks
- remain alone in the room
- accepted government-issued photo ID must match the booking name
- phone access only when explicitly permitted by a proctor

Pearson currently states that in-exam proctors cannot formally pause or extend an exam. Public experience wording was updated to describe the observed webcam event as a temporary **testing-session interruption** rather than claiming a formal timer pause.

## Community-resource freshness

Community resources are not treated as exam authorities.

The current review found:
- the Tutorials Dojo/Jon Bonso GitHub CLF-C02 repo contains some older scope/service wording
- the AWSCCPResources aggregation contains older Skill Builder links and expired promotions
- the Sudhirtmg study repo is useful but incomplete as a full curriculum

`COMMUNITY-RESOURCES.md` now labels these by freshness and warns readers to use current AWS documentation for scope decisions.

## Privacy validation

The current public branch was checked for:
- personal names and known personal projects
- employer/school/location references
- personal email/phone patterns
- candidate/registration/order IDs
- appointment/launch-token material
- AWS access-key/private-key patterns and obvious credential markers
- unfinished placeholders

No current-branch secret or sensitive exam PII was identified during the 2026-09-26 validation.

Important limitation:
- Git history can preserve removed text and public commit-author metadata.
- Known older commits still contain previously removed personal-project examples.
- No destructive history rewrite was performed as part of this validation.

See `../DISCLAIMER.md`.

## Validation methodology

For scope-sensitive claims, this repository uses this order:

1. current CLF-C02 Exam Guide
2. current Domain 1–4 pages
3. current Technologies and Concepts page
4. current In-Scope / Out-of-Scope pages
5. current AWS service documentation
6. AWS Skill Builder / Certification Prep
7. Pearson VUE AWS OnVUE rules for online-testing guidance
8. community material only as supplementary evidence

## Important limitations

AWS explicitly says the in-scope and out-of-scope service lists are **non-exhaustive and subject to change**.

This means:
- task statements remain more important than memorizing a static service list
- service lists can change after this repository's validation date
- learners should recheck the official guide if preparing much later than the validation date

## Official sources

- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
- https://aws.amazon.com/certification/certified-cloud-practitioner/
- https://aws.amazon.com/certification/certification-prep/
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html
- https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html
- https://www.pearsonvue.com/us/en/aws/onvue.html

**Validation status:** current branch revalidated on 2026-09-26.
