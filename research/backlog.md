# Research Backlog

Status: Draft planning proposal  
Last updated: 2026-07-01  

This backlog is a research planning artefact for 30 Agents in 30 Days. It is not an implementation plan, delivery commitment or approved sequence.

The backlog follows the foundation documents:

- start from workflows, users, baselines, hypotheses and assumptions;
- keep each experiment narrow enough to build, evaluate and publish;
- prefer the standard stack unless the experiment is deliberately testing a variation;
- use public demos where data can be synthetic, public or user-provided;
- use private case studies where real internal, client or operational data would create avoidable risk;
- treat the list as a hypothesis and revise it when evidence creates a better research path.

## Research Questions

| ID | Research question |
| --- | --- |
| RQ1 | When should an organisation use an AI agent rather than simpler software, workflow redesign or no automation? |
| RQ2 | What makes people trust, adopt and keep using an AI system? |
| RQ3 | What engineering patterns produce reliable AI systems? |
| RQ4 | How should autonomy be designed across observe, suggest, recommend, approve, delegate and automate? |
| RQ5 | What does safe deployment require inside organisations? |
| RQ6 | What do AI systems cost to build, run and maintain, and when is the cost justified? |

## Proposed Coverage Matrix

| Track | Primary research questions | Target coverage | Candidate agents |
| --- | --- | ---: | --- |
| Intake, triage and routing | RQ1, RQ2, RQ4 | 5 | Lead Triage Agent; Support Intake Classifier; Grant Eligibility Screener; Inbox Prioritiser; Research Request Router |
| Review, QA and risk assessment | RQ2, RQ3, RQ5 | 6 | Proposal Risk Reviewer; Contract Red-Flag Assistant; Accessibility QA Agent; Release Notes QA Agent; Data Quality Sentinel; Policy Drift Checker |
| Knowledge retrieval and synthesis | RQ1, RQ2, RQ3 | 6 | Project Memory Agent; Research Pack Builder; Meeting Evidence Extractor; Decision Log Curator; Competitor Change Monitor; Source Citation Checker |
| Content and communication workflows | RQ2, RQ3, RQ6 | 6 | Case Study Drafting Assistant; Tone-of-Voice Reviewer; Social Evidence Extractor; Bid Response Assembler; Customer Update Drafter; Internal Comms Summariser |
| Planning and operations | RQ1, RQ4, RQ6 | 7 | Scope Change Assessor; Sprint Planning Assistant; Resource Allocation Adviser; Delivery Risk Radar; Procurement Comparison Agent; Maintenance Triage Agent; Runbook Rehearsal Agent |
| Data extraction and structured outputs | RQ3, RQ5, RQ6 | 6 | Receipt Coding Assistant; CSV Reconciliation Agent; Form-to-CRM Agent; Invoice Exception Reviewer; Compliance Evidence Extractor; Spreadsheet Formula Auditor |
| Human approval and delegated action | RQ4, RQ5 | 5 | Calendar Negotiation Agent; GitHub Issue Groomer; CRM Follow-up Agent; Slack Decision Capture Agent; Vendor Renewal Assistant |
| Production constraints and safety | RQ3, RQ5, RQ6 | 4 | Permission Boundary Tester; Audit Trail Explainer; Sensitive Data Redactor; Incident Postmortem Assistant |
| Design discovery, trust and meta-research | RQ1, RQ2, RQ4, RQ6 | 5 | Friction Cartographer; Anti-Agent; Decision Archaeologist; Trust Designer; Recommendation Diff |

Coverage goals:

- Include at least five experiments where a simpler non-agent baseline may win.
- Include at least five experiments where human approval is a central design feature.
- Include at least five experiments using private or redacted case studies to test organisational constraints.
- Include at least five experiments that stress structured outputs, validation and repeatability.
- Include at least three experiments that deliberately test cost, maintenance or setup burden as the main question.
- Include at least three design-led or meta-research experiments that test whether Fieldwork is identifying the right problem before building.
- Avoid clustering the first ten around one workflow or one public-demo format.

## Candidate Agent Concepts

### 1. Lead Triage Agent

- Title: Lead Triage Agent
- Category: Intake, triage and routing
- Problem: Incoming enquiries vary in quality, urgency and fit, and manual triage is inconsistent.
- Hypothesis: An agent can classify inbound leads by fit, urgency and next action more consistently than ad hoc inbox review.
- Likely user/workflow: Founder, sales lead or studio partner reviewing new website, email or referral enquiries.
- Baseline: Manual inbox review and memory-based judgement.
- Public demo or private case study: Public demo with synthetic enquiries.
- Research question covered: RQ1, RQ2, RQ4
- Likely stack additions: Email or form fixture input; structured output schema; optional CRM mock.
- Risk/complexity: Medium; subjective fit scoring needs calibration and careful language.
- Why this belongs in the programme: Tests a common business workflow where AI may help with prioritisation without taking irreversible action.

### 2. Proposal Risk Reviewer

- Title: Proposal Risk Reviewer
- Category: Review, QA and risk assessment
- Problem: Delivery risks in proposals are easy to miss before they become commitments.
- Hypothesis: An agent can flag ambiguous scope, risky assumptions and missing constraints early enough to improve proposal review.
- Likely user/workflow: Delivery lead reviewing a proposal before it is sent.
- Baseline: Manual senior review.
- Public demo or private case study: Private case study with redacted proposal excerpts or synthetic proposals.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Document parsing; rubric-scored evals; redaction step.
- Risk/complexity: Medium; false confidence is the main risk.
- Why this belongs in the programme: Tests judgement support in a high-value workflow where humans must retain final authority.

### 3. Meeting Evidence Extractor

- Title: Meeting Evidence Extractor
- Category: Knowledge retrieval and synthesis
- Problem: Meeting notes often lose decisions, risks and evidence behind follow-up actions.
- Hypothesis: An agent can extract decisions, open questions, evidence and owner/action pairs from transcripts better than a generic summary.
- Likely user/workflow: Project manager or delivery lead after client or internal meetings.
- Baseline: Manual notes or generic transcript summary.
- Public demo or private case study: Public demo with synthetic transcript.
- Research question covered: RQ2, RQ3, RQ4
- Likely stack additions: Transcript fixture set; structured output schema; approval checklist.
- Risk/complexity: Low to medium; ambiguity and missing context can produce invented certainty.
- Why this belongs in the programme: A strong early experiment for structured outputs, workflow fit and human correction.

