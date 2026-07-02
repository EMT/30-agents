# 30 Agents in 30 Days — Codex Instructions

This repository is the programme-level source of truth for Fieldwork's "30 Agents in 30 Days" project.

## Read First

Before making project changes, read:

- `docs/project-charter.md`
- `docs/engineering-principles.md`
- `docs/evaluation-framework.md`
- `docs/content-strategy.md`

Do not change these foundation documents unless the user explicitly asks.

## Repository Role

This repository owns programme-level material:

- project documents;
- Research Register;
- agent index;
- master backlog;
- Field Notes index;
- cross-agent recommendations;
- weekly reviews;
- synthesis drafts;
- reusable operating templates.

It does not contain the implementation of the Fieldwork Agent Kit. Do not scaffold or implement Agent Kit runtime, CLI, modules, package manifests, or application code here unless explicitly asked.

## Experiment Model

Each experiment should live in its own `agent-XX-name` repository. Required files for an experiment repository are:

- `AGENTS.md`
- `README.md`
- `brief.md`
- `evaluation.md`
- `field-notes.md`
- `promotion-review.md`

Use `templates/agent-repo/` as the starting point for those files.

## Operating Rules

- Optimise for learning, not features.
- Start from the workflow, user, baseline, hypothesis and assumptions before implementation.
- Keep each experiment to one narrow problem and one hypothesis.
- Freeze the brief once coding starts.
- Evaluate before polish, publication or social output.
- Publish confirmed, refined and rejected hypotheses honestly.
- Treat published experiments as immutable snapshots.
- Promote reusable work only through Promotion Review.
- Record adoption, cost, autonomy, safety and production-readiness notes for every experiment.
- Prefer the standard stack described in `docs/engineering-principles.md` unless the experiment is deliberately testing a variation.

## Source-of-Truth Rules

- `evaluation.md` owns the full verdict, confidence level, autonomy recommendation and verdict reason for an experiment.
- The Research Register records a summary of the evaluation.
- `promotion-review.md` owns promotion decisions.
- `field-notes.md` owns observations promoted from the experiment, including a record when no Field Notes were promoted.
- Repository evidence takes priority over articles, social posts and gallery entries.

## Content Rules

- Do not publish or draft public claims that are unsupported by the repository, evaluation or evidence pack.
- Do not publish sensitive data, credentials, customer information or internal operational details.
- Use synthetic, redacted or summarised evidence for private/internal-data experiments.
- Write in Fieldwork's voice: direct, practical, specific and honest.
- Avoid hype language such as "transformative", "revolutionary", "unlock", "seamless" and "game-changing".
- Do not anthropomorphise agents unless the experiment is explicitly about agent identity or collaboration.

## Editing Guidance

- Keep foundation docs unchanged unless asked.
- Keep this repository focused on planning, records, templates and synthesis.
- Do not introduce infrastructure, dependencies or runtime code without an approved task.
- When updating templates, prefer small, reviewable changes and note why the change improves daily operation.
- When adding or changing programme records, keep links stable and use relative paths.

## GitHub API Commands

When running shell commands that pass GitHub API paths or URLs, always quote the full path or URL, especially query strings and shell metacharacters.

Prefer:

```sh
gh api 'repos/OWNER/REPO/contents/path?ref=branch'
```

over an unquoted API path.
