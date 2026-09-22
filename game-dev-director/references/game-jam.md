# Game Jam and Critical Delivery

Trigger this route for a short jam or an imminent demo/submission deadline.

Priority order:

1. The build runs on the target machine.
2. A player can complete a clear playable loop.
3. The game communicates its premise and controls.
4. Progress and user data are not lost.
5. Everything else is optional.

Confirm the hard deadline, submission requirements, current runnable state, and
the single mechanic that must survive. Freeze feature intake. Maintain a short
must/should/cut list and cut dependencies that cannot be validated in time.

Keep the project record minimal: a must/should/cut list inside
`<project>_docs/game-dev/PROJECT_STATE.md` is sufficient. Do not create
iteration, playtest, decision, or risk files during the jam; skip the record
entirely if the project lasts under a day.

Work in build-sized increments, keep a known-good artifact, and reserve explicit
time for packaging and a clean-machine smoke test. Defer broad design questions,
refactors, optional settings, generalized tools, and polish without visible
player value.
