# homebrew-shield

Homebrew tap for [shield](https://github.com/chinmaymjog/shield-go), a git
pre-commit hook that scans staged changes for secrets (gitleaks +
trufflehog) before they're committed.

The `Formula/shield.rb` file in this repo is generated and pushed
automatically by [goreleaser](https://goreleaser.com) whenever a new tag is
released from the [shield-go](https://github.com/chinmaymjog/shield-go)
repo. Don't hand-edit it — changes will be overwritten on the next release.

## Install

```sh
brew tap chinmaymjog/homebrew-shield
brew trust chinmaymjog/homebrew-shield  # one-time, newer Homebrew versions require this for new taps
brew install chinmaymjog/homebrew-shield/shield
shield install   # activates the pre-commit hook — see shield-go's README
```

## Upgrade / uninstall

```sh
brew upgrade shield
```

```sh
shield uninstall   # run this first, while `shield` is still on PATH
brew uninstall shield
```

See [shield-go](https://github.com/chinmaymjog/shield-go) for what
`install`/`uninstall` actually do, how scanning works, and how to fork this
for your own org.
