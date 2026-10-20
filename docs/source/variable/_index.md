# `glab variable`

Manage variables for a GitLab project or group.

## Synopsis

Variables store configuration and secrets used by CI/CD pipelines.

Each subcommand acts on the current project by default. Use
`--group` to manage a group's variables instead.

## Aliases

```plaintext
var
```

## Options

```plaintext
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```

## Subcommands

- [`delete`](delete.md)
- [`export`](export.md)
- [`get`](get.md)
- [`import`](import.md)
- [`list`](list.md)
- [`set`](set.md)
- [`update`](update.md)
