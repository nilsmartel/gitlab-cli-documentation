# `glab job`

Work with GitLab CI/CD jobs.

## Synopsis

Inspect CI/CD jobs from a pipeline. Download the artifacts a job
produced with `job artifact`.

Use `--repo` to target a project other than the current one.

## Options

```plaintext
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```

## Options inherited from parent commands

```plaintext
  -h, --help   Show help for this command.
```

## Subcommands

- [`artifact`](artifact.md)
