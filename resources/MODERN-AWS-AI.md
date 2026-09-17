# Modern AWS AI & Generative AI

This page keeps the repository current **without polluting CLF-C02 exam scope**.

---

# Part 1 — CLF-C02 CORE

The current official CLF-C02 in-scope Machine Learning list explicitly includes:

- **Amazon Comprehend** — natural-language processing and text insights
- **Amazon Kendra** — intelligent enterprise search
- **Amazon Lex** — conversational interfaces / bots
- **Amazon Polly** — text to speech
- **Amazon Q** — AWS generative-AI assistant family
- **Amazon Rekognition** — image/video analysis
- **Amazon SageMaker AI** — build, train, and deploy machine-learning models
- **Amazon Textract** — extract text, forms, and tables from documents
- **Amazon Transcribe** — speech to text
- **Amazon Translate** — language translation

For CLF-C02, learn these at **recognition level**: what each service does and which use case should trigger it.

Official scope:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/clf-02-in-scope-services.html

Official Domain 3 task statement:
https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02-domain3.html

---

# Part 2 — SUPPLEMENTAL: modern AWS GenAI

The services and concepts below are valuable current AWS knowledge, but this repository does **not** label them as CLF-C02 requirements unless AWS adds them to the current exam scope.

## Amazon Bedrock

Amazon Bedrock is AWS's managed platform for building generative-AI applications using foundation models.

Useful concepts to recognize beyond CLF-C02:
- foundation models
- model inference
- model choice
- prompt engineering
- generative-AI application development

Official docs:
https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html

## Foundation models

A foundation model is a large pretrained model that can be adapted or prompted for many downstream tasks such as text generation, reasoning, summarization, extraction, coding, image generation, and multimodal applications.

Do not memorize individual model names for CLF-C02.

## Retrieval-Augmented Generation (RAG)

RAG improves generated answers by retrieving relevant information from a data source and supplying that context to the model.

Think:

`user question -> retrieve relevant data -> add context -> model generates grounded response`

This is a modern GenAI concept, not a current CLF-C02 requirement.

## Amazon Bedrock Knowledge Bases

Knowledge Bases provide managed retrieval capabilities for building RAG applications over enterprise or proprietary data.

Official docs:
https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html

## Amazon Bedrock Guardrails

Guardrails provide configurable safeguards for generative-AI inputs and outputs, including controls around harmful content, denied topics, sensitive information, and other policies.

Official docs:
https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails.html

## Amazon Bedrock AgentCore

AgentCore is AWS's current platform for building, deploying, and operating AI agents securely at scale. AWS documents it as framework- and model-flexible, with services for agent runtime, identity, gateways, memory, observability, and other agent infrastructure.

Official docs:
https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html

### Important 2026 transition

AWS renamed the earlier Amazon Bedrock Agents experience to **Amazon Bedrock Agents Classic**. AWS states that Agents Classic is no longer open to new customers from **July 30, 2026**, and recommends **Amazon Bedrock AgentCore** for new agent-development workloads.

Amazon Bedrock itself remains supported; this transition applies to the Agents Classic orchestration layer.

Official transition notice:
https://docs.aws.amazon.com/bedrock/latest/userguide/agents-classic-maintenance-mode.html

---

# Part 3 — Where to go after CLF-C02

If AI/ML and generative AI interest you, the most natural next foundational credential is:

## AWS Certified AI Practitioner

Official page:
https://aws.amazon.com/certification/certified-ai-practitioner/

AWS describes it as a foundational certification focused on:
- AI concepts
- machine learning
- generative AI
- AWS AI services and use cases

That exam goes far deeper into AI than Cloud Practitioner. AWS itself notes that Cloud Practitioner contains only one task statement specifically related to AI/ML, while AI Practitioner is centered on AI/ML and generative AI.

---

# Fast mental map

| Need | Current AWS concept/service |
|---|---|
| Build/train/deploy ML models | SageMaker AI |
| Generative-AI foundation-model platform | Amazon Bedrock |
| Ground model responses in private data | Bedrock Knowledge Bases / RAG |
| Add safety controls around GenAI | Bedrock Guardrails |
| Build and operate agentic AI | Bedrock AgentCore |
| AWS generative-AI assistant family | Amazon Q |
| NLP/text insights | Comprehend |
| Enterprise search | Kendra |
| Conversational bot | Lex |
| Text to speech | Polly |
| Speech to text | Transcribe |
| Image/video analysis | Rekognition |
| Document extraction | Textract |

## Scope reminder

**Bedrock, Knowledge Bases, Guardrails, RAG, and AgentCore are supplemental here.**

Do not spend CLF-C02 cram time learning their implementation details unless the official exam scope changes.

**Last validated:** 2026-09-17
