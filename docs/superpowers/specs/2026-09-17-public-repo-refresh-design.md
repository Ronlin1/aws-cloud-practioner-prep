# Public AWS Cloud Practitioner Prep Repository Refresh — Design

**Date:** 2026-09-17  
**Repository:** `Ronlin1/aws-cloud-practioner-prep`

## Goal

Turn the repository from a personal 48-hour cram workspace into a polished, public, reusable AWS Certified Cloud Practitioner (CLF-C02) study resource that is privacy-safe, visually appealing, explicitly exam-scope-first, and backed by current official AWS sources.

## Public positioning

The repository should feel welcoming and useful to any learner, especially someone with limited preparation time. The README should be inspirational without being personal, make the scope obvious in seconds, and clearly separate:

1. **CLF-C02 exam content** — the authoritative core.
2. **Official AWS preparation resources** — current AWS docs and Skill Builder links.
3. **Modern AWS AI/GenAI learning beyond CLF-C02** — useful, current material that is clearly labeled as supplemental rather than exam scope.
4. **Community resources** — vetted but non-authoritative supplements.

The repository must not imply affiliation with or endorsement by AWS.

## Privacy requirements

The current default branch must contain no personal profile data, personal projects used as identifying examples, personal employer/education/location references, email addresses, phone numbers, IDs, private URLs, or other unnecessary PII.

Known personal reference found during inspection:
- `Project=FarmZenith`
- `Department=DataEngineering`

These will be replaced with generic examples such as:
- `Project=WebApp`
- `Department=Engineering`
- `Environment=Production`

A final privacy scan will search for names, emails, project names, employer/location references, and common PII patterns.

**History limitation:** cleaning the current branch does not erase text from historical Git commits. The GitHub connector used here does not provide a safe repository-history rewrite workflow. The public README will be clean, and a separate note will explain how to purge history locally with `git filter-repo` if historical removal is required.

## Repository structure

Keep the existing exam-focused root files because they make the repo easy to navigate under time pressure.

Add a dedicated `resources/` directory:

```text
resources/
├── README.md
├── OFFICIAL-AWS.md
├── SKILL-BUILDER.md
├── MODERN-AWS-AI.md
├── COMMUNITY-RESOURCES.md
└── VALIDATION-NOTES.md
```

Responsibilities:

- `resources/README.md` — index and trust hierarchy.
- `resources/OFFICIAL-AWS.md` — official exam guide, task statements, technologies/concepts, in-scope/out-of-scope lists, pricing/support/security/framework docs.
- `resources/SKILL-BUILDER.md` — current AWS Skill Builder and certification-prep entry points, prioritizing durable hub links over stale course IDs.
- `resources/MODERN-AWS-AI.md` — current AWS AI/GenAI ecosystem, explicitly separated into `CLF-C02 in scope` and `Beyond CLF-C02` sections.
- `resources/COMMUNITY-RESOURCES.md` — vetted public repositories and optional third-party learning resources, marked non-authoritative.
- `resources/VALIDATION-NOTES.md` — validation date, methodology, important 2026 transitions, and scope caveats.

## README design

The new README should be visually strong using plain GitHub Markdown only, without external generated images or tracking-heavy badges.

Recommended structure:

1. Centered title and concise subtitle.
2. Small set of trustworthy shields/badges for CLF-C02, validation date, exam-first scope, and community resource status.
3. Short inspirational introduction focused on helping learners pass efficiently and understand AWS fundamentals.
4. “Start here” callout with two routes:
   - 48-hour sprint
   - normal-paced study
5. Exam snapshot table with official domain weights.
6. Beautiful repository map grouped by `Learn`, `Drill`, `Practice`, `Validate`, `Go deeper`.
7. “What this repo intentionally does not do” section for implementation-heavy material.
8. Official source-of-truth disclaimer.
9. Contribution guidance inviting corrections when AWS changes scope.
10. Clear “Not affiliated with AWS” footer.

Tone: confident, encouraging, concise, public, and non-personal.

## Curriculum validation strategy

The source-of-truth hierarchy will be:

1. AWS CLF-C02 Exam Guide.
2. Official task-statement pages for Domains 1–4.
3. Official `Technologies and Concepts` page.
4. Official `In-Scope AWS Services` and `Out-of-Scope AWS Services` pages.
5. Current AWS service documentation for scope-sensitive details.
6. AWS Skill Builder / Certification Prep pages.
7. Community material only as supplemental study signal.

Current official exam facts to preserve:
- 65 total questions.
- 50 scored + 15 unscored.
- 90 minutes.
- Multiple choice and multiple response.
- Passing scaled score 700/1000.
- Domain weights: 24% / 30% / 34% / 12%.

## Modern AI design

The public repository should be modern without polluting CLF-C02 scope.

### CLF-C02 AI/ML core

The current official in-scope list includes:
- Amazon Comprehend
- Amazon Kendra
- Amazon Lex
- Amazon Polly
- Amazon Q
- Amazon Rekognition
- Amazon SageMaker AI
- Amazon Textract
- Amazon Transcribe
- Amazon Translate

These remain in the exam-focused notes and cheat sheet.

### Beyond CLF-C02: current AI/GenAI

Create a separate supplemental resource covering current concepts such as:
- Amazon Bedrock
- Foundation models
- Retrieval-Augmented Generation (RAG)
- Bedrock Knowledge Bases
- Bedrock Guardrails
- Amazon Bedrock AgentCore
- SageMaker AI
- Amazon Q family
- AWS Certified AI Practitioner as the next certification path

Important freshness note: official AWS documentation now indicates Bedrock Agents Classic is not open to new customers and points new agentic workloads toward Bedrock AgentCore. The resource must avoid presenting Agents Classic as the default modern path.

None of these supplemental items should be labeled as CLF-C02 exam requirements unless they appear in the current CLF-C02 official scope.

## Content-strengthening rules

For each exam service, retain the compact pattern:

- What it does.
- Exam trigger phrase.
- Common confusion pair.
- What it does not do.

Do not add implementation tutorials, CLI syntax, advanced configuration, architecture labs, or obscure product internals unless they directly support a CLF-C02 task statement.

Where official terminology is transitioning, explain both current and exam-guide terminology. This includes AWS Support plan changes during 2026.

## Practice strategy

Keep all practice questions original and scenario-based.

Maintain:
- weighted 50-question mock aligned to official domain weights.
- targeted-gap drill for explicit task-statement details.

Do not use exam dumps, leaked questions, or claims of “real exam questions.”

Add a public-facing note that practice percentages are readiness heuristics only and do not convert directly to AWS scaled scores.

## Validation and QA

Before completion:

1. Fetch and re-check all modified files from the current default branch.
2. Confirm all root README links point to existing repository files.
3. Search current branch for:
   - personal names
   - email patterns
   - known personal project/employer/location terms
   - obvious phone/ID patterns
   - `TODO` / `TBD`
4. Verify official source links resolve to current AWS pages.
5. Confirm Bedrock content is labeled `Beyond CLF-C02` unless AWS scope changes.
6. Confirm current CLF-C02 in-scope AI list still includes Amazon Q and SageMaker AI and does not list Amazon Bedrock.
7. Confirm no out-of-scope service is presented as required exam content.
8. Confirm README wording does not claim AWS affiliation or guaranteed exam success.

## Success criteria

The refreshed repository is successful when a new learner can open the README and, within one minute, understand:

- what CLF-C02 tests,
- what to study first,
- where the official AWS links are,
- where to practice,
- what is exam scope versus supplemental modern AWS learning,
- and that the repository is current, public, privacy-safe, and independently maintained.
