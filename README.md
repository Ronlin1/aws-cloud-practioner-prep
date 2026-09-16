# AWS Certified Cloud Practitioner CLF-C02 — 48-Hour Exam Prep

> **Goal:** Pass CLF-C02 in 2 days by studying the exam blueprint, not by trying to become an AWS engineer.

This repository is deliberately **exam-scope-first**. It prioritizes the knowledge AWS explicitly tests and removes implementation depth that AWS explicitly says is outside the target candidate's exam tasks.

## Exam facts

- Exam: **AWS Certified Cloud Practitioner (CLF-C02)**
- Level: Foundational
- Duration: **90 minutes**
- Questions: **65 total**
- Scored questions: **50**
- Unscored questions: **15** (not identified)
- Formats: multiple choice + multiple response
- Passing score: **700 / 1000 scaled**
- Unanswered questions count as incorrect; there is no penalty for guessing.

## Current official weighting

| Domain | Weight | 48-hour priority |
|---|---:|---|
| 1. Cloud Concepts | 24% | High |
| 2. Security & Compliance | 30% | **Very High** |
| 3. Cloud Technology & Services | 34% | **Very High** |
| 4. Billing, Pricing & Support | 12% | Medium, easy marks |

**64% of scored content is Domains 2 + 3.** Spend most of your time there.

## What AWS says is OUT of the target candidate's exam tasks

Do **not** spend these 48 hours learning deep implementation:

- Coding
- Designing cloud architectures
- Troubleshooting
- Implementation
- Load and performance testing

You need to know **what a service/concept is, why it exists, when to choose it, and what it is confused with**.

## Read in this order

1. [`00-EXAM-BLUEPRINT.md`](00-EXAM-BLUEPRINT.md) — exactly what AWS says can be tested
2. [`01-48-HOUR-PLAN.md`](01-48-HOUR-PLAN.md) — what to do between now and exam time
3. [`02-DOMAIN-1-CLOUD-CONCEPTS.md`](02-DOMAIN-1-CLOUD-CONCEPTS.md)
4. [`03-DOMAIN-2-SECURITY-COMPLIANCE.md`](03-DOMAIN-2-SECURITY-COMPLIANCE.md)
5. [`04-DOMAIN-3-TECHNOLOGY-SERVICES.md`](04-DOMAIN-3-TECHNOLOGY-SERVICES.md)
6. [`05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`](05-DOMAIN-4-BILLING-PRICING-SUPPORT.md)
7. [`06-SERVICE-CHEAT-SHEET.md`](06-SERVICE-CHEAT-SHEET.md) — rapid service recognition
8. [`07-CONFUSING-SERVICES-EXAM-TRAPS.md`](07-CONFUSING-SERVICES-EXAM-TRAPS.md)
9. [`08-LAST-MINUTE-CRAM.md`](08-LAST-MINUTE-CRAM.md) — final 2–3 hours
10. [`09-RESOURCES.md`](09-RESOURCES.md) — official Skill Builder + practice resources
11. [`10-OUT-OF-SCOPE-SKIP.md`](10-OUT-OF-SCOPE-SKIP.md) — things not worth studying now
12. [`practice/QUESTIONS.md`](practice/QUESTIONS.md) — exam-style practice
13. [`practice/ANSWERS.md`](practice/ANSWERS.md) — explanations

## The one rule for every AWS service

For each service, be able to answer:

1. **What problem does it solve?**
2. **What exam sentence should make me choose it?**
3. **Which service is it commonly confused with?**
4. **What does it NOT do?**

Example:

> **CloudTrail** — records AWS API/account activity.  
> Trigger: “Who changed/deleted this AWS resource?”  
> Confused with: CloudWatch.  
> Not primarily: CPU/performance monitoring.

## 48-hour success target

Before exam time, you should be able to:

- Explain all four official domains without notes.
- Identify the use case for every high-priority in-scope service.
- Instantly solve the comparison pairs in `07-CONFUSING-SERVICES-EXAM-TRAPS.md`.
- Score **80–85%+ repeatedly** on good CLF-C02 practice sets.
- Complete the **AWS Official Practice Question Set**.
- If you have Skill Builder subscription access, take the **Official Practice Exam**.

## Source of truth

AWS changes services and support offerings. The source of truth for this repo is the current AWS CLF-C02 exam guide and its in-scope/out-of-scope lists:

- Official exam page: https://aws.amazon.com/certification/certified-cloud-practitioner/
- Official CLF-C02 exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Out-of-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
- Skill Builder CLF-C02 exam prep hub: https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

> AWS says the in-scope and out-of-scope lists are **non-exhaustive and subject to change**. This repo therefore focuses on the official task statements first, then service recognition.

---

Last research refresh: **2026-09-16**.
