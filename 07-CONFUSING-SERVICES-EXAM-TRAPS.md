# 07 — Confusing Services & Exam Traps

This file is one of the highest-value things to revise before the exam.

# CloudWatch vs CloudTrail vs Config vs IAM Credential Report

## CloudWatch
- metrics
- logs
- alarms
- dashboards

Question: “CPU is above 80%; alert operations.” -> **CloudWatch**

## CloudTrail
- AWS API/account activity
- who did what and when

Question: “Who terminated this EC2 instance?” -> **CloudTrail**

## Config
- resource configuration history
- configuration/compliance rules

Question: “Was this S3 bucket configured as public?” -> **AWS Config**

## IAM Credential Report
- IAM user credential status
- password/access-key/MFA information

Question: “Which IAM users have MFA or stale access keys?” -> **IAM credential report**

---

# AWS managed vs Customer managed vs Inline IAM policies

- **AWS managed** -> created and maintained by AWS; reusable
- **Customer managed** -> created/edited by customer; reusable
- **Inline** -> embedded directly in one user/group/role; one-to-one

Trap: an AWS managed policy is not a policy that the customer edits.

---

# Secrets Manager vs Systems Manager Parameter Store

## Secrets Manager
Purpose-built for secrets/credentials such as database passwords, API keys and tokens; supports dedicated secret-management features such as rotation.

## Parameter Store
Configuration/key-value parameters; supports `String`, `StringList`, and encrypted `SecureString` values.

Exam reflex:
- rotating DB password/API secret -> **Secrets Manager**
- endpoint URL/environment/config value/SecureString parameter -> **Parameter Store**

AWS recommends Secrets Manager when the data is truly a credential/secret requiring purpose-built secret management.

---

# S3 vs EBS vs EFS vs FSx

- **S3** -> object storage
- **EBS** -> EC2 block volume/disk
- **EFS** -> shared managed filesystem
- **FSx** -> specialized managed filesystem

Question keywords:
- photos/backups/log files/data lake -> S3
- boot/database disk for EC2 -> EBS
- many Linux servers share files -> EFS

---

# RDS vs DynamoDB vs Redshift vs ElastiCache

- **RDS/Aurora** -> relational application DB
- **DynamoDB** -> NoSQL key-value/document
- **Redshift** -> data warehouse/analytics
- **ElastiCache** -> in-memory cache

Trap: Redshift is not the default relational transaction DB simply because it uses SQL.

---

# SQS vs SNS vs EventBridge vs Step Functions

## SQS
Queue/buffer. Consumer processes messages later.

## SNS
Publish/subscribe, fan-out to multiple subscribers.

## EventBridge
Event bus/routing according to rules.

## Step Functions
Orchestrate a multi-step workflow/state machine.

Mnemonic:
- **Queue** -> SQS
- **Notify many** -> SNS
- **Route events** -> EventBridge
- **Sequence steps** -> Step Functions

---

# GuardDuty vs Inspector vs Macie vs Detective vs Security Hub

- **GuardDuty** -> detect threats/suspicious activity
- **Inspector** -> vulnerabilities
- **Macie** -> sensitive data in S3
- **Detective** -> investigate security issues/findings
- **Security Hub** -> aggregate security posture/findings

---

# WAF vs Shield vs Firewall Manager

- **WAF** -> HTTP(S) request filtering; SQLi/XSS/IP rules
- **Shield** -> DDoS protection
- **Firewall Manager** -> centrally manage firewall policies

---

# IAM vs IAM Identity Center vs Cognito vs Federation

- **IAM** -> AWS identities, roles, policies, resource permissions
- **IAM Identity Center** -> workforce access across AWS accounts/apps
- **Cognito** -> end users of your web/mobile application
- **Federation** -> use external identity provider to obtain temporary AWS access

---

# KMS vs CloudHSM vs Secrets Manager vs ACM

- **KMS** -> encryption key management
- **CloudHSM** -> dedicated HSM cryptographic hardware
- **Secrets Manager** -> passwords/API credentials/secrets
- **ACM** -> SSL/TLS certificates

---

# Route 53 vs CloudFront vs Global Accelerator

