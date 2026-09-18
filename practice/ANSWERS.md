# CLF-C02 Mock — Answers & Explanations

Score the first 50 questions only. Bonus questions are extra drills.

**Answer-key validation refresh:** 2026-09-18. The full key was rechecked against the current CLF-C02 blueprint and current AWS documentation. No answer-key reversals were required; wording was tightened where a live AWS distinction could otherwise become ambiguous.

> The 50-question mock matches the official **domain weights**, but it does not attempt to reproduce AWS's unpublished task-statement distribution or exact multiple-response ratio. Use the targeted gap drill after this mock to broaden coverage.

## Study score guide

These are **study targets only**, not AWS score conversions or guarantees:

- **45–50 (90–100%)**: strong practice performance; focus on final review and weak details.
- **42–44 (84–88%)**: good practice range; patch the remaining weak categories.
- **40–41 (80–82%)**: keep drilling confusing-service pairs and explicit blueprint gaps.
- **35–39 (70–78%)**: targeted review is strongly recommended before the exam.
- **Below 35**: revisit weak domains, especially Domains 2 and 3, before more full mocks.

> AWS uses **scaled scoring**. A raw practice percentage does **not** convert directly to the official 700/1000 passing score, and AWS does not publish a simple raw-question percentage required to pass.

---

# Domain 1 — Cloud Concepts

**1. B — Elasticity**  
Elasticity is the dynamic increase and decrease of capacity with demand.

**2. C — Adding additional EC2 instances behind a load balancer**  
Horizontal scaling means scaling out/in by changing the number of resources. Making one instance larger is vertical scaling.

**3. A — Agility**  
Agility is the ability to provision/change resources rapidly and experiment quickly.

**4. B — Reliability**  
Reliability focuses on a workload performing its intended function correctly and recovering from failures.

**5. C — Cost Optimization**  
Rightsizing and eliminating idle resources are classic Cost Optimization concerns.

**6. A — People**  
The CAF People perspective covers skills, culture, leadership, workforce and organizational change.

**7. B — Rehost**  
Rehost is commonly called lift and shift: move the workload with minimal changes.

**8. B — AWS Snow Family**  
Snow devices support large-scale physical/offline data transfer when network transfer is impractical or too slow.

**9. B — Rightsizing**  
Rightsizing means matching the resource size/type to actual workload needs rather than overprovisioning.

**10. B — Provider efficiencies from aggregated demand**  
Economies of scale arise when a large cloud provider aggregates infrastructure demand across many customers.

**11. A and C — Faster provisioning; ability to adjust capacity**  
The cloud does not guarantee zero failures or eliminate all expenditure, and it reduces rather than increases the need to predict peak capacity far in advance.

**12. B — AWS Cloud Adoption Framework**  
AWS CAF structures organizational cloud transformation/readiness. Well-Architected focuses on workload best practices.

---

# Domain 2 — Security & Compliance

**13. B — Customer**  
For EC2, the customer manages and patches the guest operating system. AWS manages the underlying physical infrastructure/hypervisor layer.

**14. B — AWS manages more of the underlying DB platform for RDS**  
RDS is more managed than running a database yourself on EC2. The customer still owns data, access, schema and configuration choices.

**15. C — Assign an IAM role**  
Roles provide temporary credentials and avoid hard-coding long-term access keys in applications.

**16. A — Least privilege**  
Grant only the permissions necessary to complete the task.

**17. B — AWS CloudTrail**  
CloudTrail records AWS API/account activity and is the right place to investigate who performed an API action.

**18. C — Amazon CloudWatch**  
CloudWatch handles metrics, logs, alarms and dashboards. CPU threshold alarms are a classic CloudWatch use case.

**19. A — AWS Config**  
Config records resource configurations/changes and can evaluate resources against rules.

**20. A — AWS Artifact**  
Artifact provides self-service access to AWS compliance reports and certain agreements.

**21. B — AWS Audit Manager**  
Audit Manager helps automate collection and organization of audit evidence.

**22. B — Amazon GuardDuty**  
GuardDuty is the managed threat-detection service.

**23. A — Amazon Inspector**  
Inspector focuses on vulnerability management for supported workloads.

**24. A — Amazon Macie**  
Macie discovers/classifies sensitive data in Amazon S3.

**25. B — AWS Shield**  
Shield provides DDoS protection. WAF filters web requests and common web exploits.

**26. B — AWS WAF**  
WAF evaluates HTTP(S) requests against rules, including patterns associated with attacks such as SQL injection and XSS.

**27. A and C — Enable MFA; avoid routine root use**  
Do not share root credentials or create root access keys for applications.

