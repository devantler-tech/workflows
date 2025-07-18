# Cleanup GHCR Action

Clean up old GitHub Container Registry (GHCR) packages. This action helps maintain your registry by removing outdated container images and keeping only the specified number of tagged images. It removes container images older than the specified duration, preserves the specified number of most recent tagged images, and helps reduce storage costs while maintaining a clean registry.

## Usage

### Basic cleanup (default settings)

Uses default retention policy of 1 year for old images and keeps 10 tagged images:

```yaml
steps:
  - name: Cleanup old GHCR packages
    uses: devantler-tech/github-actions/composite-actions/cleanup-ghcr-action@{ref} # ref
```

### Custom retention policy

Specify custom duration and number of images to keep:

```yaml
steps:
  - name: Cleanup old GHCR packages
    uses: devantler-tech/github-actions/composite-actions/cleanup-ghcr-action@{ref} # ref
    with:
      older-than: "3 months"
      keep-n-tagged: "15"
```

## Inputs

| Key             | Type  | Default  | Required | Description                            |
| --------------- | ----- | -------- | -------- | -------------------------------------- |
| `older-than`    | Input | `1 year` | ❌        | Delete images older than this duration |
| `keep-n-tagged` | Input | `10`     | ❌        | Number of tagged images to keep        |

---

[← Go back to main README](../../README.md#composite-actions)
