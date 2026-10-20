# `glab config set`

Updates configuration with the value of a given key.

## Synopsis

Use `glab config set --global` to write to the global configuration.
Specifying the `--host` flag also saves to the global configuration file.

```plaintext
glab config set <key> <value> [flags]
```

## Examples

```console
glab config set editor vim
glab config set token xxxxx --host gitlab.com
glab config set check_update false --global
```

## Options

```plaintext
  -g, --global        Write to global '~/.config/glab-cli/config.yml' file rather than the repository's '.git/glab-cli/config.yml' file.
      --host string   Set per-host setting.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
