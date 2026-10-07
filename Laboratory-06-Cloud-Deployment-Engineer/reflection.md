# Reflection

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because the required infrastructure can be described in one reusable configuration file. Instead of manually typing separate commands for every container, image, port, and environment variable, the engineer can define the services once and start the complete application stack with `docker-compose up -d`. This reduces repetitive work and helps make deployments more consistent.

An indentation error in a YAML file can cause the configuration to become invalid or change the meaning of the configuration. YAML uses indentation to show relationships between keys and values, so a tab or incorrect number of spaces can cause Docker Compose to report a YAML parsing or configuration error. This is why careful formatting is important when writing Compose files.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` are used to provide configuration values to the containers. They allow the application and database settings to be defined separately from the main service configuration and make it clear which values are needed by each container. In a real production system, sensitive credentials should also be handled more securely rather than being committed directly to a public repository.

Deploying Nextcloud in only a few minutes showed me how useful containerization and automation can be. A complete application can be assembled from existing container images without manually installing every software component inside a server.

Since Mission 1, my understanding of Cloud Computing has developed from learning basic cloud concepts to understanding how cloud infrastructure can actually be deployed and managed. This mission helped me see the connection between containers, networking, databases, automation, and Infrastructure as Code. It also showed me why cloud engineers need both technical skills and careful documentation to create reliable deployments.
