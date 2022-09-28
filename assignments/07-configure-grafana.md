# 7. Configure Grafana

Using [Grafana](https://grafana.avisi.cloud) you are able to view the metrics and log events generated within your cluster. At this time, we do not automatically configure your Grafana instance to work with newly created clusters (this is on our roadmap).

By creating access tokens for your Observability data, you are able to configure Grafana with a new datasource to gain insight into your cluster.

## Tasks

- Find Observability configuration for your cluster
- Create access Token for Grafana Datasource
- Add Grafana Datasource
- View Dashboards in Grafana

## References

- [Add a grafana datasource](https://grafana.com/docs/grafana/latest/datasources/add-a-data-source/)
- [Grafana datasource management](https://grafana.com/docs/grafana/latest/administration/data-source-management/)

### Create access token

1. Select create new access token
2. Fill out the following details:
    - Name: grafana
    - IP Whitelisting: 0.0.0.0/0 (default)
    - Allowed Scopes: Configure the scope that this token has access to.
3. Select create token
    > Pay attention: Make sure you copy this token to your clipboard, because you'll need it in a few steps.
4. Click continue

## Next assignment

[08. Upgrade cluster](/assignments/08-upgrade-cluster.md)
