# Container Observability

## Application Log: 404 Error


Application logs record every request and error with a timestamp, status code, and requested path, so they show exactly what happened when something breaks. Without them, troubleshooting would be guesswork, but with them I can quickly find the failing request and trace it to its cause.

![Docker Logs](screenshots/docker-logs.png)

## Container Metrics (docker stats)
| Metric | Value |
|--------|-------|
| Container | client-website |
| CPU % | 0.00% |
| Memory Usage | 2.754MiB |

![Container Metrics](screenshots/container-metrics.png)