### 4. Scope Change Assessor

- Title: Scope Change Assessor
- Category: Planning and operations
- Problem: Small requested changes often hide schedule, budget or dependency impact.
- Hypothesis: An agent can turn a requested change into a structured impact note that helps a delivery lead decide whether to accept, defer or re-estimate it.
- Likely user/workflow: Delivery lead reviewing client change requests.
- Baseline: Manual judgement in Slack, email or project tools.
- Public demo or private case study: Public demo with synthetic project context.
- Research question covered: RQ1, RQ2, RQ4, RQ6
- Likely stack additions: Project brief fixture; impact rubric; optional approval gate.
- Risk/complexity: Medium; value depends on context quality.
- Why this belongs in the programme: Tests whether agents can improve decision preparation without pretending to own commercial judgement.

### 5. Case Study Drafting Assistant

- Title: Case Study Drafting Assistant
- Category: Content and communication workflows
- Problem: Turning project evidence into a clear case study is time-consuming and prone to unsupported claims.
- Hypothesis: An agent can draft a short case study from approved source materials while preserving evidence boundaries and voice.
- Likely user/workflow: Studio team preparing public or private project write-ups.
- Baseline: Manual drafting from notes, decks and project memory.
- Public demo or private case study: Public demo with synthetic project pack.
- Research question covered: RQ2, RQ3, RQ6
- Likely stack additions: Source pack ingestion; citation/evidence checker; voice rubric.
- Risk/complexity: Medium; unsupported claims and tone drift are key risks.
- Why this belongs in the programme: Directly supports the programme's content workflow while testing evidence-grounded generation.

### 6. Contract Red-Flag Assistant

- Title: Contract Red-Flag Assistant
- Category: Review, QA and risk assessment
- Problem: Non-lawyers need to spot obvious contract risks before legal review.
- Hypothesis: An agent can identify common red flags and questions for human/legal review without providing legal advice.
- Likely user/workflow: Founder or operations lead screening supplier or client terms.
- Baseline: Manual reading, search and escalation.
- Public demo or private case study: Public demo with sample public clauses; no real legal reliance.
- Research question covered: RQ2, RQ5
- Likely stack additions: Clause parser; refusal/limitation behaviour; red-flag taxonomy.
- Risk/complexity: High; must avoid legal advice and false assurance.
- Why this belongs in the programme: Stress-tests safety boundaries, disclaimers and escalation in a familiar organisational workflow.

### 7. Research Pack Builder

- Title: Research Pack Builder
- Category: Knowledge retrieval and synthesis
- Problem: Preparing context for a workshop or discovery call takes repeated search, reading and summarising.
- Hypothesis: An agent can assemble a concise research pack with sources, caveats and unknowns faster than manual desk research.
- Likely user/workflow: Strategist or designer preparing for a client discovery session.
- Baseline: Manual web research and notes.
- Public demo or private case study: Public demo using public sources.
- Research question covered: RQ1, RQ2, RQ3, RQ6
- Likely stack additions: Web search; citation handling; source quality rubric.
- Risk/complexity: Medium to high; current-source accuracy and citation quality matter.
- Why this belongs in the programme: Tests retrieval, synthesis and evidence quality in a practical pre-work workflow.

### 8. Support Intake Classifier

- Title: Support Intake Classifier
- Category: Intake, triage and routing
- Problem: Support requests arrive with missing context and inconsistent severity labels.
- Hypothesis: An agent can classify support requests, ask for missing information and suggest routing more reliably than first-pass manual sorting.
- Likely user/workflow: Support or operations team handling incoming tickets.
- Baseline: Manual triage in helpdesk or inbox.
- Public demo or private case study: Public demo with synthetic tickets.
- Research question covered: RQ1, RQ2, RQ4
- Likely stack additions: Ticket fixture set; classification schema; clarification behaviour evals.
- Risk/complexity: Medium; incorrect severity can harm response quality.
- Why this belongs in the programme: Tests clarification, routing and constrained autonomy in a common operational pattern.

### 9. Accessibility QA Agent

- Title: Accessibility QA Agent
- Category: Review, QA and risk assessment
- Problem: Accessibility checks often miss content, interaction and context issues that automated linters cannot fully capture.
- Hypothesis: An agent combining automated checks with guided review can produce more useful accessibility QA notes than a raw linter report.
- Likely user/workflow: Designer or frontend engineer reviewing a page before release.
- Baseline: Manual QA plus automated accessibility tooling.
- Public demo or private case study: Public demo against a sample page.
- Research question covered: RQ1, RQ2, RQ3
- Likely stack additions: Browser automation; axe or similar checker; screenshot capture.
- Risk/complexity: Medium; must distinguish tool findings from judgement calls.
- Why this belongs in the programme: Tests the boundary between deterministic tools and AI interpretation.

### 10. Decision Log Curator

- Title: Decision Log Curator
- Category: Knowledge retrieval and synthesis
- Problem: Important decisions are scattered across Slack, issues, docs and meeting notes.
- Hypothesis: An agent can propose decision-log entries with evidence links and confidence levels, reducing knowledge loss.
- Likely user/workflow: Project lead maintaining an ADR or decision log.
- Baseline: Manual decision capture, often omitted.
- Public demo or private case study: Private case study with redacted internal channels, or public demo with synthetic project artefacts.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Slack/GitHub/document connectors or fixtures; evidence links; approval gate.
- Risk/complexity: High; permissions and source attribution are central.
- Why this belongs in the programme: Tests organisational memory, source-of-truth discipline and approval-based publishing.

### 11. Tone-of-Voice Reviewer

