# helm-efk
Some sample helm chart for the efk stack

## fluentd


## Elastic


## Kibana

Connect to the Kibana dashboard:
```bash
kubectl -n default port-forward svc/helm-efk-kibana 5601:5601
```

### Export/Import objects from kibana

```
GET http://localhost:5601/api/saved_objects/_find?type=index-pattern
```
```
GET http://localhost:5601/api/saved_objects/_find?type=search
```
```
GET http://localhost:5601/api/saved_objects/_find?type=dashboard
```

### Helm Chart Repo Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

helm repo add helm-efk https://jwindhaber.github.io/helm-efk

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo
<alias>` to see the charts.

To install the efk chart:

    helm install my-efk helm-efk/efk

To uninstall the chart:

    helm delete my-efk
