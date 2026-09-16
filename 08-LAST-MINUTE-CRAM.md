# 08 — Last-Minute CLF-C02 Cram Sheet

Use this in the final 2–3 hours. Do not start new deep topics.

# Exam facts
- 65 total questions
- 50 scored + 15 unscored
- 90 minutes
- multiple choice and multiple response
- 700/1000 scaled passing score
- no penalty for guessing; unanswered = wrong

# Weighting
- Domain 1 Cloud Concepts: 24%
- Domain 2 Security & Compliance: 30%
- Domain 3 Technology & Services: 34%
- Domain 4 Billing/Pricing/Support: 12%

# Six Well-Architected pillars
**O S R P C S**
- Operational Excellence
- Security
- Reliability
- Performance Efficiency
- Cost Optimization
- Sustainability

# Six CAF perspectives
**B P G P S O**
- Business
- People
- Governance
- Platform
- Security
- Operations

CAF = organization transformation.  
Well-Architected = workload best practices.

# Global infrastructure
- Region = geographic AWS area
- AZ = separate failure domain inside Region
- Edge = close to users/content delivery
- Multi-AZ = high availability
- Multi-Region = DR/global latency/data sovereignty/business continuity

# Core cloud concepts
- scale UP = bigger machine
- scale OUT = more machines
- scalability = ability to grow
- elasticity = grow AND shrink with demand
- agility = provision/change quickly
- high availability = minimize downtime
- fault tolerance = continue despite failure
- DR = recover from major disruption
- economies of scale = cloud-provider scale efficiencies
- rightsizing = match resources to actual need

# Shared Responsibility
AWS = security **OF** cloud.  
Customer = security **IN** cloud.

EC2 customer: guest OS, patching, apps, data, IAM/security configuration.  
RDS/Lambda: AWS manages more underlying platform.

# IAM
- User = identity
- Group = users grouped
- Role = assumable identity / temporary credentials
- Policy = permissions
- least privilege
- protect root, MFA, don't use routinely
- Identity Center = workforce multi-account access
- Cognito = application end users

# Security rapid map
- CloudWatch = metrics/logs/alarms
- CloudTrail = API audit
- Config = configuration history/rules
- Artifact = compliance reports
- Audit Manager = audit evidence
- GuardDuty = threat detection
- Inspector = vulnerabilities
- Macie = sensitive S3 data
- Detective = investigation
- Security Hub = aggregate posture/findings
- WAF = web filtering
- Shield = DDoS
- Firewall Manager = centrally manage firewall policies
- KMS = encryption keys
- CloudHSM = dedicated HSM
- Secrets Manager = credentials/secrets
- ACM = TLS certificates

# Compute
- EC2 = VM
- Lambda = serverless functions
- ELB = distribute traffic
- Auto Scaling = change capacity
- ECR = container images
- ECS = AWS containers
- EKS = Kubernetes
- Fargate = serverless containers
- Batch = batch jobs
- Elastic Beanstalk = app deployment platform
- Lightsail = simple VPS/apps
- Outposts = AWS on premises

# Storage
- S3 = object
- EBS = block/disk
- EFS = shared file
- FSx = specialized file
- Glacier = archive
- Storage Gateway = hybrid storage
- Backup = centralized backups
- Elastic Disaster Recovery = DR

# Databases
- RDS = relational
- Aurora = AWS MySQL/PostgreSQL-compatible relational
- DynamoDB = serverless NoSQL key-value/document
- ElastiCache = cache
- DocumentDB = document DB
- Neptune = graph
- Redshift = warehouse
- DMS = move database data
- SCT = convert schema

# Networking
- VPC = private AWS network
- Security Group = stateful/resource
- NACL = stateless/subnet
- Route 53 = DNS
- CloudFront = CDN/cache
- Direct Connect = dedicated link
- VPN = encrypted tunnel
- Transit Gateway = network hub
- PrivateLink = private service access
- Global Accelerator = global path optimization
- API Gateway = managed APIs

# Analytics
- Athena = SQL on S3
- Glue = ETL/catalog
- EMR = Spark/Hadoop
- Kinesis = streaming
- QuickSight = BI
- Redshift = warehouse
- OpenSearch = search/log analytics

# AI/ML
- SageMaker AI = ML platform
- Comprehend = NLP
- Kendra = intelligent search
- Lex = chatbot
- Polly = text -> speech
- Transcribe = speech -> text
- Translate = translation
- Rekognition = image/video
- Textract = document extraction
- Amazon Q = generative AI assistant family

# Integration
- SQS = queue
- SNS = pub/sub fan-out
- EventBridge = event bus/routing
- Step Functions = workflow
- SES = email
- Connect = contact center

# Management
- CloudFormation = IaC
- Systems Manager = fleet/operations
- Compute Optimizer = rightsizing recommendations
- Trusted Advisor = broad best-practice checks
- Health Dashboard = AWS events affecting account/resources
- Organizations = multi-account + billing + SCP
- Control Tower = governed multi-account landing zone
- Service Catalog = approved deployable products
- Service Quotas = limits

# Migration
- Discovery Service = discover environment
- Application Migration Service = migrate servers/apps
- DMS = DB data
- SCT = DB schema
- Migration Hub = track
- Migration Evaluator = business case
- Snow Family = physical/offline data transfer

# Billing
- On-Demand = flexible/no commitment
- RI/Savings Plans = predictable commitment discount
- Spot = interruptible/cheap
- Dedicated Host = physical host/licensing
- Capacity Reservation = guarantee AZ capacity
- Pricing Calculator = estimate
- Cost Explorer = analyze
- Budgets = alert
- CUR = detailed billing data
- cost allocation tags = split costs by project/team

# Final trap list

If question says...
- “who changed?” -> CloudTrail
- “CPU alert?” -> CloudWatch
- “configuration compliant?” -> Config
- “sensitive PII in S3?” -> Macie
- “DDoS?” -> Shield
- “SQL injection/web requests?” -> WAF
- “queue?” -> SQS
- “fan-out?” -> SNS
- “route events?” -> EventBridge
- “orchestrate steps?” -> Step Functions
- “DNS?” -> Route 53
- “global cached content?” -> CloudFront
- “SQL over S3?” -> Athena
- “ETL?” -> Glue
- “Spark?” -> EMR
- “streaming?” -> Kinesis
- “relational?” -> RDS
- “NoSQL?” -> DynamoDB
- “warehouse?” -> Redshift
- “graph?” -> Neptune
- “shared files?” -> EFS
- “EC2 disk?” -> EBS
- “objects?” -> S3
- “encryption key?” -> KMS
- “secret/password?” -> Secrets Manager
- “TLS cert?” -> ACM
- “estimate cost?” -> Pricing Calculator
- “past spend?” -> Cost Explorer
- “budget alert?” -> Budgets

# Exam behavior
- Read the requirement before the story.
- Eliminate wrong service categories first.
- “Least operational overhead” often points to managed/serverless.
- “Most cost-effective” means meet the requirement first, then optimize cost.
- Multiple-response: count how many answers are requested.
- Never leave blank.
