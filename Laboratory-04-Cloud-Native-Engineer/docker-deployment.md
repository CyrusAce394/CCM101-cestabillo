# Docker Deployment

## Nginx Container Deployment

The Nginx web server was deployed using Docker in the KillerCoda Ubuntu environment.

### Pull the Nginx Image

docker pull nginx

This command downloads the official Nginx image from Docker Hub.

### Run the Nginx Container

docker run -d -p 8080:80 --name nginx-server nginx

This command runs the Nginx container in detached mode and maps port 8080 on the host to port 80 inside the container.

### Test the Nginx Web Server

curl http://localhost:8080

This command sends a request to the Nginx web server and verifies that it is running successfully.

## Container Lifecycle

### 1. List Running Containers

docker ps

This command lists the currently running Docker containers.

### 2. Stop the Nginx Container

docker stop nginx-server

This command stops the running Nginx container.

### 3. Verify the Container is Stopped

docker ps

This command verifies that the Nginx container is no longer running.

### 4. Remove the Container

docker rm nginx-server

This command removes the stopped Nginx container completely.

### 5. Verify the Container was Removed

docker ps -a

This command verifies that the Nginx container has been removed.
