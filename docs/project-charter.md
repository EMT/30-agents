# 30 Agents in 30 Days — Project Charter

**Version:** v0.6  
**Status:** Approved for planning  
**Owner:** Fieldwork  
**Primary repository:** `30-agents`

## 1. Purpose

Fieldwork will build thirty small, working AI agents in thirty days over six weeks.

The goal is not to produce thirty demos. The goal is to learn how practical AI systems should be identified, designed, engineered, evaluated and deployed safely inside real organisations.

The agents are experiments. The outputs are the Agent Kit, Field Notes, evaluation practice, reusable patterns, public evidence, and the Fieldwork Method for designing AI systems.

## 2. Fieldwork’s position

Fieldwork is a design and technology studio. AI expands our solution space; it does not replace our existing way of working.

We begin with people, workflows, systems, constraints and outcomes. We map operational workflows, customer journeys, pain points, decision points, drop-offs and time-consuming processes. Then we ask whether AI belongs in the solution.

**We are not interested in automating people away. We want to give good people superpowers.**

For this project, we define an AI system as:

> A product or workflow that combines language models, software, data and human judgement to achieve an organisational outcome.

An autonomous agent is one possible implementation. Human-in-the-loop workflows, deterministic software with AI-assisted decisions, and narrow internal tools are all valid.

## 3. Core thesis

Fieldwork is running and sharing this research project to discover what makes AI agents useful inside organisations.

Across thirty builds, we will test tools, patterns, workflows, autonomy levels, adoption factors, cost drivers, design decisions, security constraints and failure modes. We will publish what worked, what failed, and what changed our thinking.

The project begins with questions, not answers. Some hypotheses and assumptions will be wrong. When the evidence changes, our recommendations will change too.

## 4. What we intend to learn

Each experiment should contribute evidence towards one or more of these questions.

### 1. When should an organisation use an AI agent?

When does agentic behaviour create value, and when is traditional software, workflow design or deterministic automation better?

### 2. What makes people trust, adopt and keep using an AI system?

What makes an AI system legible, useful in day-to-day work, and worth returning to? What causes a technically working system to be ignored or abandoned?

### 3. What engineering patterns produce reliable AI systems?

Which patterns around tools, prompts, structured outputs, retrieval, evaluation, orchestration, memory and human approval consistently work?

### 4. How should autonomy be designed?

What level of autonomy is appropriate for a task: observe, suggest, recommend, approve, delegate or automate?

### 5. What does safe deployment require inside organisations?

How should AI systems handle permissions, sensitive data, audit trails, operational risk, delegated authority, agent identity and observability?

### 6. What do AI systems cost to build, run and maintain?

What engineering effort, runtime cost, maintenance burden and organisational change are required, and when is that cost justified?

## 5. What we will build

For thirty days over six weeks, we will build one narrow AI agent or agentic workflow.

Each experiment must include:

- one problem;
- one explicit hypothesis;
- three to five assumptions;
- a defined user or workflow;
- a baseline for how the problem is solved today;
- a working implementation;
- an evaluation;
- notes on adoption, cost and production constraints;
- a Field Notes record;
- a Promotion Review;
- a public article or case study.

Some agents will be public demos using synthetic, public or user-provided data. Others may use Fieldwork’s internal data and be shown through redacted case studies, screenshots, architecture notes or short videos.

Every experiment must be demonstrable. Not every experiment needs to be publicly usable.

## 6. What counts as finished

An agent is finished when it is ready to evaluate and share.

It should:

- solve one narrowly defined problem well enough to evaluate;
- be understandable to another person;
- be tested against representative examples;
- document limitations and failure modes;
- identify what production deployment would require;
- record build effort and runtime cost, or mark them not measured;
- leave behind evidence that supports the conclusions;
- have code we would show another engineer.

It does not need to be production-ready.

The standard is not “best possible agent”. The standard is the best experiment we can run within realistic constraints.

## 7. Operating principles

### Optimise for learning, not features

The project runs alongside client work. Scope must stay small, and the process must remain sustainable.

### Every day should make Fieldwork more capable

Each experiment should improve at least one of: the Agent Kit, templates, evaluation practice, tooling, Field Notes, public evidence, or engineering judgement.

### Start with people and workflows

AI does not change how we identify opportunities. It expands the solution space once the problem is understood.

### Design for adoption

A system that works can still fail if people do not trust it, understand it, or keep using it. Each experiment should consider the person expected to use it and the workflow it must fit into.

### Solve one problem per agent

Each agent should have a narrow scope. If the brief contains too many “and” clauses, the scope is too large.

