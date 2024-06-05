# registry-renovate-config

Base Renovate configuration for Mason registries.

## Usage

Create a `renovate.json` file in a Mason registry containing:
```json
{
    "extends": ["github>mason-org/registry-renovate-config"]
}
```

## Defaults

### Automerge

This Renovate configuration is configured to automatically enable auto-merge for pull requests. This requires the "Allow
auto-merge" setting to be enabled in the repository to function.

### Enabled managers

Only the `regex` manager is enabled. This effectively means that Renovate will only look for updates for
Mason package definitions inside `packages/`. If you want to use other Renovate managers in the same project you'll need
to [override the `enabledManagers` field](https://docs.renovatebot.com/modules/manager/).

### Renovate dashboard

This Renovate configuration is configured to create a dependency dashboard issue. Override `dependencyDashboard` to
`false` if you want to disable this.
