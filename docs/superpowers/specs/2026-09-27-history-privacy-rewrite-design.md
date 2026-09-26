# Historical Privacy Rewrite Design

**Date:** 2026-09-27  
**Repository:** `Ronlin1/aws-cloud-practitioner-prep`  
**Status:** Design approved in chat; destructive implementation not yet authorized

## Goal

Remove previously deleted personal/project references from the repository's reachable Git history while preserving normal GitHub author attribution and keeping the current `main` working tree byte-for-byte unchanged.

This is a history-sanitization operation, not a content redesign.

## Scope

### In scope

- Historical file content containing previously identified personal/project labels.
- Historical internal planning/specification files that repeat those labels.
- Descendant commits whose parent SHAs must change because an ancestor is rewritten.
- All normal repository branch refs that still make the affected history reachable.
- Post-rewrite verification of the current `main` tree and all rewritten branch tips.
- Verification of whether merged pull-request refs keep old objects reachable after branch refs are rewritten.

### Out of scope

- Rewriting the repository owner's GitHub identity.
- Rewriting author/committer names or normal GitHub noreply attribution.
- Changing current study content, practice questions, README wording, or resource material.
- Deleting merged pull requests or issue discussions.
- Changing repository visibility.
- Flattening the repository to a single root commit unless selective rewriting proves infeasible.

## Privacy target

The rewrite will remove the known historical personal/project labels already identified during the privacy audit and replace them with the same generic examples used on current `main`.

The rewritten graph must not introduce new personal data while doing so.

The concrete private strings being removed are intentionally not repeated in this public design document.

## Current repository state

At design time, `main` points to the merged validation state from PR #5. The repository also retains several older feature branches created during the public refresh, practice validation, exam-experience publication, and validation-fix work.

Those normal branch refs must be considered together because leaving one branch on the old graph can keep historical objects reachable.

A separate design branch contains this document. It must either be recreated from the rewritten `main` or removed after the rewrite so that it does not retain old ancestry.

## Chosen approach

Use a **selective history rewrite** rather than a fresh-history reset.

The rewrite starts at the earliest commit whose tree contains one of the identified personal/project references. From that point forward:

1. Recreate the affected commit with sanitized file content.
2. Recreate every descendant commit whose parent SHA changes.
3. Preserve each commit's message where practical.
4. Preserve merge-parent structure where practical.
5. Reuse unchanged trees whenever the tree itself is already privacy-safe.
6. Preserve normal GitHub author identity rather than attempting anonymization.
7. Force-move each affected normal branch ref to its rewritten equivalent only after the complete rewritten graph has been built and verified.

Because Git commit IDs depend on parent IDs and metadata, every descendant of the first rewritten commit receives a new SHA even when its file tree is unchanged.

## Rewrite mechanics

### 1. Inventory

Before writing any replacement commit:

- enumerate all normal branch refs;
- capture each branch tip SHA;
- walk the reachable commit graph far enough to locate the earliest offending tree;
- identify every commit/tree containing one of the target personal/project labels;
- record old-to-new SHA mappings during reconstruction.

### 2. Sanitize offending trees

For commits whose trees contain target references:

- fetch the affected file content;
- replace only the identifying examples with generic equivalents;
- remove historical internal planning text that unnecessarily records those personal examples where replacement would be awkward;
- do not alter unrelated educational content.

### 3. Recreate descendants

For every descendant of a rewritten commit:

- keep the same tree if that tree is already clean;
- create a new commit pointing to the rewritten parent SHA(s);
- preserve commit message and parent order;
- preserve merge topology rather than linearizing merged work.

The GitHub write interface used here does not expose exact low-level preservation of all original author dates, committer dates, GPG signatures, or verification state. Rewritten commits may therefore show new metadata/signature status even when their tree and message match the original.

### 4. Verification before ref movement

Do not move `main` or any other normal branch until all of the following pass:

- rewritten `main` tree is identical to the pre-rewrite `main` tree;
- rewritten branch tips represent the expected branch content;
- target personal/project labels are absent from all rewritten reachable trees;
- common secret/credential scans remain clean;
- merge structure has been preserved where intended;
- every old branch tip has a known rewritten equivalent.

### 5. Force-move branch refs

Once verification passes:

- force-update `main` to the rewritten main tip;
- force-update each affected historical feature branch to its rewritten tip;
- recreate or remove the temporary design branch so it no longer points into the old ancestry.

No ref is force-moved until the complete mapping and verification evidence exist.

## Pull-request ref limitation

GitHub maintains internal refs for pull requests such as `refs/pull/*`. Normal repository branch operations do not provide control over those internal refs.

After the normal branch rewrite, representative old SHAs and merged PR pages must be checked again.

Possible outcomes:

1. **Old objects are no longer reachable through public branch/PR navigation.** The cleanup is complete for practical repository access.
2. **Merged PR refs still expose old objects.** Branch rewriting alone cannot finish the purge. The remaining step is to contact GitHub Support and request removal of cached/referenced sensitive historical objects after the repository refs have already been rewritten.

This design does not claim that force-moving branches alone guarantees immediate physical deletion of unreachable Git objects from GitHub storage.

## Safety and rollback

Before any force update:

- record all current branch names and tip SHAs;
- record current `main` tree SHA;
- retain the complete old-to-new mapping;
- do not delete old branches until rewritten equivalents are verified.

If a branch move produces an unexpected result before old objects are purged, it can be pointed back to its recorded original tip.

Once GitHub Support or garbage collection permanently removes unreachable old objects, rollback to those historical objects may no longer be possible. Therefore destructive purge requests happen only after rewritten refs and current content are verified.

## Verification checklist

After branch refs move:

- [ ] Fetch `main` and confirm its tree matches the pre-rewrite tree.
- [ ] Confirm README and all current study/resource files are unchanged.
- [ ] Search current branch for known personal/project labels.
- [ ] Search rewritten historical branches for known personal/project labels.
- [ ] Search for common credential markers and private-key headers.
- [ ] Confirm all expected branch names still resolve.
- [ ] Confirm merged PRs still render sensibly.
- [ ] Test representative old commit URLs.
- [ ] Determine whether any old object remains publicly reachable through GitHub PR refs/caches.
- [ ] If necessary, prepare a GitHub Support purge request with the affected old SHAs after branch rewriting is complete.

## Success criteria

The operation is successful when:

1. Current `main` content is unchanged.
2. Normal branch history no longer exposes the identified personal/project references.
3. Normal GitHub author attribution remains intact.
4. All intended branch refs point to the rewritten clean graph.
5. No new secret or PII issue is introduced.
6. Any remaining GitHub-internal PR-ref exposure is explicitly identified and, if necessary, handed off to GitHub Support for final object purge.

## Non-goal: anonymity

This repository remains owned by the public GitHub account `Ronlin1`. The rewrite is intended to remove unnecessary historical personal/project content, not to make repository ownership anonymous.
