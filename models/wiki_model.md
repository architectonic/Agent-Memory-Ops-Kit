# Wiki Model

Use this model to create a project-local wiki for agents.

A wiki is the curated durable memory of a project. It should help agents understand the system without replacing source review.

## Template

```text
wiki/
  overview.md
  ontology.md
  decisions.md
  handoffs.md
  sources.md
  setup.md
  qa.md
  security.md
  gotchas.md
```

## Page Rules

Each page should answer:

- when should an agent read this?
- what mistake does this prevent?
- what source supports this?
- what is still unknown?
- when should this be reviewed?

## Knowledge Classes

```text
Fact        - source-backed statement.
Decision    - selected direction with reason and consequence.
Assumption  - provisional claim to revisit.
Question    - known unknown.
Rule        - durable operating instruction.
Handoff     - compact continuation note.
```

## Maintenance Rules

- Keep pages short.
- Prefer source links over copied material.
- Label assumptions.
- Delete stale notes.
- Do not promote raw conversation into canonical knowledge.
- Do not put private context in public template repos.
