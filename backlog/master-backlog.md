# Master Backlog

This is the canonical execution queue for approved programme sequencing.

`research/backlog.md` remains the draft candidate pool and coverage planning document. Promote changes here only when evidence, research gaps or sustainability make the sequence stronger.

The backlog is a hypothesis, not a contract.

Change it when evidence suggests a better experiment, a research gap appears, fresh insight suggests a stronger question, or scope needs adjustment for sustainability.

Do not change it because of hype, novelty or boredom.

## Promotion Mechanism

Agents #11–#30 are not approved yet. They exist as the provisional 20 and the reserve pool in `backlog/candidate-review.md`, drawn from the candidate pool in `research/backlog.md`.

Promotion into this queue works as follows:

- Review the queue at each weekly calibration, or sooner if fewer than five approved experiments remain unstarted.
- Promote in waves of five to ten, keeping the provisional order from `backlog/candidate-review.md` unless evidence from completed experiments supports a change.
- Record a reason for each promotion, swap or demotion: evidence, a research gap, a stronger question or sustainability. Not hype, novelty or a flashier demo.
- When a candidate is promoted, add its row here with status `Selected` and add a matching row to `registers/agent-index.md` with status `Planned`.
- Record the intended publication tier (Public / Private / Internal) in the row when promoting — the Agent Kit scaffolds the repo with it. The brief confirms the tier at freeze; after freeze it may only move toward less exposure.
- Record swaps from the reserve pool, and any demotions, in the weekly review's Backlog Changes section with the supporting evidence.

## Approved Queue

| Priority | Agent # | Working title | Problem | Hypothesis | Target user / workflow | Primary research question | Tier | Status | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | #01 | Friction Cartographer | Teams often start AI conversations from possible automation rather than observed workflow pain. | An agent can turn a recorded workflow walkthrough into a useful friction map before proposing any solution. | Designer, strategist or delivery lead observing an operational task. | RQ1, RQ2 | Public | Prepared | Repository and daily issue prepared; implementation not started. |
| 2 | #02 | Meeting Evidence Extractor | Meeting notes often lose decisions, risks and evidence behind follow-up actions. | An agent can extract decisions, open questions, evidence and owner/action pairs from transcripts better than a generic summary. | Project manager or delivery lead after client or internal meetings. | RQ2, RQ3, RQ4 | TBD | Selected | Synthetic data, structured outputs and clear baseline. |
| 3 | #03 | Anti-Agent | Teams can reach for AI before testing whether the problem needs an agent at all. | An agent designed to argue against agentic automation can improve brief quality by identifying simpler baselines, non-AI options and adoption risks before coding starts. | Project sponsor or builder preparing an experiment brief. | RQ1, RQ6 | TBD | Selected | Tests whether the programme should build an agent for a proposed problem. |
| 4 | #04 | Proposal Risk Reviewer | Delivery risks in proposals are easy to miss before they become commitments. | An agent can flag ambiguous scope, risky assumptions and missing constraints early enough to improve proposal review. | Delivery lead reviewing a proposal before it is sent. | RQ2, RQ3, RQ5 | TBD | Selected | Judgement support with human final authority. |
| 5 | #05 | Support Intake Classifier | Support requests arrive with missing context and inconsistent severity labels. | An agent can classify support requests, ask for missing information and suggest routing more reliably than first-pass manual sorting. | Support or operations team handling incoming tickets. | RQ1, RQ2, RQ4 | TBD | Selected | Clarification and routing without real external actions. |
| 6 | #06 | Case Study Drafting Assistant | Turning project evidence into a clear case study is time-consuming and prone to unsupported claims. | An agent can draft a short case study from approved source materials while preserving evidence boundaries and voice. | Studio team preparing public or private project write-ups. | RQ2, RQ3, RQ6 | TBD | Selected | Supports programme content while testing evidence boundaries. |
| 7 | #07 | Trust Designer | It is unclear how much explanation users need before they trust an agent recommendation, and when explanation becomes clutter. | A controlled interface that progressively hides rationale, evidence and uncertainty can reveal where trust collapses for a specific workflow. | Designer or product lead testing an AI recommendation pattern with internal reviewers. | RQ2, RQ4 | TBD | Selected | Makes trust and adoption an explicit experiment. |
| 8 | #08 | Scope Change Assessor | Small requested changes often hide schedule, budget or dependency impact. | An agent can turn a requested change into a structured impact note that helps a delivery lead decide whether to accept, defer or re-estimate it. | Delivery lead reviewing client change requests. | RQ1, RQ2, RQ4, RQ6 | TBD | Selected | Decision preparation without owning commercial judgement. |
| 9 | #09 | Accessibility QA Agent | Accessibility checks often miss content, interaction and context issues that automated linters cannot fully capture. | An agent combining automated checks with guided review can produce more useful accessibility QA notes than a raw linter report. | Designer or frontend engineer reviewing a page before release. | RQ1, RQ2, RQ3 | TBD | Selected | Tests deterministic tooling plus AI interpretation. |
| 10 | #10 | Sensitive Data Redactor | Teams need to share examples publicly or internally without leaking sensitive details. | An agent plus deterministic checks can redact sensitive data more usefully than manual review alone. | Team preparing evidence packs, case studies or support examples. | RQ3, RQ5 | TBD | Selected | Brings safety and publication constraints into the first third. |
