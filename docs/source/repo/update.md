# `glab repo update`

Update an existing GitLab project or repository.

## Synopsis

Change project settings such as the description or default branch, or
archive and unarchive the project with `--archive`.

```plaintext
glab repo update [path] [flags]
```

## Examples

```console
# Update the description for my-project.
glab repo update my-project --description "This project is cool."

# Update the default branch for my-project.
glab repo update my-project --defaultBranch main

# Archive my-project.
glab repo update my-project --archive
glab repo update my-project --archive=true

# Unarchive my-project.
glab repo update my-project --archive=false
```

## Options

```plaintext
      --archive                Whether the project should be archived.
      --defaultBranch string   New default branch for the project.
  -d, --description string     New description for the project.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```
