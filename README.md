# renovate-config

Shareable Renovate config templates - https://docs.renovatebot.com/config-presets/

## Usage

In a repository, create a `.github/renovate.json` file and extend any of our configuration option like this:

```json
{
    "extends": [
        "github>doist/renovate-config:integrations-base",
        "github>doist/renovate-config:integrations-automerge"
    ]
}
```

For debugging, register into the [Renovate Dashboard](https://app.renovatebot.com/dashboard) where you can see detailed error messages from your runs.

## Configurations Overview

| Template                      | Purpose                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------- |
| **Integrations**              |                                                                                             |
| `integrations-base.json`      | The base policies we apply to all repos.                                                    |
| `integrations-automerge.json` | Default automerge policy.                                                                   |
| `integrations-scheduled.json` | The default updates schedule. Use if real-time updates are overwhelming in a specific repo. |
| **Android**                   |                                                                                             |
| `android-base.json`           | The base configuration for our Android repositories.                                        |
| **Kotlin**                    |                                                                                             |
| `kotlin-base.json`            | The base configuration for our Kotlin repositories, including Kotlin Multiplatform.         |
| **Frontend**                  |                                                                                             |
| `frontend-base.json`          | The base configuration for all Frontend repositories.                                       |
| **Backend**                   |                                                                                             |
| `backend-base.json`           | The base configuration for our Backend repositories.                                       |
