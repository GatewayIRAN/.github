<div align="center">

<img src="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/banner-dark.svg#gh-dark-mode-only" alt="GatewayIRAN" width="100%">
<img src="https://raw.githubusercontent.com/GatewayIRAN/GatewayIRAN/main/assets/banner-light.svg#gh-light-mode-only" alt="GatewayIRAN" width="100%">

<br>

**Shared project health files and issue forms for every GatewayIRAN repository.**

</div>

<br>

## What this repository is

GitHub treats a public repository named `.github` as the fallback for community
health files. Anything here applies automatically to every other repository in
this account that does not define its own copy — so these documents live in one
place and are edited once.

> [!NOTE]
> This is infrastructure, not a product. If you are looking for something to
> install, start at the [profile](https://github.com/GatewayIRAN).

<br>

## What it provides

| File | Applies to | Purpose |
|---|---|---|
| [CONTRIBUTING.md](CONTRIBUTING.md) | every repo | How to propose a change and get it merged |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | every repo | Contributor Covenant 2.1 |
| [SECURITY.md](SECURITY.md) | every repo | How to report a vulnerability privately |
| [SUPPORT.md](SUPPORT.md) | every repo | Which channel answers which question |
| [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE) | every repo | Structured bug, feature and docs forms |
| [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) | every repo | Review checklist |
| [.github/CODEOWNERS](.github/CODEOWNERS) | this repo | Automatic review assignment |
| [.github/dependabot.yml](.github/dependabot.yml) | this repo | Weekly Action updates |
| [.github/release.yml](.github/release.yml) | this repo | Release-note categories |

<br>

## Reusable workflows

Each repository calls these instead of copying a pipeline, so changing a rule
across the whole account means editing one file here.

> [!NOTE]
> Only the language-agnostic workflow is published today. Build, test and
> release pipelines are toolchain-specific, and no project here has committed to
> a toolchain yet — an unused workflow that names one would be a claim the
> repositories do not back up. They land with the first project that needs them.

<details>
<summary><b>Dependency review</b></summary>

<br>

```yaml
name: Dependency review
on: [pull_request]

permissions:
  contents: read

jobs:
  review:
    uses: GatewayIRAN/.github/.github/workflows/reusable-dependency-review.yml@main
```

Fails a pull request that pulls in a dependency with a known vulnerability at
`moderate` severity or above.

</details>

<br>

## Conventions these files assume

- **Apache-2.0** everywhere. One licence across all projects; a mixed licence
  set is a signal of carelessness.
- **DCO, not a CLA.** `git commit -s` is the whole requirement.
- **Conventional Commits.** Release notes are generated from the history, so the
  message format is functional, not cosmetic.
- **Actions pinned to commit SHAs**, never to floating tags. A tag can be moved;
  a SHA cannot.
- **Least-privilege tokens.** Every workflow declares `permissions:` explicitly
  and starts from `contents: read`.
- **Reproducible, attested releases.** When release pipelines land they will
  build with a pinned source date and ship a checksum manifest plus a signed
  provenance statement.
- **No telemetry.** Nothing built here reports usage anywhere.

<br>

<div align="center">
<sub>Apache-2.0 · No trackers · Maintained by <a href="https://github.com/MrAryanMiri">@MrAryanMiri</a></sub>
</div>
