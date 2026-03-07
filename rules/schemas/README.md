# Schemas

Schemas for validating rule packages and catalog manifests live here.

Validation should happen before any downloaded package becomes active in a local
installation.

Files:

- `package-manifest.schema.json`
- `catalog.schema.json`

These schemas are descriptive references for catalog/package authors today.
Runtime validation in `agent-safe-guard` is enforced in native code and should
stay compatible with these schema files.
