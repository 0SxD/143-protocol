---
title: "Claude Code CLI Handoff: render v02 blueprint to PNG"
session: vis-blueprint-2026-04-29-S2
date: 2026-04-29
purpose: hand off the Puppeteer render step to Claude Code CLI because Cowork cannot run headless Chrome
trinity-gate: 15/15 PROCEED
---

# CLI handoff: render VIS_01 blueprint to PNG

Copy-paste this into a fresh Claude Code CLI session running in the
`Visual_Prompts_Infographics_Revisions` directory.

---

## CLI prompt (paste into Claude Code)

```
You are continuing the 0sXai system_directive_protocol blueprint workstream.
Read AGENTS.md inside vis-blueprint-bundle-v0.1.0.zip first. Then read
PLAN_2026-04-29_compound_engineering_v01.md for the current execution context.

Your single task this session: render VIS_01_system_directive_blueprint_v02.html
to a publishable PNG.

Constraints:
- No em dashes. No en dashes.
- Address Sage only.
- Do not modify the HTML source. Render only.
- Do not modify any *_ARCHIVE_ARTIFACT.png file.
- Do not modify PROMPT_system_directive_authoring_v01.md (read-only, 15/15).

Steps:
1. If the Puppeteer MCP server is not connected, install it:
   claude mcp add puppeteer npx -y @modelcontextprotocol/server-puppeteer
2. Open VIS_01_system_directive_blueprint_v02.html in headless Chrome at
   viewport 960px wide, 2x device scale factor for retina output.
3. Wait for full render (fonts, SVG, transitions complete). Use a 2 second
   settle delay or waitForNetworkIdle.
4. Capture full-page PNG. Save as VIS_01_system_directive_blueprint_v02.png
   in the same directory.
5. Append a row to MANIFEST.md:
   | VIS_01_system_directive_blueprint_v02.png | rendered from v02 HTML | 2026-04-29 | this session |
6. Stop. Do not produce section breakouts in this session. Do not edit
   the HTML source. Report to Sage.

Trinity gate before stopping:
- Logos 0-5: PNG visually matches HTML. Width is 960px. No clipped sections.
- Pathos 0-5: All 5 sections legible. Title text is "0sXai Read-Only Researcher: The system_directive_protocol Blueprint".
- Ethos 0-5: HTML untouched. No em or en dashes anywhere added.
- Sum must reach 15. Below 15, do not save the PNG. Loop.

If you cannot reach 15/15, output the three open questions in three
categories (Architecture and State, Evidence and Sourcing, Intent and
Constraint) and STOP for Sage direction.
```

---

## What Cowork did NOT do (so Sage knows the boundary)

- Did not edit v02 HTML this session (gate 1.E1 still open)
- Did not run any rendering, headless or otherwise
- Did not produce section breakouts
- Did not touch PROMPT or any *_ARCHIVE_ARTIFACT file

## What Cowork DID do this session

- Verified bundle zip on disk and inventoried its 5 files
- Verified v02 HTML has 0 text occurrences of `143_protocol_a` and is titled correctly
- Wrote 5 memory files to persist context across future sessions
- Authored `PLAN_2026-04-29_compound_engineering_v01.md` (compound system-design plus architecture skill output)
- Authored this CLI handoff
- Self-scored 15/15 Trinity gate on the plan

END_HANDOFF