- Title: Tone-of-Voice Reviewer
- Category: Content and communication workflows
- Problem: Brand and editorial voice checks are inconsistent and hard to scale.
- Hypothesis: A rubric-based agent can produce more actionable voice feedback than generic rewrite prompts.
- Likely user/workflow: Writer, marketer or studio team reviewing copy before publication.
- Baseline: Manual editorial review.
- Public demo or private case study: Public demo with synthetic copy and a compact style guide.
- Research question covered: RQ2, RQ3
- Likely stack additions: Voice rubric; before/after comparison; optional suggestion mode.
- Risk/complexity: Low to medium; taste remains subjective.
- Why this belongs in the programme: Tests rubric design, adoption and the value of suggest-only autonomy.

### 12. Sprint Planning Assistant

- Title: Sprint Planning Assistant
- Category: Planning and operations
- Problem: Sprint plans often understate dependencies, unknowns and hidden work.
- Hypothesis: An agent can review candidate work items and suggest a more realistic sprint plan with assumptions and trade-offs.
- Likely user/workflow: Product manager or delivery lead preparing sprint planning.
- Baseline: Manual planning from backlog items.
- Public demo or private case study: Public demo with synthetic backlog.
- Research question covered: RQ1, RQ2, RQ4, RQ6
- Likely stack additions: GitHub issue fixture; planning rubric; dependency extraction.
- Risk/complexity: Medium; context gaps can make suggestions shallow.
- Why this belongs in the programme: Tests planning support where adoption depends on legibility rather than automation.

### 13. Receipt Coding Assistant

- Title: Receipt Coding Assistant
- Category: Data extraction and structured outputs
- Problem: Small-business expense coding is repetitive but errors affect bookkeeping.
- Hypothesis: An agent can extract receipt data and recommend categories with confidence while routing ambiguous cases to a human.
- Likely user/workflow: Operations or finance admin processing receipts.
- Baseline: Manual entry into spreadsheet or bookkeeping software.
- Public demo or private case study: Public demo with synthetic receipts.
- Research question covered: RQ3, RQ4, RQ6
- Likely stack additions: OCR or document parsing; category schema; confidence threshold.
- Risk/complexity: Medium; financial correctness and edge cases matter.
- Why this belongs in the programme: Tests structured extraction, confidence and human approval around routine work.

### 14. Calendar Negotiation Agent

- Title: Calendar Negotiation Agent
- Category: Human approval and delegated action
- Problem: Scheduling multi-person meetings creates repeated low-value coordination work.
- Hypothesis: An agent can draft scheduling replies and propose options, but final send should remain human-approved.
- Likely user/workflow: Consultant or manager scheduling external meetings.
- Baseline: Manual email/calendar coordination.
- Public demo or private case study: Private case study or public demo with mock calendars.
- Research question covered: RQ2, RQ4, RQ5
- Likely stack additions: Calendar mock or integration; approval gate; email draft tool.
- Risk/complexity: High; real calendars and external messages require permissions and reversibility.
- Why this belongs in the programme: Tests delegated action, approval boundaries and user trust.

### 15. CSV Reconciliation Agent

- Title: CSV Reconciliation Agent
- Category: Data extraction and structured outputs
- Problem: Comparing exported data sets is tedious and error-prone.
- Hypothesis: An agent can explain mismatches and propose reconciliation actions faster than manual spreadsheet inspection.
- Likely user/workflow: Operations, finance or data admin comparing exports.
- Baseline: Manual spreadsheet formulas, filters and spot checks.
- Public demo or private case study: Public demo with synthetic CSVs.
- Research question covered: RQ1, RQ3, RQ6
- Likely stack additions: Deterministic CSV parser; diff engine; AI explanation layer.
- Risk/complexity: Medium; deterministic comparison should do most of the work.
- Why this belongs in the programme: Tests when AI should explain and guide rather than perform core computation.

### 16. GitHub Issue Groomer

- Title: GitHub Issue Groomer
- Category: Human approval and delegated action
- Problem: Backlogs degrade when issues lack scope, labels, acceptance criteria or owner context.
- Hypothesis: An agent can propose issue improvements and labels that reduce grooming time without editing issues automatically.
- Likely user/workflow: Engineering lead preparing work for review or assignment.
- Baseline: Manual issue review.
- Public demo or private case study: Public demo against a sample repo, or private case study with internal issues.
- Research question covered: RQ2, RQ3, RQ4
- Likely stack additions: GitHub API; label taxonomy; approval flow.
- Risk/complexity: Medium; repository conventions vary.
- Why this belongs in the programme: Tests low-risk developer workflow assistance and approval-based updates.

### 17. Social Evidence Extractor

- Title: Social Evidence Extractor
- Category: Content and communication workflows
- Problem: Social posts often drift away from the evidence in the underlying work.
- Hypothesis: An agent can draft concise social posts that cite the specific repository evidence behind each claim.
- Likely user/workflow: Studio team publishing daily experiment updates.
- Baseline: Manual post writing from memory and notes.
- Public demo or private case study: Public demo using programme artefacts.
- Research question covered: RQ2, RQ3, RQ6
- Likely stack additions: Markdown source reader; claim-to-evidence checker; voice rubric.
- Risk/complexity: Low to medium; risk is unsupported claims, not technical difficulty.
- Why this belongs in the programme: Helps the programme while testing evidence-grounded content generation.

### 18. Data Quality Sentinel

- Title: Data Quality Sentinel
- Category: Review, QA and risk assessment
- Problem: Small data quality issues in operational spreadsheets are found late or not at all.
- Hypothesis: An agent can identify likely data quality problems and explain why they matter to a non-technical owner.
- Likely user/workflow: Operations lead reviewing a spreadsheet export.
- Baseline: Manual inspection and spreadsheet formulas.
- Public demo or private case study: Public demo with synthetic spreadsheet.
- Research question covered: RQ1, RQ2, RQ3
- Likely stack additions: Spreadsheet parsing; deterministic validation rules; explanation layer.
- Risk/complexity: Medium; must avoid replacing deterministic validation with guesswork.
- Why this belongs in the programme: Tests hybrid deterministic/AI design for practical internal tooling.

### 19. Project Memory Agent

