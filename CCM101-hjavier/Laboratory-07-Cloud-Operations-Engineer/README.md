# Laboratory 7: Cloud Operations Engineer

## Mission Overview
<2-3 sentences in your words: you acted as an SRE at CloudNova, checked host health, deployed Nginx, generated traffic, and analyzed logs and metrics.>

## Objectives
- Monitor host CPU, memory, and disk with Linux tools
- Deploy a web container and track performance with Docker metrics
- Generate traffic and extract access logs
- Document results in Markdown
- Expand the GitHub Cloud Computing Portfolio

## Monitoring Commands Executed
| Command | Purpose |
|---------|---------|
| `free -h` | Check RAM usage |
| `df -h` | Check disk capacity |
| `top` | View processes and CPU load |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploy Nginx container |
| `curl http://localhost:8080` | Simulate successful user requests |
| `curl http://localhost:8080/hidden-admin-page` | Trigger a 404 error |
| `docker logs client-website` | View application logs |
| `docker stats` | View real-time container metrics |

## Skills Learned
- <your own list: e.g., reading memory/disk output, generating test traffic, finding HTTP status codes in logs, reading container metrics>