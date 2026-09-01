# WP1 — Presentation & README

## Goal

Make the repository immediately understandable **and worth exploring** to a reader with no project history.

A strong portfolio README should answer four questions quickly:

1. **What is this?**
2. **Why does it exist?**
3. **What can I see or do with it?**
4. **Why is this technically interesting enough to keep reading?**

WP1 is presentation/documentation work. It must not change application behavior merely to improve portfolio appearance.

## Entry criteria

- The project has a coherent purpose.
- There is enough implementation to state what it actually does.
- Existing technical documentation can be inspected and preserved.
- At least one useful visual, example, trace, output, or architecture view can be shown when the project benefits from it.

## Questions to answer first

1. What problem does the project solve?
2. Why is that problem non-trivial or interesting?
3. What is the one-sentence project definition?
4. What working end-to-end behavior exists today?
5. What can a visitor actually explore, run, inspect, or learn from this repository?
6. What did the author actually design and implement?
7. What role did AI-assisted coding play?
8. Which public claims can be verified from the repository?
9. What is explicitly outside scope?
10. What broader use, extension, or foundation does the current system naturally enable without pretending those future capabilities already exist?

## Reader journey

Design the README for progressive depth rather than one flat documentation dump.

### 0–10 seconds — category + promise

The visitor should understand the project category and central value proposition before scrolling deeply.

```text
Project name
↓
One strong sentence
↓
Visual proof / product view / result
```

Avoid opening with implementation vocabulary that only makes sense after the reader already understands the problem.

### 10–30 seconds — problem + concrete value

Explain:

- why the project exists;
- what pain, ambiguity, scale problem, or missing capability motivated it;
- what the system does differently or usefully;
- what the reader can explore in the repository.

### 30–60 seconds — make it tangible

Use concrete material such as:

- screenshots;
- short GIFs;
- before/after or input/output examples;
- short traces;
- one small architecture/data-flow diagram;
- realistic use cases;
- a compact feature/highlight list.

The visual should **explain something**, not merely decorate the page.

### 1–3 minutes — technical credibility

Then expose:

- system architecture;
- important design decisions;
- data/model boundaries;
- author contribution;
- AI-assisted development;
- tests/CI;
- installation and runtime;
- detailed documentation.

## Recommended README structure

The exact headings may vary, but the narrative should normally resemble:

```text
Project name
↓
One-sentence promise
↓
Hero visual / concrete evidence
↓
Why this exists
↓
What you can do / explore
↓
How the system works at a glance
↓
Interesting design choices / highlights
↓
What I built
↓
Architecture + technical depth
↓
Quick start / runtime
↓
Quality / evidence
↓
AI-assisted development
↓
Current scope, limitations, and possible extensions
↓
Detailed docs
```

Do not follow this mechanically when another ordering creates a clearer reader journey.

## Make the repository enjoyable to read

"Enjoyable" does not mean exaggerated marketing. It means reducing cognitive friction and rewarding curiosity.

Use:

- short sections with clear questions or outcomes;
- concrete examples before dense abstractions;
- meaningful visuals at natural transition points;
- captions that explain what a screenshot proves;
- diagrams that answer one question at a time;
- progressive disclosure: simple explanation first, implementation detail later;
- links that let an interested reader intentionally go deeper.

Avoid long uninterrupted walls of text, duplicated documentation, badge walls, and unexplained internal terminology.

## Vision and extension potential

A portfolio project can explain what it is a **foundation for**, provided current capability and future potential are separated explicitly.

Good framing:

```text
Current system
→ proven capability
→ natural extension / broader application
```

Examples:

- a monitoring system can be a foundation for alerting, comparative research, or additional evidence sources;
- a provider abstraction can support additional adapters or capability probes;
- an execution runtime can support more provider surfaces without changing the core contract.

Do not present planned or hypothetical extensions as implemented functionality.

## Actions

- Write a one-sentence definition that assumes no internal project knowledge.
- Explain the motivating problem before architecture details.
- Identify one strong visual or concrete example that proves the project is real.
- Add a concise `What you can do` / `What it does` / `Highlights` section appropriate to the project.
- Show at least one end-to-end flow in plain language before deep architecture when useful.
- Add `What I built` to make project-level contribution explicit.
- Explain AI-assisted development accurately when relevant, including responsibility for requirements, architecture, decomposition, review, acceptance criteria, testing, and rejecting unsuitable generated implementations.
- Add factual project status.
- Preserve deep technical material below the reader layer or move it into `docs/` when appropriate.
- Make limitations and non-goals explicit when they prevent misunderstanding.
- Add a restrained `What this can enable`, `Possible extensions`, or `Why this matters` section only when the repository genuinely supports that abstraction.

## Do not

- invent features;
- claim production readiness without evidence;
- replace technical docs with recruiter-only prose;
- use unverifiable marketing numbers;
- put architecture detail before the reader knows what the product does;
- hide material AI-assisted development;
- use badges/icons as a substitute for explanation;
- add decorative visuals that do not help comprehension;
- turn speculative roadmap ideas into current-product claims.

## Acceptance criteria

- [ ] A new reader can explain the project after the first screen or two.
- [ ] The opening gives a reason to keep reading, not merely a technical definition.
- [ ] Problem, solution, and current capability are clearly separated.
- [ ] At least one visual/example makes the system tangible when appropriate.
- [ ] A reader can identify what they could explore, run, inspect, or reuse.
- [ ] The narrative moves from simple explanation to technical depth.
- [ ] `What I built` reflects actual contribution.
- [ ] AI-assisted work is described accurately where relevant.
- [ ] Existing technical depth is preserved.
- [ ] Prominent claims map to evidence.
- [ ] Screenshots/examples reflect the current implementation.
- [ ] Future potential is clearly separated from current functionality.
- [ ] Known limitations are not hidden.

## PR scope

Expected scope: README and presentation assets only unless a broken documentation path requires a minimal fix.

Review focus:

1. Can an uninvolved reader understand the project without prior context?
2. Does the opening create justified curiosity?
3. Are visuals explanatory rather than decorative?
4. Are claims accurate and evidence-backed?
5. Is technical documentation preserved?
6. Did any product behavior change accidentally?
