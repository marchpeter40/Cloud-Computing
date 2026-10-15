# Multi-Tier Architecture

## What is a Two-Tier Architecture?
A two-tier architecture splits an application into two layers that run separately and communicate over a network: an application tier that users interact with, and a database tier that stores the data. In this mission, the Nextcloud container is the first tier and the MariaDB container is the second.

## The Web/Application Tier
The web/application tier serves the user interface, handles HTTP requests from browsers, runs the business logic (logins, file uploads, sharing), and queries the database when it needs data. In our deployment this is the `nextcloud` container, exposed on port 8080 of the host (mapped to port 80 inside the container).

## The Database Tier
The database tier stores persistent data: user accounts and credentials, file metadata, shares, and settings. It only answers queries from the application tier and is not exposed to the public. In our deployment this is the `mariadb:10.6` container.

## Why Separate Them?
Separating the web server and the database into two containers lets each be updated, scaled, restarted, and secured independently; for example, the web tier can be replicated under heavy traffic without duplicating the database. It also improves security (the database is not exposed to users) and fault isolation, because a crash in one component does not take down the other. It also follows the container best practice of one process/responsibility per container, which keeps images small and easier to maintain.
