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

