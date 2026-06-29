# packages

A3IP public package gallery and registry.

This repository hosts published A3IP packages — distributable
`.a3ip.bundle` files that any A3IP installer can consume. See the
[A3IP specification](https://github.com/a3ip-standard/spec) for the
package format and install protocol.

## Discovering packages

[`registry.yaml`](./registry.yaml) is the machine-readable index. It
lists every published package with its description, author, license,
latest version, minimum A3IP spec version, supported platforms, and
canonical bundle URL. Installers and discovery tools should fetch this
file rather than scraping directory listings.

Schema documentation lives at the top of `registry.yaml`.

## Available packages

Each package has its own folder with a README describing what it does, what it
requires, and how to install it:

- [**a3ip-creator**](./a3ip-creator/) — the reference A3IP authoring tool;
  guides an AI through creating a new package from scratch.
- [**ai-code-review-flow**](./ai-code-review-flow/) — generic GitLab/GitHub
  code review workflow with a structured 7-category checklist.
- [**ai-research-workspace**](./ai-research-workspace/) — captures papers, logs
  experiments, links them, and synthesizes findings as local markdown.
- [**ai-standup-assistant**](./ai-standup-assistant/) — compiles a daily
  standup from your GitHub activity across configured repos.
- [**cowork-backlog**](./cowork-backlog/) — lightweight project-execution
  tracker: backlog, stories, tasks, notes, and a read-only Kanban board, all as
  markdown owned by a deterministic engine.

## Installing a package

Give your A3IP-aware AI the `.a3ip.bundle` URL or the file itself, and
ask it to install the package. The AI follows the spec's bundle preamble
and the `INSTALL.md` inside the bundle.

Latest bundle URLs (from the registry):

- a3ip-creator: `https://github.com/a3ip-standard/packages/raw/main/a3ip-creator/a3ip-creator-v3.0.1.a3ip.bundle`
- ai-code-review-flow: `https://github.com/a3ip-standard/packages/raw/main/ai-code-review-flow/ai-code-review-flow-v1.5.0.a3ip.bundle`
- ai-research-workspace: `https://github.com/a3ip-standard/packages/raw/main/ai-research-workspace/ai-research-workspace-v1.1.0.a3ip.bundle`
- ai-standup-assistant: `https://github.com/a3ip-standard/packages/raw/main/ai-standup-assistant/ai-standup-assistant-v1.0.0.a3ip.bundle`
- cowork-backlog: `https://github.com/a3ip-standard/packages/raw/main/cowork-backlog/cowork-backlog-v1.0.0.a3ip.bundle`

## Adding a package

1. Build your package per the [A3IP spec](https://github.com/a3ip-standard/spec)
   and produce a `.a3ip.bundle` using the [a3ip CLI](https://github.com/a3ip-standard/cli)
   (`a3ip bundle <package_dir>`).
2. Create a directory `<package-name>/` at this repo's root.
3. Copy your bundle into it as `<package-name>-v<version>.a3ip.bundle`.
4. Add a short `<package-name>/README.md` so visitors can understand the
   package without unpacking the bundle.
5. Append an entry to `registry.yaml` following the schema documented
   at the top of that file.
6. Open a pull request.
