# SecureMyVPS — namespace registry

Canonical list of **owned**, **reserved**, and **unclaimed** public identifiers for the `securemyvps` project.
Last updated: **2026-11-26** (Phase 0).

Sibling organization: [`vpsinspect`](https://github.com/vpsinspect/.github/blob/main/NAMESPACES.md).

## GitHub

| Asset | Identifier | Status | Notes |
|---|---|---|---|
| GitHub org | [`securemyvps`](https://github.com/securemyvps) | **Owned** | Verified org |
| Primary repo | [`securemyvps/securemyvps`](https://github.com/securemyvps/securemyvps) | **Active** | Go module root, `main` protected |
| Org profile repo | [`securemyvps/.github`](https://github.com/securemyvps/.github) | **Active** | SECURITY.md, org profile, this file |
| Homebrew tap repo | [`securemyvps/homebrew-tap`](https://github.com/securemyvps/homebrew-tap) | **Reserved** | Public repo created 2026-11-26; no formulas until Phase 2 |
| Go module | `github.com/securemyvps/securemyvps` | **Claimed** | Tag `v0.0.1` claims the module proxy index |

## Distribution names

Checked 2026-11-26 by HTTP lookup. "Available" means the registry returned "not found" at that moment;
it is not a reservation — anyone can still claim it.

| Registry | Identifier | Status | Notes |
|---|---|---|---|
| Homebrew | `securemyvps/tap/securemyvps` | **Reserved** | Formula written in Phase 2+; install from `securemyvps/homebrew-tap` |
| npm | `securemyvps`, `@securemyvps/cli` | **Available** | Wrapper deferred; register a private stub before Phase 2 |
| PyPI | `securemyvps` | **Available** | Not used in v1 |
| RubyGems | `securemyvps` | **Available** | Not used in v1 |
| crates.io | `securemyvps` | **Available** | Not used (Go project) |
| Docker Hub | `securemyvps/securemyvps` | **Available** | No OCI image in v1 |
| GHCR | `ghcr.io/securemyvps/securemyvps` | **Available on first push** | Preferred if images ever ship; anonymous lookup returns 401 by design |

## Domains

| Asset | Identifier | Status | Notes |
|---|---|---|---|
| Domain | `securemyvps.com` | **Owned** | DNSSEC / CAA / registrar transfer lock = Step 7 (manual) |

## Typosquat watchlist (do not use)

`secure-my-vps`, `securevps`, `vpssecure`, `secure-vps`

## Maintainer actions

1. Register npm names when the Phase 2 wrapper is approved (private stub only, zero lifecycle scripts).
2. Step 7: DNSSEC + CAA + registrar transfer lock on `securemyvps.com`.
3. Phase 2: add `Formula/securemyvps.rb` to `securemyvps/homebrew-tap` that pulls the signed release assets and verifies `SHA256SUMS.txt`.
