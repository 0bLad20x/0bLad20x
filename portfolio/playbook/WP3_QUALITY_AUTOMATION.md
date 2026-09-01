# WP3 — Repository Quality & Automation

## Goal

Expose credible, repeatable repository quality signals with the smallest automation that matches the project's real responsibilities.

WP3 is **not** a governance layer. It should not create approval chains, agent hierarchies, or process gates unless the repository actually requires them.

## Step 1 — Inventory existing evidence

Before creating workflows, identify what already exists:

- unit tests;
- contract tests;
- integration tests;
- compile/build commands;
- lint/type/static checks;
- CLI smoke checks;
- schema/catalog validation;
- provider tests;
- database-backed checks;
- release/package tests.

Do not invent checks merely to fill a CI template.

## Step 2 — Classify every check

### A. Core deterministic CI

Suitable for normal pull-request/push CI:

- compilation/build from committed inputs;
- unit tests;
- contract tests;
- lint/type/static checks;
- CLI startup/help checks without external services;
- schema/catalog validation;
- generation + validation from committed inputs.

### B. Integration workflows

Keep separate when checks require:

- PostgreSQL or another external database;
- real provider credentials;
- browser sessions;
- OAuth/account flows;
- paid APIs;
- external service availability.

Possible triggers: manual, scheduled, path-filtered, or pre-release.

### C. Operational/release workflows

Examples:

- publishing packages;
- deployments;
- scheduled provider compatibility;
- generated catalog publication;
- dependency/security monitoring.

Only add these when the project owns those operations.

## Step 3 — Design core CI

A compact CI normally looks like:

```text
checkout
→ setup runtime
→ install dependencies
→ compile/static check
→ tests
→ minimal smoke checks
```

Recommended hardening:

- [ ] minimal workflow `permissions`, normally `contents: read`;
- [ ] external GitHub Actions pinned to exact commit SHAs where practical;
- [ ] `persist-credentials: false` when checkout does not need push credentials;
- [ ] `concurrency` with `cancel-in-progress: true` where superseded PR runs waste time;
- [ ] reasonable job timeouts;
- [ ] clear job names;
- [ ] no production credentials in ordinary PR CI;
- [ ] no `|| true`/`continue-on-error` on checks presented as successful quality evidence.

## Step 4 — Decide whether path filtering helps

Use path filters when a subsystem has a distinct responsibility.

Example:

```yaml
pull_request:
  paths:
    - 'packages/ai/**'
    - 'scripts/generate-catalog.*'
    - '.github/workflows/provider-catalog.yml'
```

Do not add path filtering when a small repository's normal CI is already cheap and clear.

## Step 5 — Provider/package-specific pattern

Useful for provider-oriented frameworks such as Modelrail or a model pipeline:

```text
ci.yml
    core deterministic contracts

provider-contracts.yml
    provider adapter contract matrix
    no live credentials when possible

provider-live-smoke.yml
    real provider/API checks
    manual or scheduled
    explicitly integration evidence

catalog.yml
    generate
    validate
    artifact
    optional publish
```

Prefer a matrix when all providers implement the same contract. Prefer separate workflows when providers have materially different setup/runtime requirements.

## Step 6 — Define evidence semantics

Document what a workflow proves and what it does not prove.

Example:

**Core CI proves**

- the repository installs on a clean runner;
- source compiles;
- deterministic tests pass;
- CLI entry points load.

**Core CI does not prove**

- live provider availability;
- production credential correctness;
- database runtime health;
- deployment availability.

Historical failed workflow runs remain part of GitHub history. Re-running an old run executes the historical workflow revision associated with that run, not necessarily the latest workflow on `main`.

## Step 7 — Security/dependency automation

Possible additions:

- dependency audit;
- CodeQL;
- package signature verification;
- scheduled vulnerability scans.

Add them because the dependency/security surface justifies them, not because large OSS repositories have them.

## Step 8 — Releases and artifacts

If a repository publishes packages or generated catalogs, consider:

- build artifacts;
- source-bound generated outputs;
- release smoke tests;
- scheduled catalog refresh;
- package publication workflows.

A portfolio application with no package/release lifecycle does not need release automation.

## Anti-patterns

Avoid:

- one giant workflow mixing unit tests, live APIs, DB integration, publishing, and deployment;
- fake credentials used only to make CI green;
- simulated/random checks presented as real integration evidence;
- `continue-on-error` for checks advertised as gates;
- dozens of workflows with unclear ownership;
- badges whose evidence meaning is undocumented.

## Acceptance criteria

- [ ] Existing evidence was inventoried before automation was added.
- [ ] Each automated check has a clear repository responsibility.
- [ ] Deterministic CI is separated from live integration.
- [ ] Core CI passes on a clean runner.
- [ ] Workflow permissions are minimal.
- [ ] External Actions are pinned where practical.
- [ ] Superseded runs are cancelled when useful.
- [ ] Timeouts prevent runaway jobs.
- [ ] Core CI does not require production credentials.
- [ ] README/docs state what automation proves and does not prove.
- [ ] No product logic was added solely to create a green workflow.

## Reference: Solana Token Observatory

The Solana project uses one compact CI workflow because its current deterministic quality surface is small and coherent:

- Python setup and dependency installation;
- source compilation;
- Python tests;
- CLI entry-point checks;
- frontend contract tests.

The workflow is hardened with read-only permissions, pinned Actions, non-persisted checkout credentials, concurrency cancellation, and explicit timeouts.

PostgreSQL-backed lifecycle equivalence, live providers, real credentials, and operational runtime health remain outside core CI because they are integration/runtime concerns rather than deterministic repository evidence.