- Title: Project Memory Agent
- Category: Knowledge retrieval and synthesis
- Problem: Teams waste time re-finding project context across docs, issues and messages.
- Hypothesis: A constrained project-memory agent can answer project questions with citations and uncertainty better than manual search.
- Likely user/workflow: Project team member onboarding to or returning to a project.
- Baseline: Search across repository, docs and chat.
- Public demo or private case study: Private case study with redacted internal project materials, or public demo with synthetic artefacts.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Retrieval index; citation policy; permission-aware fixtures.
- Risk/complexity: High; source boundaries and stale information are hard.
- Why this belongs in the programme: Tests a core promise of organisational AI systems under realistic constraints.

### 20. Bid Response Assembler

- Title: Bid Response Assembler
- Category: Content and communication workflows
- Problem: Responding to RFP questions requires reusing approved material without losing specificity.
- Hypothesis: An agent can assemble draft responses from approved source material and flag gaps for human input.
- Likely user/workflow: Sales or leadership team preparing a bid.
- Baseline: Manual copy/paste from previous proposals and memory.
- Public demo or private case study: Private case study with redacted source material, or public demo with synthetic RFP.
- Research question covered: RQ2, RQ3, RQ5, RQ6
- Likely stack additions: Source library; retrieval; evidence and gap markers.
- Risk/complexity: High; confidentiality and stale claims matter.
- Why this belongs in the programme: Tests value, safety and reuse in a high-effort commercial workflow.

### 21. Resource Allocation Adviser

- Title: Resource Allocation Adviser
- Category: Planning and operations
- Problem: Capacity planning mixes availability, skills, deadlines and judgement in ways that are hard to explain.
- Hypothesis: An agent can propose allocation options and expose trade-offs without making staffing decisions.
- Likely user/workflow: Studio operations or delivery lead planning the next fortnight.
- Baseline: Manual spreadsheet or calendar review.
- Public demo or private case study: Private case study with redacted synthetic capacity data.
- Research question covered: RQ2, RQ4, RQ6
- Likely stack additions: Capacity fixture; constraints model; recommendation rubric.
- Risk/complexity: High; people-related decisions require careful framing.
- Why this belongs in the programme: Tests adoption and trust in sensitive operational recommendations.

### 22. Permission Boundary Tester

- Title: Permission Boundary Tester
- Category: Production constraints and safety
- Problem: It is hard to see whether an agent respects data and tool boundaries before deployment.
- Hypothesis: A test harness can reveal permission, refusal and escalation failures earlier than manual spot checks.
- Likely user/workflow: Engineer evaluating an agent before internal release.
- Baseline: Manual prompt tests and code review.
- Public demo or private case study: Public demo using a toy agent and synthetic tools.
- Research question covered: RQ3, RQ5
- Likely stack additions: Eve evals; mock tools; adversarial scenario set.
- Risk/complexity: Medium; useful only if scenarios are realistic.
- Why this belongs in the programme: Directly improves the Agent Kit's safety evaluation practice.

### 23. Customer Update Drafter

- Title: Customer Update Drafter
- Category: Content and communication workflows
- Problem: Project updates take time and often omit risks, decisions or next steps.
- Hypothesis: An agent can draft a concise customer update from project evidence while marking uncertainties and required approvals.
- Likely user/workflow: Delivery lead sending weekly customer updates.
- Baseline: Manual email or project update writing.
- Public demo or private case study: Public demo with synthetic project record, or private case study with redacted updates.
- Research question covered: RQ2, RQ3, RQ4
- Likely stack additions: Project status fixtures; evidence links; approval step.
- Risk/complexity: Medium; tone and accuracy are important.
- Why this belongs in the programme: Tests a repeated workflow where adoption depends on time saved and editability.

### 24. Maintenance Triage Agent

- Title: Maintenance Triage Agent
- Category: Planning and operations
- Problem: Maintenance requests arrive with unclear impact, reproduction detail and urgency.
- Hypothesis: An agent can produce a first-pass maintenance triage note that improves prioritisation and follow-up questions.
- Likely user/workflow: Support engineer or account lead handling maintenance work.
- Baseline: Manual reading and follow-up.
- Public demo or private case study: Public demo with synthetic maintenance tickets.
- Research question covered: RQ1, RQ2, RQ4
- Likely stack additions: Ticket fixtures; severity rubric; clarification evaluator.
- Risk/complexity: Medium; wrong urgency can distort priorities.
- Why this belongs in the programme: Tests practical triage with clear baseline and evaluable scenarios.

### 25. Sensitive Data Redactor

- Title: Sensitive Data Redactor
- Category: Production constraints and safety
- Problem: Teams need to share examples publicly or internally without leaking sensitive details.
- Hypothesis: An agent plus deterministic checks can redact sensitive data more usefully than manual review alone.
- Likely user/workflow: Team preparing evidence packs, case studies or support examples.
- Baseline: Manual redaction and cautious omission.
- Public demo or private case study: Public demo with synthetic sensitive examples.
- Research question covered: RQ3, RQ5
- Likely stack additions: PII detection; redaction policy; verification checks.
- Risk/complexity: High; false negatives are serious.
- Why this belongs in the programme: Supports safe publication and tests a core production-readiness concern.

### 26. Invoice Exception Reviewer

- Title: Invoice Exception Reviewer
- Category: Data extraction and structured outputs
- Problem: Invoice exceptions require checking amounts, dates, supplier terms and missing information.
- Hypothesis: An agent can explain invoice exceptions and propose next actions while leaving approval to a human.
- Likely user/workflow: Finance or operations admin reviewing invoices.
- Baseline: Manual invoice review against purchase records.
- Public demo or private case study: Public demo with synthetic invoices and purchase orders.
- Research question covered: RQ3, RQ4, RQ6
- Likely stack additions: Document parsing; purchase-order fixture; exception schema.
- Risk/complexity: Medium to high; financial impact requires approval gates.
- Why this belongs in the programme: Tests financial workflow assistance with structured outputs and clear human control.

### 27. Grant Eligibility Screener

