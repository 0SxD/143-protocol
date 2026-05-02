# 143-protocol

Eight-module root operating contract for multi-agent AI systems: drop any module into CLAUDE.md and your agent changes behavior; drop all eight and you have a structurally governed agent.

## Status

Experimental. Maintained by Sage / 0SxD as part of an ongoing research portfolio focused on prompt engineering, agent skills, and LLM evaluation.

## What this is

143_protocol_a is a structured prompt engineering framework that functions as a governance layer for multi-agent AI systems. It defines identity stability, decision-making gates, memory architecture, communication patterns, and output contracts for any agent operating under the 0sXai stack. Each module is a standalone markdown file that can be composed into a CLAUDE.md (or equivalent system prompt) incrementally. The protocol is model-agnostic: it works with Claude, GPT-4-class models, and any frontier LLM that reads a system prompt.

## Approach

- Eight composable modules with explicit dependency ordering
- Root-wins-on-conflict rule: any sub-agent configuration may only add scope, never contradict the root protocol
- Zero-assumption mandate: every agent claim must cite an accessible, verified source; doubt stops execution
- Stigmergic coordination: agents communicate by writing artifacts to the environment, not peer-to-peer
- Three-gate output evaluation (Trinity Dialectic) before any finalize action
- Quarantine protocol: unverified research is held in a barrier zone until Trinity verification passes

## Layout

- `modules/` - eight markdown modules (01 through 08), each a standalone governance unit
  - `01_zero_assumption_mandate.md` - never fill a gap; ask instead
  - `02_confidence_loop.md` - 100% confidence gate before execution
  - `03_trinity_dialectic.md` - three-gate output evaluation (Logos, Pathos, Ethos)
  - `04_acceptable_output.md` - output contract and quarantine protocol
  - `05_acce_memory.md` - three-layer memory architecture (Cache / RAM / Disk)
  - `06_canary_pattern.md` - session integrity token; anomalies are signals
  - `07_mi9_identity_guard.md` - agent identity stability under adversarial prompts
  - `08_stratum_architecture_pointer.md` - where this protocol fits in the full 0sXai stack
- `examples/` - example CLAUDE.md showing full protocol composition
- `_visuals/` - protocol blueprint diagram

## Usage / How to read this

This repo is a documentation and governance spec bundle. Open `examples/CLAUDE_md_example.md` first.

To adopt a single module: copy its markdown into your project's CLAUDE.md (or system prompt), adapting the agent identity fields. Modules are designed to compose without conflict.

To adopt the full protocol: copy `examples/CLAUDE_md_example.md` into your project as CLAUDE.md. Any AGENTS.md-aware coding agent will read it on its own.

## Prior art and citations

- AGENTS.md spec (Linux Foundation Agentic AI Foundation) - AGENTS.md at repo root conforms to this spec; module 08 references the stratum layer model
- Anthropic Skills spec / agentskills.io - module composition pattern references the Agent Skills convention

See also: [trinity-dialectic](https://github.com/0SxD/trinity-dialectic) for the runnable Python engine implementing the protocol's dialectic gate.

## License

MIT. Copyright (c) 2026 Sage / 0SxD.
Author: Sage / 0SxD

## Notes

This repo is part of an active R&D portfolio. Content may move, change, or be withdrawn. Issues and PRs welcome but reviews are best-effort.
