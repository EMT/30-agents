---
name: close-out
description: Close out one "30 Agents in 30 Days" experiment day — sync the programme registers from the experiment repo's records, draft the publication tail for its tier, resolve today's daily issue, and prepare tomorrow's experiment. Use when the user says "close out" / "close out agent #XX", "end of day", "update the registers", "open tomorrow's issue", or "draft the publication tail".
---

# Daily Close-Out

Operates the programme's daily paperwork so records stay consistent without hand-copying. It **drafts and proposes** (Suggest on the autonomy ladder): show every register edit, draft and issue action for review before committing or posting anything. Never push to a published experiment repo — experiments are immutable once published.

**Never invent content.** Every claim in a register row, article, or post must trace to a record in the experiment repo (`evaluation.md`, `field-notes.md`, `promotion-review.md`, `brief.md`, `README.md`, `evidence/`). Where evidence is missing, record the gap — do not fill it. On any ownership conflict, `docs/source-of-truth-map.md` wins on paths, `evaluation.md` wins on verdicts.

## Inputs

Agent number (e.g. `/close-out 02`). Find the experiment repo as a sibling checkout (`../agent-XX-*`); if absent, clone from `EMT/agent-XX-*`.

## Workflow

**1. Verify the experiment is closeable.** `evaluation.md` must have verdict, verdict reason, confidence and recommended autonomy; `brief.md` must be approved with a declared publication tier. If anything is missing, stop and list the gaps — closing out an unevaluated experiment is the failure mode this programme exists to avoid ("evaluate before polish").

**2. Sync the registers** (in this repo, from the experiment repo's records):
- `registers/agent-index.md` — the agent's row: repo/brief/evaluation links, verdict, confidence, recommended autonomy, article/demo state, status.
- `registers/research-register.md` — hypothesis, verdict, verdict reason, confidence, key evidence, links. Leave calibration notes to the weekly review.
- `registers/field-notes-index.md` — one row per Field Note promoted in `field-notes.md`; if none were promoted, confirm the experiment recorded that explicitly.
- `registers/recommendations.md` — candidates from `promotion-review.md` only. No all-TBD placeholder rows.

**3. Draft the publication tail for the declared tier** (definitions: `templates/operating/README.md`):
- **Public** — article draft from `templates/operating/article-or-case-study.md`, social posts from `templates/operating/social-posts.md`, public evidence links.
- **Private** — case study from redacted/synthetic/summarised evidence only; social posts may point to it.
- **Internal** — no output; draft the waiver instead.
Drafts live in the experiment repository under `content/` (create it with the first draft: `content/article.md` or `content/case-study.md`, `content/social-posts.md`) — never in this public programme repo, so unreviewed drafts stay private until the experiment publishes. Internal tier creates no `content/` at all. Each tail item resolves as `Done`, `Deferred` (owner + next step) or `Waived` (reason) in the daily issue.

**4. Resolve today's daily issue** (in the experiment repo): tick what the records prove is done, record the tail states and any tier change (less exposure only), then propose closing it. Unfinished non-tail work goes to backlog changes or research debt, not into scope expansion.

**5. Prepare tomorrow.** Next agent = first unstarted row in `backlog/master-backlog.md`. Its Tier column must hold a real value (set at promotion; if it's TBD, ask the human — don't guess). If the repo doesn't exist, scaffold it with the agent kit (`../fieldwork-agent-kit/bin/create-fieldwork-agent.ts <NN>` — the kit reads the tier from the backlog row). Then open its daily build issue from `templates/operating/daily-issue.md` with links, tier and goal prefilled from the brief — title convention: `Agent #NN - Build <Title>`.

**6. Present the changeset** — register diffs, drafts, issue actions, tomorrow's prep — and wait for approval before committing to this repo or touching GitHub.

## Out of scope

Weekly reviews and calibration (`templates/operating/weekly-review.md`), backlog promotion decisions, editing a published experiment's artefacts, and anything requiring judgement the records don't contain — flag those for the human instead.
