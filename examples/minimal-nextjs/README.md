# Minimal Next.js Example

This example shows how a small app could adapt the kit.

## Suggested Files

```text
AGENTS.md
START_HERE.md
repo_contract.md
memory_model.md
decision_log.md
handoff_log.md
qa_gauntlet.md
security_review.md
tool_use_guardrails.md
```

## Example Repo Contract Values

```text
Project name: Example Web App
Project type: Next.js web application
Primary users: Placeholder users
Primary runtime: Node.js
Primary language/framework: TypeScript / Next.js
Deployment target: Placeholder hosting platform
```

## Example Agent Boundaries

Agent may change:

- page components;
- route handlers tied to the requested task;
- tests;
- documentation.

Agent must ask before changing:

- auth;
- billing;
- database migrations;
- production deployment config;
- environment variable names.
