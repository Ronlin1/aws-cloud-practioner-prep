# Public AWS Cloud Practitioner Prep Repository Refresh Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Convert the repository into a polished, public, privacy-safe, current CLF-C02 study resource with a beautiful README, validated official-resource library, stronger modern AWS AI coverage, and clear exam-vs-supplemental boundaries.

**Architecture:** Keep the exam-first root study files and `practice/` structure. Add a focused `resources/` directory for official AWS links, Skill Builder, modern AI/GenAI, community resources, and validation notes. All public-facing content must be generic, source-traceable, concise, and explicit about what is and is not CLF-C02 exam scope.

**Tech Stack:** GitHub Markdown, official AWS documentation, AWS Skill Builder, GitHub repository content.

**Spec:** `docs/superpowers/specs/2026-09-17-public-repo-refresh-design.md`

## Global Constraints

- Keep CLF-C02 task statements and official AWS scope as the source of truth.
- Remove current-branch personal/project/employer/location references and unnecessary PII.
- Do not use exam dumps or leaked-question claims.
- Clearly label Amazon Bedrock, AgentCore, RAG, and other modern GenAI material as supplemental unless the current CLF-C02 scope explicitly includes them.
- Keep practice percentages as readiness heuristics, not AWS score conversions.
- Preserve the exam-first, fast-revision character of the repository.
- README must state that the repository is independently maintained and not affiliated with AWS.

---

### Task 1: Privacy scrub public content

**Files:**
- Modify: `05-DOMAIN-4-BILLING-PRICING-SUPPORT.md`
- Inspect: all root `.md`, `practice/*.md`, `docs/**/*.md`

**Interfaces:**
- Consumes: current default-branch content.
- Produces: public-safe examples and a documented clean-current-branch state.

- [ ] **Step 1:** Replace known identifying examples `Project=FarmZenith` and `Department=DataEngineering` with generic examples such as `Project=WebApp` and `Department=Engineering`.
- [ ] **Step 2:** Search for known personal names, project names, employer/education/location terms, emails, phone-like strings, and IDs.
- [ ] **Step 3:** Review any matches manually to distinguish real PII from incidental substrings.
- [ ] **Step 4:** Verify current branch no longer contains known personal references.

### Task 2: Redesign the public README

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: root study files, practice files, new `resources/` index.
- Produces: public landing page and navigation.

- [ ] **Step 1:** Rewrite title/subtitle and intro for a public audience.
- [ ] **Step 2:** Add clean GitHub-native badges, exam snapshot, and `Start here` pathways for 48-hour and normal-paced study.
- [ ] **Step 3:** Group repository navigation into Learn, Drill, Practice, Validate, and Go Deeper.
- [ ] **Step 4:** Add source-of-truth, contribution, scope, and non-affiliation sections.
- [ ] **Step 5:** Add a polished one-line repository-description suggestion for GitHub metadata.

### Task 3: Build the validated resources library

**Files:**
- Create: `resources/README.md`
- Create: `resources/OFFICIAL-AWS.md`
- Create: `resources/SKILL-BUILDER.md`
- Create: `resources/MODERN-AWS-AI.md`
- Create: `resources/COMMUNITY-RESOURCES.md`
- Create: `resources/VALIDATION-NOTES.md`

**Interfaces:**
- Consumes: current AWS official pages and vetted community resources.
- Produces: stable public reference library linked from README.

- [ ] **Step 1:** Add trust hierarchy and index.
- [ ] **Step 2:** Add current official exam guide/domain/scope/framework/support links.
- [ ] **Step 3:** Add current Skill Builder/certification-prep entry points and warn against stale direct course IDs.
- [ ] **Step 4:** Add modern AWS AI/GenAI guide separated into CLF-C02 in-scope vs beyond-CLF-C02 material.
- [ ] **Step 5:** Add vetted community-resource page with non-authoritative warning.
- [ ] **Step 6:** Add validation-methodology/date page.

### Task 4: Strengthen current curriculum without scope pollution

**Files:**
- Modify: `04-DOMAIN-3-TECHNOLOGY-SERVICES.md`
- Modify: `06-SERVICE-CHEAT-SHEET.md`
- Modify: `08-LAST-MINUTE-CRAM.md`
- Modify: `09-RESOURCES.md`
- Modify: `11-DEEP-VALIDATION-AUDIT.md`

**Interfaces:**
- Consumes: live CLF-C02 in-scope list and Domain 3 task statements.
- Produces: refreshed AI/ML service coverage and current resource pointers.

- [ ] **Step 1:** Revalidate AI/ML services explicitly listed for CLF-C02.
- [ ] **Step 2:** Ensure Amazon Q and SageMaker AI are represented accurately at recognition level.
- [ ] **Step 3:** Keep Amazon Bedrock/AgentCore/RAG in `resources/MODERN-AWS-AI.md` rather than presenting them as required CLF-C02 content.
- [ ] **Step 4:** Refresh `09-RESOURCES.md` so it points to the new resource library and durable official entry points.
- [ ] **Step 5:** Update validation audit with September 17, 2026 findings.

### Task 5: Public-facing quality and contribution layer

**Files:**
- Create: `CONTRIBUTING.md`
- Create: `DISCLAIMER.md`

**Interfaces:**
- Consumes: public repository positioning.
- Produces: correction/update workflow and legal/scope clarity.

- [ ] **Step 1:** Add concise contribution guidance prioritizing official AWS citations for corrections.
- [ ] **Step 2:** Add exam-integrity rule against dumps/leaked content.
- [ ] **Step 3:** Add independent-maintenance/non-affiliation disclaimer and AWS trademark note.

### Task 6: Final validation

**Files:**
- Inspect all modified/created files.

**Interfaces:**
- Consumes: complete feature branch.
- Produces: evidence-backed readiness for merge.

- [ ] **Step 1:** Fetch all changed files from the feature branch and confirm expected content.
- [ ] **Step 2:** Verify README local links resolve to files that exist.
- [ ] **Step 3:** Search for known PII/project terms and `TODO`/`TBD`.
- [ ] **Step 4:** Recheck official current CLF-C02 in-scope and out-of-scope lists.
- [ ] **Step 5:** Verify Bedrock and AgentCore are never labeled as CLF-C02 requirements.
- [ ] **Step 6:** Verify current support-transition notes remain accurate.
- [ ] **Step 7:** Create a pull request to `main` only after validation passes.
