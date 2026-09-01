# WP1 — Presentation & README

## Goal

Make the repository understandable to a new visitor in roughly 30–60 seconds while preserving enough technical depth for deeper inspection.

WP1 is presentation/documentation work. It must not change application behavior merely to improve portfolio appearance.

## Entry criteria

- The project has a coherent purpose.
- There is enough implementation to state what it actually does.
- Existing technical documentation can be inspected and preserved.

## Questions to answer first

1. What problem does the project solve?
2. What is the one-sentence project definition?
3. What working end-to-end behavior exists today?
4. What did the author actually design and implement?
5. What role did AI-assisted coding play?
6. Which public claims can be verified from the repository?
7. What is explicitly outside scope?

## Recommended README structure

### Reader layer

```text
Project name
↓
One-sentence definition
↓
Hero screenshot / demo / minimal diagram
↓
Why this project exists
↓
What it does
↓
What I built
↓
AI-assisted development
↓
Project status
```

### Technical layer

```text
Architecture
↓
Domain/data model
↓
Runtime
↓
Requirements
↓
Installation
↓
Quality / CI
↓
Detailed documentation
```

## Actions

- Write a one-sentence definition that assumes no internal project knowledge.
- Explain the problem before architecture details.
- Add a concise capability list.
- Add `What I built` to make project-level contribution explicit.
- Explain AI-assisted development accurately when relevant, including responsibility for requirements, architecture, decomposition, review, acceptance criteria, testing, and rejecting unsuitable generated implementations.
- Add factual project status.
- Use one strong screenshot/GIF/example near the top when useful.
- Preserve deep technical material below the reader layer or move it into `docs/` when appropriate.
- Make limitations and non-goals explicit when they prevent misunderstanding.

## Do not

- invent features;
- claim production readiness without evidence;
- replace technical docs with recruiter-only prose;
- use unverifiable marketing numbers;
- put architecture detail before the reader knows what the product does;
- hide material AI-assisted development;
- use badges/icons as a substitute for explanation.

## Acceptance criteria

- [ ] A new reader can explain the project after the first screen or two.
- [ ] Problem, solution, and current capability are clearly separated.
- [ ] `What I built` reflects actual contribution.
- [ ] AI-assisted work is described accurately where relevant.
- [ ] Existing technical depth is preserved.
- [ ] Prominent claims map to evidence.
- [ ] Screenshots/examples reflect the current implementation.
- [ ] Known limitations are not hidden.

## PR scope

Expected scope: README and presentation assets only unless a broken documentation path requires a minimal fix.

Review focus:

1. Is the project understandable without prior context?
2. Are claims accurate?
3. Is technical documentation preserved?
4. Did any product behavior change accidentally?
