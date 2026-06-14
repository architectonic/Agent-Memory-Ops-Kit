# Memory Lifecycle

Memory should have a lifecycle.

Without promotion, demotion, and deletion, memory becomes a landfill.

## Principle

Not every observation deserves to become durable memory.

Most task-local context should disappear after the task is complete.

## Lifecycle States

```text
Observation
→ Assumption
→ Verified Fact
→ Decision
→ Rule
→ Superseded
→ Deprecated
→ Deleted
```

## Observation

A raw observation.

Example:

```text
The login request returned 401.
```

Observations are useful but should not automatically become memory.

## Assumption

A provisional explanation.

Example:

```text
The session cookie may not be sent.
```

Assumptions must remain labeled.

Do not store assumptions as facts.

## Verified Fact

A statement supported by a recoverable source.

Example:

```text
The backend uses signed session cookies.
Source: auth/session.ts
```

Facts should reference a source whenever possible.

## Decision

A chosen direction with reason and consequence.

Example:

```text
Authentication will use session cookies instead of localStorage tokens.
```

Decisions should be recorded in the decision log.

## Rule

A durable instruction for future agents.

Rules should be rare.

A rule usually emerges from repeated facts and decisions.

## Superseded

The item was once valid but has been replaced.

Do not silently delete historically useful decisions.

Mark them as superseded when they provide useful context.

## Deprecated

The item should no longer guide future work.

Keep only when historical traceability matters.

## Deleted

Remove memory that:

- cannot be verified;
- duplicates stronger sources;
- describes temporary plans;
- contains stale implementation details;
- records completed task noise;
- no longer serves a reader.

## Promotion Rules

Promote only when:

- the information survived verification;
- future agents are likely to need it;
- it reduces repeated confusion;
- it has durable value beyond the current task.

## Demotion Rules

Demote when:

- a source weakens;
- evidence disappears;
- a stronger source contradicts it;
- requirements change.

## Deletion Bias

When uncertain between keeping and deleting task-local context, prefer deletion.

The goal is operational clarity, not archival completeness.
