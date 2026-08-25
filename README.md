# 🔵 CLOUD INFRASTRUCTURE BLUEPRINT 🔴

<p align="center">

### ☁️ CCM101 – Cloud Computing

**CloudNova Technologies | Cloud Infrastructure Assessment**

</p>

<p align="center">

<a href="#mission-overview">
<img src="https://img.shields.io/badge/🏠_MISSION_OVERVIEW-1976D2?style=for-the-badge" />
</a>
<a href="#objectives">
<img src="https://img.shields.io/badge/🎯_OBJECTIVES-D32F2F?style=for-the-badge" />
</a>
<a href="#cloud-infrastructure">
<img src="https://img.shields.io/badge/🏗️_CLOUD_INFRASTRUCTURE-1976D2?style=for-the-badge" />
</a>
<a href="#compute-resources">
<img src="https://img.shields.io/badge/🖥️_COMPUTE-D32F2F?style=for-the-badge" />
</a>
<a href="#memory-resources">
<img src="https://img.shields.io/badge/🧠_MEMORY-1976D2?style=for-the-badge" />
</a>
<a href="#storage-resources">
<img src="https://img.shields.io/badge/💾_STORAGE-1976D2?style=for-the-badge" />
</a>
<a href="#networking-resources">
<img src="https://img.shields.io/badge/🌐_NETWORKING-D32F2F?style=for-the-badge" />
</a>
<a href="#operating-system">
<img src="https://img.shields.io/badge/🐧_OPERATING_SYSTEM-1976D2?style=for-the-badge" />
</a>
<a href="#linux-investigation">
<img src="https://img.shields.io/badge/⌨️_LINUX_COMMANDS-D32F2F?style=for-the-badge" />
</a>
<a href="#cloud-services">
<img src="https://img.shields.io/badge/☁️_CLOUD_SERVICES-1976D2?style=for-the-badge" />
</a>
<a href="#cloud-architecture">
<img src="https://img.shields.io/badge/🏗️_ARCHITECTURE-D32F2F?style=for-the-badge" />
</a>
<a href="#mission-reflection">
<img src="https://img.shields.io/badge/💭_REFLECTION-1976D2?style=for-the-badge" />
</a>

</p>

<p align="center">

🔵 **CLOUD ENGINEERING**   •  
🔴 **LINUX**   •  
🔵 **INFRASTRUCTURE**   •  
🔴 **DOCUMENTATION**

</p>

---

<a id="mission-overview"></a>

## 🔵 Mission Overview

As a **Cloud Engineer for CloudNova Technologies**, I conducted a comprehensive cloud infrastructure assessment using the **KillerCoda Linux environment**.

The goal of this mission was to investigate a Linux-based cloud server, identify its core **compute, storage, networking, and operating system resources**, and document the findings as a technical blueprint for a future cloud deployment.

This mission also involved comparing the infrastructure services of **Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)** and creating a simple cloud architecture diagram.

---

## 📌 Mission Information

| Information             | Details                                  |
| ----------------------- | ---------------------------------------- |
| 🎓 **Course**           | CCM101 – Cloud Computing                 |
| 🏢 **Organization**     | CloudNova Technologies                   |
| 🧑‍💻 **Role**          | Cloud Engineer                           |
| 🧪 **Environment**      | KillerCoda Linux Playground              |
| 🐧 **Operating System** | Ubuntu 24.04.4 LTS                       |
| ☁️ **Mission**          | Mission 2                                |
| 📋 **Activity**         | Build the Cloud Infrastructure Blueprint |
| ✅ **Status**            | Completed                                |

---

<a id="objectives"></a>

## 🎯 Objectives

By completing this laboratory activity, I was able to:

* 🔵 Investigate hardware and software resources available in a Linux cloud environment.
* 🔴 Identify compute, storage, networking, and operating system resources.
* 🔵 Understand how cloud infrastructure components work together.
* 🔴 Compare equivalent infrastructure services offered by AWS, Microsoft Azure, and GCP.
* 🔵 Create a simple cloud infrastructure architecture.
* 🔴 Practice Linux system investigation commands.
* 🔵 Produce organized technical documentation using Markdown.
* 🔴 Continue developing a professional GitHub Cloud Computing Portfolio.

---

<a id="cloud-infrastructure"></a>

# 🏗️ Cloud Infrastructure

The KillerCoda environment was investigated to identify the available infrastructure resources.

## 🔧 Infrastructure Components

| 🔧 Component            | 📋 Resource Identified         | 💡 Purpose                                                      |
| ----------------------- | ------------------------------ | --------------------------------------------------------------- |
| 🔵 **Compute**          | Intel Xeon E312xx CPU — 1 Core | Processes workloads and executes applications                   |
| 🔵 **Memory**           | 1.9 GiB RAM                    | Temporarily stores data required by running processes           |
| 🔴 **Storage**          | 21 GB virtual disk             | Stores the operating system, applications, and files            |
| 🔵 **Networking**       | Private IP `172.30.1.2`        | Enables communication within the virtual network                |
| 🔴 **Operating System** | Ubuntu 24.04.4 LTS             | Provides the software environment for applications and services |

