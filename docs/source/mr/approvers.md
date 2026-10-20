# `glab mr approvers`

List eligible approvers for merge requests in any state.

## Synopsis

Lists users and groups eligible to approve, based on the approval
rules configured for the project.

```plaintext
glab mr approvers [<id> | <branch>] [flags]
```

## Examples

```console
glab mr approvers 123
glab mr approvers branch-name
```

## Options

```plaintext
      --jq string       Filter JSON output with a jq expression.
  -F, --output string   Format output as: text, json. (default "text")
```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
