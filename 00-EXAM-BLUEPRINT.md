# 00 — Official CLF-C02 Exam Blueprint

This file maps the current AWS CLF-C02 task statements into exactly what you need to know.

## Domain 1 — Cloud Concepts (24%)

### 1.1 Benefits of the AWS Cloud
Know:
- AWS Cloud value proposition
- Global infrastructure benefits: global reach, faster deployment
- High availability
- Elasticity
- Agility
- Scalability
- Economies of scale
- Variable vs fixed costs

You should be able to distinguish:
- **Scalability**: ability to handle growth
- **Elasticity**: automatically scale out/in with demand
- **High availability**: minimize downtime via redundancy
- **Fault tolerance**: continue operating despite component failures
- **Agility**: provision/change resources quickly

### 1.2 Design principles of the AWS Cloud
Know the six AWS Well-Architected pillars:
1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

Know the difference between them. Typical question: a scenario describes a design decision and asks which pillar it supports.

### 1.3 Migration benefits and strategies
Know:
- Why organizations migrate to AWS
- AWS Cloud Adoption Framework (AWS CAF)
- CAF perspectives: **Business, People, Governance, Platform, Security, Operations**
- Migration approaches and supporting services
- AWS Snow Family for offline/physical data transfer scenarios
- Database replication/migration concepts

For the exam, understand migration strategy concepts such as:
- Rehost (lift and shift)
- Replatform
- Refactor/re-architect
- Repurchase
- Retire
- Retain
- Relocate

Do not spend time implementing migration tools.

### 1.4 Cloud economics
Know:
- Fixed vs variable costs
- On-premises cost categories: facilities, power, cooling, hardware, maintenance, staff, networking, capacity planning
- BYOL vs license-included
- Rightsizing
- Automation benefits
- Economies of scale

---

# Domain 2 — Security and Compliance (30%)

## 2.1 Shared Responsibility Model
Know:
- **AWS = security OF the cloud**
- **Customer = security IN the cloud**
- Responsibilities shift depending on service

High-value comparison:

### EC2
AWS: facilities, hardware, physical networking, virtualization layer.  
Customer: guest OS, patches, apps, data, IAM, firewall/security-group configuration.

### RDS
AWS additionally manages more of the DB platform/OS/maintenance layer.  
Customer still owns data, DB access, users, configuration choices.

### Lambda
AWS manages even more infrastructure/runtime platform components.  
Customer still owns code, data, permissions, application configuration.

## 2.2 Security, governance, compliance
Know:
- Encryption at rest vs encryption in transit
- AWS Artifact = compliance reports/agreements
- CloudWatch = operational monitoring/metrics/logs/alarms
- CloudTrail = API/account activity audit trail
- AWS Config = resource configuration history/rules
- AWS Audit Manager = helps collect audit evidence
- GuardDuty = threat detection
- Inspector = vulnerability management
- Security Hub = central security posture/findings
- Shield = DDoS protection
- WAF = web request filtering
- Trusted Advisor can surface security/best-practice checks

## 2.3 Access management
Know:
- IAM users, groups, roles, policies
- Least privilege
- Root-user protection
- MFA
- Access keys vs console passwords
- IAM Identity Center
- Federation
- Cross-account roles
- Secrets Manager
- Systems Manager as a management/credential/configuration resource where relevant

Critical exam rules:
- Prefer temporary credentials/roles over hard-coded long-term credentials.
- Protect the root user and avoid routine use.
- An IAM role is **assumed** and commonly provides temporary credentials.

## 2.4 Security resources
Know use cases for:
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
- AWS Marketplace third-party security products
- AWS Knowledge Center / Security Blog / official docs

---

# Domain 3 — Cloud Technology and Services (34%)

## 3.1 Deploying and operating AWS
Know when to use:
- AWS Management Console
- AWS CLI
- SDKs/APIs
- Infrastructure as Code
- CloudFormation

Know deployment models:
- Cloud
- On-premises
- Hybrid

