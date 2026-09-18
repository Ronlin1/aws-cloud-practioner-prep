# CLF-C02 Targeted Gap Drill — Answers

**Validation refresh:** 2026-09-18. These explanations were rechecked against the current CLF-C02 task statements, in-scope service list, IAM/root-user guidance, Systems Manager/Secrets Manager documentation, EC2 Reserved Instance documentation, AWS Billing, and current AWS Support resources.

## Security, IAM and compliance

**1. B — Customer managed policy**  
Customer managed policies are reusable standalone policies that the customer creates and can edit. AWS managed policies are maintained by AWS; inline policies are embedded directly in one identity.

**2. C — AWS creates and maintains it**  
AWS managed policies are reusable managed policies created and maintained by AWS.

**3. B — IAM credential report**  
The credential report lists IAM users and credential status including passwords, access keys and MFA information. It is useful for audit and compliance reviews.

**4. A — IAM account password policy**  
The IAM account password policy controls password requirements for IAM users. It does not govern the root-user password or access keys.

**5. B — Closing the standalone AWS account**  
Closing a standalone account is a current example of a task that requires root credentials. AWS Organizations can centrally close member accounts and can centrally perform some privileged root actions, so account context matters.

**6. B — AWS Secrets Manager**  
Secrets Manager is purpose-built for credentials/secrets and supports automatic rotation. Current Systems Manager guidance recommends Secrets Manager for database credentials, API keys, tokens and other secrets that need dedicated secret-management controls.

**7. A — Systems Manager Parameter Store**  
Parameter Store is designed for centralized configuration and key-value parameters and supports encrypted `SecureString` values with KMS. For credentials/secrets that need automatic rotation or dedicated secret-management features, prefer Secrets Manager.

**8. C — AWS CloudTrail**  
CloudTrail records AWS API/account activity, including the identity and API event.

**9. A — AWS Config**  
Config tracks resource configurations/configuration changes and can evaluate resources against rules.

**10. A — Federation**  
Federation lets users authenticate with an external identity provider and obtain temporary AWS access rather than requiring separate long-term IAM user credentials.

## Deploying, operating and technology

**11. A — AWS Management Console**  
For a one-time/manual task where a graphical interface is preferred, the Console is appropriate.

**12. B — Infrastructure as Code with CloudFormation**  
Repeatable infrastructure should be automated and represented consistently. CloudFormation is AWS's core Infrastructure as Code service.

**13. A — AWS Systems Manager**  
Systems Manager provides operational capabilities such as patching, inventory, automation and remote management.

**14. A — AWS Service Catalog**  
Service Catalog lets organizations create/govern approved products that users can provision. Marketplace is a marketplace for third-party and other offerings, not the same governance function.

**15. A — AWS License Manager**  
License Manager helps track and manage software-license usage.

**16. A — AWS X-Ray**  
X-Ray provides distributed tracing to follow requests across services and investigate latency/errors.

**17. B — Amazon AppStream 2.0**  
AppStream 2.0 streams applications. WorkSpaces provides cloud virtual desktops.

**18. A — AWS AppSync**  
AppSync provides managed GraphQL APIs and real-time synchronization capabilities. It remains explicitly listed in the current CLF-C02 in-scope service list.

## Billing, pricing and cost management

**19. B — Zonal Reserved Instance**  
A Zonal RI reserves capacity in the chosen Availability Zone. A Regional RI does not reserve capacity.

**20. B — Its discount can apply across AZs in the selected Region**  
Regional RIs provide Availability Zone flexibility. Eligible Linux/Unix default-tenancy Regional RIs can also provide instance-size flexibility.

**21. C — Convertible**  
Convertible RIs can be exchanged for another Convertible RI with a different configuration, subject to AWS value rules. Standard RIs cannot be exchanged in that way.

**22. B — It can be shared with eligible linked accounts according to sharing settings**  
Current AWS Billing preferences support organization-wide, prioritized-group, restricted-group and account-level control of RI/Savings Plans discount sharing. Under organization-wide or applicable group sharing, the purchasing account's matching usage is considered first and remaining eligible discount benefit can be shared.

**23. B — It reserves capacity in the selected AZ for the owning account**  
Do not confuse billing-discount sharing with capacity sharing. AWS EC2 documentation states that a Zonal RI's capacity reservation is only for the owning account and cannot be shared with other accounts, even though the RI billing discount can be applied across linked accounts under consolidated billing rules.

