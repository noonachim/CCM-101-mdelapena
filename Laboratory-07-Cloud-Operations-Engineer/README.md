# Laboratory Activity 7: The Cloud Operations Engineer

## Mission Overview

This laboratory activity focused on cloud operations, observability, and monitoring using a Linux server and Docker. The main task was to establish a baseline of the host system, deploy an Nginx web server in a container, generate HTTP traffic, examine application logs, and monitor the container's resource consumption.

The activity simulated the work of a Cloud Operations Engineer at CloudNova Technologies. Instead of relying on assumptions when troubleshooting, system metrics and application logs were used as evidence of the server and application's health.

## Objectives

- Monitor host CPU, memory, and disk capacity using Linux command-line tools.
- Deploy an Nginx web container and monitor its performance with Docker.
- Generate successful and failed HTTP requests using `curl`.
- Examine Docker application logs and identify an HTTP 404 error.
- Monitor container CPU, memory, and network activity using `docker stats`.
- Document the results using Markdown and maintain the Cloud Computing GitHub portfolio.

## Monitoring Commands Executed

```bash
free -h
df -h /
top
docker run -d --name client-website -p 8080:80 nginx
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080/hidden-admin-page
docker logs client-website
docker stats
```

## Skills Learned

- Linux system resource monitoring
- Disk and memory health checking
- Docker container deployment
- HTTP traffic simulation
- Application log analysis
- Real-time container monitoring
- Technical documentation using Markdown
- Git and GitHub portfolio management
