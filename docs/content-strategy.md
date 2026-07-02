# 30 Agents in 30 Days — Content Strategy

**Version:** v0.4  
**Status:** Approved for planning  
**Owner:** Fieldwork  
**Primary repository:** `30-agents`  
**Related documents:** `project-charter.md`, `engineering-principles.md`, `evaluation-framework.md`

## 1. Purpose

This document defines how experiment outputs become public evidence without creating a content treadmill.

Content has four jobs:

- explain what was built;
- show how it was evaluated;
- record what changed;
- make the work easy to trust and revisit.

The goal is trust, not reach.

## 2. Non-negotiables

Every published experiment must include:

- `README.md`;
- `brief.md`;
- `evaluation.md`;
- `field-notes.md`, even when no Field Notes were promoted;
- `promotion-review.md`;
- a public article or case study;
- a screenshot when there is a visible interface or output.

Capture if it takes under 10 minutes or can be generated automatically:

- 30–60 second demo recording;
- before/after or input/output examples;
- architecture diagram;
- cost or latency snapshot.

Do not publish an article or social post before the evaluation is complete and the README reflects the evidence.

Do not publish claims unsupported by the repository, evaluation or evidence pack.

Do not publish sensitive data, credentials, customer information or internal operational details.

## 3. Content principles

### Repository first

The repository is the source of truth. Articles, social posts, gallery entries and weekly summaries are derived from it.

If a public post conflicts with the repo, evaluation or Research Register, fix the public post. If the repo and Research Register disagree, use the source-of-truth rules in `evaluation-framework.md`.

### Research before publishing

Protect evaluation before article writing, social posting or visual polish.

On a compressed day, the article and social posts may lag or be batched. The evaluation and README may not.

### Trust over reach

Write for people who already know Fieldwork, or people who may hear about us through a trusted connection. Do not write for a generic AI audience.

### Short daily, deeper weekly

Daily content should be short. Weekly reviews and final synthesis carry the broader story.

### Show the evidence

Screenshots, examples, eval outputs, short recordings, architecture notes and verdicts are stronger than claims about what the agent can do.

### Publish rejections clearly

Confirmed, refined and rejected hypotheses are all valid. Do not soften a rejected hypothesis into “future work”.

### AI drafts; humans publish

Agents may draft, summarise, format, extract, update and suggest. Humans approve what is published, promoted or recommended.

## 4. Audiences

### Primary audience

People who already know Fieldwork:

- current clients;
- past clients;
- partners;
- collaborators;
- peers;
- people likely to recommend us.

The business aim is to shift how they describe Fieldwork: from a design and technology studio that builds digital products to one that can identify, design, build and deploy AI systems safely.

### Secondary audiences

- Technical decision-makers assessing Fieldwork’s engineering depth.
- Product and design leaders exploring where AI belongs in workflows.
- Engineers interested in practical agent implementation.
- Future hires or collaborators.

## 5. Source of truth

| Artefact | Owns |
| --- | --- |
| Agent repo | Complete record of one experiment. |
| `README.md` | Canonical public summary. |
| `brief.md` | Original hypothesis, assumptions, baseline and scope. |
| `evaluation.md` | Verdict, confidence, autonomy recommendation and evidence. |
| `field-notes.md` | Observations promoted from the experiment, or a record that no Field Notes were promoted. |
| `promotion-review.md` | What should graduate into the Agent Kit, templates, patterns or recommendations. |
| `30-agents` repo | Programme index, Research Register, Field Notes index, weekly summaries and synthesis drafts. |
| Website/social | Public views derived from the research record. |

Do not maintain separate narratives across repo, article and social.

## 6. Daily flow

The standard flow is:

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

## 7. README

The README should let another person understand the experiment in five minutes.

Recommended structure:

```md
# Agent #XX — Title

## Summary

## Problem

## Hypothesis

## Baseline

## Approach

## How it works

## Evaluation summary

## Verdict

## Field Notes

## Promotion Review

## Demo / recording

## Repository structure

## Running locally
```

A technical reader should understand what was built, how it was evaluated and what conclusion was reached without reading the article.

## 8. Daily article or case study

Daily articles should be short and repeatable.

Recommended structure:

```md
# Agent #XX — Title

## What we tested

## Why this matters

## What we built

## What happened

## Verdict

## Field Notes

## What we would do next

## Links
```

Use a public article when the agent can be shown with public, synthetic or user-provided data.

Use a case study when the agent uses internal data or cannot be made public. Case studies may use redacted screenshots, architecture notes, summarised evidence or a short recording.

Avoid long setup stories. The useful content is the problem, hypothesis, evidence, verdict and what changed.

## 9. Field Notes

Field Notes are observations from the day’s experiment that may affect future work.

Capture notes about:

- reusable patterns;
- changed assumptions;
- unexpected failures;
- design or adoption insights;
- cost, maintenance or safety concerns;
- backlog changes;
- questions for later synthesis.

Capture what the day produced. Some days will produce several notes. Some days may produce one. Some days may produce none.

Do not target a number. Do not pad.

If no observation is worth keeping, record that no Field Notes were promoted from the experiment.

