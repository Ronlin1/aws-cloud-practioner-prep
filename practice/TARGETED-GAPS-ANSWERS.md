# CLF-C02 Targeted Gap Drill — Answers

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
Closing a standalone account is a common root-level task. AWS Organizations can centrally perform some privileged actions for member accounts, so read account context carefully.

**6. B — AWS Secrets Manager**  
Secrets Manager is purpose-built for credentials/secrets and supports features such as rotation. AWS recommends it for database credentials, API keys and tokens.

**7. A — Systems Manager Parameter Store**  
Parameter Store is designed for configuration and key-value parameters and supports encrypted `SecureString` values with KMS. For credentials/secrets needing dedicated secret-management features, prefer Secrets Manager.

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
AppStream streams applications. WorkSpaces provides cloud virtual desktops.

**18. A — AWS AppSync**  
AppSync provides managed GraphQL APIs and real-time synchronization capabilities.

## Billing, pricing and cost management

**19. B — Zonal Reserved Instance**  
A Zonal RI reserves capacity in the chosen Availability Zone. A Regional RI does not reserve capacity.

**20. B — Its discount can apply across AZs in the selected Region**  
Regional RIs provide Availability Zone flexibility. Eligible Linux/Unix default-tenancy regional RIs can also provide instance-size flexibility.

**21. C — Convertible**  
Convertible RIs can be exchanged for another Convertible RI with a different configuration, subject to AWS value rules. Standard RIs cannot be exchanged in that way.

**22. B — It can be shared with eligible linked accounts according to sharing settings**  
AWS Organizations billing settings can share eligible RI/Savings Plans discount benefits across linked accounts. The purchasing account's matching usage is considered first.

**23. B — It reserves capacity in the selected AZ for the owning account**  
Do not confuse discount sharing with capacity sharing. A Zonal RI's capacity-reservation benefit belongs to the owning account.

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

---

# What a miss means

- 1–4, 10 -> IAM/access fundamentals
- 5 -> root-user task recognition
- 6–7 -> Secrets Manager vs Parameter Store
- 8–9 -> CloudTrail vs Config
- 11–12 -> one-time vs repeatable operations
- 13–18 -> lower-frequency Domain 3 service recognition
- 19–23 -> Reserved Instance flexibility/Organizations
- 24–26 -> cost allocation/data transfer
- 27–30 -> Domain 4.3 support/partner resources

If you score below 24/30, revisit only the matching sections before doing another full mock.