---

<a id="compute-resources"></a>

## 🔵 Compute Resources

The **Intel Xeon E312xx CPU** provides the processing capability of the cloud server.

CPU resources are essential because cloud applications require processing power to:

* Execute programs
* Process user requests
* Run background services
* Perform computational tasks
* Support application workloads

The environment provides **1 available CPU core**.

---

<a id="memory-resources"></a>

## 🔴 Memory Resources

The cloud environment provides approximately **1.9 GiB of RAM**.

Memory is used by the operating system and running applications to temporarily store data and instructions.

RAM is important for:

* Running applications
* Managing active processes
* Supporting system services
* Improving application responsiveness

---

<a id="storage-resources"></a>

## 🔵 Storage Resources

The environment provides approximately **21 GB of virtual disk capacity**.

Storage is required for:

* Operating system files
* Application files
* Configuration files
* Logs
* User data
* System packages

Virtual storage allows cloud environments to provide flexible and scalable data storage.

---

<a id="networking-resources"></a>

## 🔴 Networking Resources

The server uses the private IP address:

```text
172.30.1.2
```

The private IP address allows the server to communicate with other resources within its virtual network.

Networking resources are important for:

* Server-to-server communication
* Application connectivity
* Internal cloud services
* Network-based administration
* Access to cloud resources

A private IP address is generally used for internal communication rather than direct public access from the Internet.

---

<a id="operating-system"></a>

## 🐧 Operating System

The cloud environment runs:

```text
Ubuntu 24.04.4 LTS
```

Ubuntu is a Linux-based operating system commonly used for cloud servers because of its stability, flexibility, security features, and extensive software support.

The operating system provides the foundation for:

* Application execution
* System administration
* Network configuration
* User management
* Package management
* Cloud services

---

## 🖥️ System Information Summary

```text
Operating System : Ubuntu 24.04.4 LTS
Kernel           : 6.8.0-136-generic
CPU              : Intel Xeon E312xx
CPU Cores        : 1
Memory           : 1.9 GiB
Storage          : 21 GB
Private IP       : 172.30.1.2
Environment      : KillerCoda Ubuntu Playground
```

---

<a id="linux-investigation"></a>

## ⌨️ Linux Investigation Commands

The following Linux commands were useful for investigating the cloud environment:

| Command               | Purpose                                         |
| --------------------- | ----------------------------------------------- |
| `hostname`            | Displays the system hostname                    |
| `uname -a`            | Displays detailed kernel and system information |
| `lscpu`               | Displays CPU information                        |
| `free -h`             | Displays memory usage                           |
| `lsblk`               | Displays block storage devices                  |
| `df -h`               | Displays disk space usage                       |
| `ip addr`             | Displays network interfaces and IP addresses    |
| `ip route`            | Displays routing information                    |
| `cat /etc/os-release` | Displays operating system information           |

These commands demonstrate how Linux administrators can investigate server resources directly from the command line.

---

<a id="cloud-services"></a>

# ☁️ Cloud Services

Cloud providers offer managed infrastructure services that correspond to the resources identified in the KillerCoda environment.

The three major cloud providers considered for this assessment are:

* 🔵 **Amazon Web Services (AWS)**
* 🔴 **Microsoft Azure**
* 🔵 **Google Cloud Platform (GCP)**

---

## 🖥️ Compute Service Comparison

| Infrastructure        | 🔵 AWS                                | 🔴 Microsoft Azure                  | 🔵 Google Cloud                |
| --------------------- | ------------------------------------- | ----------------------------------- | ------------------------------ |
| **Virtual Machine**   | Amazon EC2                            | Azure Virtual Machines              | Google Compute Engine          |
| **Purpose**           | Runs virtual servers and applications | Runs virtual machines and workloads | Runs scalable virtual machines |
| **Operating Systems** | Linux / Windows                       | Linux / Windows                     | Linux / Windows                |
| **Scalability**       | Flexible instance sizes               | Flexible VM sizes                   | Flexible machine types         |

### 🔵 AWS – Amazon EC2

**Amazon Elastic Compute Cloud (EC2)** provides resizable virtual servers that can be used to run applications and workloads in the cloud.

### 🔴 Microsoft Azure – Virtual Machines

**Azure Virtual Machines** provide configurable virtual machines for running Linux and Windows workloads.

### 🔵 Google Cloud – Compute Engine

**Google Compute Engine** provides scalable virtual machines for hosting applications and services.

---

## 💾 Storage Service Comparison

| Infrastructure     | 🔵 AWS                             | 🔴 Microsoft Azure                | 🔵 Google Cloud                            |
| ------------------ | ---------------------------------- | --------------------------------- | ------------------------------------------ |
| **Block Storage**  | Amazon EBS                         | Azure Managed Disks               | Google Persistent Disk                     |
| **Object Storage** | Amazon S3                          | Azure Blob Storage                | Google Cloud Storage                       |
| **Purpose**        | Stores application and system data | Provides persistent cloud storage | Stores application and infrastructure data |

