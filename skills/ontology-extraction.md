# Ontology Extraction Skill

## Trigger

Use when an agent needs to understand a domain, product, codebase, or workflow before changing it.

## Inputs

- Source artifacts.
- Existing docs.
- User-stated scope.

## Procedure

1. Read source artifacts before naming concepts.
2. Extract recurring nouns, workflows, entities, states, and boundaries.
3. Define each concept using source language.
4. Identify relationships between concepts.
5. Separate concepts from decisions and preferences.
6. Mark uncertain concepts as open questions.
7. Write the smallest useful glossary or ontology note.

## Verification

A domain expert should recognize the vocabulary as native to the project.

## Failure Modes

- Imposing generic architecture terms.
- Renaming project concepts casually.
- Treating UI labels as full ontology.
- Turning assumptions into definitions.
