# Cloud Infrastructure Report

<p align="center">

🔵 **CCM101 – CLOUD COMPUTING** 🔴  
**CloudNova Technologies | Cloud Infrastructure Assessment**

</p>

<p align="center">

<img src="https://img.shields.io/badge/CCM101-Cloud_Computing-1976D2?style=for-the-badge" />
<img src="https://img.shields.io/badge/MISSION-2-D32F2F?style=for-the-badge" />
<img src="https://img.shields.io/badge/STATUS-COMPLETED-1976D2?style=for-the-badge" />

</p>

<p align="center">

🔵 **CLOUD ENGINEERING** &nbsp; • &nbsp;
🔴 **LINUX** &nbsp; • &nbsp;
🔵 **INFRASTRUCTURE** &nbsp; • &nbsp;
🔴 **DOCUMENTATION**

</p>

---

## 📋 Report Overview

This report documents the results of the **Cloud Infrastructure Assessment** conducted during **Mission 2 – Build the Cloud Infrastructure Blueprint**.

The assessment was performed using the **KillerCoda Linux environment** to identify and document the server's system, compute, memory, storage, networking, and virtualization resources.

The collected information provides a technical overview of the cloud server and serves as supporting documentation for the overall **Cloud Infrastructure Blueprint**.

---

## 1. System Identification

*   **Hostname:** ubuntu
*   **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
*   **Kernel Version:** 6.8.0-138-generic

### 🔎 System Identification Summary

| System Information | Details |
|---|---|
| 🖥️ **Hostname** | `ubuntu` |
| 🐧 **Operating System** | Ubuntu 24.04.4 LTS |
| 📦 **Codename** | Noble Numbat |
| ⚙️ **Kernel Version** | `6.8.0-138-generic` |
| ☁️ **Environment** | KillerCoda Linux Playground |

### 💡 Observation

The server is running **Ubuntu 24.04.4 LTS**, a Linux distribution commonly used for server and cloud computing environments.

The Linux kernel is responsible for managing the system's hardware resources and providing the core services required by applications and system processes.

---

## 2. Compute Resources

*   **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
*   **Number of CPU Cores:** 1 Core
*   **Total RAM:** 1.9 GiB (Approx. 2GB)
*   **Virtualization Type:** Full (KVM Hypervisor)

### ⚙️ Compute Resource Summary

| Compute Resource | Specification |
|---|---|
| 🔵 **CPU Model** | Intel Xeon E312xx |
| 🔵 **CPU Architecture/Generation** | Sandy Bridge |
| 🔴 **CPU Cores** | 1 Core |
| 🔵 **Total RAM** | 1.9 GiB |
| 🔴 **Approximate RAM** | 2 GB |
| 🔵 **Virtualization Type** | Full Virtualization |
| 🔴 **Hypervisor** | KVM |

### 🔵 CPU Resources

The **Intel Xeon E312xx** processor provides the computational capability of the virtual server.

The available **1 CPU core** is responsible for executing system instructions, applications, background processes, and other workloads running on the server.

A single-core configuration is appropriate for lightweight cloud workloads, development environments, testing, and educational activities.

### 🔴 Memory Resources

The server provides approximately **1.9 GiB of RAM**, which is approximately **2 GB of memory**.

RAM is used to temporarily store data and instructions required by running applications and system processes.

The available memory can support lightweight services, development environments, small applications, and basic server workloads.

### 🔵 Virtualization

The server uses **Full Virtualization through a KVM Hypervisor**.

KVM allows physical hardware resources to be presented as virtual resources to a guest operating system.

This is an important concept in cloud computing because cloud providers commonly use virtualization to provide customers with isolated virtual machines.

---

## 3. Storage Resources

*   **Total Disk Capacity:** 21 GB (Total across all partitions)
*   **Main Partition Size:** 19 GB (`/dev/vda1`)
*   **Mounted File Systems:**
    | Name | Size | Mount Point |
    | :--- | :--- | :--- |
    | vda1 | 19G | / |
    | vda15| 106M | /boot/efi |
    | vda16| 913M | /boot |

### 💾 Storage Summary

| Storage Resource | Specification |
|---|---|
| 🔵 **Total Disk Capacity** | 21 GB |
| 🔴 **Main Partition** | `/dev/vda1` |
| 🔵 **Main Partition Size** | 19 GB |
| 🔴 **Boot EFI Partition** | 106 MB |
| 🔵 **Boot Partition** | 913 MB |
| 🔴 **Storage Type** | Virtual Disk |

### 🔵 Main Partition

The main partition is:

```text
/dev/vda1
