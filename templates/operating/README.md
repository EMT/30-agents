# Operating Templates v0.2

These templates support the daily operating rhythm for 30 Agents in 30 Days.

Use them to reduce setup cost, make missing evidence visible and keep publication tied to the research record. They do not replace the foundation documents or human judgement.

## Source Of Truth

These templates are derived from:

- `docs/project-charter.md`
- `docs/engineering-principles.md`
- `docs/evaluation-framework.md`
- `docs/content-strategy.md`
- `docs/source-of-truth-map.md`

If a template conflicts with a foundation document on principles, evaluation or content rules, the foundation document wins. If a template conflicts with `docs/source-of-truth-map.md` on repository paths or ownership, the source-of-truth map wins.

## Templates

| Template | File | Use when |
| --- | --- | --- |
| Daily issue | `daily-issue.md` | Opening the daily GitHub issue that drives one experiment from brief to publication. |
| Evidence pack | `evidence-pack.md` | Checking whether the experiment has enough safe evidence to support the verdict and public output. |
| Article or case study | `article-or-case-study.md` | Drafting the short public write-up after evaluation and README are complete. |
| Social posts | `social-posts.md` | Drafting concise posts that point back to the repository, article or case study. |
| Weekly review | `weekly-review.md` | Calibrating verdicts, confidence levels, repeated findings and research debt across the week. |

## Publication Tiers

Each experiment declares one publication tier in its brief. The daily issue repeats the tier so the publication tail is judged against it.

| Tier | Meaning | Publication tail owed |
| --- | --- | --- |
| Public | The experiment can be shown with public, synthetic or user-provided data. | Article, social posts and public evidence links. |
| Private | The experiment uses internal, client or operational data that needs redaction. | Case study built from redacted, synthetic or summarised evidence; social posts may point to it. |
| Internal | The experiment is an internal run with no public output expected. | None. Record a waiver in the daily issue instead of leaving tail items open. |

Publication-tail items resolve in one of three states:

- `Done` — the output is published or ready to publish.
- `Deferred` — the output is still owed; record an owner and next step. Use when publishing lags or batches.
- `Waived` — the output is intentionally not produced; record the reason. This is the expected state for Internal experiments.

After the brief freezes, the tier may move only toward less exposure (Public → Private → Internal), with a one-line reason recorded in the daily issue. Moving toward more exposure requires a recorded human decision before publication.

## Source-Of-Truth Reminders

| Record | Owns |
| --- | --- |
| `brief.md` | Original hypothesis, assumptions, baseline, scope and approval. |
| `evaluation.md` | Verdict, verdict reason, confidence, autonomy recommendation and evaluation evidence. |
| `field-notes.md` | Promoted observations, or the record that no Field Notes were promoted. |
| `promotion-review.md` | Promotion decisions for templates, modules, patterns, recommendations and backlog changes. |
| Research Register | Programme-level summary of evaluation evidence and later calibration notes. |
| Agent Index | Programme-level experiment index and status. |

## How To Use

Copy the relevant template into the experiment repository, issue body or programme record.

Replace placeholder values such as `Agent #XX`, `TBD` and bracketed guidance notes. Keep guidance notes while drafting if they help; remove them before publication when they no longer add useful context.

Do not invent agent concepts while filling these templates. Start from the approved brief, completed evaluation, evidence pack, Field Notes and Promotion Review.

## Operating Rules

- Keep each experiment focused on one problem and one hypothesis.
- Evaluate before polish, article drafting or social output.
- Publish confirmed, refined and rejected hypotheses honestly.
- Record when evidence is missing instead of hiding the gap.
- Use synthetic, redacted or summarised evidence for private or internal-data experiments.
- Promote reusable work only through Promotion Review.
- Leave published experiments as immutable snapshots.

## Version Notes

v0.1 is the first operating set. Update these templates only when daily use shows that a change reduces friction, improves evidence quality or clarifies decisions.

v0.2 adds publication tiers and publication-tail states so internal and private experiments can record intentional deferrals or waivers without appearing incomplete. Resolves RD-000 from Agent #0.
