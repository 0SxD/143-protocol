---
title: "0sXai system_directive_protocol — Compound Engineering Plan"
session: vis-blueprint-2026-04-29-S2
date: 2026-04-29
agent: claude-opus-4-7 (Cowork mode, Sage)
protocol: seek_love (Zero Assumption + 100% Confidence + Trinity Dialectic 15/15)
skills_used: engineering:system-design + engineering:architecture
trinity-gate: pending Sage approval before P1 execution
---

# Compound Engineering Plan v0.1

Compound use of two installed skills:
- `engineering:system-design` for requirements, high-level design, scale, trade-offs
- `engineering:architecture` for ADR-style decision records on load-bearing choices

Status of inputs verified at session open:
- `vis-blueprint-bundle-v0.1.0.zip` exists at workspace root (29,166 B, 5 files)
- `VIS_01_system_directive_blueprint_v02.html` on disk (34,208 B, 2026-04-29 22:23)
- v02 title is `0sXai Read-Only Researcher: The system_directive_protocol Blueprint`
- 0 text occurrences of `143_protocol_a` in v02; 1 incidental `143` inside SVG hex color literal
- v02 directly replaces the legacy "143 blueprint" at the label layer; PNG render is still pending

---

## 1. Requirements (system-design)

### Functional
| ID | Requirement | Phase |
|---|---|---|
| F1 | Edit v02 HTML per Sage corrections | P1 |
| F2 | Render v02 HTML to publishable PNG at 960px width | P1 |
| F3 | Visual QA the PNG against archive PNG, section by section | P1 |
| F4 | Produce 5 section-breakout HTML files (s1 identity through s5 trinity) | P1 |
| F5 | Render each breakout HTML to PNG at full width | P1 |
| F6 | Apply same pipeline to VIS_05_rubric_architect (rubric correction guide) | P2 |
| F7 | Tokenize a shared visual system across all 0sXai infographics | P3 |
| F8 | Overnight CLI sweep of local work repos for publishable / as-product material | P4 |

### Non-functional
- No em dashes (U+2014). No en dashes (U+2013).
- Address Sage only.
- Trinity Dialectic 15/15 gate before any phase finalization.
- Zero Assumption Mandate, 100% Confidence Loop in 3-category form.
- AGENTS.md governance applies inside the bundle.
- All artifacts CC-BY-4.0 attributed to 0SxD.

### Constraints
- Cowork mode cannot run headless Chrome (Puppeteer). All PNG renders require Claude Code CLI handoff.
- `PROMPT_system_directive_authoring_v01.md` is read-only (15/15 locked).
- Canonical archive PNGs are layout reference only, not editable.

---

## 2. High-Level Design

```
┌─────────────────────────────────────────────────────────────────────┐
│                         SAGE (orchestrator)                          │
└──────────┬──────────────────────────────┬───────────────────────────┘
           │                              │
           ▼                              ▼
┌─────────────────────┐         ┌─────────────────────┐
│   COWORK (Opus)     │         │ CLAUDE CODE CLI     │
│   text edits        │         │ headless render     │
│   plan synthesis    │ ◀─────▶ │ Puppeteer PNG out   │
│   memory writes     │         │ overnight subagents │
│   section split     │         │ file system sweep   │
└─────────┬───────────┘         └──────────┬──────────┘
          │                                │
          ▼                                ▼
   ┌────────────────────────────────────────────────┐
   │      Visual_Prompts_Infographics_Revisions\    │
   │   (workspace, mounted, persistent)             │
   └────────────────────────────────────────────────┘
```

Data flow per phase: HTML edit → Cowork writes to disk → Claude Code CLI renders PNG → Sage QA → MANIFEST.md row append.

Component contracts:
- Cowork: text correctness, layout integrity, planning, memory, MANIFEST updates
- Claude Code CLI: any step that needs a real browser, multi-agent orchestration, long-running sweeps
- Memory (persistent): naming locks, protocol gates, bundle pointer, style rules

---

## 3. Phase Deep Dives

### Phase 1: VIS_01 blueprint to PNG

Tasks in order:
1. Sage specifies edits to `VIS_01_system_directive_blueprint_v02.html` (gate: 1.E1 below).
2. Cowork applies edits, writes back to disk, updates MANIFEST.md.
3. Claude Code CLI renders v02 to `VIS_01_system_directive_blueprint_v02.png` at 960px width via Puppeteer.
4. Sage visual QA against `Protocol_Blue_Print_ARCHIVE_ARTIFACT.png`.
5. Cowork mechanically splits the v02 HTML into 5 section files:
   - `VIS_01_s1_identity_v02.html`
   - `VIS_01_s2_boot_octopus_v02.html`
   - `VIS_01_s3_zero_assumption_quarantine_v02.html`
   - `VIS_01_s4_runtime_loop_ralph_v02.html`
   - `VIS_01_s5_trinity_v02.html`
