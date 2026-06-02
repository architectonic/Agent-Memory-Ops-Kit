# Docs Index

A lightweight index of documentation sources worth consulting when adapting this kit.

This file intentionally avoids becoming a link dump. Add links only when they are stable, official, and useful.

## Agent Instruction Files

Useful source types:

- official docs for agent instruction files;
- repository examples from public open-source projects;
- IDE-specific rule file docs.

Review note:

These conventions change. Re-check before publishing claims about current support.

## MCP

Useful source types:

- official Model Context Protocol docs;
- official SDK docs;
- security guidance for tool permissions.

Review note:

MCP servers may expose local files, secrets, and write actions. Treat docs as security-sensitive.

## Coding Agents

Useful source types:

- official docs for Codex, Cursor, Claude Code, OpenHands, and other coding agents;
- public examples of `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and equivalent files.

Review note:

Do not assume one tool reads another tool's instruction format.

## Source Control

Useful source types:

- Git documentation;
- GitHub pull request, branch protection, and Actions docs.

Review note:

Prefer official docs for behavior that affects repository mutation.

## Security

Useful source types:

- secrets-management docs;
- OWASP guidance;
- supply-chain security docs;
- package-manager security docs.

Review note:

Security guidance becomes stale. Mark review dates when adding specific claims.
