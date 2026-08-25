# ☁️ Cloud Infrastructure Report

<p align="center">

### 🔵 CCM101 – Cloud Computing 🔴

**CloudNova Technologies | Cloud Infrastructure Assessment**

</p>

<p align="center">

<img src="https://img.shields.io/badge/CCM101-CLOUD_COMPUTING-1976D2?style=for-the-badge" />
<img src="https://img.shields.io/badge/MISSION-2-D32F2F?style=for-the-badge" />
<img src="https://img.shields.io/badge/STATUS-COMPLETED-1976D2?style=for-the-badge" />

</p>

---

<!-- ========================================================= -->
<!-- 🔵🔴 CLOUDNOVA DROPDOWN NAVIGATION -->
<!-- ========================================================= -->

<details>
<summary>

🔵 **☁️ CLOUD INFRASTRUCTURE REPORT — NAVIGATION** 🔴

</summary>

<br>

<p align="center">

<a href="#report-overview">
<img src="https://img.shields.io/badge/📋_OVERVIEW-1976D2?style=for-the-badge" />
</a>

<a href="#system-identification">
<img src="https://img.shields.io/badge/🖥️_SYSTEM-D32F2F?style=for-the-badge" />
</a>

<a href="#compute-resources">
<img src="https://img.shields.io/badge/⚙️_COMPUTE-1976D2?style=for-the-badge" />
</a>

<a href="#storage-resources">
<img src="https://img.shields.io/badge/💾_STORAGE-D32F2F?style=for-the-badge" />
</a>

</p>

<p align="center">

<a href="#networking">
<img src="https://img.shields.io/badge/🌐_NETWORK-1976D2?style=for-the-badge" />
</a>

<a href="#linux-investigation-commands">
<img src="https://img.shields.io/badge/⌨️_LINUX_COMMANDS-1976D2?style=for-the-badge" />
</a>

<a href="#combined-infrastructure-information-command">
<img src="https://img.shields.io/badge/🚀_COMBINED_COMMAND-D32F2F?style=for-the-badge" />
</a>

<a href="#technical-observations">
<img src="https://img.shields.io/badge/🔬_OBSERVATIONS-1976D2?style=for-the-badge" />
</a>

</p>

<p align="center">

<a href="#cloud-infrastructure-interpretation">
<img src="https://img.shields.io/badge/☁️_CLOUD_INFRASTRUCTURE-D32F2F?style=for-the-badge" />
</a>

<a href="#evidence">
<img src="https://img.shields.io/badge/📸_EVIDENCE-1976D2?style=for-the-badge" />
</a>

<a href="#skills-demonstrated">
<img src="https://img.shields.io/badge/📚_SKILLS-D32F2F?style=for-the-badge" />
</a>

<a href="#assessment-conclusion">
<img src="https://img.shields.io/badge/💭_CONCLUSION-1976D2?style=for-the-badge" />
</a>

</p>

</details>


</p>

---

<a id="report-overview"></a>

# 📋 Report Overview

This report documents the results of the **Cloud Infrastructure Assessment** conducted during **Mission 2 – Build the Cloud Infrastructure Blueprint**.

The assessment was performed using the **KillerCoda Linux environment** to identify and document the server's system, compute, memory, storage, networking, and virtualization resources.

The collected information provides a technical overview of the cloud server and serves as supporting documentation for the overall **Cloud Infrastructure Blueprint**.

## 🎯 Assessment Purpose

| Area | Purpose |
|---|---|
| 🖥️ **System Identification** | Identify the hostname, operating system, and Linux kernel |
| ⚙️ **Compute** | Determine the available CPU resources |
| 🧠 **Memory** | Determine the available RAM |
| 💾 **Storage** | Examine disk capacity, partitions, and filesystems |
| 🌐 **Networking** | Identify the server's network addresses |
| 🔐 **Virtualization** | Determine the virtualization technology |
| 📝 **Documentation** | Record and organize the infrastructure findings |
| ☁️ **Cloud Computing** | Relate the Linux resources to cloud infrastructure concepts |

---

<a id="system-identification"></a>

# 1. 🖥️ System Identification

## 📋 System Information

| Information | Details | Purpose |
|---|---|---|
| **Hostname** | `ubuntu` | Identifies the Linux server |
| **Operating System** | Ubuntu 24.04.4 LTS | Provides the server's software environment |
| **Codename** | Noble Numbat | Identifies the Ubuntu release |
| **Kernel Version** | `6.8.0-138-generic` | Identifies the running Linux kernel |
| **Environment** | KillerCoda Linux Playground | Provides the virtual Linux server |

## Original System Identification

*   **Hostname:** ubuntu
*   **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
*   **Kernel Version:** 6.8.0-138-generic

## 🎯 Purpose

The purpose of system identification is to determine the basic software environment in which the cloud infrastructure is running.

## 💡 Explanation

The **hostname** identifies the server within the environment.

The **operating system** provides the software platform used to manage applications, files, networking, users, and hardware resources.

The **Linux kernel** is the core component of Ubuntu responsible for communicating with the underlying hardware and managing system resources.

## ☁️ Cloud Computing Relevance

