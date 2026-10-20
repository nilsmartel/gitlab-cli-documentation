# `glab gpg-key`

Manage GPG keys registered with your GitLab account.

## Synopsis

Add, list, get, and delete the GPG keys associated with your account.

GitLab uses GPG keys to verify the signatures on signed commits and tags.

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
