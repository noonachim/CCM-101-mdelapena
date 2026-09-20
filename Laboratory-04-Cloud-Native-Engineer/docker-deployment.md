# Docker Deployment

## Commands Used

1. `sudo docker pull nginx` — Downloads the official Nginx image from Docker Hub to the local machine.
2. `sudo docker run -d -p 8080:80 nginx` — Runs the Nginx container in detached (background) mode and maps port 8080 on the host to port 80 inside the container.
3. `curl http://localhost:8080` — Sends an HTTP request to the running container to verify the web server is responding.
4. `sudo docker ps` — Lists all currently running containers.
5. `sudo docker stop 9a01d04fbb92` — Stops the running Nginx container.
6. `sudo docker ps -a` — Lists all containers, including stopped ones, to verify the container has stopped.
7. `sudo docker rm 9a01d04fbb92` — Permanently removes the stopped container from the system.