Cloud engineers need to know the operating system and kernel version because software compatibility, security updates, system administration, and application deployment depend on the underlying operating environment.

---

<a id="compute-resources"></a>

# 2. ⚙️ Compute Resources

## 📋 Compute Information

| Compute Resource | Specification | Purpose |
|---|---|---|
| **CPU Model** | Intel Xeon E312xx | Processes system and application workloads |
| **CPU Generation** | Sandy Bridge | Identifies the processor generation |
| **CPU Cores** | 1 Core | Provides processing capacity |
| **Total RAM** | 1.9 GiB | Provides temporary working memory |
| **Approximate RAM** | 2 GB | Simplified memory capacity |
| **Virtualization Type** | Full Virtualization | Provides an isolated virtual machine |
| **Hypervisor** | KVM | Manages the virtual machine |

## Original Compute Resources

*   **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
*   **Number of CPU Cores:** 1 Core
*   **Total RAM:** 1.9 GiB (Approx. 2GB)
*   **Virtualization Type:** Full (KVM Hypervisor)

---

## ⚙️ CPU Resources

The **Intel Xeon E312xx** processor provides the computational capability of the virtual server.

The available **1 CPU core** is responsible for executing system instructions, applications, background processes, and other workloads running on the server.

A single-core configuration is appropriate for lightweight cloud workloads, development environments, testing, and educational activities.

### 🎯 Purpose

| Purpose | Explanation |
|---|---|
| Processing | Executes application instructions |
| Workload Handling | Processes requests and system tasks |
| Application Execution | Provides processing power for programs |
| Cloud Computing | Represents the virtual CPU allocated to the server |

### 💡 Why CPU Matters

CPU capacity affects how much processing a server can perform.

A server with more CPU cores can generally handle more simultaneous processing tasks, while a single-core environment is more appropriate for lightweight workloads.

---

## 🧠 Memory Resources

The server provides approximately **1.9 GiB of RAM**, which is approximately **2 GB of memory**.

### 🎯 Purpose

The purpose of checking RAM is to determine how much temporary memory is available for the operating system and running applications.

### 💡 Explanation

RAM temporarily stores data and instructions that are actively being used by the operating system and applications.

Unlike storage, RAM is temporary and is cleared when the system is restarted or powered off.

### 📊 RAM Usage Suitability

| Workload | Suitability |
|---|---|
| Linux administration | ✅ Suitable |
| Development environment | ✅ Suitable |
| Small web application | ✅ Suitable |
| Small API | ✅ Suitable |
| Small database | ⚠️ Limited |
| Large database | ❌ Not recommended |
| Machine learning | ❌ Not recommended |
| Heavy data processing | ❌ Not recommended |

---

## 🔐 Virtualization

The server uses **Full Virtualization through a KVM Hypervisor**.

### 🎯 Purpose

The purpose of identifying virtualization is to determine how the server's hardware resources are being provided to the operating system.

### 💡 Explanation

**KVM (Kernel-based Virtual Machine)** is a Linux virtualization technology that allows a physical host machine to run virtual machines.

The virtual machine receives virtualized resources such as:

| Virtual Resource | Function |
|---|---|
| ⚙️ CPU | Provides processing power |
| 🧠 RAM | Provides temporary memory |
| 💾 Storage | Provides persistent disk space |
| 🌐 Network | Provides network communication |

### ☁️ Cloud Computing Relevance

Virtualization is one of the fundamental technologies behind cloud computing.

Cloud providers can use virtualization to divide physical server resources into multiple virtual machines.

Each virtual machine can run its own operating system and applications while sharing the underlying physical infrastructure.

---

<a id="storage-resources"></a>

# 3. 💾 Storage Resources

## 📋 Storage Information

| Storage Resource | Specification | Purpose |
|---|---|---|
| **Total Disk Capacity** | 21 GB | Total storage across partitions |
| **Main Partition** | `/dev/vda1` | Main Linux filesystem |
| **Main Partition Size** | 19 GB | Stores the primary Linux environment |
| **Storage Device** | `vda` | Virtual disk device |
| **Storage Type** | Virtual Disk | Provides storage to the virtual machine |

## Original Storage Resources

*   **Total Disk Capacity:** 21 GB (Total across all partitions)
*   **Main Partition Size:** 19 GB (`/dev/vda1`)
*   **Mounted File Systems:**
    | Name | Size | Mount Point |
    | :--- | :--- | :--- |
    | vda1 | 19G | / |
    | vda15| 106M | /boot/efi |
    | vda16| 913M | /boot |

## 🎯 Purpose

The purpose of investigating storage resources is to determine how much persistent disk capacity is available and how the disk is divided among the system's filesystems.

## 💡 Storage Explanation

Storage is used to permanently store:

| Data Type | Examples |
|---|---|
| 🐧 Operating System | Ubuntu system files |
| 📦 Applications | Installed software |
| ⚙️ Configuration | System configuration files |
| 📋 Logs | System and application logs |
| 👤 User Data | Files created by users |
| 📚 Packages | Installed and downloaded packages |

Unlike RAM, storage retains information after the system is restarted.

---

## 🔵 Main Partition

The main partition is:

```text
/dev/vda1
