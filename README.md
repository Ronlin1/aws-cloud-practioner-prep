<div align="center">

# ☁️ AWS Certified Cloud Practitioner — CLF-C02 Prep

### A focused, modern, exam-first study repository built for clarity, speed, and confidence.

`CLF-C02` · `65 Questions` · `90 Minutes` · `4 Domains` · `Validated 2026-09-18`

</div>

---

## Why this repository exists

AWS is broad. The Cloud Practitioner exam is not.

This repository is designed to help learners focus on **what CLF-C02 actually tests**, recognize AWS services quickly, avoid common exam traps, and use official AWS resources without getting lost in unnecessary implementation detail.

Whether you have **48 hours** or several weeks, the goal is the same:

> Learn the exam blueprint, understand the core AWS ideas, practice scenario recognition, and spend your time where it matters most.

This is an independently maintained community study resource. It is **not affiliated with, endorsed by, or sponsored by Amazon Web Services (AWS)**.

---

## 🚀 Start here

| Your situation | Recommended path |
|---|---|
| **Exam in 48 hours** | Start with [`01-48-HOUR-PLAN.md`](01-48-HOUR-PLAN.md), then focus heavily on Domains 2 and 3 |
| **A few days to a few weeks** | Follow the domain files in order, then drill comparisons and practice questions |
| **Already studied AWS** | Use [`06-SERVICE-CHEAT-SHEET.md`](06-SERVICE-CHEAT-SHEET.md), [`07-CONFUSING-SERVICES-EXAM-TRAPS.md`](07-CONFUSING-SERVICES-EXAM-TRAPS.md), and the practice sets |
| **Want official links only** | Go straight to [`resources/`](resources/README.md) |
| **Want modern AWS AI/GenAI too** | Read [`resources/MODERN-AWS-AI.md`](resources/MODERN-AWS-AI.md) after the exam-focused material |

---

## 🧭 Exam snapshot

| Domain | Weight | Study priority |
|---|---:|---|
| **1. Cloud Concepts** | **24%** | High |
| **2. Security & Compliance** | **30%** | Very High |
| **3. Cloud Technology & Services** | **34%** | Very High |
| **4. Billing, Pricing & Support** | **12%** | Medium |

**Domains 2 + 3 = 64% of scored content.**

Current official format:

- **65 total questions**
- **50 scored + 15 unscored**
- **90 minutes**
- Multiple choice and multiple response
- Passing score: **700/1000 scaled**
- No penalty for guessing; unanswered questions are incorrect

> Practice percentages in this repository are **study-readiness heuristics only**. They are not conversions to AWS's scaled score.

---

## 📚 Repository map

### 1. Learn

- [`00-EXAM-BLUEPRINT.md`](00-EXAM-BLUEPRINT.md) — official blueprint translated into what to know
- [`02-DOMAIN-1-CLOUD-CONCEPTS.md`](02-DOMAIN-1-CLOUD-CONCEPTS.md) — cloud value, Well-Architected, CAF, migration, economics
- [`03-DOMAIN-2-SECURITY-COMPLIANCE.md`](03-DOMAIN-2-SECURITY-COMPLIANCE.md) — shared responsibility, IAM, security, compliance
- [`04-DOMAIN-3-TECHNOLOGY-SERVICES.md`](04-DOMAIN-3-TECHNOLOGY-SERVICES.md) — compute, storage, databases, networking, analytics, AI/ML, integration
- [`05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`](05-DOMAIN-4-BILLING-PRICING-SUPPORT.md) — pricing, cost tools, Organizations, Support, partner resources

### 2. Drill

- [`06-SERVICE-CHEAT-SHEET.md`](06-SERVICE-CHEAT-SHEET.md) — rapid service recognition
- [`07-CONFUSING-SERVICES-EXAM-TRAPS.md`](07-CONFUSING-SERVICES-EXAM-TRAPS.md) — high-value comparison pairs
- [`08-LAST-MINUTE-CRAM.md`](08-LAST-MINUTE-CRAM.md) — condensed final review

### 3. Practice

- [`practice/QUESTIONS.md`](practice/QUESTIONS.md) — 50-question mock weighted exactly to the official domains
- [`practice/ANSWERS.md`](practice/ANSWERS.md) — validated explanations and mistake diagnosis
- [`practice/TARGETED-GAPS-QUESTIONS.md`](practice/TARGETED-GAPS-QUESTIONS.md) — 40 questions on easy-to-miss and underrepresented blueprint details
- [`practice/TARGETED-GAPS-ANSWERS.md`](practice/TARGETED-GAPS-ANSWERS.md) — validated explanations for the targeted drill
- [`practice/VALIDATION-AUDIT.md`](practice/VALIDATION-AUDIT.md) — deep audit of weighting, answer keys, ambiguity, coverage and current AWS terminology

