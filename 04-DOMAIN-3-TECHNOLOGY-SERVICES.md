# Domain 3 — Cloud Technology & Services (34%)

This is the largest domain. Your job is primarily **service recognition**: what a service does, when to choose it, and what it is confused with.

# 1. Ways to deploy and operate AWS

## AWS Management Console
Browser GUI.

## AWS CLI
Command-line access to AWS.

## AWS SDKs / APIs
Programmatic access from applications/code.

## Infrastructure as Code
Repeatable infrastructure provisioning from code/templates.

### AWS CloudFormation
AWS IaC service.

Trigger:
> “Provision the same infrastructure repeatedly from a template.”

## Deployment models
- Cloud
- On-premises
- Hybrid

Hybrid = combine on-premises and AWS.

---

# 2. AWS global infrastructure

## Region
Separate geographic AWS area.

Selection considerations:
- latency/proximity to users
- legal/data-residency requirements
- service availability
- pricing

## Availability Zone (AZ)
Separate failure domain inside a Region, made of one or more discrete data centers.

Use multiple AZs for high availability.

## Edge locations
Used by edge services such as CloudFront to bring content/services closer to users.

## Multi-AZ vs Multi-Region
- Multi-AZ -> high availability inside one Region
- Multi-Region -> DR/business continuity/global latency/data sovereignty

---

# 3. COMPUTE

## Amazon EC2
Virtual servers in AWS.

Use when you need OS-level control and a VM.

### EC2 instance family concepts
- General purpose -> balanced
- Compute optimized -> CPU-intensive
- Memory optimized -> RAM-intensive
- Storage optimized -> high storage I/O/local storage workloads
- Accelerated computing -> GPUs/special accelerators

## Elastic Load Balancing (ELB)
Distributes incoming traffic among targets.

Trigger:
> “Distribute traffic across multiple servers.”

## EC2 Auto Scaling / AWS Auto Scaling
Automatically changes capacity according to demand.

Trigger:
> “Elasticity”, “add/remove instances based on demand”.

### ELB vs Auto Scaling
- ELB -> distributes traffic
- Auto Scaling -> changes capacity

## AWS Lambda
Serverless functions/event-driven compute.

Trigger:
> “Run code without provisioning/managing servers.”

Common scenario:
S3 upload -> Lambda processes object.

## AWS Batch
Runs/schedules batch computing jobs.

Trigger:
> “Large number of non-interactive batch jobs.”

## Elastic Beanstalk
Deploy applications while AWS provisions/manages much of the environment.

Trigger:
> “Upload application code and let AWS handle environment provisioning.”

## Amazon Lightsail
Simplified bundled VPS/application hosting.

Trigger:
> “simple website/small application with predictable bundled resources.”

## AWS Outposts
AWS infrastructure/services in an on-premises environment.

Trigger:
> “AWS infrastructure on premises / hybrid requirement.”

---

# 4. CONTAINERS

## Amazon ECR
Container image registry.

Trigger:
> “store Docker/container images.”

## Amazon ECS
AWS-native container orchestration.

Trigger:
> “run/orchestrate containers on AWS without requiring Kubernetes.”

## Amazon EKS
Managed Kubernetes.

Trigger:
> “Kubernetes on AWS.”

## AWS Fargate
Serverless compute engine for containers.

Trigger:
> “run containers without managing EC2 worker servers.”

### Memorize
- ECR -> store images
- ECS -> orchestrate containers
- EKS -> Kubernetes
- Fargate -> serverless container compute

---

# 5. STORAGE

## Amazon S3
Object storage.

Use for:
- files/objects
- images/videos
- backups
- logs
- static assets
- data lakes

### Key concepts
- buckets contain objects
- versioning keeps object versions
- lifecycle policies transition/delete objects automatically
- storage classes optimize for access pattern/cost

