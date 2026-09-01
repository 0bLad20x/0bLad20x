# Portfolio Repository Playbook

This playbook is a reusable review and improvement process for turning an existing repository into credible public portfolio evidence.

A portfolio repository must do two things at once:

1. **stand up technically** under inspection;
2. **earn attention** from a reader who has no prior context.

The goal is not marketing polish detached from engineering. The goal is to make the engineering easy to understand, interesting to explore, and honest about what is proven.

## Work packages

| WP | Name | Main question |
|---|---|---|
| [WP1](WP1_PRESENTATION.md) | Presentation & README | Can an external reader quickly understand the project, see why it matters, and want to explore further? |
| [WP2](WP2_HYGIENE_METADATA.md) | Hygiene & Metadata | Is the repository safe, clean, intentional, and discoverable? |
| [WP3](WP3_QUALITY_AUTOMATION.md) | Repository Quality & Automation | Which existing quality signals should be exposed automatically, and how? |
| [WP4](WP4_FINALIZATION.md) | Final Portfolio Review | Is the repository technically credible **and** compelling enough to use as direct portfolio evidence? |
| [WP5](WP5_PROFILE_INTEGRATION.md) | Profile Integration | Should this project be featured, and what distinct signal does it add? |

Use [WP_TEMPLATE.md](WP_TEMPLATE.md) for project-specific work packages that do not belong in the universal sequence.

## Principle: optimize the reader journey, not just the document

A README is not a flat specification. A strong technical portfolio normally offers progressive depth:

```text
What is this?
↓
Why should I care?
↓
Show me something real
↓
What can I do / explore?
↓
How does it work?
↓
What makes the engineering interesting?
↓
How can I run or inspect it?
↓
What is proven, limited, or extensible?
```

The exact section names are not standardized. The questions the reader needs answered are.

Visuals, demos, examples, diagrams, and traces are useful when they shorten the path to understanding. They are not decoration requirements.

## Principle: current capability before future possibility

A repository may explain what its architecture is a foundation for, but must distinguish:

```text
implemented now
≠
natural extension
≠
long-term vision
```

Future potential should increase understanding of the current architecture, not inflate the feature list.

## Principle: standardize evaluation, not machinery

Two repositories may both complete WP3 while ending with very different automation:

```text
small application
└── one deterministic CI workflow

provider framework
├── core CI
├── provider contract matrix
├── scheduled/manual live-provider smoke
└── catalog/release workflow
```

Both can be correct if the automation maps to real repository responsibilities.

## Evidence classes

### Deterministic repository evidence

Suitable for normal pull-request CI:

- compilation/build from committed inputs;
- unit tests;
- contract tests;
- lint/type/static checks;
- schema or catalog validation;
- CLI smoke checks without external services;
- generated artifact validation from committed inputs.

### Integration evidence

Usually separate from core CI:

- real PostgreSQL or other external database state;
- real provider credentials;
- browser sessions;
- OAuth/account flows;
- paid APIs;
- third-party service availability.

### Operational evidence

Usually scheduled, release-triggered, or manually dispatched:

- package publication;
- deployment smoke tests;
- scheduled provider compatibility;
- vulnerability/dependency monitoring;
- generated catalog refresh/publication.

## Decision test for new repository machinery

Before adding any workflow, gate, bot, generated artifact, or policy, answer:

1. What concrete repository responsibility does it own?
2. What recurring failure does it detect or prevent?
3. What does a green result actually prove?
4. Does it require live infrastructure or can it be deterministic?
5. Is there a smaller mechanism that provides the same evidence?

If the responsibility cannot be stated clearly, do not add the mechanism.

## Decision test for presentation material

Before adding a section, image, badge, diagram, or claim, answer:

1. What question does this answer for an uninvolved reader?
2. Does it make the project more concrete or merely longer?
3. Does it show current reality or speculation?
4. Is there evidence behind it?
5. Would the README become clearer if this moved into deeper documentation instead?

If it does not improve comprehension, confidence, or justified curiosity, omit it.

## Updating this playbook

The playbook is intentionally a working standard. Update it when a later project reveals a reusable improvement, for example:

- better reader-flow or visual explanation patterns;
- provider-specific path filters;
- package-level contracts;
- better supply-chain hardening;
- release artifact verification;
- a security practice that is useful across repositories.

Do not back-port every newly discovered technique to every project automatically. Re-evaluate applicability first.