- Title: Grant Eligibility Screener
- Category: Intake, triage and routing
- Problem: Organisations waste time reading grant criteria before knowing whether an opportunity is plausible.
- Hypothesis: An agent can screen eligibility, identify uncertain criteria and recommend whether to investigate further.
- Likely user/workflow: Founder, nonprofit lead or funding researcher reviewing grant opportunities.
- Baseline: Manual reading of criteria and guidance.
- Public demo or private case study: Public demo using public grant criteria and synthetic organisation profiles.
- Research question covered: RQ1, RQ2, RQ3
- Likely stack additions: Web/document retrieval; eligibility schema; uncertainty handling.
- Risk/complexity: Medium; criteria interpretation can be nuanced.
- Why this belongs in the programme: Tests decision support where uncertainty and caveats are more valuable than confident answers.

### 28. CRM Follow-up Agent

- Title: CRM Follow-up Agent
- Category: Human approval and delegated action
- Problem: Follow-ups after calls or sales conversations are often late, generic or forgotten.
- Hypothesis: An agent can draft CRM notes and follow-up messages from call evidence, with human approval before updates or sending.
- Likely user/workflow: Sales or account lead after a discovery call.
- Baseline: Manual CRM update and email drafting.
- Public demo or private case study: Private case study or public demo with mock CRM and synthetic transcript.
- Research question covered: RQ2, RQ4, RQ5
- Likely stack additions: CRM mock/integration; transcript parser; approval gate.
- Risk/complexity: High; external communication and customer data require safeguards.
- Why this belongs in the programme: Tests delegated action in a commercially important workflow.

### 29. Release Notes QA Agent

- Title: Release Notes QA Agent
- Category: Review, QA and risk assessment
- Problem: Release notes can omit user-visible changes, overstate features or miss known limitations.
- Hypothesis: An agent can compare merged work with draft release notes and flag unsupported or missing claims.
- Likely user/workflow: Product or engineering lead preparing release communication.
- Baseline: Manual review of PRs, tickets and notes.
- Public demo or private case study: Public demo against sample PRs and release notes.
- Research question covered: RQ2, RQ3
- Likely stack additions: GitHub API or fixtures; claim checker; changelog parser.
- Risk/complexity: Medium; repository context quality matters.
- Why this belongs in the programme: Tests evidence-grounded communication in a developer-adjacent workflow.

### 30. Audit Trail Explainer

- Title: Audit Trail Explainer
- Category: Production constraints and safety
- Problem: Agent actions and tool calls are hard for non-engineers to inspect and trust.
- Hypothesis: An agent can turn execution logs into an understandable audit summary that supports review and accountability.
- Likely user/workflow: Operations lead, compliance reviewer or engineer reviewing an agent run.
- Baseline: Raw logs and engineer explanation.
- Public demo or private case study: Public demo with synthetic agent logs.
- Research question covered: RQ2, RQ5
- Likely stack additions: Log parser; event schema; summary rubric.
- Risk/complexity: Medium; summaries must not hide important details.
- Why this belongs in the programme: Tests transparency and observability, which are essential for organisational trust.

### 31. Procurement Comparison Agent

- Title: Procurement Comparison Agent
- Category: Planning and operations
- Problem: Comparing supplier options involves pricing, constraints, terms and qualitative trade-offs.
- Hypothesis: An agent can produce a structured comparison and identify missing decision evidence better than a spreadsheet alone.
- Likely user/workflow: Operations or leadership team comparing tools or vendors.
- Baseline: Manual spreadsheet comparison and discussion.
- Public demo or private case study: Public demo with synthetic supplier proposals.
- Research question covered: RQ1, RQ2, RQ6
- Likely stack additions: Comparison schema; source document parser; scoring rubric.
- Risk/complexity: Medium; scoring can smuggle in hidden assumptions.
- Why this belongs in the programme: Tests whether AI improves complex comparison or just decorates a table.

### 32. Policy Drift Checker

- Title: Policy Drift Checker
- Category: Review, QA and risk assessment
- Problem: Internal documents drift away from approved policy or current practice.
- Hypothesis: An agent can identify likely inconsistencies between an approved policy and downstream documents.
- Likely user/workflow: Operations, compliance or people team reviewing docs.
- Baseline: Manual document review.
- Public demo or private case study: Public demo with synthetic policy and derived documents.
- Research question covered: RQ3, RQ5
- Likely stack additions: Document diffing; policy-rule extraction; evidence-linked findings.
- Risk/complexity: Medium; must distinguish contradiction from allowed variation.
- Why this belongs in the programme: Tests reliable review against source-of-truth documents.

### 33. Internal Comms Summariser

- Title: Internal Comms Summariser
- Category: Content and communication workflows
- Problem: People returning from time away need useful summaries without reading every message.
- Hypothesis: An agent can summarise internal updates by decisions, blockers and required attention better than chronological catch-up.
- Likely user/workflow: Team member returning after absence.
- Baseline: Manual Slack/email catch-up.
- Public demo or private case study: Private case study with redacted internal messages, or public synthetic channel.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Message fixtures; summarisation rubric; privacy boundaries.
- Risk/complexity: High; internal message privacy and context loss matter.
- Why this belongs in the programme: Tests adoption, trust and safe summarisation in a frequent knowledge-work scenario.

### 34. Form-to-CRM Agent

- Title: Form-to-CRM Agent
- Category: Data extraction and structured outputs
- Problem: Form submissions require cleanup before they become useful CRM records.
- Hypothesis: An agent can normalise form input, flag missing fields and draft a CRM update for approval.
- Likely user/workflow: Sales or operations admin processing inbound forms.
- Baseline: Manual copy, cleanup and CRM entry.
- Public demo or private case study: Public demo with mock CRM and synthetic submissions.
- Research question covered: RQ3, RQ4, RQ6
- Likely stack additions: CRM mock; validation schema; approval gate.
- Risk/complexity: Medium; automated updates should wait until trust is proven.
- Why this belongs in the programme: Tests structured transformation and approval in a repeatable workflow.

### 35. Compliance Evidence Extractor

- Title: Compliance Evidence Extractor
- Category: Data extraction and structured outputs
- Problem: Preparing compliance evidence requires finding, labelling and explaining relevant artefacts.
- Hypothesis: An agent can map documents to evidence requirements and flag gaps faster than manual collection.
- Likely user/workflow: Operations or security lead preparing an audit pack.
- Baseline: Manual document search and checklist completion.
- Public demo or private case study: Private case study or public demo with synthetic control checklist.
- Research question covered: RQ3, RQ5, RQ6
- Likely stack additions: Checklist schema; retrieval; evidence citation.
- Risk/complexity: High; evidence quality and permissions are critical.
- Why this belongs in the programme: Tests high-value organisational workflows with strong safety and audit requirements.

