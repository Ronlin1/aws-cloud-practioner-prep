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

CAF = organizational transformation/readiness.  
Well-Architected = workload best practices.

# Global infrastructure
- Region = geographic AWS area
- AZ = separate failure domain inside Region
- Edge = close to users/content delivery
- Multi-AZ = high availability/resilience
- Multi-Region = DR/regional resilience/global latency/data sovereignty

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
- Group = collection of users
- Role = assumable identity / temporary credentials
- Policy = permissions
- AWS managed policy = AWS creates/maintains, reusable
- Customer managed policy = customer creates/edits, reusable
- Inline policy = embedded in one identity
- least privilege
- protect root, use MFA, do not use routinely
- IAM credential report = IAM user password/access-key/MFA status
- IAM password policy = complexity/rotation rules for IAM-user passwords
- Identity Center = workforce multi-account access
- Federation = external IdP / temporary AWS access
- Cognito = application end users

## Root-only task examples
For standalone accounts, recognize examples such as:
- change root email/password/access keys
- close the account
- restore IAM admin permissions after lockout
- activate IAM access to Billing and Cost Management

Organizations can centrally perform some privileged actions for member accounts.

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
- Secrets Manager = credentials/secrets, especially rotation/dedicated secret management
- Parameter Store = configuration/key-value parameters, SecureString option
- ACM = TLS certificates

# Compute
- EC2 = VM
- Lambda = serverless functions
- ELB = distribute traffic
- Auto Scaling = change capacity
- ECR = container images
- ECS = AWS-native containers
- EKS = Kubernetes
- Fargate = serverless containers
- Batch = batch jobs
- Elastic Beanstalk = app deployment platform
- Lightsail = simple VPS/apps
- Outposts = AWS on premises

# One-time vs repeatable operations
- one-time visual/manual task -> Console can fit
- repeatable script/API operation -> CLI / SDK / API
- repeatable infrastructure definition -> CloudFormation / IaC

# Storage
- S3 = object
- EBS = block/disk
- EFS = shared file
- Instance Store = ephemeral host-attached block
- FSx = specialized managed file
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
- Amazon Q = generative-AI assistant family

# Integration
- SQS = queue
- SNS = pub/sub fan-out
- EventBridge = event bus/routing
- Step Functions = workflow
- SES = email
- Connect = contact center

# Management
- CloudFormation = IaC
- Systems Manager = fleet/operations + Parameter Store
- Compute Optimizer = rightsizing recommendations
- Trusted Advisor = broad best-practice checks
- Health Dashboard = AWS events affecting account/resources
- Organizations = multi-account + billing + SCPs
- Control Tower = governed multi-account landing zone
- Service Catalog = approved deployable products
- Service Quotas = limits
- License Manager = software-license tracking
- X-Ray = distributed tracing

# End-user/frontend recognition
- WorkSpaces = cloud virtual desktop
- AppStream 2.0 = stream applications
- WorkSpaces Secure Browser = secure browser access
- Amplify = frontend/mobile development/hosting platform
- AppSync = managed GraphQL + real-time sync

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
- Spot = interruptible/low cost
- Dedicated Host = physical host/licensing
- Dedicated Instance = dedicated hardware, less host control
- Capacity Reservation = guarantee capacity; not inherently a discount

## Reserved Instance traps
- Standard RI = less exchange flexibility
- Convertible RI = exchange for different Convertible config of equal/higher value
- Regional RI = discount across AZs in Region; no capacity reservation; eligible size flexibility
- Zonal RI = capacity reservation in one AZ; no AZ/size flexibility
- Organizations can share eligible RI/Savings Plans **discount benefits** according to billing settings
- discount sharing != automatically sharing a zonal RI's capacity reservation

# Cost tools
- Pricing Calculator = estimate
- Cost Explorer = analyze
- Budgets = alert
- CUR = detailed billing data
- cost allocation tags = AWS-generated or user-defined; activate for supported cost reporting

# Support and customer resources
- Documentation = official product docs
- re:Post = community Q&A
- Prescriptive Guidance = patterns/strategies
- Support Center = support cases
- Trusted Advisor = best-practice recommendations
- Health Dashboard / AWS Health = AWS events affecting your resources/account
- Trust & Safety = report abuse/misuse
- Marketplace = third-party software/data/services procurement
- APN = consulting/technology partner ecosystem
- ISV = software vendor
- system integrator/consulting partner = implementation/migration help
- Professional Services = AWS experts for transformations/complex engagements
- Solutions Architects = AWS technical solution guidance

## 2026 Support-plan transition
Current live plans:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

The CLF-C02 Domain 4 page still names legacy/transitional plans such as Developer Support, Business Support and Enterprise On-Ramp. Those legacy plans are scheduled to retire January 1, 2027. Recognize both generations of terminology; do not memorize every price table.

# Final trap list

If question says...
- “who changed?” -> CloudTrail
- “CPU alert?” -> CloudWatch
- “configuration compliant?” -> Config
- “IAM users with MFA/stale access keys?” -> IAM credential report
- “sensitive PII in S3?” -> Macie
- “DDoS?” -> Shield
- “SQL injection/web requests?” -> WAF
- “app config parameter?” -> Parameter Store
- “rotating DB secret?” -> Secrets Manager
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
- “external AWS partner?” -> APN
- “third-party software?” -> Marketplace
- “AWS incident affects my resources?” -> Health Dashboard
- “report abuse?” -> Trust & Safety

# Exam behavior
- Read the requirement before the story.
- Eliminate wrong service categories first.
- “Least operational overhead” often points to managed/serverless.
- “Most cost-effective” means meet the requirement first, then optimize cost.
- Multiple-response: count how many answers are requested.
- Never leave blank.