---

# Domain 3 — Cloud Technology & Services

**28. B — Amazon EC2**  
EC2 provides virtual servers with operating-system-level control.

**29. A — AWS Lambda**  
Lambda runs event-driven code without the customer provisioning/managing servers.

**30. B — Amazon EKS**  
EKS is managed Kubernetes. ECS is AWS-native container orchestration.

**31. A — Amazon ECR**  
ECR stores container images.

**32. A — AWS Fargate**  
Fargate is serverless compute for containers used with services such as ECS/EKS.

**33. C — Amazon S3**  
S3 is highly durable object storage and is appropriate for images, documents, logs, backups and data-lake objects.

**34. A — Amazon EFS**  
EFS is a shared managed file system that can be mounted by multiple compatible compute instances.

**35. A — Amazon EBS**  
EBS provides persistent block-storage volumes for EC2.

**36. B — Amazon RDS**  
RDS is the managed relational database service.

**37. C — Amazon DynamoDB**  
DynamoDB is a serverless NoSQL key-value/document database.

**38. A — Amazon Redshift**  
Redshift is a cloud data warehouse optimized for analytical workloads.

**39. A — Amazon Neptune**  
Neptune is a graph database for highly connected data/relationships.

**40. B — Amazon Athena**  
Athena provides serverless SQL querying directly over data stored in S3.

**41. A — AWS Glue**  
Glue is the serverless data-integration/ETL service and includes the Glue Data Catalog.

**42. A — Amazon Kinesis**  
Kinesis is associated with real-time streaming data such as clickstreams, logs and telemetry.

**43. B — Amazon Route 53**  
Route 53 is AWS's DNS service.

**44. B — Amazon CloudFront**  
CloudFront is AWS's CDN and uses edge locations to deliver/cache content closer to users. Global Accelerator improves network paths to application endpoints but is not a CDN/content cache.

---

# Domain 4 — Billing, Pricing & Support

**45. B — AWS Pricing Calculator**  
Use Pricing Calculator to estimate the cost of a proposed architecture before deployment.

**46. A — AWS Cost Explorer**  
Cost Explorer analyzes historical/current costs, usage patterns, trends and forecasts.

**47. A — AWS Budgets**  
Budgets tracks cost/usage against thresholds and can send alerts.

**48. B — Spot Instances**  
Spot uses spare EC2 capacity at deep discounts, but instances can be interrupted, making it ideal for fault-tolerant batch workloads.

**49. C — On-Demand Capacity Reservation**  
An On-Demand Capacity Reservation reserves EC2 capacity for specified attributes, commonly in a specific Availability Zone, without requiring a term commitment. It is primarily a capacity-availability mechanism and does not by itself provide a pricing discount. A Zonal Reserved Instance can also reserve capacity, which is why the question explicitly rules out a long-term pricing commitment.

**50. A — Dedicated Host**  
Dedicated Hosts provide a physical server dedicated to the customer with host visibility/control useful for certain socket/core/server-bound licensing requirements.

---

# Bonus Domain 3 drill

**B1. A — AWS Direct Connect**  
Dedicated network connection from customer premises/network to AWS. A VPN is an encrypted tunnel rather than the dedicated circuit itself.

**B2. A and C**  
Security groups are stateful; network ACLs are stateless and apply at the subnet level.

**B3. B — Amazon SQS**  
SQS is a message queue that buffers/decouples producers and consumers.

**B4. B — Amazon SNS**  
SNS is publish/subscribe and commonly used for fan-out to multiple subscribers/endpoints.

**B5. B — Amazon Transcribe**  
Transcribe converts speech to text. Polly does the reverse: text to speech.

**B6. B — Amazon Textract**  
Textract extracts text, forms and tables from documents. Rekognition analyzes images/video more generally.

---

# Diagnose mistakes by category

When you miss a question, tag it with one of these labels:

- `CONCEPT` — cloud benefit/framework misunderstanding
- `SECURITY-SERVICE` — confused GuardDuty/Inspector/Macie/etc.
- `IAM` — identity/role/policy/shared-responsibility issue
- `COMPUTE`
- `STORAGE`
- `DATABASE`
- `NETWORK`
- `ANALYTICS-AI`
- `INTEGRATION`
- `COST`
- `READING` — knew it but misread keywords

Then study only the corresponding section in the repo. After this mock, also do `TARGETED-GAPS-QUESTIONS.md`, because it covers explicit task-statement details that cannot all fit into one 50-question weighted mock.

## Official validation references

- CLF-C02 exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
