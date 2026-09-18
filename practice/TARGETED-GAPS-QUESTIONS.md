# CLF-C02 Targeted Gap Drill — 40 Questions

These questions target explicit AWS CLF-C02 task-statement items that are easy to under-study in generic Cloud Practitioner courses or underrepresented in a single domain-weighted mock.

They are **original practice questions**, not exam dumps.

Do not open `TARGETED-GAPS-ANSWERS.md` until you finish.

**Validation refresh:** 2026-09-18.

## Security, IAM and compliance

### 1
An administrator wants a reusable IAM policy that the company can create, edit, version, and attach to multiple identities. Which policy type fits BEST?

A. AWS managed policy  
B. Customer managed policy  
C. Inline policy  
D. Service Control Policy only

### 2
Which statement about an AWS managed IAM policy is correct?

A. It is created and edited by the customer.  
B. It is embedded in exactly one IAM user.  
C. AWS creates and maintains it.  
D. It grants access even if an SCP denies the action.

### 3
A security auditor wants a report showing IAM users, MFA status, password status, and access-key information. Which feature should be used?

A. AWS Config snapshot  
B. IAM credential report  
C. CloudWatch dashboard  
D. AWS Artifact

### 4
A company wants to define minimum password length and complexity requirements for IAM users. Which feature should it configure?

A. IAM account password policy  
B. Security group  
C. KMS key policy  
D. AWS Shield

### 5
Which task is a common example of a task that can require AWS account root credentials for a standalone account?

A. Launching an EC2 instance  
B. Closing the standalone AWS account  
C. Creating an S3 bucket  
D. Reading CloudWatch metrics

### 6
An application needs to store database credentials and automatically rotate them. Which service is the BEST fit?

A. AWS Systems Manager Parameter Store  
B. AWS Secrets Manager  
C. Amazon S3  
D. AWS Artifact

### 7
A team needs a central key-value store for application configuration such as environment names, endpoint URLs, resource IDs, and an encrypted SecureString value. Which service is MOST appropriate?

A. AWS Systems Manager Parameter Store  
B. Amazon Macie  
C. AWS Shield  
D. AWS Audit Manager

### 8
Which service is BEST for answering “Which AWS API call changed this resource, and who made it?”

A. AWS Config only  
B. Amazon CloudWatch  
C. AWS CloudTrail  
D. IAM credential report

### 9
Which service is BEST for answering “What configuration did this AWS resource have, and did it comply with our configuration rule?”

A. AWS Config  
B. CloudTrail  
C. GuardDuty  
D. Artifact

### 10
A company uses a corporate identity provider and wants employees to access AWS without creating separate long-term IAM user credentials for each employee. Which concept is MOST relevant?

A. Federation  
B. S3 lifecycle policies  
C. Spot Instances  
D. Dedicated Hosts

## Deploying, operating and technology

### 11
An administrator needs to create one S3 bucket once and prefers a graphical interface. Which method is MOST suitable?

A. AWS Management Console  
B. CloudFormation is mandatory  
C. CodePipeline  
D. AWS DMS

### 12
A company must repeatedly deploy the same VPC, subnets, and security resources across multiple environments with consistent configuration. Which approach is BEST?

A. Manually recreate everything in the Console each time  
B. Infrastructure as Code with AWS CloudFormation  
C. AWS Artifact  
D. Amazon QuickSight

### 13
Which service is BEST for centrally operating fleets with capabilities such as patching, inventory, automation, and remote management?

A. AWS Systems Manager  
B. AWS CloudTrail  
C. AWS WAF  
D. Amazon Route 53

### 14
Which service helps an organization offer a governed catalog of approved cloud products that users can deploy?

A. AWS Service Catalog  
B. AWS Marketplace  
C. Amazon ECR  
D. AWS Artifact

### 15
Which service helps track and manage software licenses used with AWS resources?

A. AWS License Manager  
B. AWS Budgets  
C. Amazon Macie  
D. AWS Step Functions

### 16
A team wants to trace requests across distributed application components to investigate latency. Which service is MOST appropriate?

A. AWS X-Ray  
B. AWS CloudTrail  
C. AWS Artifact  
D. Amazon Route 53

### 17
Which service is designed to stream desktop applications to users without providing each user a full persistent cloud desktop?

A. Amazon WorkSpaces  
B. Amazon AppStream 2.0  
C. Amazon Connect  
D. AWS Outposts

### 18
Which service provides managed GraphQL APIs and real-time data synchronization capabilities?

A. AWS AppSync  
B. Amazon SNS  
C. Amazon SES  
D. AWS Glue

## Billing, pricing and cost management

### 19
Which Reserved Instance type reserves EC2 capacity in a specific Availability Zone?

A. Regional Reserved Instance  
B. Zonal Reserved Instance  
C. Savings Plan  
D. Spot Instance

### 20
Which statement about a Regional Reserved Instance is correct?

A. It always reserves capacity in one AZ.  
B. Its discount can apply across Availability Zones in the selected Region.  
C. It can only be used for Windows workloads.  
D. It is identical to a Dedicated Host.

### 21
Which Reserved Instance offering class can be exchanged for a different Convertible Reserved Instance configuration of equal or greater value?

