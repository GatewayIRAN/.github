## What this changes

<!-- One paragraph. What behaviour is different after this merges? -->

## Why

<!-- The problem being solved. Link the issue: Closes #123 -->

## How to verify

<!-- Exact commands a reviewer runs to see it work. Not "run the tests". -->

```bash

```

## Checklist

- [ ] Commits are signed off (`git commit -s`) — the DCO check enforces this
- [ ] Commit messages follow Conventional Commits
- [ ] `gofmt -l .` prints nothing
- [ ] `go vet ./...` is clean
- [ ] `go test ./...` passes
- [ ] Tests cover the change; a bug fix has a regression test
- [ ] Documentation updated in this same pull request if behaviour changed
- [ ] No new third-party dependency, or the description below justifies it
- [ ] Nothing new phones home

## Anything a reviewer should push back on

<!-- Shortcuts taken, assumptions made, parts you are unsure about.
     Naming these gets the review you actually want. -->
