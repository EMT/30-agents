# 30 Agents in 30 Days — Engineering Principles

**Version:** v0.4  
**Status:** Approved for planning  
**Owner:** Fieldwork  
**Related documents:** `project-charter.md`, `evaluation-framework.md`, `content-strategy.md`

## 1. Purpose

This document defines how we build, evaluate and publish each experiment.

Use it when deciding scope, stack, tests, evidence, security, delegation, promotion and backlog changes.

## 2. Non-negotiables

Every experiment must follow these rules:

1. Build one agent or agentic workflow.
2. Test one hypothesis.
3. Start from a brief approved before coding begins.
4. Freeze the brief once coding starts.
5. Keep scope narrow enough to finish, evaluate and publish.
6. Evaluate before polishing or publishing.
7. Capture evidence that supports the verdict.
8. Publish confirmed, refined and rejected hypotheses.
9. Promote reusable work deliberately.
10. Leave the experiment immutable once published.

## 3. Scope

### One problem per agent

Each agent should focus on one problem. If the brief needs several “and” clauses, reduce the scope.

Bad:

> Summarise meetings and create tasks and update Jira and email attendees.

Better:

> Turn a meeting transcript into an actionable task list.

### One hypothesis per agent

Each experiment needs one hypothesis. The hypothesis gives the evaluation something to test.

Examples:

> AI can reduce the effort required to review a proposal for delivery risk.

> Structured outputs make the result easier to evaluate than free-form Markdown.

### Record assumptions

Each brief should include three to five assumptions. Assumptions are the conditions we rely on but may not be directly testing.

If an assumption matters, capture it in `evaluation.md`, `field-notes.md` or `promotion-review.md`.

### Define the baseline

Each brief must state how the problem is solved today. The baseline may be manual work, search, a spreadsheet, deterministic software, an existing product or doing nothing.

Without a baseline, we cannot judge whether the agent is worth building.

## 4. Engineering stance

### Optimise for learning

When time forces a choice, choose the work that teaches us most about the hypothesis, adoption, cost, safety or future delivery.

Do not spend the daily budget on features, social reach, premature abstraction or polish unless they improve the experiment.

### Start with the workflow

Do not start with a model, framework or prompt. Start with the person, workflow, current process, pain point, cost and outcome.

### Use AI only where it helps

The right answer may be an agent, a human-in-the-loop workflow, deterministic software, workflow redesign or no AI.

### Design for adoption

For each experiment, identify:

- who uses it;
- where it fits in the workflow;
- what would make someone trust it;
- what would make someone ignore or abandon it.

## 5. Stack

Use the standard stack unless the experiment is testing an alternative.

### Foundation

Eve is the foundation because setup time is a constraint. It gives us the agent runtime, filesystem conventions, tool loading, approvals, evals, durable execution, sandboxed execution and Vercel integration without assembling that infrastructure for every experiment.

The Agent Kit should start from Eve and add Fieldwork’s research workflow around it. Do not hide, replace or unnecessarily wrap Eve.

### Default stack

- Eve for the agent runtime;
- Vercel for deployment;
- Vercel AI Gateway for model access;
- TypeScript;
- GitHub for source control, issues and review.

### Optional capabilities

Add capabilities only when the brief requires them.

Use Eve or Vercel-native primitives first:

| Need | Default approach |
| --- | --- |
| Agent scaffold | Eve init, or Agent Kit command that composes Eve |
| Behaviour tests | Eve evals where they fit |
| Human confirmation | Eve approval gates |
| Delegated service access | Vercel Connect where suitable |
| Durable execution | Vercel Workflows through Eve |
| Isolated execution | Vercel Sandbox through Eve |
| Channels | Eve channels where suitable |

Add other services only when the default stack does not cover the need:

| Need | Add |
| --- | --- |
| Rich custom UI | Next.js |
| Relational persistence | Neon/Postgres |
| User or organisation auth beyond the agent runtime | WorkOS |
| Caching or transient state | Redis |
| Persistent files | Blob storage |
| External integrations not covered by Connect/Eve | Specific integration or MCP server |

Do not include infrastructure by default. Add what the brief requires.

### Accept the stack trade-off

This project accepts Vercel/Eve coupling in exchange for low setup time, comparable experiments and a compounding Agent Kit.

This is a project choice, not a client recommendation.

Do not spend daily build time engineering portability into every agent. If lock-in, portability or migration cost emerges as evidence, capture it in Field Notes or Promotion Review.

## 6. Repository model

