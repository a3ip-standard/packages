# ai-research-workspace

A research-workspace curator, packaged as an installable A3IP package. The AI
captures papers, logs experiments, links them bidirectionally, applies review
templates (concise / detailed / critical), and synthesizes findings across a
structured `papers/` + `experiments/` + `syntheses/` layout. Everything lives
as local markdown files with YAML frontmatter — no external services, no
scripts, no database.

## What you get

Five workflows — **"add paper"**, **"log experiment"**, **"link experiment to
paper"**, **"review papers"**, and **"synthesize findings"** — plus a **Paper
Inbox** Kanban card and an **Experiment Log** table (both degrade gracefully to
markdown tables off Cowork).

## Requirements

- **Platforms:** Cowork, Claude Code, Codex
- **Tools / MCPs:** none — the AI does the work with its built-in file tools
- **Config (collected during install):** an install directory and your research
  workspace directory. Your notes live in the workspace directory and persist
  across uninstalls.

## Install

Give the bundle URL to your A3IP-aware AI and ask it to install the package:

```
https://github.com/a3ip-standard/packages/raw/main/ai-research-workspace/ai-research-workspace-v1.1.0.a3ip.bundle
```

## Try it

Say **"add paper"** with an arXiv ID, DOI, or URL — the AI files it under
`papers/` with frontmatter and a notes block. Once you have a few reviewed,
**"synthesize findings"** rolls them into a themed summary (themes, methods,
gaps, recommendations).

---

Author: Maksym Prydorozhko · License: Apache-2.0 · Source:
[a3ip-standard/packages](https://github.com/a3ip-standard/packages)
