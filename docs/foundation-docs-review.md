# 30 Agents in 30 Days — Foundation Docs Review

> Historical note: this document records the 2026-06-30 foundation document review. It is planning context, not the current repository structure contract. For current canonical paths and ownership, use `docs/source-of-truth-map.md`.

**Status:** Complete for planning  
**Date:** 2026-06-30  
**Documents reviewed:**

- `project-charter.md` v0.6
- `engineering-principles.md` v0.4
- `evaluation-framework.md` v0.4
- `content-strategy.md` v0.4

## Review test

The final pass checked the documents as a system, not as separate drafts.

Criteria:

1. Remove contradictions across the four documents.
2. Align terminology: Agent Kit, Field Notes, Promotion Review, Research Register, verdict, confidence, autonomy level and Fieldwork Method.
3. Remove repeated philosophy unless it adds an operating rule.
4. Clarify source of truth for verdicts, confidence, autonomy and publishing claims.
5. Make the documents usable mid-challenge under time pressure.
6. Align evidence thresholds and publishing triage.
7. Preserve the core principle: experiments are immutable; the operating system evolves.

## Changes made

### Project Charter v0.6

- Set status to `Approved for planning`.
- Replaced “lasting outputs” with “outputs”.
- Restored “useful” in the core thesis where it clarifies the goal: agents should be useful inside organisations, not merely working.
- Aligned Field Notes language with the Content Strategy: an experiment may produce a Field Notes record even if no Field Notes are promoted.
- Aligned demo-recording language with the shared evidence threshold: capture recordings when they take under 10 minutes or can be generated automatically.
- Added the business posture from the Content Strategy: shifting how trusted clients, partners and peers describe Fieldwork.
- Replaced “playbook” with “Fieldwork Method” where referring to the final post-project method.

### Engineering Principles v0.4

- Set status to `Approved for planning`.
- Added links to the Evaluation Framework and Content Strategy.
- Changed “Evaluate before polishing” to “Evaluate before polishing or publishing”.
- Capitalised Research Register consistently.
- Expanded the lifecycle so README/evidence completion and Research Register update are explicit before publication.
- Replaced the local evaluation checklist with a pointer to the Evaluation Framework’s standard record.
- Aligned evaluation terminology with the Evaluation Framework: baseline/value, adoption/disuse, cost/maintenance, autonomy, safety/production readiness and promotion evidence.
- Clarified how to handle deferred article/social publishing.
- Replaced “playbook” with “Fieldwork Method” where referring to the evolving post-project method.

### Evaluation Framework v0.4

- Set status to `Approved for planning`.
- Added the Content Strategy as a related document.
- Aligned Field Notes records with the Content Strategy: `field-notes.md` exists even when no Field Notes are promoted.
- Strengthened calibration: weekly review should re-read recent verdicts plus at least one earlier evaluation outside the current week.
- Clarified that the Research Register records article/case-study links, not only write-ups.
- Reordered downstream usage so Promotion Review decides what moves into wider use, and Field Notes record promoted observations.
- Clarified cost completion wording: build/run costs should be recorded or marked `not measured`.

### Content Strategy v0.4

- Set status to `Approved for planning`.
- Added related document links.
- Clarified public source-of-truth conflicts: fix public posts when they conflict with repo/evaluation/register; use Evaluation Framework source-of-truth rules when repo and Research Register disagree.
- Clarified `field-notes.md` ownership: promoted observations, or a record that no Field Notes were promoted.
- Aligned the daily flow with the Engineering Principles: Promotion Review precedes Field Notes.
- Moved tomorrow’s brief/GitHub issue into the research core, leaving article/social as the publishing tail.
- Clarified that the publishing tail can lag or batch, but the research core cannot be skipped.

## Cross-document source-of-truth rules

- `brief.md` owns the original hypothesis, assumptions, baseline and scope.
- `evaluation.md` owns verdict, verdict reason, confidence and recommended autonomy level.
- `promotion-review.md` owns what graduates into the Agent Kit, templates, modules, patterns or recommendations.
- `field-notes.md` owns observations promoted from the experiment, or records that no Field Notes were promoted.
- `README.md` owns the canonical public summary of one experiment.
- The Research Register summarises experiments and records later calibration notes.
- Website articles, social posts and gallery entries are derived from the repository record.

## Remaining open questions

These do not block the foundation documents.

1. Exact daily time budget after the Agent #0 dry run.
2. Exact template wording for `brief.md`, `evaluation.md`, `field-notes.md`, `promotion-review.md`, `README.md` and GitHub issues.
3. Agent Kit and CLI specification.
4. Initial 30-agent backlog and coverage matrix.
5. Co-founder review before public publication.

## Readiness

The four foundation documents are ready to seed the `30-agents` repository and guide the next phase: creating the operating templates.
