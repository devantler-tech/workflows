# Dockerfile Lint Action

Lint Dockerfiles using Hadolint. This action performs static analysis on your Dockerfiles to ensure they follow best practices and security guidelines. It recursively scans all Dockerfiles in your repository, checks for Docker best practices and common mistakes, identifies potential security issues, and ensures consistent formatting and structure.

## Usage

Automatically finds and lints all Dockerfiles in your repository:

```yaml
steps:
  - name: Lint Dockerfiles
    uses: devantler-tech/github-actions/composite-actions/dockerfile-lint-action@{ref} # ref
```

---

[← Go back to main README](../../README.md#composite-actions)
