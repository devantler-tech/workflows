# Flux GitOps Deploy Action

Push Kubernetes manifests to OCI and deploy them using Flux. This action packages your manifests into an OCI artifact, uploads it to GitHub Container Registry, sets up cluster authentication with kubeconfig, and triggers Flux CD to reconcile and deploy the new manifests to the specified environment.

## Usage

Deploy to a development cluster for testing:

```yaml
steps:
  - name: Deploy with GitOps
    uses: devantler-tech/github-actions/composite-actions/flux-gitops-deploy-action@{ref} # ref
    with:
      DEPLOYMENT_ENV: "dev"
      KUBE_CONFIG: ${{ secrets.KUBE_CONFIG }}
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| Key              | Type  | Default | Required | Description                        |
| ---------------- | ----- | ------- | -------- | ---------------------------------- |
| `DEPLOYMENT_ENV` | Input | -       | ✅        | Deployment environment (dev, prod) |
| `KUBE_CONFIG`    | Input | -       | ✅        | Kubeconfig for the target cluster  |
| `GITHUB_TOKEN`    | Input | -       | ✅         | Token for accessing GHCR            |

---

[← Go back to main README](../../README.md#composite-actions)