### 4. Validate

- [`10-OUT-OF-SCOPE-SKIP.md`](10-OUT-OF-SCOPE-SKIP.md) — material not worth deep study for CLF-C02
- [`11-DEEP-VALIDATION-AUDIT.md`](11-DEEP-VALIDATION-AUDIT.md) — what was checked against current AWS sources
- [`resources/VALIDATION-NOTES.md`](resources/VALIDATION-NOTES.md) — latest validation notes and methodology

### 5. Go deeper

- [`resources/OFFICIAL-AWS.md`](resources/OFFICIAL-AWS.md) — official AWS source links
- [`resources/SKILL-BUILDER.md`](resources/SKILL-BUILDER.md) — current AWS learning and exam-prep entry points
- [`resources/MODERN-AWS-AI.md`](resources/MODERN-AWS-AI.md) — current AI/GenAI services, clearly separated from CLF-C02 scope
- [`resources/COMMUNITY-RESOURCES.md`](resources/COMMUNITY-RESOURCES.md) — vetted supplemental community material

---

## 🧠 The one rule for every AWS service

For every service, be able to answer four things:

1. **What problem does it solve?**
2. **What exam phrase should make me choose it?**
3. **What is it commonly confused with?**
4. **What does it not primarily do?**

Example:

> **CloudTrail**  
> **Does:** records AWS API and account activity  
> **Trigger:** “Who changed or deleted this AWS resource?”  
> **Confused with:** CloudWatch and Config  
> **Not primarily for:** CPU/performance monitoring

That pattern is much more useful than memorizing long service descriptions.

---

## 🎯 What this repository intentionally does not do

AWS explicitly says the CLF-C02 target candidate is not expected to perform deep:

- coding
- cloud architecture design
- troubleshooting
- implementation
- load/performance testing

So this repository does **not** spend your study time on advanced CLI syntax, Kubernetes administration, deep VPC routing labs, production IaC, database tuning, or long implementation walkthroughs unless they directly support an exam concept.

Those are valuable real-world skills, but they are not the fastest route to CLF-C02 readiness.

---

## 🤖 Modern AWS AI without exam-scope confusion

AWS evolves quickly. This repository separates **current AWS technology** from **current CLF-C02 requirements**.

The current explicit CLF-C02 Machine Learning list includes services such as:

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

Modern topics such as **Amazon Bedrock, foundation models, RAG, Bedrock Knowledge Bases, Bedrock Guardrails, and Amazon Bedrock AgentCore** are useful AWS knowledge, but they are kept in [`resources/MODERN-AWS-AI.md`](resources/MODERN-AWS-AI.md) and are **not presented as CLF-C02 requirements** unless AWS adds them to the official scope.

---

## 🔐 Privacy and public-repo policy

This repository is intended to be safe to share publicly.

- Examples are generic rather than tied to a person, employer, school, or private project.
- No exam dumps or leaked questions are accepted.
- Corrections should cite official AWS documentation wherever possible.
- Historical Git commits can preserve old text even after the latest branch is cleaned; see [`DISCLAIMER.md`](DISCLAIMER.md) for that limitation.

---

## ✅ Source-of-truth hierarchy

When sources disagree, use this order:

1. Official CLF-C02 Exam Guide
2. Official Domain 1–4 task statements
3. Official Technologies and Concepts page
4. Official In-Scope / Out-of-Scope service lists
5. Current AWS service documentation
6. AWS Skill Builder / Certification Prep
7. Community material only as supplemental guidance

The AWS in-scope and out-of-scope lists are explicitly **non-exhaustive and subject to change**, so the current task statements remain the most important reference.

See [`resources/OFFICIAL-AWS.md`](resources/OFFICIAL-AWS.md) for the validated links.

---

## 🤝 Contributing

Found a stale AWS service name, broken official link, changed exam scope, or confusing explanation?

Contributions are welcome. Please use [`CONTRIBUTING.md`](CONTRIBUTING.md) and include an official AWS source for scope-sensitive corrections whenever possible.

Do **not** submit exam dumps, memorized live-exam questions, or content presented as leaked/real exam material.

---

## ✨ A note to learners

You do not need to know every AWS service in depth to pass CLF-C02.

You need to understand the cloud fundamentals, recognize the major services, distinguish the common look-alikes, and read scenario wording carefully.

**Learn the map. Drill the distinctions. Practice the scenarios. Then go into the exam calm and prepared.**

---

### Suggested GitHub repository description

> **Exam-first AWS Certified Cloud Practitioner (CLF-C02) prep: concise notes, service cheat sheets, traps, original practice questions, official AWS resources, and modern AI guidance.**

---

**Last deep validation:** 2026-09-18  
**Maintained independently. Not affiliated with Amazon Web Services.**
