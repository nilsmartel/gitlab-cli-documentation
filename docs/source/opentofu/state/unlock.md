# `glab opentofu state unlock`

Unlock the given state.

## Synopsis

Unlocking a state releases a lock held on it, so others can modify
the state again.

```plaintext
glab opentofu state unlock <state> [flags]
```

## Examples

```console
glab opentofu state unlock production
```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
