# 09 — Verified CLF-C02 Resources

Use official AWS resources first. Public repos/community reports are supplemental only.

# Tier 1 — Must use

## Official AWS Certified Cloud Practitioner page
https://aws.amazon.com/certification/certified-cloud-practitioner/

Why use it:
- current exam format
- exam duration/cost/languages
- links to AWS's recommended prep flow

## Official CLF-C02 Exam Guide
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html

Why use it:
- source of truth for domains, task statements and weighting
- explicitly states target-candidate scope and out-of-scope job tasks

## Official Domain pages
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html

## Official in-scope service list
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html

## Official out-of-scope service list
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html

---

# Tier 2 — AWS Skill Builder

## CLF-C02 Exam Prep hub
https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

This is the safest current entry point because individual Skill Builder course URLs can change/retire.

## AWS Cloud Practitioner Essentials
https://explore.skillbuilder.aws/learn/courses/134/aws-cloud-practitioner-essentials

Current AWS listing shows this as a long foundational course. With only 48 hours, use it to patch weak areas rather than insisting on finishing every lesson.

## Official Practice Question Set
Common direct course URL:
https://explore.skillbuilder.aws/learn/course/external/view/elearning/14050/aws-certified-cloud-practitioner-official-practice-question-set-clf-c02-english

AWS states its free Official Practice Question Sets contain **20 exam-style questions** with feedback and recommended resources.

## Official Practice Exam
Available through AWS Skill Builder subscription. AWS describes it as full-length, with exam-style rigor/scoring and feedback.

Exam-prep overview:
https://aws.amazon.com/certification/certification-prep/

---

# Tier 3 — Official framework/security references

## AWS Cloud Adoption Framework
https://aws.amazon.com/cloud-adoption-framework/

Memorize six perspectives:
Business, People, Governance, Platform, Security, Operations.

## AWS Well-Architected Framework
https://docs.aws.amazon.com/wellarchitected/latest/framework/the-pillars-of-the-framework.html

Memorize six pillars:
Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability.

## AWS Support plans — CURRENT 2026
https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

## AWS Support pricing — CURRENT 2026
https://aws.amazon.com/premiumsupport/pricing/

Important: current AWS Support portfolio is transitioning during 2026, while CLF-C02 exam-guide examples still mention some older plans. Learn the exam concepts and consult live AWS docs for current product names/features.

---

# Tier 4 — Public GitHub repos reviewed for supplemental structure/practice

These are **not authoritative**. Use them only after the official guide.

## Tutorials Dojo / Jon Bonso CLF-C02 resources repo
https://github.com/jsbonso/aws-certified-cloud-practitioner-clf-c02

Useful because it gathers CLF-C02 resource links including the official AWS question set and practice resources.

## yiannis88 practice-question application
https://github.com/yiannis88/aws-certified-cloud-practitioner-questions_CLF_C02

Contains a large bank of community practice questions. Treat these as practice only, not as actual exam questions or authoritative scope.

## Sudhirtmg CLF-C02 study notes
https://github.com/Sudhirtmg/aws-clf-c02-study-notes

Useful as another beginner-oriented notes structure, but always cross-check facts against current AWS docs.

## Other resource aggregation
https://github.com/AnuragAnalog/AWSCCPResources

Contains links to free/paid CLF-C02 preparation resources.

---

# Community findings from recent 2026 candidate reports

These are anecdotal, not official scope, but useful for prioritization:

- Recent pass reports repeatedly emphasize **service-use-case recognition** rather than deep implementation.
- Several candidates report aiming for **80–85%+** on practice exams before sitting the real exam.
- Recent reports also mention the **Well-Architected Framework and AWS CAF** as areas worth revising carefully.
- Practice-question exposure is repeatedly described as useful because AWS distractors can be plausible.

Relevant discussion searches can be found in r/AWSCertifications. Do not treat remembered/reported questions as guaranteed exam content.

---

# Optional third-party practice

If you already have access, Tutorials Dojo and well-maintained CLF-C02 practice sets are commonly recommended by learners. With only 48 hours, prioritize **quality explanations** over the sheer number of questions.

Do not use dumps or material claiming to contain stolen/current exam questions. Besides ethics and certification rules, dumps are often outdated and teach memorization instead of scenario reasoning.

---

# What to skip with only 48 hours

Do not spend significant time on:
- AWS labs purely for hands-on completion
- configuring Kubernetes
- writing production IaC
- deep IAM JSON syntax
- advanced VPC routing
- CLI command memorization
- detailed database tuning
- exact S3 per-GB prices
- obscure service internals

Those can be useful for real AWS skills later, but AWS explicitly says coding, architecture design, troubleshooting, implementation, and performance testing are outside the CLF-C02 target candidate's expected tasks.
