# Domain 4 — Billing, Pricing & Support (12%)

This is the smallest domain, but many questions are straightforward if the distinctions are instant.

# 1. EC2 purchasing options

## On-Demand Instances
No long-term usage commitment.

Best for:
- short-term workloads
- unpredictable demand
- new applications
- maximum purchasing flexibility

**Trigger:** “no commitment”, “unpredictable”, “short term”.

## Reserved Instances (RIs)
A Reserved Instance is primarily a **billing discount mechanism** applied to matching EC2 usage; some zonal RIs also reserve capacity.

Best for:
- predictable long-running EC2 usage
- commitment in exchange for discount relative to On-Demand under applicable terms

### Standard vs Convertible RIs
At exam level:
- **Standard RI** -> less configuration exchange flexibility; typically stronger discount potential.
- **Convertible RI** -> can be exchanged for another Convertible RI of equal or greater value with different configuration attributes.

Do not memorize exchange mechanics.

### Regional vs Zonal RIs
This distinction is explicitly examinable.

**Regional RI**
- discount can apply across Availability Zones in the selected Region
- does **not** reserve capacity
- can provide instance-size flexibility for eligible Linux/Unix default-tenancy usage within an instance family

**Zonal RI**
- scoped to one specific Availability Zone
- reserves capacity there
- no AZ flexibility
- no instance-size flexibility

### RIs and AWS Organizations
Under consolidated billing/discount-sharing settings, eligible unused RI discount benefits can be applied across linked accounts in an AWS Organization. The purchasing account is considered first; sharing behavior is controlled by organization billing preferences.

Important distinction:
- **RI discount benefit** can be shared according to billing settings.
- a **zonal RI's capacity reservation itself** is for the owning account, not automatically shared as capacity to other accounts.

## AWS Savings Plans
Commit to a consistent amount of eligible compute usage/spend (USD/hour) for a term and receive discounted pricing.

Best for:
- long-running predictable compute usage
- customers wanting commitment discounts with broader compute flexibility than some RI configurations

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
Instances run on hardware dedicated to one customer, but without the same host-level visibility/control as Dedicated Hosts.

## On-Demand Capacity Reservations
Reserve EC2 capacity for specified attributes, commonly in a specific Availability Zone.

Key exam point:
- reserves/guarantees capacity availability
- does **not by itself provide a pricing discount**
- can still be covered by eligible Savings Plans or Regional RI billing discounts

### Purchasing-option instant map
- flexible/no commitment -> On-Demand
- predictable commitment -> RI or Savings Plans
- interruptible lowest-cost capacity -> Spot
- dedicated physical server/licensing -> Dedicated Host
- dedicated hardware without host-level control -> Dedicated Instance
- guarantee capacity -> Capacity Reservation

---

# 2. Storage pricing concepts

Different storage classes trade cost against access pattern, resilience and retrieval characteristics.

General S3 logic:
- frequent access -> Standard
- changing/unknown access -> Intelligent-Tiering
- infrequent but rapid retrieval -> Standard-IA
- infrequent and one-AZ resilience acceptable -> One Zone-IA
- long-term archive -> Glacier classes

Lifecycle policies can automatically transition or expire objects.

Do not memorize exact per-GB prices.

---

# 3. Data-transfer pricing concepts

Know conceptually:
- data transfer **into** AWS is often free in many common scenarios
- data transfer **out** to the internet is commonly charged
- inter-Region transfer can incur charges
- pricing varies by service/path/Region

Do not assume all AWS network traffic is free.

---

# 4. AWS Pricing Calculator

Use to estimate expected cost for a proposed AWS architecture.

Trigger:
> “Estimate monthly cost before deployment.”

---

# 5. AWS Cost Explorer

Analyze historical/current AWS costs, usage patterns, trends and forecasts.

Trigger:
> “Where did our money go?” / “view cost trend over previous months”.

---

# 6. AWS Budgets

Set budgets and alerts for cost/usage and supported commitment metrics.

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

---

# 9. AWS Organizations + consolidated billing

AWS Organizations can centrally manage multiple accounts.

Know:
- consolidated billing
- organizational units (OUs)
- Service Control Policies (SCPs)
- aggregate cost visibility
- RI/Savings Plans discount-sharing concepts

## SCP reminder
SCP = permission guardrail, not a permission grant.

---

# 10. Cost allocation tags

The exam guide explicitly expects you to understand cost allocation tags and their relation to billing reports.

Two types:

## AWS-generated cost allocation tags
Defined and applied by AWS for supported resources/use cases.

## User-defined cost allocation tags
Tags you create/apply, such as:
- `Project=FarmZenith`
- `Department=DataEngineering`
- `Environment=Production`

Cost allocation tags must be activated for use in supported billing/cost-management reporting.

Trigger:
> “show or allocate costs by project/team/environment”.

Think:
> cost allocation tags + Cost Explorer/CUR/billing tools.

---

# 11. AWS Marketplace

Marketplace for third-party software, data and services.

Exam concepts:
- find/deploy third-party software
- centralized procurement and billing in supported scenarios
- governance/entitlement capabilities
- software/security products from independent software vendors (ISVs)

