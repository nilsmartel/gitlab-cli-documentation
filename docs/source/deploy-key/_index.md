# `glab deploy-key`

Manage deploy keys.

## Synopsis

Add, list, get, and delete the deploy keys for a project.

Deploy keys grant access to a repository over SSH without being tied to a
user account, and are commonly used by CI/CD jobs and external systems.
These commands operate on the current project. Use `--repo` to target
another project.

## Options

```plaintext
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```

## Subcommands

- [`add`](add.md)
- [`delete`](delete.md)
- [`get`](get.md)
- [`list`](list.md)
