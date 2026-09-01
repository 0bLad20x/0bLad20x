# WP2 — Hygiene & Metadata

## Goal

Make the repository safe to expose, easy to discover, and free of avoidable local/development noise.

WP2 is primarily repository hygiene and GitHub metadata. It should not introduce product behavior.

## Entry criteria

- WP1 is stable enough that the intended public identity of the project is known.
- Configuration, local state, generated artifacts, and repository history can be inspected.

## Security and privacy audit

Check current files and, where practical, Git history for:

- [ ] `.env` or environment variants;
- [ ] API keys, tokens, passwords, credentials;
- [ ] cookies, browser profiles, sessions;
- [ ] private certificates or SSH keys;
- [ ] local databases or dumps;
- [ ] personal/private data;
- [ ] private URLs/endpoints;
- [ ] machine-specific absolute paths;
- [ ] logs and large generated outputs;
- [ ] provider/account artifacts.

If a secret was ever committed, deleting the current file is not sufficient. Rotate the credential and clean history when required.

## `.gitignore` audit

Include only categories justified by the actual toolchain. Common examples:

```text
.env
.env.*
!.env.example

virtual environments
Python caches
test/lint/typecheck caches
coverage
packaging/build output
node_modules
logs
OS/editor noise
local data
runtime/session artifacts
```

Do not ignore files required for reproducible setup.

## Configuration audit

- [ ] `.env.example` contains placeholders only.
- [ ] Required environment variables are documented.
- [ ] Example configuration is sufficient to understand setup.
- [ ] Secrets are read from environment/configuration rather than hard-coded.

## Repository metadata

### Description

One sentence describing the actual product.

### Topics

Use focused discovery keywords rather than a keyword dump.

### Homepage

Set only when a meaningful public demo/docs/product URL exists.

### License

Make a deliberate decision:

- add an OSS license when reuse is intended;
- omit it when public source visibility should not imply permission to reuse.

Do not add a license automatically because other repositories have one.

## Root structure audit

Common useful public files, when relevant:

```text
README.md
.gitignore
.env.example
requirements.txt / pyproject.toml / package.json
src/
tests/
docs/
.github/
```

Optional for mature OSS/release projects:

```text
LICENSE
CONTRIBUTING.md
SECURITY.md
CHANGELOG.md
```

Only add optional files when the repository actually owns those processes.

## Actions

- Harden `.gitignore` against actual local/runtime artifacts.
- Remove accidental local/generated files from tracking.
- Confirm example configuration contains no secrets.
- Inspect Git history for high-risk credential files where feasible.
- Set GitHub description.
- Set focused topics.
- Decide homepage intentionally.
- Decide license intentionally.
- Check that README links and media paths are stable.

## Do not

- add generic governance files with no process behind them;
- add a license by default;
- publish a private project before checking history;
- create fake demo links;
- remove useful technical artifacts merely to make the root look smaller.

## Acceptance criteria

- [ ] No known secrets/private runtime state are exposed.
- [ ] `.gitignore` reflects the actual toolchain.
- [ ] `.env.example` is safe and useful.
- [ ] Description is set.
- [ ] Topics are set.
- [ ] Homepage decision is intentional.
- [ ] License decision is intentional.
- [ ] Repository root is understandable.
- [ ] No product logic changed solely for WP2.
