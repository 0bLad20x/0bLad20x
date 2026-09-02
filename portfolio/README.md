# Portfolio Build — Working Standard

> **Status: Work in progress.** This is a lightweight working process for turning existing repositories into clear, credible portfolio projects. It should evolve only when real project work shows a better way.

## Goal

A portfolio repository should be:

- understandable to someone with no prior context;
- interesting enough to explore further;
- safe to expose publicly;
- technically credible and evidence-backed;
- reproducible to the degree that the project actually requires.

The process standardizes the **questions we ask**, not the machinery every repository must contain.

## Repository process

```text
existing project
    ↓
WP1 — Presentation
    ↓
WP2 — Public Hygiene
    ↓
WP3 — Evidence & Reproducibility
    ↓
WP4 — Final Review
    ↓
ready repository
```

After a repository is ready, portfolio/profile integration is a separate curation step rather than another repository work package.

Detailed guidance lives under [`playbook/`](playbook/README.md).

## Current portfolio build status

| Project | WP1 | WP2 | WP3 | WP4 | Portfolio | Next |
|---|---|---|---|---|---|---|
| [Solana Token Observatory](https://github.com/0bLad20x/solana-token-observatory) | Done | Done | Done | [READY](reviews/solana-token-observatory-wp4.md) | [Profile ready](reviews/solana-token-observatory-wp5.md) | Pin in GitHub UI / refine presentation |
| Modelrail | Pending | Pending | Pending | Pending | Pending | Initial repository review |
| LLM Model Pipeline | Pending | Pending | Pending | Pending | Pending | Initial repository review |
| Mandate | Candidate | Candidate | Candidate | Candidate | Candidate | Portfolio-fit review |

Curated project positioning and reusable CV/application copy may live under [`projects/`](projects/) when useful.

## Working rules

1. **Understand before presenting.** Inspect the actual product, code, tests, and runtime before deciding what the README should emphasize.
2. **Progressive depth.** GitHub metadata creates the first signal; README explains the project; `docs/` holds rabbit holes; source and tests provide verification. Do not duplicate the same explanation at every layer.
3. **Evidence over claims.** Important statements should map to working behavior, code, tests, runtime evidence, or reproducible artifacts.
4. **Complexity must earn itself.** CI, Docker, security workflows, release automation, extra documentation, or other machinery are added only when they solve a concrete problem.
5. **Public safety is non-negotiable.** Secrets, private data, local runtime state, and misleading claims are checked before a repository is used as public evidence.

## How to use this

Take the next unfinished WP, apply only the parts relevant to the repository, and stop when its goal is met. A WP is not a checklist quota. If a proposed mechanism does not improve understanding, safety, evidence, or reproducibility, do not add it.

Use [`WP_TEMPLATE.md`](playbook/WP_TEMPLATE.md) only when a repository exposes a real extra responsibility that does not fit WP1–WP4.
