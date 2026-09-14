# Docker Deployment Log

## Commands Executed

1. `docker pull nginx` — Downloaded the official Nginx image from Docker Hub.
2. `docker run -d -p 8080:80 --name my-nginx nginx` — Ran Nginx in the background, mapping host port 8080 to container port 80.
3. `curl http://localhost:8080` — Verified the web server was serving the default Nginx welcome page.
4. `docker ps` — Listed running containers.
5. `docker stop my-nginx` — Stopped the running container.
6. `docker ps -a` — Verified the container was stopped (Exited status).
7. `docker rm my-nginx` — Removed the stopped container completely.

## Screenshots
- docker-version.png
- nginx-running.png
- container-lifecycle.png