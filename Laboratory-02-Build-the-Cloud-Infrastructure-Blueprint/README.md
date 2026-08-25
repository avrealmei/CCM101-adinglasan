# 🚀 Mission 2: Build the Cloud Infrastructure Blueprint

<div align="center">
  <img src="https://img.shields.io/badge/CLOUD-NOVA-blue?style=for-the-badge&logo=icloud" />
  <img src="https://img.shields.io/badge/MISSION-02-red?style=for-the-badge" />
</div>

---

### 🗺️ Navigation
[**Mission Overview**](#-mission-overview) | [**Objectives**](#-objectives) | [**Infrastructure Specs**](#%EF%B8%8F-cloud-infrastructure-components) | [**Tools Used**](#-tools-used) | [**Linux Commands**](#-linux-commands-executed) | [**Reflection & Skills**](#-skills-learned)

---

## 📋 Mission Overview
As a Cloud Engineer for **CloudNova Technologies**, I conducted a comprehensive cloud infrastructure assessment. The goal of this mission was to investigate a Linux-based cloud server, identify its core hardware and software components, and prepare a technical blueprint and report for a client migration project.

## 🎯 Objectives
*   🔴 Investigate hardware and software resources available in a Linux cloud environment.
*   🔵 Differentiate between compute, storage, networking, and identity resources.
*   🔴 Interpret the relationship between different cloud infrastructure components.
*   🔵 Compare equivalent infrastructure services across AWS, Microsoft Azure, and GCP.
*   🔴 Create professional technical documentation and architectural diagrams.

## 🏗️ Cloud Infrastructure Components
Based on the investigation of the KillerCoda environment, the following infrastructure specs were identified:

| Component | Specification |
| :--- | :--- |
| <font color="blue">**Compute**</font> | Intel Xeon E312xx CPU (1 Core), 1.9 GiB RAM |
| <font color="red">**Storage**</font> | 21GB Total Disk Capacity (Virtual Block Storage) |
| <font color="blue">**Networking**</font> | Private IP Address (172.30.1.2) within a virtual network |
| <font color="red">**OS**</font> | Ubuntu 24.04.4 LTS (Noble Numbat) |

## 🛠️ Tools Used
*   **KillerCoda:** Terminal-based environment for server investigation.
*   **GitHub:** Portfolio hosting and version control.
*   **Canva:** Used to design the stylish Cloud Architecture Diagram.
*   **Markdown:** Language used for all technical documentation.

---

## ⌨️ Linux Commands Executed

To generate the infrastructure report, I utilized specific Linux commands to audit the cloud environment. Below is a breakdown of the primary commands used within the automation script.

### 🔍 Command Breakdown

| Command | Purpose | Explanation | Example |
| :--- | :--- | :--- | :--- |
| `hostname` | **System Identity** | Identifies the unique name of the server on the network. | `controlplane` |
| `os-release` | **Software OS** | Displays distribution details (e.g., Ubuntu, Debian). | `Ubuntu 24.04.4 LTS` |
| `uname -r` | **Kernel Version** | Shows the specific kernel version governing the hardware. | `6.8.0-1015-azure` |
| `lscpu` | **Compute Audit** | Lists detailed CPU architecture and core information. | `Intel(R) Xeon(R) CPU` |
| `free -h` | **Memory Audit** | Provides real-time RAM usage in human-readable format. | `1.9 GiB` |
| `df -h` | **Storage Audit** | Reports the amount of disk space used and available. | `21G` |
| `hostname -I` | **Network Audit** | Retrieves the internal IP address of the cloud instance. | `172.30.1.2` |

### 🛠️ Automated Report Script
This custom command block was used to extract and format all system data simultaneously:

```bash
cat <<EOF
\$(hostname)
\$(grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"')
\$(uname -r)
\$(lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs)
\$(nproc) Core
\$(free -h | awk '/Mem:/ {print \$2}')
\$(df -h --total | grep total | awk '{print \$2}')
\$(df -h / | awk 'NR==2 {print \$2}') (/dev/vda1)
\$(lsblk -lo NAME,SIZE,MOUNTPOINT | grep -E 'vda1 |vda15|vda16' | awk '{printf "%-7s %-7s %s\n", \$1, \$2, \$3}')
\$(hostname -I | awk '{print \$1}')
\$(hostname -I | awk '{print \$2}')
EOF
