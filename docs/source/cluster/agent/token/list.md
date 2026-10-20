# `glab cluster agent token list`

List tokens for a GitLab Agent for Kubernetes.

## Synopsis

Lists all tokens for the specified agent. Requires the numeric agent ID.

```plaintext
glab cluster agent token list <agent-id> [flags]
```

## Examples

```console
# List tokens for agent 123
glab cluster agent token list 123

# List tokens in JSON format
glab cluster agent token list 123 --output json
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