- **Route 53** -> DNS
- **CloudFront** -> CDN/edge caching/content delivery
- **Global Accelerator** -> optimize global network path/availability to app endpoints

---

# Direct Connect vs VPN

- **Direct Connect** -> dedicated network connection
- **VPN** -> encrypted tunnel

A company can combine the two in real-world designs, but exam questions usually distinguish the primary requirement.

---

# Security Group vs Network ACL

- **Security Group** -> stateful, resource/network-interface level
- **NACL** -> stateless, subnet level

Stateful means response traffic is tracked automatically for allowed connections.

---

# Multi-AZ vs Multi-Region

- **Multi-AZ** -> availability/resilience within a Region
- **Multi-Region** -> regional DR, business continuity, data sovereignty, global user latency

Trap: Auto Scaling across instances in only one AZ does not automatically eliminate the AZ as a failure domain.

---

# ELB vs Auto Scaling

- **ELB** -> distributes traffic
- **Auto Scaling** -> changes capacity

They are commonly used together but are not the same service/function.

---

# EC2 vs Lambda vs Fargate

- **EC2** -> virtual machine, OS-level control
- **Lambda** -> serverless functions
- **Fargate** -> serverless compute for containers

---

# ECS vs EKS vs ECR

- **ECS** -> AWS container orchestration
- **EKS** -> Kubernetes
- **ECR** -> image registry

---

# Athena vs Glue vs EMR vs Redshift

- **Athena** -> SQL directly against S3
- **Glue** -> ETL/data integration/Data Catalog
- **EMR** -> Spark/Hadoop big-data platform
- **Redshift** -> data warehouse

---

# Polly vs Transcribe vs Translate vs Comprehend

- **Polly** -> text to speech
- **Transcribe** -> speech to text
- **Translate** -> one language to another
- **Comprehend** -> understand/analyze text (NLP)

---

# Rekognition vs Textract

- **Rekognition** -> understand/analyze images and video
- **Textract** -> extract text/forms/tables from documents

---

# Pricing Calculator vs Cost Explorer vs Budgets vs CUR

- **Pricing Calculator** -> estimate future/proposed cost
- **Cost Explorer** -> analyze spending/trends
- **Budgets** -> alerts against thresholds
- **Cost and Usage Report** -> detailed cost/usage dataset

---

# Trusted Advisor vs Compute Optimizer

- **Trusted Advisor** -> broad AWS best-practice recommendations/checks
- **Compute Optimizer** -> right-sizing/resource recommendations for supported resources based on utilization

---

# Health Dashboard vs CloudWatch

- **Health Dashboard / AWS Health** -> AWS events impacting your account/resources
- **CloudWatch** -> workload/service operational metrics/logs/alarms

---

# Artifact vs Audit Manager

- **Artifact** -> AWS compliance reports/agreements
- **Audit Manager** -> automate collection/organization of audit evidence

---

# Service Catalog vs Marketplace

- **Service Catalog** -> organization's governed catalog of approved products users can provision
- **Marketplace** -> discover/procure third-party software, data and services

---

# DMS vs SCT

- **DMS** -> move database data
- **SCT** -> convert schema/code between engines

---

# Application Discovery vs Application Migration vs Migration Hub

- **Application Discovery Service** -> discover inventory/dependencies
- **Application Migration Service** -> migrate servers/apps
- **Migration Hub** -> track migration projects

---

# Backup vs High Availability vs Disaster Recovery

- **Backup** -> data copy for restore
- **High availability** -> keep service available through component failure
- **Disaster recovery** -> restore/continue after major disruption

---

# Scalability vs Elasticity

- **Scalability** -> ability to handle growth
- **Elasticity** -> dynamically grow and shrink capacity with demand

---

# Agility vs Elasticity

- **Agility** -> deploy/change quickly
- **Elasticity** -> match capacity to demand dynamically

---

# Well-Architected vs CAF

- **Well-Architected Framework** -> workload architecture/operations best practices; six pillars
- **Cloud Adoption Framework** -> organizational cloud transformation; six perspectives

### Well-Architected pillars
Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability.

### CAF perspectives
Business, People, Governance, Platform, Security, Operations.

