# 10 — Explicitly Out-of-Scope Services: SKIP FOR THIS 48-HOUR CRAM

AWS publishes an explicit non-exhaustive list of services/features that are out of scope for CLF-C02. Do not spend your limited time learning these unless they are needed to understand an in-scope concept.

Official source:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-out-of-scope-services.html

> AWS says this list is **non-exhaustive and subject to change**. The official task statements remain the primary source of truth.

# Analytics
- Amazon AppFlow
- AWS Clean Rooms
- AWS Data Exchange
- Amazon DataZone
- Amazon MSK
- Amazon Timestream for LiveAnalytics

# Application Integration
- AWS AppFabric
- Amazon Simple Workflow Service

# Business Applications
- Amazon WorkDocs
- Amazon WorkMail

# Compute
- AWS App Runner
- AWS Copilot
- AWS Wavelength

# Cost Management
- AWS Application Cost Profiler
- Amazon DevPay

# Customer Enablement
- AWS Activate
- AWS IQ
- AWS Managed Services (AMS)

# Cloud Financial Management
- AWS Billing Conductor

# Database
- Amazon Keyspaces
- Amazon MemoryDB for Redis OSS
- AWS AppConfig (listed under database in the current exam guide's out-of-scope page)

# Developer Tools
- AWS Application Composer
- AWS CodeArtifact
- AWS CodeDeploy
- Amazon CodeGuru
- AWS CloudShell
- AWS Device Farm

# Game Tech
- Amazon GameLift
- Amazon Lumberyard

# IoT
- AWS IoT Device Defender
- AWS IoT Greengrass
- Amazon Monitron

# Machine Learning
- Amazon Fraud Detector
- Amazon Lookout for Metrics
- Amazon Mechanical Turk
- AWS Panorama
- Amazon Personalize

# Management and Governance
- AWS Chatbot
- Amazon Data Lifecycle Manager
- Amazon Elastic Transcoder
- AWS Launch Wizard

# Media Services
- AWS Elemental Appliances and Software
- AWS Elemental MediaConnect
- AWS Elemental MediaConvert
- AWS Elemental MediaLive
- AWS Elemental MediaPackage
- AWS Elemental MediaStore
- AWS Elemental MediaTailor
- Amazon Interactive Video Service (IVS)

# Migration and Transfer
- AWS Migration Hub Refactor Spaces
- AWS Transfer Family

# Networking and Content Delivery
- AWS Cloud Map
- AWS Network Access Analyzer
- AWS Ground Station
- Amazon VPC Lattice

# Security, Identity, and Compliance
- Amazon Cloud Directory
- AWS Network Firewall

# Robotics
- AWS RoboMaker

# Storage
- Amazon FSx for Lustre

## Important nuance
The broader **Amazon FSx** service family is in scope, while the current guide explicitly lists **Amazon FSx for Lustre** as out of scope. For this exam, recognize FSx as managed file-system capability and do not deep-dive Lustre-specific implementation.

---

# Also explicitly out-of-scope JOB TASKS

AWS says the target candidate is not expected to perform:
- coding
- designing cloud architecture
- troubleshooting
- implementation
- load and performance testing

Therefore, skip deep tutorials on:
- Kubernetes commands
- detailed subnet/route-table labs
- Terraform/CloudFormation coding exercises
- advanced IAM JSON authoring
- application debugging
- performance tuning

You can learn those after the exam.
