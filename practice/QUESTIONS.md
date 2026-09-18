# CLF-C02 50-Question High-Yield Mock

These are **original practice questions**, not real/dumped AWS exam questions. The 50 scored-style questions mirror the official domain weighting exactly:

- Domain 1: 12 questions = 24%
- Domain 2: 15 questions = 30%
- Domain 3: 17 questions = 34%
- Domain 4: 6 questions = 12%

Suggested time: **70 minutes** for 50 questions. This is approximately proportional to the official 90 minutes for 65 total exam questions.

> **Important:** The domain percentages are exact, but AWS does not publish the exact question mix within each task statement or the ratio of multiple-choice to multiple-response questions. This mock is a study instrument, not a reconstruction of the live exam.

Do not open `ANSWERS.md` until you finish.

**Practice-bank validation refresh:** 2026-09-18. See [`VALIDATION-AUDIT.md`](VALIDATION-AUDIT.md).

---

# Domain 1 — Cloud Concepts (Questions 1–12)

## 1
A retailer automatically increases application capacity during a flash sale and reduces it when traffic returns to normal. Which cloud characteristic is demonstrated?

A. Agility  
B. Elasticity  
C. Durability  
D. Vertical scaling

## 2
Which action is an example of horizontal scaling?

A. Moving from 4 GB to 32 GB RAM on one EC2 instance  
B. Increasing one EBS volume from 100 GB to 1 TB  
C. Adding additional EC2 instances behind a load balancer  
D. Moving a workload to a different Region

## 3
A company wants to launch experimental environments in minutes instead of waiting weeks for hardware procurement. Which cloud benefit is MOST relevant?

A. Agility  
B. Fault tolerance  
C. Data sovereignty  
D. Dedicated tenancy

## 4
Which AWS Well-Architected pillar focuses on the ability of a workload to recover from failures and perform its intended function correctly?

A. Operational Excellence  
B. Reliability  
C. Performance Efficiency  
D. Sustainability

## 5
A team is reviewing whether its resources are right-sized and whether idle capacity can be removed. Which Well-Architected pillar is MOST directly involved?

A. Security  
B. Reliability  
C. Cost Optimization  
D. Operational Excellence

## 6
Which AWS Cloud Adoption Framework perspective focuses primarily on workforce skills, culture, leadership, and organizational change?

A. People  
B. Platform  
C. Security  
D. Operations

## 7
Which migration strategy means moving an application with minimal changes, commonly called “lift and shift”?

A. Repurchase  
B. Rehost  
C. Refactor  
D. Retire

## 8
A company has 300 TB of data to move to AWS, but its available network connection would take too long. Which AWS option should it consider?

A. Amazon Route 53  
B. AWS Snow Family  
C. AWS Direct Connect only  
D. Amazon CloudFront

## 9
Which cloud economics concept describes selecting resource sizes based on actual workload needs instead of overprovisioning?

A. Consolidated billing  
B. Rightsizing  
C. Fault isolation  
D. Federation

## 10
Which statement BEST describes economies of scale in cloud computing?

A. Customers receive unlimited capacity for one fixed fee.  
B. Large cloud providers can achieve infrastructure efficiencies by aggregating demand across many customers.  
C. Every AWS service becomes free after a one-year commitment.  
D. Customers no longer need to track cloud costs.

## 11 — Select TWO
Which TWO are common benefits of moving from traditional on-premises infrastructure to the AWS Cloud?

A. Faster resource provisioning  
B. Guaranteed elimination of all failures  
C. Ability to adjust capacity with demand  
D. Elimination of all operating expenditure  
E. Requirement to forecast peak capacity years in advance

## 12
Which framework is primarily used to help an organization assess cloud readiness and structure its cloud transformation journey?

A. AWS Well-Architected Framework  
B. AWS Cloud Adoption Framework  
C. AWS Shared Responsibility Model  
D. AWS Support Center

---

# Domain 2 — Security & Compliance (Questions 13–27)

## 13
Under the AWS Shared Responsibility Model, who is responsible for patching the guest operating system on an Amazon EC2 instance?

A. AWS  
B. Customer  
C. AWS Partner Network  
D. Amazon Inspector automatically in all cases

## 14
Which statement BEST describes responsibility for Amazon RDS compared with EC2?

A. The customer manages more underlying infrastructure for RDS than EC2.  
B. AWS manages more of the underlying database platform for RDS than for a self-managed database on EC2.  
C. AWS becomes responsible for the customer’s data in RDS.  
D. The customer has no security responsibilities when using RDS.

