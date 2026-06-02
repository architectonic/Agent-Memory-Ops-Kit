# Tool Categories

Use this index to think about which kinds of tools belong in an agent memory workflow.

## Agent Interfaces

Examples:

- IDE agents;
- terminal coding agents;
- browser agents;
- chat-based agents;
- multi-agent runtimes.

Why it matters:

Agents need readable operating context regardless of interface.

## Memory And Retrieval

Examples:

- Markdown vaults;
- local search;
- vector databases;
- codebase indexing;
- knowledge graphs.

Why it matters:

Memory should help agents recover context without treating summaries as evidence.

## Source Control

Examples:

- Git;
- GitHub;
- pull requests;
- branch policies;
- commit logs.

Why it matters:

Repository state is a primary source of truth for code and documentation.

## Verification

Examples:

- tests;
- linters;
- type checks;
- deployment checks;
- manual QA scripts.

Why it matters:

Agent confidence is not proof. Verification closes the loop.

## Security Boundaries

Examples:

- secrets management;
- MCP server permissions;
- sandbox policies;
- production access rules.

Why it matters:

Agents can act quickly and destructively if boundaries are not explicit.

## Documentation Systems

Examples:

- README files;
- AGENTS files;
- ADRs;
- runbooks;
- handoff logs;
- project glossaries.

Why it matters:

Good documentation gives agents a stable operating map.
