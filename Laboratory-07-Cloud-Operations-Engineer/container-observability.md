# Container Observability

## Nginx Deployment

The client website was deployed as an Nginx Docker container using:

```bash
docker run -d --name client-website -p 8080:80 nginx
```

The container was named `client-website` and port `8080` on the host was mapped to port `80` inside the container.

![Nginx Deployment](screenshots/install-nginx.png)

## Traffic Simulation

Three successful HTTP requests were sent to the website:

```bash
curl http://localhost:8080
curl http://localhost:8080
curl http://localhost:8080
```

A fourth request intentionally accessed a page that does not exist:

```bash
curl http://localhost:8080/hidden-admin-page
```

The invalid request generated an HTTP `404 Not Found` response.

![Simulation 1](screenshots/simulation1.png)

![Simulation 2](screenshots/simulation2.png)

## Application Logs

The container logs were retrieved using:

```bash
docker logs client-website
```

### 404 Error Log

Copy the exact single log line containing `404` from your KillerCoda output below:

```text
[PASTE THE EXACT 404 LOG LINE HERE]
```

Application logs are vital for troubleshooting because they provide a record of requests and events handled by the application. They help an operations engineer identify errors, determine when they occurred, and investigate what happened without relying only on user reports.

![Docker Logs](screenshots/docker-logs.png)

## Real-Time Container Metrics

The container was monitored using:

```bash
docker stats
```

**Exact CPU percentage at the time of the screenshot:** `[ENTER EXACT CPU %]`

**Exact Memory usage at the time of the screenshot:** `[ENTER EXACT MEMORY USAGE, e.g. 3.5MiB]`

The `docker stats` command provides a live view of CPU, memory, network I/O, and other resource information for running containers.

![Container Metrics](screenshots/container-metrics.png)

## Observability Summary

| Metric / Evidence | Result |
|---|---|
| Container | `client-website` |
| Web Server | Nginx |
| Host Port | `8080` |
| Successful Requests | 3 |
| Failed Request | HTTP 404 |
| CPU Usage | `[ENTER EXACT VALUE]` |
| Memory Usage | `[ENTER EXACT VALUE]` |
