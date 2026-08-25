# Cloud Infrastructure Report

## 1. System Identification
*   **Hostname:** ubuntu
*   **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
*   **Kernel Version:** 6.8.0-138-generic

## 2. Compute Resources
*   **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
*   **Number of CPU Cores:** 1 Core
*   **Total RAM:** 1.9 GiB (Approx. 2GB)
*   **Virtualization Type:** Full (KVM Hypervisor)

## 3. Storage Resources
*   **Total Disk Capacity:** 21 GB (Total across all partitions)
*   **Main Partition Size:** 19 GB (`/dev/vda1`)
*   **Mounted File Systems:**
    | Name | Size | Mount Point |
    | :--- | :--- | :--- |
    | vda1 | 19G | / |
    | vda15| 106M | /boot/efi |
    | vda16| 913M | /boot |

## 4. Networking
*   **Primary IP Address:** 172.30.1.2
*   **Internal/Docker IP:** 172.17.0.1

---

## 5. Technical Observations
Based on the investigation, this server is a virtualized instance running on a **KVM Hypervisor**. It is a "General Purpose" entry-level instance (1 vCPU, 2GB RAM), which is suitable for lightweight web services, small databases, or development environments. The storage is handled via virtual disk images (`vda`), which is standard for cloud-based Linux deployments.

## 6. Evidence
*Refer to the screenshots folder for terminal output verification.*
