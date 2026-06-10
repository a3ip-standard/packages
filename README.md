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

## Installing a package

Give your A3IP-aware AI the `.a3ip.bundle` URL or the file itself, and
ask it to install the package. The AI follows the spec's bundle preamble
and the `INSTALL.md` inside the bundle.

Example URLs (from the registry):

- a3ip-creator: `https://github.com/a3ip-standard/packages/raw/main/a3ip-creator/a3ip-creator-v3.0.0.a3ip.bundle`
- ai-code-review-flow: `https://github.com/a3ip-standard/packages/raw/main/ai-code-review-flow/ai-code-review-flow-v1.4.1.a3ip.bundle`

## Adding a package

1. Build your package per the [A3IP spec](https://github.com/a3ip-standard/spec)
   and produce a `.a3ip.bundle` using the [a3ip CLI](https://github.com/a3ip-standard/cli)
   (`a3ip bundle <package_dir>`).
2. Create a directory `<package-name>/` at this repo's root.
3. Copy your bundle into it as `<package-name>-v<version>.a3ip.bundle`.
4. Append an entry to `registry.yaml` following the schema documented
   at the top of that file.
5. Open a pull request.
