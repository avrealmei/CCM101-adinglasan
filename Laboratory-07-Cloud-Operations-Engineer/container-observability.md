## Checkpoint 4: Application Logging Analysis

### 🔍 Captured 404 Error Log Line
```text
172.17.0.1 - - [30/Oct/2026:01:59:36 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

```
### 💡 Why Application Logs are Vital for Troubleshooting
Application logs provide an exact, timestamped chronological record of every interaction and request hitting a container or server. They are vital during troubleshooting because they eliminate guesswork, allowing engineers to pinpoint exact error codes, client IP addresses, and failing endpoints instantly.

## Checkpoint 5: Real-Time Container Metrics

### 📊 Container Resource Consumption Summary
* **Container ID:** `6ccd29c86146`
* **Container Name:** `client-website`
* **CPU Usage:** `0.00%`
* **Memory Usage / Limit:** `2.727MiB / 1.859GiB`
* **Memory Percentage:** `0.14%`
* **Network I/O:** `2.8kB / 2.26kB`
* **Block I/O:** `0B / 12.3kB`
* **PIDs:** `2`

### 💡 SRE Analysis on Container Efficiency
Monitoring container metrics in real-time ensures that unexpected traffic spikes do not starve the underlying host of system resources. Low and stable memory footprints (such as ~2.727MiB for Nginx) confirm that the containerized web server is lightweight, production-ready, and optimized for high-concurrency scaling.
