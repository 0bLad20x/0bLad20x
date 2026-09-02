# WP1 — Presentation

## Goal

Make the project understandable and interesting to someone who has no prior context.

WP1 is not about making the repository sound impressive. It is about finding the strongest real signals in the project and presenting them with the least friction.

## Start by reading the project

Before rewriting the README, inspect the implementation, tests, existing docs, runtime behavior, and available visuals.

Identify:

- what the project actually does end to end;
- what a user can see, run, explore, or build on;
- the strongest product experience;
- the strongest engineering decisions;
- which details are useful hooks and which belong only in a technical rabbit hole;
- what is already visually demonstrable.

Do not assume the most heavily documented part of the current README is the most interesting part of the project.

## README job

The first screen or two should answer:

1. What is this?
2. Why does it exist?
3. What can I see or do with it?
4. What makes it worth exploring further?

Then add enough depth to explain the system at a high level and expose the most interesting technical signals.

A typical flow may be:

```text
name + one sentence
↓
strong visual / concrete result
↓
problem and product experience
↓
how it works at a glance
↓
selected engineering highlights
↓
run / verify / deeper docs
```

This is a writing guide, not a required heading template.

## Progressive depth

Keep the README focused on orientation and the main story. Put detailed contracts, algorithms, data semantics, provider behavior, or subsystem internals in `docs/` when they are useful there.

A good path is:

```text
README claim
→ relevant deep-dive doc
→ source / test when someone wants proof
```

Do not repeat the same explanation at every layer.

## Visuals

Use visuals only when they communicate faster than prose:

- **Screenshot** — what the product/state looks like;
- **GIF/video** — behavior, interaction, or motion;
- **Diagram** — relationships, flow, or architecture.

Prefer a few strong visuals over documenting every subsystem visually.

## Writing quality

AI-assisted authorship is fine. AI-shaped redundancy is not.

Remove or compress:

- repeated explanations of the same idea;
- generic statements that something is "interesting" instead of showing why;
- excessive caveats and defensive wording;
- speculative feature lists;
- sections that exist only because a template suggested them.

Current capability should remain clearly separate from possible future use.

## AI-assisted development

If AI coding tools materially contributed, say so plainly and briefly. Do not hide it, and do not turn the section into a long responsibility defense. The repository itself should provide the engineering evidence.

## Done when

- [ ] An uninvolved reader can explain the project after the first screen or two.
- [ ] The opening shows a real product/result/behavior when the project has something visual to show.
- [ ] The strongest project signals come from the implementation, not from inherited README emphasis.
- [ ] The README progresses from simple understanding to optional technical depth.
- [ ] Important claims are accurate and link naturally to deeper evidence.
- [ ] Redundant detail has been removed or moved to `docs/`.
- [ ] Visuals explain something rather than decorate the page.
- [ ] Current capability, limitations, and future possibilities are not confused.