## 15
An application running on EC2 needs permission to read objects from an S3 bucket. Which approach follows AWS security best practices?

A. Store root-user credentials in the application  
B. Hard-code an IAM user access key in source code  
C. Assign an IAM role with the required permissions to the EC2 workload  
D. Make the S3 bucket public

## 16
Which security principle means giving identities only the permissions required to complete their tasks?

A. Least privilege  
B. Elasticity  
C. Federation  
D. High availability

## 17
Which service should be used to determine which identity called an AWS API that deleted a resource?

A. Amazon CloudWatch  
B. AWS CloudTrail  
C. AWS Config  
D. Amazon Inspector

## 18
A security team wants an alarm when an EC2 CPU metric exceeds a threshold. Which service is MOST appropriate?

A. AWS CloudTrail  
B. Amazon GuardDuty  
C. Amazon CloudWatch  
D. AWS Artifact

## 19
Which service records resource configuration changes and can evaluate resources against configuration rules?

A. AWS Config  
B. Amazon Macie  
C. AWS Shield  
D. AWS Secrets Manager

## 20
A compliance officer needs to download AWS compliance reports. Which service should be used?

A. AWS Artifact  
B. AWS Audit Manager  
C. AWS Trusted Advisor  
D. Amazon Detective

## 21
Which service helps automate the collection of evidence for audits?

A. AWS Artifact  
B. AWS Audit Manager  
C. AWS WAF  
D. Amazon Cognito

## 22
Which service is primarily used for managed threat detection?

A. Amazon Inspector  
B. Amazon GuardDuty  
C. Amazon Macie  
D. AWS Certificate Manager

## 23
Which service is designed to help identify software vulnerabilities in supported workloads?

A. Amazon Inspector  
B. Amazon GuardDuty  
C. AWS Shield  
D. AWS CloudTrail

## 24
A company needs to discover personally identifiable or sensitive data stored in Amazon S3. Which service should it use?

A. Amazon Macie  
B. Amazon Detective  
C. AWS Security Hub  
D. AWS Firewall Manager

## 25
Which service is primarily intended to protect applications against distributed denial-of-service attacks?

A. AWS WAF  
B. AWS Shield  
C. AWS Config  
D. Amazon Inspector

## 26
Which service should a company use to filter HTTP requests based on rules designed to block malicious web traffic?

A. AWS Shield  
B. AWS WAF  
C. AWS CloudHSM  
D. Amazon Macie

## 27 — Select TWO
Which TWO practices improve protection of the AWS account root user?

A. Enable MFA  
B. Share root credentials with administrators  
C. Avoid routine root-user usage  
D. Create root access keys for each application  
E. Disable IAM entirely

---

# Domain 3 — Cloud Technology & Services (Questions 28–44)

## 28
Which option provides virtual servers with operating-system-level control?

A. AWS Lambda  
B. Amazon EC2  
C. Amazon S3  
D. Amazon DynamoDB

## 29
A company wants to run event-driven code without provisioning or managing servers. Which service should it use?

A. AWS Lambda  
B. Amazon EC2  
C. Amazon EBS  
D. AWS Direct Connect

## 30
Which service is a managed Kubernetes service?

A. Amazon ECS  
B. Amazon EKS  
C. Amazon ECR  
D. AWS Fargate

## 31
Which service stores container images?

A. Amazon ECR  
B. Amazon ECS  
C. Amazon EKS  
D. AWS Batch

## 32
Which service provides serverless compute for containers?

A. AWS Fargate  
B. AWS Lambda only  
C. Amazon ECR  
D. Amazon Lightsail

## 33
A workload needs highly durable object storage for millions of images and documents. Which service is MOST appropriate?

A. Amazon EBS  
B. Amazon EFS  
C. Amazon S3  
D. Amazon EC2 Instance Store

## 34
Several EC2 instances need simultaneous access to the same managed file system. Which service is MOST appropriate?

A. Amazon EFS  
B. Amazon EBS  
C. Amazon S3 Glacier  
D. AWS Snow Family

## 35
An EC2 instance requires a persistent block-storage volume. Which service should be used?

A. Amazon EBS  
B. Amazon EFS  
C. Amazon S3  
D. Amazon Route 53

## 36
Which service is a managed relational database service?

A. Amazon DynamoDB  
B. Amazon RDS  
C. Amazon SQS  
D. Amazon OpenSearch Service

## 37
Which database is a serverless NoSQL key-value/document database?

