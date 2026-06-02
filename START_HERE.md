# START HERE

Use this file as the first human/agent entrypoint after `AGENTS.md`.

## Read Order For Agents

1. `AGENTS.md`
2. `repo_contract.md`
3. `memory_model.md`
4. `decision_log.md`
5. `handoff_log.md`
6. `qa_gauntlet.md`
7. `security_review.md`
8. `tool_use_guardrails.md`
9. any relevant skill or runbook

## First 5 Minutes

Before writing code or changing files:

1. Identify the user's actual request.
2. Read the repo contract.
3. Check recent decisions and handoffs.
4. Identify affected files.
5. State what is known, inferred, and unknown.
6. Make the smallest coherent plan.

## When To Ask Before Acting

Ask before acting when:

- the target system is ambiguous;
- the change affects secrets, auth, billing, data deletion, production, or user data;
- the user request conflicts with repo rules;
- the agent would need to invent missing requirements;
- the change is broad, irreversible, or hard to test.

## When To Proceed

Proceed without extra process when:

- the task is local and reversible;
- the affected files are clear;
- the acceptance criteria are clear;
- the change does not touch sensitive boundaries;
- the verification method is known.

## Output Standard

At the end of work, report:

- what changed;
- where it changed;
- how it was verified;
- what remains unknown or risky.
