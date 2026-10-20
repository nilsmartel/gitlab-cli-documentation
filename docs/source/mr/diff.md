# `glab mr diff`

View changes in a merge request.

## Synopsis

Defaults to the currently checked-out branch. Use `--color=never`
to disable color output.

For automated scripts or patch tools, use `--raw` for an unmodified Git patch.

```plaintext
glab mr diff [<id> | <branch>] [flags]
```

## Examples

```console
glab mr diff 123
glab mr diff branch

# Get merge request from current branch
glab mr diff

glab mr diff 123 --color=never
```

## Options

```plaintext
      --color string   Use color in diff output: always, never, auto. (default "auto")
      --raw            Use raw diff format that can be piped to commands.
```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
