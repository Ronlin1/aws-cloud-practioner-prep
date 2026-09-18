# Practice Bank Deep Validation Audit — CLF-C02

**Validation date:** 2026-09-18  
**Scope:** `practice/QUESTIONS.md`, `practice/ANSWERS.md`, `practice/TARGETED-GAPS-QUESTIONS.md`, and `practice/TARGETED-GAPS-ANSWERS.md`

This audit checks the practice section for **blueprint alignment, factual accuracy, answer-key correctness, ambiguity, current AWS terminology, exam-style structure, coverage gaps, and exam-integrity risk**.

---

## Executive result

The practice bank is aligned with the current AWS Certified Cloud Practitioner **CLF-C02** exam guide after the 2026-09-18 refresh.

The original 50-question mock had correct top-level domain weighting and a correct answer key, but its **subdomain distribution was uneven**:

- Domain 3 leaned heavily toward compute, storage, databases, and analytics.
- Domain 4's six scored-style questions leaned heavily toward pricing/cost tools.
- Important explicit blueprint areas were mostly left to notes rather than practice.

The solution was **not** to distort the official 50-question domain weighting. Instead, the targeted drill was expanded from **30 to 40 questions** to close the underrepresented task-statement gaps.

---

# 1. Official exam format validation

Current AWS exam-guide facts:

- **65 total questions**
- **50 scored questions**
- **15 unscored questions**
- **90 minutes**
- question types: **multiple choice** and **multiple response**
- multiple choice: one correct response and three distractors
- multiple response: two or more correct responses from five or more options
- unanswered questions count as incorrect
- no penalty for guessing

Official exam guide:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html

### Mock timing

The repository suggests **70 minutes for 50 questions**.

A proportional equivalent of the official timing is:

`90 minutes × 50 / 65 ≈ 69.2 minutes`

So 70 minutes is a reasonable timed-practice target.

### Important limitation

AWS does **not** publish:

- the exact ratio of multiple-choice to multiple-response questions
- the exact number of questions from each individual task statement
- the raw number of correct answers required to reach the scaled 700/1000 passing score

Therefore the repository does not claim to reproduce those unpublished distributions.

---

# 2. 50-question domain weighting validation

The scored-style mock contains exactly:

| Domain | Questions | Percentage | Official weight |
|---|---:|---:|---:|
| Domain 1 — Cloud Concepts | 12 | 24% | 24% |
| Domain 2 — Security & Compliance | 15 | 30% | 30% |
| Domain 3 — Cloud Technology & Services | 17 | 34% | 34% |
| Domain 4 — Billing, Pricing & Support | 6 | 12% | 12% |
| **Total** | **50** | **100%** | **100%** |

**Result: exact match.**

Official domain pages:
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html

---

# 3. Answer-key audit

Every answer in the 50-question mock and six bonus questions was rechecked.

**Result:** no answer-key reversal was required.

Two questions received wording improvements to reduce possible ambiguity:

### Main mock Question 44

The CloudFront question previously used the distractor wording `AWS Global Accelerator only`.

It was simplified to `AWS Global Accelerator` and the answer explanation now explicitly distinguishes:

- **CloudFront** -> CDN/content caching at edge locations
- **Global Accelerator** -> optimized network path to application endpoints

### Main mock Question 49

A generic capacity-reservation question could overlap conceptually with a **Zonal Reserved Instance**, because a Zonal RI also reserves capacity in one Availability Zone.

The question now explicitly asks for capacity **without requiring a long-term pricing commitment**, making **On-Demand Capacity Reservation** unambiguously correct.

AWS EC2 references:
- Regional vs Zonal RIs: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/reserved-instances-scope.html
- On-Demand Capacity Reservations: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html

---

# 4. Practice coverage audit

## Domain 1

The main mock already gives solid coverage of:

- elasticity and scalability
- agility
- Well-Architected Framework
- AWS Cloud Adoption Framework
- migration strategy recognition
- Snow Family/offline transfer
- rightsizing
- economies of scale
- cloud benefits

**Status: adequate for the domain weight.**

## Domain 2

The main mock covers:

- shared responsibility
- EC2 vs managed-service responsibility
- IAM roles
- least privilege
- CloudTrail / CloudWatch / Config
- Artifact / Audit Manager
- GuardDuty / Inspector / Macie
- Shield / WAF
- root-user protection

The targeted drill adds:

- customer managed vs AWS managed vs inline IAM policies
- IAM credential report
- IAM password policy
- root-only task recognition
- Secrets Manager vs Parameter Store
- federation

**Status: strong combined coverage.**

## Domain 3

The 50-question mock correctly assigns 17 questions to Domain 3, but the original set was disproportionately concentrated in:

- EC2/Lambda/containers
- S3/EBS/EFS
- databases
- Athena/Glue/Kinesis
- Route 53/CloudFront

The targeted drill already covered Systems Manager, Service Catalog, License Manager, X-Ray, AppStream 2.0 and AppSync.

The 2026-09-18 refresh adds direct practice for:

- **Amazon SageMaker AI**
- **Amazon Q**
- **Amazon QuickSight**
- **Amazon EventBridge**
- **AWS Step Functions**
- **AWS Control Tower**
- **Amazon API Gateway**
- **Multi-AZ design**
- **Region-selection factors**

This materially improves Task Statements 3.2, 3.5, 3.7 and 3.8 coverage.

