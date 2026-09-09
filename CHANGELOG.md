# Changelog

## 0.2.0 - 2026-09-09

Breaking: records now go under the workflow's run directory,
`<run-directory>/.horus-lineage/<run>/`, instead of `~/.horus-lineage/`.
Set `HORUS_LINEAGE_DIR` to an absolute path to keep the old location.
`HORUS_LINEAGE_DIR=@run` now names the default. See ADR 0009.

- Test that a YAML workflow is copied into the run directory.
- ADRs 0001, 0002 and 0005 are accepted.
- Release workflow can publish: trusted publishing permissions and a
  full checkout for the version tag.
- CI runs on pushes to main.
- Add SECURITY.md, CONTRIBUTING.md, dependabot and an issue template.

## 0.1.0 - 2026-09-03

First release: four recording middlewares, `conformance`, and the
optional `report` behind `HORUS_LINEAGE_REPORT`.
