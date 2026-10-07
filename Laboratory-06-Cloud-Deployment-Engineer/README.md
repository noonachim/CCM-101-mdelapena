# Laboratory Activity 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity demonstrates how Docker Compose can be used to deploy a multi-tier private cloud storage application. The application consists of a Nextcloud web/application container and a MariaDB database container. Instead of deploying each container manually, Docker Compose defines the infrastructure in a YAML configuration file and allows the complete stack to be started with one command.

## Objectives

- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Create a Docker Compose configuration using a Linux command-line editor.
- Deploy Nextcloud and MariaDB as a multi-container application.
- Verify, access, and tear down the deployed stack.
- Document Infrastructure as Code (IaC) concepts using Markdown.
- Maintain a structured Cloud Computing portfolio on GitHub.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

If the Docker installation uses the newer Compose plugin, the equivalent commands are:

```bash
docker compose up -d
docker compose ps
docker compose down
```

## Skills Learned

- Multi-tier application architecture
- Docker container deployment
- Docker Compose
- YAML configuration
- Linux command-line editing
- Container verification and troubleshooting
- Infrastructure as Code (IaC)
- Technical documentation using Markdown
- GitHub portfolio organization
