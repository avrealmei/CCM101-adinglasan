# ☁️ Cloud Components

<p align="center">

### 🔵 CCM101 – Cloud Computing 🔴

**CloudNova Technologies | Cloud Infrastructure Blueprint**



---

## 📌 Project Information

| Information | Details |
|---|---|
| **Project** | CloudNova Technologies - Blueprint Phase |
| **Date** | August 25, 2026 |
| **Mission** | Mission 2 – Build the Cloud Infrastructure Blueprint |
| **Environment** | KillerCoda Linux Playground |
| **Operating System** | Ubuntu 24.04.4 LTS |
| **Infrastructure Type** | Virtualized Linux Server |

---

In this mission, I analyzed a virtualized Linux server. Below is the mapping of hardware resources to core cloud infrastructure components.

The purpose of this document is to explain how the resources discovered during the Linux investigation relate to fundamental cloud computing concepts.

---

<!-- ===================================================== -->
<!-- 🔵 COMPUTE -->
<!-- ===================================================== -->

<a id="compute-resources"></a>

# 🔵 Compute Resources

*   **Purpose:** Compute resources provide the "brain" of the server, including the CPU for processing instructions and RAM for temporary data storage during active tasks.
*   **Importance in Cloud:** In the cloud, compute is scalable. It allows businesses to pay only for the processing power they need, whether it is a small micro-service or a massive database.
*   **KillerCoda Relationship:** My investigation revealed an **Intel Xeon E312xx CPU** with **1 CPU core** and **1.9GiB of RAM**. This represents a "General Purpose" compute instance, similar to an AWS t3.micro.

---

## ⚙️ Compute Resource Breakdown

| Resource | KillerCoda Finding | Function |
|---|---|---|
| 🔵 **CPU** | Intel Xeon E312xx | Executes instructions and processes workloads |
| 🔵 **CPU Cores** | 1 Core | Provides processing capacity |
| 🔵 **RAM** | 1.9 GiB | Temporarily stores active data and instructions |
| 🔵 **Compute Type** | Virtualized | Provides isolated virtual computing resources |

### 🎯 Purpose

The CPU and RAM work together to execute applications and maintain active processes.

The **CPU** performs calculations and executes instructions, while **RAM** temporarily holds the information that the operating system and applications are actively using.

### 💡 Deeper Understanding

In a physical server, CPU and memory are installed directly on the hardware.

In a cloud environment, these resources are usually **virtualized and allocated to virtual machines**.

For example:

```text
Physical Server
      │
      ▼
┌───────────────────────┐
│     Hypervisor        │
└───────────────────────┘
      │
      ├───────────────┐
      ▼               ▼
 Virtual Machine   Virtual Machine
      │               │
   CPU + RAM       CPU + RAM
