# Reference Protocol Analysis

This document records what Exam Protocol learned from two private revision protocols and how those lessons were translated into public sanitized fixtures.

The original protocols covered two different course profiles:

- a calculation-heavy systems course;
- a terminology-heavy requirements course.

The originals are not stored in this public repository. They contained identifiable course metadata, lecturer-specific exam intelligence, source-file details, and material-derived wording. The fixtures preserve the design evidence without preserving that content.

## Classification model

Every protocol element is classified into one of five categories:

| Category | Meaning | Compiler treatment |
|---|---|---|
| **Stable kernel** | A cross-course rule required for reliable execution | Rendered from a shared base module |
| **Course variable** | A confirmed fact that differs by course or exam | Read from the Revision Manifest |
| **Strategy proposal** | A useful but inferential planning decision | Requires evidence and human approval |
| **Runtime state** | Mutable learner progress or session continuity data | Stored outside generated instructions |
| **Export-only rule** | Formatting or host-specific behavior | Added only by the selected export adapter |

This classification prevents a future compiler from confusing a good example with a universal default.

## Cross-case extraction matrix

| Protocol dimension | Systems fixture | Requirements fixture | Classification | Compiler implication |
|---|---|---|---|---|
| Mission | Reach exam readiness through concepts and repeatable calculation procedures | Produce terminology-precise, archetype-shaped answers | Course variable | Mission module receives assessment profile and answer style |
| Grounding | Search routed lecture/tutorial sources before teaching | Verify every taxonomy or claim and attach source tags | Stable kernel + course variable | Shared grounding module with configurable citation strictness |
| Terminology | Preserve technical terms and contrast confusable pairs | Preserve course labels and reject unsourced synonyms | Stable kernel | Shared terminology-fidelity rule |
| Exam contract | Mixed structured questions and calculations with mark allocation | Structured questions organized around recurring task forms | Course variable | Exam format, marks, duration, and answer policy live in manifest |
| Scope | Confirmed units, excluded units, and one unresolved calculation type | Confirmed archetypes plus lower-confidence recall coverage | Course variable | `confirmed`, `excluded`, and `uncertain` remain distinct |
| Evidence levels | Confirmed scope vs planning hypothesis | Strong/medium evidence behind archetype priorities | Stable kernel | Proposal schema requires evidence and confidence |
| Atomic revision unit | Concept or reusable calculation procedure | Question archetype | Course variable | Revision units need typed capability metadata |
| Priority | Tier-based allocation with strict time protection | Weighted archetype allocation | Strategy proposal | Priority representation must support labels and numeric ordering |
| Source routing | Topic and calculation type map to primary/supporting sources | Archetype maps to lecture, tutorial, and format reference | Stable kernel + course variable | Provider receives allowed source IDs, not the whole corpus |
| Teaching loop | Teach → Check → Drill → Produce → Grade | Orient → Teach → Worked example → You-do → Lock-in | Course variable assembled from stable phases | Runtime loop is ordered configuration, not hard-coded behavior |
| Completion | Closed-book explanation and timed unseen calculation | Consecutive clean drills including a harder variant | Course variable | Every revision unit requires observable exit criteria |
| Calculation behavior | Reusable numbered procedure, student attempts first, units and sanity checks | Mostly absent | Capability module | Calculation module is selected only when a unit requires it |
| Question archetypes | Secondary planning aid | Primary organizing model | Capability module | Archetype module must be optional, not assumed for every exam |
| Trap registry | Confusable concepts and unit-conversion errors | Sibling taxonomies, wording traps, and format traps | Stable structure + course data | Trap entries are data with evidence, not prose embedded in templates |
| Strict grading | Steps, working, units, and mark coverage | Expected terminology, structure, evidence, and exact fix | Stable kernel + rubric variable | Shared grading contract accepts rubric dimensions |
| Artifact rules | Concept guides and procedure cards | Guides, drills, MCQs, and mock formats | Export-only rule | Artifact specifications belong in output modules |
| Commands | Session and drill operations | Named commands for day, guide, drill, grade, and status | Export-only rule | Command vocabulary is host/export configuration |
| Progress | Status per revision unit and calculation errors | Status per archetype and terminology errors | Runtime state | Progress schema references unit IDs and recurring errors |
| Handover | Explicit next session, unfinished topics, and calculation weaknesses | Tracker copied into the next conversation | Stable kernel + runtime state | Generated protocol requires handover; values stay in state file |
| Quality gate | Source verification, units, exclusions, and exit criteria | Source tags, terminology, trap count, formats, and no invention | Stable kernel + capability checks | Compiler emits a composed checklist from selected modules |

