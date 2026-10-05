---
name: parallel-work-coordination
description: Decompose software work into coordinated parallel streams with explicit ownership, dependencies, handoffs, and conflict resolution.
---

# Parallel Work Coordination

Use this skill when multiple humans or agents will work on related parts of a project at the same time.

## Decomposition

For each workstream, define:

- one outcome;
- one owner;
- the files or interfaces it may change;
- the inputs it requires;
- the dependencies it creates;
- one verification condition.

Prefer boundaries that can be reviewed independently. Keep shared contracts in a clearly identified source of truth and avoid parallel edits to the same contract without an explicit owner.

## Handoff

Every handoff must state what changed, what was verified, what remains uncertain, and whether another stream must adapt. A handoff is incomplete when it reports only that work is finished.

## Conflict handling

When streams disagree:

1. identify the conflicting contract or assumption;
2. compare each option against the project objective and constraints;
3. record the decision and its consequence;
4. update affected workstreams before continuing.

Do not silently merge incompatible assumptions.

## Boundaries

This skill coordinates work but does not authorize merging, deployment, publication, or destructive changes.
