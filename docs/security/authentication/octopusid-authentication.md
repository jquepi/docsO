---
title: Octopus ID authentication
description: Octopus Deploy can use Octopus accounts to identify users.
position: 30
---

:::hint
Octopus ID authentication is only available in [Octopus Cloud](/docs/octopus-cloud/index.md).
:::

Octopus ID authentication allows you to log in to your Octopus Cloud instance using the same account that you use to sign in at [Octopus.com](https://Octopus.com). This allows you to manage who is able to access your Octopus instance from [your organization](https://Octopus.com/organization/) and saves you time when moving between our website and your instance.

## Inviting users and configuring teams with Octopus ID

After you've used Octopus.com to [invite some other users](/docs/octopus-cloud/index.md#OctopusCloud-Invitingusers) to your instance, you can configure the users with [Teams](/docs/security/users-and-teams/index.md) and [User Roles](/docs/security/users-and-teams/user-roles.md) as you normally would using the product.

## Supported authentication providers

Octopus ID allows you to sign in using the following external authentication providers:

- Google
- Microsoft Azure Active Directory (AAD)
- GitHub

:::hint
Octopus ID does not currently support configuring [external groups and roles](/docs/security/users-and-teams/external-groups-and-roles.md) using any of the authentication providers listed.
:::

### Learn more

- [Invite users via Octopus.com](/docs/octopus-cloud/index.md#OctopusCloud-Invitingusers)
- [Octopus Cloud specific permissions](/docs/octopus-cloud/permissions.md)
- [Octopus Cloud documentation](/docs/octopus-cloud/index.md)