### 36. Runbook Rehearsal Agent

- Title: Runbook Rehearsal Agent
- Category: Planning and operations
- Problem: Operational runbooks look complete until an incident exposes missing steps or ownership.
- Hypothesis: An agent can rehearse a runbook against incident scenarios and identify gaps before production use.
- Likely user/workflow: Engineer or operations lead reviewing incident procedures.
- Baseline: Manual tabletop exercise or no rehearsal.
- Public demo or private case study: Public demo with synthetic runbook and incident.
- Research question covered: RQ1, RQ3, RQ5
- Likely stack additions: Scenario generator; runbook parser; gap rubric.
- Risk/complexity: Medium; simulations can be superficial.
- Why this belongs in the programme: Tests whether AI can improve readiness without touching production systems.

### 37. Vendor Renewal Assistant

- Title: Vendor Renewal Assistant
- Category: Human approval and delegated action
- Problem: Renewals are missed or accepted without checking usage, price change and alternatives.
- Hypothesis: An agent can prepare renewal decisions with usage evidence, cost changes and recommended next action for human approval.
- Likely user/workflow: Operations or finance lead reviewing subscriptions.
- Baseline: Calendar reminders, invoices and manual checking.
- Public demo or private case study: Private case study with redacted subscription data, or public synthetic data.
- Research question covered: RQ2, RQ4, RQ6
- Likely stack additions: Invoice/subscription fixtures; comparison rubric; approval workflow.
- Risk/complexity: Medium; data access and authority boundaries matter.
- Why this belongs in the programme: Tests cost/value reasoning and approval around operational spend.

### 38. Incident Postmortem Assistant

- Title: Incident Postmortem Assistant
- Category: Production constraints and safety
- Problem: Postmortems can become narrative-heavy and action-light.
- Hypothesis: An agent can draft a postmortem from timeline evidence that separates facts, contributing factors and follow-up actions.
- Likely user/workflow: Engineering or operations lead after an incident.
- Baseline: Manual postmortem writing from logs and notes.
- Public demo or private case study: Public demo with synthetic incident timeline.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Timeline parser; evidence citation; action extraction.
- Risk/complexity: Medium; blame and certainty must be handled carefully.
- Why this belongs in the programme: Tests evidence-grounded synthesis in a sensitive organisational workflow.

### 39. Competitor Change Monitor

- Title: Competitor Change Monitor
- Category: Knowledge retrieval and synthesis
- Problem: Teams miss meaningful changes in competitor messaging, pricing or product positioning.
- Hypothesis: An agent can monitor selected public pages and produce a concise change report with source links and uncertainty.
- Likely user/workflow: Product, marketing or strategy lead doing periodic market review.
- Baseline: Manual website checks and notes.
- Public demo or private case study: Public demo using public websites.
- Research question covered: RQ1, RQ3, RQ6
- Likely stack additions: Web fetch/snapshot comparison; summarisation; source links.
- Risk/complexity: Medium; scraping reliability and change significance matter.
- Why this belongs in the programme: Tests monitoring, change detection and the cost of keeping agents running.

### 40. Spreadsheet Formula Auditor

- Title: Spreadsheet Formula Auditor
- Category: Data extraction and structured outputs
- Problem: Business-critical spreadsheets often contain fragile formulas and unexplained exceptions.
- Hypothesis: An agent can inspect formulas, identify suspicious patterns and explain review priorities more accessibly than manual inspection.
- Likely user/workflow: Finance, operations or data owner reviewing a spreadsheet.
- Baseline: Manual spreadsheet audit.
- Public demo or private case study: Public demo with synthetic workbook.
- Research question covered: RQ1, RQ2, RQ3
- Likely stack additions: Spreadsheet parser; formula graph extraction; explanation rubric.
- Risk/complexity: Medium; deterministic parsing is essential.
- Why this belongs in the programme: Tests AI as an explanatory layer over structured analysis.

### 41. Research Request Router

- Title: Research Request Router
- Category: Intake, triage and routing
- Problem: Open-ended research requests often lack enough detail to route or estimate.
- Hypothesis: An agent can classify a research request, ask clarifying questions and recommend a lightweight research plan.
- Likely user/workflow: Strategy, design or product team receiving research asks.
- Baseline: Manual clarification and planning.
- Public demo or private case study: Public demo with synthetic requests.
- Research question covered: RQ1, RQ2, RQ4
- Likely stack additions: Request taxonomy; clarification behaviour evals; plan schema.
- Risk/complexity: Low to medium; scope creep is the main risk.
- Why this belongs in the programme: Tests clarification-first agent behaviour instead of premature answer generation.

### 42. Delivery Risk Radar

- Title: Delivery Risk Radar
- Category: Planning and operations
- Problem: Delivery risk signals are scattered across status notes, issues, decisions and blockers.
- Hypothesis: An agent can identify likely delivery risks and explain evidence without replacing project leadership judgement.
- Likely user/workflow: Delivery lead reviewing weekly project health.
- Baseline: Manual project review and intuition.
- Public demo or private case study: Private case study or synthetic project pack.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Project artefact fixtures; risk taxonomy; evidence links.
- Risk/complexity: High; risk scoring can become misleading if context is thin.
- Why this belongs in the programme: Tests high-value decision support and whether legible evidence improves trust.

### 43. Source Citation Checker

- Title: Source Citation Checker
- Category: Knowledge retrieval and synthesis
- Problem: Drafts can cite sources that do not support the specific claim being made.
- Hypothesis: An agent can compare claims with cited sources and flag unsupported, weak or missing citations.
- Likely user/workflow: Writer, researcher or strategist reviewing a draft.
- Baseline: Manual source checking.
- Public demo or private case study: Public demo with synthetic draft and public sources.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Claim extraction; source retrieval; support rubric.
- Risk/complexity: Medium to high; semantic support is hard to evaluate.
- Why this belongs in the programme: Tests evidence discipline and reliability in publication workflows.

