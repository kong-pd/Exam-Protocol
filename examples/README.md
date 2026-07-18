# Sanitized Reference Fixtures

This directory preserves the structural evidence behind Exam Protocol without publishing the private course packages from which the product idea emerged.

The two fixtures intentionally represent different revision demands:

| Fixture | Distinctive pressure | Structures preserved |
|---|---|---|
| [Operating Systems](./operating-systems/) | Calculation-heavy, procedure-driven assessment | Calculation procedures, source routing, session exit criteria, priority tiers, and handover state |
| [Requirements Engineering](./requirements-engineering/) | Terminology-heavy, archetype-driven assessment | Question archetypes, source tags, trap registry, strict grading, commands, and artifact quality gates |

## What a fixture contains

Each case currently contains:

```text
<fixture>/
├── README.md
├── revision.yaml
├── source-routes.yaml
├── progress.yaml
└── expected/
    └── CLAUDE.md
```

- `revision.yaml` is a fixture-level representation of confirmed facts, approved strategy, and runtime rules. It is **not yet the official schema**.
- `source-routes.yaml` demonstrates how revision units restrict retrieval to synthetic source IDs.
- `progress.yaml` demonstrates state that survives outside a conversation.
- `expected/CLAUDE.md` is the human-readable target that a future compiler should reproduce from the fixture inputs.

## Sanitization boundary

These fixtures preserve protocol mechanics while removing or replacing:

- institution names and real course codes;
- dates, grade thresholds, and personal scheduling details;
- lecturer identity and lecturer-specific intelligence;
- real lecture, tutorial, marking-scheme, and past-paper filenames;
- direct slide wording and answer-key-derived phrases;
- real questions, numerical examples, and student error history.

All source IDs, evidence statements, sample questions, learner state, and numerical values in this directory are synthetic. They must not be interpreted as claims about a real course or exam.

The private originals are not required at runtime and must never become package dependencies. Their role is limited to validating that the public fixtures retain the important structural distinctions.

## How these fixtures should be used

Before a compiler exists, the fixtures are design records. Once a compiler exists, they should become executable regression cases:

1. Validate `revision.yaml`, `source-routes.yaml`, and `progress.yaml`.
2. Compile the case into a temporary output directory.
3. Compare required sections and semantic invariants with `expected/CLAUDE.md`.
4. Confirm that no fixture-specific branch exists in compiler code.
5. Run a deny-list scan to prevent private identifiers from entering public outputs.

Exact byte-for-byte snapshots may be useful for deterministic templates, but semantic assertions should remain primary so harmless formatting changes do not hide structural regressions.

See [Reference Analysis](../docs/reference-analysis.md) for the cross-case extraction matrix and future compiler contract.
