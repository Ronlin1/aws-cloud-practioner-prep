# 00 — Official CLF-C02 Exam Blueprint

This is the scope-control file. It maps the current AWS CLF-C02 task statements into exactly what you need to know for the exam.

Official weights:
- Domain 1: Cloud Concepts — **24%**
- Domain 2: Security and Compliance — **30%**
- Domain 3: Cloud Technology and Services — **34%**
- Domain 4: Billing, Pricing, and Support — **12%**

# Domain 1 — Cloud Concepts (24%)

## 1.1 Benefits of the AWS Cloud
Know:
- AWS Cloud value proposition
- global infrastructure benefits: global reach, faster deployment
- high availability
- elasticity
- agility
- scalability
- economies of scale
- variable vs fixed costs

Distinguish:
- **Scalability**: ability to handle growth
- **Elasticity**: dynamically scale out/in with demand
- **High availability**: minimize downtime through redundancy
- **Fault tolerance**: continue operating despite component failure
- **Agility**: provision/change resources rapidly

## 1.2 Design principles of the AWS Cloud
Know the six AWS Well-Architected pillars:
1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

Recognize which pillar a scenario describes.

## 1.3 Migration benefits and strategies
Know:
- business/technical benefits of migrating
- AWS Cloud Adoption Framework (CAF)
- CAF perspectives: **Business, People, Governance, Platform, Security, Operations**
- migration approaches
- AWS Snow Family physical/offline transfer concept
- database/application migration-service recognition

Migration strategies:
- Rehost
- Replatform
- Refactor/re-architect
- Repurchase
- Retire
- Retain
- Relocate

## 1.4 Cloud economics
Know:
- fixed vs variable costs
- on-premises cost categories
- BYOL vs license-included
- rightsizing
- automation benefits
- economies of scale

---

# Domain 2 — Security and Compliance (30%)

## 2.1 Shared Responsibility Model
Know:
- **AWS = security OF the cloud**
- **Customer = security IN the cloud**
- responsibilities vary by service

High-value comparison:

### EC2
AWS: facilities, hardware, physical network, virtualization layer.  
Customer: guest OS/patches, apps, data, IAM, network/security configuration.

### RDS
AWS additionally manages more of the DB host/platform/maintenance layer.  
Customer still manages data, DB access, users, schema/application choices.

### Lambda
AWS manages still more infrastructure/runtime operations.  
Customer manages code, data, permissions and application configuration.

## 2.2 Security, governance and compliance
Know:
- encryption at rest vs in transit
- AWS Artifact = compliance reports/agreements
- CloudWatch = operational metrics/logs/alarms
- CloudTrail = API/account activity
- Config = resource configuration history/rules
- Audit Manager = audit evidence collection
- GuardDuty = threat detection
- Inspector = vulnerability management
- Security Hub = central security posture/findings
- Shield = DDoS protection
- WAF = web request filtering
- where security logs/audit evidence can be found
- IAM credential/access reporting concepts

## 2.3 Access management
Know:
- IAM users, groups, roles and policies
- AWS managed vs customer managed vs inline policies
- least privilege
- root-user protection and **common root-only task examples**
- MFA
- access keys vs console passwords
- IAM password policies
- IAM Identity Center
- federation
- cross-account roles
- Secrets Manager
- Systems Manager Parameter Store / SecureString at recognition level
- IAM credential report

Critical exam rules:
- prefer temporary credentials/roles over hard-coded long-term credentials
- protect the root user; do not use root routinely
- an IAM role is assumed and commonly supplies temporary credentials
- an IAM credential report audits IAM user credential/MFA/key status

## 2.4 Security resources
Recognize use cases for:
- WAF
- Firewall Manager
- Shield
- GuardDuty
- Inspector
- Macie
- Security Hub
- Detective
- KMS
- CloudHSM
- ACM
- Secrets Manager
- Parameter Store
- AWS Marketplace third-party security products
- AWS Knowledge Center / security documentation / Security Blog
- Trusted Advisor security checks

---

# Domain 3 — Cloud Technology and Services (34%)

## 3.1 Deploying and operating AWS
Know:
- one-time/manual operations vs repeatable/automated operations
- AWS Management Console
- AWS CLI
- SDKs/APIs
- Infrastructure as Code
- CloudFormation

Exam logic:
- one-off visual/manual administration -> Console may fit
- repeatable scripting/automation -> CLI/SDK/API
- repeatable infrastructure definition -> IaC/CloudFormation

Know deployment models:
- Cloud
- On-premises
- Hybrid

## 3.2 Global infrastructure
Know:
- Region
- Availability Zone
- edge location
- Region-selection factors: compliance, proximity/latency, service availability, pricing
- Multi-AZ = availability/resilience inside a Region
- Multi-Region = regional resilience/DR/global requirements/data sovereignty
- edge services such as CloudFront

## 3.3 Compute
Know:
- EC2 and instance-family categories
- Auto Scaling = elasticity/capacity adjustment
- Elastic Load Balancing = distribute traffic
- ECS = AWS container orchestration
- EKS = managed Kubernetes
- Fargate = serverless compute for containers
- Lambda = serverless/event-driven functions
- ECR = container image registry
- Elastic Beanstalk = managed application deployment environment
- Lightsail = simplified hosting
- Batch = batch jobs
- Outposts = AWS infrastructure on premises

