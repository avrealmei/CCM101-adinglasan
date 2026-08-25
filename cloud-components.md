# Cloud Infrastructure Components

## 1. Compute Services
*   **What I found:** Intel Xeon E312xx CPU with 1.9GB RAM.
*   **Cloud Equivalent:** In AWS, this is similar to a `t2.small` or `t3.micro` instance. 
*   **Function:** This provides the processing power (CPU) and temporary memory (RAM) needed to run applications.

## 2. Storage Services
*   **What I found:** 20GB Virtual Disk (`/dev/vda`).
*   **Cloud Equivalent:** This is Block Storage (e.g., AWS EBS or Azure Managed Disks).
*   **Function:** It acts as a virtual hard drive to store the Operating System and persistent files.

## 3. Networking Services
*   **What I found:** IP Address `172.30.1.2`.
*   **Cloud Equivalent:** This represents a Virtual Private Cloud (VPC) or Virtual Network (VNet).
*   **Function:** It allows the cloud resource to communicate with other servers and the internet.

## 4. Identity & Access Management (IAM)
*   **Observation:** I logged in as `root`. 
*   **Function:** In a production cloud, we use IAM to restrict who can access this server via SSH keys or passwords.