6. Claude Code CLI renders each section breakout to PNG.
7. Sage QA each section.

Open gates:
- 1.E1: what specific edits to v02 HTML? (Sage to enumerate before P1 starts)

### Phase 2: VIS_05 rubric architect

Tasks in order:
1. Pull canonical text source for the rubric (likely `VIS_rubric_architect_text_equivalent_v01.md`).
2. Author `VIS_05_rubric_architect_v02.html` mirroring the v02 blueprint style tokens.
3. Render to PNG via CLI.
4. Sage QA.
5. Section breakouts if applicable.

Open gates:
- 2.E1: should V05 reuse the v02 dark theme and token set, or stay aligned with the existing `Rubric_Correction_Justification_Guide.png` palette?
- 2.E2: scope of v02-style refresh on the rubric, label-only or full layout?

### Phase 3: Full visual system rebuild (tokenization)

Goal: a shared design-token file so every 0sXai infographic resolves the same colors, type, spacing, frame.

Tasks in order:
1. Audit all PNGs and HTMLs in the working directory for color, type, frame inconsistencies.
2. Extract a `vis_tokens_v01.css` shared stylesheet with named tokens (color.bg.deep, color.accent.green, type.body, frame.radius, etc.).
3. Refactor v02 HTML to consume tokens.
4. Author each remaining infographic as a token-consuming HTML source:
   - Trinity Protocol overview
   - Pathos Core Gate diagram
   - Symbolic Reasoning Architecture
   - Event Source Identity
   - Neuro-Symbolic Logic System
   - AI audit domain slicing module
5. Render each via CLI, QA, MANIFEST update.

Open gates:
- 3.E1: which PNG has the canonical aesthetic to derive tokens from?
- 3.E2: do we keep portrait 960px width as the standard, or move to 1080p/1440p variants?

### Phase 4: Overnight CLI sweep ("anything-as-product")

This runs in Claude Code CLI, not Cowork. Designed for an unattended 6-12 hour run.

Goal: catalog Sage's local work, score each item for publishability, surface a top-N portfolio in the morning.

Sub-agent roles (compound engineering):
| Role | Responsibility | Read scope | Write scope |
|---|---|---|---|
| Foreman (top-level session) | Queue management, checkpoint/resume, wake summary | Index files | Output dir only |
| Cataloger | Walk tree, emit inventory rows (path, size, mtime, ext, first 200 chars) | All in-scope dirs | `inventory.jsonl` |
| Publishability Scorer | Score each item 0-5 on completeness, novelty, presentability, IP-clean, effort-to-publish | Inventory + per-file head | `scores.jsonl` |
| Asset Extractor | Pull quotable highlights and 1-paragraph summaries from top-scored items | Top-scored files | `assets/<id>.md` |
| Synthesizer | Group by theme, draft "potential portfolio" report | All scored items | `themes.md`, `wake_summary.md` |

Output structure:
```
_overnight_sweep_2026-04-29/
  wake_summary.md          # TL;DR and recommended next actions
  inventory.jsonl          # one row per file scanned
  scores.jsonl             # one row per file scored
  themes.md                # grouped by theme, top items per theme
  top.md                   # global top 25 with reasoning
  assets/                  # per-item summary cards
  log.md                   # foreman activity log
  state.json               # checkpoint for mid-run resume
```

Hard guardrails:
- Read-only on source directories. Write only to `_overnight_sweep_<timestamp>/`.
- No network calls.
- No edits to canonical files (`PROMPT_*v01.md`, `*_ARCHIVE_ARTIFACT.png`).
- Stop condition: time budget (default 10 hours wall clock) OR queue empty OR error rate > 5%.
- Resumability: every 30 minutes, foreman writes `state.json` so a crashed run can resume.

