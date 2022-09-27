# 1. Create Cluster

We are going to create a new cluster. For this we first have to create an `environment`. Once this is done, you can create a new cluster using the [Console](https://console.avisi.cloud). You can use our [how-to create a new cluster](https://docs.avisi.cloud/docs/how-to/how-to-create-a-new-cluster/) as a reference.

On the create cluster page, you can enter the following information:

- Select the Cloud Provider `AWS`, use as region `eu-west-1`.
- For `version`, select one of the stable channels (for example: `v1.23-stable`).
- Name: enter your cluster name
- Configure a node pool with the name `workers`, type `t3.large` and size `3`.

### Example 

Here is an example:

![create cluster example](/img/create-cluster-example.png)
