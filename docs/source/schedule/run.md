# `glab schedule run`

Trigger a pipeline schedule to run immediately.

## Synopsis

Trigger a CI/CD pipeline schedule, identified by its numeric ID, to
run immediately. The schedule's normal recurrence is not affected;
this is a one-time, on-demand run in addition to the configured cron.

By default, the schedule is run in the current project. Use `--repo`
to target another project.

```plaintext
glab schedule run <id> [flags]
```

## Examples

```console
# Run the schedule with ID 1 immediately
glab schedule run 1

# Run a schedule in another project
glab schedule run 1 -R owner/repo

```

## Options inherited from parent commands

```plaintext
  -h, --help          Show help for this command.
  -R, --repo string   Select another repository. You can use either OWNER/REPO or GROUP/NAMESPACE/REPO. The full URL or Git URL is also accepted.
```