Format:

```md
## Field Notes — Agent #XX

### FN-XXX — Short title

Observation:

Evidence:

Why it matters:

Related experiments:
```

Field Notes are not recommendations. Recommendations require repeated evidence.

## 10. Social posts

Social posts should point to the evidence, not replace it.

Daily posts should usually include:

- agent number and title;
- problem tested;
- one finding;
- verdict if relevant;
- screenshot, clip or diagram;
- link to article or repo.

Recommended channels:

- LinkedIn for clients, partners and longer reflections;
- short-form channels for concise technical notes;
- Fieldwork website as the durable public home.

Avoid engagement bait, generic AI commentary, unsupported claims and platform-specific hacks.

## 11. Screenshots and recordings

Capture a screenshot when there is a visible interface or output.

Capture a 30–60 second recording if it takes under 10 minutes or can be generated automatically.

The recording should show:

- the input;
- the agent acting;
- the output;
- any approval or correction step;
- the result.

For private agents, record an internal demo if it fits the threshold, and publish only redacted or synthetic material.

Screenshots should show the work product, not just a chat box.

## 12. Weekly synthesis and calibration

Weekly synthesis turns daily outputs into programme-level evidence.

Each week, review:

- completed experiments;
- verdicts and confidence levels;
- whether verdicts and confidence levels are being applied consistently;
- at least one earlier evaluation to anchor calibration;
- Field Notes;
- Promotion Reviews;
- adoption, cost, autonomy and safety patterns;
- backlog changes;
- research debt;
- contradictions or repeated findings.

Weekly outputs may include:

- short public recap;
- internal research note;
- Field Notes index update;
- emerging recommendation update;
- Research Register calibration note.

Do not force a weekly article if there is no synthesis to publish.

Do not rewrite published evaluations during calibration. Record reinterpretations or consistency notes in the Research Register or weekly summary and link back to the original evaluation.

## 13. Final synthesis

After Day 30, the daily content becomes source material for:

- the Fieldwork Method for designing AI systems;
- engineering recommendations;
- adoption and disuse guidance;
- safety and production-readiness guidance;
- cost and maintenance reflections;
- patterns and anti-patterns;
- “what we would not build” articles;
- follow-up research tracks.

The final synthesis should cite experiments as evidence. The agents support the method; they are not the method.

## 14. AI-assisted content production

AI should reduce publishing overhead.

Agents may help:

- draft READMEs from briefs, evaluations and Promotion Reviews;
- draft articles from READMEs;
- extract Field Notes from evaluations;
- draft social posts;
- update the Research Register;
- prepare weekly summaries;
- check for missing evidence;
- prepare tomorrow’s GitHub issue.

Humans remain responsible for:

- approving Field Notes;
- approving verdicts and recommendations;
- deciding what gets published;
- checking factual accuracy;
- removing sensitive information;
- preserving Fieldwork’s voice.

Do not let AI-generated content add length. Use AI to compress, structure and clarify.

## 15. Voice and editorial standards

Write like Fieldwork: direct, practical, specific and honest.

Prefer:

- concrete nouns;
- short sentences;
- specific evidence;
- clear verdicts;
- plain descriptions of trade-offs.

Avoid:

- “transformative”;
- “revolutionary”;
- “unlock”;
- “seamless”;
- “game-changing”;
- “learnings” when “notes”, “findings” or “evidence” is clearer;
- broad claims about the future of AI;
- claims that are not supported by the experiment.

Use “we” when describing Fieldwork’s decisions. Use “the agent” when describing behaviour. Do not anthropomorphise agents unless the experiment is explicitly about agent identity or collaboration.

## 16. Time budget

Publishing must not threaten the challenge.

These targets assume AI-assisted drafting as described in section 14.

Target daily content budget:

| Task | Target |
| --- | ---: |
| Complete README | 20 min |
| Draft/edit article or case study | 20 min |
| Capture screenshot or recording | 10 min |
| Draft/edit social posts | 10 min |
| Update central index/register | 10 min |

If the content budget slips, reduce article length before reducing evaluation quality.

A short, evidence-backed post is better than a polished essay that delays tomorrow’s work.

## 17. What we do not optimise for

We do not optimise for:

- virality;
- daily novelty;
- long posts;
- platform-specific hacks;
- posting before the evidence is ready;
- making every agent look successful;
- publishing private or sensitive material;
- maintaining separate narratives across repo, article and social.

Content should make the research easier to understand and easier to trust.

## 18. Version history

| Version | Notes |
| --- | --- |
| v0.1 | Initial draft based on approved project documents and planning decisions. |
| v0.2 | Added weekly calibration, removed Field Notes quota, clarified daily publishing triage, aligned evidence threshold wording and tied time budget to AI-assisted drafting. |
| v0.3 | Final signal-to-noise pass: removed publishing-theatre language, clarified source-of-truth rules, tightened daily triage, preserved calibration and aligned evidence thresholds. |
| v0.4 | Cross-document pass: aligned related documents, source-of-truth conflict handling, Field Notes ownership, daily Promotion Review order and version status. |
