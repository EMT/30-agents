# Agent #XX — Title

Guidance: draft this only after `evaluation.md` is complete and the README reflects the evidence. Use an article when the publication tier is Public. Use a case study when the tier is Private: build it only from redacted, synthetic or summarised evidence. Internal experiments do not produce this document; record a Waived state in the daily issue instead.

Guidance — style (distilled from the Agent #01 editing pass, 2026-08-20). The article must stand alone for a reader who knows nothing about the programme's internals:

- Open by explaining the practice problem in its own right, in two or three plain sentences, before stating the hypothesis. Describe the general problem and its mechanism (why it happens, what makes it hard), not a compressed hook — and don't frame a general problem as an AI-specific one when it applies to any process-improvement work.
- State the hypothesis precisely, including every half of a requirement. For example, if the agent must keep solutions out of its analysis, that has two directions — it must not propose solutions, and it must not let solution ideas in the input shape its analysis — and the hypothesis statement should carry both, in whatever wording fits the article, not just the catchier half.
- Explain or avoid insider terms at first use. "Evals" are scripted test cases and need a plain-language sentence before the word appears; say "fictional" rather than "synthetic"; say "known answers written into the test input" rather than "planted ground truth". Do not use autonomy-ladder labels (Suggest, Recommend) in prose — the plain form is behavioural: "the agent prepares analysis only; a human decides".
- Sanctioned plain forms for other programme terms: "eve" is "the agent framework used across the programme" (gloss once, then use the name); "the kit" and "scaffold" are "our shared tooling" or "the project starting point"; a "promoted" Field Note "was recorded for future experiments"; "research debt" is "open questions we've recorded for later". Adapt the gloss to the sentence rather than pasting it — "the default model we use" reads better than "the project starting point's default model".
- Describe mechanism, not abstraction: what the system actually does ("makes a single LLM call with its instructions and the transcript, returning structured markdown"), not what it "is" or where its behaviour "lives".
- State the hypothesis as the concrete artefact, not a self-assessment: "a structured map of friction points", not "a useful friction map". Usefulness is for the verdict to establish. This rule wins over the brief's or evaluation's literal hypothesis wording — restate, don't quote.
- Prefer plain connectives and ordinary sentences over aphorisms, em-dash appositions and metaphors ("quarantined", "wearing a question mark"). Cut words that manufacture atmosphere or immediacy the facts don't need: "quietly depends on" → "depends on", "has just recorded" → "has recorded". Conversational-practical register; "etc." is fine.
- One job per sentence. A sentence makes a claim, enumerates examples, or defines a term — never more than one of these. If a draft sentence needs an interrupting clause (an em-dash list, a "meaning…" or "which is…" aside) to finish its point, split it: give the definition its own short sentence before the term is used, and let examples follow as a separate sentence or list. Bad: "Mechanical checks assert facts about the output — the eight sections are present, every known friction point appears, each has an evidence line — and a judge model, meaning a second model given the output and scoring criteria, covers what mechanical checks cannot read." Good: "Mechanical checks assert facts about the output: the eight sections are present, every known friction point appears, and each has an evidence line. A judge model covers what those checks cannot read. The judge is a second model, given the output and scoring criteria."
- Use bullet lists when prose starts enumerating rules or results. Give each test case its own paragraph, in order ("The first case… The second case…").
- Do not lead with insider numbers (gate counts, judge percentages). Translate them into what was checked, or drop them.
- Length: aim for around 1,200–1,400 words of body text, with a hard cap of 2,000 in extreme cases; over 2,000 is allowed only in very extreme cases. Body text is everything between the "## What We Tested" heading and the "## Links" heading, including headings and bullets. "Extreme" means the article would lose significant data or meaning with fewer words, and there is no more concise way to write the same data and meaning. If substance must be compressed, start with Why This Matters and Production Notes — never the acknowledged evidence gaps.
- Reconcile counts and names across sections. If What Happened describes four test cases, the Verdict must not say "three scenarios" because a record phrased it that way — restate the record's substance in the article's own terms.
- The article summarises the records; it does not replace them. Say each thing once and let the linked records hold the rest: each caveat appears in one place (not re-hedged per section), justify the verdict in one direction (why not higher — skip why not lower), report the metrics a reader needs and leave the full table to the evaluation, and don't narrate the record-keeping itself ("this is recorded in the brief", "these are recorded for later"). Start sections with their content, not with a sentence announcing what the section is about.

## Source Links

- Publication tier (from the brief):
- Repository:
- README:
- Brief:
- Evaluation:
- Field Notes:
- Promotion Review:
- Evidence pack:
- Demo or screenshot:

Guidance: public content is derived from the repository. If a claim is not supported there, remove it or update the research record first. When no demo or screenshot exists, say so and link the nearest captured output (e.g. example outputs in `evidence/`) rather than leaving the field empty.

## What We Tested

TBD

Guidance: name the workflow, user, baseline and hypothesis. Keep this narrow; one problem and one hypothesis.

## Why This Matters

TBD

Guidance: explain the organisational outcome or workflow cost. Avoid hype and broad claims about AI.

## What We Built

TBD

Guidance: describe the working implementation at a practical level. Include the autonomy level and human approval points where relevant. The planned tests are part of the build: end this section by explaining the testing approach — that behaviour was checked with scripted test cases on fictional inputs with known answers written in, what the mechanical checks assert, and what a judge model scores. Do not enumerate the individual cases here; each case is introduced and resolved in What Happened, so it is described exactly once.

## What Happened

TBD

Guidance: summarise the representative case, baseline comparison and stress case. Open with results ("All four cases passed"), not test-setup explanation — the testing approach was already described at the end of What We Built. Then one paragraph per case, in order, each fusing a one-clause description of the case with its result: "The first case was a fictional walkthrough of a client-onboarding process, with eight known friction points written into it. The map found all eight…". Include failures, regressions or missing evidence. Run-level facts (what each case did, latency, what wasn't measured) belong here; Production Notes reframes cost and risk for deployment, it does not repeat the run story.

## Verdict

TBD

Guidance: use `Confirmed`, `Refined` or `Rejected`. State the verdict reason and confidence faithfully from `evaluation.md` — same substance, same caveats — but restated in the article's own register, not copied verbatim (records may use insider terms the style guidance bans). Do not re-enumerate the case results: point back to What Happened ("passed its pass criteria, as described above") and spend this section's words on the confidence reasoning. Confirmed does not mean production-ready.

## Field Notes

TBD

Guidance: include only observations promoted in `field-notes.md`, or state that no Field Notes were promoted.

## Production Notes

TBD

Guidance: briefly cover cost, maintenance, data, auth, permissions, auditability, human approval or deployment blockers when they affect trust or future work.

## What We Would Do Next

TBD

Guidance: describe future work without rewriting a rejected hypothesis as a success. New features belong in future experiments, backlog changes or research debt.

## Links

- Repository:
- Evaluation:
- Demo:

Guidance: this is the short reader-facing subset of Source Links, repeated at the end for readers who skip the front matter. The same demo-field rule applies.

## Publication Checks

- [ ] Evaluation is complete.
- [ ] README reflects the evidence.
- [ ] Evidence gaps are either resolved or acknowledged in the article itself, not only in the records.
- [ ] Claims are supported by the repository, evaluation or evidence pack.
- [ ] Sensitive data, credentials, customer information and internal operational details are removed, redacted or summarised.
- [ ] Output matches the declared publication tier.
- [ ] Verdict and confidence match `evaluation.md`.
- [ ] Language is direct, practical, specific and honest.
- [ ] Hype language has been removed.

Guidance: daily articles should be short. Weekly reviews and final synthesis carry the broader story.
