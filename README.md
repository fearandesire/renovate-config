# fearandesire Renovate preset

Shared, secret-free Renovate policy for active repositories owned by
`fearandesire`.

## Use

Add this repository-level configuration on the default branch:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>fearandesire/renovate-config"]
}
```

The preset is deliberately quiet. Pull requests open only for **major** updates and for **security fixes**:

- Minor, patch, digest, pin and lockfile-maintenance updates are off.
- Major updates open as PRs (at most three at a time, Monday mornings) and are never auto-merged.
- Security fixes are labelled `security` and wait for approval on the Dependency Dashboard, so they cost one tick instead of a PR you did not ask for. Renovate cannot filter them by severity.
- Replacement updates wait for approval on the Dependency Dashboard.

This matches the `charyon` org preset (`renovate/default.json` in `charyon/repository-kit`).

Repository configuration can add narrow overrides. Do not weaken required
checks or introduce tokens, credentials, or host rules into this public preset.

## Validate

```bash
npx --yes --package renovate renovate-config-validator default.json
```
