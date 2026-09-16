# 06 — Service Recognition Cheat Sheet

Use this for rapid recall. Read the requirement, cover the answer, and answer within 3 seconds.

| Requirement / trigger phrase | AWS service / concept |
|---|---|
| Virtual machine/server | Amazon EC2 |
| Run code without managing servers | AWS Lambda |
| Automatically add/remove EC2 capacity | Auto Scaling |
| Distribute traffic across targets | Elastic Load Balancing |
| Store container images | Amazon ECR |
| AWS-native container orchestration | Amazon ECS |
| Managed Kubernetes | Amazon EKS |
| Serverless containers | AWS Fargate |
| Batch computing jobs | AWS Batch |
| Simple VPS/small app hosting | Amazon Lightsail |
| Upload app code, managed environment | Elastic Beanstalk |
| AWS infrastructure on premises | AWS Outposts |
| Object storage | Amazon S3 |
| EC2 persistent block disk | Amazon EBS |
| Temporary host-attached block storage | Instance Store |
| Shared managed filesystem | Amazon EFS |
| Specialized managed filesystems | Amazon FSx |
| Long-term archive | S3 Glacier classes |
| Hybrid on-prem/cloud storage | AWS Storage Gateway |
| Centralized backups | AWS Backup |
| Disaster recovery replication/recovery | AWS Elastic Disaster Recovery |
| Managed relational DB | Amazon RDS |
| AWS MySQL/PostgreSQL-compatible relational DB | Amazon Aurora |
| Serverless NoSQL key-value/document DB | Amazon DynamoDB |
| In-memory cache | Amazon ElastiCache |
| MongoDB-compatible document DB | Amazon DocumentDB |
| Graph DB | Amazon Neptune |
| Data warehouse | Amazon Redshift |
| SQL directly against data in S3 | Amazon Athena |
| ETL/data integration/catalog | AWS Glue |
| Spark/Hadoop big data | Amazon EMR |
| Real-time streaming data | Amazon Kinesis |
| BI dashboards | Amazon QuickSight |
| Search/log analytics | Amazon OpenSearch Service |
| Virtual private network in AWS | Amazon VPC |
| DNS | Amazon Route 53 |
| CDN/content caching at edge | Amazon CloudFront |
| Managed API front door | Amazon API Gateway |
| Dedicated customer-to-AWS network connection | AWS Direct Connect |
| Encrypted network tunnel | AWS VPN |
| Connect many VPCs/networks through hub | AWS Transit Gateway |
| Private service connectivity | AWS PrivateLink |
| Improve global network path to app endpoints | AWS Global Accelerator |
| Resource-level stateful firewall | Security Group |
| Subnet-level stateless control | Network ACL |
| AWS permissions/identities | IAM |
| Central workforce access to accounts/apps | IAM Identity Center |
| End-user app sign-up/sign-in | Amazon Cognito |
| Reusable policy created/maintained by AWS | AWS managed IAM policy |
| Reusable policy customer creates and edits | Customer managed IAM policy |
| Policy embedded directly in one identity | Inline IAM policy |
| Audit IAM user password/key/MFA status | IAM credential report |
| Manage encryption keys | AWS KMS |
| Dedicated HSM | AWS CloudHSM |
| Store credentials/API secrets with secret-management features | AWS Secrets Manager |
| Store application/configuration parameters; encrypted SecureString option | Systems Manager Parameter Store |
| TLS certificates | AWS Certificate Manager |
| Metrics/logs/alarms | Amazon CloudWatch |
| AWS API/account audit trail | AWS CloudTrail |
| Resource configuration history/rules | AWS Config |
| Audit evidence collection | AWS Audit Manager |
| AWS compliance reports/agreements | AWS Artifact |
| Threat detection | Amazon GuardDuty |
| Vulnerability management | Amazon Inspector |
| Sensitive/PII discovery in S3 | Amazon Macie |
| Investigate security findings | Amazon Detective |
| Central security findings/posture | AWS Security Hub |
| Filter malicious HTTP(S) requests | AWS WAF |
| DDoS protection | AWS Shield |
| Centrally manage firewall policies | AWS Firewall Manager |
| Share supported resources across accounts | AWS RAM |
| Multi-account management/SCPs/billing | AWS Organizations |
| Governed multi-account landing zone | AWS Control Tower |
| Queue/decouple producers and consumers | Amazon SQS |
| Pub/sub fan-out notifications | Amazon SNS |
| Event bus/routing | Amazon EventBridge |
| Workflow/state-machine orchestration | AWS Step Functions |
| Application email | Amazon SES |
| Cloud contact center | Amazon Connect |
| Infrastructure as Code | AWS CloudFormation |
| Fleet/patching/automation operations | AWS Systems Manager |
| Service limits/quotas | Service Quotas |
| AWS events affecting account/resources | AWS Health Dashboard / AWS Health |
| Best-practice recommendations | AWS Trusted Advisor |
| Right-sizing recommendations | AWS Compute Optimizer |
| Approved governed cloud products | AWS Service Catalog |
| Track software licenses | AWS License Manager |
| Review against Well-Architected | AWS Well-Architected Tool |
| Migrate database data | AWS DMS |
| Convert DB schema | AWS SCT |
| Discover on-prem migration inventory | Application Discovery Service |
| Migrate servers/apps | Application Migration Service |
| Track migrations | Migration Hub |
| Build migration cost/business case | Migration Evaluator |
| Offline/physical large-data transfer | AWS Snow Family |
| ML build/train/deploy | Amazon SageMaker AI |
| NLP/sentiment/entities | Amazon Comprehend |
| Intelligent enterprise search | Amazon Kendra |
| Chatbot/conversational AI | Amazon Lex |
| Text to speech | Amazon Polly |
| Speech to text | Amazon Transcribe |
| Language translation | Amazon Translate |
| Image/video analysis | Amazon Rekognition |
| Extract forms/tables/text from documents | Amazon Textract |
| Generative AI assistant family | Amazon Q |
| IoT device connectivity/messaging | AWS IoT Core |
| Build/test source code | AWS CodeBuild |
| CI/CD pipeline orchestration | AWS CodePipeline |
| Distributed tracing | AWS X-Ray |
| Cloud virtual desktop | Amazon WorkSpaces |
| Stream desktop applications | Amazon AppStream 2.0 |
| Secure browser access | WorkSpaces Secure Browser |
| Web/mobile frontend platform | AWS Amplify |
| Managed GraphQL API | AWS AppSync |
| Estimate future AWS bill | AWS Pricing Calculator |
| Analyze past/current costs/trends | AWS Cost Explorer |
| Cost threshold/alert | AWS Budgets |
| Detailed billing dataset | AWS Cost and Usage Report |
| Categorize costs by team/project | Cost allocation tags |
| Third-party AWS software/services | AWS Marketplace |
| Community AWS Q&A | AWS re:Post |
| AWS expert transformation/consulting engagement | AWS Professional Services |
| AWS technical solution guidance | AWS Solutions Architects |
| Consulting/technology partner ecosystem | AWS Partner Network |
| Third-party software vendor | APN Independent Software Vendor (ISV) |
| External integration/migration/consulting implementer | APN consulting/system integrator |
| Report abuse/misuse involving AWS resources | AWS Trust & Safety |

