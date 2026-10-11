# Laboratory 07 – Cloud Operations Engineer

## Mission Reflection

Completing of Laboratory 07 provided me a better understanding about the need for monitoring in cloud operations. Even if Docker containers running properly, there could be issues with the resources available to the host server. Monitoring those would ensure no lags or downtime in terms of memory, CPU, and disk space. With the help of Linux commands, I identified 1.9 GiB of total RAM, 13 GB of available disk storage, and 99.7% of CPU idle.

Application logs can be very helpful for troubleshooting. In case a user faces some problems while trying to log into a web application, `docker logs` will provide recorded errors or failed requests that may explain what went wrong. During our activity, I performed three requests for existing websites and one for a non-existing one and received 3 HTTP 200 responses and one HTTP 404 response.

Logs and metrics offer different information. While logs provide the details of some events or errors occurred, metrics represent measurable resource utilization. With `docker stats` I was able to observe the resource utilization of our Nginx container at 0.00% CPU and 2.73 MiB of memory.

Large company cannot monitor all their thousands of containers manually. There are tools such as Prometheus that help to collect performance metrics and Grafana that provides visual representation through dashboard and graphs. Alerting might be used to notify about some unusual system behavior.

I have acquired some additional troubleshooting skills in Linux. Now, I am more confident about the ability to check resource availability, HTTP status codes, and Docker statistics. Also, I understood that cloud operations need to rely on logs and metrics for proof of application health rather than on assumption.
