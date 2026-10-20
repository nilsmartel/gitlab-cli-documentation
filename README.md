# GLab

GLab is an open source GitLab CLI tool. It brings GitLab to your terminal, next to where you are already working with `git` and your code, without switching between windows and browser tabs. While it's powerful for issues and merge requests, `glab` does even more:

- View, manage, and retry CI/CD pipelines directly from your CLI.
- Create changelogs.
- Create and manage releases.
- Ask GitLab Duo Chat (Classic) questions about Git.
- Manage GitLab agents for Kubernetes.

`glab` is available for repositories hosted on GitLab.com, GitLab Dedicated, and GitLab Self-Managed. It supports multiple authenticated GitLab instances, and automatically detects the authenticated hostname from the remotes available in your working Git directory.

## Requirements

`glab` officially supports GitLab versions 16.0 and later. Certain commands might require
more recent versions. While many commands might work properly in GitLab versions
15.x and earlier, no support is provided for these versions.

## Usage

To get started with `glab`:

1. Follow the [installation instructions](#installation) appropriate for your operating system.
1. [Authenticate](#authentication) into your instance of GitLab.
1. Optional. Configure `glab` further to meet your needs:
   - 1Password users can configure it to [authenticate to `glab`](https://developer.1password.com/docs/cli/shell-plugins/gitlab/).
   - Set any needed global, per-project, or per-host [configuration](#configuration).
   - Set any needed [environment variables](#environment-variables).

You're ready!

### Commands

Run `glab --help` to view a list of core commands in your terminal.

- [`glab alias`](docs/source/alias): Create, list, and delete aliases.
- [`glab api`](docs/source/api): Make an authenticated request to the GitLab API.
- [`glab artifact-registry`](docs/source/artifact-registry): Authenticate with GitLab Artifact Registry. (EXPERIMENTAL)
- [`glab attestation`](docs/source/attestation): Manage software attestations. (EXPERIMENTAL)
- [`glab auth`](docs/source/auth): Manage authentication for glab.
- [`glab changelog`](docs/source/changelog): Generate changelogs from your project's commit history.
- [`glab check-update`](docs/source/check-update): Check for the latest glab version.
- [`glab ci`](docs/source/ci): Work with GitLab CI/CD pipelines and jobs.
- [`glab cluster`](docs/source/cluster): Manage GitLab Agents for Kubernetes and their clusters.
- [`glab completion`](docs/source/completion): Generate shell completion scripts.
- [`glab config`](docs/source/config): Manage glab settings.
- [`glab container-registry`](docs/source/container-registry): Work with GitLab container registries.
- [`glab dependency-firewall`](docs/source/dependency-firewall): Configure and monitor GitLab Dependency Firewall for local package managers. (EXPERIMENTAL)
- [`glab deploy-key`](docs/source/deploy-key): Manage deploy keys.
- [`glab duo`](docs/source/duo): Work with GitLab Duo.
- [`glab govern`](docs/source/govern): Manage AI agent governance. (EXPERIMENTAL)
- [`glab gpg-key`](docs/source/gpg-key): Manage GPG keys registered with your GitLab account.
- [`glab incident`](docs/source/incident): Work with GitLab incidents.
- [`glab issue`](docs/source/issue): Work with GitLab issues.
- [`glab iteration`](docs/source/iteration): Retrieve iteration information.
- [`glab job`](docs/source/job): Work with GitLab CI/CD jobs.
- [`glab label`](docs/source/label): Manage project and group labels.
- [`glab milestone`](docs/source/milestone): Manage group or project milestones.
- [`glab mr`](docs/source/mr): Create, view, and manage merge requests.
- [`glab opentofu`](docs/source/opentofu): Work with the OpenTofu or Terraform integration.
- [`glab orbit`](docs/source/orbit): Query the GitLab Orbit context graph. (EXPERIMENTAL)
- [`glab packages`](docs/source/packages): Manage packages in the GitLab package registry.
- [`glab release`](docs/source/release): Manage GitLab releases.
- [`glab repo`](docs/source/repo): Work with GitLab repositories and projects.
- [`glab runner`](docs/source/runner): Manage GitLab CI/CD runners.
- [`glab runner-controller`](docs/source/runner-controller): Manage runner controllers. (EXPERIMENTAL)
- [`glab schedule`](docs/source/schedule): Work with GitLab CI/CD schedules.
- [`glab search`](docs/source/search): Search for code and resources in a GitLab project. (BETA)
- [`glab securefile`](docs/source/securefile): Manage secure files for a project.
- [`glab security`](docs/source/security): Manage GitLab security scan profiles for a project. (EXPERIMENTAL)
- [`glab skills`](docs/source/skills): Manage glab agent skills. (EXPERIMENTAL)
- [`glab snippet`](docs/source/snippet): Create snippets.
- [`glab ssh-key`](docs/source/ssh-key): Manage SSH keys registered with your GitLab account.
- [`glab stack`](docs/source/stack): Create, manage, and work with stacked diffs. (EXPERIMENTAL)
- [`glab todo`](docs/source/todo): Manage your to-do list.
- [`glab token`](docs/source/token): Manage personal, project, or group tokens.
- [`glab user`](docs/source/user): Interact with a GitLab user account.
- [`glab variable`](docs/source/variable): Manage variables for a GitLab project or group.
- [`glab version`](docs/source/version): Show version information for glab.
- [`glab whatsnew`](docs/source/whatsnew): Show release notes for new versions of glab.
- [`glab work-items`](docs/source/work-items): Manage work items. (EXPERIMENTAL)

Commands follow this pattern:

```shell
glab <command> <subcommand> [flags]
```

Many core commands also have sub-commands. Some examples:

- List merge requests assigned to you: `glab mr list --assignee=@me`
- List review requests for you: `glab mr list --reviewer=@me`
- Approve a merge request: `glab mr approve 235`
- Create an issue, and add milestone, title, and label: `glab issue create -m release-2.0.0 -t "My title here" --label important`

### GitLab Duo for the CLI

The GitLab CLI also includes support for using the GitLab Duo Agent Platform directly in your terminal.

Use `glab duo cli` to ask GitLab Duo questions about your codebase and to autonomously perform actions on your behalf.

For more information, see [GitLab Duo CLI](https://docs.gitlab.com/user/gitlab_duo_cli/).

## Documentation

Read the [documentation](docs/source/_index.md) for usage instructions or check out `glab help`.

## Installation

Download a binary suitable for your OS at the [releases page](https://gitlab.com/gitlab-org/cli/-/releases).
Other installation methods depend on your operating system.

### Homebrew

Homebrew is the officially supported package manager for macOS, Linux, and Windows (through [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install))

- Homebrew
  - Install with: `brew install glab`
  - Update with: `brew upgrade glab`

### Other installation methods

Other options to install the GitLab CLI that may not be officially supported or are maintained by the community are [also available](docs/installation_options.md).

## Authentication

To authenticate `glab` with OAuth, a personal access token, or a CI job token, see
[Authenticate with GitLab](docs/source/authentication.md).

## Configuration

For configuration levels, the configuration search order, and platform-specific file
locations, see [Configure the CLI](docs/source/configuration.md).

For connecting to a GitLab Self-Managed or GitLab Dedicated instance, and for mTLS and
self-signed certificates, see
[Connect to your GitLab instance](docs/source/connection.md).

For authenticating proxies, including custom HTTP headers and Google Identity-Aware
Proxy, see [Connect through a proxy](docs/source/proxies.md).

## Environment variables

`glab` reads its configuration from environment variables as well as the configuration
file. Every configuration key has a matching variable, and the variable wins over the
stored value. Setting them centrally is a good way to give everyone in an organization
the same setup.

For the full reference, see
[Environment variables](docs/source/configuration.md#environment-variables).
For how `glab` picks which token to use, see
[Token precedence](docs/source/authentication.md#token-precedence).

### Debugging

When the `GLAB_DEBUG` environment variable is set to `true`, `glab` outputs more logging information, including:

- Underlying Git commands.
- Expanded aliases.
- DNS error details.

## Troubleshooting

For help with common authentication issues, see
[Troubleshooting](docs/source/authentication.md#troubleshooting) in the GitLab CLI documentation.
