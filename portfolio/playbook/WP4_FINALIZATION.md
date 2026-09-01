# WP4 — Final Portfolio Review

## Goal

Review the repository as a new external visitor and decide whether the current state is genuinely ready to be used as public portfolio evidence.

WP4 should primarily discover inconsistencies. It is not a reason to redesign a working system.

## Fresh-eye review

Read the repository from the top without relying on project history.

Check:

- [ ] repository name is understandable;
- [ ] GitHub description matches the README;
- [ ] the first README screen explains the project;
- [ ] hero screenshot/demo loads;
- [ ] internal and external links work;
- [ ] architecture diagrams render;
- [ ] installation commands match current files;
- [ ] runtime commands still exist;
- [ ] test/CI commands match the repository;
- [ ] project-status claims are current;
- [ ] limitations/non-goals are visible;
- [ ] deep docs are linked rather than duplicated unnecessarily.

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

Rewrite or remove claims that cannot be defended.

## Public-readiness review for private/local projects

Before changing visibility:

- [ ] repeat the WP2 secret/history audit;
- [ ] inspect tracked, ignored, and untracked local state;
- [ ] verify no local datasets/account artifacts are included unintentionally;
- [ ] confirm license decision;
- [ ] confirm documentation does not expose private infrastructure;
- [ ] confirm screenshots do not expose sensitive information.

## Acceptance criteria

- [ ] Repository is understandable without project history.
- [ ] Current `main` is the intended presentation state.
- [ ] Important automated checks are green.
- [ ] Documentation commands are current.
- [ ] No known sensitive material is exposed.
- [ ] Prominent claims are evidence-backed.
- [ ] No unnecessary portfolio-only architecture has been introduced.
- [ ] Repository is ready to link directly from profile/CV.

## Required outcome

End WP4 with exactly one readiness class:

- **READY** — suitable for profile/CV use;
- **READY WITH LIMITATIONS** — usable with explicit documented limitations;
- **NOT READY** — concrete blockers remain.

If the result is not `READY`, list the blockers explicitly rather than using vague status language.
