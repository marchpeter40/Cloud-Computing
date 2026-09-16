# Mission Reflection – Laboratory 04

Working with Docker containers for the first time was a significant shift from traditional virtual machines. The most noticeable difference is the boot time. A virtual machine needs to start an entire operating system, which usually takes several minutes. In contrast, a Docker container starts in just a few seconds because it only launches the application process and reuses the host operating system kernel. This speed makes containers ideal for development and testing environments where quick iteration is important.

Port mapping (`-p 8080:80`) is necessary because containers run in an isolated network namespace. The Nginx web server inside the container listens on port 80 by default, but that port is not automatically accessible from outside the container. By mapping host port 8080 to container port 80, we create a bridge that allows external tools (like the `curl` command or a web browser) to reach the application running inside the container.

When the `docker rm` command is executed, the container is permanently deleted. Any data that was written inside the container’s writable layer is lost unless it was stored in a Docker volume or bind mount. This behavior teaches the importance of separating application code from persistent data.

Containerization is changing the way developers and IT operations teams work together. Developers can package their application with all dependencies into a single image, guaranteeing that it will run the same way in every environment. Operations teams can then deploy, scale, and manage these containers consistently using orchestration tools. This shared responsibility model is the foundation of DevOps culture and enables faster delivery of software.

My GitHub portfolio continues to evolve with each laboratory. From documenting multi-cloud platforms to now demonstrating hands-on container skills, the repository is becoming a clear record of my growing cloud-native knowledge. Each new folder and documentation file shows not only what I learned, but also how I am applying industry-standard tools and practices.
