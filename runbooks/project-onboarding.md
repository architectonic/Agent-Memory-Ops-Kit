# Project Onboarding Runbook

Use this runbook when adding the kit to an existing repository.

## Procedure

1. Read the repository README and top-level docs.
2. Identify package manifests, build scripts, test scripts, and deployment config.
3. Fill in `repo_contract.md`.
4. Add known decisions to `decision_log.md` only when supported by source or human confirmation.
5. Add current work state to `handoff_log.md` only when useful.
6. Customize `qa_gauntlet.md` with actual project commands.
7. Customize `security_review.md` for the project risk profile.
8. Remove files that do not apply.

## Output

The onboarded repo should answer:

- what the project is;
- how to run it;
- how to test it;
- what the agent may change;
- what the agent must not touch without permission;
- where decisions and handoffs live.

## Avoid

- Filling unknowns with guesses.
- Copying every template without pruning.
- Adding private notes to public repos.
- Treating this kit as a substitute for reading the actual code.
