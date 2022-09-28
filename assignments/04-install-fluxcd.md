# 4. Install FluxCD

We will now be installing fluxcd and integrating it with your Kubernetes cluster.

## Tasks

- [Install fluxcd](https://fluxcd.io/flux/installation/) locally (`brew install fluxcd/tap/flux`)
- Fork our examples repository to your own Github profile or organisation.
- Bootstrap fluxcd in your cluster (See below).
- Observe Kubernetes deployments being installed in your cluster (`kubectl get deploy -A`).

## References

- [fluxcd installation](https://fluxcd.io/flux/installation/)
- [Github Fork a Repo](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [Install flux into your cluster](https://fluxcd.io/flux/get-started/#install-flux-onto-your-cluster)

## Examples

### Bootstrap

[flux bootstrap github](https://fluxcd.io/flux/cmd/flux_bootstrap_github/)

```bash
# Create a GitHub personal access token and export it as an env var
export GITHUB_TOKEN=<my-token>

flux bootstrap github \
  --owner=<your user name> \
  --repository=<name of the github repository (fork)> \
  --branch=main \
  --path=clusters/ame-techday \
  --personal
```

The output is similar to:

```bash
► connecting to github.com
✔ repository created
✔ repository cloned
✚ generating manifests
✔ components manifests pushed
► installing components in flux-system namespace
deployment "source-controller" successfully rolled out
deployment "kustomize-controller" successfully rolled out
deployment "helm-controller" successfully rolled out
deployment "notification-controller" successfully rolled out
✔ install completed
► configuring deploy key
✔ deploy key configured
► generating sync manifests
✔ sync manifests pushed
► applying sync manifests
◎ waiting for cluster sync
✔ bootstrap finished
```
