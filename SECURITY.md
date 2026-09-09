# Security Policy

## Supported versions

Security fixes land on the latest release. Upgrade before reporting.

## Reporting a vulnerability

Do not open a public issue for a security problem. Report it privately:

- [Open a private security advisory](https://github.com/QuietFlare/horus-lineage/security/advisories/new)
  on this repository (preferred).
- Email [quietflare.co@gmail.com](mailto:quietflare.co@gmail.com).

Include the impact you believe it has, the versions of horus-lineage and
horus-runtime, and a minimal workflow that reproduces it.

## What to expect

An acknowledgement within a week, then an agreed fix and disclosure
timeline, and credit in the advisory if you want it.

## Scope note

The plugin records paths, digests and the resolved command line, and
never command output, file contents, or executor and target settings.
See Sharing in the README. A record that carries more than that is a
vulnerability, report it the same way.

Dependencies are audited with pip-audit and the tree is scanned with
gitleaks on every push and pull request.
