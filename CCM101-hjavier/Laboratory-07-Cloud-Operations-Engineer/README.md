# Laboratory 7: Cloud Operations Engineer

## Mission Overview
In this laboratory activity, I acted as a Cloud Operations Engineer (SRE) at CloudNova Technologies, preparing a client's website for a large marketing campaign. I checked the host server's memory, disk, and CPU to establish a baseline, then deployed an Nginx container named `client-website` on port 8080. I generated test traffic with `curl`, including an intentional 404 error, and used `docker logs` and `docker stats` to analyze the application logs and real-time resource usage.

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
-## Skills Learned

- Checking host memory usage with `free -h` and reading total, used, and available RAM
- Checking disk capacity with `df -h` and identifying the size of the root (`/`) file system
- Reading live CPU load and running processes with `top`
- Deploying a containerized Nginx web server with Docker, including port mapping (`-p 8080:80`)
- Simulating user traffic and triggering an HTTP 404 error using `curl`
- Retrieving and analyzing application logs with `docker logs` to find HTTP 200 and 404 status codes
- Monitoring real-time container CPU, memory, and network usage with `docker stats`
- Understanding the difference between logs (events) and metrics (numbers over time)
- Documenting system health and observability results in Markdown
- Organizing evidence and committing work to a GitHub portfolio repository