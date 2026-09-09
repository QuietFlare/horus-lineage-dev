# Contributing

```bash
uv sync --group dev
make test
make lint
make type-check
```

Decisions live in `docs/adr/`. Read 0005 before touching the record
shape: a semantic change is a new format version, never an edit.

Rules the tests enforce:

- The plugin never fails a run. A recorder error is logged and dropped
  (ADR 0004).
- One file per task, written when the task finishes (ADR 0002).
- Records carry paths, digests and the command line, nothing else.

Keep commits brief, one change each. Put the reasoning in the pull
request. Docstrings are one line, two at most.
