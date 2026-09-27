# Historical Privacy Rewrite Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Remove the already-identified personal/project labels from all normal-branch-reachable Git history while preserving normal GitHub author attribution and leaving the current `main` tree unchanged.

**Architecture:** Perform a selective Git-history rewrite. First inventory every reachable branch tip and every historical tree containing the private target labels, then recreate only dirty trees and all descendant commits with rewritten parents. Build and verify the entire replacement graph before force-moving any existing branch ref; move `main` last and retain rollback SHAs until post-rewrite verification completes.

**Tech Stack:** Git/Git object model, GitHub REST/Git Data APIs through the connected GitHub tool, read-only local mirror analysis where useful, Markdown verification records kept outside the repository during execution.

**Spec:** `docs/superpowers/specs/2026-09-27-history-privacy-rewrite-design.md`

## Global Constraints

- Preserve normal GitHub author identity; do not anonymize author/committer names or the repository owner.
- Do not change current study content, practice questions, README wording, or resource material.
- The pre-rewrite `main` tree SHA is `c2ce0dcf9f1b617790b373cf072bf95edd082d4f`; rewritten `main` must use this exact tree SHA.
- Do not repeat the private target labels in new repository files, commit messages, branch names, or public audit notes.
- Keep target values only in execution memory / private tool state; if a local helper needs them, pass them as environment variables rather than writing them into the repository.
- The approved generic replacement values are `Project=WebApp` and `Department=Engineering`.
- Preserve commit messages and merge-parent order where supported by the GitHub write interface.
- Accept that rewritten commits can have new timestamps/signature state because the available GitHub commit-creation interface does not expose exact preservation of all original metadata.
- No existing branch ref may move until the complete replacement graph and old-to-new mapping pass verification.
- Save rollback data outside the repository only; do not commit an old-SHA rollback manifest to the public repo.
- If selective reconstruction cannot preserve the required graph/content invariants, stop. Do not fall back to a fresh-history reset without a new explicit design approval.

## Fixed branch inventory at planning time

| Branch | Current tip |
|---|---|
| `main` | `33d64b3256d2919f2c1982dbb3f09046f73df14d` |
| `practice-validation-2026-09-18` | `34703c06d9e51474f4cec0cac2c20dbef3f741a8` |
| `public-exam-experience-2026-09-26` | `c16a4d3281baf2ef79ff22942672dfcd216d10b3` |
| `public-refresh-2026-09-17` | `f695a9baacd64535283e4a7b254b55f025f0cab3` |
| `repo-validation-fixes-2026-09-26` | `6cbbed12e3a7273e793ed856c597d9be351dabb0` |
| `history-privacy-rewrite-spec-2026-09-27` | planning branch; re-read its tip immediately before execution because this plan commit advances it |

Before execution, re-list branches. Any new or moved branch means the inventory must be refreshed before proceeding.

## Review Focus

1. **A branch moves during execution:** abort before any force-update and rebuild the mapping from the new tips; never overwrite unseen work.
2. **A dirty tree is missed:** the historical target scan must cover every commit reachable from every normal branch, not just `main`.
3. **A merge is accidentally linearized:** every recreated merge commit must have the same number and order of parents after old-to-new substitution.
4. **Current content changes:** rewritten `main` must point to the exact pre-rewrite tree SHA `c2ce0dcf9f1b617790b373cf072bf95edd082d4f` before `main` is moved.
5. **Old objects remain public through PR refs/cache:** treat branch rewriting and GitHub object purging as separate stages; do not claim full deletion if an old SHA or merged PR still exposes the dirty object.

---

### Task 1: Freeze and verify the pre-rewrite state

**Files:**
- Read: repository branch refs and commit/tree metadata
- Create outside repo only: `/mnt/data/aws-clf-history-rewrite/preflight.json`

**Interfaces:**
- Consumes: the six planned branch names and their live GitHub refs.
- Produces: immutable execution snapshot with `branch_tips`, `main_tree_sha`, and `captured_at`; later tasks must use this snapshot for concurrency checks and rollback.

- [ ] **Step 1: Re-list all repository branches and compare names/tips to the planning inventory**

Expected: the same six normal branches exist; only `history-privacy-rewrite-spec-2026-09-27` may have advanced because the plan was committed there. If any other branch moved or a new branch appeared, stop and refresh the plan inputs before writing Git objects.

- [ ] **Step 2: Fetch `main` commit metadata and assert its tree SHA**

Assertion:

