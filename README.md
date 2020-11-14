# Docker Kubernetes Prometheus Grafana NodeJS Application Monitoring
```
docker-compose up -d --build nodejs-application
```

## Start Prometheus, Grafana & Dashboards

```
docker-compose up -d prometheus
docker-compose up -d grafana
docker-compose up -d grafana-dashboards
```


## Generate some requests by opening the application in the browser

```
http://localhost:83 #NodeJS
```

## Check Dashboards
```
http://localhost:3000

```
## Prometheus Queries

Requests per Second over 2minutes
```
irate(go_request_operations_total[2m])
```
Request duration
```
rate(go_request_duration_seconds_sum[2m]) / rate(go_request_duration_seconds_total[2m])
```