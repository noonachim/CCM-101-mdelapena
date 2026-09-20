# Reflection

This laboratory activity helped me understand the difference between Virtual Machines and containers and how containerization is used in cloud computing. One of the main things I learned is that a Docker container can start much faster than installing and starting a complete operating system inside a Virtual Machine. A Virtual Machine requires its own operating system, while a container shares the host operating system. Because of this, containers can be lightweight and faster to deploy.

The port mapping `-p 8080:80` is necessary because the Nginx web server runs inside the container on port 80. Port 8080 on the host is connected to port 80 inside the container. This makes it possible to access the Nginx server through `http://localhost:8080` from the host environment. Testing the address with the `curl` command demonstrates whether the Nginx server is responding.

I also learned what happens when a container is removed using `docker rm`. The container itself is removed, including data stored only in its writable container layer. This shows why persistent data should use appropriate Docker storage when it needs to remain after a container is removed.

Containerization also changes how software developers and IT operations teams work together. Developers can package applications and their dependencies into containers, while operations teams can deploy those containers in different environments. This can make application deployment more consistent.

My GitHub portfolio is evolving as I add laboratory activities, technical documentation, commands, screenshots, and reflections. This activity improved my understanding of Docker and gave me practical experience documenting cloud-native operations.