```text
main tree == c2ce0dcf9f1b617790b373cf072bf95edd082d4f
```

Expected: PASS. If not, stop; current content changed after planning.

- [ ] **Step 3: Record the live branch tips and `main` tree SHA to `/mnt/data/aws-clf-history-rewrite/preflight.json`**

The local file must contain SHAs only plus branch names/timestamp; it must not contain private target strings.

- [ ] **Step 4: Verify branch protection / rules do not block the intended ref update path**

Expected: `main` and the historical feature branches remain movable through the available GitHub ref-update action. If policy changed, stop before creating replacement commits.

- [ ] **Step 5: Commit nothing**

Task 1 is a read-only gate. No repository ref or file changes.

---

### Task 2: Build an exhaustive dirty-history inventory

**Files:**
- Read: all commits/trees reachable from the six branch tips
- Create outside repo only: `/mnt/data/aws-clf-history-rewrite/dirty-inventory.json`

**Interfaces:**
- Consumes: `preflight.json` plus the two approved private target labels from the prior audit, supplied only through private execution state/environment variables.
- Produces: `dirty-inventory.json` with offending commit SHAs, tree SHAs, and file paths; the file must not contain the literal private strings.

- [ ] **Step 1: Traverse every commit reachable from every snapshotted branch tip**

Deduplicate by commit SHA and record for each commit: commit SHA, tree SHA, ordered parent SHAs, commit message, and which branch tips reach it.

- [ ] **Step 2: Search every reachable tree for either private target label**

Use the target labels from private execution state. Do not echo them into a public repo file or commit message.

Expected before rewrite: at least one hit. Known evidence already includes the old cost-allocation-tag example and historical public-refresh planning/specification commits.

- [ ] **Step 3: Record only non-sensitive inventory metadata**

`dirty-inventory.json` must contain:

```json
{
  "offending_commits": [
    {
      "commit_sha": "...",
      "tree_sha": "...",
      "paths": ["relative/path.md"]
    }
  ],
  "earliest_offending_commit": "..."
}
```

No file excerpts or private strings.

- [ ] **Step 4: Verify the known historical evidence is represented**

Assertions:
- the historical cost-allocation-tag file is present in at least one offending tree;
- historical public-refresh design/plan files that repeated the identifying examples are present where reachable;
- the earliest offending commit is an ancestor of every dirty descendant that must be rewritten.

- [ ] **Step 5: Negative-control scan for common secret material**

Scan reachable historical trees for AWS access-key prefixes, private-key headers, obvious secret-access-key assignments, appointment/registration-token markers, and personal email patterns previously checked in the current branch.

Expected: no new high-severity credential finding. If a credential/secret is found, stop and redesign the purge scope before continuing because secret-removal handling is stricter than this two-label rewrite.

---

### Task 3: Build the sanitized tree map without moving refs

**Files:**
- Historical paths identified in `dirty-inventory.json`
- Create outside repo only: `/mnt/data/aws-clf-history-rewrite/tree-map.json`

**Interfaces:**
- Consumes: dirty commit/tree/path inventory and private target-to-generic replacements.
- Produces: `tree_map: old_tree_sha -> clean_tree_sha`; clean original trees may map to themselves, dirty trees map to newly created GitHub trees.

- [ ] **Step 1: For each unique dirty tree, fetch every affected file at that tree**

Expected: fetched content contains at least one target label in each inventoried path.

- [ ] **Step 2: Produce sanitized file content in memory**

Replacement rules:
- replace the approved identifying project label with exactly `Project=WebApp`;
- replace the approved identifying department label with exactly `Department=Engineering`;
- in historical planning/specification text, substitute those same generic examples rather than deleting unrelated process content.

- [ ] **Step 3: Assert the sanitized content contains neither target label**

Expected: zero occurrences of both private targets in every rewritten file.

- [ ] **Step 4: Create new blobs and a replacement tree based on the original tree**

Use the original tree as `base_tree_sha` and replace only inventoried paths. Do not rebuild unrelated entries manually.

- [ ] **Step 5: Fetch each new tree/file and verify exact targeted replacement only**

Assertions:
- target labels absent;
- `Project=WebApp` / `Department=Engineering` present where their corresponding identifying examples existed;
- unrelated surrounding content unchanged;
- file count/modes unchanged except where GitHub's tree API necessarily reuses existing entries.

- [ ] **Step 6: Record `old_tree_sha -> clean_tree_sha` in `tree-map.json`**

No private strings in the map.

