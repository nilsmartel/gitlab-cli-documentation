# `glab auth logout`

Log out from a GitLab instance.

## Synopsis

Logs out from a GitLab instance. The credentials for the specified instance
are removed from the global configuration file (default
`~/.config/glab-cli/config.yml`) and from the operating system's keyring,
if a token was stored there.

```plaintext
glab auth logout [flags]
```

## Examples

```console
# Log out of a specific instance
glab auth logout --hostname gitlab.example.com

```

## Options

```plaintext
      --hostname string   The hostname of the GitLab instance.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
