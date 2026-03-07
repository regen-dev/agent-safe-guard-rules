# Catalogs

Catalog manifests generated or maintained for publication live here.

The runtime should sync catalogs from published immutable content, then cache
and activate packages locally.

Current first-party entrypoint:

- `github-core.json`: curated `regen-dev` catalog for the default shared rule
  packages under `../core/`

Publication convention:

- keep package `download_url` values relative to the catalog file when possible
- this keeps the same catalog usable from a local checkout and from a published
  HTTP URL later
- publish first-party bootstrap URLs from tags or releases, not from `main`