The project uses three repository types.

### `30-agents`

Programme-level truth:

- project documents;
- Research Register;
- agent index;
- master backlog;
- Field Notes index;
- cross-agent recommendations;
- synthesis drafts.

### `fieldwork-agent-kit`

Reusable platform:

- base template;
- CLI commands;
- optional modules;
- shared evaluation helpers;
- documentation for creating and extending agent projects.

### `agent-XX-name`

One repository per experiment.

Required files:

```txt
AGENTS.md
README.md
brief.md
evaluation.md
field-notes.md
promotion-review.md
```

`README.md` is the canonical summary. Another engineer should be able to understand, evaluate and reproduce the experiment from the repository.

`brief.md`, `evaluation.md`, `field-notes.md` and `promotion-review.md` are research artefacts.

`AGENTS.md` is reserved for instructions to AI coding agents.

## 7. Daily lifecycle

Each agent follows this lifecycle:

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
README and evidence complete
↓
Research Register updated
↓
Publication
↓
Archived
```

### Prepare tomorrow today

At the end of each day:

1. complete the Promotion Review;
2. write Field Notes;
3. complete the README and evidence pack;
4. update the Research Register;
5. prepare tomorrow’s brief;
6. open tomorrow’s GitHub issue.

Morning work should begin with a ready brief and issue, not open-ended planning.

### Use the GitHub issue as the daily cockpit

The issue in the agent repository drives the day. It should contain:

- link to the brief;
- implementation checklist;
- evaluation checklist;
- evidence checklist;
- Promotion Review checklist;
- publication checklist.

Close the issue when the experiment is published and recorded.

### Freeze the brief when coding starts

Once implementation begins, the brief is frozen.

During the build, scope may shrink. Scope should not expand. New ideas go to the backlog, research debt or a future experiment.

## 8. Immutability and evolution

### Experiments are immutable

A published agent is a snapshot of what we built and believed on that day.

After publication, only bug fixes and documentation corrections are allowed. New features, architectural changes and major improvements belong in future experiments.

### Promoted operational tools may evolve

If an agent is used in the daily process, it may graduate into the Agent Kit or internal tooling and evolve there.

The public experiment remains immutable. The promoted tool may improve.

### The operating system evolves

The Agent Kit, templates, backlog, Research Register, recommendations and the Fieldwork Method should improve during the project.

Previous experiments are not rewritten to match newer standards.

## 9. Evaluation and tests

### Evaluation before polish

When time is limited, prioritise:

1. evaluation;
2. user experience;
3. documentation;
4. code polish.

Before publication, remove confusing dead code, avoid leaked secrets, and document how to run the project. Do not abstract beyond what the experiment requires.

### Use Eve evals where they fit

Use Eve’s native evals when a check can be expressed as repeatable inputs, expected behaviour and a scoring rubric.

The Fieldwork Evaluation Framework defines what we assess and how we interpret the result. Eve evals are one execution mechanism. They do not replace `evaluation.md`, Field Notes or Promotion Review.

For each experiment, decide which checks should be:

- automated through Eve evals;
- tested manually with representative scenarios;
- assessed through human judgement;
- recorded as production-readiness questions.

Use the Evaluation Framework for the standard evaluation record.

Every evaluation must record:

- baseline and value;
- scenario results;
- adoption and disuse risks;
- cost and maintenance notes;
- implemented and recommended autonomy level;
- safety and production-readiness constraints;
- reuse or promotion evidence.

Record autonomy using the standard ladder:

```txt
Observe → Suggest → Recommend → Approve → Delegate → Automate
```

### Write tests when they increase confidence

Do not chase coverage. Behavioural evaluation matters more than unit test percentage.

Use AI to reduce the cost of testing. If AI can generate tests that increase confidence without increasing the time budget, use them.

Prioritise tests for:

- tool behaviour;
- structured outputs;
- evaluation scenarios;
- data handling;
- permission boundaries;
- failure modes.

## 10. Evidence

Each experiment should leave evidence that supports its verdict.

Always capture:

- brief;
- README;
- evaluation;
- Field Notes;
- Promotion Review;
- representative inputs;
- representative outputs;
- screenshot when the agent has a visible interface or output.

Capture if it takes under 10 minutes or can be generated automatically:

- 30–60 second demo recording;
- architecture diagram;
- cost estimate;
- latency or runtime metrics;
- logs or traces;
- comparison against the baseline.

Do not publish sensitive data. Private experiments may be represented through redacted screenshots, synthetic examples, architecture notes or video without public access.

## 11. Security and delegation

Every experiment should ask what could go wrong if deployed in an organisation.

Consider:

- authentication;
- authorisation;
- agent identity;
- delegated authority;
- least privilege;
- secrets management;
- sensitive data;
- data retention;
- audit trails;
- tool permissions;
- human approval;
- reversibility;
- failure recovery;
- observability.

Not every experiment needs to implement these controls. Every experiment should identify which would matter in production.

Use platform primitives when they match the risk:

- Eve approval gates for actions that need human confirmation;
- Vercel Connect for delegated access to external services;
- Eve/Vercel traces and Agent Runs for session, tool-call, timing and token visibility.

Agent permissions should be designed, not inherited accidentally.

### Human decision boundary

AI may prepare, suggest, draft, evaluate and recommend.

Humans decide:

- what gets built;
- what gets published;
- what gets promoted;
- which decisions are delegated;
- whether an experiment confirms, refines or rejects its hypothesis.

Some experiments may test whether a decision can be delegated. The decision to delegate remains human.

### Map autonomy to implementation

The autonomy ladder should map to system behaviour:

| Level | Behaviour |
| --- | --- |
| Suggest | Agent produces options only. |
| Recommend | Agent proposes one option with reasoning. |
| Approve | Agent prepares an action and waits for confirmation. |
| Delegate | Human assigns a bounded task to the agent. |
| Automate | Agent acts without confirmation inside defined limits. |

When approval is required, use platform approval gates unless the experiment is testing a different approval mechanism.

## 12. Promotion Review

Every experiment ends with a Promotion Review.

The review decides what, if anything, moves from the day’s experiment into wider use.

Promotion targets:

| Target | Promote when |
| --- | --- |
| Template | Every future agent should start with it, or it removes recurring setup work without adding services, secrets or configuration. |
| Module | At least two planned or completed experiments need it, and Eve or the default stack does not already cover it. |
| Pattern | It can be written as “use this when… / avoid this when…” and applies to at least one future experiment. |
| Field Note | It records an observation that may change future implementation, evaluation, scope or deployment decisions. |
| Recommendation | At least three experiments support it, with trade-offs and counterexamples recorded. |

Do not promote a recommendation from one experiment unless it reveals a clear security, reliability or adoption risk.

## 13. Backlog and research debt

The backlog is a hypothesis, not a contract.

Change it when:

- evidence suggests a better experiment;
- a research gap appears;
- fresh insight suggests a stronger question;
- scope needs to be adjusted for sustainability.

Do not change it because:

- a new model or framework is fashionable;
- a social post suggests a flashier demo;
- the team is bored with the plan.

Research debt is the set of questions the programme now owes itself.

Capture research debt when an experiment reveals a gap, contradiction or follow-up question that cannot be answered that day.

## 14. Sustainability

The process must fit alongside client work.

Track approximate time spent on:

- briefing;
- implementation;
- evaluation;
- documentation;
- publication;
- Promotion Review.

Use agents to reduce repetitive work:

- issue creation;
- README drafting;
- article drafting;
- social post drafting;
- evaluation summaries;
- Research Register updates;
- tomorrow’s handover.

Do not automate the decisions listed in section 11 unless the experiment is testing delegation.

## 15. Trade-off rules

When two priorities conflict, choose:

- learning over features;
- reliability over autonomy;
- evidence over novelty;
- evaluation over polish;
- trust over reach;
- the standard stack over framework changes without a research reason;
- simpler software over AI when simpler software is better;
- the repository and evidence over keeping every deployment alive;
- the daily time budget over portability work.

Live deployments may be retired.

## 16. Versioning

This document may evolve during the project.

When these principles change, record why. Valid reasons include:

- evidence from experiments;
- process friction;
- security findings;
- better evaluation practice;
- improved Agent Kit capabilities.

Do not update old experiments to match new principles. Let the history show how the methodology evolved.

---

## Version history

| Version | Notes |
| ------- | ----- |
| v0.1 | Initial draft based on `project-charter.md` v0.5 and planning decisions. |
| v0.2 | Clarified Eve’s role, native evals and approval gates, accepted Vercel/Eve coupling as a project trade-off, and tightened the learning principle. |
| v0.3 | Tightened language, removed repetition, turned principles into operating rules, and compressed Eve-specific guidance. |
| v0.4 | Cross-document pass: aligned terminology, related documents, evidence thresholds, Field Notes records, Research Register capitalisation, publication triage and Fieldwork Method naming. |
