# Operating Systems Fixture

This sanitized fixture represents a **calculation-heavy systems exam**. It preserves the structural lessons of the private reference protocol without publishing its institution, course code, lecturer intelligence, source filenames, definitions, or real examination content.

All facts and sources in this directory are synthetic.

## Why this case exists

This case forces the future compiler to support concerns that a generic tutoring prompt often misses:

- revision units that are reusable procedures rather than concepts alone;
- attempt-before-reveal for calculations;
- units, intermediate working, and sanity checks;
- source routes that differ by topic and procedure type;
- strict exclusions that protect limited study time;
- session exit criteria based on unseen timed problems;
- calculation-specific error tracking;
- explicit cross-conversation handover.

## Fixture files

| File | Role |
|---|---|
| [`revision.yaml`](./revision.yaml) | Synthetic exam contract, units, priorities, rules, and runtime loop |
| [`source-routes.yaml`](./source-routes.yaml) | Synthetic source catalog and per-unit retrieval routes |
| [`progress.yaml`](./progress.yaml) | Empty learner state demonstrating durable progress and error fields |
| [`expected/CLAUDE.md`](./expected/CLAUDE.md) | Human-authored target output for a future compiler |

## Structural invariants

A compiler output for this fixture must:

1. Preserve the configured exam contract and excluded unit.
2. Search only the allowed sources for each revision unit.
3. Require a learner attempt before revealing calculation solutions.
4. Render numbered calculation procedures with units and sanity checks.
5. Keep the loop `teach → recall_check → drill → produce → grade` in order.
6. Require observable exit criteria before setting a unit to `exam_ready`.
7. Track calculation errors separately from terminology errors.
8. Produce an end-of-session handover with the next unit and unfinished work.

## Deliberate differences from the Requirements Engineering fixture

- Topics and calculation procedures are the primary revision units.
- Priority is driven by procedural importance and synthetic exam evidence.
- Grading emphasizes working, units, and a defensible final result.
- Procedure cards are more important than question-archetype drill formats.

These differences must be expressed through data and capability modules—not an `if operating-systems` branch in compiler code.

## Not included

- real lecture or tutorial files;
- real slide definitions;
- real lecturer statements;
- real exam questions or numerical examples;
- real learner progress.

This is a design fixture, not revision material for an actual Operating Systems course.
