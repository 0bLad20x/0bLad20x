# Portfolio Build — Working Standard

> **Status: Work in progress.** This directory is the current working source of truth while the portfolio is being built. The process is expected to evolve when later repositories expose better patterns, missing checks, or unnecessary steps.

## Purpose

The goal is to turn existing local, private, or unfinished repositories into public portfolio projects that are:

- understandable to an external reader;
- technically credible;
- safe to expose;
- reproducible where appropriate;
- explicit about what is actually verified;
- maintained without portfolio-specific process overhead becoming part of the product.

This is not a requirement that every repository looks identical. The work packages provide a repeatable **review process**. Their concrete implementation remains repository-specific.

## Current process

```text
existing project
    ↓
WP1 — Presentation & README
    ↓
WP2 — Hygiene & Metadata
    ↓
WP3 — Repository Quality & Automation
    ↓
WP4 — Final Portfolio Review
    ↓
WP5 — Profile Integration
```

Detailed work packages live under [`playbook/`](playbook/README.md).

## Current portfolio build status

| Project | WP1 | WP2 | WP3 | WP4 | WP5 | Next |
|---|---|---|---|---|---|---|
| [Solana Token Observatory](https://github.com/0bLad20x/solana-token-observatory) | Done | Done | Done | [READY](reviews/solana-token-observatory-wp4.md) | [Profile ready](reviews/solana-token-observatory-wp5.md) | Pin in GitHub UI |
| Modelrail | Pending | Pending | Pending | Pending | Pending | Initial repository review |
| LLM Model Pipeline | Pending | Pending | Pending | Pending | Pending | Initial repository review |
| Mandate | Candidate | Candidate | Candidate | Candidate | Candidate | Portfolio-fit review |

Curated project positioning and reusable CV/application copy live under [`projects/`](projects/).

The project set is intentionally not final. A local project may replace a current candidate if it provides stronger or more complementary evidence.

## Working rules

1. **Evidence over decoration.** Claims should map to code, tests, runtime behavior, documentation, or reproducible artifacts.
2. **Preserve product boundaries.** Do not add product architecture merely to make a repository appear more sophisticated.
3. **Automation must own a real responsibility.** A workflow is justified by a recurring check, integration, publication, security, or operational responsibility—not by the desire to have more badges.
4. **Separate deterministic and live evidence.** Core CI should be reproducible without production credentials; database/provider/browser/live-service checks belong in explicit integration workflows when justified.
5. **Use repository-specific depth.** A provider-oriented framework may warrant provider matrices and live smoke tests; a small application may only need one compact CI workflow.
6. **Public exposure is a deliberate step.** Secret/history review, metadata, license decision, docs, and current evidence are checked before a private/local project becomes portfolio evidence.
7. **This standard can change.** When a later repository reveals a better reusable pattern, update the playbook rather than silently changing the process for only one project.
8. **Pins are earned, not filled.** Do not use profile pin slots for projects that have not reached the same evidence standard merely to make the profile look complete.

## How to use this directory

For each repository:

1. start from the next incomplete WP;
2. copy its checklist into an issue, planning note, or agent task;
3. remove items that genuinely do not apply;
4. add repository-specific checks only when a concrete responsibility justifies them;
5. record new reusable lessons back in this playbook.

The generic [`WP_TEMPLATE.md`](playbook/WP_TEMPLATE.md) is used for additional work packages such as provider live-smoke tests, package releases, deployment, generated catalogs, or security monitoring.
