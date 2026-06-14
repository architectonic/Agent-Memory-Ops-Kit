# Authority Model

This file defines how an agent should rank sources when working in a repository.

Memory is useful only when the agent knows how much authority each source has.

## Principle

Memory is context, not evidence.

Use memory to decide what to inspect first.

Do not use memory to avoid inspecting stronger sources.

## Authority Hierarchy

When sources conflict, use this order:

```text
1. Current user instruction
2. Current repository source files
3. Tests, typechecks, build output, CI, and runtime evidence
4. Repo-local AGENTS.md
5. Repo contract
6. Accepted decision records
7. Current handoff
8. Memory facts with recoverable sources
9. Assumptions explicitly labeled as assumptions
10. Agent inference
11. Model prior knowledge
```

The hierarchy does not remove judgment. It prevents weaker sources from silently overruling stronger ones.

## Conflict Rule

When two sources disagree:

1. identify both sources;
2. rank them by authority;
3. inspect the strongest available source;
4. state the conflict if it affects the task;
5. update, demote, or delete stale memory when appropriate.

Do not average conflicting sources into a compromise claim.

## Source Classes

### Current User Instruction

The current user instruction defines the task and may override previous plans.

It does not automatically rewrite durable project decisions unless the user explicitly asks for that.

### Source Files

Current source files are the strongest evidence for how the system currently behaves.

Read source files before changing them.

When source files contradict memory, trust the source files and update the memory.

### Tests And Runtime Evidence

Passing tests, failing tests, logs, build output, and runtime behavior are evidence.

They can reveal that both source comments and memory are stale.

### AGENTS.md

`AGENTS.md` defines repository-local agent behavior.

It should be read before substantial work.

### Repo Contract

`repo_contract.md` defines project identity, source-of-truth locations, agent permissions, definition of done, and non-goals.

### Decision Records

Accepted decisions should not be accidentally undone.

A decision record may be superseded, but the agent should make that status explicit.

### Handoffs

Handoffs are useful for continuation.

They are not proof of current state.

A handoff should guide inspection, not replace it.

### Memory Facts

A memory fact should be backed by a recoverable source when possible.

Unsourced facts are weaker than sourced facts.

### Assumptions

Assumptions are provisional.

They must remain labeled until verified, rejected, or deleted.

### Inference

Inference is allowed, but it must be named as inference when it affects decisions.

### Model Prior Knowledge

Model prior knowledge is the weakest source.

It may help generate hypotheses, but it must not override repository evidence.

## Private Context Rule

Private memory, personal context, raw transcripts, hidden system state, or external private repositories must not be treated as publishable source material.

When copying this kit into a public repo, keep private context outside the public repository.

## Action Rule

Before making a sensitive change, the agent should identify the highest-authority source that permits the change.

Sensitive changes include:

- authentication;
- authorization;
- billing;
- payments;
- secrets;
- production deployment;
- data deletion;
- public API contracts;
- legal or compliance text.

If no sufficient authority exists, ask before acting.
