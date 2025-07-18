# Install Flux Action

Installs Flux in a Kubernetes cluster using the Flux CLI. This action verifies cluster prerequisites, deploys Flux CD controllers and CRDs, and prepares the cluster for GitOps-based continuous deployment with all necessary components, including Source Controller, Kustomize Controller, Helm Controller, and Image Automation Controllers.

## Usage

Install Flux CD with default configuration:

```yaml
steps:
  - name: Install Flux CD
    uses: devantler-tech/github-actions/composite-actions/install-flux-action@{ref} # ref
```

---

[← Go back to main README](../../README.md#composite-actions)
