---
title: Service
description:  Start, stop, install and configure the Octopus service.
position: 190
---

Use this to configure and manage your Octopus service.

**Service options**

```text
Usage: octopus.server service [<options>]

Where [<options>] is any of:

      --start                Start the service if it is not already running
      --stop                 Stop the service if it is running
      --restart              Restart the service if it is running
      --reconfigure          Reconfigure the service
      --install              Install the service
      --username, --user=VALUE
                             Username to run the service under
                               (DOMAIN\Username format for Windows). Only used
                               when --install or --reconfigure are used.  Can
                               also be passed via an environment variable
                               OCTOPUS_SERVICE_USERNAME. Defaults to 'root' for
                               Systemd services.
      --uninstall            Uninstall the service
      --password=VALUE       Password for the username specified with --
                               username. Only used when --install or --
                               reconfigure are used. Can also be passed via an
                               environment variable OCTOPUS_SERVICE_PASSWORD.
      --dependOn=VALUE
      --instance=VALUE       Name of the instance to use, or * to use all
                               instances

Or one of the common options:

      --help                 Show detailed help for this command
```

## Basic examples

This example restarts the Octopus Server service for the instance `MyNewInstance`:

```text
octopus.server service --restart --instance="MyNewInstance"
```

This example starts the Octopus Server service for the default instance:

```text
octopus.server service --start
```

This example stops all Octopus Server instances on the machine:

```text
octopus.server service --stop --instance=*
```
