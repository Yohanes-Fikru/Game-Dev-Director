# Project Record Layout

All durable project knowledge lives under `<project>_docs/game-dev/` at the
repository root, where `<project>` is the repository root folder name (for a
checkout at `~/games/cursed-relics/`, the record is
`cursed-relics_docs/game-dev/`). Create a file only when it will preserve
knowledge worth resuming from.

The folder is plain Markdown in a visible, distinctly named directory so the
user can open or add it to an Obsidian vault and pick it out of a list of
folders. Never place it under an engine-managed asset folder such as Unity's
`Assets/` or Godot's `res://` import roots.

## Resolving the docs folder

1. If `<project>_docs/` exists at the repository root, use it.
2. Otherwise, if exactly one `*_docs/` folder exists at the root, use it and
   note the name in the Director Brief.
3. Otherwise, create `<project>_docs/` the first time a record is written.
4. If a legacy `.game-dev/` folder exists, keep reading it, and offer to move
   its contents into `<project>_docs/game-dev/` (update links; do not
   duplicate). Move only with the user's agreement.

Other project documentation (design notes, art bibles, marketing copy) may
live in `<project>_docs/` alongside `game-dev/`; do not reorganize it.

## Layout

| Path | Cardinality | Maintenance |
| --- | --- | --- |
| `<project>_docs/game-dev/PROJECT_STATE.md` | single | Update in place; the resume point for every session |
| `<project>_docs/game-dev/GAME_VISION.md` | single | Update in place when the promise, pillars, or scope boundary change |
| `<project>_docs/game-dev/DECISIONS.md` | single | Append new entries; mark superseded ones instead of deleting |
| `<project>_docs/game-dev/ASSUMPTIONS.md` | single | Update rows in place as evidence arrives |
| `<project>_docs/game-dev/RISKS.md` | single | Update rows in place; remove retired risks |
| `<project>_docs/game-dev/iterations/NNN-short-slug.md` | one per iteration | Create at plan time; fill `Result` at review |
| `<project>_docs/game-dev/playtests/YYYY-MM-DD-short-slug.md` | one per playtest | Create per session; never rewrite observations afterwards |

Number iterations with three digits (`001`, `002`, …). Use short lowercase
hyphenated slugs (`003-dash-cancel`, `2025-03-14-first-external-test`).

## Rules

- Start each file from the matching template under `assets/templates/`.
- Write standard Markdown: relative links (`[text](path.md)`), not
  `[[wikilinks]]`, so files render on GitHub and in Obsidian alike. Do not
  create or edit `.obsidian/` configuration; that belongs to the user.
- `PROJECT_STATE.md` holds the current objective, `NOW`/`NEXT` focus, and
  links to the active iteration and latest playtest. Detail lives in the
  per-iteration and per-playtest files, not in `PROJECT_STATE.md`.
- Link to builds, recordings, telemetry, and external docs; do not copy them in.
- If the project already keeps equivalent documentation elsewhere, reference it
  from `PROJECT_STATE.md` instead of duplicating it.

## Profile minimums

- `micro`: at most `<project>_docs/game-dev/PROJECT_STATE.md`; none at all if
  the project lasts under a day. No other records.
- Jams and critical deliveries: a must/should/cut list inside
  `PROJECT_STATE.md` is sufficient. See [game-jam.md](game-jam.md).
- `small` and above: add the other files only when their absence would cause
  rework or lost evidence.