A. Amazon Aurora  
B. Amazon RDS  
C. Amazon DynamoDB  
D. Amazon Redshift

## 38
Which service is primarily used as a cloud data warehouse?

A. Amazon Redshift  
B. Amazon RDS  
C. Amazon ElastiCache  
D. Amazon Neptune

## 39
Which database is designed for highly connected graph data?

A. Amazon Neptune  
B. Amazon DynamoDB  
C. Amazon DocumentDB  
D. Amazon Aurora

## 40
A company wants to query files stored in S3 using SQL without managing database servers. Which service should it use?

A. AWS Glue  
B. Amazon Athena  
C. Amazon EMR  
D. Amazon QuickSight

## 41
Which service is MOST associated with serverless data integration, ETL, and a data catalog?

A. AWS Glue  
B. Amazon Kinesis  
C. Amazon CloudFront  
D. AWS Step Functions

## 42
Which service is designed for real-time streaming data such as clickstreams and telemetry?

A. Amazon Kinesis  
B. Amazon Redshift  
C. Amazon Route 53  
D. AWS Artifact

## 43
Which service provides DNS functionality?

A. Amazon CloudFront  
B. Amazon Route 53  
C. AWS Direct Connect  
D. Amazon API Gateway

## 44
A company wants to cache and deliver web content globally with low latency. Which service should it use?

A. AWS Global Accelerator  
B. Amazon CloudFront  
C. AWS VPN  
D. Amazon VPC

---

# Domain 4 — Billing, Pricing & Support (Questions 45–50)

## 45
A solutions team is designing a new AWS workload and wants to estimate its expected monthly cost before deployment. Which tool should it use?

A. AWS Cost Explorer  
B. AWS Pricing Calculator  
C. AWS Budgets  
D. AWS Cost and Usage Report

## 46
A finance team wants to analyze AWS spending trends over the previous six months. Which tool is MOST appropriate?

A. AWS Cost Explorer  
B. AWS Pricing Calculator  
C. AWS Artifact  
D. AWS Service Catalog

## 47
A company wants an alert when monthly AWS spend reaches 80% of a defined limit. Which service should it use?

A. AWS Budgets  
B. AWS Cost Explorer  
C. Amazon CloudWatch only  
D. AWS Marketplace

## 48
A batch-processing workload can tolerate interruptions and needs the lowest-cost EC2 capacity option. Which purchasing option is MOST appropriate?

A. On-Demand Instances  
B. Spot Instances  
C. Dedicated Hosts  
D. Capacity Reservations

## 49
A company must ensure EC2 capacity is available in a specific Availability Zone **without requiring a long-term pricing commitment**. Which option addresses this requirement directly?

A. Savings Plans  
B. Spot Instances  
C. On-Demand Capacity Reservation  
D. S3 Intelligent-Tiering

## 50
A company has software licensing requirements tied to physical server sockets and cores and needs visibility/control of the underlying EC2 host. Which option is MOST appropriate?

A. Dedicated Host  
B. Dedicated Instance  
C. Spot Instance  
D. Savings Plan

---

# Bonus Domain 3 service drill

These six are extra because they are high-value service distinctions that did not fit the exact 50-question weighting.

## B1
Which network service provides a dedicated private connection from a company’s network to AWS?

A. AWS Direct Connect  
B. AWS Client VPN  
C. Amazon CloudFront  
D. AWS PrivateLink

## B2 — Select TWO
Which TWO statements are correct?

A. Security groups are stateful.  
B. Network ACLs are stateful.  
C. Network ACLs operate at the subnet level.  
D. Security groups are primarily DNS services.  
E. Route 53 is a firewall.

## B3
Which service should be used when a producer needs to place messages in a queue so a consumer can process them later?

A. Amazon SNS  
B. Amazon SQS  
C. Amazon EventBridge  
D. AWS Step Functions

## B4
Which service is MOST appropriate for fan-out publish/subscribe notifications to multiple subscribers?

A. Amazon SQS  
B. Amazon SNS  
C. AWS Step Functions  
D. Amazon EBS

## B5
Which AI service converts speech to text?

A. Amazon Polly  
B. Amazon Transcribe  
C. Amazon Translate  
D. Amazon Rekognition

## B6
A company needs to extract text, forms, and tables from scanned documents. Which service is MOST appropriate?

A. Amazon Rekognition  
B. Amazon Textract  
C. Amazon Comprehend  
D. Amazon Lex

Check `ANSWERS.md` only after completing the mock.
