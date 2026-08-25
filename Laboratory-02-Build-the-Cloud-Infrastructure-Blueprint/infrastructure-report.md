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

### 🎯 Purpose of the Assessment

The purpose of this assessment is to understand the resources available on a Linux-based cloud server and determine how those resources work together to provide a functional cloud computing environment.

The investigation focuses on:

- 🔵 Identifying the operating system and kernel.
- 🔴 Measuring available compute and memory resources.
- 🔵 Examining virtual storage and mounted filesystems.
- 🔴 Identifying network addresses.
- 🔵 Understanding virtualization through KVM.
- 🔴 Documenting the infrastructure for future reference.

---

# 1. 🖥️ System Identification

*   **Hostname:** ubuntu
*   **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
*   **Kernel Version:** 6.8.0-138-generic

### 🎯 Purpose

The purpose of system identification is to determine the basic software environment of the cloud server.

Knowing the hostname, operating system, and kernel version helps administrators identify the server and understand the software platform on which applications and services are running.

### 🔎 System Identification Summary

| System Information | Details |
|---|---|
| 🖥️ **Hostname** | `ubuntu` |
| 🐧 **Operating System** | Ubuntu 24.04.4 LTS |
| 📦 **Codename** | Noble Numbat |
| ⚙️ **Kernel Version** | `6.8.0-138-generic` |
| ☁️ **Environment** | KillerCoda Linux Playground |

### 💡 Explanation

The **hostname** identifies the server within the environment.

The **operating system** provides the software platform used to manage hardware resources and run applications.

The **Linux kernel** is the core component of the operating system. It manages CPU, memory, storage, networking, and communication between hardware and software.

---

# 2. ⚙️ Compute Resources

*   **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
*   **Number of CPU Cores:** 1 Core
*   **Total RAM:** 1.9 GiB (Approx. 2GB)
*   **Virtualization Type:** Full (KVM Hypervisor)

### 🎯 Purpose

The purpose of investigating compute resources is to determine how much processing capability is available to the cloud server.

CPU resources directly affect how many instructions and workloads the server can process.

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

### 💡 Explanation

The CPU can be considered the **processing engine** of the server.

When an application needs to perform a task, the CPU executes the instructions required to complete that task.

More CPU cores generally allow a system to handle more simultaneous processing workloads.

---

### 🔴 Memory Resources

The server provides approximately **1.9 GiB of RAM**, which is approximately **2 GB of memory**.

RAM is used to temporarily store data and instructions required by running applications and system processes.

The available memory can support lightweight services, development environments, small applications, and basic server workloads.

### 💡 Explanation

RAM is temporary memory.

Unlike storage, RAM is actively used while programs are running. When an application is closed or the server is powered off, the information stored in RAM is normally cleared.

The available 1.9 GiB is sufficient for the lightweight workloads expected in this laboratory environment.

---

### 🔵 Virtualization

The server uses **Full Virtualization through a KVM Hypervisor**.

KVM allows physical hardware resources to be presented as virtual resources to a guest operating system.

This is an important concept in cloud computing because cloud providers commonly use virtualization to provide customers with isolated virtual machines.

### 🎯 Purpose

The purpose of virtualization is to allow multiple virtual machines to operate on physical hardware while keeping their computing environments logically separated.

### 💡 Explanation

**KVM (Kernel-based Virtual Machine)** is a Linux virtualization technology.

Instead of directly using a physical server's hardware, the Ubuntu environment receives virtual CPU, memory, storage, and networking resources.

This is similar to how many cloud providers deliver virtual machines to customers.

---

# 3. 💾 Storage Resources

*   **Total Disk Capacity:** 21 GB (Total across all partitions)
*   **Main Partition Size:** 19 GB (`/dev/vda1`)
*   **Mounted File Systems:**
    | Name | Size | Mount Point |
    | :--- | :--- | :--- |
    | vda1 | 19G | / |
    | vda15| 106M | /boot/efi |
    | vda16| 913M | /boot |

### 🎯 Purpose

The purpose of investigating storage resources is to determine how much persistent disk space is available and how that storage is organized.

Storage is required for:

- Operating system files
- Applications
- Configuration files
- Logs
- User files
- Packages
- Other persistent data

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
