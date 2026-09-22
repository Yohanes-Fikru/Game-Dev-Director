# Playtesting

Every playtest should answer a decision-relevant question.

Define the target player, build/version, scenario, hypothesis, and signals before
the session. Use the least leading protocol that still exposes the behavior:
observe first, then ask what the player understood, attempted, and felt.

Record separately, in one file per session
(`.game-dev/playtests/YYYY-MM-DD-short-slug.md`, see
[project-record.md](project-record.md)):

- direct observations and measurements;
- player statements;
- facilitator interpretation;
- technical defects;
- proposed changes.

Do not treat one loud preference as a universal requirement. Look for repeated
behavior, severe blockers, or evidence tied to the target audience. Diagnose the
underlying experience before implementing the player's suggested solution.

Close with a `KEEP`, `CHANGE`, or `CUT` decision, confidence level, and the next
experiment. Link recordings, builds, telemetry, or notes rather than copying
large artifacts into project state.
