# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture separates an application into two main tiers: a web/application tier and a database tier. In this laboratory, Nextcloud provides the web/application tier while MariaDB provides the database tier. The two containers communicate through Docker Compose so that the application can use the database to store persistent information.

## The Web/Application Tier

The web/application tier is responsible for interacting with users and handling application requests. In this laboratory, the Nextcloud container provides the web interface and processes HTTP requests from the user's browser.

The Nextcloud application is exposed through port `8080` on the host environment and connects to the MariaDB container for database operations.

## The Database Tier

The database tier stores persistent application data. In this laboratory, MariaDB is used as the database service.

The database is configured with:

- Database name: `nextcloud_db`
- Database user: `nextcloud_user`
- Database password: `cloudnova_pass`
- Root password: `cloudnova_root`

These values are supplied through environment variables in the Compose configuration.

## Why Separate Them?

Keeping the web/application server and database in separate containers makes the system easier to manage, update, and troubleshoot. Each tier can be changed or scaled independently, and separating responsibilities also keeps the architecture organized instead of placing the entire application in one contain