### 44. Slack Decision Capture Agent

- Title: Slack Decision Capture Agent
- Category: Human approval and delegated action
- Problem: Decisions made in chat rarely reach the durable project record.
- Hypothesis: An agent can propose decision records from chat threads with source links and human approval.
- Likely user/workflow: Project lead or team member maintaining project documentation.
- Baseline: Manual copy from Slack into docs or no capture.
- Public demo or private case study: Private case study with redacted threads, or public demo with synthetic Slack export.
- Research question covered: RQ2, RQ4, RQ5
- Likely stack additions: Slack export/parser; decision schema; approval flow.
- Risk/complexity: High; privacy, consent and source attribution matter.
- Why this belongs in the programme: Tests organisational memory with strong safety and permission constraints.

### 45. Inbox Prioritiser

- Title: Inbox Prioritiser
- Category: Intake, triage and routing
- Problem: Important emails compete with noise, and priority is often inferred from incomplete signals.
- Hypothesis: An agent can group and prioritise messages with explanations and suggested next actions without sending replies.
- Likely user/workflow: Founder, consultant or operations lead processing daily email.
- Baseline: Manual inbox scanning and filtering rules.
- Public demo or private case study: Private case study or public demo with synthetic inbox.
- Research question covered: RQ1, RQ2, RQ4, RQ5
- Likely stack additions: Email fixture/integration; priority rubric; privacy boundary.
- Risk/complexity: Medium to high; sensitive data and user-specific priorities matter.
- Why this belongs in the programme: Tests adoption in a familiar workflow where personal trust thresholds are high.

### 46. Friction Cartographer

- Title: Friction Cartographer
- Category: Design discovery, trust and meta-research
- Problem: Teams often start AI conversations from possible automation rather than observed workflow pain.
- Hypothesis: An agent can turn a recorded workflow walkthrough into a useful friction map that reveals hesitation, waiting, context switching, duplication and uncertainty before proposing any solution.
- Likely user/workflow: Designer, strategist or delivery lead observing someone perform a real operational task.
- Baseline: Manual workflow observation, interview notes and service blueprinting.
- Public demo or private case study: Public demo with synthetic screen recording, or private case study with redacted workflow evidence.
- Research question covered: RQ1, RQ2
- Likely stack additions: Screen recording or transcript fixture; timeline annotation; friction taxonomy; optional visual map.
- Risk/complexity: Medium to high; capture quality and privacy constraints matter.
- Why this belongs in the programme: It makes the programme more Fieldwork-specific by testing whether agents can help find better AI opportunities, not just implement them.

### 47. Anti-Agent

- Title: Anti-Agent
- Category: Design discovery, trust and meta-research
- Problem: Teams can reach for AI before testing whether the problem needs an agent at all.
- Hypothesis: An agent designed to argue against agentic automation can improve brief quality by identifying simpler baselines, non-AI options and adoption risks before coding starts.
- Likely user/workflow: Project sponsor or builder preparing an experiment brief.
- Baseline: Informal critique by a senior product, design or engineering reviewer.
- Public demo or private case study: Public demo using synthetic automation proposals.
- Research question covered: RQ1, RQ6
- Likely stack additions: Brief parser; alternative-solution rubric; falsifiability checklist.
- Risk/complexity: Low to medium; the challenge is making critique specific rather than performatively negative.
- Why this belongs in the programme: It directly tests the charter's claim that the goal is not to maximise AI use.

### 48. Decision Archaeologist

- Title: Decision Archaeologist
- Category: Design discovery, trust and meta-research
- Problem: Organisations remember what was decided more easily than why it was decided.
- Hypothesis: An agent can reconstruct a decision timeline, alternatives considered, evidence used and missing information from scattered project artefacts.
- Likely user/workflow: Project lead, strategist or researcher revisiting a past decision.
- Baseline: Manual reconstruction from emails, docs, meeting notes and memory.
- Public demo or private case study: Private case study with redacted project artefacts, or public demo with synthetic project history.
- Research question covered: RQ2, RQ3, RQ5
- Likely stack additions: Multi-source artefact fixtures; timeline builder; citation and uncertainty markers.
- Risk/complexity: High; the agent must avoid inventing intent or overstating evidence.
- Why this belongs in the programme: It tests organisational memory at a deeper level than summary or decision capture.

### 49. Trust Designer

- Title: Trust Designer
- Category: Design discovery, trust and meta-research
- Problem: It is unclear how much explanation users need before they trust an agent recommendation, and when explanation becomes clutter.
- Hypothesis: A controlled interface that progressively hides rationale, evidence and uncertainty can reveal where trust collapses for a specific workflow.
- Likely user/workflow: Designer or product lead testing an AI recommendation pattern with internal reviewers.
- Baseline: Unstructured feedback on agent output or single fixed explanation design.
- Public demo or private case study: Public demo with synthetic recommendations and reviewer notes.
- Research question covered: RQ2, RQ4
- Likely stack additions: Lightweight UI; explanation toggles; trust rating capture; scenario fixtures.
- Risk/complexity: Medium; findings may be qualitative and low-confidence without enough reviewers.
- Why this belongs in the programme: Trust and adoption are central research questions, and this turns them into an explicit experiment rather than a retrospective note.

### 50. Recommendation Diff

- Title: Recommendation Diff
- Category: Design discovery, trust and meta-research
- Problem: Programme recommendations will change, but those changes can become invisible unless explicitly linked to evidence.
- Hypothesis: An agent can compare earlier and current recommendations, identify what changed and cite the experiments that caused the change.
- Likely user/workflow: Programme lead preparing weekly synthesis or final Fieldwork Method updates.
- Baseline: Manual review of Field Notes, Promotion Reviews, weekly summaries and recommendations.
- Public demo or private case study: Public demo using programme artefacts.
- Research question covered: RQ2, RQ3, RQ6
- Likely stack additions: Markdown diffing; Research Register reader; citation/evidence mapper.
- Risk/complexity: Medium; it depends on consistent programme records and careful source-of-truth handling.
- Why this belongs in the programme: It makes the evolution of Fieldwork's judgement visible while preserving published experiments as immutable snapshots.

