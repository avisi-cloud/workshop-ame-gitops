# 6. Connect to application

After finishing assignment 4, a reverse proxy (ingress-nginx) and loadbalancer have been provisioned within your cluster. You can verify this by checking the running pods within the `nginx-ingress` namespace in your cluster:

```bash
kubectl -n nginx-ingress get pods
```

You can find the `LoadBalancer` by running the following kubectl command:

```bash
kubectl -n nginx-ingress get svc
```

You will find output similar to this:

```bash
NAME                                             TYPE           CLUSTER-IP      EXTERNAL-IP                                                                     PORT(S)                      AGE
nginx-ingress-ingress-nginx-controller           LoadBalancer   172.16.40.136   b46e8a98b4ab3391a98541a8624abd5d-6fec4f4d0c82b5aa.elb.eu-west-1.amazonaws.com   80:32313/TCP,443:30198/TCP   1d
nginx-ingress-ingress-nginx-controller-metrics   ClusterIP      172.16.14.72    <none>                                                                          10254/TCP                    1d
nginx-ingress-ingress-nginx-defaultbackend       ClusterIP      172.16.8.214    <none>                                                                          80/TCP                       1d
```

Copy the address of the `LoadBalancer` and visit it through your Browser to connect to the application deployed in assignement 4.

## References

- [kubernetes.io](https://kubernetes.io/docs/concepts/services-networking/service/#loadbalancer)
- [ingress-nginx](https://kubernetes.github.io/ingress-nginx/)

## Next assignment

[07. Configure grafana](/assignments/07-configure-grafana.md)
