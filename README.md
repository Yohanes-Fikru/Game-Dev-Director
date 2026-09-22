# Game Dev Director

`game-dev-director` is an Agent Skill that helps an agent inspect, plan, challenge,
iterate on, and ship game projects—from a 48-hour jam to a commercial release.

The skill adapts to the project's scale and actual maturity. It can start with a
new idea or reconstruct an existing project, then keeps continuity in a small
`.game-dev/` project record.

## Install

The skill is host-agnostic. Copy (or symlink) the
[`game-dev-director`](game-dev-director) directory into your host's skills
location:

| Host | Location |
| --- | --- |
| Codex | `~/.codex/skills/game-dev-director/` |
| Claude Code | `~/.claude/skills/game-dev-director/` (user) or `.claude/skills/game-dev-director/` (project) |
| GitHub Copilot | `.github/skills/game-dev-director/` |

Or, with the [`skills`](https://github.com/vercel-labs/skills) CLI:

```sh
npx skills add Yohanes-Fikru/AgenticGameDeveloper
```

Then ask your agent to use `game-dev-director` for a game project. On first use
it will inspect the project, ask only consequential questions, and propose or
create the smallest useful project state.

## Project record

Durable project knowledge lives under `.game-dev/` in the game repository:

```text
.game-dev/
├── PROJECT_STATE.md                 # single; updated in place; resume point
├── GAME_VISION.md                   # single
├── DECISIONS.md                     # single; appended
├── ASSUMPTIONS.md                   # single; updated in place
├── RISKS.md                         # single; updated in place
├── iterations/NNN-short-slug.md     # one per iteration
└── playtests/YYYY-MM-DD-short-slug.md  # one per playtest
```

Files are created only when they preserve useful knowledge; `micro` and jam
projects keep at most `PROJECT_STATE.md`. See
[`references/project-record.md`](game-dev-director/references/project-record.md)
and the filled-in
[`PROJECT_STATE.example.md`](game-dev-director/assets/examples/PROJECT_STATE.example.md).

## Operating loop

```text
Inspect → Understand → Challenge → Plan → Build → Playtest → Learn → Reprioritize → Repeat
```

The skill directs the work; engine-specific skills and project conventions
still govern implementation details.
