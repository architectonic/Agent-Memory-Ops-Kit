# Safe Repo Update Runbook

Use this runbook before mutating a repository through an external tool or API.

## Skills Used

- `skills/external-system-mutation.md`
- `skills/repo-discovery.md`
- `skills/handoff-writing.md`

## Procedure

1. Verify the repository owner/name.
2. Verify the branch.
3. Read the current files to be changed.
4. Decide whether the change should be a direct commit or pull request.
5. Apply the smallest coherent change.
6. Read back changed files.
7. Compare intended and actual state.
8. Record verification in the final response or handoff.

## Never

- Do not assume the UI-selected repo is correct.
- Do not overwrite files without reading current content.
- Do not batch unrelated changes.
- Do not force-update branches without explicit instruction.
