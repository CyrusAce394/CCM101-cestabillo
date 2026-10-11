
# Laboratory 07 – Cloud Operations Engineer

## Mission Overview

This laboratory activity focused on monitoring the performance and resource usage of a Linux server and a Docker container using the KillerCoda Ubuntu Playground.

The activity involved checking the server's CPU, memory, and disk storage, deploying an Nginx web server using Docker, simulating website traffic through HTTP requests, and analyzing application logs and real-time container metrics.

Through this activity, I learned how cloud operations engineers monitor system performance, identify application errors, and ensure that cloud services operate efficiently and reliably.

## Objectives

- Monitor Linux server CPU, memory, and disk utilization.
- Establish a baseline of the host server's available resources.
- Deploy an Nginx web server using Docker.
- Simulate website traffic using HTTP requests.
- Generate and identify an HTTP 404 Not Found error.
- Retrieve and analyze Docker application logs.
- Monitor real-time CPU and memory consumption of a container.
- Document system monitoring results using Markdown.
- Improve troubleshooting and cloud operations skills.

## Monitoring Commands Executed

### 1. Check Server Memory

```bash
free -h
```

Displays the total, used, free, and available RAM of the Linux server.

**Result:** 1.9 GiB total RAM and 1.4 GiB available memory.

### 2. Check Disk Storage

```bash
df -h /
```

Displays the total, used, and available storage capacity of the root file system.

**Result:** 19 GB total storage, 13 GB available, and 30% disk usage.

### 3. Monitor CPU and Running Processes

```bash
top
```

Displays real-time CPU utilization, memory usage, and running system processes.

**Result:** 99.7% CPU idle, 131 total tasks, and a load average of 0.00.

### 4. Deploy Nginx Web Server

```bash
docker run -d --name client-website -p 8080:80 nginx:latest
```

Creates and starts an Nginx web server container named `client-website` in the background.

### 5. Verify Running Containers

```bash
docker ps
```

Displays active Docker containers to confirm that the Nginx web server is running.

### 6. Generate Website Traffic

```bash
curl http://localhost:8080/
```

Executed three times to simulate successful website visits.

**Result:** Three HTTP 200 successful responses.

### 7. Generate an HTTP 404 Error

```bash
curl http://localhost:8080/hidden-admin-page
```

Simulates a user attempting to access a nonexistent page.

**Result:** HTTP 404 Not Found response.

### 8. Retrieve Application Logs

```bash
docker logs client-website
```

Displays application logs containing successful and failed HTTP requests.

**Result:** Three HTTP 200 requests and one HTTP 404 request were recorded.

### 9. Monitor Container Performance

```bash
docker stats
```

Displays real-time CPU usage, memory consumption, network activity, and disk I/O of Docker containers.

**Results:**
- Container Name: client-website
- CPU Usage: 0.00%
- Memory Usage: 2.73 MiB
- Memory Percentage: 0.14%
- Network I/O: 3.88 kB / 5.33 kB

## Skills Learned

I learned to monitor the performance and resource consumption of Linux servers and Docker containers using command-line monitoring tools.

I practice those command properly the `free -h`, `df -h /`, and `top` to check the host server's memory, disk storage, CPU utilization, and running processes.

I also learned how to deploy an Nginx web server using Docker and simulate website traffic using `curl`. By generating successful HTTP requests and an intentional 404 error, I understood how applications respond to different user requests.