**24. A — AWS-generated and user-defined**  
These are the two cost-allocation tag types.

**25. A — Activate them for cost allocation**  
Cost allocation tags need activation in Billing/Cost Management before they appear in supported cost-allocation reporting/analysis.

**26. B — Inbound often free; outbound/cross-Region may incur charges**  
Transfer pricing depends on service/path/Region. Never assume all AWS network transfer is free.

## Support, partners and customer resources

**27. A — AWS Partner Network (APN)**  
APN is the ecosystem for AWS consulting and technology partners. System integrators/consulting partners can help with migrations and implementations.

**28. A — AWS Marketplace**  
Marketplace is where customers discover/procure third-party software and other offerings with AWS-integrated purchasing/billing capabilities in supported scenarios.

**29. A — AWS Health Dashboard / AWS Health**  
AWS Health shows AWS events that may affect the customer's account/resources. CloudWatch monitors workload metrics/logs/alarms.

**30. A — AWS Trust & Safety**  
Trust & Safety is the relevant AWS resource for reporting abuse or misuse of AWS resources.

## Coverage-completion drill

**31. B — Amazon SageMaker AI**  
SageMaker AI is the current in-scope AWS service for building, training and deploying machine-learning models. Domain 3 explicitly uses SageMaker AI as an AI/ML example.

**32. C — Amazon Q**  
Amazon Q is explicitly present in the current CLF-C02 Machine Learning service list. For this exam, recognition of the service family and its generative-AI assistant role is sufficient. Amazon Bedrock is useful modern AWS knowledge but is not currently on the explicit CLF-C02 in-scope service list.

**33. D — Amazon QuickSight**  
QuickSight is AWS's business-intelligence and visualization service. Kinesis is for streaming data; ECR is a container registry; CloudHSM provides dedicated hardware security modules.

**34. B — Amazon EventBridge**  
EventBridge is an event bus/router that matches events against rules and sends them to targets. SQS is a queue; SNS is publish/subscribe; Step Functions orchestrates workflows.

**35. C — AWS Step Functions**  
Step Functions coordinates multi-step workflows/state machines, including sequences involving Lambda and other AWS services.

**36. B — AWS Control Tower**  
Control Tower helps set up and govern a multi-account AWS landing zone with guardrails and AWS best-practice controls. Organizations provides the underlying multi-account structure/governance capabilities but is not the same turnkey landing-zone service.

**37. D — Amazon API Gateway**  
API Gateway is the managed API front door for creating, publishing, securing and managing APIs. It commonly integrates with Lambda in serverless applications.

**38. B — Deploy redundant resources across multiple Availability Zones in the Region**  
Multi-AZ design improves availability against an Availability Zone failure while keeping the workload in one Region.

**39. A and C — Data residency/regulatory requirements; latency/proximity to users**  
Common Region-selection considerations include legal/data-residency requirements, proximity/latency, service availability and pricing. The other options listed are account configuration choices, not Region-selection drivers.

**40. C — AWS Support Center**  
Support Center is the AWS resource used to create and manage support cases according to the customer's support entitlement. AWS re:Post is community knowledge/Q&A; AWS Health is for account/resource-relevant AWS events.

---

# What a miss means

- 1–4, 10 -> IAM/access fundamentals
- 5 -> root-user task recognition
- 6–7 -> Secrets Manager vs Parameter Store
- 8–9 -> CloudTrail vs Config
- 11–12 -> one-time vs repeatable operations
- 13–18 -> Domain 3 management/developer/end-user/frontend services
- 19–23 -> Reserved Instance flexibility/Organizations behavior
- 24–26 -> cost allocation/data transfer
- 27–30, 40 -> Domain 4.3 support/partner/customer resources
- 31–33 -> AI/ML and analytics
- 34–35 -> application integration
- 36 -> multi-account governance
- 37 -> networking/API services
- 38–39 -> global infrastructure and Region/AZ selection

If you score below **32/40**, revisit only the matching sections before doing another full mock. This threshold is a study heuristic only, not an AWS scaled-score conversion.

## Official validation references

- CLF-C02 exam guide: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html
- Domain 2: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain2.html
- Domain 3: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html
- Domain 4: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain4.html
- In-scope services: https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html
- Root-user guidance: https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html
- Parameter Store: https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html
- Secrets Manager rotation: https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html
- Regional vs Zonal RIs: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/reserved-instances-scope.html
- RI/Savings Plans sharing: https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ri-turn-off.html
- Current AWS Support plans: https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html
