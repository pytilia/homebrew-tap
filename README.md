# Pytilia Homebrew Tap

Homebrew formulae for Pytilia tools.

## goldline-cli

```sh
brew install pytilia/tap/goldline-cli
```

This installs the `goldline` command. To authenticate docker with the Goldline
registry:

```sh
goldline docker login
```

### Upgrade

```sh
brew update && brew upgrade goldline-cli
```

### Shell completion

```sh
goldline --install-completion
```

### Migrating from convoy-cli

The CLI was called `convoy` (formula `convoy-cli`) before version 0.2.0.

```sh
brew update && brew upgrade
```

Homebrew moves an existing `convoy-cli` install to `goldline-cli`. If it does
not, reinstall under the new name:

```sh
brew uninstall convoy-cli && brew install pytilia/tap/goldline-cli
```

The `convoy` command and the `CONVOY_*` environment variables keep working for
now and print a deprecation notice. Switch to `goldline` and `GOLDLINE_*`.

## Maintenance

Formulae and release artifacts in this repository are published automatically
by CI in the (private) `pytilia/convoy` repository — do not edit `Formula/` or
`formula_renames.json` by hand. To release a new version, bump `version` in
`cli/pyproject.toml` there and merge to `main`.

## Licensing

The formula files in this repository are MIT-licensed (see LICENSE). The
software they install (artifacts attached to Releases) is proprietary,
© Pytilia Ltd.