---

## 🌐 Networking Service Comparison

| Infrastructure       | 🔵 AWS                  | 🔴 Microsoft Azure    | 🔵 Google Cloud  |
| -------------------- | ----------------------- | --------------------- | ---------------- |
| **Virtual Network**  | Amazon VPC              | Azure Virtual Network | Google Cloud VPC |
| **Private IP**       | Supported               | Supported             | Supported        |
| **Routing**          | Route Tables            | Route Tables          | Routes           |
| **Network Security** | Security Groups / NACLs | NSGs / Azure Firewall | Firewall Rules   |

Virtual networking allows cloud resources to communicate securely while controlling traffic between different infrastructure components.

---

## 🐧 Operating System Support

All three major cloud providers support common Linux distributions.

Examples include:

* Ubuntu
* Debian
* Red Hat Enterprise Linux
* SUSE Linux Enterprise

Linux is widely used in cloud infrastructure because it provides:

* Stability
* Security
* Flexibility
* Open-source software
* Command-line administration
* Extensive cloud support

---

<a id="cloud-architecture"></a>

# 🏗️ Cloud Infrastructure Architecture

The following architecture represents a simple cloud infrastructure blueprint based on the resources investigated during the mission.

```text
                    ☁️ CLOUD INFRASTRUCTURE
                           │
                           ▼
                  ┌──────────────────┐
                  │   🌐 INTERNET    │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │ 🔥 NETWORK /     │
                  │    FIREWALL      │
                  └────────┬─────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │      ☁️ VIRTUAL NETWORK  │
              │                          │
              │      Private Network     │
              │       172.30.1.0/24      │
              └────────────┬─────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │     🖥️ CLOUD SERVER      │
              │                          │
              │   Ubuntu 24.04.4 LTS     │
              │   Intel Xeon CPU         │
              │   1 CPU Core             │
              │   1.9 GiB RAM            │
              │   Private IP             │
              │   172.30.1.2             │
              └────────────┬─────────────┘
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ▼             ▼             ▼
       ┌──────────┐  ┌──────────┐  ┌──────────┐
       │ 💾 Disk  │  │ ⚙️ Apps  │  │ 📊 Logs  │
       │ 21 GB    │  │ Services │  │ & Data   │
       └──────────┘  └──────────┘  └──────────┘
```

---

## 🔄 Infrastructure Flow

The infrastructure operates through the following basic flow:

**1. Internet**

Users or external systems send requests toward the cloud environment.

**2. Network Security**

Firewall and network security mechanisms control incoming and outgoing traffic.

**3. Virtual Network**

The cloud server operates inside a private virtual network.

**4. Cloud Server**

The virtual machine provides compute resources for applications and services.

**5. Storage**

The virtual disk stores the operating system, applications, configurations, logs, and other data.

**6. Applications**

Applications execute using the available CPU and memory resources.

---

## 📊 AWS, Azure, and GCP Mapping

| Resource            | 🔵 AWS                 | 🔴 Azure               | 🔵 GCP                  |
| ------------------- | ---------------------- | ---------------------- | ----------------------- |
| 🖥️ Compute         | Amazon EC2             | Azure Virtual Machines | Compute Engine          |
| 💾 Block Storage    | Amazon EBS             | Azure Managed Disks    | Persistent Disk         |
| 📦 Object Storage   | Amazon S3              | Azure Blob Storage     | Cloud Storage           |
| 🌐 Virtual Network  | Amazon VPC             | Azure Virtual Network  | Google Cloud VPC        |
| 🔐 Network Security | Security Groups / NACL | NSG / Firewall         | Firewall Rules          |
| 🐧 Linux VM         | EC2 Linux              | Azure Linux VM         | Compute Engine Linux VM |

---

<a id="mission-reflection"></a>

# 💭 Mission Reflection

This mission helped me understand how cloud infrastructure is composed of different resources that work together as a complete system.

By investigating the KillerCoda Linux environment, I was able to identify important infrastructure resources such as **CPU, memory, storage, networking, and the operating system**.

I also learned that Linux commands can provide valuable information about the underlying infrastructure of a server. Commands such as `lscpu`, `free -h`, `lsblk`, `df -h`, and `ip addr` can be used to inspect different parts of a system.

The comparison between **AWS, Microsoft Azure, and Google Cloud Platform** also helped me understand that different cloud providers offer similar infrastructure capabilities using different service names.

Overall, this mission improved my understanding of cloud infrastructure and showed me how individual server resources can be organized into a complete cloud architecture.

---

# ✅ Mission Completion

<p align="center">

### 🔵 CLOUD INFRASTRUCTURE BLUEPRINT COMPLETE 🔴

**CloudNova Technologies**

☁️ **COMPUTE**   •  
💾 **STORAGE**   •  
🌐 **NETWORKING**   •  
🐧 **LINUX**

</p>

---

<p align="center">

🔵 **CCM101 – CLOUD COMPUTING** 🔴

**Cloud Infrastructure Assessment**

</p>