## Recommended First 10 Agents

The first ten should create useful programme evidence quickly, exercise different research questions and avoid beginning with the highest-risk integrations.

| Order | Agent | Reason |
| ---: | --- | --- |
| 1 | Friction Cartographer | Starts from observed workflow pain, not automation, and anchors the programme in design-led discovery. |
| 2 | Meeting Evidence Extractor | Strong first implementation build: synthetic data, structured outputs, clear baseline, useful eval scenarios. |
| 3 | Anti-Agent | Tests whether the brief should exist before the programme gets too committed to building agents by default. |
| 4 | Proposal Risk Reviewer | Tests judgement support and evidence-grounded review in a high-value workflow. |
| 5 | Support Intake Classifier | Adds clarification and routing without real external actions. |
| 6 | Case Study Drafting Assistant | Supports programme content while testing evidence boundaries and voice. |
| 7 | Trust Designer | Makes trust and adoption an explicit experiment rather than a retrospective evaluation note. |
| 8 | Scope Change Assessor | Tests decision preparation, autonomy limits and cost/value reasoning. |
| 9 | Accessibility QA Agent | Tests hybrid deterministic tooling plus AI interpretation. |
| 10 | Sensitive Data Redactor | Brings safety and publication constraints into the first third of the programme. |

## 20 Provisional Agents

These are strong candidates for the remaining planned slots, subject to evidence from the first ten.

| Provisional order | Agent | Main reason to keep |
| ---: | --- | --- |
| 11 | Decision Log Curator | Tests organisational memory once the programme has early artefacts to draw on. |
| 12 | GitHub Issue Groomer | Introduces a real developer workflow and approval-based tool use. |
| 13 | CSV Reconciliation Agent | Tests whether AI should explain deterministic analysis rather than perform it. |
| 14 | Research Pack Builder | Tests public-source research, citation and preparation workflows. |
| 15 | Tone-of-Voice Reviewer | Focused rubric and adoption experiment. |
| 16 | Sprint Planning Assistant | Practical planning support with visible trade-offs. |
| 17 | Receipt Coding Assistant | Structured extraction with confidence and finance constraints. |
| 18 | Calendar Negotiation Agent | Tests human-approved delegated action. |
| 19 | Data Quality Sentinel | Useful hybrid deterministic/AI operational pattern. |
| 20 | Project Memory Agent | High-value organisational memory experiment. |
| 21 | Permission Boundary Tester | Strengthens Agent Kit safety evaluation. |
| 22 | Customer Update Drafter | Repeated workflow with clear adoption signal. |
| 23 | Maintenance Triage Agent | Practical service workflow and easy baseline comparison. |
| 24 | Invoice Exception Reviewer | Financial workflow with approval gates. |
| 25 | Grant Eligibility Screener | Public demo with uncertainty handling. |
| 26 | Audit Trail Explainer | Trust, observability and non-engineer legibility. |
| 27 | Decision Archaeologist | Deeper organisational-memory experiment than summary or capture. |
| 28 | Recommendation Diff | Makes changed recommendations visible and evidence-backed. |
| 29 | Runbook Rehearsal Agent | Safety/readiness without production access. |
| 30 | Source Citation Checker | Direct test of evidence discipline. |

## Reserve Pool

These are useful if a planned agent becomes too similar to earlier evidence, too risky for the available day, or less valuable after calibration.

| Agent | Reserve reason |
| --- | --- |
| Lead Triage Agent | Strong concept, but overlaps with intake/routing agents already in the first set. |
| Social Evidence Extractor | Useful programme helper, but may be redundant after Case Study Drafting Assistant. |
| Resource Allocation Adviser | Valuable but sensitive; better after trust and recommendation patterns mature. |
| Compliance Evidence Extractor | High value but likely heavy for a daily experiment. |
| Internal Comms Summariser | Useful but privacy-heavy and similar to knowledge synthesis concepts. |
| Form-to-CRM Agent | Good structured workflow but overlaps with CRM Follow-up Agent. |
| Vendor Renewal Assistant | Useful cost experiment; can replace a planning/ops agent if needed. |
| Incident Postmortem Assistant | Strong safety workflow; keep if incident/runbook track needs more evidence. |
| Competitor Change Monitor | Good monitoring/cost experiment; may require ongoing infrastructure. |
| Spreadsheet Formula Auditor | Strong hybrid analysis concept; can replace Data Quality Sentinel or CSV Reconciliation Agent. |
| Research Request Router | Good clarification experiment; overlaps with Support Intake Classifier. |
| Delivery Risk Radar | High-value but broad; should wait until Proposal Risk Reviewer and Scope Change Assessor produce evidence. |
| Slack Decision Capture Agent | Strong but permission-heavy; may follow Decision Log Curator. |
| Inbox Prioritiser | Familiar workflow but privacy and personal-priority calibration may dominate the day. |
| Contract Red-Flag Assistant | Important safety test, but legal-adjacent framing makes it a better later or reserve experiment. |
| CRM Follow-up Agent | Strong delegated-action candidate, but customer data and external communication make it better after approval patterns mature. |
| Release Notes QA Agent | Useful developer workflow, but lower programme distinctiveness than Recommendation Diff or Source Citation Checker. |
| Procurement Comparison Agent | Useful comparison workflow, but can wait if cost/value evidence is covered elsewhere. |
| Policy Drift Checker | Strong source-of-truth experiment, but overlaps with Source Citation Checker and Decision Archaeologist. |

## Sequencing Notes

- Keep the first week mostly synthetic and low-permission to stabilise brief, evaluation, evidence and publication operations.
- Include at least one design-discovery experiment in the first week so the programme starts from workflow observation, not document transformation.
- Introduce approval-based tool use before any experiment that could update, send or persist external changes.
- Use private case studies deliberately, not as a default. They should test a research question that public synthetic data cannot answer.
- Revisit the matrix after every five experiments. If one research question is overrepresented, swap from the reserve pool rather than forcing the original sequence.
- Do not promote stack additions from one experiment into the default stack without a Promotion Review.