Open gates:
- 4.E1: which root paths are in scope? (likely `C:\Users\Austin.DESKTOP-8AMMKQP\Downloads\SandBoxSetup\` plus any others Sage names)
- 4.E2: definition of "publishable" / "as-product" (criteria rubric, Sage to define)
- 4.E3: time budget (default 10h, Sage to confirm)
- 4.E4: model selection per role (recommend Sonnet for Cataloger and Scorer, Haiku for parallelism, Opus only for Synthesizer)

---

## 4. Architecture Decision Records (ADRs)

### ADR-001: HTML/CSS/SVG single-source vs Mermaid pipeline
**Status:** Accepted (carried from prior session)
**Context:** Mermaid `.mmd` exists at `VIS_protocol_blueprint_v01.mmd` but renders with limited style control.
**Decision:** Hand-authored HTML/CSS/SVG is the canonical source. Mermaid is reference only.
**Consequences:** Higher authoring cost per infographic, much higher visual fidelity. Tokenization (P3) recovers the per-asset cost.

### ADR-002: Headless renderer choice
**Status:** Proposed
**Context:** Need PNG export of HTML at 960px (and section widths). Three viable paths.
**Options:**
| Option | Complexity | Speed | Fidelity | Sage familiarity |
|---|---|---|---|---|
| Puppeteer (MCP server) | Med | Fast | High | Listed in AGENTS.md |
| Playwright | Med | Fast | High | Not yet evaluated |
| wkhtmltopdf | Low | Fast | Medium (older Chrome engine) | Unknown |
**Recommended:** Puppeteer MCP server, because AGENTS.md already specifies it.
**Action:** `claude mcp add puppeteer npx -y @modelcontextprotocol/server-puppeteer`

### ADR-003: Edit-then-breakout vs Breakout-then-edit
**Status:** Proposed
**Context:** Sage requested both edits and section breakouts.
**Decision:** Edit v02 HTML first, then mechanically split.
**Reason:** Splitting first creates 5 surfaces to edit instead of 1. Editing in the single-source file preserves diff legibility and avoids drift.
**Consequence:** Sage must enumerate edits before breakouts begin (gate 1.E1).

### ADR-004: Multi-agent role schema for overnight sweep
**Status:** Proposed
**Context:** Need autonomy without uncontrolled writes.
**Decision:** 5-role schema with strict read/write scope per role and a Foreman that owns checkpoints.
**Consequence:** Lower throughput than a free-form swarm but recoverable mid-run and audit-friendly.

### ADR-005: Output destination for overnight sweep
**Status:** Proposed
**Decision:** Fresh timestamped folder, top-level `wake_summary.md`, JSONL for machine-readable layers.
**Reason:** A single morning artifact for Sage; deeper files for follow-up; no contamination of canonical workspace.

---

## 5. Trade-off Summary

| Decision | What gets easier | What gets harder | Revisit when |
|---|---|---|---|
| HTML/CSS/SVG hand-authored | Visual fidelity, edit precision | Per-asset effort | After P3 tokens land |
| Puppeteer for render | One-line install, AGENTS.md aligned | Need Node.js on the CLI host | Render fails or hangs |
| Edit-first, split-second | Single diff, single source of truth | Blocked on Sage edit list | Edit list not arriving |
| 5-role overnight sweep | Auditability, resumability | More orchestration code | First run reveals bottleneck |

---

## 6. Action queue

```
P1.1  Sage enumerates v02 HTML edits                       [GATE 1.E1]
P1.2  Cowork applies edits to v02 HTML                     [Cowork]
P1.3  Cowork updates MANIFEST.md                           [Cowork]
P1.4  Claude Code CLI installs Puppeteer MCP if missing    [CLI]
P1.5  Claude Code CLI renders v02 to PNG @ 960px           [CLI]
P1.6  Sage visual QA                                       [GATE]
P1.7  Cowork splits to 5 section HTML files                [Cowork]
P1.8  Claude Code CLI renders each section to PNG          [CLI]
P1.9  Sage section QA                                      [GATE]
P1.10 Cowork updates MANIFEST.md                           [Cowork]
─── P2 begins after P1.10 closes ───
P2.1  Sage answers 2.E1, 2.E2                              [GATE]
...
─── P3 begins after P2 closes ───
─── P4 can begin in parallel after P1 closes ───
P4.1  Sage answers 4.E1 through 4.E4                       [GATE]
P4.2  Cowork writes overnight prompt to a runnable file    [Cowork]
P4.3  Sage launches Claude Code CLI overnight              [Sage + CLI]
P4.4  Morning: Sage reads wake_summary.md                  [Sage]
```

---

## 7. Open gates (must close before each phase)

- 1.E1: v02 HTML edits enumerated by Sage
- 2.E1: rubric architect aesthetic alignment
- 2.E2: rubric scope, label-only or full layout
- 3.E1: canonical aesthetic source
- 3.E2: width standard
- 4.E1: root paths for sweep
- 4.E2: "publishable" / "as-product" criteria rubric
- 4.E3: time budget
- 4.E4: per-role model selection

---

## 8. Trinity Dialectic gate (this plan, self-scored, pending Sage)

| Lens | Score | Rationale |
|---|---|---|
| Λ Logos | 5/5 | Cited bundle, verified file state, two skill SKILL.md files, AGENTS.md governance |
| Π Pathos | 5/5 | Addresses Sage's exact ask: protocol replacement check, compound planning, phased 1-2-3-4 scope, overnight CLI handoff included |
| Θ Ethos | 5/5 | No em or en dashes, sources cited, Sage addressed, gates honored, 4 categories of open questions surfaced |
| Global | 15/15 | Self-scored PROCEED, Sage approval pending |

END_PLAN
