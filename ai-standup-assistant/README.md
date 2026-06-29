# ai-standup-assistant

A daily-standup generator, packaged as an installable A3IP package. The AI
aggregates your last-24h GitHub activity across configured repos and reports
yesterday's commits and merged PRs, today's work in progress (open PRs,
in-flight issues), and blockers (PRs awaiting review, issues stalled beyond a
threshold). The result renders to a **Today's Standup** Cowork card, degrading
to a markdown file on other runtimes.

## What you get

A **"run standup"** workflow and a three-section **Today's Standup** card —
Yesterday, Today, Blockers — refreshed each time you run it.

## Requirements

- **Platforms:** Cowork, Claude Code, Codex
- **MCPs:** **GitHub MCP required** — the official server at
  `api.githubcopilot.com/mcp/`, added via Connectors. (Not the built-in "GitHub
  Integration", which only handles file attachment.) The Cowork artifact MCP is
  optional: it powers the live card, and without it the standup degrades to a
  markdown file.
- **Config (collected during install):** the list of GitHub repos to track
  (owner / repo) and your author login

## Install

Give the bundle URL to your A3IP-aware AI and ask it to install the package:

```
https://github.com/a3ip-standard/packages/raw/main/ai-standup-assistant/ai-standup-assistant-v1.0.0.a3ip.bundle
```

## Try it

Say **"run standup"**. The AI queries your configured repos, classifies the
activity into Yesterday / Today / Blockers, and refreshes the Today's Standup
card.

---

Author: Maksym Prydorozhko · License: Apache-2.0 · Source:
[a3ip-standard/packages](https://github.com/a3ip-standard/packages)
