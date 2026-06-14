# Memory Reconciliation

Use this runbook after major work.

The purpose is to prevent future agents from repeating the same confusion.

## Principle

Code changes and memory changes should be reconciled together.

A task is not fully complete if durable knowledge changed but memory did not.

## Reconciliation Questions

Ask:

```text
What became true?
How do we know?
Who decided?
What should be remembered?
What should be forgotten?
What became obsolete?
```

## Review Checklist

### Facts

- Did we learn any source-backed facts?
- Should they be added to memory?
- Can they be sourced?

### Decisions

- Was a new direction chosen?
- Should it be recorded in decision_log.md?
- Did an older decision become superseded?

### Rules

- Did repeated failures reveal a durable rule?
- Is the rule broad enough to justify future enforcement?

### Handoffs

- Is unfinished work remaining?
- Can the next agent continue without guessing?

### Assumptions

- Which assumptions were verified?
- Which assumptions were rejected?
- Which assumptions remain open?

### Deletions

- Which notes became stale?
- Which notes duplicate stronger sources?
- Which notes describe completed task noise?

## Minimal Memory Diff

A useful end-of-task summary may look like:

```text
Facts added:
Decisions added:
Rules added:
Handoffs added:
Assumptions resolved:
Memory items removed:
```

## Failure Mode

A common agent failure is:

```text
same bug
same confusion
same investigation
same fix
```

Memory reconciliation exists to break that cycle.

## Completion Check

Before closing a task, ask:

```text
Will the next agent avoid repeating this work?
```

If the answer is no, memory reconciliation is incomplete.
