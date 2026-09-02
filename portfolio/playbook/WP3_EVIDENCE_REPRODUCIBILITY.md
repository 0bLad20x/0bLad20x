# WP3 — Evidence & Reproducibility

## Goal

Make the project's important technical claims easy to trust and, where appropriate, easy to reproduce.

Tests, CI, Docker, runtime samples, integration checks, or generated artifacts are possible tools. None of them is mandatory by itself.

## Start with what already exists

Identify the current evidence and the simplest supported run path:

- tests and contract checks;
- build/compile/static checks;
- CLI or application startup;
- database/provider/browser requirements;
- existing CI;
- representative runtime output or artifacts.

Do not create new checks just to make the repository look mature.

## Choose the smallest useful mechanism

### Deterministic repository checks

Put stable checks in normal CI when that meaningfully improves trust or catches regressions. Examples include tests, build/compile checks, schema validation, and credential-free smoke checks.

Keep ordinary PR CI independent of production credentials where possible.

### Live or integration evidence

Real databases, provider credentials, browser sessions, OAuth, paid APIs, and third-party availability are different from deterministic repository checks. Keep them explicit rather than making normal CI fragile or faking the environment.

### Reproducible startup

Improve the setup path only as much as the project benefits from it.

Docker is useful when it materially removes environment/setup friction. A multi-service application may justify Docker Compose; a simple library may not need containers at all. Do not containerize a browser/session-heavy runtime merely to add a Docker badge.

### Representative runtime evidence

If scale or live behavior is part of what makes the project interesting, a clearly labelled captured run, benchmark, compatibility result, or sample artifact can be stronger evidence than another paragraph of description. Keep it reproducible or clearly timestamped so it does not masquerade as a permanent guarantee.

## Automation rules

When CI or another workflow is justified:

- keep permissions minimal;
- avoid production credentials in normal PR checks;
- use clear job names and reasonable timeouts;
- pin external actions where practical;
- do not hide failing evidence with `continue-on-error` or `|| true`;
- state what the workflow actually proves.

Separate additional provider, release, deployment, or security workflows only when the repository really owns those responsibilities.

## Done when

- [ ] The repository's important claims have visible evidence.
- [ ] The simplest supported setup/run path is understandable.
- [ ] Deterministic checks are reproducible without pretending to prove live infrastructure.
- [ ] CI exists only where it provides useful automatic evidence.
- [ ] Docker/containerization exists only where it meaningfully simplifies reproduction.
- [ ] Live/integration requirements are explicit rather than hidden or simulated.
- [ ] No product logic or infrastructure was added solely to manufacture a quality signal.
