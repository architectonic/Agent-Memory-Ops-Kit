# Agent Memory Ops Kit

Give your AI coding agent a working memory before it touches your repo.

Agent Memory Ops Kit is a public, plain-Markdown starter vault for humans supervising AI coding agents. It gives agents a small set of files to read before acting: project rules, memory boundaries, decision records, handoff templates, QA checks, security checks, tool-use guardrails, reusable cognitive models, and maintenance cycles.

It is not a SaaS, runtime, database, RAG stack, prompt dump, or long wiki. It is an operational filesystem for agentic development.

## Who It Is For

- Developers using Codex, Cursor, Claude Code, ChatGPT, OpenHands, or similar coding agents.
- Teams that want durable project memory without a heavy platform.
- Builders who want agents to preserve decisions, respect boundaries, and stop relearning the same context every session.

## What This Repo Provides

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
mcp_security.md

models/
cognition/
skills/
runbooks/
templates/
examples/
ecosystem/
```

## Core Idea

Agents perform better when the project carries its own operating context.

The files in this repo answer:

- What should the agent read first?
- What is the project contract?
- What can the agent change without asking?
- What decisions have already been made?
- What long-term goals should the agent preserve?
- What evidence must be produced before work is considered complete?
- What data must never be committed?
- How should work be handed off between sessions?
- How should the repo periodically prune junk and improve itself?

## Use

Copy the files you need into your repository or knowledge vault.

Start with:

1. `AGENTS.md`
2. `START_HERE.md`
3. `repo_contract.md`
4. `memory_model.md`
5. `decision_log.md`
6. `handoff_log.md`
7. `qa_gauntlet.md`
8. `security_review.md`
9. `tool_use_guardrails.md`

Then adapt the models, examples, and templates to your project.

## Public Boundary

This repo contains generic public patterns only.

Do not commit:

- personal memory;
- private client/project context;
- secrets or credentials;
- private communications;
- raw chat transcripts;
- proprietary source indexes;
- internal names, emails, handles, or private identifiers.

Private operating memory belongs in a private repo or local vault.

## Design Principles

- Markdown first.
- Small files over giant manuals.
- Source artifacts over model memory.
- Decisions over vibes.
- Verification over confidence.
- Root causes over workarounds.
- Minimal process before heavy process.
- Public templates, private context elsewhere.
- Connector-driven automation should always target an explicitly named repository.
