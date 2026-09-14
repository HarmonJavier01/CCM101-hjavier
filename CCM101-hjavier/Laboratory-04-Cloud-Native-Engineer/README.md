# Laboratory 04 — Cloud-Native Engineer

## Mission Overview
(1-2 sentences: you deployed a containerized Nginx web server using Docker
on a KillerCoda playground, as part of exploring cloud-native infrastructure
for CloudNova Technologies' client.)

## Objectives
- Differentiate between traditional VMs and Containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute fundamental Docker CLI commands.
- Pull, run, manage, and terminate a containerized application (Nginx).
- Document container operations in Markdown.

## Docker Commands Executed
- `docker --version`
- `docker info`
- `docker pull nginx`
- `docker run -d -p 8080:80 --name my-nginx nginx`
- `curl http://localhost:8080`
- `docker ps`
- `docker stop my-nginx`
- `docker ps -a`
- `docker rm my-nginx`

## Skills Learned
(Your own bullet points — e.g. verifying a container runtime, running
detached containers, port mapping, managing the container lifecycle.)

## Challenges Encountered
(Your own notes — e.g. any confusion about port mapping direction,
KillerCoda session timeouts, etc. Be honest — this is meant to be real.)