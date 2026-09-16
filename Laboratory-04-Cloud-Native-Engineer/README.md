# Laboratory 04 - Cloud Native Engineer

**Mission 4: The Cloud-Native Engineer**

**University of Eastern Pangasinan**  
**College of Information Technology**  
**First Semester A.Y. 2026-2027**

---

## Mission Overview
This laboratory introduces the fundamental concepts of cloud-native computing by comparing Virtual Machines (VMs) and Containers, and by deploying a real containerized application using Docker.

## Objectives
- Understand the key differences between Virtual Machines and Containers
- Use Docker in a playground environment (KillerCoda)
- Deploy and manage an Nginx container
- Document the complete container lifecycle
- Reflect on how containerization impacts modern software development and operations

## Docker Commands Executed
```bash
# Check Docker version
docker --version
docker version

# Pull Nginx image
docker pull nginx

# Run Nginx container (detached + port mapping)
docker run -d -p 8080:80 --name my-nginx nginx

# Verify the container is serving content
curl http://localhost:8080

# List running containers
docker ps

# Stop the container
docker stop my-nginx

# List all containers (including stopped)
docker ps -a

# Remove the container
docker rm my-nginx
```

## Skills Learned
- Difference between VMs and Containers
- Basic Docker commands (pull, run, ps, stop, rm)
- Port mapping (`-p`)
- Container lifecycle management
- Documenting technical work in Markdown + GitHub

## Challenges Encountered
*(To be filled after performing the hands-on activity)*

## Folder Structure
```
Laboratory-04-Cloud-Native-Engineer/
├── README.md
├── virtualization-vs-containers.md
├── docker-deployment.md
├── reflection.md
└── screenshots/
    ├── docker-version.png
    ├── nginx-running.png
    └── container-lifecycle.png
```