## 3.2 Global infrastructure
Know:
- Region
- Availability Zone
- Edge location
- Multi-AZ = high availability within a Region
- Multi-Region = disaster recovery, business continuity, data sovereignty, low latency for global users

## 3.3 Compute
Know:
- EC2 and instance-family categories
- Auto Scaling = elasticity
- Elastic Load Balancing = distribute traffic
- ECS = AWS container orchestration
- EKS = managed Kubernetes
- Fargate = serverless compute for containers
- Lambda = serverless functions/event-driven code
- ECR = container image registry
- Elastic Beanstalk = managed app deployment platform
- Lightsail = simplified VPS/application hosting
- Batch = batch jobs
- Outposts = AWS infrastructure on premises

## 3.4 Databases
Know:
- RDS = managed relational DB
- Aurora = AWS relational engine compatible with MySQL/PostgreSQL
- DynamoDB = serverless NoSQL key-value/document DB
- ElastiCache = in-memory cache
- DocumentDB = document database
- Neptune = graph database
- DMS = move/migrate databases/data
- SCT = convert database schemas

## 3.5 Networking
Know:
- VPC
- Public/private subnets
- Internet Gateway
- NAT concept
- Security Groups = stateful resource-level firewall
- Network ACLs = stateless subnet-level control
- Route 53 = DNS
- CloudFront = CDN
- Direct Connect = dedicated network connection
- VPN = encrypted tunnel
- Transit Gateway = network hub
- PrivateLink = private service connectivity
- Global Accelerator = improve global path/availability to application endpoints
- API Gateway = managed API front door

## 3.6 Storage
Know:
- S3 = object storage
- EBS = block storage for EC2
- EFS = shared file storage
- FSx = managed specialized file systems
- S3 storage classes and lifecycle policies
- S3 Glacier = archival tiers
- Instance Store = ephemeral block storage tied to host/instance lifecycle
- Storage Gateway = hybrid storage
- AWS Backup = centralized backups
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

Know storage-tier pricing concepts and data-transfer concepts.

General exam heuristics:
- On-Demand = flexible/unpredictable/short-term
- Reserved/Savings = predictable long-running usage/commitment discount
- Spot = cheapest for interruptible/fault-tolerant workloads
- Dedicated Host = physical server dedicated to you; licensing/compliance scenarios
- Capacity Reservation = reserve EC2 capacity in a specific AZ without necessarily providing a price discount

## 4.2 Billing and cost management
Know:
- AWS Budgets = thresholds/alerts
- Cost Explorer = analyze historical cost/usage and trends
- Pricing Calculator = estimate proposed architecture cost
- Cost and Usage Report = granular billing dataset
- Organizations consolidated billing
- Cost allocation tags
- Marketplace billing concepts

## 4.3 Technical resources and support
Know:
- AWS Documentation
- AWS whitepapers
- AWS Prescriptive Guidance
- AWS Knowledge Center
- AWS re:Post
- AWS Support Center
- AWS Professional Services
- AWS Solutions Architects
- AWS Partner Network
- Marketplace
- Trusted Advisor
- Health Dashboard / Health API
- Trust & Safety team for abuse reports

### Important 2026 support-plan note
The current AWS Support portfolio has changed. Current AWS Support documentation lists **Basic, Business Support+, Enterprise Support, and Unified Operations**, while the CLF-C02 domain text still includes older plan names as examples during the 2026 transition period. Do not spend hours memorizing old pricing tables. Learn the **support-level concept** and use the current AWS docs for live plan details.

---

# What to deliberately NOT study deeply

AWS explicitly says these job tasks are outside the CLF-C02 target candidate scope:
- coding
- architecture design
- troubleshooting
- implementation
- load/performance testing

So do not spend the next 48 hours configuring Kubernetes clusters, writing IAM JSON from scratch, building VPC route tables, tuning databases, or doing advanced labs.

# Official source links

- Exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Domain 1: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain1.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Out-of-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html
