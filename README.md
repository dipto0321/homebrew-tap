# dipto0321/homebrew-tap

Homebrew tap for [dipto0321/nodeup](https://github.com/dipto0321/nodeup).

## Install

```bash
brew install dipto0321/tap/nodeup
```

## How this is maintained

This tap is **automatically managed** by
[GoReleaser](https://goreleaser.com/) on every `v*.*.*` tag push to
`dipto0321/nodeup`. Do not edit the cask by hand — your changes will
be overwritten on the next release.

The pipeline is configured in
[`.goreleaser.yaml`](https://github.com/dipto0321/nodeup/blob/main/.goreleaser.yaml)
under the `homebrew_casks:` section. Required secret on the nodeup
repo: `HOMEBREW_TAP_TOKEN` (fine-grained PAT with `contents:write` on
this repo).

## Formula → cask

`nodeup` shipped as a Homebrew **formula** up to v1.2.1 and switched
to a **cask** in v1.2.2. The install command is unchanged, but
Homebrew treats a formula and a cask as different packages.

If you installed the formula, run:

```bash
brew uninstall --formula nodeup
brew install dipto0321/tap/nodeup
```

`tap_migrations.json` lets Homebrew perform that hand-off for you
automatically on `brew update` — it unlinks the old keg and installs
the cask in its place.

The cask also strips the macOS Gatekeeper quarantine attribute after
install. Without that, macOS refuses to run the unsigned binary at
all (the process is killed before `main()` starts), so `nodeup` would
appear to do nothing.
