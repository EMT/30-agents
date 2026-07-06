# Evidence Pack — Agent #XX

Guidance: use this checklist before publication. The evidence pack should let another person understand what was tested, what happened and why the verdict is credible. Do not keep or publish evidence that creates avoidable data risk.

## Summary

| Field | Value |
| --- | --- |
| Agent | #XX |
| Title | TBD |
| Repository | TBD |
| Evaluation | TBD |
| Verdict | TBD |
| Confidence | TBD |
| Evidence owner | TBD |

Guidance: copy verdict and confidence from `evaluation.md`. If the Research Register disagrees, `evaluation.md` is the source of truth unless the register records a later calibration note.

## Required

| Evidence | Location | Status | Notes |
| --- | --- | --- | --- |
| `brief.md` | TBD | TBD | TBD |
| `README.md` | TBD | TBD | TBD |
| `evaluation.md` | TBD | TBD | TBD |
| `field-notes.md` | TBD | TBD | TBD |
| `promotion-review.md` | TBD | TBD | TBD |
| Representative inputs | TBD | TBD | TBD |
| Representative outputs | TBD | TBD | TBD |
| Screenshot when there is a visible interface or output | TBD | TBD | TBD |

Guidance: use `present`, `missing`, `not applicable` or `unsafe to publish` for status. These are required for every published experiment. `field-notes.md` should still exist when no Field Notes were promoted.

## Capture If Under 10 Minutes Or Automated

- [ ] 30-60 second demo recording
- [ ] Before/after or input/output examples
- [ ] Architecture diagram
- [ ] Cost or latency snapshot
- [ ] Eval run output
- [ ] Logs or traces
- [ ] Baseline comparison notes

Guidance: capture these when they are cheap and safe. Do not let optional evidence displace evaluation work.

## Missing Or Withheld Evidence

| Evidence | Reason | Confidence impact | Follow-up |
| --- | --- | --- | --- |
| TBD | TBD | TBD | TBD |

Guidance: record gaps explicitly. Missing evidence should usually reduce confidence unless it is not applicable or unsafe to publish.

## Scenario Evidence

| Scenario | Evidence location | Result | Notes |
| --- | --- | --- | --- |
| Representative intended-use case | TBD | TBD | TBD |
| Baseline comparison | TBD | TBD | TBD |
| Stress case | TBD | TBD | TBD |

Guidance: use pass, partial or fail for result. The minimum scenario set is representative case, baseline comparison and one stress case.

## Cost And Runtime Evidence

| Measure | Evidence location | Value | Notes |
| --- | --- | --- | --- |
| Setup time | TBD | TBD | TBD |
| Build time | TBD | TBD | TBD |
| Evaluation time | TBD | TBD | TBD |
| Runtime latency | TBD | TBD | TBD |
| Model/token cost | TBD | TBD | TBD |
| Tool calls | TBD | TBD | TBD |
| External services | TBD | TBD | TBD |

Guidance: estimates are acceptable. Use `not measured` when unavailable.

## Data Safety Check

- [ ] No credentials
- [ ] No sensitive customer data
- [ ] No unnecessary internal operational details
- [ ] Private evidence is synthetic, redacted or summarised
- [ ] Evidence does not disclose unsafe permissions, tokens, secrets or customer information.

Guidance: for internal-data experiments, publish redacted screenshots, summarised evidence, architecture notes or synthetic examples.

## Evidence Summary

TBD

Guidance: briefly state the strongest evidence, the weakest evidence and any gap that affects confidence.
