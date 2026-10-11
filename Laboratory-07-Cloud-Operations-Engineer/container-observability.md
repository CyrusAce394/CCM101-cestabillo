
# Container Observability Report

## Laboratory 07 – Cloud Operations Engineer

### Checkpoint 4: Application Logging

## 1. Application Logs

**Command Executed:**

```bash
docker logs client-website
```

The `docker logs` command was used to retrieve the application logs from the running Nginx web server container named `client-website`.

The logs recorded three successful HTTP requests with status code 200 and one failed request with status code 404.

### HTTP Status Codes

| HTTP Status | Description |
|-------------|-------------|
| 200 | Successful website request |
| 404 | Requested page was not found |

## 2. HTTP Request Log Analysis

The following successful HTTP requests were recorded:

```text
172.17.0.1 - - [10/Oct/2026:23:51:54 +0000] "GET / HTTP/1.1" 200 896 "-" "curl/8.5.0" "-"
172.17.0.1 - - [10/Oct/2026:23:52:43 +0000] "GET / HTTP/1.1" 200 896 "-" "curl/8.5.0" "-"
172.17.0.1 - - [10/Oct/2026:23:53:00 +0000] "GET / HTTP/1.1" 200 896 "-" "curl/8.5.0" "-"
```

These three entries indicate that the Nginx web server successfully responded to the simulated website visits.

## 3. HTTP 404 Error Log

**Actual Log Entry:**

```text
172.17.0.1 - - [10/Oct/2026:23:53:39 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

The HTTP 404 error occurred when a request was sent to `/hidden-admin-page`, a page that does not exist on the Nginx server.

The application logs also reported that the requested file could not be found in the server's default web directory.

## 4. Importance of Application Logs

Application logs are important for troubleshooting because they record HTTP requests, errors, and system events that help cloud engineers identify problems within a running application. By analyzing these logs, engineers can determine why a request failed, locate missing resources, and take appropriate actions to resolve application issues.

---



### Checkpoint 5: Real-Time Container Metrics

## 5. Docker Container Monitoring

**Command Executed:**

```bash
docker stats
```

The `docker stats` command was used to monitor the real-time resource consumption of the Nginx container, including CPU usage, memory utilization, network activity, and disk input/output.

## 6. Container Performance Results

**Container Name:** client-website

**Container ID:** 995b95340712

| Performance Metric | Recorded Value |
|--------------------|----------------|
| CPU Usage | 0.00% |
| Memory Usage | 2.73 MiB |
| Memory Limit | 1.859 GiB |
| Memory Percentage | 0.14% |
| Network I/O | 3.88 kB / 5.33 kB |
| Block I/O | 0 B / 12.3 kB |
| PIDs | 2 |

## 7. Performance Observation

Based on the Docker statistics, the Nginx container was consuming only 0.00% CPU and 2.73 MiB of memory during monitoring. The memory utilization was approximately 0.14%, indicating that the container was using only a small portion of its available memory limit.

The network I/O recorded 3.88 kB of received data and 5.33 kB of transmitted data, showing that the container had network activity during the HTTP request simulation.

The block I/O showed 0 B of data read and 12.3 kB of data written. Additionally, the container had 2 PIDs, indicating a small number of active processes.

These results show that the Nginx container was operating with low resource consumption during the testing period. However, additional load testing would be necessary to determine its performance under thousands of simultaneous requests.
