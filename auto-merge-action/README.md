# Auto Merge Action

Composite action to approve and auto-merge PRs from specific bots/users. This action automatically approves pull requests and enables auto-merge for trusted sources like Dependabot, Renovate, and specific maintainers. It generates an authenticated token using GitHub App credentials, automatically approves the pull request, and enables auto-merge with squash strategy.

## Usage

```yaml
steps:
  - name: Auto-merge PR
    uses: devantler-tech/github-actions/composite-actions/auto-merge-action@{ref} # ref
    with:
      app_id: ${{ vars.APP_ID }}
      app_private_key: ${{ secrets.APP_PRIVATE_KEY }}
      github_token: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| Key               | Type  | Default | Required | Description            |
| ----------------- | ----- | ------- | -------- | ---------------------- |
| `app_id`          | Input | -       | ✅        | GitHub App ID          |
| `app_private_key` | Input | -       | ✅        | GitHub App Private Key |
| `github_token`    | Input | -       | ✅        | GitHub Token           |

---

[← Go back to main README](../README.md#composite-actions)
