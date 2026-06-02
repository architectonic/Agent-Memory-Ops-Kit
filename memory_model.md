# Memory Model

This file defines what belongs in project memory and what does not.

## Principle

Memory is context, not evidence.

A project should carry durable operating context, but current source files remain the highest authority.

## Good Memory

Store:

- stable project rules;
- durable architectural decisions;
- recurring bugs and their verified fixes;
- domain terminology;
- setup gotchas;
- testing commands;
- deployment constraints;
- handoffs from unfinished work.

## Bad Memory

Do not store:

- guesses;
- temporary plans;
- stale implementation details;
- emotional reactions;
- private user data;
- credentials;
- raw chat logs;
- conclusions that were never verified.

## Memory Classes

```text
Rule        - durable instruction for future agents.
Decision    - chosen direction with reason and consequence.
Fact        - statement backed by a recoverable source.
Assumption  - provisional claim that must be labeled.
Question    - known unknown that must not be filled by guessing.
Handoff     - compact transfer note for continuing work.
```

## Update Rule

Before writing memory:

1. classify the information;
2. check whether it is already captured;
3. remove temporary context;
4. cite or point to the source when possible;
5. write the smallest durable note.

## Staleness Rule

Memory should be revised or deleted when:

- source code contradicts it;
- requirements change;
- a decision is superseded;
- the note becomes too specific to a past task;
- the note can no longer be verified.
