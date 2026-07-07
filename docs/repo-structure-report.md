# Repository Structure Report

Date: 2026-07-06

Scope: checked `AGENTS.md`, the four foundation documents, `docs/foundation-docs-review.md`, `docs/planning-summary.md`, repository records, backlog files and templates. Foundation documents were not changed.

Resolution note: issue #1 turned the main recommendation from this report into `docs/source-of-truth-map.md`. Treat this report as the dated audit evidence, not the current operational structure contract.

Post-PR note: several findings below describe the pre-PR state and are now resolved in the same branch that added the source-of-truth map. Resolved items are marked as such in the recommendations section.

## Summary

The repository is broadly aligned with its programme role: it contains foundation docs, registers, indexes, backlog material, weekly review and synthesis folders, evidence placeholder, and reusable templates. The main mismatch is that the implemented structure has evolved away from the initial shape in `docs/planning-summary.md`.

That drift is mostly reasonable, but it is not yet documented cleanly. The repo now has `registers/`, `backlog/`, `templates/agent-repo/` and `templates/operating/`, while the planning summary still describes flatter `templates/`, `research/` records and `agents/index.md`.

## Missing Files

Files listed in the planning summary but not present at those paths:

- `templates/README.md`
- `templates/brief.md`
- `templates/evaluation.md`
- `templates/field-notes.md`
- `templates/promotion-review.md`
- `templates/github-issue.md`
- `research/research-register.md`
- `research/field-notes.md`
- `research/recommendations.md`
- `agents/index.md`

Likely replacements already exist:

- `templates/agent-repo/README.md`
- `templates/agent-repo/brief.md`
- `templates/agent-repo/evaluation.md`
- `templates/agent-repo/field-notes.md`
- `templates/agent-repo/promotion-review.md`
- `templates/operating/daily-issue.md`
- `registers/research-register.md`
- `registers/field-notes-index.md`
- `registers/recommendations.md`
- `agents/README.md`

Other expected programme artefacts exist as placeholders rather than filled records:

- `registers/agent-index.md`
- `registers/research-register.md`
- `registers/field-notes-index.md`
- `registers/recommendations.md`
- `backlog/master-backlog.md`
- `backlog/research-debt.md`

## Outdated References

- `docs/planning-summary.md` still shows the original repository plan with flat `templates/`, research records under `research/`, and `agents/index.md`.
- `docs/planning-summary.md` names `templates/github-issue.md`; the implemented operating template is `templates/operating/daily-issue.md`.
- `docs/planning-summary.md` says the next work is to create the repo structure, add foundation docs, create `AGENTS.md`, draft operating templates and review them. Those first steps are already complete or partly complete.
- `docs/foundation-docs-review.md` still lists exact template wording and initial 30-agent backlog/coverage matrix as open questions. The repo now contains operating templates and a drafted 50-concept research backlog with coverage matrix in `research/backlog.md`.
- Resolved by issue #1: `README.md` described the current structure but omitted `research/`, even though `research/backlog.md` exists and appears substantive.
- `docs/planning-summary.md` uses “lasting outputs”, while `docs/foundation-docs-review.md` says that wording was replaced with “outputs” in the charter.

## Contradictions

- Backlog source of truth is split. `backlog/master-backlog.md` contains only a TBD `#01` row, while `research/backlog.md` contains a full draft planning backlog, coverage matrix, recommended first 10 and provisional 20. It is unclear which file should drive sequencing.
- Register/index locations differ between the planning summary and implementation. The foundation docs describe programme records conceptually, but the planning summary points to `research/` while `README.md` points to `registers/` and `backlog/`.
- Agent index naming differs. The planning summary expects `agents/index.md`; the repo has `agents/README.md` and a fuller `registers/agent-index.md`.
- Resolved by issue #1: the repo had both `agents/README.md` and `registers/agent-index.md` with overlapping purpose and placeholder `#01` rows. `agents/README.md` now points to the canonical register.
- `research/backlog.md` says it is a draft planning proposal, while `backlog/master-backlog.md` is named as the master backlog. Without a promotion step between them, daily planning can drift.

## Recommended Next PRs

1. **Resolved by issue #1: align structure references without changing foundation docs.** `docs/source-of-truth-map.md` now records the implemented structure, and historical planning docs carry warning banners.
2. **Resolved by issue #1 and PR #17: clarify backlog ownership.** `docs/source-of-truth-map.md` records `research/backlog.md` as a planning input to `backlog/master-backlog.md`, and the master backlog now records the promotion mechanism for provisional candidates.
3. **Resolved by PR #8: promote the initial backlog.** The recommended first ten agents were promoted into `backlog/master-backlog.md` and `registers/agent-index.md`, with the candidate review recorded in `backlog/candidate-review.md` (PR #13).
4. **Resolved by issue #1: resolve duplicate indexes.** `registers/agent-index.md` is the canonical source and `agents/README.md` is a lightweight pointer.
5. **Close stale open questions.** Add a non-foundation status note for which planning questions are now answered, partly answered or still open.
6. **Resolved by PR #9: review operating templates.** The operating templates were tightened against the foundation documents before the Agent #0 dry run, and later revised to v0.2 (publication tiers, PR #15) and v0.3 (backlog promotion, PR #17).
7. **Resolved by issue #1: add a source-of-truth map.** `docs/source-of-truth-map.md` now lists current canonical paths for programme records, templates, backlog, research debt, evidence, weekly reviews and synthesis.
