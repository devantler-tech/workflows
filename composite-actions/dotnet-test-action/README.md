# .NET Test Action

Test .NET solutions or projects across multiple platforms with code coverage reporting. This action installs the .NET 9 SDK, configures NuGet sources (including GHCR for private packages), restores dependencies, runs tests with coverage collection, and uploads reports to Codecov.

## Usage

### Standard .NET testing with coverage

Test .NET projects with code coverage reporting:

```yaml
steps:
  - name: Test .NET project
    uses: devantler-tech/github-actions/composite-actions/dotnet-test-action@{ref} # ref
    with:
      app_id: ${{ vars.APP_ID }}
      app_private_key: ${{ secrets.APP_PRIVATE_KEY }}
      github_token: ${{ secrets.GITHUB_TOKEN }}
      codecov-token: ${{ secrets.CODECOV_TOKEN }}
```

### Testing in specific directory

Run tests for projects in a specific directory:

```yaml
steps:
  - name: Test .NET project
    uses: devantler-tech/github-actions/composite-actions/dotnet-test-action@{ref} # ref
    with:
      app_id: ${{ vars.APP_ID }}
      app_private_key: ${{ secrets.APP_PRIVATE_KEY }}
      github_token: ${{ secrets.GITHUB_TOKEN }}
      working-directory: "src/MyProject"
```

### Testing without coverage upload

Run tests without uploading coverage to Codecov:

```yaml
steps:
  - name: Test .NET project
    uses: devantler-tech/github-actions/composite-actions/dotnet-test-action@{ref} # ref
    with:
      app_id: ${{ vars.APP_ID }}
      app_private_key: ${{ secrets.APP_PRIVATE_KEY }}
      github_token: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| Key                 | Type  | Default | Required | Description                              |
| ------------------- | ----- | ------- | -------- | ---------------------------------------- |
| `app_id`            | Input | -       | ✅        | GitHub App ID to generate a token        |
| `app_private_key`   | Input | -       | ✅        | Private key of the GitHub App            |
| `github_token`      | Input | -       | ✅        | GitHub token to access the repository    |
| `codecov-token`     | Input | -       | ❌        | Token to upload code coverage to CodeCov |
| `working-directory` | Input | `.`     | ❌        | Directory to run the tests in            |

---

[← Go back to main README](../../README.md#composite-actions)
