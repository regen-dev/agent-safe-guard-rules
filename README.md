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

Current catalog entrypoint for the curated first-party set:

- [`rules/catalogs/github-core.json`](rules/catalogs/github-core.json)
- Published immutable bootstrap URL:
  `https://raw.githubusercontent.com/regen-dev/agent-safe-guard-rules/rules-v0.2.0/rules/catalogs/github-core.json`

Current first-party core packages:

- `command-defense`
- `output-defense`
- `read-defense`
- `approval-defense`
- `agent-defense`
- `telemetry`
- `memory-defense`

Typical local development flow with a checkout on the same machine:

```bash
asg-cli --catalog-add /home/wendel/src/agent-safe-guard-rules/rules/catalogs/github-core.json
asg-cli --catalog-sync
asg-cli --catalog-search command
```

Published bootstrap flow:

```bash
asg-cli --catalog-add https://raw.githubusercontent.com/regen-dev/agent-safe-guard-rules/rules-v0.2.0/rules/catalogs/github-core.json
asg-cli --catalog-sync
asg-cli --catalog-search command
```
