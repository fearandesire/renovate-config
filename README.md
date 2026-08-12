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

The preset schedules updates weekly, limits Renovate to five concurrent pull
requests, rebases branches that fall behind, and uses GitHub native auto-merge.
Patch, minor, digest, lockfile-maintenance, and GitHub Actions updates can merge
only after repository protections and required checks pass. Major and
replacement updates require approval through the Dependency Dashboard.

Repository configuration can add narrow overrides. Do not weaken required
checks or introduce tokens, credentials, or host rules into this public preset.

## Validate

```bash
npx --yes --package renovate renovate-config-validator default.json
```
