# Contributing

Contributions are welcome from anyone, anywhere. This file applies to every
repository under [@GatewayIRAN](https://github.com/GatewayIRAN) unless a
repository overrides it.

## Before you start

- Search [existing issues](https://github.com/search?q=org%3AGatewayIRAN&type=issues) first.
- For anything larger than a bug fix, open an issue and agree on the approach
  before writing code. It saves both of us a wasted afternoon.
- Issues labelled `good first issue` are deliberately scoped small.

## Ground rules

**Every commit must be signed off.** We use the
[Developer Certificate of Origin](https://developercertificate.org/), not a CLA
— no legal paperwork, just one trailer line:

```bash
git commit -s -m "fix(core): reject an empty SNI value"
```

That appends `Signed-off-by: Your Name <your@email>`. The DCO check enforces it.

**Cryptographic signing is encouraged.** SSH signing is the least painful route:

```bash
git config gpg.format ssh
git config user.signingkey ~/.ssh/id_ed25519.pub
git config commit.gpgsign true
```

**Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/).**
The release notes are generated from them, so the format is load-bearing:

```
feat(cli): add a --dns-provider flag
fix(core): retry a stale nonce instead of failing the order
docs(readme): document the renewal threshold
chore(deps): bump actions/checkout to v4.2.2
perf(store): stop re-reading the account key per order
refactor(solver): extract the challenge server
test(order): cover the wildcard path
```

Allowed types: `feat`, `fix`, `docs`, `chore`, `perf`, `refactor`, `test`, `build`, `ci`, `revert`.

## Workflow

1. Fork, then branch from `main`. Name it `feat/short-thing` or `fix/short-thing`.
2. Make the change. Add or adjust tests — a bug fix without a regression test
   will be asked for one.
3. Run whatever local gate the repository documents before pushing — formatter,
   linter, tests. If CI runs it, run it locally first.

4. Open a pull request against `main`. Fill in the template; "see title" is not
   a description.
5. CI must be green and the branch must be linear. `main` requires a pull
   request, passing checks, and no force pushes — that applies to maintainers too.

## What gets merged

- Small and reviewable beats large and impressive. Split big changes.
- Public API changes need a documentation change in the same pull request.
  Undocumented means unfinished.
- New third-party dependencies need a justification. The default answer is
  whatever ships with the platform already.
- No telemetry, no analytics, no phoning home. This is not negotiable.

## What we will not merge

- Reformatting unrelated files alongside a functional change.
- Vendored binaries or generated artifacts committed by hand.
- Changes that silently widen a permission, scope, or attack surface.

## Reporting a security issue

Do **not** open a public issue. See [SECURITY.md](SECURITY.md).
