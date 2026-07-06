# 30 Agents in 30 Days — Source Of Truth Map

**Status:** Current operational structure  
**Date:** 2026-07-06  
**Primary repository:** `30-agents`

This document defines the current canonical paths and ownership for the programme repository. Use it when deciding where records, templates, backlog items, evidence notes and synthesis material should live.

The foundation documents still define the project principles, evaluation rules and content rules. This map only defines current repository structure and path ownership.

## Document hierarchy

1. Foundation docs define the programme principles and operating rules:
   - `docs/project-charter.md`
   - `docs/engineering-principles.md`
   - `docs/evaluation-framework.md`
   - `docs/content-strategy.md`
2. `AGENTS.md` defines instructions for Codex and other AI coding agents working in this repository.
3. `docs/source-of-truth-map.md` defines current canonical paths and ownership.
4. `docs/planning-summary.md` and `docs/foundation-docs-review.md` are historical planning records, not current structure contracts.

## Structure decision

The implemented repository structure differs from the original planning summary. That change happened in the initial programme repository commit on 2026-07-02.

The current structure is preferred because it separates:

- programme registers from research planning;
- approved backlog from candidate backlog concepts;
- reusable agent repository templates from daily operating templates;
- programme records from external experiment repositories.

The issue was not the structure itself. The issue was that the planning summary was not clearly marked as historical after the scaffold established a better current structure.

## Canonical paths

| Path | Owns |
| --- | --- |
| `AGENTS.md` | AI coding-agent instructions for this repository. |
| `README.md` | Human-facing orientation to the repository. |
| `docs/project-charter.md` | Project purpose, thesis, deliverables and success measures. |
| `docs/engineering-principles.md` | Engineering stance, stack, lifecycle, security, testing and promotion principles. |
| `docs/evaluation-framework.md` | Evaluation dimensions, verdicts, confidence levels, autonomy levels and evidence requirements. |
| `docs/content-strategy.md` | Publication, Field Notes, article, social and synthesis rules. |
| `docs/source-of-truth-map.md` | Current canonical repository paths and ownership. |
| `docs/planning-summary.md` | Historical 2026-06-30 planning handoff. |
| `docs/foundation-docs-review.md` | Historical 2026-06-30 cross-document review record. |
| `docs/repo-structure-report.md` | Dated audit report used to identify current structure drift. |
| `registers/agent-index.md` | Canonical programme-level index of experiments. |
| `registers/research-register.md` | Summary of experiment evidence and later calibration notes. |
| `registers/field-notes-index.md` | Index of promoted Field Notes from experiments. |
| `registers/recommendations.md` | Cross-agent recommendations supported by repeated evidence. |
| `backlog/master-backlog.md` | Canonical approved execution sequence for experiments. |
| `backlog/research-debt.md` | Questions raised by experiments that the programme owes itself. |
| `research/backlog.md` | Candidate concept pool, coverage matrix and sequencing analysis. |
| `agents/README.md` | Pointer to external experiment repositories and the canonical agent index. |
| `templates/agent-repo/` | Starting files for each external `agent-XX-name` repository. |
| `templates/operating/` | Daily issue, evidence, article, social and weekly review templates. |
| `evidence/` | Programme-level evidence notes or pointers that do not belong to one experiment repo. |
| `weekly-reviews/` | Weekly synthesis and calibration records. |
| `synthesis/` | Programme-level synthesis drafts, including emerging method and recommendations. |

## Backlog ownership

`backlog/master-backlog.md` is the canonical source for approved experiment sequencing.

`research/backlog.md` is a planning input. It may contain more concepts than the programme will run and should feed future changes to the master backlog.

`backlog/research-debt.md` records questions created by experiments that cannot be answered immediately.

## Agent index ownership

`registers/agent-index.md` is the canonical programme-level experiment index.

`agents/README.md` should not duplicate the full canonical table unless it is generated from the register. It should point readers to `registers/agent-index.md` and explain that experiments live in separate repositories.

## Conflict rules

- If a foundation document conflicts with this map on principles, evaluation or content rules, the foundation document wins.
- If a historical planning document conflicts with this map on repository paths or ownership, this map wins.
- If `README.md` conflicts with this map on repository paths, this map wins and `README.md` should be corrected.
- If `registers/research-register.md` conflicts with an experiment `evaluation.md`, the experiment `evaluation.md` wins unless the register explicitly records a later calibration note.
- If a public article, social post or gallery entry conflicts with repository evidence, fix the public material.
