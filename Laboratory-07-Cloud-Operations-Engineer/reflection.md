# Mission Reflection

This laboratory activity helped me understand why cloud operations engineers need to monitor both the host server and the applications running on it. Even when containers are running perfectly, the host server can still become a limitation. Containers depend on the host's CPU, memory, storage, and other resources. If the host runs out of memory or disk space, the applications inside the containers can become slow or unavailable. Checking the host baseline therefore gives an operations engineer an early warning and a reference point for later troubleshooting.

If a user reports that they cannot log into a web application, the `docker logs` command can help identify what the application is reporting. I would run `docker logs client-website` and examine recent entries for errors, failed requests, or other useful information. The logs could show whether requests are reaching the container and whether the application is returning an error that needs investigation.

Monitoring logs and monitoring metrics provide different types of evidence. Logs describe events and requests that happened inside an application, while metrics provide numerical measurements such as CPU usage, memory usage, and network activity. Logs help explain what happened, while metrics help show the condition and resource behavior of the system.

Large enterprise companies can monitor thousands of containers by using centralized monitoring and observability platforms. Tools such as Prometheus can collect and store metrics, while Grafana can display those metrics through dashboards. Centralized systems make it easier for operations teams to identify unusual resource usage and monitor many services from one place.

My ability to troubleshoot Linux environments improved because I learned to use practical command-line tools instead of guessing about system health. Commands such as `free`, `df`, `top`, `docker logs`, and `docker stats` provide direct evidence that can be used to investigate problems. This activity showed me that effective cloud operations depends on continuous monitoring, careful observation, and evidence-based troubleshooting.
