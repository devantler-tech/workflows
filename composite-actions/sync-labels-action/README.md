# Sync Labels Action

Sync GitHub labels across repositories using a configuration file for consistent labeling. This action reads the specified configuration, then creates, updates, or deletes labels to match it, ensuring label names, colors, and descriptions are standardized across all repositories.

The configuration file has the following format:

```yaml
labels:
  - name: "bug"
    color: "d73a4a"
    description: "Something isn't working"
  - name: "enhancement"
    color: "a2eeef"
    description: "New feature or request"
```

## Usage

### Standard label sync with default config

Use the default DevantlerTech label configuration:

```yaml
steps:
  - name: Sync repository labels
    uses: devantler-tech/github-actions/composite-actions/sync-labels-action@{ref} # ref
```

### Custom label configuration

Use your own label configuration file:

```yaml
steps:
  - name: Sync repository labels
    uses: devantler-tech/github-actions/composite-actions/sync-labels-action@{ref} # ref
    with:
      config-file: "https://raw.githubusercontent.com/my-org/configs/main/labels.yaml"
```

### Preserve existing labels

Sync without deleting labels not in the configuration:

```yaml
steps:
  - name: Sync repository labels
    uses: devantler-tech/github-actions/composite-actions/sync-labels-action@{ref} # ref
    with:
      delete-other-labels: "false"
```

## Inputs

| Key                   | Type  | Default                                                                                               | Required | Description                                |
| --------------------- | ----- | ----------------------------------------------------------------------------------------------------- | -------- | ------------------------------------------ |
| `config-file`         | Input | `https://raw.githubusercontent.com/devantler-tech/github-actions/refs/heads/main/.github/labels.yaml` | ❌        | URL or path to the labels config file      |
| `delete-other-labels` | Input | `true`                                                                                                | ❌        | Whether to delete labels not in the config |

---

[← Go back to main README](../../README.md#composite-actions)
