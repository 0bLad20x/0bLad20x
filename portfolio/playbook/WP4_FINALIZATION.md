# WP4 — Final Portfolio Review

## Goal

Review the repository as a completely uninvolved external visitor and decide whether the current state is genuinely ready to be used as public portfolio evidence.

WP4 has two equally important dimensions:

1. **technical credibility** — the repository is accurate, reproducible, safe, and evidence-backed;
2. **reader experience** — the repository is understandable, visually coherent, interesting to explore, and gives the reader a reason to continue.

WP4 should primarily discover inconsistencies and presentation gaps. It is not a reason to redesign a working system.

## Review mindset

Assume the reviewer:

- has never seen the project before;
- does not know its internal terminology;
- may spend only 10–30 seconds initially;
- may not know why the technical problem matters;
- will continue only if the repository earns their attention;
- may be a recruiter, engineering manager, developer, or technically curious user.

Do not mentally fill in missing explanations from project history.

## Reader-experience audit

### First 10 seconds — orientation

Without scrolling deeply, can the visitor answer:

- [ ] What kind of project is this?
- [ ] What central problem does it address?
- [ ] What is the useful/interesting result?
- [ ] Is there a visual or concrete signal that the project actually exists and works?

The first screen should create orientation before introducing dense implementation details.

### First 30–60 seconds — curiosity

Can the visitor answer:

- [ ] Why was this worth building?
- [ ] What can I do, inspect, explore, or learn with it?
- [ ] What makes the problem non-trivial?
- [ ] What is distinctive about the solution?
- [ ] Where should I click/read next if I want more depth?

A technically correct README can still fail WP4 if it is dry, abstract, or requires too much context before becoming interesting.

### Progressive depth

Check that the narrative roughly moves through:

```text
what is it?
↓
why does it matter?
↓
what can it do?
↓
show me something real
↓
how does it work?
↓
what is technically interesting?
↓
how can I run / inspect it?
↓
what is proven, limited, or extensible?
```

The exact headings are flexible. The reader journey is not.

## Visual review

Every major visual should have a job.

Check:

- [ ] hero screenshot/demo loads and is legible;
- [ ] screenshot captions explain what the reader is seeing;
- [ ] GIF/video demonstrates behavior rather than acting as decoration;
- [ ] architecture diagrams answer a concrete question;
- [ ] visuals are placed near the text they clarify;
- [ ] the README is not dominated by badges or decorative graphics;
- [ ] light/dark rendering remains usable where relevant.

Ask of every image:

> What does this help an uninvolved reader understand faster than text alone?

If the answer is unclear, remove or replace it.

## Use-case and exploration review

The repository should make its usefulness tangible.

Check whether a reader can identify at least one of:

- a concrete use case;
- an example workflow;
- an input → system → output path;
- a meaningful UI interaction;
- an API/CLI example;
- a research or engineering question the project helps answer.

For libraries/frameworks, explain what someone could build on top of the current abstraction.

For applications, explain what the user can observe or accomplish now.

## Vision / foundation review

A good portfolio project may also show where its architecture could lead.

Check:

- [ ] current capability is clearly separated from future potential;
- [ ] possible extensions follow naturally from existing architecture;
- [ ] the text explains why the current design is a useful foundation;
- [ ] no speculative feature is presented as implemented;
- [ ] vision is concise enough that it strengthens rather than dilutes the current project.

Useful pattern:

```text
Today: what works
↓
Foundation: what abstraction/capability now exists
↓
Possible extensions: what could be added without redefining the project
```

## Fresh-eye technical review

Read the repository from the top without relying on project history.

Check:

- [ ] repository name is understandable;
- [ ] GitHub description matches the README;
- [ ] internal and external links work;
- [ ] architecture diagrams render;
- [ ] installation commands match current files;
- [ ] runtime commands still exist;
- [ ] test/CI commands match the repository;
- [ ] project-status claims are current;
- [ ] limitations/non-goals are visible;
- [ ] deep docs are linked rather than duplicated unnecessarily;
- [ ] internal jargon is introduced only after its meaning is clear.

## Reproducibility review

Where practical, validate from a clean environment:

```text
clone
→ create environment
→ install
→ run deterministic checks
→ start the simplest supported entry point
```

Do not require paid/live providers merely to call a repository reproducible. Document external prerequisites explicitly.

## GitHub presentation review

- [ ] description;
- [ ] topics;
- [ ] homepage decision;
- [ ] license decision;
- [ ] README;
- [ ] screenshots/GIFs;
- [ ] current `main` CI state;
- [ ] issue tracker is not dominated by accidental/internal noise;
- [ ] default branch is correct.

## Evidence review

For every prominent claim, ask:

1. Where can an external reviewer verify this?
2. Is the evidence current?
3. Does a screenshot imply more than it proves?
4. Does CI actually prove the advertised property?
5. Are integration/runtime claims separated from deterministic checks?
6. Is a future possibility clearly marked as future rather than current functionality?

Rewrite or remove claims that cannot be defended.

## Public-readiness review for private/local projects

Before changing visibility:

- [ ] repeat the WP2 secret/history audit;
- [ ] inspect tracked, ignored, and untracked local state;
- [ ] verify no local datasets/account artifacts are included unintentionally;
- [ ] confirm license decision;
- [ ] confirm documentation does not expose private infrastructure;
- [ ] confirm screenshots do not expose sensitive information.

## Portfolio signal review

Before calling the repository finished, be able to state in one sentence:

> What capability does this repository prove about the author that another featured repository does not?

If the answer is unclear, improve positioning rather than inventing functionality.

## Acceptance criteria

- [ ] Repository is understandable without project history.
- [ ] The opening gives a justified reason to keep reading.
- [ ] A reader can identify what they can explore, run, inspect, or build on.
- [ ] Visuals materially improve comprehension.
- [ ] Technical depth appears after sufficient orientation.
- [ ] Current capability and future potential are clearly separated.
- [ ] Current `main` is the intended presentation state.
- [ ] Important automated checks are green.
- [ ] Documentation commands are current.
- [ ] No known sensitive material is exposed.
- [ ] Prominent claims are evidence-backed.
- [ ] The project's distinct portfolio signal can be stated clearly.
- [ ] No unnecessary portfolio-only architecture has been introduced.
- [ ] Repository is ready to link directly from profile/CV.

## Required outcome

End WP4 with exactly one readiness class:

- **READY** — suitable for profile/CV use;
- **READY WITH LIMITATIONS** — usable with explicit documented limitations;
- **NOT READY** — concrete blockers remain.

If the result is not `READY`, list the blockers explicitly rather than using vague status language.

## WP4 output format

For consistency, record:

```text
Readiness: READY | READY WITH LIMITATIONS | NOT READY

Reader experience:
- strengths
- remaining friction

Technical/public readiness:
- strengths
- blockers or limitations

Evidence:
- key checks / links / artifacts

Portfolio signal:
- one sentence

Changes made in WP4:
- only concrete corrections discovered by the audit
```
