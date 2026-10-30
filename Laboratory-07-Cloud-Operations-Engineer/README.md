<div align="center">

# ☁️ Laboratory 7: The Cloud Operations Engineer

<!-- Navigation Bar -->
<p align="center">
  <a href="#-mission-overview">
    <img src="https://img.shields.io/badge/👤%20MISSION%20OVERVIEW-0056B3?style=for-the-badge&logoColor=white" alt="Mission Overview">
  </a>
  <a href="#-objectives">
    <img src="https://img.shields.io/badge/📖%20OBJECTIVES-D9381E?style=for-the-badge&logoColor=white" alt="Objectives">
  </a>
  <a href="#-monitoring-commands-executed">
    <img src="https://img.shields.io/badge/📁%20COMMANDS-0056B3?style=for-the-badge&logoColor=white" alt="Commands">
  </a>
  <a href="#-skills-learned">
    <img src="https://img.shields.io/badge/☁️%20SKILLS%20LEARNED-D9381E?style=for-the-badge&logoColor=white" alt="Skills Learned">
  </a>
</p>

🔵 **Observe • Measure • Log • Optimize** 🔴

---

</div>

## 🚀 Mission Overview
CloudNova Technologies is preparing for a massive marketing campaign, and management needs to ensure the production servers and containerized Nginx web applications can handle high concurrency without failing. In this mission, we stepped into the role of a Cloud Operations (SRE) Engineer to establish a baseline system health check, deploy containerized web services, generate traffic, inspect live access logs, and monitor real-time container metrics.

---

## 🎯 Objectives
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity[cite: 2].
- Deploy a web container and track its real-time performance using Docker metrics[cite: 2].
- Generate web traffic and extract application access logs for analysis[cite: 2].
- Translate raw performance data into a readable technical report using Markdown[cite: 2].
- Expand and maintain a professional GitHub Cloud Computing Portfolio[cite: 2].

---

## 💻 Monitoring Commands Executed
During this laboratory activity, the following Linux and Docker commands were utilized to inspect system health and container observability:

| Command | Purpose / Description |
| :--- | :--- |
| `free -h` | Checks the server's current RAM availability and usage[cite: 3]. |
| `df -h` | Checks the total storage capacity and usage of the root file system[cite: 3]. |
| `top` | Views active running processes, CPU load, and shifting system performance[cite: 3]. |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploys an Nginx web server container in the background mapped to port 8080[cite: 3]. |
| `curl http://localhost:8080/` | Simulates user web traffic by sending HTTP GET requests[cite: 3]. |
| `docker logs client-website` | Extracts application access and error logs for troubleshooting[cite: 4]. |
| `docker stats client-website` | Monitors live container resource consumption (CPU, Memory, Network I/O)[cite: 3]. |

---

## 🧠 Skills Learned
- **System Resource Baseline Profiling:** Gained proficiency in assessing underlying host memory, storage, and CPU loads using native Linux utilities[cite: 2].
- **Container Observability:** Learned how to extract and interpret container logs to isolate successful HTTP 200 responses from failing HTTP 404 errors[cite: 2, 4].
- **Real-Time Performance Metrics Tracking:** Mastered the use of Docker stats to verify that web applications maintain a lightweight, production-ready memory footprint.
- **Technical SRE Documentation:** Improved ability to translate raw infrastructure data into structured, professional Markdown documentation for enterprise transparency[cite: 2].
