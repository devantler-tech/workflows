# TODOs Action

A composite action that scans your repository for TODO comments and automatically creates corresponding GitHub issues for improved task tracking. It authenticates API access, locates TODOs with file and line references, and can optionally add issues to a specified GitHub Project.

## Usage

### Standard TODO scanning

Scan for TODOs and create issues without project integration:

```yaml
steps:
  - name: Create issues from TODOs
    uses: devantler-tech/github-actions/composite-actions/todos-action@{ref} # ref
    with:
      APP_ID: ${{ vars.APP_ID }}
      APP_PRIVATE_KEY: ${{ secrets.APP_PRIVATE_KEY }}
```

### TODO scanning with project integration

Scan for TODOs and add created issues to a GitHub Project:

```yaml
steps:
  - name: Create issues from TODOs
    uses: devantler-tech/github-actions/composite-actions/todos-action@{ref} # ref
    with:
      APP_ID: ${{ vars.APP_ID }}
      APP_PRIVATE_KEY: ${{ secrets.APP_PRIVATE_KEY }}
      PROJECT: "organization/my-org/1"
```

## Inputs

| Key               | Type  | Default | Required | Description                     |
| ----------------- | ----- | ------- | -------- | ------------------------------- |
| `APP_ID`          | Input | -       | ✅        | GitHub App ID                   |
| `APP_PRIVATE_KEY` | Input | -       | ✅        | GitHub App Private Key          |
| `PROJECT`         | Input | -       | ❌        | GitHub Project to add issues to |

---

[← Go back to main README](../../README.md#composite-actions)
