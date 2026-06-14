# Memory Ops Doctrine

Agent memory is not chat history.

Agent memory is not RAG.

Agent memory is not a prompt library.

Agent memory is an operational control surface for preserving project continuity, decision integrity, safety boundaries, and epistemic hygiene across sessions, agents, and humans.

## Core Thesis

Long-running agent work does not fail only because models lack intelligence or tools.

It also fails because memory degrades.

Agents repeat old mistakes, trust stale notes, confuse assumptions with facts, overwrite decisions, forget safety boundaries, and treat prior context as proof.

Memory Ops is the discipline of preventing that degradation.

## Operating Claim

A repository that uses agents should carry its own governed operating memory.

That memory must be:

- typed;
- scoped;
- sourced when possible;
- ranked by authority;
- maintained over time;
- pruned when stale;
- separated from private context;
- treated as context, not evidence.

## What Memory Ops Is

Memory Ops is the practice of managing the information agents use to continue work safely and coherently.

It includes:

- project contracts;
- source-of-truth maps;
- authority hierarchy;
- memory classes;
- decision records;
- handoffs;
- open questions;
- known failures;
- safety boundaries;
- verification rituals;
- pruning cycles.

## What Memory Ops Is Not

Memory Ops is not:

- storing every conversation;
- summarizing every chat;
- dumping documents into a vector database;
- trusting model memory;
- replacing source review;
- replacing tests;
- inventing process for its own sake.

The goal is not more memory.

The goal is better-governed memory.

## The Four Questions

Before an agent acts, operational memory should help answer:

```text
What is true?
How do we know?
Who decided?
What must not be forgotten?
```

If the memory system cannot answer these questions, it is only a note pile.

## The Failure Pattern

Ungoverned agent memory commonly fails through:

- stale context;
- unsourced claims;
- duplicated decisions;
- hidden assumptions;
- private context leakage;
- overfitted session notes;
- obsolete implementation details;
- vague handoffs;
- forgotten verification steps;
- confidence without evidence.

Memory Ops exists to reduce those failures.

## The Minimum Viable Memory System

A useful agent memory system needs only a few durable files:

```text
AGENTS.md
START_HERE.md
repo_contract.md
authority.md
memory_model.md
decision_log.md
handoff_log.md
qa_gauntlet.md
security_review.md
tool_use_guardrails.md
```

Keep it boring.

Plain Markdown is enough at first because it is inspectable, diffable, portable, reviewable, and easy for humans and agents to edit.

Automation can come later.

## Source Discipline

Memory must never outrank stronger evidence.

When a memory entry conflicts with current source code, tests, deployment state, or an accepted decision record, the memory entry must be revised, demoted, or deleted.

Never use memory to avoid reading the source.

Use memory to know what to inspect first.

## Lifecycle Discipline

Memory should move through explicit states:

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

Not every observation deserves promotion.

Most task-local context should die with the task.

## Scope Discipline

Do not collapse memory scopes.

Keep separate:

```text
public reusable patterns
private user preferences
project-specific rules
task-local scratch context
source-derived facts
agent inferences
```

Mixing these scopes creates privacy risk, bad assumptions, and false authority.

## Completion Standard

Agentic work is not complete merely because code changed.

A task is complete when:

1. the requested change is addressed;
2. relevant checks were run or explicitly skipped with reason;
3. risks and unknowns are stated;
4. no private context or secrets were introduced;
5. durable decisions, handoffs, or memory updates were reconciled;
6. stale memory discovered during the work was corrected or marked for pruning.

The final question is:

```text
Will the next agent avoid repeating the same confusion?
```

If not, the memory work is not done.
