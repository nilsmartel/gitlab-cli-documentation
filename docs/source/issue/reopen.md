# `glab issue reopen`

Reopen a closed issue.

## Synopsis

You can use a full GitLab URL instead of an ID.

```plaintext
glab issue reopen [<id> | <url>] [flags]
```

## Aliases

```plaintext
open
```

## Examples

```console
glab issue reopen 123
glab issue open 123
glab issue reopen https://gitlab.com/NAMESPACE/REPO/-/issues/123
```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
