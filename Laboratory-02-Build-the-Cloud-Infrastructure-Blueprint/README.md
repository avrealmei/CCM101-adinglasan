# Mission 2: Build the Cloud Infrastructure Blueprint

## 📋 Mission Overview
As a Cloud Engineer for **CloudNova Technologies**, I conducted a comprehensive cloud infrastructure assessment. The goal of this mission was to investigate a Linux-based cloud server, identify its core hardware and software components, and prepare a technical blueprint and report for a client migration project.

## 🎯 Objectives
*   Investigate hardware and software resources available in a Linux cloud environment.
*   Differentiate between compute, storage, networking, and identity resources.
*   Interpret the relationship between different cloud infrastructure components.
*   Compare equivalent infrastructure services across AWS, Microsoft Azure, and GCP.
*   Create professional technical documentation and architectural diagrams.

## 🏗️ Cloud Infrastructure Components
Based on the investigation of the KillerCoda environment, the following infrastructure specs were identified:
*   **Compute:** Intel Xeon E312xx CPU (1 Core), 1.9 GiB RAM.
*   **Storage:** 21GB Total Disk Capacity (Virtual Block Storage).
*   **Networking:** Private IP Address (172.30.1.2) within a virtual network.
*   **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat).

## 🛠️ Tools Used
*   **KillerCoda:** Terminal-based environment for server investigation.
*   **GitHub:** Portfolio hosting and version control.
*   **Canva:** Used to design the stylish Cloud Architecture Diagram.
*   **Markdown:** Language used for all technical documentation.

## ⌨️ Linux Commands Executed
To generate the infrastructure report, I used the following custom command block to extract and format system data:

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
