# `glab dependency-firewall maven`

Run Maven through the GitLab Dependency Firewall. (EXPERIMENTAL)

## Synopsis

Run the Maven binary (`mvn`) through the GitLab Dependency Firewall. The command checks each package download and upload against the policy for the current project, refuses blocked packages, and summarizes the results after the run.

The command uses your package manager's registry or index configuration, and does not modify it.

All arguments are forwarded to `mvn` verbatim.

This feature is an experiment and is not ready for production use.
It might be unstable or removed at any time.
For more information, see
<https://docs.gitlab.com/policy/development_stages_support/>.

```plaintext
glab dependency-firewall maven <mvn args> [flags]
```

## Examples

```console
# Build a project through the Dependency Firewall
glab dependency-firewall maven verify

```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