### S3 classes to recognize
- S3 Standard -> frequent/general access
- S3 Intelligent-Tiering -> changing/unknown access patterns
- S3 Standard-IA -> infrequent access, rapid retrieval
- S3 One Zone-IA -> infrequent access in one AZ where that resilience is acceptable
- S3 Glacier classes -> archive

Do not memorize every price or retrieval minute.

## Amazon EBS
Block storage commonly attached to EC2.

Trigger:
> “persistent disk/volume for EC2.”

## Instance Store
Temporary/ephemeral block storage physically attached to host.

Trigger:
> “very fast temporary local storage where data can be lost when instance/host lifecycle ends.”

## Amazon EFS
Managed shared file system.

Trigger:
> “multiple Linux compute instances need the same shared filesystem.”

## Amazon FSx
Managed specialized file systems.

Recognition level is enough. Know it is **file storage**, not object/block storage.

## AWS Storage Gateway
Hybrid on-premises access/integration with AWS cloud storage.

Trigger:
> “on-premises applications need cloud-backed storage.”

## AWS Backup
Centralized backup management for supported AWS services.

## AWS Elastic Disaster Recovery
Disaster-recovery replication/recovery capability.

### Storage master distinction
- S3 -> object
- EBS -> block
- EFS -> file
- FSx -> specialized managed file
- Glacier -> archive
- Storage Gateway -> hybrid storage
- Backup -> centralized backup

---

# 6. DATABASES

## Amazon RDS
Managed relational database service.

Engines include PostgreSQL, MySQL, MariaDB, Oracle, SQL Server and others supported by RDS.

Trigger:
> “managed relational database.”

## Amazon Aurora
AWS-designed relational database compatible with MySQL/PostgreSQL.

Trigger:
> “AWS relational engine compatible with MySQL/PostgreSQL.”

## Amazon DynamoDB
Serverless NoSQL key-value/document database.

Triggers:
- NoSQL
- key-value
- massive scale
- low latency
- serverless DB

## Amazon ElastiCache
Managed in-memory caching.

Trigger:
> “reduce database load/accelerate repeated reads using cache.”

## Amazon DocumentDB
Managed document database compatible with MongoDB workloads/APIs.

## Amazon Neptune
Graph database.

Triggers:
- relationships
- social graph
- fraud graph
- knowledge graph

## EC2-hosted database vs managed DB
Use EC2 when you need more OS/DB-platform control.
Use managed database services when you want AWS to handle more of the underlying operations.

## AWS DMS
Database Migration Service.

Trigger:
> move/migrate database data.

## AWS SCT
Schema Conversion Tool.

Trigger:
> convert database schema/code between database engines.

### Critical DB distinctions
- RDS/Aurora -> relational
- DynamoDB -> NoSQL key-value/document
- ElastiCache -> cache
- DocumentDB -> document DB
- Neptune -> graph
- Redshift -> analytical data warehouse

---

# 7. NETWORKING

## Amazon VPC
Logically isolated network in AWS.

Know these components conceptually:
- CIDR/IP ranges
- subnets
- route tables
- gateways
- security controls

## Public subnet
Has routing that can support internet connectivity through an Internet Gateway for appropriately configured resources.

## Private subnet
No direct public-internet route for resources in the usual design.

## Internet Gateway
Connects a VPC to the internet.

## NAT Gateway concept
Allows resources in private subnets to initiate outbound internet access without exposing them to unsolicited inbound traffic like public resources.

## Security Group
Stateful firewall associated with resource/network interface.

## Network ACL
Stateless subnet-level network control.

Memorize:
- Security Group -> stateful, resource level
- NACL -> stateless, subnet level

## Amazon Route 53
DNS service.

Trigger:
> domain-name resolution/routing.

## Amazon CloudFront
Content Delivery Network (CDN).

Trigger:
> cache/distribute content globally with low latency.

## AWS Direct Connect
Dedicated private network connectivity from customer environment to AWS.

## AWS VPN
Encrypted network tunnel, usually across public connectivity.

### Direct Connect vs VPN
- dedicated connection -> Direct Connect
- encrypted tunnel -> VPN

