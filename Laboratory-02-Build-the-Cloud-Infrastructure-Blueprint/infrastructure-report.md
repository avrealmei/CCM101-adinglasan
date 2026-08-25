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

### 🎯 Assessment Purpose

The purpose of this assessment was to investigate a Linux-based virtual server and determine the resources available to it.

The investigation focused on:

* 🔵 Identifying the operating system and kernel.
* 🔴 Identifying the available CPU resources.
* 🔵 Measuring the available memory.
* 🔴 Examining disk capacity and mounted filesystems.
* 🔵 Identifying network addresses.
* 🔴 Determining the virtualization environment.
* 🔵 Connecting Linux system resources to cloud computing concepts.
* 🔴 Collecting technical evidence for the Cloud Infrastructure Blueprint.

---

# 1. 🖥️ System Identification

## 📋 System Information

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

### 🎯 Purpose

The purpose of system identification is to determine the basic software environment in which the cloud infrastructure is running.

### 💡 Explanation

The **hostname** identifies the server within the environment.

The **operating system** provides the software platform used to manage applications, files, networking, users, and hardware resources.

The **Linux kernel** is the core component of Ubuntu responsible for communicating with the underlying hardware and managing system resources.

### 🔵 Why It Matters in Cloud Computing

Cloud engineers need to know the operating system and kernel version because software compatibility, security updates, system administration, and application deployment depend on the underlying operating environment.

---

# 2. ⚙️ Compute Resources

## 📋 Compute Information

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

### 🎯 Purpose

The purpose of investigating compute resources is to determine how much processing capability is available to the virtual server.

### 🔵 CPU Resources

The **Intel Xeon E312xx** processor provides the computational capability of the virtual server.

The available **1 CPU core** is responsible for executing system instructions, applications, background processes, and other workloads running on the server.

A single-core configuration is appropriate for lightweight cloud workloads, development environments, testing, and educational activities.

### 💡 Explanation

The CPU, or **Central Processing Unit**, performs the calculations and instructions required by applications and the operating system.

A server with more CPU cores can generally handle more simultaneous processing tasks.

### 🔴 Why It Matters in Cloud Computing

CPU capacity is an important factor when selecting a cloud virtual machine.

Applications that require more processing power may require additional virtual CPUs, while lightweight applications can operate using fewer resources.

---

## 🧠 Memory Resources

The server provides approximately **1.9 GiB of RAM**, which is approximately **2 GB of memory**.

### 🎯 Purpose

The purpose of checking RAM is to determine how much temporary memory is available for the operating system and running applications.

### 💡 Explanation

RAM temporarily stores data and instructions that are actively being used by the operating system and applications.

Unlike storage, RAM is temporary and is cleared when the system is restarted or powered off.

The available memory can support:

* Lightweight web services
* Development environments
* Testing applications
* Linux system services
* Small databases
* Educational cloud laboratories

### 🔵 Why It Matters in Cloud Computing

RAM affects how many applications and processes can run efficiently at the same time.

If an application requires more memory than is available, the system may experience slower performance or rely more heavily on disk-based memory mechanisms.

---

## 🔐 Virtualization

The server uses **Full Virtualization through a KVM Hypervisor**.

### 🎯 Purpose

The purpose of identifying virtualization is to determine how the server's hardware resources are being provided to the operating system.

### 💡 Explanation

**KVM (Kernel-based Virtual Machine)** is a Linux virtualization technology that allows a physical host machine to run virtual machines.

The virtual machine receives virtualized resources such as:

* CPU
* RAM
* Storage
* Network interfaces

### ☁️ Cloud Computing Connection

Virtualization is one of the fundamental technologies behind cloud computing.

Cloud providers can use virtualization to divide physical server resources into multiple virtual machines.

Each virtual machine can run its own operating system and applications while sharing the underlying physical infrastructure.

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

The purpose of investigating storage resources is to determine how much persistent disk capacity is available and how the disk is divided among the system's filesystems.

### 💡 Explanation

Storage is used to permanently store:

* Operating system files
* Applications
* Configuration files
* Logs
* User files
* Packages
* Other system data

Unlike RAM, storage retains information after the system is restarted.

---

## 🔵 Main Partition

The main partition is:

```text
/dev/vda1