Current Domain 3 task statements explicitly include AI/ML/analytics and other service categories such as EventBridge, SNS, SQS, CodeBuild, CodePipeline, X-Ray, AppStream 2.0, WorkSpaces, Amplify and AppSync.

Official Domain 3:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html

## Domain 4

The main six questions heavily test:

- Pricing Calculator
- Cost Explorer
- Budgets
- Spot
- Capacity Reservations
- Dedicated Hosts

The targeted drill adds the important Domain 4 areas:

- Regional vs Zonal RI flexibility
- RI behavior in AWS Organizations
- cost allocation tags
- transfer pricing concepts
- AWS Partner Network
- AWS Marketplace
- AWS Health
- AWS Trust & Safety
- **AWS Support Center**

This gives much better coverage of Task Statements 4.1, 4.2 and 4.3 as a package.

Official Domain 4:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html

---

# 5. Current AI/ML scope validation

The current explicit CLF-C02 Machine Learning list includes:

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

The practice bank now directly tests **SageMaker AI**, **Amazon Q**, **Transcribe**, and **Textract**, while the study notes cover the broader list.

Current in-scope service list:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html

### Bedrock scope guardrail

Amazon Bedrock is valuable modern AWS knowledge, but it is **not currently present in the explicit CLF-C02 in-scope service list**. It is therefore not treated as a required answer in this CLF-C02 practice bank.

---

# 6. IAM/root-user validation

The exam explicitly expects candidates to:

- understand the importance of protecting the root user
- identify tasks only the account root user can perform
- understand root-user protection methods

The targeted question about **closing a standalone AWS account** remains valid. Current AWS documentation says standalone accounts not managed through AWS Organizations require root credentials to close, while member accounts can be closed centrally in Organizations.

Current root-user guidance:
https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html

---

# 7. Secrets Manager vs Parameter Store validation

The distinction in the targeted drill is current:

### Systems Manager Parameter Store
Best fit for:
- configuration values
- environment names
- endpoint URLs
- resource IDs
- `SecureString` configuration values

### AWS Secrets Manager
Preferred for:
- database credentials
- API keys
- tokens
- secrets requiring automatic rotation and dedicated secret-management controls

AWS Systems Manager currently explicitly recommends Secrets Manager for credentials and secrets that need features such as automatic rotation.

References:
- Parameter Store: https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html
- Secrets Manager rotation: https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html

---

# 8. Reserved Instance validation

Questions 19–23 of the targeted drill were checked against current EC2/Billing documentation.

Validated distinctions:

### Regional RI
- no capacity reservation
- discount can apply across AZs in the selected Region
- eligible Linux/Unix default-tenancy use can receive instance-size flexibility

### Zonal RI
- reserves capacity in a specific AZ
- no AZ flexibility
- no instance-size flexibility
- capacity reservation belongs to the owning account and cannot be shared as capacity across accounts

### AWS Organizations
Current Billing preferences support controlled sharing of RI/Savings Plans **discount benefits** across eligible accounts. The purchasing account is considered first under applicable sharing modes.

References:
- RI scope: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/reserved-instances-scope.html
- RI discount application: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/apply_ri.html
- Discount sharing: https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ri-turn-off.html

---

# 9. AWS Support transition validation

Current live AWS Support plans in September 2026 are:

- Basic
- Business Support+
- Enterprise Support
- Unified Operations

AWS states these legacy plans will be discontinued **January 1, 2027**:

- Developer Support
- legacy Business Support
- Enterprise On-Ramp

However, the current CLF-C02 Domain 4 task page still gives the legacy names as examples. The practice bank therefore avoids fragile exact-price/response-time memorization and focuses on stable support resources and selection concepts.

Current Support docs:
https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

---

# 10. Question-quality audit

## What is good

- all questions are original
- no exam dumps or leaked-question claims
- answer choices generally stay within the same conceptual neighborhood
- multiple-response questions clearly state how many answers to select
- explanations teach the distinction, not only the letter answer
- scenarios focus on foundational service recognition rather than implementation

## What remains intentionally imperfect

A 50-question public mock cannot perfectly reproduce the live exam because AWS does not publish:

- task-statement-level question counts
- exact question-type proportions
- unscored-question identity
- live item difficulty calibration

The repository therefore uses a **two-layer practice model**:

1. **50-question domain-weighted mock** -> pacing and domain-level readiness
2. **40-question targeted gap drill** -> blueprint breadth and easy-to-miss distinctions

For the closest official simulation, use the AWS Certification Official Pretest or Official Practice Exam through AWS Skill Builder.

AWS states that Official Practice Question Sets contain 20 exam-style questions, while Official Pretests and Official Practice Exams are the same length as the certification exam.

Official prep page:
https://aws.amazon.com/certification/certified-cloud-practitioner/

---

# Final validation status

After this audit:

- domain weights: **verified**
- timer: **reasonable and proportional**
- answer keys: **verified**
- obvious ambiguity: **patched**
- current AI/ML services: **validated and strengthened**
- root-user question: **validated**
- Secrets Manager / Parameter Store: **validated**
- Reserved Instance behavior: **validated**
- support-transition risk: **documented**
- major Domain 3/4 practice gaps: **patched through expanded targeted drill**
- exam-dump risk: **none identified**

**Next validation should be triggered whenever AWS changes the CLF-C02 exam guide, in-scope list, or support portfolio.**
