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