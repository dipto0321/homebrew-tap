# dipto0321/homebrew-tap

Homebrew tap for [dipto0321/nodeup](https://github.com/dipto0321/nodeup).

## Install

```bash
brew install dipto0321/tap/nodeup
```

## How this is maintained

This tap is **automatically managed** by
[GoReleaser](https://goreleaser.com/) on every `v*.*.*` tag push to
`dipto0321/nodeup`. Do not edit formulas by hand — your changes will
be overwritten on the next release.

The pipeline is configured in
[`.goreleaser.yaml`](https://github.com/dipto0321/nodeup/blob/main/.goreleaser.yaml)
under the `brews:` section. Required secret on the nodeup repo:
`HOMEBREW_TAP_TOKEN` (fine-grained PAT with `contents:write` on this
repo).