---

### Task 4: Recreate the affected commit graph

**Files:**
- Read: original commit metadata for every descendant of `earliest_offending_commit` that is reachable from any snapshotted branch tip
- Create outside repo only: `/mnt/data/aws-clf-history-rewrite/commit-map.json`

**Interfaces:**
- Consumes: `tree-map.json`, original commit graph, and preflight branch tips.
- Produces: `commit_map: old_commit_sha -> new_commit_sha` plus rewritten equivalents for every affected branch tip.

- [ ] **Step 1: Topologically order all commits that require recreation**

A commit requires recreation when either:
- its tree is dirty and mapped to a new tree; or
- at least one parent is recreated.

Every recreated parent must appear before its child.

- [ ] **Step 2: Recreate each non-merge commit**

For each commit:
- tree = `tree_map[old_tree]` if present, else original tree;
- parent = `commit_map[old_parent]` if parent was rewritten, else original parent;
- message = original commit message.

After creation, fetch the new commit and verify its tree, parent, message, and that normal GitHub attribution resolves to the authenticated `Ronlin1` identity when GitHub exposes an author login.

- [ ] **Step 3: Recreate each merge commit with ordered rewritten parents**

For each original merge parent in order, substitute `commit_map[parent]` when rewritten; otherwise preserve the original SHA.

Assertions:
- new merge has the same parent count and equivalent parent order;
- commit message matches the original;
- normal GitHub attribution remains associated with `Ronlin1` when GitHub exposes an author login.

- [ ] **Step 4: Record every `old_commit_sha -> new_commit_sha` immediately**

Persist the SHA-only mapping outside the repo after every successful commit creation so an interrupted session can resume without guessing.

- [ ] **Step 5: Resolve rewritten tips for all six snapshotted branches**

Each old branch tip must either:
- have a new SHA in `commit-map.json`; or
- be proven unaffected and safe to keep unchanged.

Expected for branches descending from the dirty ancestry: rewritten tip exists.

---

### Task 5: Pre-move verification gate

**Files:**
- Read: rewritten GitHub commits/trees by SHA
- Read: `/mnt/data/aws-clf-history-rewrite/*.json`

**Interfaces:**
- Consumes: complete old-to-new tree and commit mappings.
- Produces: explicit PASS/FAIL gate; only PASS authorizes Task 6.

- [ ] **Step 1: Verify rewritten `main` uses the exact original `main` tree**

Assertion:

```text
rewritten_main.tree == c2ce0dcf9f1b617790b373cf072bf95edd082d4f
```

This is the strongest proof that current public content remains byte-for-byte unchanged.

- [ ] **Step 2: Verify every rewritten branch tip's tree against its original tip tree**

Expected: identical tree SHA for branches whose tip content was already clean; if a historical branch tip itself contained target labels, its rewritten tree must differ only by the approved substitutions.

- [ ] **Step 3: Verify every recreated commit's parent topology and attribution**

For each mapping:
- same parent count;
- same parent order after old-to-new substitution;
- same commit message;
- expected tree SHA;
- GitHub author login is `Ronlin1` when the API exposes a linked author.

- [ ] **Step 4: Verify privacy across all rewritten reachable trees**

Use the same private target set from Task 2. Expected: **zero occurrences** across the complete rewritten graph reachable from all rewritten tips.

- [ ] **Step 5: Re-run secret/credential scans on rewritten trees**

Expected: no AWS access-key prefix, private-key header, secret-access-key assignment, exam launch/registration token, or newly introduced personal email/identifier pattern.

- [ ] **Step 6: Concurrency check immediately before ref movement**

Re-read every current branch tip from GitHub and compare to `preflight.json`.

Expected: exact match for all branches. If any branch moved, STOP. Do not force-update any ref; rebuild the affected mapping from the new state.

---

### Task 6: Force-move normal branch refs with rollback protection

**Files:**
- Mutate: six GitHub branch refs only
- Preserve outside repo: `preflight.json` and `commit-map.json`

**Interfaces:**
- Consumes: PASS from Task 5 and rewritten tip mapping.
- Produces: all normal branch refs pointing to the clean rewritten graph.

- [ ] **Step 1: Move historical feature branches first**

Force-update, one at a time, only after checking the current ref still equals its preflight SHA:

1. `practice-validation-2026-09-18`
2. `public-refresh-2026-09-17`
3. `public-exam-experience-2026-09-26`
4. `repo-validation-fixes-2026-09-26`

