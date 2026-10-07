# Docker Compose Guide

## The `services:` Block

The `services:` block defines the containers that make up the application. In this laboratory, there are two services:

- `database` — runs MariaDB 10.6.
- `app` — runs the Nextcloud application.

Each service specifies the Docker image, environment variables, and other configuration needed to run the container.

## How Does Nextcloud Find the Database?

The Nextcloud container uses the following environment variable:

```yaml
- MYSQL_HOST=database
```

The value `database` is the service name of the MariaDB container. Docker Compose provides service-to-service networking, so the Nextcloud container can use the service name to locate the database container instead of needing to know its IP address.

The other database-related variables tell Nextcloud which database, username, and password to use:

```yaml
- MYSQL_PASSWORD=cloudnova_pass
- MYSQL_DATABASE=nextcloud_db
- MYSQL_USER=nextcloud_user
- MYSQL_HOST=database
```

## `docker run` vs. `docker-compose up -d`

`docker run` starts an individual container and normally requires the configuration to be provided through command-line options. It is useful for simple or one-container deployments.

`docker-compose up -d` reads the `docker-compose.yml` file and creates the services described in it. It can therefore deploy multiple related containers together using one configuration file. The `-d` option runs the containers in detached/background mode.

## Deployment Commands

Create the project directory:

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
```

Create the Compose file:

```bash
nano docker-compose.yml
```

Start the application:

```bash
docker-compose up -d
```

Check the containers:

```bash
docker-compose ps
```

After accessing and testing Nextcloud, stop and remove the stack:

```bash
docker-compose down
```

## Infrastructure as Code

The Compose YAML file acts as Infrastructure as Code because the desired container infrastructure is written as a reusable configuration file. Instead of repeatedly typing many deployment commands, an engineer can use the same file to recreate the defined application stack consistently.

## Important YAML Note

YAML depends on indentation. Use spaces rather than tabs and keep child properties indented consistently under their parent keys.
