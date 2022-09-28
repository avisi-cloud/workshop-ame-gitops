# 9. Create snapshots

Creating and managing back-ups for persistent data within a Kubernetes cluster is extremly important. There are multiple strategies and back-up tools available within Kubernetes. The easiest solution to use within AME Kubernetes is by using `VolumeSnapshots`. Using our `acloud-toolkit` CLI tool you can easily create and restore snapshots of volumes.

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
