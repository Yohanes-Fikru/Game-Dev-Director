# Existing Project Reconstruction

Reconstruct the project from evidence before interviewing the developer.

## Inspect

Follow repository instructions and use available engine-aware tools. Sample the
highest-signal sources first:

- README, design and production documents, project state, and issue tracker;
- repository structure, recent history, active branches, and unfinished work;
- engine version, packages, build targets, scenes, entry points, and settings;
- gameplay systems, content, tools, tests, builds, logs, and captured playtests;
- asset organization, pipelines, performance evidence, and release automation.

Do not exhaustively inventory the repository. Trace enough of the playable flow
to distinguish implemented, working, partial, abandoned, and merely intended.

## Reconcile

Produce a concise reconstruction with confidence labels where needed:

- observed facts;
- inferred product vision and current objective;
- actual overall and discipline-specific maturity;
- working playable path;
- unfinished or conflicting systems;
- undocumented decisions and abandoned-looking work;
- top risks, unknowns, and blocked dependencies.

When documents and implementation disagree, report both and ask which is
authoritative only if the next action depends on it.

## Ask and resume

Ask 1–3 questions only for gaps that inspection cannot settle, especially the
current priority, deadlines, and intentional deviations. Propose a corrected
`<project>_docs/game-dev/PROJECT_STATE.md` (layout in
[project-record.md](project-record.md)); preserve existing documentation
instead of duplicating it.

## Output

The output of reconstruction is a [Director Brief](director-brief.md) plus any
proposed state files. The reconciliation above fills the brief's **Current
state**; end with one playable objective and the next evidence-producing
increment.
