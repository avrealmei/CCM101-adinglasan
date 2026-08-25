## Cloud Components
**Project:** CloudNova Technologies - Blueprint Phase
**Date:** August 25, 2026

In this mission, I analyzed a virtualized Linux server. Below is the mapping of hardware resources to core cloud infrastructure components.

---

## 1. Compute Resources
*   **Purpose:** Compute resources provide the "brain" of the server, including the CPU for processing instructions and RAM for temporary data storage during active tasks.
*   **Importance in Cloud:** In the cloud, compute is scalable. It allows businesses to pay only for the processing power they need, whether it is a small micro-service or a massive database.
*   **KillerCoda Relationship:** My investigation revealed an **Intel Xeon E312xx CPU** with **1 CPU core** and **1.9GiB of RAM**. This represents a "General Purpose" compute instance, similar to an AWS t3.micro.

## 2. Storage Resources
*   **Purpose:** Storage provides a persistent location for data, applications, and the Operating System. Unlike RAM, data remains safe here even when the power is off.
*   **Importance in Cloud:** Cloud storage (Block Storage) is decoupled from the hardware, meaning data can be easily backed up, snapshotted, or moved between different virtual machines.
*   **KillerCoda Relationship:** I identified a **21GB Disk** using virtual block devices (**vda**). The root partition (**/**) is 19GB, which houses the system files and user data.

## 3. Networking Resources
*   **Purpose:** Networking components allow the server to communicate with other servers, internal databases, and the public internet.
*   **Importance in Cloud:** Networking defines the security boundary (VPC/VNet). It manages data traffic through IP addresses, subnets, and firewalls to ensure only authorized users can access the system.
*   **KillerCoda Relationship:** The system is assigned a private IP address of **172.30.1.2**. This identifies the instance within the virtual private network provided by the KillerCoda infrastructure.

## 4. Operating System
*   **Purpose:** The OS acts as the interface between the hardware and the software applications. It manages system resources and security.
*   **Importance in Cloud:** Cloud providers offer "Images" (AMIs or VHDs) of Operating Systems. Choosing an LTS (Long Term Support) version is critical for enterprise stability and security updates.
*   **KillerCoda Relationship:** The environment is running **Ubuntu 24.04.4 LTS**. This is a modern, high-performance Linux distribution widely used in professional cloud deployments for its stability and security.

---
**Summary:** Understanding these components is essential for the planning phase. Each resource must be balanced to ensure the migrated services are both performant and cost-effective.
