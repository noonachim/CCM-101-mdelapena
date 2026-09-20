# Docker Deployment

## Check Docker Version

```bash
docker --version
```

Displays the installed Docker version.

## Check Docker Environment

```bash
docker info
```

Displays information about the Docker environment and its current configuration.

## Pull the Nginx Image

```bash
docker pull nginx
```

Downloads the official Nginx image.

## Run the Nginx Container

```bash
docker run -d -p 8080:80 --name nginx-server nginx
```

Starts an Nginx container in detached mode and maps host port 8080 to container port 80.

## List Running Containers

```bash
docker ps
```

Displays currently running Docker containers.

## Test the Nginx Web Server

```bash
curl http://localhost:8080
```

Sends an HTTP request to the Nginx server through host port 8080.

## Stop the Container

```bash
docker stop nginx-server
```

Stops the running Nginx container.

## Verify the Container Status

```bash
docker ps -a
```

Displays both running and stopped containers so the stopped Nginx container can be verified.

## Remove the Container

```bash
docker rm nginx-server
```

Removes the stopped Nginx container.

## Container Lifecycle Summary

1. `docker ps` — lists running containers.
2. `docker stop nginx-server` — stops the Nginx container.
3. `docker ps -a` — verifies that the container is stopped.
4. `docker rm nginx-server` — removes the stopped container.
