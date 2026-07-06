# 30 Agents in 30 Days — Planning Summary

> Historical note: this document records the 2026-06-30 planning handoff. It is not the current repository structure contract. For current canonical paths and ownership, use `docs/source-of-truth-map.md`.

**Status:** Ready for Codex handoff  
**Date:** 2026-06-30  
**Primary repository:** `30-agents`

## Purpose

This summary captures the working agreement from the planning phase so the project can move into Codex without copying the whole chat history.

The full source of truth is the foundation document set:

- `project-charter.md`
- `engineering-principles.md`
- `evaluation-framework.md`
- `content-strategy.md`
- `foundation-docs-review.md`

Use this file as a quick orientation layer, not as a replacement for the foundation docs.

## Project in one paragraph

Fieldwork will build thirty small, working AI agents in thirty days over six weeks. The agents are experiments, not products. The goal is to learn how practical AI systems should be identified, designed, engineered, evaluated and deployed safely inside real organisations. The lasting outputs are the Agent Kit, Field Notes, evaluation practice, reusable patterns, public evidence and the Fieldwork Method for designing AI systems.

## Core stance

Fieldwork is a design and technology studio. AI expands the solution space; it does not replace the existing way of working.

Start with people, workflows, systems, constraints and outcomes. Then decide whether AI belongs in the solution.

The project is not about automating people away. It is about giving good people superpowers.

## Key decisions

- Agents are experiments, not production products.
- Each experiment has one problem, one hypothesis, three to five assumptions, a baseline, an evaluation and a Promotion Review.
- Experiments are immutable once published.
- The operating system evolves: Agent Kit, templates, backlog, recommendations and the Fieldwork Method.
- The repository is the source of truth. Articles, social posts and gallery entries are derived from it.
- Evaluation happens before publication.
- `evaluation.md` owns verdict, verdict reason, confidence and recommended autonomy level.
- `promotion-review.md` owns what graduates into the Agent Kit, templates, modules, patterns or recommendations.
- `field-notes.md` records promoted observations, or records that no Field Notes were promoted.
- Field Notes are evidence-driven. There is no quota.
- The Research Register summarises experiments and records calibration notes.
- Humans decide what gets built, published, promoted and delegated.
- AI may prepare, draft, evaluate, summarise and recommend.
- The backlog is a hypothesis. It can change because of evidence, research gaps or new insight, not hype or novelty.
- The Agent Kit starts from Eve and composes around it; it should not hide or replace Eve.

## Standard stack

The standard stack is deliberately Vercel/Eve-centric for this project because negligible per-agent setup is more important than portability during the challenge.

- Eve as the agent framework.
- Vercel AI Gateway for model calls.
- Vercel Sandboxes for isolated execution where needed.
- Vercel Workflows for durability where needed.
- Vercel Connect for service auth where needed.
- Eve evals for repeatable automated checks where they fit.
- Eve approval gates for human-in-the-loop workflows where they fit.
- Next.js only when a custom interface is required.
- Neon/Postgres only when persistence is required.
- WorkOS only when user/org auth is required.

Vercel/Eve coupling is an accepted project trade-off, not a general client recommendation.

## Repository plan

Create a `30-agents` repository with this initial shape:

```txt
30-agents/
  AGENTS.md

  docs/
    project-charter.md
    engineering-principles.md
    evaluation-framework.md
    content-strategy.md
    foundation-docs-review.md
    planning-summary.md

  templates/
    README.md
    brief.md
    evaluation.md
    field-notes.md
    promotion-review.md
    github-issue.md

  research/
    research-register.md
    field-notes.md
    recommendations.md
    backlog.md

  agents/
    index.md
```

The `30-agents` repo is the programme record, not the Agent Kit and not the individual agent codebase.

Each daily agent should live in its own repository.

## Individual agent repo model

Each agent repo should tell the complete story of one experiment.

Expected top-level files:

```txt
AGENTS.md
README.md
brief.md
evaluation.md
field-notes.md
promotion-review.md
```

The README is the canonical public summary. Another engineer should be able to understand the experiment in about five minutes from the README, then inspect the supporting files for detail.

## Daily flow

The standard daily flow is:

1. Finish implementation.
2. Run evaluation.
3. Complete `evaluation.md`.
4. Complete `promotion-review.md`.
5. Complete `field-notes.md`.
6. Complete the README.
7. Capture screenshot or recording.
8. Update the Research Register and central index.
9. Prepare tomorrow’s brief and GitHub issue.
10. Derive article or case study from the README.
11. Derive social posts from the README and Field Notes.

Steps 1–9 are the research core. Steps 10–11 are the publishing tail.

The publishing tail can lag or batch. The research core cannot be skipped.

## Agent lifecycle

```txt
Idea
  ↓
Brief approved
  ↓
Repository created
  ↓
Implementation
  ↓
Deployment or demonstration
  ↓
Evaluation
  ↓
Promotion Review
  ↓
Field Notes
  ↓
README and evidence pack
  ↓
Research Register update
  ↓
Publication
  ↓
Archived as immutable experiment
```

New ideas discovered during an experiment should become backlog items, research debt or future experiments. Do not expand the current agent once coding has started, except to reduce scope.

## Evaluation rules

Each evaluation should answer:

- Did the agent address the hypothesis?
- Compared to what baseline?
- For whom?
- At what build/run/maintenance cost?
- With what adoption or disuse risk?
- With what level of autonomy?
- With what safety or production constraints?
- With what confidence?

Verdicts are:

- `Confirmed`
- `Refined`
- `Rejected`

Every verdict needs a reason. Confidence levels need to remain comparable across the thirty experiments, so weekly review should include calibration against at least one earlier evaluation.

## Content rules

- Repository first.
- Research before publishing.
- Trust over reach.
- Short daily, deeper weekly.
- Show evidence rather than claims.
- Publish rejections clearly.
- AI drafts; humans publish.

Do not publish an article, social post or gallery entry before the evaluation is complete and the README reflects the evidence.

## Suggested first Codex task

```txt
We are creating the 30-agents repository for Fieldwork’s “30 Agents in 30 Days” project.

Read docs/project-charter.md, docs/engineering-principles.md, docs/evaluation-framework.md, docs/content-strategy.md and docs/planning-summary.md first.

Do not change the foundation docs unless asked.

Your first task is to scaffold the repository structure, create the empty template files, create AGENTS.md with project-specific instructions for future Codex work, and propose the first set of operating templates for review.

Do not implement the Agent Kit yet.
Do not create Agent #01 yet.
```

## Suggested `AGENTS.md` instruction

The first repository-level `AGENTS.md` should tell Codex:

- read the foundation docs before making changes;
- preserve source-of-truth rules;
- do not invent new process where the docs already define one;
- do not edit foundation docs unless explicitly asked;
- treat templates as living artefacts;
- prefer small, reviewable changes;
- keep examples consistent with the project vocabulary;
- do not implement the Agent Kit or individual agents until the operating templates are approved.

## Next work after handoff

1. Create the `30-agents` repo structure.
2. Add the foundation docs and planning summary.
3. Create `AGENTS.md`.
4. Draft operating templates.
5. Review and tighten operating templates.
6. Specify the Agent Kit.
7. Specify the CLI.
8. Create the initial backlog and coverage matrix.
9. Run Agent #0 as a private dry run.
10. Start Agent #01.

## Open questions

These do not block the Codex handoff.

- Exact wording of the operating templates.
- Exact Agent Kit and CLI specification.
- Initial 30-agent backlog and coverage matrix.
- Exact daily time budget after Agent #0.
- Co-founder review before public publication.