CAF outcome examples from the exam guide include reduced business risk, improved ESG performance, increased revenue and increased operational efficiency.

---

# On-Demand vs Spot vs Reserved vs Savings Plans

- unpredictable/no commitment -> **On-Demand**
- interruption-tolerant/very low-cost spare capacity -> **Spot**
- predictable EC2 commitment -> **Reserved Instance**
- predictable eligible compute-spend commitment with broader flexibility -> **Savings Plans**

---

# Standard vs Convertible Reserved Instance

- **Standard RI** -> no exchange to a different RI configuration; less flexible
- **Convertible RI** -> can be exchanged for a different Convertible RI configuration of equal or greater value

---

# Regional vs Zonal Reserved Instance

## Regional RI
- discount can apply across AZs in selected Region
- does **not** reserve capacity
- eligible Linux/Unix default-tenancy regional RIs can provide instance-size flexibility

## Zonal RI
- scoped to one AZ
- **reserves capacity in that AZ**
- no AZ flexibility
- no instance-size flexibility

Important correction to a common oversimplification:
> Not every Reserved Instance is “discount only.” A **Zonal RI includes a capacity reservation**. A Regional RI does not.

---

# Reserved Instance vs On-Demand Capacity Reservation

- **Reserved Instance** -> commitment-based billing discount; Zonal RI also reserves capacity
- **On-Demand Capacity Reservation** -> reserve EC2 capacity without inherently creating a pricing discount commitment

Eligible Savings Plans or Regional RI discounts can still apply to matching usage in a Capacity Reservation.

---

# Dedicated Host vs Dedicated Instance vs Capacity Reservation

- **Dedicated Host** -> physical host dedicated to you, licensing/host visibility
- **Dedicated Instance** -> instance on dedicated hardware, less host-level control
- **Capacity Reservation** -> reserve EC2 capacity for specified attributes

---

# Support Center vs re:Post vs Health vs Trust & Safety

- **Support Center** -> create/manage AWS Support cases according to entitlement
- **re:Post** -> AWS community Q&A/knowledge
- **AWS Health** -> AWS events affecting your resources/account
- **Trust & Safety** -> report abuse/misuse involving AWS resources

---

# Professional Services vs Solutions Architects vs APN

- **AWS Professional Services** -> AWS expert engagement for transformations/complex initiatives
- **AWS Solutions Architects** -> AWS technical solution guidance
- **AWS Partner Network (APN)** -> external AWS consulting/technology partner ecosystem

APN examples:
- ISV -> software vendor
- system integrator/consulting partner -> migration/integration/implementation help

AWS Partner benefits explicitly called out by the CLF-C02 guide include partner training/certification, partner events and partner volume discounts.

---

# How AWS distractors work

AWS says incorrect options are deliberately plausible for candidates with incomplete knowledge. Use category elimination.

Example:
> Need DNS.

Choices might include CloudFront, Route 53, Direct Connect, API Gateway.

Before comparing details, eliminate everything that is not DNS. Answer Route 53.

# Question-solving algorithm

1. Read the final question sentence.
2. Identify keywords: **MOST cost-effective, LEAST operational overhead, managed, serverless, audit, monitor, queue, notify, archive, relational, NoSQL, high availability**.
3. Identify the service category.
4. Eliminate options from other categories.
5. Compare the final two by the exact requirement.
6. For multiple response, validate every option independently.

# Common wording traps

## “Managed”
Often points away from running software yourself on EC2 and toward a managed AWS service.

## “Least operational overhead”
Often favors serverless/managed solutions over EC2/self-managed software.

## “Highly available”
Look for redundancy/Multi-AZ, not merely a larger server.

## “Durable object storage”
S3.

## “Audit API activity”
CloudTrail, not CloudWatch.

## “Monitor performance”
CloudWatch, not CloudTrail.

## “Sensitive S3 data”
Macie.

## “DDoS”
Shield.

## “Web exploit/filter requests”
WAF.

## “No servers to manage”
Lambda/Fargate/other serverless service depending on workload.

## “Decouple”
Usually SQS.

## “Fan out”
Usually SNS.

## “Global cached content”
CloudFront.

## “DNS”
Route 53.
