# ☁️ Mission 2: Build the Cloud Infrastructure Blueprint

# 🔵 CLOUD INFRASTRUCTURE BLUEPRINT 🔴

<p align="center">

### ☁️ CCM101 – Cloud Computing

**CloudNova Technologies | Cloud Infrastructure Assessment**

</p>

<p align="center">

🔵 **CLOUD ENGINEERING**   •  
🔴 **LINUX**   •  
🔵 **INFRASTRUCTURE**   •  
🔴 **DOCUMENTATION**

</p>

---

<details>
<summary><strong>🔵 ☰ CLOUD INFRASTRUCTURE MENU 🔴</strong></summary>

<br>

<p align="center">

<a href="#mission-overview">
<img src="https://img.shields.io/badge/🏠_OVERVIEW-1976D2?style=for-the-badge" />
</a>

<a href="#objectives">
<img src="https://img.shields.io/badge/🎯_OBJECTIVES-D32F2F?style=for-the-badge" />
</a>

<a href="#cloud-infrastructure-components">
<img src="https://img.shields.io/badge/🏗️_INFRASTRUCTURE-1976D2?style=for-the-badge" />
</a>

<a href="#linux-commands-executed">
<img src="https://img.shields.io/badge/⌨️_LINUX_COMMANDS-D32F2F?style=for-the-badge" />
</a>

<a href="#cloud-providers">
<img src="https://img.shields.io/badge/☁️_CLOUD_PROVIDERS-1976D2?style=for-the-badge" />
</a>

<a href="#cloud-architecture">
<img src="https://img.shields.io/badge/📐_ARCHITECTURE-D32F2F?style=for-the-badge" />
</a>

<a href="#mission-reflection">
<img src="https://img.shields.io/badge/💭_REFLECTION-1976D2?style=for-the-badge" />
</a>

</p>

</details>

---

<a id="mission-overview"></a>

## 🔵 Mission Overview

As a **Cloud Engineer for CloudNova Technologies**, I conducted a comprehensive cloud infrastructure assessment using the **KillerCoda Linux environment**.

The goal of this mission was to investigate a Linux-based cloud server, identify its core **compute, storage, networking, and operating system resources**, and document the findings as a technical blueprint for a future cloud deployment.

This mission also involved comparing the infrastructure services of **Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)** and creating a simple cloud architecture diagram.

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

<a id="cloud-infrastructure-components"></a>

## 🏗️ Cloud Infrastructure Components

The KillerCoda environment was investigated to identify the available infrastructure resources.

| 🔧 Component            | 📋 Resource Identified         | 💡 Purpose                                                      |
| ----------------------- | ------------------------------ | --------------------------------------------------------------- |
| 🔵 **Compute**          | Intel Xeon E312xx CPU — 1 Core | Processes workloads and executes applications                   |
| 🔵 **Memory**           | 1.9 GiB RAM                    | Temporarily stores data required by running processes           |
| 🔴 **Storage**          | 21 GB virtual disk             | Stores the operating system, applications, and files            |
| 🔵 **Networking**       | Private IP `172.30.1.2`        | Enables communication within the virtual network                |
| 🔴 **Operating System** | Ubuntu 24.04.4 LTS             | Provides the software environment for applications and services |

### 🔵 Compute Resources

The **Intel Xeon E312xx CPU** provides the processing capability of the cloud server.

CPU resources are essential because cloud applications require processing power to execute programs, handle requests, and perform computational tasks.

### 🔴 Storage Resources

The environment provides approximately **21 GB of virtual disk capacity**.

Storage is required for the operating system, application files, configuration files, logs, and other data.

### 🔵 Networking Resources

The server uses a **private IP address (`172.30.1.2`)** within its virtual network.

Networking allows the server to communicate with other systems and cloud infrastructure components.

### 🔴 Operating System

The server runs **Ubuntu 24.04.4 LTS (Noble Numbat)**.

The operating system manages the hardware resources and provides the environment required to run cloud applications and services.

---

<a id="linux-commands-executed"></a>

## ⌨️ Linux Commands Executed

The following commands were used to investigate and collect information from the Linux cloud environment.

### 1. `hostname`

**Purpose:**
Displays the hostname of the Linux server.

```bash
hostname
```

### 2. Operating System Information

```bash
grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"'
```

**Purpose:**
Identifies the Linux distribution and version.

### 3. `uname -r`

```bash
uname -r
```

**Purpose:**
Displays the Linux kernel version.

### 4. CPU Model

```bash
lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs
```

**Purpose:**
Displays information about the processor.

### 5. `nproc`

```bash
nproc
```

**Purpose:**
Displays the number of available processing units.

### 6. RAM Information

```bash
free -h | awk '/Mem:/ {print $2}'
```

**Purpose:**
Displays the total RAM available to the cloud server.

### 7. Disk Capacity

```bash
df -h --total | grep total | awk '{print $2}'
```

**Purpose:**
Displays the total available disk capacity.

### 8. Root Disk Information

```bash
df -h / | awk 'NR==2 {print $2}'
```

**Purpose:**
Displays the size of the root filesystem.

### 9. Mounted File Systems

```bash
lsblk -lo NAME,SIZE,MOUNTPOINT
```

**Purpose:**
Displays storage devices, partitions, sizes, and mount points.

### 10. IP Address

```bash
hostname -I
```

**Purpose:**
Displays the IP addresses assigned to the server.

---

<a id="cloud-providers"></a>

## ☁️ Cloud Providers

Three major public cloud providers were considered for the infrastructure comparison.

