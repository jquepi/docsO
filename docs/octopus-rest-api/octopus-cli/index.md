---
title: The Octopus Command Line (CLI)
description: The Octopus CLI (octo) is the Octopus command line tool that builds on top of the Octopus REST API.
position: 30
hideInThisSection: true
---

!include <octopus-cli>

## Commands {#octoCommandLine-Commands}

`octo` supports the following commands:

- **[allow-releaseprogression](/docs/octopus-rest-api/octopus-cli/allow-releaseprogression.md)**:  Allows a release to progress to the next phase.
- **[build-information](/docs/octopus-rest-api/octopus-cli/build-information.md)**:  Pushes build information to Octopus Server.
- **[clean-environment](/docs/octopus-rest-api/octopus-cli/clean-environment.md)**:  Cleans all Offline Machines from an Environment.
- **[clean-workerpool](/docs/octopus-rest-api/octopus-cli/clean-workerpool.md)**:  Cleans all Offline Workers from a WorkerPool.
- **[complete](/docs/octopus-rest-api/octopus-cli/complete.md)**:  Supports command line auto completion.
- **[create-autodeployoverride](/docs/octopus-rest-api/octopus-cli/create-autodeployoverride.md)**:  Overrides the release that auto deploy will use.
- **[create-channel](/docs/octopus-rest-api/octopus-cli/create-channel.md)**:  Creates a channel for a project.
- **[create-environment](/docs/octopus-rest-api/octopus-cli/create-environment.md)**:  Creates a deployment environment.
- **[create-project](/docs/octopus-rest-api/octopus-cli/create-project.md)**:  Creates a project.
- **[create-release](/docs/octopus-rest-api/octopus-cli/create-release.md)**:  Creates (and, optionally, deploys) a release.
- **[create-workerpool](/docs/octopus-rest-api/octopus-cli/create-workerpool.md)**:  Creates a pool for workers.
- **[delete-autodeployoverride](/docs/octopus-rest-api/octopus-cli/delete-autodeployoverride.md)**:  Deletes auto deploy release overrides.
- **[delete-package](/docs/octopus-rest-api/octopus-cli/delete-package.md)**:  Deletes a package from the built-in NuGet repository in an Octopus Server.
- **[delete-releases](/docs/octopus-rest-api/octopus-cli/delete-releases.md)**:  Deletes a range of releases.
- **[deploy-release](/docs/octopus-rest-api/octopus-cli/deploy-release.md)**:  Deploys a release.
- **[dump-deployments](/docs/octopus-rest-api/octopus-cli/dump-deployments.md)**:  Writes deployments to an XML file that can be imported in Excel.
- **[export](/docs/octopus-rest-api/octopus-cli/export.md)**:  Exports an object to a JSON file. Deprecated. Please see [https://g.octopushq.com/DataMigration](https://g.octopushq.com/DataMigration) for alternative options.
- **[import](/docs/octopus-rest-api/octopus-cli/import.md)**:  Imports an Octopus object from an export file. Deprecated. Please see [https://g.octopushq.com/DataMigration](https://g.octopushq.com/DataMigration) for alternative options.
- **[install-autocomplete](/docs/octopus-rest-api/octopus-cli/install-autocomplete.md)**:  Install a shell auto-complete script into your shell profile, if they aren't already there. Supports pwsh, zsh, bash & powershell.
- **[list-deployments](/docs/octopus-rest-api/octopus-cli/list-deployments.md)**:  Lists a number of deployments by project, environment or by tenant.
- **[list-environments](/docs/octopus-rest-api/octopus-cli/list-environments.md)**:  Lists environments.
- **[list-latestdeployments](/docs/octopus-rest-api/octopus-cli/list-latestdeployments.md)**:  Lists the releases last-deployed in each environment.
- **[list-machines](/docs/octopus-rest-api/octopus-cli/list-machines.md)**:  Lists all machines.
- **[list-projects](/docs/octopus-rest-api/octopus-cli/list-projects.md)**:  Lists all projects.
- **[list-releases](/docs/octopus-rest-api/octopus-cli/list-releases.md)**:  Lists releases by project.
- **[list-tenants](/docs/octopus-rest-api/octopus-cli/list-tenants.md)**:  Lists tenants.
- **[list-workerpools](/docs/octopus-rest-api/octopus-cli/list-workerpools.md)**:  Lists worker pools.
- **[list-workers](/docs/octopus-rest-api/octopus-cli/list-workers.md)**:  Lists all workers.
- **[pack](/docs/octopus-rest-api/octopus-cli/pack.md)**:  Creates a package (.nupkg or .zip) from files on disk, without needing a .nuspec or .csproj.
- **[prevent-releaseprogression](/docs/octopus-rest-api/octopus-cli/prevent-releaseprogression.md)**:  Prevents a release from progressing to the next phase.
- **[promote-release](/docs/octopus-rest-api/octopus-cli/promote-release.md)**:  Promotes a release.
- **[push](/docs/octopus-rest-api/octopus-cli/push.md)**:  Pushes a package (.nupkg, .zip, .tar.gz, .jar, .war, etc.) package to the built-in NuGet repository in an Octopus Server.
- **[push-metadata](/docs/octopus-rest-api/octopus-cli/push-metadata.md)**:  Pushes package metadata to Octopus Server.  Deprecated. Please use the build-information command for Octopus Server 2019.10.0 and above.
- **[run-runbook](/docs/octopus-rest-api/octopus-cli/run-runbook.md)**:  Runs a Runbook.
- **[version](/docs/octopus-rest-api/octopus-cli/version.md)**:  Outputs Octopus CLI version.

## General Usage {#OctopusCLI-GeneralUsage}

All commands take the form of:

```powershell
octo <command> [<options>]
```

You can see a list of commands using:

```powershell
octo help
```

And you can get help for a specific command using:

```powershell
octo help <command>
octo <command> --help
```

Arguments are not case sensitive and can take the following forms:

```powershell
--project OctoFX                # Space between argument name and value
--project=OctoFX                # Equal sign between argument name and value
--project "OctoFX Web Site"     # Argument values with spaces need to be quoted
"--project=OctoFX Web Site"     # If using equals, quote both the name and value, not just the value
```

All commands require you to pass the URL of the Octopus Server's API endpoint, and an API key which is used to authenticate you.

```bash
octo ... --server http://your-octopus-server/ --apiKey API-ABCDEF123456
```

Most commands also support [JSON formatted output](formatted-output.md).

:::success
**Create an API key**
Learn about [how to create an API key](/docs/octopus-rest-api/how-to-create-an-api-key.md).
:::

The server URL, API key, username and password can be set as the environment variables `OCTOPUS_CLI_SERVER`, `OCTOPUS_CLI_API_KEY`, `OCTOPUS_CLI_USERNAME` and `OCTOPUS_CLI_PASSWORD` respectively. Values set via command line arguments take precedence over environment variables.

!include <octo-autocomplete-tabcompletion>
