# WP5 — Profile Integration

## Goal

Integrate only the strongest completed repositories into the GitHub profile and CV so the portfolio communicates complementary capabilities rather than a random project inventory.

WP5 is curation, not another engineering pass. A WP4-ready repository should not gain new product architecture merely to fit the profile.

## Entry criteria

- Candidate repository has completed WP4.
- Public links resolve correctly.
- The repository is suitable for external review.
- Its distinct portfolio signal can be stated without inventing capabilities.

## Project selection score

Score each project from 0–2 on each question:

| Question | Score |
|---|---:|
| Solves an understandable problem | 0–2 |
| Has working end-to-end behavior | 0–2 |
| Demonstrates relevant technical ability | 0–2 |
| Adds a distinct portfolio signal | 0–2 |
| Can be understood/demonstrated quickly | 0–2 |

Typical interpretation:

- **8–10** — strong featured candidate;
- **6–7** — useful but may need more work or a clearer story;
- **0–5** — normally leave unfeatured/private.

Record the score and reasoning rather than keeping the selection only in chat.

## Define the project's portfolio role

A featured repository should own one primary signal in the portfolio.

Example composition:

```text
End-to-end product
    ↓
AI runtime / automation
    ↓
AI infrastructure / provider abstraction
    ↓
optional deep architecture project
```

Prefer complementary evidence rather than several repositories telling the same story. The exact projects can change while the portfolio is being built.

## Create a canonical project card

Store a small durable project card under a shared portfolio directory, for example:

```text
portfolio/projects/<repository>.md
```

Recommended contents:

- portfolio status;
- portfolio role;
- WP5 selection score;
- canonical short profile copy;
- one-line project signal;
- compact CV/application entry;
- 2–3 evidence bullets;
- technology line;
- pin recommendation;
- claims/positioning to avoid.

The purpose is to stop profile, CV, application, and later portfolio edits from independently inventing different stories for the same repository.

## GitHub profile README

For each selected project include only enough information to create a useful path into the repository:

- project name;
- one-sentence value statement;
- direct repository link;
- optionally one strong visual;
- one compact set of technical/evidence signals.

A visual should explain the project, not decorate the profile. Prefer a maintained product screenshot/demo already owned by the project repository.

Do not duplicate the full project README on the profile.

## GitHub pins

Aim for roughly 3–5 repositories **after** enough projects have earned that status.

Rules:

1. **Pins are earned, not filled.** Do not pin unfinished projects simply to occupy empty slots.
2. A repository should normally be WP4-ready before it becomes a portfolio pin.
3. Pinning is curation, not a complete project inventory.
4. Re-evaluate the full pin set when another project reaches WP4; do not assume an earlier pin remains optimal forever.
5. If the available automation/API cannot change profile pins, record the recommendation explicitly and leave one clear manual UI action instead of claiming completion.

## CV integration

CV entries should be more aggressively curated than GitHub.

Useful structure:

```text
Problem / outcome
→ personal scope
→ relevant technologies
→ one or two credible technical signals
→ repository link
```

GitHub remains the evidence source; the CV is the compact summary.

Prepare canonical CV/application copy during WP5 even when the actual CV file is not yet being edited. Store it in the project card so later applications can reuse reviewed language.

## Final WP5 record

Create a short durable WP5 review record containing:

- selection score;
- portfolio role;
- profile changes;
- CV/application preparation;
- pin decision;
- any manual action still required;
- final status.

Useful final states:

- **DONE** — profile integration and intended pinning are complete;
- **PROFILE READY — MANUAL PIN PENDING** — all repository/document work is complete and only a GitHub UI pin remains;
- **NOT FEATURED** — repository is valid but intentionally not selected for the current portfolio set.

## Acceptance criteria

- [ ] Featured repositories are WP4-ready.
- [ ] Each featured repository adds a distinct capability signal.
- [ ] Selection score and reasoning are recorded.
- [ ] Canonical project/profile/CV copy is stored.
- [ ] Profile README statements match repository evidence.
- [ ] Profile visuals, when used, explain rather than decorate.
- [ ] Pinned projects represent the current strongest portfolio set; empty slots are acceptable.
- [ ] CV/application copy leads directly to useful public evidence.
- [ ] No private/unreviewable repository is presented as public proof.
- [ ] Manual pinning is explicitly tracked when automation cannot perform it.
- [ ] The project set can be revised later without changing the playbook process.
