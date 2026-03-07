# agent-safe-guard-rules

Curated rule packages for `agent-safe-guard`.

This repository is the source of truth for the shared rule set maintained by
`regen-dev`.

Operating model:

- rules are proposed through pull requests
- accepted rules are committed to `main`
- local `agent-safe-guard` installations sync metadata from GitHub and decide
  locally which packages or rules are enabled
- policy activation remains local; this repo publishes rule content, not runtime
  decisions

For now, all repository content lives under [`rules/`](rules/README.md).
