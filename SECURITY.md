# Security Policy

## Reporting a vulnerability

**Do not open a public issue, discussion, or pull request for a security
problem.** Public disclosure before a fix exists puts every user at risk.

Use GitHub's private vulnerability reporting, which is enabled on every
repository in this account:

1. Go to the affected repository.
2. Open the **Security** tab.
3. Choose **Report a vulnerability**.

That opens a private advisory visible only to you and the maintainers, and it
is the only channel we monitor for undisclosed issues. If private reporting is
somehow unavailable to you, open a public issue containing **only** the words
"requesting a security contact" — no details — and we will open a private
advisory and invite you to it.

## What to include

A report we can act on immediately contains:

- The affected repository and version, or commit SHA.
- What an attacker gains — the impact, stated plainly.
- Reproduction steps, ideally a minimal test case or command.
- Your assessment of severity, and any suggested fix.

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement | within 72 hours |
| Initial assessment | within 7 days |
| Fix or documented mitigation | within 90 days |
| Public advisory + credit | when the fix ships |

You will be credited in the advisory by whatever name or handle you choose,
unless you ask to stay anonymous. We will not involve legal counsel over a
good-faith report.

## Scope

**In scope** — anything in a repository under this account: the shipped code,
build and release workflows, and the published artifacts.

**Out of scope** — GitHub's own infrastructure, third-party services, results
from automated scanners without a demonstrated impact, missing hardening
headers on the documentation site, and denial of service that requires
privileged local access.

## Verifying what you run

Every release ships a `checksums.txt` alongside the binaries. Verify before you
trust:

```bash
sha256sum -c checksums.txt --ignore-missing
```

Release tags are signed. Commits on `main` are signed and the branch requires
signed commits.

## Supported versions

Until a project reaches `v1.0.0`, only the latest minor release receives
security fixes. After `v1.0.0`, the current and previous minor releases are
supported.
