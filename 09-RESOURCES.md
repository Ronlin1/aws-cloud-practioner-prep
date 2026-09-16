# 09 — Validated CLF-C02 Resources

Use **official AWS resources first**. Community material is supplemental only.

Validation refresh: **2026-09-16**.

# Tier 1 — Must use

## Official AWS Certified Cloud Practitioner page
https://aws.amazon.com/certification/certified-cloud-practitioner/

Why use it:
- current exam format: 65 questions, 90 minutes
- official preparation flow
- links into current AWS Skill Builder exam prep

AWS currently recommends this sequence:
1. Review the exam guide.
2. Take the AWS Certification Official Practice Question Set.
3. Take the Official Pretest to identify gaps.
4. Refresh only the weak topics.
5. Review/practice exam-style questions.
6. Take the full Official Practice Exam if you have subscription access.

## Official CLF-C02 Exam Guide
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html

This is the primary source of truth for:
- domains and weights
- task statements
- target candidate
- scored/unscored question counts
- out-of-scope job tasks

## Official Domain pages
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html

## Official in-scope service list
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html

## Official out-of-scope service list
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html

## Official technologies and concepts list
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html

---

# Tier 2 — AWS Skill Builder

## CLF-C02 Exam Prep hub
https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

Use this as the safest entry point because individual Skill Builder course URLs can be changed or retired.

## Free Exam Prep course
AWS's certification-prep page states that the free Exam Prep digital courses are about **2 hours** and cover the exam domains plus sample certification questions.

Official prep overview:
https://aws.amazon.com/certification/certification-prep/

With only two days, this short exam-prep course is a higher-priority use of time than completing a long general fundamentals course end-to-end.

## AWS Cloud Practitioner Essentials
Current Skill Builder course:
https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7

AWS currently lists it as:
- **12h 45m**
- free
- Fundamental level
- last updated **May 15, 2026**

It is good foundational training, but with 48 hours remaining use only selected weak-topic sections unless you genuinely have time for the full course.

## Official Practice Question Set
AWS states the free Official Practice Question Sets contain **20 exam-style questions**, with detailed feedback and recommended resources.

Do **not** rely on old bookmarked direct course IDs. The previously common direct CLF-C02 question-set URL now redirects to Skill Builder search. Open the current Cloud Practitioner certification page or Exam Prep hub and choose **AWS Certification Official Practice Question Set** from there.

Certification page:
https://aws.amazon.com/certification/certified-cloud-practitioner/

Exam prep hub:
https://skillbuilder.aws/category/exam-prep/cloud-practitioner-foundational-CLF-C02

## Official Pretest
The current AWS Cloud Practitioner certification page explicitly recommends the **AWS Certification Official Pretest** to identify areas that need refresh.

Use it early in the 48-hour sprint so you spend time only on weak domains.

## Official Practice Exam
Available with AWS Skill Builder subscription. AWS says its official practice exams use exam-style rigor and scoring and provide feedback.

---

# Tier 3 — Official framework, IAM, cost and support references

## AWS Cloud Adoption Framework
https://aws.amazon.com/cloud-adoption-framework/

Memorize six perspectives:
Business, People, Governance, Platform, Security, Operations.

## AWS Well-Architected Framework
https://docs.aws.amazon.com/wellarchitected/latest/framework/the-pillars-of-the-framework.html

Memorize six pillars:
Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability.

## AWS root user tasks
https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

The exam guide explicitly expects you to identify tasks that only the root user can perform. Do not memorize the entire long list, but know common examples in `03-DOMAIN-2-SECURITY-COMPLIANCE.md`.

## AWS cost allocation tags
https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html

Know the two types:
- AWS-generated
- user-defined

## EC2 Reserved Instance flexibility
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/reserved-instances-scope.html

Know at exam level:
- Regional RI: AZ flexibility; no capacity reservation.
- Zonal RI: reserves capacity in a specific AZ.
- Regional RI instance-size flexibility exists for eligible Linux/Unix default-tenancy use cases.

## AWS Support plans — CURRENT 2026
https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

Current portfolio:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

The CLF-C02 Domain 4 page still names legacy/transitional options such as Developer Support, Business Support, and Enterprise On-Ramp as examples. Those plans are scheduled for retirement on **January 1, 2027**, so you must recognize both the exam-guide terminology and the current portfolio.

---

# Tier 4 — Community resources reviewed for supplemental practice

These are **not authoritative**. Cross-check facts against AWS.

## Tutorials Dojo / Jon Bonso CLF-C02 repository
https://github.com/jsbonso/aws-certified-cloud-practitioner-clf-c02

Useful for topic/resource organization. Note that parts of its README reflect older versions of the CLF-C02 guide, so do not use it as the current scope authority.

## Sudhirtmg CLF-C02 study notes
https://github.com/Sudhirtmg/aws-clf-c02-study-notes

Beginner-oriented notes and practice structure; verify every scope-sensitive claim against AWS.

## AnuragAnalog resource aggregation
https://github.com/AnuragAnalog/AWSCCPResources

Useful for discovering learning resources, not for defining current exam scope.

---

# Recent 2026 community signal — use cautiously

Recent r/AWSCertifications pass reports from August–September 2026 repeatedly emphasize:
- service-to-use-case recognition
- careful reading of plausible distractors
- repeated practice tests
- CAF / Well-Architected review
- 80%+ practice performance as a common personal readiness target

These are **anecdotes**, not AWS rules. They support the strategy in this repo but do not define exam content.

---

# What to skip with only 48 hours

Do not spend significant time on:
- Kubernetes administration
- production IaC coding
- advanced IAM JSON syntax
- deep VPC routing labs
- CLI command memorization
- detailed database tuning
- exact per-GB storage prices
- obscure service internals

AWS explicitly says coding, architecture design, troubleshooting, implementation, and load/performance testing are outside the CLF-C02 target candidate's expected job tasks.
