# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application stack. In this laboratory, it contains two services: `database` for MariaDB and `app` for Nextcloud.

## Database Service

The database service uses the `mariadb:10.6` image.

The environment variables configure the MariaDB database:

- `MYSQL_ROOT_PASSWORD` sets the root password.
- `MYSQL_PASSWORD` sets the password for the Nextcloud database user.
- `MYSQL_DATABASE` specifies the database name.
- `MYSQL_USER` specifies the database user.

## Nextcloud App Service

The `app` service uses the `nextcloud` image and maps host port `8080` to container port `80`:

```yaml
ports:
  - 8080:80
```

This allows the Nextcloud web interface to be accessed through port 8080 of the playground environment.

## How Does Nextcloud Find MariaDB?

The Nextcloud container uses:

```yaml
MYSQL_HOST=database
```

The value `database` matches the name of the MariaDB service in the Compose file. Docker Compose provides service-to-service networking, allowing the Nextcloud container to reach the database using that service name.

## `docker run` vs. `docker-compose up -d`

`docker run` is normally used to create and start an individual container with its configuration supplied through command-line options. `docker-compose up -d` reads the Compose YAML file and creates/starts the services defined in the application stack together, while running them in detached/background mode.

For a multi-container application, Compose makes the configuration repeatable and easier to manage because the infrastructure is described as code.

## Infrastructure as Code

The Compose file is an example of Infrastructure as Code because the desired application infrastructure is written in a configuration file instead of being configured entirely through manual commands.

## Student Note

Before submission, compare this guide with your actual terminal output and revise anything that differs from your experience.
