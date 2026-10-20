# `glab container-registry repository delete`

Delete a container registry repository.

## Synopsis

This action permanently deletes the repository and all images and tags
published to it.

```plaintext
glab container-registry repository delete <repository-id> [flags]
```

## Aliases

```plaintext
del
```

## Examples

```console
# Delete a container registry repository with a confirmation prompt
glab container-registry repository delete 123

# Skip the confirmation prompt
glab container-registry repository delete 123 --yes
```

## Options

```plaintext
  -y, --yes   Skip the confirmation prompt.
```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
