# Install Cilium Action

Installs Cilium as the CNI in a Kubernetes cluster using Helm, with optimized configurations for cloud-native networking and security. This action sets up the official Cilium Helm chart repository, ensures the latest chart version, and deploys Cilium with features like Kubernetes IPAM, kube-proxy replacement, enhanced security contexts, and custom service configuration for localhost API server access.

## Usage

Install Cilium CNI:

```yaml
steps:
  - name: Install Cilium CNI
    uses: devantler-tech/github-actions/composite-actions/install-cilium-action@{ref} # ref
```

---

[← Go back to main README](../README.md#composite-actions)
