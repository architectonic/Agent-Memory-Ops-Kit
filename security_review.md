# Security Review

Use this file before merging or shipping agent-made changes.

## Secret Safety

- [ ] No API keys, tokens, passwords, private keys, or session cookies were committed.
- [ ] `.env` and local secret files are ignored.
- [ ] Examples use placeholders, not real values.

## Data Safety

- [ ] No private user data was added.
- [ ] No client-sensitive or proprietary context was added.
- [ ] Logs, screenshots, and fixtures are sanitized.

## Access Control

- [ ] Authentication behavior was not changed accidentally.
- [ ] Authorization checks were preserved.
- [ ] Admin-only operations remain protected.
- [ ] Public routes do not expose private data.

## Dependency Safety

- [ ] New dependencies are necessary.
- [ ] Package names are verified.
- [ ] Install scripts or binaries are treated cautiously.
- [ ] License impact is understood for production use.

## Destructive Operations

Ask before changing anything involving:

- deletion;
- migrations;
- production data;
- billing;
- deployment secrets;
- auth configuration;
- security policies.

## Security Note Template

```text
Sensitive area touched:
Risk:
Mitigation:
Verification:
```
