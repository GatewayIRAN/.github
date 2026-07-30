<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)"  srcset="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/banner-light.svg">
  <img alt="GatewayIRAN — open-source infrastructure tools, small, sharp, documented" src="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/banner-light.svg" width="100%">
</picture>

<br><br>

[![License](https://img.shields.io/badge/license-Apache--2.0-2A44B4?style=for-the-badge&labelColor=0D1117)](https://www.apache.org/licenses/LICENSE-2.0)
[![Releases](https://img.shields.io/badge/releases-attested-2A44B4?style=for-the-badge&labelColor=0D1117)](https://github.com/GatewayIRAN/.github#reusable-workflows)
[![Commits](https://img.shields.io/badge/commits-signed-2A44B4?style=for-the-badge&labelColor=0D1117)](#how-this-is-built)
[![Telemetry](https://img.shields.io/badge/telemetry-none-17A34A?style=for-the-badge&labelColor=0D1117)](#how-this-is-built)

</div>

<br>

## Projects

| | | Status |
|---|---|---|
| **[certway](https://github.com/GatewayIRAN/certway)** | Get a TLS certificate in one command | ![in design](https://img.shields.io/badge/in%20design-3455D8?style=flat-square&labelColor=0D1117) |
| **[.github](https://github.com/GatewayIRAN/.github)** | Shared health files and reusable CI and release workflows | ![live](https://img.shields.io/badge/live-17A34A?style=flat-square&labelColor=0D1117) |

<br>

## certway

Getting a TLS certificate should be one command that either works, or tells you
exactly why it did not.

<div align="center">
<img src="https://raw.githubusercontent.com/GatewayIRAN/certway/main/assets/flow-dark.svg#gh-dark-mode-only" alt="Order, prove control over HTTP, TLS-ALPN or DNS, receive the certificate" width="94%">
<img src="https://raw.githubusercontent.com/GatewayIRAN/certway/main/assets/flow-light.svg#gh-light-mode-only" alt="Order, prove control over HTTP, TLS-ALPN or DNS, receive the certificate" width="94%">
</div>

<br>

> [!IMPORTANT]
> **certway is in design.** The interface, the scope and the documentation are
> settled; there is no release to install yet. The repository says so on its
> front page rather than implying otherwise — read the
> [scope](https://github.com/GatewayIRAN/certway#scope) and tell us where it is
> wrong.

<br>

## How this is built

> [!NOTE]
> Every repository here follows the same rules. No exceptions, no "we will get
> to it later".

- **Reproducible builds.** The same tag produces the same bytes, so anyone can
  rebuild a release and compare.
- **Attested releases.** Every artefact ships with a checksum manifest and a
  signed provenance statement tying it to the commit and workflow that built it.
- **Signed commits.** `main` requires them, and unsigned commits attributed to
  this account are flagged as unverified.
- **Actions pinned to commit SHAs.** A tag can be moved under you; a digest
  cannot.
- **No telemetry.** Nothing phones home. No analytics, no version pings, no
  crash uploads.
- **Documentation is part of done.** An undocumented flag is an unfinished flag.
- **Apache-2.0** everywhere. Permissive, with an explicit patent grant. One
  licence across every project, because a mixed licence set is a signal of
  carelessness.
- **Honest status badges.** `in design` stays until there is something worth
  downloading.

<br>

## Contributing

Contributions are welcome from anyone, anywhere.

- Read [CONTRIBUTING.md](https://github.com/GatewayIRAN/.github/blob/main/CONTRIBUTING.md)
- Sign off your commits with `git commit -s` — we use DCO, not a CLA
- Start with issues labelled [`good first issue`](https://github.com/search?q=owner%3AGatewayIRAN+label%3A%22good+first+issue%22+state%3Aopen&type=issues)
- Questions and design feedback belong in
  [Discussions](https://github.com/GatewayIRAN/.github/discussions), not issues

<br>

## Security

Found a vulnerability? **Do not open a public issue.**
Use [private vulnerability reporting](https://github.com/GatewayIRAN/certway/security/advisories/new)
and read the [policy](https://github.com/GatewayIRAN/.github/blob/main/SECURITY.md) first.

<br>

<div align="center">

<img src="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/rule.svg" alt="" width="100%">

<sub>Apache-2.0 · No trackers · No accounts required · Maintained by <a href="https://github.com/MrAryanMiri">@MrAryanMiri</a></sub>

</div>
