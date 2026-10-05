---
name: project-evolution
description: Organize the evolution of software projects using clear architecture, coordinated parallel work, and evidence-based validation.
---

# Project Evolution

Use this skill when a project needs to be planned, divided among specialized agents, reviewed across workstreams, or advanced through explicit quality gates.

## Core method

Apply the three pillars:

1. **Architecture**: define boundaries, responsibilities, interfaces, dependencies, and acceptance criteria before parallel work begins.
2. **Coordination**: divide work into low-overlap units with explicit inputs, outputs, owned files, and dependency order.
3. **Evidence**: connect each completion claim to a test, inspection, demonstration, or other concrete verification.

## Required behavior

- Preserve the user's scope and authorization.
- Identify the source of truth before delegating work.
- Make ownership and handoff conditions explicit.
- Prefer small, independently verifiable work units.
- Surface conflicts between architecture and implementation early.
- Distinguish `PASS`, `PASS CONTROLADO`, `NOT_VERIFIED`, and `BLOCKED`.
- Never present source-level evidence as proof of production behavior unless production was actually verified.

## Suggested output

When organizing a project, produce:

- objective and non-goals;
- architecture map;
- workstream table with owners and dependencies;
- decision log;
- evidence plan;
- current gate status and open risks.

## Boundaries

This skill does not authorize deployment, publication, destructive changes, or external communication. Those actions require explicit user authorization and their own verification.
