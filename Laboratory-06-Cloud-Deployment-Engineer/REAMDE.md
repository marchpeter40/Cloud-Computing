# Laboratory 06 – The Cloud Deployment Engineer

## Mission Overview
CloudNova Technologies needs a proof-of-concept private cloud storage system for a university. This mission deploys a two-tier stack, a **Nextcloud** web container and a **MariaDB** database container, using **Docker Compose** and Infrastructure as Code (IaC) instead of manual `docker run` commands.

## Objectives
- Explain multi-tier application architecture.
- Understand the purpose and structure of `docker-compose.yml`.
- Create configuration files with the `nano` text editor.
- Deploy a multi-container application (Nextcloud + MariaDB) with Docker Compose.
- Document the deployment and IaC principles in Markdown.
- Expand my GitHub Cloud Computing Portfolio.

## Commands Executed
```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml      # write the Compose file, save with Ctrl+O, exit with Ctrl+X
docker-compose up -d         # deploy the stack in the background
docker-compose ps            # verify both containers are running
# Open port 8080 in KillerCoda "Traffic / Ports" to view the Nextcloud setup page
docker-compose down          # stop and remove the stack
```

## Screenshots
| File | Shows |
|---|---|
| <img width="956" height="900" alt="image" src="https://github.com/user-attachments/assets/d36252ae-a667-4df9-8224-9db9ff31739a" />
 | Successful deployment and running containers |
| <img width="1487" height="783" alt="image" src="https://github.com/user-attachments/assets/2c2a1644-045f-4a97-a54c-f6d311191431" />
 | Nextcloud installation page in the browser |
| <img width="938" height="895" alt="image" src="https://github.com/user-attachments/assets/97810691-7eac-434d-97a4-84d20f59ef79" />
 | Containers stopped and removed |

## Skills Learned
- Writing YAML configuration with correct, space-only indentation
- Using `nano` to create and edit files in the terminal
- Defining multi-container applications with Docker Compose
- Service-name networking between containers
- Passing configuration through environment variables
- Mapping container ports to the host
- Deploying and tearing down a whole stack with one command
- Documenting infrastructure in Markdown and Git

## Related Files
- [multi-tier-architecture.md](multi-tier-architecture.md)
- [docker-compose-guide.md](docker-compose-guide.md)
- [reflection.md](reflection.md)
- [docker-compose.yml](docker-compose.yml)
