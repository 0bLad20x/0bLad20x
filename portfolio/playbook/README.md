# Portfolio Repository Playbook

This playbook is a lightweight process for turning an existing repository into strong public portfolio evidence.

It is deliberately small. The goal is not to make every repository look identical or to introduce portfolio-specific governance.

## Repository work packages

| WP | Main question |
|---|---|
| [WP1 — Presentation](WP1_PRESENTATION.md) | Can an uninvolved reader quickly understand the project and see why it is worth exploring? |
| [WP2 — Public Hygiene](WP2_HYGIENE_METADATA.md) | Is the repository safe, intentional, and presentable in public? |
| [WP3 — Evidence & Reproducibility](WP3_EVIDENCE_REPRODUCIBILITY.md) | Can the important technical claims be trusted and, where appropriate, reproduced? |
| [WP4 — Final Review](WP4_FINALIZATION.md) | Would we now be comfortable sending this repository directly to a recruiter or engineer? |

After WP4, [`Portfolio Integration`](PORTFOLIO_INTEGRATION.md) decides whether and how the repository appears on the profile/CV. That is portfolio curation, not another repository engineering pass.

## Presentation depth

Use the natural GitHub layers rather than putting everything into the README:

```text
GitHub surface
name · description · topics · preview
        ↓
README
what · why · product experience · main technical signals
        ↓
docs/
technical rabbit holes
        ↓
source + tests
implementation and verification
```

These are writing layers, not required README headings.

## Core rules

**Inspect before presenting.** Do not inherit the existing README's emphasis automatically. Read the implementation and identify the strongest product and engineering signals first.

**Progressive depth.** A reader should get a useful picture quickly and be able to go deeper intentionally. Avoid explaining the same idea repeatedly at different depths.

**Visuals must explain.** Use a screenshot for state, a GIF for behavior, and a diagram for relationships when those formats communicate faster than prose.

**Evidence over decoration.** Tests, real behavior, reproducible commands, representative runtime evidence, and code matter more than badges or claims.

**Complexity must earn itself.** Before adding CI, Docker, a security workflow, another document, release automation, or any other layer, ask what concrete problem it solves. If the answer is unclear, omit it.

## Extra work packages

Use [WP_TEMPLATE.md](WP_TEMPLATE.md) only for a real repository-specific responsibility such as deployment, package publication, provider compatibility, or generated catalog release. Do not create extra WPs just because the template exists.

## Updating this playbook

Apply the process to real repositories first. Only promote a lesson into the playbook when it is clearly reusable. The playbook should stay smaller than the work it is helping to present.
