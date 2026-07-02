# 30 Agents in 30 Days — Evaluation Framework

**Version:** v0.4  
**Status:** Approved for planning  
**Owner:** Fieldwork  
**Related documents:** `project-charter.md`, `engineering-principles.md`, `content-strategy.md`

## 1. Purpose

This document defines the evidence required for each experiment.

An evaluation should answer:

- did the experiment test its hypothesis;
- what baseline it was compared against;
- whether it worked for the intended user or workflow;
- what it cost to build, run and maintain;
- what autonomy level it used and what autonomy level we would recommend;
- what organisational risks or production constraints matter;
- what should change in future work.

Evaluation does not prove production readiness. It supports the verdict, Field Notes and Promotion Review.

## 2. Non-negotiables

Every evaluation must record:

- hypothesis;
- baseline;
- minimum scenario set;
- verdict and reason;
- confidence level;
- implemented and recommended autonomy level;
- adoption or disuse risks;
- cost, effort and maintenance notes;
- safety and production-readiness notes.

If time is limited, reduce scope before reducing evaluation.

Do not publish based only on a happy-path run.

## 3. Evaluation timing

Evaluation starts before implementation.

Before coding, `brief.md` should define the hypothesis, assumptions, baseline, success criteria, first scenarios, intended user, expected autonomy level and main production concerns.

During implementation, capture evidence as it appears.

After implementation, run evaluation before polish, publication or social output.

## 4. Eve evals and manual evidence

Use Eve evals for repeatable behavioural checks: structured output validity, tool selection, refusal or approval behaviour, regression scenarios, repeated runs and rubric-scored output quality.

Eve evals are evidence. They are not the whole evaluation.

| Check type | Use when |
| --- | --- |
| Eve eval | Behaviour can be repeated and scored. |
| Manual scenario | The result needs human interpretation. |
| Human judgement | Adoption, trust, taste, ambiguity or risk matter. |
| Production-readiness note | The issue concerns deployment, permissions, data, audit or maintenance. |

Summarise automated eval results in `evaluation.md`. Raw logs are supporting evidence, not the source of truth.

## 5. Standard evaluation record

Use this table to structure `evaluation.md`.

| Dimension | Required record |
| --- | --- |
| Hypothesis and verdict | Hypothesis, verdict, reason, confidence, supporting evidence. |
| Baseline and value | Baseline, improvement or added capability, regressions, value vs effort, whether simpler software would be better. |
| Scenarios | Inputs, expected behaviour, observed behaviour, pass/partial/fail result. |
| Correctness | Incorrect outputs, missing outputs, recoverability, whether success criteria were met. |
| Reliability | Repeatability, tool-call reliability, structured output reliability, clear failures, silent failures. |
| Adoption | User, workflow fit, trust factors, disuse risks, legibility, override or correction needs. |
| Cost and maintenance | Setup, build, evaluation, publication, latency, model or token cost, tool calls, services, maintenance risks. |
| Autonomy | Implemented level, recommended level, rationale, approval gates used or needed. |
| Safety and production readiness | Data, auth, permissions, agent identity, audit, reversibility, failure recovery, observability, production blockers. |
| Reuse and promotion | Evidence for Agent Kit, module, template, pattern, recommendation or backlog changes. |

Promotion decisions belong in `promotion-review.md`. Evaluation provides the evidence.

## 6. Scenarios and baseline

Default scenario set:

- straightforward success case;
- realistic messy case;
- edge case;
- clarification, refusal or approval case;
- baseline comparison.

Minimum scenario set:

- representative intended-use case;
- baseline comparison;
- stress case: messy input, edge case, refusal, clarification, approval or failure recovery.

If the minimum cannot be met, reduce scope. If it still cannot be met, record the gap and publish with `Low` confidence.

Each scenario should record input, expected behaviour, pass criteria, observed output, result and notes.

Each evaluation must answer one of:

- Better than what?
- New capability at what cost?

Valid baselines include manual work, search, a spreadsheet, deterministic software, an existing product, doing nothing, or not currently possible.

If the baseline is “doing nothing” or “not currently possible,” evaluate value against effort, risk and maintenance burden. Do not force a better/worse comparison where the real question is whether the new capability is worth having.

If simpler software, doing nothing or a human process is better, say so.

## 7. Instruments

Use these instruments when completing the relevant dimensions in section 5.

### Adoption

| Question | Answer |
| --- | --- |
| Who would use this? |  |
| What job are they trying to do? |  |
| Where would this fit in their workflow? |  |
| What would they need to trust before using it? |  |
| What would cause them to ignore or abandon it? |  |
| What feedback or control would they need? |  |
| Would they use it once, occasionally or repeatedly? |  |

Record adoption risks as hypotheses unless tested with real users.

### Cost

Use estimates rather than false precision.

| Measure | Value | Notes |
| --- | --- | --- |
| Setup time |  |  |
| Build time |  |  |
| Evaluation time |  |  |
| Documentation/publication time |  |  |
| Runtime latency |  |  |
| Model/token cost |  |  |
| Tool calls |  |  |
| External services or credentials |  |  |
| Maintenance risks |  |  |

