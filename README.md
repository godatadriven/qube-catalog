# qube-catalog

Published post-quantum cryptography knowledge catalog for
[Qube](https://github.com/godatadriven/xdnl-qube).

> **Generated - do not edit here.**
> The source of truth is `src/qube/catalog/data/` in `godatadriven/xdnl-qube`.
> This repository is written by CI on every push to that repo's `main` branch.
> Edits made directly here will be overwritten without warning.

## Endpoint

Qube's `qube catalog update` fetches these files over plain HTTPS with no
credentials:

```
https://godatadriven.github.io/qube-catalog/v1/services.yaml
https://godatadriven.github.io/qube-catalog/v1/policies.yaml
https://godatadriven.github.io/qube-catalog/v1/algorithms.yaml
```

## Versioning

Two independent version axes:

- **`v1/` path segment** - the catalog *schema* version.
  A breaking schema change is published under a new prefix (`v2/`) so existing
  clients keep resolving the format they understand.
- **`version:` inside each file** - the *content* version.
  `qube catalog update` compares this against the copy embedded in the installed
  package and merges only when the remote is newer.

## Files

| File | Contents |
|------|----------|
| `v1/services.yaml` | Per-AWS-service PQC support, recommended policies, migration effort, impact notes |
| `v1/policies.yaml` | TLS/security policy classifications (`pqc_ready`, key exchange, TLS versions) |
| `v1/algorithms.yaml` | NIST-aligned algorithm reference (FIPS 203/204/205), sizes, quantum-safety |

## Licence

MIT, matching the upstream project.
