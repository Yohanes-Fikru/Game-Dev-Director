# Project State

Last verified: 2025-03-14

## Direction

- Game promise: Every run is a five-minute gamble where you choose which of
  three cursed relics to carry and the dungeon reshapes itself around that choice.
- Target player and platform: PC (Steam) players who like short-session
  roguelites (Downwell, Nuclear Throne); keyboard + gamepad.
- Process profile: small
- Overall stage: Prototype
- Hard constraints: solo developer, ~10 h/week, Godot 4.3, first public
  playable by 2025-05-01 for a local indie showcase.

## Current Iteration

- Objective: A first-time player finishes at least one full run (three rooms +
  boss) without being told the controls.
- Hypothesis: A relic choice screen before room 1 gives runs a visible identity
  early enough that players want a second run, even with placeholder art.
- Playable increment: Three relics with one mechanical effect each, a relic
  pick screen, and one boss that reads the equipped relic. No meta-progression.
- Success signals: 3 of 5 testers replay unprompted; median run length
  4–6 minutes; testers can name their relic after the run.
- Review point: after playtest on 2025-03-21, or when the boss is beatable.
- Iteration file: `.game-dev/iterations/003-relic-choice.md`

## Focus

### NOW

- Relic pick screen (three cards, keyboard and gamepad navigable)
- `Ember Heart` relic: fire trail on dash, self-damage on idle
- Boss reads equipped relic and swaps one attack accordingly
- Fix: player can clip through room 2 east door (blocks full-run test)

### NEXT

- Run summary screen with relic name and room count
- Placeholder SFX for relic pickup and boss phase change
- Second external playtest with five new players

## Risks and Unknowns

- Boss-per-relic variation triples boss work per relic; trigger: adding a fourth
  relic; mitigation: boss reads a relic *tag*, not the relic itself
  (see `.game-dev/RISKS.md`).
- Placeholder art may hide whether the relic identity reads; trigger: testers
  cannot name their relic; mitigation: one distinct color + silhouette per relic
  before the 03-21 test.
- Unknown: whether five-minute runs are long enough to feel like a gamble.
  Test: measure run length and ask "did the relic matter?" in the 03-21 test.

## Evidence and Links

- Latest playtest: `.game-dev/playtests/2025-03-07-internal-loop-test.md`
  (2 testers, `CHANGE`: loop works, no run identity)
- Known-good build: tag `proto-0.2` (Windows/Linux export, runs on clean machine)
- Design notes: `docs/relics.md`
- Decisions: `.game-dev/DECISIONS.md` (D-002: no meta-progression before showcase)
