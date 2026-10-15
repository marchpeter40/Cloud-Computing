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
The `services:` block defines every container that makes up the application. Each key under it (`database` and `app`) is one service, with its own image, environment variables, and port mappings. Compose creates one container per service, puts them all on a shared default network, and manages them together as one stack.

## How did the Nextcloud container find the database container?
Through the `MYSQL_HOST=database` environment variable. Compose places both services on the same private network and registers each service name as a DNS hostname, so `database` resolves to the MariaDB container's IP address. Nextcloud uses that hostname, along with the matching `MYSQL_DATABASE`, `MYSQL_USER` and `MYSQL_PASSWORD` values, to connect. No IP address needs to be hard-coded.

## `docker run` vs `docker-compose up -d`
| | `docker run` | `docker-compose up -d` |
|---|---|---|
| Scope | Starts one container per command | Starts all services in the file at once |
| Configuration | Long list of flags typed by hand | Declared in a reusable `docker-compose.yml` |
| Networking | Networks/links set up manually | Shared network and service-name DNS created automatically |
| Repeatability | Easy to mistype; hard to reproduce | Version-controllable Infrastructure as Code |
| Teardown | Stop and remove each container separately | `docker-compose down` removes the whole stack |

`-d` runs the stack in detached (background) mode.