A. Spot  
B. Standard  
C. Convertible  
D. Capacity Reservation

### 22
Under AWS Organizations billing preferences, what can happen to an eligible unused Reserved Instance discount benefit after the purchasing account's matching usage is satisfied?

A. It must always expire unused.  
B. It can be shared with eligible linked accounts according to sharing settings.  
C. It automatically converts to AWS credits.  
D. It turns into a Capacity Reservation.

### 23
Which statement is correct about a Zonal Reserved Instance?

A. Its capacity reservation is automatically shared as capacity across all accounts in the organization.  
B. It reserves capacity in the selected Availability Zone for the owning account.  
C. It never provides a billing discount.  
D. It is the same as a Savings Plan.

### 24
AWS cost allocation tags come in which TWO broad types?

A. AWS-generated and user-defined  
B. Public and private  
C. Regional and zonal  
D. Standard and Convertible

### 25
A finance team wants project tags to appear in supported AWS billing reports and cost analysis. What must be done with the relevant cost allocation tags?

A. Activate them for cost allocation  
B. Convert them to security groups  
C. Store them in Secrets Manager  
D. Attach them to CloudFront only

### 26
Which statement about data-transfer pricing is MOST accurate?

A. All network traffic inside and outside AWS is always free.  
B. Data transfer into AWS is often free in many common cases, while outbound and cross-Region transfer can incur charges.  
C. AWS always charges the same transfer rate globally.  
D. Only S3 has data-transfer charges.

## Support, partners and customer resources

### 27
A company needs an external AWS-qualified consulting or technology partner to help implement a migration. Which AWS ecosystem should it use?

A. AWS Partner Network (APN)  
B. AWS Artifact  
C. Amazon Route 53  
D. AWS Budgets

### 28
A company wants to buy third-party software from an independent software vendor with procurement/billing integrated into AWS. Which service is MOST relevant?

A. AWS Marketplace  
B. AWS Service Catalog only  
C. AWS Systems Manager  
D. Amazon Athena

### 29
A company wants to know whether a current AWS service event is affecting its own account resources. Which resource should it check?

A. AWS Health Dashboard / AWS Health  
B. AWS CloudTrail  
C. Amazon Macie  
D. AWS Artifact

### 30
A customer needs to report suspected abuse or malicious activity involving AWS resources. Which AWS resource is MOST appropriate?

A. AWS Trust & Safety  
B. AWS Pricing Calculator  
C. Amazon QuickSight  
D. AWS Config

## Coverage-completion drill

These ten questions close important blueprint gaps that were underrepresented in the original 50-question mock.

### 31
A data science team wants a managed AWS service to build, train, and deploy machine-learning models. Which service is MOST appropriate?

A. Amazon SageMaker AI  
B. Amazon Route 53  
C. AWS Artifact  
D. Amazon SQS

### 32
Which current in-scope AWS service is a generative-AI assistant family for supported AWS and business use cases?

A. Amazon Q  
B. Amazon Textract  
C. Amazon Kinesis  
D. AWS Shield

### 33
A business team wants interactive business-intelligence dashboards and visualizations from cloud data. Which service is MOST appropriate?

A. Amazon QuickSight  
B. Amazon Kinesis  
C. Amazon ECR  
D. AWS CloudHSM

### 34
A company wants to route application events from multiple sources to different targets according to event-matching rules. Which service should it use?

A. Amazon EventBridge  
B. Amazon SQS  
C. Amazon EBS  
D. AWS Artifact

### 35
A serverless application needs to coordinate a sequence of Lambda functions and service actions as a stateful workflow. Which service is MOST appropriate?

A. AWS Step Functions  
B. Amazon SNS  
C. AWS Direct Connect  
D. Amazon EFS

### 36
An enterprise wants to establish and govern a multi-account AWS landing zone using AWS best practices and guardrails. Which service is MOST appropriate?

A. AWS Control Tower  
B. AWS Cost Explorer  
C. Amazon Macie  
D. AWS Batch

### 37
A company needs a managed service to create, publish, secure, and manage APIs that can invoke backend services such as Lambda. Which service should it use?

A. Amazon API Gateway  
B. Amazon Route 53  
C. AWS Storage Gateway  
D. Amazon CloudFront

### 38
A workload must remain available if a single Availability Zone fails, but all resources must stay within one AWS Region. Which design is MOST appropriate?

A. Deploy redundant resources across multiple Availability Zones in the Region  
B. Place all resources in one Availability Zone  
C. Use only one larger EC2 instance  
D. Move the workload to an edge location

### 39 — Select TWO
Which TWO are common factors when selecting an AWS Region for a workload?

A. Data-residency or regulatory requirements  
B. Latency/proximity to users  
C. Whether the account has an IAM password policy  
D. Whether Cost Explorer is enabled  
E. Whether the root user has an access key

### 40
A customer with the appropriate support entitlement needs to create and manage a technical support case with AWS. Which resource should the customer use?

A. AWS Support Center  
B. AWS Artifact  
C. Amazon QuickSight  
D. AWS Pricing Calculator

---

After answering, check `TARGETED-GAPS-ANSWERS.md` and tag every miss by topic.
