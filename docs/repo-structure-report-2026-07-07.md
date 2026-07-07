# Repository Structure Report

Date: 2026-07-07

Scope: checked `AGENTS.md`, the four foundation documents, `docs/source-of-truth-map.md`, the historical planning records, `README.md`, registers, backlog files, research backlog, templates and directory READMEs. Foundation documents were not changed.

This report re-audits the repository after the 2026-07-06 report (`docs/repo-structure-report.md`) and the work that followed it: the source-of-truth map, Agent #0 dry-run records, Agent #01 preparation and the candidate review.

## Summary

The repository now matches its own current structure contract. Every path listed in `docs/source-of-truth-map.md` exists, the historical planning documents carry clear banners, `backlog/master-backlog.md` holds an approved first-10 sequence, and the registers record Agent #0 and Agent #01 consistently with each other and with the external repositories, which exist at the linked GitHub locations.

The planning summary's original repository plan (flat `templates/`, records under `research/`, `agents/index.md`) still differs from the implemented structure, but that document is explicitly marked historical and the source-of-truth map records the decision, so this is documented drift, not a mismatch. Remaining findings are small housekeeping items and one open research-debt item that is sequenced before Agent #01.

## Missing Files

Checked against `docs/source-of-truth-map.md`, nothing is missing: all 23 canonical paths exist, and `templates/agent-repo/` contains all six files required by `AGENTS.md` and `engineering-principles.md` section 6.

Checked against the historical plan in `docs/planning-summary.md`, the previously reported gaps (`templates/*.md`, `research/research-register.md`, `agents/index.md`, `templates/github-issue.md`) remain "missing" only in the sense that the plan was superseded; each has a documented replacement. No action needed.

Genuinely empty areas, all expected at this stage:

- `evidence/`, `weekly-reviews/` and `synthesis/` contain only READMEs. The first weekly review will be due at the end of week one.
- `backlog/master-backlog.md` and `registers/agent-index.md` cover only Agents #01–#10. Agents #11–#30 exist only as the provisional 20 in `backlog/candidate-review.md`; no file records how or when they get promoted into the master backlog.

## Outdated References

- `README.md` does not link `backlog/candidate-review.md`, added in the most recent commit, although it links every other backlog and register file. The source-of-truth map says `README.md` should be corrected when it lags the map on paths.
- `docs/source-of-truth-map.md` is dated 2026-07-06 but already lists `backlog/candidate-review.md` (dated 2026-07-07). Bump the date when the map next changes.
- `docs/source-of-truth-map.md` describes `docs/repo-structure-report.md` as "Dated audit report"; with this second report, that entry should become a pattern (dated audit reports) or list both files.
- `docs/repo-structure-report.md` recommendations 2 (clarify backlog ownership), 3 (promote the initial backlog) and 6 (review operating templates) have since been resolved by the master backlog, candidate review and template-tightening commits, but only 1, 4 and 7 are marked resolved. A one-line resolution note would close the loop; the report is otherwise correctly framed as dated evidence.
- `registers/recommendations.md` contains a placeholder row `REC-001` with every field `TBD` and status `Candidate`. An all-TBD row reads as if a candidate recommendation exists. Prefer an empty table or a "none yet" note.

## Contradictions

- **FN-000 status.** `registers/field-notes-index.md` lists FN-000 as `Candidate`, while `registers/research-register.md` records that Agent #0 "promoted FN-000". Under the source-of-truth rules, `field-notes.md` in the Agent #0 repository owns promotion; whichever state is correct, the two programme records should agree.
- **No promotion path for the provisional 20.** `backlog/master-backlog.md` calls itself the canonical execution queue and `backlog/candidate-review.md` explicitly defers to it, so there is no conflict of authority — but neither file states when or how provisional candidates are promoted (per wave, weekly review, or on demand). Without that, week-two planning could drift back into `research/backlog.md`.
- No contradictions found between the four foundation documents, `AGENTS.md`, the source-of-truth map and the operating templates. Lifecycle order (evaluation → Promotion Review → Field Notes), source-of-truth ownership, verdict/confidence vocabulary and the required agent-repo file set are consistent everywhere they appear.

## Recommended Next PRs

1. **Resolved by PR #15: resolve RD-000 before Agent #01 implementation.** Operating templates v0.2 added publication tiers (Public / Private / Internal) and Done / Deferred / Waived tail states across `daily-issue.md`, `article-or-case-study.md`, `social-posts.md` and `brief.md`. Note: the already-prepared Agent #01 daily issue in `agent-01-friction-cartographer` predates the format and still needs the tier field.
2. **Resolved by PR #16: housekeeping pass on programme records.** Candidate review linked from `README.md`; FN-000 reconciled to `Promoted` per the owning `field-notes.md` in the Agent #0 repository; `REC-001` placeholder replaced with a none-yet note; source-of-truth map date bumped and both dated reports listed.
3. **Resolved by PR #17: record the backlog promotion mechanism.** `backlog/master-backlog.md` now records the wave-based promotion mechanism, and the weekly-review template's Backlog Changes guidance points at it (operating templates v0.3).
4. **Resolved by PR #18: mark resolved recommendations in the 2026-07-06 report.** Resolution notes added for its recommendations 2, 3 and 6, matching the treatment its other recommendations already received.
