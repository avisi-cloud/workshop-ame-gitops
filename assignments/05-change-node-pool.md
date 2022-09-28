# 5. Change node pool

Modify a node pool within your cluster. You can do this from the [Console](https://console.avisi.cloud).

## Tasks

- Switch the node pool type from `t3.medium` to `t3.large`.
- Observe the replacement of nodes within your cluster. What happens when a node is being replaced?
- Add a label to your node pool.

## References

- [docs.avisi.cloud](https://docs.avisi.cloud/docs/how-to/scale-node-pool/#modifying-node-type)

### Modifying node type

Changing the node type within a pool results in a full node pool replacement. Any missing nodes will first be provisioned before replacing existing nodes, similarly to how the scaling up works, if you modify both the node type and count within the same action.

### Node Labels/Annotations

Labels and annotations will not result in a node replacement and will be configured within a couple of minutes on each node within a pool. Be careful with modifying existing labels when using these for affinity rules within Kubernetes, as this could result in pods being moved around the cluster.

Labels starting with the following suffix cannot be configured:

- `k8s.avisi.cloud`
- `kubernetes.io`
