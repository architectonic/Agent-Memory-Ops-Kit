# Ontology

Ontology files define the shared vocabulary an agent should use before it edits a project, memory vault, or documentation set.

## Purpose

Agents drift when they invent terms. A small ontology gives them a stable vocabulary for classifying work, evidence, decisions, and memory.

## Rule

Do not treat this ontology as project truth. Treat it as a starter vocabulary that must be adapted to the target repository.

## Core Concepts

- **Source artifact**: A recoverable artifact such as code, docs, commits, issues, design files, public references, or explicit human answers.
- **Fact**: A claim backed by a recoverable source artifact.
- **Decision**: A chosen direction with reason, scope, consequence, and status.
- **Assumption**: A provisional claim that must be labeled and revisited.
- **Open question**: A known unknown that must not be filled by guessing.
- **Goal**: A desired state with scope, constraints, and evidence of completion.
- **Constraint**: A boundary that must not be violated while pursuing a goal.
- **Contract**: A clarified deliverable with acceptance criteria and validity conditions.
- **Slice**: The smallest coherent unit of work that can be changed, reviewed, and verified.
- **Patch**: A concrete change to files, behavior, configuration, documentation, or state.
- **Handoff**: A compact transfer note that lets another human or agent continue work without guessing.
- **Skill**: A repeatable procedure with trigger, inputs, steps, verification, and failure modes.
- **Runbook**: An ordered composition of skills for a recurring workflow.

## Adaptation

When copying this kit into a real project:

1. Keep generic concepts that fit.
2. Remove concepts that do not apply.
3. Add project-native terms only after source review or human confirmation.
4. Keep invented terms out of canonical files until validated.
