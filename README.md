# Game Dev Director

`game-dev-director` is a Codex skill that helps an agent inspect, plan, challenge,
iterate on, and ship game projects—from a 48-hour jam to a commercial release.

The skill adapts to the project's scale and actual maturity. It can start with a
new idea or reconstruct an existing project, then keeps continuity in a small
`.game-dev/` project record.

## Install

Copy [`game-dev-director`](game-dev-director) into your Codex skills directory:

```text
~/.codex/skills/game-dev-director/
```

Then ask Codex to use `$game-dev-director` for a game project. On first use it
will inspect the project, ask only consequential questions, and propose or
create the smallest useful project state.

## Operating loop

```text
Inspect → Understand → Challenge → Plan → Build → Playtest → Learn → Reprioritize → Repeat
```

The skill directs the work; engine-specific skills and project conventions
still govern implementation details.
