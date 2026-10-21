# 📊 System Baseline Report

<p align="center">
  <img src="https://img.shields.io/badge/Module-Host%20Monitoring-blue?style=for-the-badge" alt="Module">
  <img src="https://img.shields.io/badge/Status-Completed-red?style=for-the-badge" alt="Status">
</p>

## 🎯 Objective
Establish a baseline health check on the production server using native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.

---

## 🛠️ Baseline Metrics Recorded

* **Total RAM Available on the Server:** 1.9Gi
* **Total Storage Capacity of the Root (/) File System:** 39Gi

---

## 💡 Critical Infrastructure Insight
Checking disk space before a massive traffic surge is critical because a sudden influx of users drastically accelerates application log generation, cache writing, and temporary file creation, which can easily fill up the root partition and crash the server if storage capacity is exhausted.

---

## 📸 Evidence & Screenshots
* `screenshots/memory-check.png` - Captured output of server RAM availability (`free -h`).
* `screenshots/disk-check.png` - Captured output of root file system storage capacity (`df -h`).
