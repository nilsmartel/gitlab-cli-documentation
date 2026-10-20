# `glab auth docker-helper`

A Docker credential helper for GitLab container and artifact registries.

## Synopsis

Responds to Docker credential helper requests for GitLab container
registries and Artifact Registries. Docker invokes this command
automatically.

```plaintext
glab auth docker-helper [flags]
```

## Examples

```console
# Docker invokes the helper automatically; supported actions are 'store', 'get', and 'erase'.
# Retrieve the stored credentials for a registry:
echo registry.gitlab.com | glab auth docker-helper get
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
