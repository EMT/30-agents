# Agent #XX — Daily Build Issue

Guidance: use this issue as the daily cockpit for one experiment. It should link to the approved brief, track the minimum work needed to evaluate the hypothesis and make publication blockers visible. Do not use it to expand scope after coding starts.

## Links

- Brief:
- Repository:
- Programme index entry:
- Research Register entry:
- Evidence pack:

## Publication Tier

TBD

Guidance: copy from the approved brief: Public, Private or Internal, as defined in `templates/operating/README.md`. After the brief freezes, the tier may only move toward less exposure; record the reason here. Moving toward more exposure needs a recorded human decision before publication.

## Goal

TBD

Guidance: one or two sentences. Name the workflow, user, baseline and hypothesis being tested. If the goal needs several "and" clauses, reduce scope before implementation.

## Brief Freeze

- [ ] Brief is approved.
- [ ] Hypothesis is explicit.
- [ ] Assumptions are recorded.
- [ ] Baseline is recorded.
- [ ] Initial scenarios are recorded.
- [ ] Scope still fits one narrow problem.
- [ ] Scope is frozen for implementation.

Guidance: once this section is checked, scope may shrink but should not expand. Put new ideas in backlog changes or research debt.

## Implementation Checklist

- [ ] Implement the smallest working version that tests the hypothesis.
- [ ] Use the standard stack unless the brief deliberately tests a variation.
- [ ] Add only the capabilities required by the brief.
- [ ] Include approval gates where the autonomy level requires them.
- [ ] Remove confusing dead code before publication.
- [ ] Document how to run or demonstrate the agent.

Guidance: prioritise learning about the hypothesis, workflow, adoption, cost, safety or future delivery. Do not spend daily build time on polish unless it affects evaluation.

## Evaluation Checklist

- [ ] Run representative intended-use case.
- [ ] Run baseline comparison.
- [ ] Run stress case.
- [ ] Record pass, partial or fail for each scenario.
- [ ] Record verdict reason.
- [ ] Record confidence level.
- [ ] Record implemented and recommended autonomy level.
- [ ] Record adoption or disuse risks.
- [ ] Record cost, maintenance, safety and production-readiness notes.

Guidance: do not publish from a happy-path run alone. If the minimum scenario set cannot be met, record the gap and use `Low` confidence.

## Evidence Checklist

- [ ] `brief.md` complete.
- [ ] `README.md` complete.
- [ ] `evaluation.md` complete.
- [ ] `field-notes.md` complete, including a note if no Field Notes were promoted.
- [ ] `promotion-review.md` complete.
- [ ] Representative inputs captured.
- [ ] Representative outputs captured.
- [ ] Screenshot captured when visible interface or output exists.
- [ ] Demo recording captured if under 10 minutes or automated.
- [ ] Cost, latency, logs or traces captured if available and safe.
- [ ] Missing required or optional evidence is recorded with reason and confidence impact.
- [ ] Sensitive or internal material removed, redacted or summarised.

Guidance: evidence supports the verdict. Raw logs are supporting evidence, not the source of truth.

## Promotion Review Checklist

- [ ] Template candidates reviewed.
- [ ] Module candidates reviewed.
- [ ] Pattern candidates reviewed.
- [ ] Field Notes candidates reviewed.
- [ ] Recommendation candidates reviewed only if repeated evidence exists or a major risk emerged.
- [ ] Backlog changes recorded.
- [ ] Research debt recorded.

Guidance: promotion requires evidence. Field Notes are observations; recommendations require repeated evidence unless a major risk clearly changes future work.

## Publication Checklist

- [ ] `README.md` reflects the evidence.
- [ ] `evaluation.md` is complete enough to support publication.
- [ ] `field-notes.md` records promoted notes or explicitly records none.
- [ ] `promotion-review.md` is complete.
- [ ] Research Register updated.
- [ ] Agent Index updated.
- [ ] Field Notes index updated when notes were promoted, or left unchanged when none were promoted.
- [ ] Backlog or research debt updated when the Promotion Review creates follow-up work.
- [ ] Article or case study is Done, Deferred or Waived in the publication tail record.
- [ ] Social posts are Done, Deferred or Waived in the publication tail record.

Publication tail record:

| Output | State (Done / Deferred / Waived) | Owner and next step, or waiver reason |
| --- | --- | --- |
| Article or case study | TBD | TBD |
| Social posts | TBD | TBD |

Guidance: public content comes after evaluation. Do not publish claims unsupported by the repository, evaluation or evidence pack. Deferred items need an owner and next step. Waived is the expected state for Internal experiments and needs a reason, not further work.

## Close Criteria

- [ ] Experiment is published or recorded as intentionally unpublished.
- [ ] Repository evidence is complete.
- [ ] Programme records are updated.
- [ ] Follow-up work is captured as backlog changes or research debt.
- [ ] Every publication tail item is Done, Deferred with an owner and next step, or Waived with a reason.

Guidance: close the issue when the experiment is published and recorded. If publication lags, make that explicit rather than leaving research work incomplete. An Internal experiment closes when its research record is complete and its tail items are Waived.
