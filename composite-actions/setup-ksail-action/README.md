# Setup KSail Action

Installs the KSail CLI via Homebrew, a tool for managing Kubernetes clusters with simplicity and a developer-friendly experience. This action ensures Homebrew is available, adds the DevantlerTech formulas repository, and installs the latest KSail CLI, enabling simplified cluster operations, GitOps workflows, and local development cluster management.

## Usage

Install the latest KSail CLI via Homebrew:

```yaml
steps:
  - name: Setup KSail CLI
    uses: devantler-tech/github-actions/composite-actions/setup-ksail-action@{ref} # ref
```

---

[← Go back to main README](../../README.md#composite-actions)