| Infrastructure Component         | 🔶 AWS     | 🔷 Microsoft Azure             | 🔵 Google Cloud       |
| -------------------------------- | ---------- | ------------------------------ | --------------------- |
| **Compute**                      | Amazon EC2 | Azure Virtual Machines         | Compute Engine        |
| **Storage**                      | Amazon S3  | Azure Blob Storage             | Cloud Storage         |
| **Networking**                   | Amazon VPC | Azure Virtual Network          | Virtual Private Cloud |
| **Identity & Access Management** | AWS IAM    | Microsoft Entra ID / Azure IAM | Cloud IAM             |

### Which provider offers the broadest range of services?

All three major cloud providers offer a broad range of infrastructure, application, database, networking, storage, security, and AI-related services.

### Which platform would you recommend for an organization that primarily uses Microsoft products?

**Microsoft Azure** would be a strong choice because it integrates closely with Microsoft's existing ecosystem.

### Which platform is widely recognized for AI, ML, and Kubernetes services?

**Google Cloud Platform (GCP)** is widely recognized for its strengths in artificial intelligence, machine learning, and Kubernetes technologies.

### What similarities were observed?

AWS, Azure, and GCP all provide comparable fundamental cloud infrastructure services, including:

* Compute
* Storage
* Networking
* Identity and access management
* Security
* Monitoring

Although the providers use different product names and interfaces, the fundamental infrastructure concepts are similar.

---

<a id="cloud-architecture"></a>

## 📐 Cloud Architecture

The proposed cloud infrastructure contains:

```text
                    🌐 INTERNET
                         │
                         ▼
                    👤 USER
                         │
                         ▼
                  🔵 CLOUD NETWORK
                         │
                ┌────────┴────────┐
                │                 │
                ▼                 ▼
        🖥️ COMPUTE            💾 STORAGE
        RESOURCE              RESOURCE
```

The architecture demonstrates how a user can connect through the Internet to a cloud network, access a compute resource, and interact with a storage resource.

### Architecture Components

| Component       | Role                                       |
| --------------- | ------------------------------------------ |
| 🌐 **Internet** | Provides external connectivity             |
| 👤 **User**     | Represents the person accessing the system |
| 🔵 **Network**  | Connects the cloud resources               |
| 🖥️ **Compute** | Processes application workloads            |
| 💾 **Storage**  | Stores application and user data           |

**Architecture Diagram:**
`/screenshots/cloud-architecture.png`

---

<a id="mission-reflection"></a>

## 💭 Mission Reflection

This laboratory helped me understand that cloud computing is not only about deploying applications but also about understanding the infrastructure that supports those applications.

Investigating the KillerCoda Linux environment allowed me to see how **compute, storage, networking, and operating system resources** work together.

I learned that compute resources provide processing power, storage resources maintain data, networking resources connect systems, and the operating system manages the overall environment.

I also learned the importance of technical documentation before deploying infrastructure. Proper documentation provides engineers with a clear reference of the resources, configurations, and decisions involved in a system.

Another important skill I developed was comparing cloud services between **AWS, Azure, and GCP**. Although the providers use different product names, their fundamental infrastructure concepts are similar.

Finally, this mission improved my GitHub Cloud Computing Portfolio by adding a structured laboratory project containing technical reports, infrastructure documentation, commands, screenshots, and an architecture diagram.

---

## 📚 Skills Learned

* 🔵 Linux system administration
* 🔴 Cloud infrastructure identification
* 🔵 CPU, RAM, disk, and filesystem investigation
* 🔴 Network information gathering
* 🔵 Linux command-line usage
* 🔴 Cloud service comparison
* 🔵 Technical Markdown documentation
* 🔴 Cloud architecture design
* 🔵 GitHub repository management
* 🔴 Infrastructure assessment and reporting

---

## ⚠️ Challenges Encountered

One challenge was understanding how individual Linux commands could be combined to collect infrastructure information efficiently.

Another challenge was understanding how hardware resources available in a Linux environment relate to cloud infrastructure concepts.

Comparing AWS, Azure, and GCP was also challenging because each provider uses different names for services that perform similar functions.

Creating a structured technical document was important because the information needed to be organized clearly enough for another engineer to understand.

---

## 📂 Repository Structure

```text
CCM101-adinglasan/
│
├── README.md
│
├── Laboratory-01-Welcome-to-the-Cloud/
│
└── Laboratory-02-Build-the-Cloud-Infrastructure-Blueprint/
    │
    ├── README.md
    ├── infrastructure-report.md
    ├── cloud-components.md
    ├── cloud-provider-comparison.md
    ├── reflection.md
    │
    └── screenshots/
        ├── server-information.png
        ├── network-information.png
        ├── storage-information.png
        └── cloud-architecture.png
```

---

## ✅ Mission Success Criteria

* [x] Investigated a Linux server running in a cloud environment.
* [x] Identified major cloud infrastructure components.
* [x] Documented compute, storage, networking, and operating system resources.
* [x] Compared AWS, Microsoft Azure, and Google Cloud.
* [x] Designed a simple cloud infrastructure architecture.
* [x] Practiced Linux command-line investigation.
* [x] Created organized Markdown documentation.
* [x] Continued developing the GitHub Cloud Computing Portfolio.

---

<p align="center">

🔵 **CLOUD ENGINEERING**   •  
🔴 **LINUX**   •  
🔵 **INFRASTRUCTURE**   •  
🔴 **DOCUMENTATION**

</p>

<p align="center">

**CCM101 – Cloud Computing**
**Mission 2 Completed**

</p>

<p align="center">

<a href="#-mission-2-build-the-cloud-infrastructure-blueprint">
<img src="https://img.shields.io/badge/⬆️_BACK_TO_TOP-1976D2?style=for-the-badge" />
</a>

</p>
