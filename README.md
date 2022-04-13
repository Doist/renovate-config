# renovate-config

Shareable Renovate config templates - https://docs.renovatebot.com/config-presets/

## Usage

In a repo, create a `.github/renovate.json` file. See [example](https://github.com/Doist/app-console/blob/main/.github/renovate.json).

For debugging, register into the [Renovate Dashboard](https://app.renovatebot.com/dashboard#github/Doist/) where you can see detailed error messages from your runs.

## Integrations

|Template|Purpose|
|-|-|
|`integrations-base.json`|The base policies we apply to all repos.|
|`integrations-automerge.json`|Default automerge policy.|
|`integrations-scheduled.json`|The default updates schedule. Use if real-time updates are overwhelming in a specific repo.|
|`integrations-electron.json`|Rules specific to Electron-based repos.|

## Android

The base configuration for our Android repositories is defined in `android-base.json`.  
