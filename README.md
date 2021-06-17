# helm-efk
Some sample helm chart for the efk stack

## fluentd


## Elastic


## Kibana

Connect to the Kibana dashboard:
```bash
kubectl -n default port-forward svc/helm-efk-kibana 5601:5601
```

