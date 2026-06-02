# Repo Contract

This file defines what an agent should assume about the repository it is working in.

Replace the placeholders when copying this kit into a real project.

## Project Identity

```text
Project name:
Project type:
Primary users:
Primary runtime:
Primary language/framework:
Deployment target:
```

## Source Of Truth

```text
Product requirements:
Architecture decisions:
Issue tracker:
Design system:
API contract:
Database schema:
Deployment config:
```

## Agent Permissions

The agent may change:

```text
- documentation files;
- tests related to the requested task;
- implementation files directly required by the task;
- examples and templates when explicitly requested.
```

The agent must ask before changing:

```text
- authentication or authorization;
- billing or payments;
- database migrations;
- production deployment config;
- secrets or environment variable names;
- public API contracts;
- destructive scripts;
- legal, compliance, or licensing text.
```

## Definition Of Done

A task is complete when:

1. the named problem is addressed;
2. relevant tests or checks were run, or the reason they could not run is stated;
3. changed files are listed;
4. risks and unknowns are stated;
5. no private data or secrets were added.

## Non-Goals

Record what the project is not trying to do.

```text
- Non-goal 1:
- Non-goal 2:
- Non-goal 3:
```
