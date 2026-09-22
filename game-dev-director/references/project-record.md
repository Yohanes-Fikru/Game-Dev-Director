# Project Record Layout

All durable project knowledge lives under `.game-dev/` at the repository root.
Create a file only when it will preserve knowledge worth resuming from.

## Layout

| Path | Cardinality | Maintenance |
| --- | --- | --- |
| `.game-dev/PROJECT_STATE.md` | single | Update in place; the resume point for every session |
| `.game-dev/GAME_VISION.md` | single | Update in place when the promise, pillars, or scope boundary change |
| `.game-dev/DECISIONS.md` | single | Append new entries; mark superseded ones instead of deleting |
| `.game-dev/ASSUMPTIONS.md` | single | Update rows in place as evidence arrives |
| `.game-dev/RISKS.md` | single | Update rows in place; remove retired risks |
| `.game-dev/iterations/NNN-short-slug.md` | one per iteration | Create at plan time; fill `Result` at review |
| `.game-dev/playtests/YYYY-MM-DD-short-slug.md` | one per playtest | Create per session; never rewrite observations afterwards |

Number iterations with three digits (`001`, `002`, …). Use short lowercase
hyphenated slugs (`003-dash-cancel`, `2025-03-14-first-external-test`).

## Rules

- Start each file from the matching template under `assets/templates/`.
- `PROJECT_STATE.md` holds the current objective, `NOW`/`NEXT` focus, and
  links to the active iteration and latest playtest. Detail lives in the
  per-iteration and per-playtest files, not in `PROJECT_STATE.md`.
- Link to builds, recordings, telemetry, and external docs; do not copy them in.
- If the project already keeps equivalent documentation elsewhere, reference it
  from `PROJECT_STATE.md` instead of duplicating it.

## Profile minimums

- `micro`: at most `.game-dev/PROJECT_STATE.md`; none at all if the project
  lasts under a day. No other records.
- Jams and critical deliveries: a must/should/cut list inside
  `PROJECT_STATE.md` is sufficient. See [game-jam.md](game-jam.md).
- `small` and above: add the other files only when their absence would cause
  rework or lost evidence.
