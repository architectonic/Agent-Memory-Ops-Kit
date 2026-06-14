# Agent Memory Ops Kit

A Markdown-native operating memory layer for AI coding agents.

Agent Memory Ops Kit gives coding agents governed project context before they touch your repo: source hierarchy, authority rules, memory classes, decision records, handoff rituals, QA checks, security boundaries, tool-use guardrails, and memory reconciliation.

It is not a SaaS, runtime, database, RAG stack, prompt dump, or long wiki.

It is a small operational filesystem for turning stateless coding agents into safer, more consistent project operators.

## Core Claim

Better models are not enough.

Agentic work fails when agents forget decisions, trust stale context, confuse assumptions with facts, repeat old investigations, or act without understanding the repo's safety boundaries.

Memory Ops is the discipline of governing that layer.

The goal is not more memory.

The goal is better-governed memory.

## Who It Is For

- Developers using Codex, Cursor, Claude Code, ChatGPT, OpenHands, or similar coding agents.
- Teams that want durable project memory without a heavy platform.
- Builders who want agents to preserve decisions, respect boundaries, verify work, and stop relearning the same context every session.

## What This Repo Provides

```text
AGENTS.md
START_HERE.md
memory_ops_doctrine.md
modus_operandi.md
repo_contract.md
authority.md
memory_model.md
memory_lifecycle.md
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
- Which source has authority when sources conflict?
- What can the agent change without asking?
- What decisions have already been made?
- What long-term goals should the agent preserve?
- What evidence must be produced before work is considered complete?
- What data must never be committed?
- How should work be handed off between sessions?
- How should durable memory be promoted, demoted, pruned, or deleted?
- How should the repo periodically prune junk and improve itself?

## Use

Copy the files you need into your repository or knowledge vault.

Start with:

1. `AGENTS.md`
2. `START_HERE.md`
3. `memory_ops_doctrine.md`
4. `modus_operandi.md`
5. `repo_contract.md`
6. `authority.md`
7. `memory_model.md`
8. `memory_lifecycle.md`
9. `decision_log.md`
10. `handoff_log.md`
11. `qa_gauntlet.md`
12. `security_review.md`
13. `tool_use_guardrails.md`

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
- Authority before recall.
- Decisions over vibes.
- Verification over confidence.
- Memory reconciliation over context hoarding.
- Root causes over workarounds.
- Minimal process before heavy process.
- Public templates, private context elsewhere.
- Connector-driven automation should always target an explicitly named repository.