## Stable kernel recovered from both cases

The first base template should contain only rules supported by both references:

1. Define a mission against a confirmed exam contract.
2. Search or verify approved sources before teaching factual course content.
3. Preserve course terminology and identify confusable terms.
4. Separate confirmed facts, inferred strategy, and unknowns.
5. Route each revision unit to explicit evidence sources.
6. Teach before testing when the learner profile says `teach_first`.
7. Require the learner to produce an answer before revealing a solution.
8. Grade against marks, terminology, structure, or procedures defined by the unit.
9. Use observable exit criteria before marking a unit ready.
10. Update progress, error history, and handover after each session.
11. Respect confirmed exclusions and protect scarce study time.
12. Run a composed quality gate before generating study artifacts.

Anything more specific should be a variable, capability module, or export rule.

## Sanitization record

### Removed

- real institution and module identifiers;
- real academic dates and assessment thresholds;
- professor statements and audio-derived hints;
- real source filenames and internal storage instructions;
- exact course definitions, taxonomies, examples, and answer-key phrases;
- recognizable past-paper structures tied to one lecturer;
- the learner's genuine mistakes and schedule.

### Preserved

- rule precedence and grounding behavior;
- exam-contract structure;
- evidence/confidence separation;
- source routing and retrieval boundaries;
- typed revision units and priority models;
- session protocols and exit criteria;
- calculation and archetype capability differences;
- grading dimensions, tracker semantics, and handover;
- trap registry and quality-gate structure.

### Replaced with synthetic data

- course names and source IDs;
- exam values and planning assumptions;
- numerical calculation inputs;
- question examples and error entries;
- terminology tokens used to demonstrate fidelity rules.

## Reconstruction contract

A future compiler passes the reference milestone when it can consume both fixtures and produce outputs that satisfy the following invariants without fixture-specific code paths.

### Shared invariants

- A mission and exam contract are present.
- Grounding, terminology, unsupported-claim, and exclusion rules are present.
- Every revision unit has a priority, source route, and exit criteria.
- The runtime loop preserves the configured order.
- Grading responds to mark allocation and the unit's rubric dimensions.
- Progress and handover refer to stable revision-unit IDs.
- The output contains a composed quality gate.

### Systems-specific invariants

- Calculation units require attempt-before-reveal.
- Procedures include numbered steps, units, and sanity checks.
- Session completion depends on an unseen timed calculation.
- Calculation errors have a distinct place in progress state.

### Requirements-specific invariants

- Revision is organized around question archetypes rather than chapters alone.
- Evidence-bearing source tags are required in generated artifacts.
- Standard and advanced drill levels remain distinct.
- The trap registry and artifact quality gate are first-class sections.

## Testing strategy

The fixture suite should eventually contain four layers:

1. **Schema tests** — valid fixtures pass; missing evidence, exit criteria, or IDs fail.
2. **Compiler tests** — deterministic inputs produce stable module selection and ordering.
3. **Semantic snapshot tests** — required sections and invariants match expected outputs.
4. **Privacy tests** — public outputs reject deny-listed private identifiers and source paths.

The expected `CLAUDE.md` files are human-authored targets for R0. They are not proof that `CLAUDE.md` will remain the only or preferred export format.

## Limits of the current fixtures

- The fixture YAML is versioned as `fixture_version: 0`; it is design input, not a promised public schema.
- No course documents are included, so retrieval behavior cannot yet be evaluated end to end.
- No compiler exists, so expected outputs are normative examples rather than generated artifacts.
- Sanitization deliberately reduces content realism to protect the original sources.

These limits are acceptable for the first milestone: preserve the protocol architecture well enough to design the schema and test the compiler later.
