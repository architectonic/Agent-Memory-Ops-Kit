# Agent Session Runbook

Use this runbook for a normal coding-agent work session.

## Procedure

1. Read `AGENTS.md` and `START_HERE.md`.
2. Read `repo_contract.md`.
3. Check `decision_log.md` and `handoff_log.md`.
4. Discover affected files.
5. State known facts, assumptions, and unknowns.
6. Make the smallest coherent plan.
7. Apply changes.
8. Run available verification.
9. Update handoff or decision logs when useful.
10. Report changed files, verification, risks, and next step.

## Stop Conditions

Stop and ask before continuing when:

- target repo/account is ambiguous;
- secrets or production data may be affected;
- requirements conflict;
- verification cannot be performed and risk is high;
- the requested change expands beyond the original task.
