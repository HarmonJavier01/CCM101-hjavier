# Docker Compose Guide

## The Compose File
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?
The `services:` block defines each container that makes up the application. Here it declares two services, `database` (MariaDB) and `app` (Nextcloud). Each service has its own image, environment variables, and port settings. Compose creates and manages one container per service.

## How did the Nextcloud container find the database?
Through `MYSQL_HOST=database`. Compose automatically puts all services in the same private network and registers each service name as a DNS hostname. Nextcloud therefore connects to the hostname `database`, which resolves to the MariaDB container's IP address. No IP address had to be hardcoded. The credentials in the `app` service also match those in the `database` service, so authentication succeeds.

## `docker run` vs `docker-compose up -d`
| | `docker run` | `docker-compose up -d` |
|---|---|---|
| Scope | One container per command | Entire multi-container stack |
| Configuration | Long flags typed manually | Declared in a YAML file |
| Networking | Must be created and linked manually | Created automatically |
| Repeatability | Easy to make typos or forget flags | Same file gives the same result every time |
| Version control | Commands are hard to track | File can be committed to Git (Infrastructure as Code) |

The `-d` flag runs the containers in the background (detached mode).