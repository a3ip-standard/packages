# cowork-backlog

A lightweight project-execution tracker, packaged as an installable A3IP
package. The AI manages a backlog of iterations (logical phases), stories,
tasks, and notes across one or more projects, and renders a read-only Kanban
board you can keep coming back to. All state lives as human-readable markdown
owned by a deterministic Python engine, so ids, derived fields, and the board
never drift — it exists to fix the two things that break on long, multi-session
projects: losing the overview of progress, and forgetting what was discovered
mid-work.

## What you get

Four workflows — **"set up a backlog"**, **"add a story"**, **"log a
decision"**, and **"show the board"** — backed by a deterministic `backlog.py`
engine, plus a **Backlog Board** artifact: a read-only Kanban view across the
planned → in_progress → test → completed columns, with a project switcher for
the multi-project shared board.

## Requirements

- **Platforms:** Cowork, Claude Code
- **Tools:** Python ≥ 3.9 (runs the backlog engine; writes only inside your
  configured directories)
- **MCPs:** none
- **Config (collected during install):** an install directory and a shared hub
  directory for the cross-project board

## Install

Give the bundle URL to your A3IP-aware AI and ask it to install the package:

```
https://github.com/a3ip-standard/packages/raw/main/cowork-backlog/cowork-backlog-v1.0.0.a3ip.bundle
```

## Try it

Say **"set up a backlog"** in a project, then **"add a story"** as work comes
up and **"show the board"** to see it. When something worth remembering surfaces
mid-work, **"log a decision"** files it as a durable note rather than losing it
in a transcript.

---

Author: Maksym Prydorozhko · License: Apache-2.0 · Source:
[a3ip-standard/packages](https://github.com/a3ip-standard/packages)