After each update, fetch the branch and verify it points to the expected rewritten tip.

- [ ] **Step 2: Move the design/plan branch**

Force-update `history-privacy-rewrite-spec-2026-09-27` to its rewritten equivalent so the spec and plan remain available without preserving old ancestry.

- [ ] **Step 3: Re-run the pre-move `main` concurrency check**

Assertion: `main` still equals `33d64b3256d2919f2c1982dbb3f09046f73df14d` (or the exact preflight value if planning inventory was refreshed before execution).

- [ ] **Step 4: Move `main` last**

Force-update `main` to the verified rewritten main SHA.

- [ ] **Step 5: Fetch `main` immediately**

Assertions:
- branch tip = expected rewritten main SHA;
- tree SHA = `c2ce0dcf9f1b617790b373cf072bf95edd082d4f`;
- README/current files still resolve normally.

- [ ] **Step 6: If any branch update fails, stop and assess before continuing**

Do not blindly continue. Because old tips are preserved in `preflight.json`, any already-moved branch can be force-restored to its exact old SHA while those objects remain available.

---

### Task 7: Post-rewrite repository validation

**Files:**
- Read: all six rewritten branch refs, current public files, representative historical commits

**Interfaces:**
- Consumes: rewritten live refs.
- Produces: evidence that branch-level history sanitization succeeded and current content remains intact.

- [ ] **Step 1: List all branches and verify the expected six names remain**

Expected: all six names resolve to their mapped clean tips; no old normal branch ref remains.

- [ ] **Step 2: Re-run target-label searches across all normal branches**

Expected: zero matches.

- [ ] **Step 3: Re-run the current-public-branch PII/secret scan**

Expected: same clean result as before the history rewrite.

- [ ] **Step 4: Verify the renamed canonical repository and current README links**

Expected canonical repository: `Ronlin1/aws-cloud-practitioner-prep`.

- [ ] **Step 5: Verify merged PR pages still render**

Check PRs #1 through #5 for basic accessibility and conversation integrity. Do not require their internal commits to have been rewritten; that is assessed separately in Task 8.

---

### Task 8: Assess GitHub PR refs, old SHA reachability, and final purge requirement

**Files:**
- Read: representative known old dirty commit URLs and merged PR refs/pages
- Create outside repo only if needed: `/mnt/data/aws-clf-history-rewrite/github-support-request.md`

**Interfaces:**
- Consumes: old dirty SHAs from `dirty-inventory.json` and successfully rewritten normal refs.
- Produces: either proof that practical public access is gone or a ready-to-send GitHub Support purge request.

- [ ] **Step 1: Test representative old dirty commit URLs directly**

Record whether GitHub still serves the object by SHA after all normal branches have moved.

- [ ] **Step 2: Inspect merged PR pages/refs for exposure of old dirty objects**

Expected possibilities:
- old objects no longer navigable from PR UI; or
- GitHub's internal `refs/pull/*` / cache still exposes them.

- [ ] **Step 3: Do not claim complete physical deletion if old objects still resolve**

Branch history sanitization and GitHub object garbage collection are distinct.

- [ ] **Step 4: If old dirty objects remain reachable, draft a GitHub Support request outside the repo**

The request should include:
- canonical repository URL;
- statement that normal branch history was rewritten to remove personal information;
- old dirty commit SHAs from the private inventory;
- request to purge cached views and internal PR references to the sensitive objects;
- confirmation that the replacement branch history is already live.

Do not paste the private target strings into the support draft unless GitHub Support explicitly requires them.

- [ ] **Step 5: Final status**

Report one of:
- **Branch-level purge complete; old objects not publicly reachable in checks**, or
- **Branch-level purge complete; GitHub Support purge still required for old PR/object refs**.

---

## Execution completion evidence

Do not call this task complete without all of the following:

- pre-rewrite branch/tip snapshot;
- exact original `main` tree SHA verification;
- exhaustive dirty-tree inventory across every normal branch;
- old-to-new tree and commit mappings kept outside the repo;
- rewritten `main` tree exactly equal to `c2ce0dcf9f1b617790b373cf072bf95edd082d4f`;
- zero target-label matches in rewritten normal-branch history;
- normal GitHub attribution still associated with `Ronlin1` where the API exposes linked authors;
- successful current-branch secret/PII scan;
- all expected branch refs moved and verified;
- explicit PR-ref/old-object reachability result;
- GitHub Support handoff if internal refs/cache still expose dirty objects.
