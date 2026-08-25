cat << 'EOF' > infrastructure-report.md
# ☁️ Cloud Infrastructure Assessment Report

## 🖥️ System Identification
* **Hostname:** ubuntu
* **Operating System:** Ubuntu 24.04.4 LTS
* **Kernel Version:** 6.8.0-138-generic

## ⚙️ Compute Resources
* **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
* **CPU Cores:** 1 Core
* **Total RAM:** 1.9Gi

## 💾 Storage Resources
* **Total Disk Capacity:** 21G
* **Root Partition:** 19G (/dev/vda1)
* **Storage Layout:**
  * vda1    19G     /
  * vda15   106M    /boot/efi
  * vda16   913M    /boot
EOF 
