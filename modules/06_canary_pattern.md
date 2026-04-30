---
title: "Module 06  -  Canary Pattern"
parent: 143_protocol_a
module: "06"
date: 2026-04-16
tags: [canary, session-integrity, continuity, drift-detection, scope-tag]
---

# Module 06  -  Canary Pattern

**Classification:** Session Integrity / Continuity Verification

## Purpose

The canary is a structured session-integrity token appended to every major artifact. It serves three functions:

1. **Continuity verification** -- confirms the receiving agent loaded the correct protocol context
2. **Scope tag** -- encodes active flags and constraints into a scannable string
3. **Drift detection** -- when an agent echoes the canary, it demonstrates it parsed and accepted the full directive

## The Canonical Canary

```
```

## Tag Glossary

| Tag | Meaning |
|-----|---------|
| `143` | Root protocol identifier |
| `PLAN-ONLY` | Active planning mode; no live execution without gate clearance |
| `cascade` | Territorial cascade in effect (sub-agents inherit root) |
| `emergence` | Design favors emergent architecture over pre-planned structure |
| `Trinity` | Trinity Dialectic gates active on all outputs |
| `no-duplication` | Do not create duplicate artifacts |
| `let-it-emerge` | Do not over-engineer; let structure emerge naturally |
| `design-101` | Foundational design principles apply |
| `0sXai` | Primary agent OS namespace |
| `xDx` | FATExD sub-territory active |
| `A2A` | Agent-to-Agent circuit breaker active |
| `FCEE` | Full Confidence and Evidence Evaluation required |
| `dormant-main` | Main branch remains dormant pending gate clearance |
| `short-form-pending` | Short-Form Principle output standard pending review |

## Usage

Append the full canary string at the end of every protocol artifact, handoff document, and finalized module. When receiving a dispatch, echo the canary in the first response to confirm boot was successful.

*Source: 0sXai Protocol Specification, 2026-04-16*
