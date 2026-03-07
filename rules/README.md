# Rules Layout

Everything in this repository is organized under `./rules`.

Current layout:

- `core/`: curated first-party rule packages
- `catalogs/`: catalog manifests published from this repository
  - current canonical catalog: `catalogs/github-core.json`
- `schemas/`: JSON schemas for package and catalog validation

This stays intentionally small until the runtime format is finalized in
`agent-safe-guard`.
