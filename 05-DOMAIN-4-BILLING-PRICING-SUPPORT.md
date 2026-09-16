# Domain 4 — Billing, Pricing & Support (12%)

Smallest domain, but many questions are straightforward if you know the distinctions.

# 1. EC2 purchasing options

## On-Demand Instances
No long-term usage commitment.

Best for:
- short-term workloads
- unpredictable demand
- new applications
- workloads where flexibility matters more than commitment discounts

**Trigger:** “no commitment”, “unpredictable”, “short term”.

## Reserved Instances (RIs)
Commitment-based pricing for eligible EC2 usage over a term.

Best for:
- predictable long-running workloads
- commitment in exchange for discount relative to On-Demand under applicable terms

Know conceptually that RI attributes/flexibility and billing benefits can interact with AWS Organizations. Do not spend precious time memorizing obscure RI edge cases.

## AWS Savings Plans
Commit to a consistent amount of eligible compute usage/spend (USD/hour) for a term and receive discounted pricing.

Best for:
- long-running predictable compute usage
- customers wanting more flexibility than some traditional reservation models

## Spot Instances
Use spare EC2 capacity at deep discounts, but capacity can be interrupted.

Best for:
- fault-tolerant jobs
- batch jobs
- CI/CD workers
- distributed processing
- workloads that can checkpoint/restart

Bad for:
- critical workload that cannot tolerate interruption

**Trigger:** “lowest-cost compute + interruption tolerant”.

## Dedicated Hosts
Physical EC2 server dedicated to one customer.

Common exam reasons:
- software licensing tied to sockets/cores/physical host
- compliance requiring physical host visibility/control

## Dedicated Instances
Instances run on hardware dedicated to one customer, but with less host-level control/visibility than Dedicated Hosts.

## Capacity Reservations
Reserve EC2 capacity in a specific Availability Zone.

Key exam point:
- guarantees/reserves capacity availability
- does **not by itself imply a pricing discount**

### Purchasing-option instant map
- flexible/no commitment -> On-Demand
- predictable/commitment -> RI or Savings Plans
- interruptible cheapest -> Spot
- dedicated physical server/licensing -> Dedicated Host
- dedicated hardware without host-level control -> Dedicated Instance
- guarantee capacity in an AZ -> Capacity Reservation

---

# 2. Storage pricing concepts

The exam may test that different storage classes trade cost against access pattern/retrieval characteristics.

General S3 logic:
- frequent access -> Standard
- changing/unknown access -> Intelligent-Tiering
- infrequent but rapid retrieval -> Standard-IA
- infrequent and one-AZ resilience acceptable -> One Zone-IA
- long-term archive -> Glacier classes

Lifecycle policies can automatically transition objects between classes or expire them.

Do not memorize exact per-GB prices.

---

# 3. Data transfer pricing concepts

Know conceptually:
- data transfer **into** AWS is often free for many services/scenarios
- data transfer **out** to the internet is commonly charged
- cross-Region transfer can incur charges
- transfer pricing varies by service/path/Region

Do not assume “all network traffic inside AWS is free”.

---

# 4. AWS Pricing Calculator

Use BEFORE deployment/planning to estimate cost.

Trigger:
> “Estimate monthly cost of proposed architecture.”

Answer:
> AWS Pricing Calculator.

---

# 5. AWS Cost Explorer

Analyze historical/current AWS costs and usage patterns/trends and forecasts.

Trigger:
> “Where did our money go?” / “view cost trend over last months”.

---

# 6. AWS Budgets

Set cost/usage/reservation/Savings Plans budgets and alert thresholds.

Trigger:
> “Notify me when monthly AWS spending reaches 80% of $1,000.”

---

# 7. AWS Cost and Usage Report (CUR)

Detailed/granular cost and usage data for deeper billing analysis.

Trigger:
> “most detailed billing/usage dataset”.

---

# 8. Pricing Calculator vs Cost Explorer vs Budgets vs CUR

- **Pricing Calculator** -> estimate future/proposed cost
- **Cost Explorer** -> analyze spend/trends
- **Budgets** -> threshold/alert
- **CUR** -> granular billing dataset

This comparison is highly examinable.

---

# 9. AWS Organizations + consolidated billing

AWS Organizations can centrally manage multiple AWS accounts.

Know:
- consolidated billing
- organizational units (OUs)
- Service Control Policies (SCPs)
- aggregate cost visibility
- some pricing/discount benefits can be shared across eligible linked accounts under AWS billing rules

## SCP reminder
SCP = permission guardrail, not a permission grant.

---

# 10. Cost allocation tags

Tags help categorize spend by attributes such as:
- project
- department
- owner
- environment

Example:
`Project=FarmZenith`
`Environment=Production`

