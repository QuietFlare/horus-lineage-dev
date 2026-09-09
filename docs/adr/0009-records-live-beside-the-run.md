# ADR 0009: Records live beside the run

Status: accepted

## Context

ADR 0002 makes the run directory the unit but does not say where it
goes. 0.1.0 wrote to `~/.horus-lineage/` on the launch host, with
`HORUS_LINEAGE_DIR=@run` as an opt-in for the workflow's run directory.

The first cluster run showed the cost: results under the project,
lineage in a home directory on the login node, read together only by
collecting from both.

## Decision

Records go under the workflow's run directory by default:

    <run-directory>/.horus-lineage/<run>/

That is the directory Horus resolves for the orchestrator target, so
lineage moves, archives and is deleted with the results it describes.

`HORUS_LINEAGE_DIR` set to an absolute path sends records elsewhere,
for purgeable scratch or a slow filesystem. `@run` stays as a name for
the default.

## Consequences

Readers of `~/.horus-lineage/` look in the run directory instead. This
is the breaking change in 0.2.0.

A purged run directory takes its records with it. Records that outlive
their results describe files nobody can check, so that is the trade.
