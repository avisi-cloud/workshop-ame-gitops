# 2. Configure acloud

Most actions can be performed through the [Console](https://console.avisi.cloud). However they can also be done by using our CLI tool [acloud](https://docs.avisi.cloud/product/cli/).

You can use our acloud CLI tool to;

- Manage cluster resources
- Create new environments
- Scale clusters up and down
- Manage clusters lifecycle (create, delete, stop/start)
- Manage our observability tooling

## Tasks

- Try and find your cluster using `acloud`.
- Start a shell using `acloud` so you can use `kubectl` to interact with your cluster.
- List the nodes in the cluster using `kubectl`
- Create a new node pool called `database` for your cluster. Use `t3.medium` for `node-type` and `1` for `node-count`.

## References

- [Acloud introduction](https://docs.avisi.cloud/references/acloud/)

## Next assignment

[03. view Audit log](/assignments/03-view-audit-log.md)
