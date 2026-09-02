# WP4 — Final Review

## Goal

Look at the finished repository once as an uninvolved external visitor and fix only the remaining friction that would stop us from linking it confidently from a profile or CV.

WP4 is a review pass, not another build phase.

## Fresh-eye pass

Start from the public GitHub page, not from project history.

In the first 30–60 seconds, check:

- can I tell what the project is and why it exists?
- is there a strong real signal of the product or result?
- do I understand what I can explore, run, or build on?
- are the strongest project signals visible early enough?
- is anything repeated, defensive, stale, or unnecessarily long?

Then follow the natural rabbit holes:

- README → deeper docs;
- docs → relevant implementation where useful;
- claims → tests, CI, runtime evidence, or source.

The README does not need to contain every technical detail if the deeper path is clear.

## Verify the public state

Check only the things that can invalidate the presentation:

- important links and visuals work;
- setup/runtime commands match the current repository;
- the documented product matches the current code;
- important checks on `main` are green/current;
- no known sensitive material is exposed;
- GitHub description/topics/preview still fit;
- current limitations are not hidden.

Where practical, try the simplest clean setup/run path.

## Delete pass

WP4 should ask not only "what is missing?" but also:

> What can be removed, merged, or moved deeper without losing understanding?

Prefer a shorter path to the interesting parts over another layer of explanation.

## Result

Use a simple final decision:

- **READY** — comfortable to link directly as portfolio evidence;
- **NOT READY** — concrete blockers remain.

A READY repository may still have clearly documented limitations. Limitations are not automatically blockers.

If something is not ready, list the concrete blockers. Do not create process work to make the review look complete.

## Done when

- [ ] The repository works as a first impression without prior context.
- [ ] The README is concise enough that the strongest signals are not buried.
- [ ] Deeper technical material is reachable without being duplicated everywhere.
- [ ] Public claims, commands, visuals, and evidence match the current repository.
- [ ] No real safety/reproducibility blocker remains.
- [ ] We would be comfortable sending the repository link directly to a recruiter or engineer.
