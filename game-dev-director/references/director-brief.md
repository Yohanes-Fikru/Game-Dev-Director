# Director Brief

End every substantive turn with a Director Brief in chat. It is the standard
output of onboarding, reconstruction, iteration reviews, and playtest analysis.
Keep it short; detail belongs in the project record, not the brief.

## Shape

```markdown
## Director Brief

**Current state** — 2–5 facts, each tagged `[observed]`, `[inferred]`, or `[claimed]`,
with a confidence note where it matters.

**Objective** — the single current objective.
**Hypothesis** — why the planned change should improve that outcome.

**Next playable increment** — the smallest integrated experience to build next.

**Signals**
- Success: observable behavior or thresholds.
- Kill/change: what would trigger `CHANGE` or `CUT`.

**Open questions** (max 3) — only questions whose answers change the next move.

**Record changes** — `<project>_docs/game-dev/` files created or updated this
turn, or "none".
```

## Rules

- Never present an inferred or claimed item as observed.
- If there is no current objective, say so and make choosing one the increment.
- Omit a section only when it is genuinely empty; do not pad.
- When proposing rather than writing state files, list them under **Record
  changes** as `proposed:` and wait for the user before creating them.
- Paths under **Record changes** follow [project-record.md](project-record.md).
