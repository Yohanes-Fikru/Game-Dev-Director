# Project Recovery

Use when the project is stalled, repeatedly rewritten, far behind, or no longer
has a credible playable target.

## Audit reality

Identify:

- the original and currently desired player experience;
- the last known-good playable build;
- scope added without validating the core;
- blocked dependencies, fragile systems, and missing ownership;
- sunk-cost work being protected without current evidence;
- the next external constraint or deadline.

Do not start with a rewrite. First attempt to isolate a playable spine from what
already works.

## Create a recovery milestone

Choose one player-visible target with a short review horizon. Classify work as
keep, repair, replace, defer, or cut. Put only blockers for that target in
`NOW`, assign a clear kill condition to risky rescue work, and preserve a
known-good build.

Recovery ends when the team can repeatedly build, play, evaluate, and plan from
evidence again—not when every historical problem is repaired.
