# AWS Certified Cloud Practitioner CLF-C02 — 48-Hour Exam Prep

> **Goal:** Pass CLF-C02 in 2 days by studying the exam blueprint, not by trying to become an AWS engineer.

This repository is deliberately **exam-scope-first**. It prioritizes knowledge AWS explicitly tests and removes implementation depth that AWS explicitly says is outside the target candidate's exam tasks.

**Deep validation refresh:** 2026-09-16. See [`11-DEEP-VALIDATION-AUDIT.md`](11-DEEP-VALIDATION-AUDIT.md).

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
| 4. Billing, Pricing & Support | 12% | Medium, relatively direct marks |

**64% of scored content is Domains 2 + 3.** Spend most of your time there.

## What AWS says is outside the target candidate's expected tasks

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
3. [`03-DOMAIN-2-SECURITY-COMPLIANCE.md`](03-DOMAIN-2-SECURITY-COMPLIANCE.md) — 30%
4. [`04-DOMAIN-3-TECHNOLOGY-SERVICES.md`](04-DOMAIN-3-TECHNOLOGY-SERVICES.md) — 34%
5. [`02-DOMAIN-1-CLOUD-CONCEPTS.md`](02-DOMAIN-1-CLOUD-CONCEPTS.md) — 24%
6. [`05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`](05-DOMAIN-4-BILLING-PRICING-SUPPORT.md) — 12%
7. [`06-SERVICE-CHEAT-SHEET.md`](06-SERVICE-CHEAT-SHEET.md) — rapid recognition
8. [`07-CONFUSING-SERVICES-EXAM-TRAPS.md`](07-CONFUSING-SERVICES-EXAM-TRAPS.md)
9. [`practice/QUESTIONS.md`](practice/QUESTIONS.md) — 50-question weighted mock
10. [`practice/TARGETED-GAPS-QUESTIONS.md`](practice/TARGETED-GAPS-QUESTIONS.md) — 30 questions on explicit blueprint gaps
11. [`practice/ANSWERS.md`](practice/ANSWERS.md)
12. [`practice/TARGETED-GAPS-ANSWERS.md`](practice/TARGETED-GAPS-ANSWERS.md)
13. [`08-LAST-MINUTE-CRAM.md`](08-LAST-MINUTE-CRAM.md) — final 2–3 hours
14. [`09-RESOURCES.md`](09-RESOURCES.md) — validated official resources
15. [`10-OUT-OF-SCOPE-SKIP.md`](10-OUT-OF-SCOPE-SKIP.md) — things not worth studying now
16. [`11-DEEP-VALIDATION-AUDIT.md`](11-DEEP-VALIDATION-AUDIT.md) — what was checked and patched

## The one rule for every AWS service

For each service, be able to answer:

1. **What problem does it solve?**
2. **What exam sentence should make me choose it?**
3. **Which service is it commonly confused with?**
4. **What does it NOT do?**

Example:

> **CloudTrail** — records AWS API/account activity.  
> Trigger: “Who changed/deleted this AWS resource?”  
> Confused with: CloudWatch and Config.  
> Not primarily: CPU/performance monitoring.

## 48-hour success target

Before exam time, you should be able to:

- Explain all four official domains without notes.
- Identify the use case for every high-priority in-scope service.
- Instantly solve the comparison pairs in `07-CONFUSING-SERVICES-EXAM-TRAPS.md`.
- Handle explicit task-statement details in `practice/TARGETED-GAPS-QUESTIONS.md`.
- Complete the **AWS Certification Official Practice Question Set**.
- Use the **Official Pretest** to identify weak areas.
- If you have Skill Builder subscription access, take the **Official Practice Exam**.
- Repeatedly score around **80–85%+ on quality practice sets as a study heuristic**, not as an AWS score conversion.

## Current Skill Builder strategy

With only two days:

**Prioritize:**
- official exam guide
- Official Pretest
- Official Practice Question Set
- free Exam Prep digital course
- targeted weak-area refresh
- official practice exam if available

**Do not feel compelled to complete the full Cloud Practitioner Essentials course end-to-end.** AWS currently lists it at about 12h45m; use it selectively for weak topics.

See `09-RESOURCES.md` for validated entry links.

## Source of truth

AWS changes services, learning URLs and support offerings. The source of truth for this repo is the current AWS CLF-C02 exam guide and its official scope pages:

- Official exam page: https://aws.amazon.com/certification/certified-cloud-practitioner/
- Official CLF-C02 exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Technologies/concepts: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Out-of-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
- Skill Builder CLF-C02 exam prep hub: https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

> AWS says the in-scope and out-of-scope lists are **non-exhaustive and subject to change**. The official task statements therefore take priority over memorizing a service list.

---

Last deep validation refresh: **2026-09-16**.
