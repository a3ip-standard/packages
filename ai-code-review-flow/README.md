# ai-code-review-flow

Generic GitLab/GitHub code review workflow, packaged as an installable A3IP
package. The AI reads a merge/pull request diff, applies a structured
7-category review checklist (correctness, security, performance, code quality,
tests, breaking changes, documentation), and posts the review comment back to
GitLab or GitHub via REST API. The platform and project are chosen at install
time, so the same package works against any repo you have a token for.

## What you get

- A **"start code review"** workflow your AI runs on demand against an open MR/PR.
- A **Last Review** card tracking the most recent verdict — Approved, Needs
  Changes, or Commented — with a link back to the review.

## Requirements

- **Platforms:** Cowork, Claude Code, Codex, Cursor
- **Tools:** Python ≥ 3.9 (runs the bundled API call)
- **Network:** `gitlab.com` and/or `api.github.com` (to post review comments)
- **MCPs:** none
- **Config (collected during install):** target platform (GitLab or GitHub),
  the project/repo reference, and an API token

## Install

Give the bundle URL to your A3IP-aware AI and ask it to install the package:

```
https://github.com/a3ip-standard/packages/raw/main/ai-code-review-flow/ai-code-review-flow-v1.5.0.a3ip.bundle
```

The AI follows the bundle's `INSTALL.md` and runs a short configuration wizard.

## Try it

With the package installed and pointed at an open MR/PR, say **"start code
review"**. The AI reads the diff, applies the checklist, posts a structured
review comment, and refreshes the Last Review card.

---

Author: Maksym Prydorozhko · License: Apache-2.0 · Source:
[a3ip-standard/packages](https://github.com/a3ip-standard/packages)
