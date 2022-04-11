# renovate-config

Shareable Renovate config templates - https://docs.renovatebot.com/config-presets/

## Usage

In a repo, create a `.github/renovate.json` file. See [example](https://github.com/Doist/app-console/blob/main/.github/renovate.json).

## Integrations

|Template|Purpose|
|-|-|
|`integrations-base.json`|The base policies we apply to all repos.|
|`integrations-automerge.json`|Default automerge policy.|
|`integrations-npm-token.json`|Encrypted token to pull packages from GitHub-hosted NPM.|
|`integrations-scheduled.json`|The default updates schedule. Use if real-time updates are overwhelming in a specific repo.|
