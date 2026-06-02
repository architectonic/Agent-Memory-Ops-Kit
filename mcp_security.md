# MCP Security

Model Context Protocol servers can expose powerful local or remote capabilities to agents. Treat every MCP tool as an execution boundary.

## Before Adding An MCP Server

Record:

```text
Server name:
Source:
Transport:
Permissions requested:
Data exposed:
Write capabilities:
Authentication method:
```

## Review Questions

- What files, APIs, accounts, or services can this server access?
- Can it mutate external systems?
- Can it read secrets or private local files?
- Is the package/source trusted?
- Is the server pinned to a version?
- Is the server scoped to one project or global?
- Are logs safe to share?

## Rules

- Prefer least privilege.
- Prefer project-scoped config over global config.
- Do not expose broad filesystem roots unless necessary.
- Do not pass secrets through prompts.
- Do not install untrusted MCP servers into a sensitive workspace.
- Document every server that can mutate state.

## MCP Server Inventory Template

```md
## Server Name

Purpose:
Source:
Transport:
Read access:
Write access:
Secrets required:
Risk level: low | medium | high
Review date:
Notes:
```
