# `glab dependency-firewall uv`

Run uv through the GitLab Dependency Firewall. (EXPERIMENTAL)

## Synopsis

Run the uv binary through the GitLab Dependency Firewall. The command checks each package download and upload against the policy for the current project, refuses blocked packages, and summarizes the results after the run.

The command uses your package manager's registry or index configuration, and does not modify it.

All arguments are forwarded to `uv` verbatim.

This feature is an experiment and is not ready for production use.
It might be unstable or removed at any time.
For more information, see
<https://docs.gitlab.com/policy/development_stages_support/>.

```plaintext
glab dependency-firewall uv <uv args> [flags]
```

## Examples

```console
# Install a package through the Dependency Firewall
glab dependency-firewall uv pip install requests

```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