### Standardise the platform; experiment intentionally

Use a standard stack and reusable Agent Kit. Vary technology only when the experiment is deliberately testing that variation.

### Value must justify effort

Working is not enough. Each experiment should ask what the system costs to build, run and maintain, and whether the value would justify that cost.

### Evidence beats opinion

An unevaluated agent is a demo. Evaluation turns each build into research.

### Publish failures

Confirmed, refined and rejected hypotheses all produce evidence.

### Design for organisational constraints

Every experiment should consider security, permissions, auditability, data handling, reliability, human approval and operational risk.

### Humans decide what gets delegated

AI may prepare, suggest, draft, evaluate and recommend. Humans decide what gets built, what gets published, what gets promoted, and which decisions are delegated.

### Experiments are immutable; the system evolves

Published agents are snapshots of what we built and believed on that day. The Agent Kit, templates, backlog, recommendations and the Fieldwork Method evolve.

### Reusable ideas must be promoted deliberately

Code, modules, patterns, process changes and recommendations enter the methodology only through Promotion Review.

### The backlog is a hypothesis

The agent list may change when evidence, research gaps or new insight suggests a better experiment. It should not change because of hype or novelty.

## 8. What this project is not

This is not:

- a stunt to prove AI is impressive;
- a marketing campaign disguised as engineering;
- an attempt to build thirty production-ready products;
- an attempt to maximise the use of AI;
- an argument for maximum autonomy;
- a framework-hopping exercise;
- a search for the flashiest demo.

The purpose of AI engineering is not to maximise AI. It is to improve organisational outcomes.

## 9. Deliverables

By the end of the project, we expect to produce:

- thirty AI agent experiments;
- one repository per experiment;
- a README, brief, evaluation, Field Notes record and Promotion Review for each experiment;
- a central `30-agents` repository;
- a public index of all experiments;
- a Field Notes index;
- a Research Register tracking hypotheses, status and verdicts;
- the Fieldwork Agent Kit;
- improved templates for briefs, evaluations, READMEs and Promotion Reviews;
- short write-ups or case studies for each experiment;
- short demo recordings when they take under 10 minutes or can be generated automatically;
- synthesis articles;
- the first version of the Fieldwork Method for designing AI systems.

## 10. Measures of success

The project succeeds if:

1. We complete thirty experiments.
2. Each experiment is evaluated, not just demonstrated.
3. We publish successes, failures and changed assumptions.
4. The Agent Kit improves between Day 1 and Day 30.
5. The templates and daily process improve through use.
6. Our judgement about AI systems improves.
7. We identify factors that affect adoption and disuse.
8. We understand more about build, run and maintenance trade-offs.
9. We can identify specific moments where evidence changed our approach.
10. Existing clients, partners and peers increasingly associate Fieldwork with practical AI system design and delivery.
11. We finish with a method we would confidently use on real organisational AI projects.

Ultimately, the question is: **How much more capable is Fieldwork on Day 30 than on Day 1?**

## 11. Public posture

This project is public because transparency improves the work.

Publishing the charter, experiments, evaluations and Field Notes makes the research accountable. It also shows how Fieldwork thinks: design-led, engineering-led, evidence-driven and willing to revise its recommendations.

The business aim is to shift how trusted clients, partners and peers describe Fieldwork: from a design and technology studio that builds digital products to one that can identify, design, build and deploy AI systems safely.

We are not optimising for reach. We are optimising for trust.

## 12. After thirty days

After Day 30, we will synthesise the evidence into outputs:

- the Fieldwork Method for designing AI systems;
- engineering recommendations supported by the experiments;
- patterns and anti-patterns;
- adoption, safety and production-readiness guidance;
- reflections on what we would and would not build for real organisations;
- future research tracks.

After the project is complete we can extract a more general research protocol from the process.

Right now, keep the focus simple:

**Build thirty focused agents. Evaluate them. Promote what earns its place. Use the evidence to become better at designing AI systems.**

---

## Version history

| Version | Notes                                            |
| ------- | ------------------------------------------------ |
| v0.1    | Initial draft based on planning discussions.     |
| v0.2    | Tightened for clarity and signal-to-noise ratio. |
| v0.3    | Applied wording refinements after review.        |
| v0.4    | Removed vague or superfluous wording.            |
| v0.5    | Added adoption and cost as top-level research questions; tightened reliability and deployment scope. |
| v0.6    | Cross-document pass: aligned evidence thresholds, Field Notes terminology, public posture and Fieldwork Method naming. |