## AWS Site-to-Site VPN
Connect on-premises network to VPC.

## AWS Client VPN
Individual client/device remote access.

## AWS Transit Gateway
Central networking hub connecting VPCs and supported on-premises networks.

Trigger:
> many VPCs/networks need hub-and-spoke connectivity.

## AWS PrivateLink
Private connectivity to supported services without exposing traffic to public internet.

## AWS Global Accelerator
Uses AWS global network to improve application availability/performance to global users.

Do not confuse with CloudFront:
- CloudFront -> CDN/content caching
- Global Accelerator -> optimized network path to application endpoints

## Amazon API Gateway
Managed service to create/publish/manage APIs.

Common serverless pattern:
Client -> API Gateway -> Lambda

---

# 8. ANALYTICS

## Amazon Athena
Serverless SQL query service for data in S3.

Trigger:
> “SQL directly over S3 files.”

## AWS Glue
Data integration/ETL + Data Catalog.

Trigger:
> transform/catalog/integrate data.

## Amazon EMR
Managed big-data platform for frameworks such as Spark/Hadoop.

Trigger:
> managed Spark/Hadoop/big-data clusters.

## Amazon Kinesis
Real-time streaming data.

Triggers:
- clickstreams
- logs
- telemetry
- real-time stream processing

## Amazon QuickSight
Business intelligence and dashboards.

## Amazon Redshift
Cloud data warehouse/large analytical SQL workloads.

## Amazon OpenSearch Service
Managed search/log analytics/observability search use cases.

### Analytics master mapping
- SQL on S3 -> Athena
- ETL/catalog -> Glue
- Spark/Hadoop -> EMR
- real-time streams -> Kinesis
- dashboards -> QuickSight
- warehouse -> Redshift
- search/log analytics -> OpenSearch

---

# 9. AI/ML SERVICES

For CLF-C02, recognition is enough.

## Amazon SageMaker AI
Build/train/deploy machine-learning models.

## Amazon Comprehend
Natural-language processing/text insights.

Triggers:
- sentiment
- entities
- text analysis

## Amazon Kendra
Intelligent enterprise search.

## Amazon Lex
Conversational chatbot/voice interfaces.

## Amazon Polly
Text -> speech.

## Amazon Transcribe
Speech -> text.

## Amazon Translate
Language translation.

## Amazon Rekognition
Image/video analysis.

## Amazon Textract
Extract text/forms/tables from documents.

## Amazon Q
Generative-AI assistant/service family for supported AWS/business use cases.

### Memorize pairs
- Polly = text to speech
- Transcribe = speech to text
- Translate = language to language
- Rekognition = images/video
- Textract = documents/forms/tables
- Comprehend = NLP/text meaning
- Lex = conversational bot
- Kendra = intelligent search
- SageMaker AI = ML platform

---

# 10. APPLICATION INTEGRATION

## Amazon SQS
Message queue. Decouples producers and consumers.

Trigger:
> “queue work”, “buffer messages”, “consumer can process later”.

## Amazon SNS
Publish/subscribe/fan-out notifications.

Trigger:
> “one message to multiple subscribers/endpoints.”

## Amazon EventBridge
Event bus/routing for event-driven applications.

Trigger:
> “route events from sources to targets according to rules.”

## AWS Step Functions
Workflow orchestration/state machines.

Trigger:
> “coordinate a sequence of application/service steps.”

### Critical distinction
- SQS -> queue
- SNS -> pub/sub notification fan-out
- EventBridge -> event routing/bus
- Step Functions -> workflow orchestration

---

# 11. BUSINESS APPLICATIONS

## Amazon Connect
Cloud contact center.

## Amazon SES
Simple Email Service.

Trigger:
> send application/transactional/bulk email.

---

# 12. DEVELOPER TOOLS

## AWS CLI
Command-line management.

## AWS CodeBuild
Managed build/test service.

## AWS CodePipeline
Continuous delivery pipeline orchestration.

## AWS X-Ray
Distributed tracing for applications.

