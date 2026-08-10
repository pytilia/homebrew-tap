# Pytilia Homebrew Tap

Homebrew formulae for Pytilia tools.

## convoy-cli

```sh
brew install pytilia/tap/convoy-cli
```

This installs the `convoy` command. To authenticate docker with the Convoy
registry:

```sh
convoy docker login
```

### Upgrade

```sh
brew update && brew upgrade convoy-cli
```

### Shell completion

```sh
convoy --install-completion
```

## Maintenance

Formulae and release artifacts in this repository are published automatically
by CI in the (private) `pytilia/convoy` repository — do not edit `Formula/` by
hand. To release a new version, bump `version` in `cli/pyproject.toml` there
and merge to `main`.

## Licensing

The formula files in this repository are MIT-licensed (see LICENSE). The
software they install (artifacts attached to Releases) is proprietary,
© Pytilia Ltd.
