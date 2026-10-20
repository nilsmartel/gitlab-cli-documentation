# `glab auth configure-docker`

Register glab as a Docker credential helper.

## Synopsis

Configures Docker to use glab for authentication with GitLab
container registries. This command runs only on Linux and macOS.

After you run this command, Docker uses glab to obtain credentials
when it pulls from or pushes to a GitLab container registry.

Docker looks for the credential helper script by name on your `PATH`. By default, glab installs the script next to the glab binary. If that directory is not writable, glab falls back to `~/.local/bin`, then to any other writable directory on your `PATH`. If the script lands in a directory that is not on your `PATH`, glab tells you which directory to add.

```plaintext
glab auth configure-docker [flags]
```

## Examples

```console
# Configure Docker to use glab for GitLab container registry authentication
glab auth configure-docker

```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