# Framework flashcards

| Trigger | Answer |
|---|---|
| Workload best-practice framework | AWS Well-Architected Framework |
| Organizational cloud transformation/readiness | AWS Cloud Adoption Framework |
| Operate/improve workloads | Operational Excellence |
| Protect systems/data | Security |
| Recover/perform correctly | Reliability |
| Efficient performance as demand/tech changes | Performance Efficiency |
| Lowest cost for required business value | Cost Optimization |
| Reduce environmental/resource impact | Sustainability |

# EC2 pricing flashcards

| Trigger | Model |
|---|---|
| No commitment/unpredictable | On-Demand |
| Predictable commitment | Reserved Instances / Savings Plans |
| Interruptible, low-cost batch | Spot |
| RI can be exchanged for different config | Convertible RI |
| RI discount across AZs in Region, no capacity reservation | Regional RI |
| RI reserves capacity in one AZ | Zonal RI |
| Physical host dedicated to customer | Dedicated Host |
| Dedicated hardware without host-level control | Dedicated Instance |
| Guarantee EC2 capacity | Capacity Reservation |

# Root-user flashcards

Recognize that root credentials can be required for high-privilege account tasks such as:
- changing standalone-account root email/password/access keys
- closing a standalone AWS account
- restoring IAM admin permissions after lockout
- activating IAM access to Billing and Cost Management

Do **not** use root routinely. AWS Organizations can centrally perform some privileged actions for member accounts.

# 2026 Support terminology

Current live plans:
- Basic
- Business Support+
- Enterprise Support
- Unified Operations

CLF-C02 Domain 4 still includes legacy/transitional names in examples:
- Developer Support
- Business Support
- Enterprise On-Ramp
- Enterprise Support

Developer Support, legacy Business Support and Enterprise On-Ramp are scheduled to retire January 1, 2027. For the exam, understand support levels/resources and recognize both generations of names.