Trigger:
> “Purchase third-party AWS-compatible software through AWS.”

---

# 12. Official AWS technical resources

Know the role of each.

## AWS Documentation
Official service/product documentation.

## AWS Whitepapers
Architecture, security, economics, frameworks and best-practice material.

## AWS Prescriptive Guidance
Patterns, strategies and guidance for common cloud objectives/migrations.

## AWS Knowledge Center / re:Post Knowledge Center
Curated troubleshooting answers and support knowledge.

## AWS re:Post
AWS community Q&A/knowledge platform.

## AWS Support Center
Create/manage support cases according to support entitlement.

## AWS Trusted Advisor
Best-practice recommendations/checks across areas such as cost optimization, security, performance, resilience and service quotas. Exact checks/features depend on support entitlement.

## AWS Health Dashboard / AWS Health API
Account/resource-relevant AWS events and health information.

## AWS Trust & Safety
Contact/report channel for abuse or misuse involving AWS resources.

---

# 13. AWS people and partner resources

This is explicitly in Domain 4.3.

## AWS Professional Services
AWS experts who help customers execute cloud transformations and complex initiatives.

## AWS Solutions Architects
AWS technical experts who help customers understand and design solutions on AWS.

## AWS Partner Network (APN)
Ecosystem of AWS partners.

Recognize:
- **Independent Software Vendors (ISVs)** -> build/provide software products
- **system integrators / consulting partners** -> help plan, migrate, integrate and implement solutions

Exam trigger:
> “Need an AWS-qualified external consulting or technology partner.”

Think:
> AWS Partner Network.

### Why partners matter
At exam level, benefits include access to specialized expertise, software/solutions, migration/implementation support and industry/workload experience.

---

# 14. AWS Support plans — important 2026 transition

The CLF-C02 Domain 4 task page still names legacy/transitional plans as examples:
- Developer Support
- Business Support
- Enterprise On-Ramp
- Enterprise Support

Current live AWS Support documentation in September 2026 lists:
- **Basic**
- **Business Support+**
- **Enterprise Support**
- **Unified Operations**

AWS states that Developer Support, legacy Business Support and Enterprise On-Ramp will be discontinued **January 1, 2027**.

## What to learn for CLF-C02
Do not spend precious time memorizing every current monthly price or response-time table.

Learn the support-selection principle:
- **Basic** -> included foundational/account/self-service resources
- paid business-level support -> 24/7 technical support and faster response options than Basic, depending on plan
- enterprise-level offerings -> deeper proactive/strategic support and designated expertise such as TAM capabilities depending on current plan

Because AWS is in a transition period and the exam guide still references legacy names, read the answer options carefully. Recognize both old guide terminology and the current live portfolio.

Current Support docs:
https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html

---

# 15. High-value exam scenarios

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

### “RI discount should be usable across AZs in one Region and no capacity reservation is required.”
**Regional RI**

### “Need RI-linked capacity reservation in one specific AZ.”
**Zonal RI**

### “Need to exchange the RI for different configuration later.”
**Convertible RI**

### “Company must guarantee EC2 capacity.”
**Capacity Reservation**

### “Company uses server-bound licensing and needs physical host visibility/control.”
**Dedicated Host**

### “Need AWS best-practice recommendations across cost/security/performance.”
**Trusted Advisor**

### “Need to determine whether an AWS event is affecting account resources.”
**AWS Health Dashboard / AWS Health**

### “Need third-party AWS-compatible software from a vendor.”
**AWS Marketplace**

### “Need an external AWS consulting/technology partner.”
**AWS Partner Network (APN)**

### “Need AWS experts for a transformation engagement.”
**AWS Professional Services**

---

# Domain 4 instant recall

1. No commitment -> **On-Demand**
2. Interruptible lowest-cost -> **Spot**
3. Long predictable commitment -> **RI/Savings Plans**
4. RI exchange flexibility -> **Convertible RI**
5. RI applies across AZs in Region, no capacity reservation -> **Regional RI**
6. RI reserves capacity in specific AZ -> **Zonal RI**
7. Dedicated physical host -> **Dedicated Host**
8. Guarantee EC2 capacity -> **Capacity Reservation**
9. Estimate proposed cost -> **Pricing Calculator**
10. Analyze historical spend -> **Cost Explorer**
11. Spending alert -> **Budgets**
12. Detailed cost data -> **CUR**
13. Group account bills -> **Organizations consolidated billing**
14. Allocate cost to project -> **cost allocation tags**
15. Third-party software -> **Marketplace**
16. Best-practice recommendations -> **Trusted Advisor**
17. AWS account-impacting event -> **Health Dashboard / AWS Health**
18. Community Q&A -> **re:Post**
19. AWS expert consulting/transformation -> **Professional Services**
20. Partner ecosystem -> **APN**
21. Abuse report involving AWS resources -> **AWS Trust & Safety**

# Official references

- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- RI scope/flexibility: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/reserved-instances-scope.html
- RI sharing: https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ri-turn-off.html
- Cost allocation tags: https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html
- Current Support plans: https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html
