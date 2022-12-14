---
title: Nexus Hosted Maven repository
description: Configuring a Nexus Hosted Maven repository as an Octopus feed.
position: 10
---
Both Nexus OSS and Nexus Pro offer three types of Maven repository, Hosted, Group, and Proxy.  This guide will cover creating a Hosted Maven repository and adding it as an External Feed in Octopus Deploy.

:::info
This guide was written using Nexus OSS version 3.37.0-01
:::


## Configuring a Hosted Maven repository

From the Nexus web portal, click on the **gear icon** to get to the **Administration** screen.

![Administration gear Icon](../images/nexus-nuget-administration.png)

Click on **Repositories**

![Repositories](../images/nexus-repositories.png)

Click **Create repository**

![Create repository](../images/nexus-create-repository.png)

Choose **maven2 (hosted)** from the list of repositories to create

![Maven (hosted)](images/nexus-maven-repository.png)

Give the repository a name and change any applicable configuration options.  Click **Create repository** when you are done.

![Create repository](images/nexus-create-maven-repository.png)

When the repository has been created, click on the entry in the list to bring up the repository properties.

![MyNexusMavenRepo](images/nexus-mynexusmavenrepo.png)

Copy the URL property, that is what you will use when adding it as an external feed

![Repository URL](images/nexus-maven-url.png)

Optionally upload a package to the repository so you can verify search functionality when added as an external feed.

## Adding a Nexus Maven repository as an Octopus External Feed
Create a new Octopus Feed by navigating to **{{Library, External Feeds}}** and select the `Maven Feed` Feed type. 

Give the feed a name and in the URL field, paste the URL you copied earlier.  It should look similar to this format:

`https://your.nexus.url/repository/[repository name]`

![Nexus NuGet feed](images/nexus-maven-feed.png)