# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

The activity focused on understanding cloud-native technologies, because the recent topic is the Docker containers. The activity involved comparing Virtual Machines and Containers, using KillerCoda, and deploying an Nginx web server using Docker.

## Objectives

- Differentiate Virtual Machines from Containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute basic Docker commands.
- Pull, run, manage, and remove an Nginx container.
- Document Docker operations using Markdown.

## Docker Commands Executed

### Check Docker Installation

    docker --version

### Check Docker Environment

    docker info

### Pull Nginx Image

    docker pull nginx

### Run Nginx Container

    docker run -d -p 8080:80 --name nginx-server nginx

### Test Nginx Web Server

    curl http://localhost:8080

### List Running Containers

    docker ps

### Stop Nginx Container

    docker stop nginx-server

### Verify Container Status

    docker ps
    docker ps -a

### Remove Nginx Container

    docker rm nginx-server

### Verify Container Removal

    docker ps -a

## Skills Learned

- Understanding the difference between Virtual Machines and Containers.
- Using basic Docker CLI commands.
- Deploying an Nginx web server using Docker.
- Managing the Docker container lifecycle.
- Using KillerCoda as a cloud-based Linux environment.
- Creating technical documentation using Markdown.

## Challenges Encountered

The challenge that i encountered is the commands and understanding the container lifecycle, because i only encountered those for the firstime.
