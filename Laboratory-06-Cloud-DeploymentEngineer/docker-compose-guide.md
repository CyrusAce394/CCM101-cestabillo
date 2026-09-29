# Docker Compose Guide

## What Does the services: Block Do?

The `services:` block lists the containers that Docker Compose will create and run. In our project, there are two services: `database`, which runs MariaDB, and `app`, which runs Nextcloud.

## How Does Nextcloud Find the Database?

Nextcloud uses the `MYSQL_HOST` setting to find the MariaDB database.

In our Compose file, we have:

`MYSQL_HOST=database`

The word `database` is the name of the MariaDB service. This allows the Nextcloud container to connect to the database container.

## docker run vs docker-compose up -d

The `docker run` command is usually used to create and run one container at a time.

The `docker-compose up -d` command uses the `docker-compose.yml` file to create and run multiple containers together. The `-d` means that the containers run in the background, so we can continue using the terminal.
