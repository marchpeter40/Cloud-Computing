# Docker Deployment & Container Lifecycle

This document records the commands used to deploy an Nginx container and manage its complete lifecycle on KillerCoda.

## 1. Check Docker Installation
```bash
docker --version
docker version
```
**Explanation:** Verifies that Docker is installed and shows the client and server version information.

## 2. Pull the Nginx Image
```bash
docker pull nginx
```
**Explanation:** Downloads the official Nginx image from Docker Hub so it can be used to create containers.

## 3. Run the Nginx Container
```bash
docker run -d -p 8080:80 --name my-nginx nginx
```
**Explanation:**  
- `-d` runs the container in detached (background) mode  
- `-p 8080:80` maps host port 8080 to container port 80  
- `--name my-nginx` gives the container a friendly name  
- `nginx` is the image used

## 4. Verify Nginx is Running
```bash
curl http://localhost:8080
```
**Explanation:** Sends an HTTP request to the mapped port. A successful response returns the default Nginx welcome page HTML.

## 5. List Running Containers
```bash
docker ps
```
**Explanation:** Shows all currently running containers, including their Container ID, image, status, ports, and names.

## 6. Stop the Container
```bash
docker stop my-nginx
```
**Explanation:** Gracefully stops the running container named `my-nginx`.

## 7. List All Containers (Including Stopped)
```bash
docker ps -a
```
**Explanation:** Displays both running and stopped containers so we can confirm the container has been stopped.

## 8. Remove the Container
```bash
docker rm my-nginx
```
**Explanation:** Permanently deletes the stopped container. Any data written inside the container (that was not stored in a volume) is lost.

---

## Screenshots Required
- `screenshots/docker-version.png` – output of `docker --version` or `docker version`
- `screenshots/nginx-running.png` – successful `curl http://localhost:8080` showing the Nginx welcome page
- `screenshots/container-lifecycle.png` – terminal showing `docker ps`, `docker stop`, `docker ps -a`, and `docker rm`
