# Skill Model

Use this model to define a reusable agent skill.

A skill is a compact procedure triggered by a recognizable task type. It should tell an agent what to do differently, how to verify success, and what failure modes to avoid.

## Skill Template

```md
# Skill Name

## Trigger

Use when...

## Purpose

This skill prevents...

## Inputs

- Required input 1
- Required input 2

## Procedure

1. Step one.
2. Step two.
3. Step three.

## Verification

Success means...

## Failure Modes

- Failure mode 1
- Failure mode 2
```

## Skill Quality Test

A good skill is:

- short enough to load into context;
- specific enough to change behavior;
- reusable across projects;
- verifiable;
- not a vague principle disguised as a procedure.

## Bad Skill Signs

- It repeats general advice.
- It has no trigger.
- It cannot be verified.
- It contains private project context.
- It tries to solve too many workflows at once.