Triggers:
- trace request path
- analyze distributed-service latency/errors

---

# 13. END USER COMPUTING

## Amazon WorkSpaces
Cloud virtual desktops.

## Amazon AppStream 2.0
Stream desktop applications to users.

## Amazon WorkSpaces Secure Browser
Secure browser-based access to internal/SaaS/web resources.

---

# 14. FRONTEND WEB/MOBILE

## AWS Amplify
Build/deploy/host web/mobile application frontends and related backend integrations.

## AWS AppSync
Managed GraphQL APIs and real-time data synchronization capabilities.

Recognition level is enough.

---

# 15. INTERNET OF THINGS

## AWS IoT Core
Connect/manage IoT devices and exchange messages securely.

Trigger:
> sensors/devices/telemetry.

---

# 16. MANAGEMENT & GOVERNANCE

## AWS CloudFormation
Infrastructure as Code.

## AWS CloudTrail
API audit/activity.

## Amazon CloudWatch
Metrics/logs/alarms.

## AWS Config
Configuration tracking/compliance.

## AWS Compute Optimizer
Right-sizing recommendations for supported compute/resources.

## AWS Control Tower
Governed multi-account landing zone.

## AWS Health Dashboard
AWS events/issues affecting your account/resources.

## AWS License Manager
Track/manage software licenses.

## AWS Organizations
Multi-account governance/consolidated billing/SCPs.

## AWS Service Catalog
Governed catalog of approved products/resources users can deploy.

## Service Quotas
View/manage/request increases to AWS service quotas.

## AWS Systems Manager
Operate/manage fleets/resources: patching, automation, inventory, remote operations, configuration capabilities.

## AWS Trusted Advisor
Best-practice checks/recommendations.

## AWS Well-Architected Tool
Review workloads against Well-Architected Framework best practices.

---

# 17. MIGRATION & TRANSFER

## Application Discovery Service
Discover on-premises inventory/dependencies for migration planning.

## Application Migration Service
Migrate servers/applications to AWS.

## Database Migration Service (DMS)
Migrate database data.

## Migration Evaluator
Build migration business case/cost analysis.

## Migration Hub
Track/manage migration progress centrally.

## Schema Conversion Tool (SCT)
Convert DB schema/code.

## Snow Family
Physical devices for data migration/edge scenarios when network transfer is impractical.

---

# 18. SERVICE RECOGNITION DRILL

Say the answer within 3 seconds:

- VM -> EC2
- serverless function -> Lambda
- load distribution -> ELB
- elastic EC2 capacity -> Auto Scaling
- container images -> ECR
- AWS containers -> ECS
- Kubernetes -> EKS
- serverless containers -> Fargate
- object storage -> S3
- EC2 disk -> EBS
- shared filesystem -> EFS
- archive -> Glacier
- hybrid storage -> Storage Gateway
- relational DB -> RDS
- AWS MySQL/PostgreSQL relational engine -> Aurora
- NoSQL key-value -> DynamoDB
- cache -> ElastiCache
- graph -> Neptune
- document DB -> DocumentDB
- DNS -> Route 53
- CDN -> CloudFront
- dedicated network link -> Direct Connect
- encrypted tunnel -> VPN
- network hub -> Transit Gateway
- private service connectivity -> PrivateLink
- global application network optimization -> Global Accelerator
- managed APIs -> API Gateway
- SQL on S3 -> Athena
- ETL/catalog -> Glue
- Spark/Hadoop -> EMR
- streaming -> Kinesis
- dashboards -> QuickSight
- warehouse -> Redshift
- queue -> SQS
- pub/sub -> SNS
- event bus -> EventBridge
- workflow -> Step Functions
- email -> SES
- contact center -> Connect
- text to speech -> Polly
- speech to text -> Transcribe
- NLP -> Comprehend
- intelligent search -> Kendra
- image/video AI -> Rekognition
- document extraction -> Textract
- ML platform -> SageMaker AI

# Official reference

https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
