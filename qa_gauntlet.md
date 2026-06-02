# QA Gauntlet

Use this checklist before declaring work complete.

## Scope Check

- [ ] The named problem is understood.
- [ ] The affected files are known.
- [ ] The change is no broader than necessary.
- [ ] Non-goals were respected.

## Correctness Check

- [ ] The implementation matches the requested behavior.
- [ ] Edge cases were considered.
- [ ] Errors are handled intentionally.
- [ ] No unrelated behavior was changed.

## Test Check

Record what was run:

```text
Command:
Result:
Notes:
```

When tests cannot run, record why:

```text
Reason:
Risk:
Manual verification:
```

## Review Check

- [ ] No secrets or private data were added.
- [ ] No dead code or placeholder logic was left behind.
- [ ] No speculative abstractions were added.
- [ ] The final response names changed files and verification.

## Completion Statement

```text
Changed:
Verified:
Known risks:
Next step:
```