## 3.4 Databases
Know:
- RDS = managed relational DB
- Aurora = AWS relational engine compatible with MySQL/PostgreSQL
- DynamoDB = serverless NoSQL key-value/document DB
- ElastiCache = in-memory cache
- DocumentDB = document DB
- Neptune = graph DB
- DMS = database/data migration
- SCT = schema conversion
- Redshift distinction as analytics warehouse

## 3.5 Networking
Know:
- VPC, subnets, route tables, gateways
- Internet Gateway
- NAT concept
- Security Groups = stateful resource-level control
- Network ACLs = stateless subnet-level control
- Route 53 = DNS
- CloudFront = CDN
- Direct Connect = dedicated network connection
- VPN = encrypted tunnel
- Site-to-Site vs Client VPN
- Transit Gateway = network hub
- PrivateLink = private service connectivity
- Global Accelerator = optimized global path to application endpoints
- API Gateway = managed API front door

## 3.6 Storage
Know:
- S3 = object storage
- S3 storage classes / lifecycle policies
- S3 Glacier = archival tiers
- EBS = persistent block storage for EC2
- Instance Store = ephemeral host-attached storage
- EFS = shared managed file storage
- FSx = managed specialized file systems
- Storage Gateway = hybrid storage
- AWS Backup = centralized backup
- Elastic Disaster Recovery = DR

## 3.7 AI/ML and analytics
Recognition-level use cases matter most.

Analytics:
- Athena = SQL directly over S3
- Glue = ETL/data integration/catalog
- EMR = managed Hadoop/Spark big data
- Kinesis = streaming data
- QuickSight = BI/dashboards
- Redshift = data warehouse
- OpenSearch = search/log analytics

AI/ML:
- SageMaker AI = build/train/deploy ML
- Comprehend = NLP/text insights
- Kendra = intelligent enterprise search
- Lex = conversational bots
- Polly = text to speech
- Transcribe = speech to text
- Translate = language translation
- Rekognition = image/video analysis
- Textract = document text/forms/tables extraction
- Amazon Q = generative-AI assistant family

## 3.8 Other in-scope categories
Know recognition/use cases for:
- EventBridge
- SNS
- SQS
- Step Functions
- Connect
- SES
- CodeBuild
- CodePipeline
- X-Ray
- WorkSpaces
- AppStream 2.0
- WorkSpaces Secure Browser
- Amplify
- AppSync
- IoT Core
- Management Console
- Compute Optimizer
- Control Tower
- Health Dashboard
- License Manager
- Organizations
- Service Catalog
- Service Quotas
- Systems Manager
- Trusted Advisor
- Well-Architected Tool
- Application Discovery Service
- Application Migration Service
- Migration Evaluator
- Migration Hub
- AWS Support

---

# Domain 4 — Billing, Pricing, and Support (12%)

## 4.1 Pricing models
Know EC2 purchasing concepts:
- On-Demand
- Reserved Instances
- Savings Plans
- Spot Instances
- Dedicated Hosts
- Dedicated Instances
- Capacity Reservations

Explicit RI concepts:
- Standard vs Convertible
- Regional vs Zonal
- Regional RI: AZ flexibility; no capacity reservation
- Zonal RI: capacity reservation in specific AZ
- eligible Regional Linux/Unix default-tenancy RI instance-size flexibility
- RI/Savings Plans discount sharing behavior in AWS Organizations at high level

Know storage-tier pricing and basic data-transfer pricing concepts.

General heuristics:
- On-Demand = flexible/unpredictable/short-term
- Reserved/Savings = predictable commitment discount
- Spot = interruption-tolerant low-cost capacity
- Dedicated Host = physical host/licensing scenarios
- Capacity Reservation = guarantee capacity without inherently adding a discount

## 4.2 Billing and cost management
Know:
- AWS Budgets = thresholds/alerts
- Cost Explorer = historical cost/usage analysis/trends/forecasts
- Pricing Calculator = estimate proposed architecture cost
- Cost and Usage Report = granular billing dataset
- Organizations consolidated billing
- AWS-generated vs user-defined cost allocation tags
- relationship of cost tags to Cost Explorer/CUR
- Marketplace billing/procurement concepts

## 4.3 Technical resources and support
Know:
- AWS Documentation
- AWS Whitepapers
- AWS Prescriptive Guidance
- AWS Knowledge Center / re:Post Knowledge Center
- AWS re:Post
- AWS Support Center
- AWS Professional Services
- AWS Solutions Architects
- AWS Partner Network
- Independent Software Vendors vs system integrators/consulting partners
- partner benefits/use cases
- AWS Marketplace key purpose
- Trusted Advisor
- Health Dashboard / Health API
- Trust & Safety for abuse reports

### Important 2026 Support-plan transition
Current AWS Support docs list:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

The CLF-C02 Domain 4 page still gives legacy/transitional plan names as examples, including Developer Support, Business Support and Enterprise On-Ramp. AWS states those legacy plans retire January 1, 2027.

For the exam:
- recognize support-plan concepts and levels
- recognize both current and legacy names if they appear in answer choices
- do not spend 48-hour cram time memorizing every price/response-time table

---

# Explicitly out-of-scope candidate job tasks

AWS says the CLF-C02 target candidate is not expected to perform:
- coding
- designing cloud architecture
- troubleshooting
- implementation
- load/performance testing

So do not spend these 48 hours configuring Kubernetes clusters, writing IAM JSON from scratch, building advanced VPC route tables, tuning databases, or doing complex deployment labs.

# Official source links

- Exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Technologies and concepts: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-technologies-concepts.html
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Out-of-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html

Last validated: **2026-09-16**.
