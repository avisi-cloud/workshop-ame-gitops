# 9. Create snapshots

Creating and managing back-ups for persistent data within a Kubernetes cluster is extremly important. There are multiple strategies and back-up tools available within Kubernetes. The easiest solution to use within AME Kubernetes is by using `VolumeSnapshots`. Using our [acloud-toolkit](https://docs.avisi.cloud/references/acloud-toolkit/) CLI tool you can easily create and restore snapshots of volumes.

Install the acloud-toolkit using Brew:

```bash
brew install avisi-cloud/tools/acloud-toolkit
```

## Tasks

- Install `acloud-toolkit`
- Create a `VolumeSnapshot` of a persistent volume (you have created one when completing assignment 4)
- Restore the `VolumeSnapshot` in a different namespace using `acloud-toolkit`

## References

- [Create persistent volume snapshot](https://docs.avisi.cloud/docs/runbooks/create-persistent-volume-snapshots/)
- [acloud-toolkit snapshot create](https://docs.avisi.cloud/references/acloud-toolkit/acloud-toolkit_snapshot_create/)
- [acloud-toolkit snapshot restore](https://docs.avisi.cloud/references/acloud-toolkit/acloud-toolkit_snapshot_restore/)

### Finding persistent volumes

```bash
kubectl get pvc -A
```

```bash
kubectl get pvc -n <namespace>
```

### Finding VolumeSnapshots

```bash
acloud-toolkit snapshot ls -n <namespace>
```

```bash
kubectl get VolumeSnapshot -n <namespace>
```

### Using acloud-toolkit snapshot create

```bash
❯ acloud-toolkit snapshot create -h
create creates a snapshot for a pvc

Usage:
  acloud-toolkit snapshot create <snapshot> [flags]

Examples:

acloud-toolkit snapshot create my-snapshot --pvc my-pvc


Flags:
  -h, --help                    help for create
  -n, --namespace string        If present, the namespace scope for this CLI request. Otherwise uses the namespace from the current Kubernetes context
  -p, --pvc string              Name of the persistent volume to snapshot
  -s, --snapshot-class string   CSI volume snapshot class. If empty, use default volume snapshot class
```
