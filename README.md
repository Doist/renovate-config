# renovate-config

Shareable Renovate config templates - https://docs.renovatebot.com/config-presets/

## Usage

In a repository, create a `.github/renovate.json` file and extend any of our configuration option like this:

```json
{
    "extends": [
        "github>todoist/renovate-config:integrations-base",
        "github>todoist/renovate-config:integrations-automerge"
    ]
}
```

For debugging, register into the [Renovate Dashboard](https://app.renovatebot.com/dashboard) where you can see detailed error messages from your runs.

These references resolve from this repository's default branch (`main`). The nested
presets also use the default branch; pinning only a consumer's top-level preset does
not pin those nested references. Keep preset filenames, including `doist-base`,
unchanged when migrating consumers to the `todoist` owner. Merge the shared presets
after the organization rename and before resuming dependent Renovate runs.

The public presets do not configure registry routing or credentials. Public-only
npm consumers can use npmjs. Consumers of private `@todoist/*` packages must also extend
`github>todoist/renovate-config-internal:npm-registry-token`, which routes the scope
to GitHub Packages, and give Renovate access to that private preset and the required
packages, including public mirrors. Verify new package versions and access before
resuming their updates. Maven coordinates such as `com.doist` and `com.todoist` are
product identifiers and remain unchanged.

## Validation

With Node.js 24.11 or later in the Node.js 24 release line, run the standalone
[configuration validator](https://docs.renovatebot.com/config-validation/):

```sh
npm exec --yes --ignore-scripts --package=renovate@44.221.4 -- renovate-config-validator --no-global *.json
```

This validates the local files without running dependency updates. It can report
existing configuration migration notices. It does not verify remote preset
availability, resolve the full top-level `extends` graph, or prove registry access;
check those separately before enabling consumers under the new owner.

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
