# Requirements Engineering Fixture

This sanitized fixture represents a **terminology-heavy, question-archetype-driven exam**. It preserves the structural lessons of the private reference protocol without publishing its institution, course code, lecturer intelligence, source filenames, definitions, taxonomies, or real assessment content.

All facts and sources in this directory are synthetic.

## Why this case exists

This case forces the future compiler to support concerns that differ from a calculation-heavy protocol:

- question archetypes as the primary revision units;
- evidence-weighted priorities;
- source tags attached to factual claims and artifacts;
- exact course terminology with no unsourced synonym substitution;
- standard and advanced drill levels;
- a trap registry built from confusable categories and formats;
- strict grading by expected term, structure, and exact fix;
- artifact-specific quality gates;
- tracker continuity across conversations.

## Fixture files

| File | Role |
|---|---|
| [`revision.yaml`](./revision.yaml) | Synthetic exam contract, archetypes, evidence, rules, and runtime loop |
| [`source-routes.yaml`](./source-routes.yaml) | Synthetic source catalog and per-archetype retrieval routes |
| [`progress.yaml`](./progress.yaml) | Empty learner state demonstrating archetype readiness and error history |
| [`expected/CLAUDE.md`](./expected/CLAUDE.md) | Human-authored target output for a future compiler |

## Structural invariants

A compiler output for this fixture must:

1. Organize revision by archetype rather than chapter alone.
2. Preserve evidence-backed priority weights without turning proposals into facts.
3. Require source tags for factual definitions, lists, and artifact claims.
4. Keep the loop `orient → teach → worked_example → you_do → lock_in` in order.
5. Generate standard and advanced drills with distinct expectations.
6. Grade using expected terminology, required structure, marks, and an exact correction.
7. Render a trap registry and artifact quality gate.
8. Persist status and recurring terminology or classification errors by archetype ID.

## Deliberate differences from the Operating Systems fixture

- Archetypes, not procedures, are the primary revision units.
- Priority is represented by evidence weight and expected assessment value.
- Grading emphasizes terminology, classification, rationale, and response format.
- Trap-aware guides and drills are more important than calculation procedure cards.

These differences must be expressed through data and capability modules—not an `if requirements-engineering` branch in compiler code.

## Not included

- real lecture or tutorial files;
- real course definitions or category lists;
- real lecturer statements;
- real revision-paper questions or answer-key language;
- real learner progress.

This is a design fixture, not revision material for an actual Requirements Engineering course.
