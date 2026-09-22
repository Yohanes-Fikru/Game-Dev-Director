# Iteration Engine

The unit of progress is a playable increment that tests a belief.

## Plan

State:

- objective: player or production outcome, not a task bundle;
- hypothesis: why the proposed change should improve that outcome;
- increment: the smallest integrated experience that can test it;
- success signals: observable behavior or measurable thresholds;
- kill or change signals when failure would otherwise invite sunk-cost drift;
- constraints and review point.

Put only work required for the increment in `NOW`. Prefer vertical slices
through interacting systems over completing one system in isolation.

## Build and review

Protect a runnable baseline. Build just enough fidelity for the question being
tested. Then playtest in the target context, separate observations from
interpretation, and decide:

- `KEEP`: evidence supports retaining the change;
- `CHANGE`: the belief remains plausible but implementation or framing failed;
- `CUT`: the value is not supported or the cost threatens the game.

Record the evidence and rationale, update the backlog, and choose the next
objective. Plans are disposable; decisions and evidence are durable.