If a metric is unavailable, write `not measured`. Explain why only if the missing metric affects the verdict.

### Autonomy

| Level | Implemented? | Recommended? | Notes |
| --- | --- | --- | --- |
| Observe |  |  |  |
| Suggest |  |  |  |
| Recommend |  |  |  |
| Approve |  |  |  |
| Delegate |  |  |  |
| Automate |  |  |  |

Record what the agent was allowed to do, what a production version should be allowed to do, whether approval gates were used and where human judgement should remain.

`evaluation.md` is the source of truth for recommended autonomy level. The Research Register records a summary.

### Safety

| Question | Answer |
| --- | --- |
| What data does the agent handle? |  |
| Does it require authentication? |  |
| Does it require authorisation or permissions? |  |
| Would the agent need its own identity? |  |
| Could it take actions in another system? |  |
| Would actions need approval? |  |
| What should be logged or audited? |  |
| What is the worst plausible failure? |  |
| How would that failure be detected? |  |
| How would that failure be reversed or mitigated? |  |
| What would block production deployment? |  |

Private or internal-data experiments must not publish sensitive inputs, outputs, credentials, customer information or operational details. Use synthetic, redacted or summarised evidence.

## 8. Evidence pack

Always capture:

- `brief.md`;
- `README.md`;
- `evaluation.md`;
- `field-notes.md`, including when no Field Notes are promoted;
- `promotion-review.md`;
- representative inputs;
- representative outputs;
- screenshot when there is a visible interface or output.

Capture if it takes under 10 minutes or can be generated automatically:

- 30–60 second demo recording;
- architecture diagram;
- eval run output;
- cost estimate;
- latency or runtime metrics;
- logs or traces;
- baseline comparison notes.

Do not keep or publish evidence that creates avoidable data risk.

## 9. Verdict and confidence

Each experiment receives one verdict and one reason.

| Verdict | Use when | Record |
| --- | --- | --- |
| Confirmed | Evidence supports the hypothesis well enough to continue with the approach. | Why it was confirmed. |
| Refined | Evidence supports part of the hypothesis, but something should change. | What should change: scope, workflow, architecture, autonomy, UX, evaluation, cost, safety, maintenance or baseline. |
| Rejected | Evidence does not support the hypothesis. | Why: contradicted hypothesis, did not beat baseline, additive value did not justify effort, risk too high, cost unjustified, maintenance burden too high, adoption risk too high or simpler software would be better. |

Confirmed does not mean production-ready. Rejected is a valid outcome.

Record confidence separately from verdict.

| Confidence | Use when |
| --- | --- |
| Low | Evidence is thin, scenarios were limited, results were inconsistent, or the minimum scenario set was not met. |
| Medium | Scenarios were representative, included a baseline comparison and included at least one non-happy-path case. |
| High | Multiple scenarios, baseline comparison, failure cases and repeatability checks support the verdict. |

Most daily experiments will produce low or medium confidence.

Do not upgrade confidence because the agent is impressive. Upgrade confidence only because the evidence is stronger.

## 10. Calibration and downstream use

The synthesis depends on verdicts and confidence levels meaning roughly the same thing across thirty experiments.

Once a week, re-read recent verdicts and confidence levels against section 9, plus at least one earlier evaluation outside the current week.

Do not rewrite published experiments. If a verdict or confidence level needs reinterpretation, record the update in the Research Register or weekly review and link back to the original evaluation.

The source of truth for full verdict, confidence, recommended autonomy level and verdict reason is `evaluation.md`.

The Research Register records a summary: agent number, title, hypothesis, verdict, verdict reason, confidence, recommended autonomy level, key evidence, repository, demo and article or case study.

If the Research Register and `evaluation.md` disagree, `evaluation.md` wins unless the register explicitly records a later calibration note.

Promotion Review decides what moves into the Agent Kit, modules, templates, patterns or recommendations.

Field Notes record observations promoted from the experiment that may change future implementation, evaluation, scope, adoption, cost or deployment decisions.

## 11. Completion bar

An evaluation is complete when another person can understand:

- what was tested;
- what evidence was gathered;
- what passed and failed;
- what the verdict was;
- why that verdict was chosen;
- how confident we are;
- build/run costs, or `not measured` entries;
- what adoption or disuse risks exist;
- what production constraints matter;
- what should change tomorrow.

If the evaluation cannot answer these questions, the agent is not ready to publish.

---

## Version history

| Version | Notes |
| ------- | ----- |
| v0.1 | Initial draft based on `project-charter.md` v0.5 and `engineering-principles.md` v0.3. |
| v0.2 | Deduplicated adoption, cost and safety sections; clarified additive baselines; added scenario floor, verdict reasons and calibration. |
| v0.3 | Tightened for daily use; merged repeated sections, clarified non-negotiables, source of truth and completion bar. |
| v0.4 | Cross-document pass: aligned related documents, publication terminology, cost wording, Field Notes records, calibration wording and version status. |
