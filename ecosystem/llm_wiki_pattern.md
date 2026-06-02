# LLM Wiki Pattern

An LLM wiki is a small, structured, project-local knowledge base designed to be read by agents before they act.

It is not a raw documentation dump. It is a curated operating map that helps agents understand the project, preserve decisions, avoid repeated mistakes, and recover context across sessions.

## Why It Matters

Coding agents often fail because they enter a repo with no durable memory of:

- project ontology;
- architecture decisions;
- local setup gotchas;
- known failure modes;
- source-of-truth boundaries;
- security constraints;
- handoff state.

A wiki gives the repo a readable memory layer.

## What Belongs In An LLM Wiki

Useful pages include:

- project overview;
- glossary or ontology;
- architecture notes;
- decision log;
- handoff log;
- source index;
- setup notes;
- QA checklist;
- security boundaries;
- agent permissions;
- recurring bug notes with verified fixes.

## What Does Not Belong

Do not include:

- secrets;
- raw private transcripts;
- personal memory;
- temporary plans;
- stale guesses;
- unchecked generated summaries;
- private client context in public repos;
- broad documentation copied from elsewhere.

## Canonicalization Rule

Before promoting a note into the wiki, classify it as:

```text
Fact        - backed by a recoverable source.
Decision    - chosen direction with reason and consequence.
Assumption  - provisional claim that must be labeled.
Question    - known unknown.
Rule        - durable operating instruction.
Handoff     - transfer note for future work.
Junk        - temporary context to delete or ignore.
```

Only facts, decisions, questions, rules, and useful handoffs belong in durable wiki pages.

## Suggested Structure

```text
wiki/
  overview.md
  ontology.md
  decisions.md
  handoffs.md
  sources.md
  setup.md
  qa.md
  security.md
  gotchas.md
```

For small repos, do not create every file. Start with the files that prevent real errors.

## Maintenance Cycle

Periodically review the wiki:

1. Remove stale or duplicated notes.
2. Promote verified recurring lessons.
3. Mark assumptions and open questions.
4. Link decisions to source artifacts.
5. Keep pages short enough for agents to read.

## Failure Modes

- Turning the wiki into a hallucination archive.
- Treating generated summaries as source truth.
- Adding every thought instead of durable knowledge.
- Duplicating rules across many files.
- Letting stale decisions silently control future work.
- Confusing public reusable patterns with private project memory.
