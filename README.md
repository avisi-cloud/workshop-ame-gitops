# Workshop Avisi Managed Environments & GitOps

![Avisi Cloud Logo](/img/avisi-cloud-logo-black.png)

This repository contains instructions for the AME & GitOps workshop. In this workshop you will manage a cluster's lifecycle, deploy node pools, work with FluxCD & GitOps and more.

## Workshop

### Assigments

- [01. Create cluster](assignments/01-create-cluster.md)
- [02. Configure acloud](assignments/02-configure-acloud.md)
- [03. view audit log](assignments/03-view-audit-log.md)
- [04. Install fluxcd](assignments/04-install-fluxcd.md)
- [05. Change node pool](assignments/05-change-node-pool.md)
- [06. Connect to application](assignments/06-connect-to-application.md)
- [07. Configure grafana](assignments/07-configure-grafana.md)
- [08. Upgrade cluster](assignments/08-upgrade-cluster.md)
- [09. Create snapshots](assignments/09-create-snapshots.md)
- [10. Cluster Lifecycle](assignments/10-cluster-lifecycle.md)

### References

- [docs.avisi.cloud](https://docs.avisi.cloud)
- [kubernetes.io](https://kubernetes.io)
- [Avisi Cloud Console](https://console.avisi.cloud)

### Installed tooling

#### kubectl

```bash
brew install kubectl
```

*[Install kubectl on MacOS](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)*


#### fluxcd

```bash
brew install fluxcd/tap/flux
```

*[Install fluxcd](https://fluxcd.io/flux/installation/)*

#### acloud & acloud-toolkit

```bash
brew install avisi-cloud/tools/acloud avisi-cloud/tools/acloud-toolkit
```

*[Install acloud](https://docs.avisi.cloud/references/acloud/)*

---

### Avisi Cloud

Avisi Cloud Kubernetes is a Kubernetes platform with built-in compliance and day-2 operational tooling.

[![Avisi Cloud CNCF member](/img/avisi-cloud-cncf-member.jpeg)](https://www.avisi.nl/en-gb/blog/avisi-is-trotse-silver-member-van-cncf?__hstc=205717955.b5eb8201cfb102e5a1051fa1bc9bbd78.1656488150292.1663879770786.1664302257949.30&__hssc=205717955.4.1664302257949&__hsfp=2607337039)

## License

[MIT](LICENSE)
