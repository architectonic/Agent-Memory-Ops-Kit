# Stack Patterns

Common ways to use Agent Memory Ops Kit with different development stacks.

## Small Solo Repo

Use:

- `AGENTS.md`
- `START_HERE.md`
- `repo_contract.md`
- `decision_log.md`
- `handoff_log.md`
- `qa_gauntlet.md`

Avoid:

- heavy process;
- multiple role files;
- large knowledge graphs.

## Team Repo

Use:

- decision log;
- pull request templates;
- QA gauntlet;
- security review;
- onboarding runbook;
- tool-use guardrails.

Add:

- ownership boundaries;
- review rules;
- branch policies;
- release checklist.

## Agent-Heavy Repo

Use:

- skill files;
- runbooks;
- handoff logs;
- memory model;
- MCP security;
- external-system mutation skill.

Add:

- agent roles only when they map to real workflows;
- explicit permissions per tool;
- periodic maintenance cycle.

## Public Template Repo

Use:

- generic examples;
- placeholders;
- public-safe docs;
- no private memory.

Avoid:

- client names;
- private source indexes;
- real secrets;
- raw transcripts;
- personal operating doctrine.
