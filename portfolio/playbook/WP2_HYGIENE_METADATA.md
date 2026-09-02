# WP2 — Public Hygiene

## Goal

Make the repository safe and intentional to expose publicly.

This is a hygiene pass, not a reason to add product features or generic governance files.

## Check the repository

Review current files and, where practical, history for:

- secrets, API keys, tokens, passwords, cookies, sessions, certificates;
- `.env` files and provider/account artifacts;
- private data, private URLs, local databases or dumps;
- machine-specific paths, logs, generated output, caches and runtime state;
- screenshots or examples that expose sensitive information.

If a real credential was committed, removing the current file is not enough. Rotate it and clean history where necessary.

## Check setup and configuration

- `.gitignore` matches the actual toolchain and runtime artifacts;
- `.env.example` contains placeholders only;
- required configuration is understandable;
- files required for reproducible setup are not accidentally ignored.

## Check the GitHub surface

Keep the public metadata simple and accurate:

- repository name;
- one-sentence description;
- focused topics;
- homepage/demo link only when one really exists;
- social preview when a useful maintained visual is available;
- deliberate license decision.

Do not add `LICENSE`, `CONTRIBUTING`, `SECURITY`, `CHANGELOG`, or similar files merely because mature OSS repositories have them. Add them only when the project actually owns those processes.

## Done when

- [ ] No known secret, private runtime state, or sensitive visual is exposed.
- [ ] `.gitignore` and example configuration match the real project.
- [ ] GitHub description/topics accurately represent the project.
- [ ] Homepage, preview image, and license have intentional decisions.
- [ ] The repository root is understandable without removing useful technical files.
- [ ] No product behavior or governance machinery was added solely for presentation.