Trigger:
> “show costs by project/team/environment”.

Think:
> cost allocation tags + billing/cost reports.

---

# 11. AWS Marketplace

Marketplace for third-party software, data/services, and AWS-compatible offerings.

Exam concepts:
- find/deploy third-party software
- centralized procurement/billing in supported scenarios
- governance/entitlement/cost-management capabilities
- security products can also be obtained here

---

# 12. AWS Support resources

Know the role of:

## AWS Documentation
Official technical product docs.

## AWS Whitepapers
Architecture, security, economics, frameworks, best-practice material.

## AWS Prescriptive Guidance
Patterns/strategies/guidance for common cloud objectives.

## AWS Knowledge Center / re:Post Knowledge Center
Curated answers/troubleshooting information.

## AWS re:Post
AWS community Q&A/knowledge platform.

## AWS Support Center
Manage AWS Support cases based on support entitlement.

## AWS Professional Services
AWS experts who help customers with transformations/complex projects.

## AWS Solutions Architects
AWS technical experts who help customers understand/design AWS solutions.

## AWS Partner Network (APN)
Ecosystem of consulting and technology partners, including system integrators and software vendors.

## AWS Trust & Safety
Report abuse/misuse of AWS resources.

---

# 13. Trusted Advisor

Provides best-practice checks/recommendations across areas such as:
- cost optimization
- security
- performance
- resilience/fault tolerance
- service quotas

Exact feature availability can depend on support plan.

Trigger:
> “best-practice recommendations for AWS environment”.

---

# 14. AWS Health Dashboard / Health API

Shows AWS events that may affect your account/resources.

Trigger:
> “Is an AWS service event affecting my resources/account?”

Do not confuse:
- CloudWatch -> your workload metrics/logs/alarms
- Health Dashboard -> AWS events affecting resources/account

---

# 15. AWS Support plans — important 2026 note

The CLF-C02 exam guide's Domain 4 text still uses some legacy/transitional plan names as examples, including Developer Support, Business Support, Enterprise On-Ramp, and Enterprise Support.

Current AWS Support documentation in 2026 lists:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

AWS also states that legacy Developer Support, Business Support, and Enterprise On-Ramp are being retired by January 1, 2027, with customers transitioning during 2026.

## What to learn for the exam
Do **not** waste time memorizing old monthly prices and every response-time table.

Learn the principle:
- **Basic** -> included, account/billing/customer service, docs/community/self-service resources
- higher paid support -> more technical support, faster response, more proactive/expert engagement
- Enterprise-style support -> deeper proactive/strategic assistance, TAM-style capabilities depending on current plan

Because the exam guide and live AWS support portfolio are in transition, read any support-plan question carefully and answer from the options/context presented.

Current Support docs:
https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

---

# 16. Exam scenarios

### “We are designing an application and need to estimate monthly AWS cost.”
**Pricing Calculator**

### “Finance wants to see which services cost the most over the last six months.”
**Cost Explorer**

### “Notify us if forecast monthly spend exceeds $5,000.”
**AWS Budgets**

### “Finance needs the most detailed raw cost-and-usage data.”
**Cost and Usage Report**

### “Batch workload can be interrupted and must minimize EC2 cost.”
**Spot Instances**

### “Production workload is predictable for years and can make a commitment.”
**Reserved Instances / Savings Plans**, depending on scenario wording.

### “Company must guarantee that EC2 capacity is available in a particular AZ.”
**Capacity Reservation**

### “Company uses server-bound licensing and needs visibility/control of physical EC2 host.”
**Dedicated Host**

### “Need AWS best-practice recommendations across cost/security/performance.”
**Trusted Advisor**

### “Need to determine whether an AWS event is affecting account resources.”
**AWS Health Dashboard**

---

# Domain 4 instant recall

1. No commitment -> On-Demand
2. Interruptible cheapest -> Spot
3. Long predictable commitment -> RI/Savings Plans
4. Dedicated physical host -> Dedicated Host
5. Guarantee AZ capacity -> Capacity Reservation
6. Estimate proposed cost -> Pricing Calculator
7. Analyze historical spend -> Cost Explorer
8. Spending alert -> Budgets
9. Detailed cost data -> CUR
10. Group account bills -> Organizations consolidated billing
11. Allocate cost to project -> cost allocation tags
12. Third-party software -> Marketplace
13. Best-practice recommendations -> Trusted Advisor
14. AWS account-impacting event -> Health Dashboard
15. Community Q&A -> re:Post
16. AWS expert consulting/transformation -> Professional Services
17. Partner ecosystem -> APN

# Official references

- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- Current Support plans: https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html
- Current Support pricing: https://aws.amazon.com/premiumsupport/pricing/
