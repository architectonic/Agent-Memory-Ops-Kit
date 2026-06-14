# Ontology

This file defines the core entities used by Agent Memory Ops Kit.

The purpose is to give humans and agents a shared world model for agentic software work.

## Principle

Agents need more than memory.

They need a stable model of what exists, how entities relate, which sources have authority, and which claims are safe to act on.

Ontology shapes memory.

Memory without ontology becomes a pile of notes.

## Core Entities

```text
Human
Agent
Repository
Task
Plan
Action
Artifact
Source
Claim
Fact
Assumption
Decision
Rule
Question
Risk
Verification
Memory
Handoff
Boundary
Authority
```

## Human

A person responsible for intent, judgment, approval, and accountability.

Humans define goals, clarify ambiguity, approve sensitive changes, and own final responsibility.

## Agent

A model-driven worker operating inside a bounded context.

An agent may inspect, plan, edit, test, summarize, and hand off work.

An agent should not treat its own memory or prior output as proof.

## Repository

The working system under change.

A repository may contain source code, tests, docs, configs, scripts, memory files, and project contracts.

The current repository is usually the strongest source of truth for current implementation state.

## Task

A bounded unit of work requested by a human or assigned by a system.

A task should have a target, scope, expected outcome, and verification method.

## Plan

A proposed sequence of actions for completing a task.

A plan is provisional until executed and verified.

Plans should be small, coherent, and sensitive to risk.

## Action

A concrete operation performed by an agent or human.

Actions include reading files, editing files, running tests, creating commits, opening issues, changing settings, or mutating external systems.

Actions that mutate external state require explicit target identification.

## Artifact

A produced or modified object.

Artifacts include code files, docs, tests, reports, logs, design files, prompts, configs, generated outputs, and handoffs.

Artifacts should not be assumed canonical unless authority has been established.

## Source

A recoverable origin for a claim.

Sources include current files, tests, logs, CI output, issues, PRs, decisions, external docs, user instructions, and runtime observations.

A claim with a recoverable source is stronger than an unsourced claim.

## Claim

A statement about the project, task, system, or environment.

Claims must be classified before they are stored as memory.

Common claim classes:

```text
Fact
Assumption
Decision
Rule
Question
Risk
```

## Fact

A claim backed by a recoverable source.

Facts can become stale when the source changes.

A fact is not permanent truth. It is source-backed current belief.

## Assumption

A provisional claim that has not been verified.

Assumptions must remain labeled and should not guide sensitive actions without verification.

## Decision

A chosen direction with context, reason, and consequence.

Decisions should be recorded when future agents are likely to encounter plausible alternatives.

Accepted decisions should not be accidentally undone.

## Rule

A durable instruction for future work.

Rules should be rare, explicit, and justified by durable project needs.

Rules are stronger than preferences but weaker than current source evidence and current user instruction.

## Question

A known unknown.

Questions prevent agents from silently filling gaps with guesses.

Unanswered questions should remain visible until answered, rejected, or made irrelevant.

## Risk

A potential failure, harm, uncertainty, or sensitive boundary.

Risks should be named before action when work touches security, data, production, billing, legal, or irreversible changes.

## Verification

Evidence that work behaves as intended or that a claim is supported.

Verification includes tests, typechecks, builds, runtime checks, source review, logs, and human review.

If verification cannot be performed, the limitation must be stated.

## Memory

Durable operating context stored for future agents and humans.

Memory should be typed, scoped, sourced when possible, maintained, and pruned.

Memory is context, not evidence.

## Handoff

A compact transfer note for continuing work across sessions, agents, or humans.

Handoffs should describe current state, completed work, changed files, verification, open questions, risks, and next step.

Handoffs guide continuation but do not prove current state.

## Boundary

A constraint on what an agent may do without escalation.

Boundaries include permissions, security limits, public/private context separation, destructive-action limits, and sensitive-system limits.

## Authority

The relative strength of a source or claim when deciding what to trust.

Authority is defined in `authority.md`.

When sources conflict, agents should rank them explicitly rather than blending them into a compromise.

## Relationships

```text
Human assigns Task.
Agent performs Action.
Action modifies or produces Artifact.
Artifact may contain Source.
Source supports Claim.
Claim is classified as Fact, Assumption, Decision, Rule, Question, or Risk.
Verification strengthens or rejects Claim.
Memory preserves selected durable Claims.
Handoff transfers Task state.
Boundary constrains Action.
Authority ranks Sources and Claims.
```

## Operating Implication

Before an agent writes durable memory, it should ask:

```text
What entity is this about?
What claim is being made?
What source supports it?
What authority does the source have?
What lifecycle state should this claim occupy?
Who will need this later?
```

If those questions cannot be answered, the note probably belongs in scratch context, not durable memory.
