# 1. Create Cluster

We are going to create a new cluster. For this we first have to create an `environment`. Once this is done, you can create a new cluster using the [Console](https://console.avisi.cloud). You can use our [how-to create a new cluster](https://docs.avisi.cloud/docs/how-to/how-to-create-a-new-cluster/) as a reference.

**Make sure you use the organisation AME-Techday**

On the create cluster page, you can enter the following information:

- Select the Cloud Provider `AWS`, use as region `eu-west-1`.
- For `version`, select the stable channel `v1.23-stable`.
- Name: enter your cluster name
- Configure a node pool with the name `workers`, type `t3.large` and size `3`.

## References

- [docs.avisi.cloud Console](https://docs.avisi.cloud/product/console/)
- [how-to create a new cluster](https://docs.avisi.cloud/docs/how-to/how-to-create-a-new-cluster/)

### Example 

Here is an example:

![create cluster example](/img/create-cluster-example.png)

## Next assignment

[02. Configure acloud](/assignments/02-configure-acloud.md)
