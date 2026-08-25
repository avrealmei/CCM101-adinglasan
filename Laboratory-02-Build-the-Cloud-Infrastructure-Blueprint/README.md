# ☁️ Mission 2: Build the Cloud Infrastructure Blueprint

# 🔵 CLOUD INFRASTRUCTURE BLUEPRINT 🔴

### CCM101 – Cloud Computing

**CloudNova Technologies | Cloud Infrastructure Assessment**

<p align="center">

[🏠 Overview](#-mission-overview) •
[🎯 Objectives](#-objectives) •
[🏗️ Infrastructure](#️-cloud-infrastructure-components) •
[🛠️ Tools](#️-tools-used) •
[⌨️ Commands](#️-linux-commands-executed) •
[☁️ Providers](#️-cloud-providers) •
[📐 Architecture](#-cloud-architecture) •
[📚 Skills](#-skills-learned) •
[⚠️ Challenges](#️-challenges-encountered) •
[💭 Reflection](#-mission-reflection)

</p>

---

## 🔵 Mission Overview

As a **Cloud Engineer for CloudNova Technologies**, I conducted a comprehensive cloud infrastructure assessment using the **KillerCoda Linux environment**.

The goal of this mission was to investigate a Linux-based cloud server, identify its core **compute, storage, networking, and operating system resources**, and document the findings as a technical blueprint for a future cloud deployment.

This mission also involved comparing the infrastructure services of **Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP)** and creating a simple cloud architecture diagram.

---

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

The **Intel Xeon E312xx CPU** provides the processing capability of the cloud server. CPU resources are essential because cloud applications require processing power to execute programs, handle requests, and perform computational tasks.

### 🔴 Storage Resources

The environment provides approximately **21 GB of virtual disk capacity**. Storage is required for the operating system, application files, configuration files, logs, and other data.

### 🔵 Networking Resources

The server uses a **private IP address (`172.30.1.2`)** within its virtual network. Networking allows the server to communicate with other systems and cloud infrastructure components.

### 🔴 Operating System

The server runs **Ubuntu 24.04.4 LTS (Noble Numbat)**. The operating system manages the hardware resources and provides the environment required to run cloud applications and services.

---

## 🛠️ Tools Used

| 🔧 Tool               | 🎯 Purpose                              |
| --------------------- | --------------------------------------- |
| 🔵 **KillerCoda**     | Linux-based cloud server investigation  |
| 🔴 **GitHub**         | Portfolio hosting and version control   |
| 🔵 **Canva**          | Cloud architecture diagram design       |
| 🔴 **Markdown**       | Technical documentation                 |
| 🔵 **Linux Terminal** | System and infrastructure investigation |

---

## ⌨️ Linux Commands Executed

The following commands were used to investigate and collect information from the Linux cloud environment.

### 1. `hostname`

**Purpose:**
Displays the hostname of the Linux server.

```bash
hostname
```

**Use in this mission:**
Used to identify the name assigned to the cloud server.

---

### 2. Operating System Information

**Purpose:**
Identifies the Linux distribution and version.

```bash
grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"'
```

**Use in this mission:**
Used to determine that the environment is running **Ubuntu 24.04.4 LTS**.

---

### 3. `uname -r`

**Purpose:**
Displays the Linux kernel version.

```bash
uname -r
```

**Use in this mission:**
Used to identify the kernel currently running on the server.

---

### 4. CPU Model

**Purpose:**
Displays information about the processor.

```bash
lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs
```

**Use in this mission:**
Used to identify the available CPU model.

---

### 5. `nproc`

**Purpose:**
Displays the number of available processing units.

```bash
nproc
```

**Use in this mission:**
Used to determine the number of CPU cores available to the environment.

---

### 6. RAM Information

**Purpose:**
Displays information about system memory.

```bash
free -h | awk '/Mem:/ {print $2}'
```

**Use in this mission:**
Used to determine the total RAM available to the cloud server.

---

### 7. Disk Capacity

**Purpose:**
Displays disk usage and available storage.

```bash
df -h --total | grep total | awk '{print $2}'
```

**Use in this mission:**
Used to determine the total available disk capacity.

---

### 8. Root Disk Information

**Purpose:**
Displays the size of the root filesystem.

```bash
df -h / | awk 'NR==2 {print $2}'
```

**Use in this mission:**
Used to identify the capacity of the root filesystem.

---

### 9. Mounted File Systems

**Purpose:**
Displays storage devices, partitions, sizes, and mount points.

```bash
lsblk -lo NAME,SIZE,MOUNTPOINT
```

**Use in this mission:**
Used to inspect the server's storage structure and mounted filesystems.

---

### 10. IP Address

**Purpose:**
Displays the IP addresses assigned to the server.

```bash
hostname -I
```

**Use in this mission:**
Used to identify the server's network addresses, including the private IP address.

---

## 🚀 Combined Infrastructure Information Command

The following command block combines several Linux commands to collect the main infrastructure information in one execution.

```bash
cat <<EOF
Hostname: $(hostname)
Operating System: $(grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"')
Kernel Version: $(uname -r)
CPU Model: $(lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs)
CPU Cores: $(nproc)
Total RAM: $(free -h | awk '/Mem:/ {print $2}')
Total Disk Capacity: $(df -h --total | grep total | awk '{print $2}')
Root Filesystem: $(df -h / | awk 'NR==2 {print $2}')
Mounted Filesystems:
$(lsblk -lo NAME,SIZE,MOUNTPOINT | grep -E 'vda1|vda15|vda16' | awk '{printf "%-7s %-7s %s\n", $1, $2, $3}')
IP Address: $(hostname -I | awk '{print $1}')
Secondary IP: $(hostname -I | awk '{print $2}')
EOF
```

### 📌 Why Use a Combined Command?

Instead of manually executing every command separately, this script collects the major infrastructure details in a single formatted output.

This makes it easier to:

* 🔵 Collect system information.
* 🔴 Reduce repetitive commands.
* 🔵 Prepare the infrastructure report.
* 🔴 Verify server specifications.
* 🔵 Capture evidence for documentation.

---

## ☁️ Cloud Providers

Three major public cloud providers were considered for the infrastructure comparison:

| Infrastructure Component         | 🔶 AWS     | 🔷 Microsoft Azure             | 🔵 Google Cloud       |
| -------------------------------- | ---------- | ------------------------------ | --------------------- |
| **Compute**                      | Amazon EC2 | Azure Virtual Machines         | Compute Engine        |
| **Storage**                      | Amazon S3  | Azure Blob Storage             | Cloud Storage         |
| **Networking**                   | Amazon VPC | Azure Virtual Network          | Virtual Private Cloud |
| **Identity & Access Management** | AWS IAM    | Microsoft Entra ID / Azure IAM | Cloud IAM             |

### Which provider offers the broadest range of services?

All three major cloud providers offer a broad range of infrastructure, application, database, networking, storage, security, and AI-related services. The exact breadth depends on the category being considered and the specific requirements of an organization.

### Which platform would you recommend for an organization that primarily uses Microsoft products?

**Microsoft Azure** would be a strong choice because it integrates closely with Microsoft's existing ecosystem. Organizations already using Microsoft technologies can benefit from Azure's integration with Microsoft identity, productivity, and enterprise services.

### Which platform is widely recognized for AI, ML, and Kubernetes services?

**Google Cloud Platform (GCP)** is widely recognized for its strengths in artificial intelligence, machine learning, and Kubernetes technologies.

### What similarities were observed?

AWS, Azure, and GCP all provide comparable fundamental cloud infrastructure services, including compute, storage, networking, and identity and access management. They use different product names and interfaces, but the underlying infrastructure concepts are similar.

---

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

## 📚 Skills Learned

During this laboratory activity, I developed the following skills:

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

One challenge was understanding how individual Linux commands could be combined to collect infrastructure information efficiently. I also needed to understand how hardware resources available in a Linux environment relate to cloud infrastructure concepts.

Another challenge was comparing AWS, Azure, and GCP because each provider uses different names for services that perform similar functions.

Creating a structured technical document was also important because the information needed to be organized clearly enough for another engineer to understand.

---

## 💭 Mission Reflection

This laboratory helped me understand that cloud computing is not only about deploying applications but also about understanding the infrastructure that supports those applications. Investigating the KillerCoda Linux environment allowed me to see how compute, storage, networking, and operating system resources work together.

I learned that compute resources provide processing power, storage resources maintain data, networking resources connect systems, and the operating system manages the overall environment. Linux is especially useful in cloud computing because it provides powerful command-line tools for monitoring and managing servers.

I also learned the importance of technical documentation before deploying infrastructure. Proper documentation provides engineers with a clear reference of the resources, configurations, and decisions involved in a system. It can also make troubleshooting and future maintenance easier.

Another important skill I developed was comparing cloud services between AWS, Azure, and GCP. Although the providers use different product names, their fundamental infrastructure concepts are similar.

Finally, this mission improved my GitHub Cloud Computing Portfolio by adding a structured laboratory project containing technical reports, infrastructure documentation, commands, screenshots, and an architecture diagram. It demonstrates my ability to investigate a cloud environment and communicate technical information in an organized way.

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

## 🔵 CLOUD ENGINEERING • LINUX • INFRASTRUCTURE • DOCUMENTATION 🔴

**CCM101 – Cloud Computing**

*Mission 2 Completed*

---

<p align="center">

🔵 **CLOUDNOVA TECHNOLOGIES** 🔴
☁️ **Cloud Infrastructure Assessment** ☁️

</p>

<p align="center">

[🏠 Overview](#-mission-overview) •
[🏗️ Infrastructure](#️-cloud-infrastructure-components) •
[⌨️ Commands](#️-linux-commands-executed) •
[☁️ Providers](#️-cloud-providers) •
[📐 Architecture](#-cloud-architecture) •
[💭 Reflection](#-mission-reflection)

</p>

<p align="center">

⬆️ [Back to Top](#-mission-2-build-the-cloud-infrastructure-blueprint)

</p>
