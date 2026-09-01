# Solana Token Observatory — Portfolio Project Card

**Portfolio status:** Featured  
**Repository status:** WP4 READY  
**Portfolio role:** End-to-end applied AI / data product

Repository: https://github.com/0bLad20x/solana-token-observatory

## Why this project belongs in the portfolio

The repository demonstrates one complete engineering story rather than a single isolated technique:

```text
problem framing
→ live multi-source ingestion
→ observation and persistence semantics
→ deterministic lifecycle automation
→ read-only product interface
→ bounded LLM-assisted investigation
→ tests + CI + explicit evidence boundaries
```

It is currently the strongest public example of taking an applied AI/data problem from system definition through implementation, operation, frontend exposure, and verification.

## WP5 selection score

| Question | Score | Evidence |
|---|---:|---|
| Solves an understandable problem | 2/2 | high-churn token discovery creates an explicit observation-capacity problem |
| Working end-to-end behavior | 2/2 | discovery, observation, persistence, lifecycle, Observatory, and Analyst paths are implemented |
| Demonstrates relevant technical ability | 2/2 | Python, APIs, PostgreSQL, async processing, frontend state, LLM/tool integration, testing |
| Adds a distinct portfolio signal | 2/2 | applied end-to-end product rather than framework/infrastructure only |
| Understandable / demonstrable quickly | 2/2 | reader-first README plus maintained screenshots/GIF and clear system path |

**Total: 10/10 — featured candidate.**

## Canonical profile copy

### Short

**Solana Token Observatory** — a real-time observation and research system that discovers emerging Solana tokens, preserves meaningful source-version changes, reduces the tracked population with deterministic lifecycle rules, and exposes the resulting state through a read-only Observatory with bounded AI-assisted research.

### One-line signal

**Discover → observe → filter → investigate emerging Solana tokens in real time.**

## CV / application copy

### Compact project entry

**Solana Token Observatory — End-to-end AI/data system**  
Designed and implemented a real-time Solana token observation pipeline with multi-source discovery, version-aware PostgreSQL persistence, deterministic lifecycle automation, an interactive read-only Observatory, and bounded LLM-assisted analysis. Added backend/frontend contract tests and GitHub CI with explicit separation between deterministic checks and live integration concerns.

### Evidence bullets

- Designed the end-to-end data path from multi-source mint discovery through continuous observation, source-version persistence, lifecycle reduction, and interactive investigation.
- Integrated LLM tool calling, web research, temporal summaries, and RugCheck evidence while keeping lifecycle decisions deterministic and the UI/Analyst read-only.
- Defined architecture and frontend/lifecycle contracts, regression coverage, and CI-backed Python/frontend checks; public-readiness review completed with no known WP4 blockers.

### Technology line

Python · asyncio · REST APIs · PostgreSQL · FastAPI · LLM APIs · Tool Calling · GitHub Actions

## Distinct portfolio signal

Use this project to demonstrate:

- end-to-end implementation ownership;
- applied AI integration without giving the LLM operational authority;
- reasoning about real-time/high-churn data;
- architecture and data ownership boundaries;
- iterative debugging and validation;
- ability to turn an engineering system into understandable public evidence.

Do not primarily position it as a crypto/trading project. Its broader engineering signal is a **high-churn observation and research system** in which entities arrive continuously, upstream state changes asynchronously, and only a changing subset deserves continued observation.

## Pin recommendation

**Pin now.**

Solana Token Observatory is the first WP4-ready featured project. Keep it pinned while the rest of the portfolio is built. Re-evaluate the complete 3–5 repository pin set only after Modelrail, Model Pipeline, and any competing local projects complete WP4.

## Claims to avoid

Do not describe the project as:

- a trading engine;
- an investment recommendation system;
- a complete historical market index;
- production infrastructure proven against all live providers by CI;
- an autonomous LLM decision system.

The repository deliberately documents those boundaries.
