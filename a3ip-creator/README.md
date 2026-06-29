# a3ip-creator

The reference A3IP authoring tool — distributed as an A3IP package itself. It
guides an AI through authoring a new A3IP package from scratch via a structured
intake conversation, or reverse-engineers an existing workflow via Discovery
mode, then drives the `a3ip` CLI through scaffold, validate, and bundle to
produce a distributable `.a3ip.bundle`. Platform-agnostic by design.

## What you get

Two workflows: **"create a package"** (intake → scaffold → validate → build)
and **"cut a new version"** (bump manifest → prepend changelog → validate →
rebundle).

## Requirements

- **Platforms:** Cowork, Claude Code, Codex, Cursor
- **Tools:** Python ≥ 3.9 and the
  [a3ip CLI](https://github.com/a3ip-standard/cli) ≥ 1.5.4
  (`pip install --upgrade a3ip`). PyYAML is optional and only improves manifest
  parsing accuracy.
- **MCPs / config:** none — no configuration wizard

## Install

Give the bundle URL to your A3IP-aware AI and ask it to install the package:

```
https://github.com/a3ip-standard/packages/raw/main/a3ip-creator/a3ip-creator-v3.0.1.a3ip.bundle
```

## Try it

Say **"create a package"**. The Creator interviews you about the workflow,
scaffolds the package, validates it against the spec, and hands you a
ready-to-publish bundle.

---

Author: Maksym Prydorozhko · License: Apache-2.0 · Source:
[a3ip-standard/creator](https://github.com/a3ip-standard/creator)
