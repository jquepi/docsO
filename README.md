This repository contains the documentation for [Octopus Deploy](https://octopus.com/docs).

Contributions to help improve this documentation are welcome, however, you must sign the [Contribution License Agreement (CLA)](https://cla-assistant.io/OctopusDeploy/docs) before we can accept your contribution.

See the [Octopus style guide](https://style.octopus.com) for information including:

* [Markdown quick reference](https://style.octopus.com/markdown)
* [Capitalization](https://style.octopus.com/capitalization)
* [Working with images](https://style.octopus.com/images)
* [Predefined snippets to include in your text](https://style.octopus.com/octopus-snippets)

## How to contribute a change to the docs

* Fork this repo and create a branch for your changes.
* Make the changes you'd like to contribute.
* Submit a pull request (PR) to master with your changes and include a comment explaining the changes.
* Sign the [Contribution License Agreement (CLA)](https://cla-assistant.io/OctopusDeploy/docs).
* We'll review your PR and accept it or suggest changes.

## Deploying to preview environment (Octopus Developers)

Before merging to `master` it's possible you'd like to see your changes in a preview environment. It's simple to do this:

1. Navigate to TeamCity.
1. Find the build configuration for the environment you want to preview the changes in. They live under the `Octofront / CPT` project and the build configuration will be prefixed with `Docs`.
1. Select `Run...` and choose your branch to build the docs and deploy it to the preview environment.
1. Make a note of the preview environment base url (this is available in the build-configuration description) and then preview your changes using that url.

**Note:** You may need to refresh the preview environment several times as various caching layers are invalidated. It may take a minute or two between when the pipeline completes and your changes
become visible.

> For more detailed information about the build process and preview environments, take a look at the [internal documentation](https://octopushq.atlassian.net/wiki/spaces/CPT/pages/49718/How+docs+works) (private link).