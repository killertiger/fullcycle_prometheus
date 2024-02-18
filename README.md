# Description

[cAdvisor](https://prometheus.io/docs/guides/cadvisor/) - Monitoring docker container metrics using cAdivisor

# Running application

```
$ docker compose up -d
```

## Prometheus

Access url:
http://localhost:9090/

PromQL example:
```
rate(prometheus_http_requests_total{handler="/metrics"}[5m])
```


## cAdvisor

http://localhost:8080/

## Grafana

### Access
http://localhost:3000/
User: admin / admin


### Setup
Add new datasource
prometheus

url: http://prometheus:9090

Recommendation use dashboard:
https://grafana.com/grafana/dashboards/14282-cadvisor-exporter/

Dashboard -> Import -> Dashboard Id: 14282 -> Import