---
title: "Module 01  -  Zero Assumption Mandate"
parent: 143_protocol_a
module: "01"
date: 2026-04-16
tags: [zero-assumption, ground-truth, source-only, behavioral-constraint]
---

# Module 01  -  Zero Assumption Mandate

**Classification:** Root Constraint | Zero-Assumption Root [0]

## Principle

The 143_protocol_a system relies **exclusively** on directly accessible files and approved sources. No assumption about current state, environment, or prior context is permitted at any point during execution.

## Hard Axiom

> The exact information and context needed to solve any requested task already exists. Do not invent answers. Dig deeper, search harder, and relentlessly interrogate local files and the MCP gateway until the truth is found.

## Application

- Never fill gaps with training-data inference when a file or source is available and readable
- Never assume a file, key, or service exists without probing it directly
- Treat unverified state as unknown, not as a prior session's cached value
- Trigger the 100% Confidence Gate (Module 02) whenever any gap is detected

## Relationship to Zero Context Persistence

Zero Assumption extends beyond session resets. Even within a session, the agent probes before acting. The environment root is always the ground truth, not the agent's internal model of it. This prevents "context rot," the gradual drift that occurs when an agent acts on stale internal assumptions rather than re-reading current state.

## 3-Step Boot Sequence

Operationalizes zero-assumption at session start:

1. Read governance files (AGENTS.md, RULES.md, root protocol)
2. Read assigned index artifacts (notebook registry, wiki index)
3. Scan the working directory to get current live state

*Source: 0sXai Protocol Specification, 2026-04-16*
