<div align="center">

# 🔵 CLOUD INFRASTRUCTURE ASSESSMENT 🔴

### CCM101 – Cloud Computing


**CloudNova Technologies**
*Cloud Infrastructure Blueprint*

</div>

---

<div align="center">

### 🧭 NAVIGATION

[🏠 Mission 2](../README.md)   |  
[🔵 Checkpoint 2](#-checkpoint-2--cloud-server-investigation)   |  
[🔴 Evidence](#-evidence)

</div>

---

> 🔵 **Mission:** Build the Cloud Infrastructure Blueprint
>
> 🔴 **Checkpoint:** 2 – Investigate the Cloud Server
>
> 🖥️ **Environment:** KillerCoda Ubuntu 24.04 Playground

---

## 🔵 Checkpoint 2 – Cloud Server Investigation

### 📌 Purpose

The purpose of this checkpoint is to investigate the Linux server provided through the KillerCoda Playground.

The investigation focuses on identifying the server's:

* Operating System
* Kernel Version
* CPU Model
* Number of CPU Cores
* Total RAM
* Disk Capacity
* Mounted File Systems
* Hostname
* IP Address

These details provide a basic infrastructure profile that can be used when planning and documenting a cloud environment.

---

## 🧪 Investigation Environment

| Category                 | Information              |
| :----------------------- | :----------------------- |
| **Platform**             | KillerCoda Playground    |
| **Operating System**     | Ubuntu 24.04.4 LTS       |
| **Server Type**          | Virtualized Linux Server |
| **Virtualization**       | KVM Hypervisor           |
| **Investigation Method** | Linux Terminal Commands  |

---

# 🔵 1. System Identification

## 🖥️ Hostname

### Command

```bash
hostname
```

### Purpose

The `hostname` command displays the name assigned to the Linux server.

### Explanation

A hostname provides an identifier for a server inside a network or cloud environment. It is useful when managing multiple servers because administrators can distinguish one machine from another.

### Example

```text
ubuntu
```

### Result

**Hostname:** `ubuntu`

---

## 🐧 Operating System

### Command

```bash
grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"'
```

### Purpose

This command identifies the name and version of the operating system.

### Explanation

The `/etc/os-release` file contains information about the installed Linux distribution. The command searches for `PRETTY_NAME`, extracts the value, and removes the quotation marks.

### Example

```text
Ubuntu 24.04.4 LTS
```

### Result

**Operating System:** `Ubuntu 24.04.4 LTS (Noble Numbat)`

---

## ⚙️ Kernel Version

### Command

```bash
uname -r
```

### Purpose

The `uname -r` command displays the currently running Linux kernel version.

### Explanation

The Linux kernel manages important system resources such as CPU, memory, hardware devices, processes, and networking.

### Example

```text
6.8.0-138-generic
```

### Result

**Kernel Version:** `6.8.0-138-generic`

---

# 🔴 2. Compute Resources

## 🧠 CPU Model

### Command

```bash
lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs
```

### Purpose

This command retrieves the CPU model detected by the Linux system.

### Explanation

`lscpu` displays detailed CPU information. The command filters the output to find the CPU model and cleans the formatting so that only the model is displayed.

### Example

```text
Intel Xeon E312xx (Sandy Bridge, IBRS update)
```

### Result

**CPU Model:** `Intel Xeon E312xx (Sandy Bridge, IBRS update)`

---

## 🔢 Number of CPU Cores

### Command

```bash
nproc
```

### Purpose

The `nproc` command displays the number of processing units available to the system.

### Explanation

In cloud computing, CPU resources are commonly allocated to virtual machines as virtual CPUs or vCPUs. This value represents the compute capacity available to the server.

### Example

```text
1
```

### Result

**CPU Cores:** `1 Core`

---

## 🧮 Compute Summary

| Compute Resource   | Detected Value        |
| :----------------- | :-------------------- |
| **CPU Model**      | Intel Xeon E312xx     |
| **CPU Cores**      | 1 Core                |
| **Virtualization** | Full (KVM Hypervisor) |
| **RAM**            | 1.9 GiB               |

---

# 🔵 3. Memory Resources

## 💾 Total RAM

### Command

```bash
free -h | awk '/Mem:/ {print $2}'
```

### Purpose

This command determines the total amount of RAM available to the Linux server.

### Explanation

`free -h` displays memory statistics in a human-readable format. The `awk` portion extracts the total memory value from the `Mem:` row.

### Example

```text
1.9Gi
```

### Result

**Total RAM:** `1.9 GiB (approximately 2 GB)`

---

# 🔴 4. Storage Resources

## 💽 Total Disk Capacity

### Command

```bash
df -h --total | grep total | awk '{print $2}'
```

### Purpose

This command determines the total disk capacity available across the mounted file systems.

### Explanation

`df -h` reports disk space usage in a human-readable format. The `--total` option produces a total value, while `awk` extracts the disk capacity.

### Example

```text
21G
```

### Result

**Total Disk Capacity:** `21 GB`

---

## 💿 Main Root Partition

### Command

```bash
df -h / | awk 'NR==2 {print $2}'
```

### Purpose

This command determines the size of the filesystem mounted at the root directory `/`.

### Explanation

The root filesystem contains the main Linux operating system and many files required for the server to operate.

### Example

```text
19G
```

### Result

**Main Partition:** `19 GB (/dev/vda1)`

---

## 📦 Mounted File Systems

### Command

```bash
lsblk -lo NAME,SIZE,MOUNTPOINT
```

### Purpose

The `lsblk` command displays available block devices, their sizes, and their mount points.

### Explanation

This command is useful for understanding how storage devices and partitions are organized. In a cloud environment, virtual disks are commonly presented as block devices.

### Example

```text
NAME    SIZE  MOUNTPOINT
vda1    19G   /
vda15   106M  /boot/efi
vda16   913M  /boot
```

### Result

| Device  | Size | Mount Point |
| :------ | ---: | :---------- |
| `vda1`  |  19G | `/`         |
| `vda15` | 106M | `/boot/efi` |
| `vda16` | 913M | `/boot`     |

---

# 🔵 5. Networking Resources

## 🌐 IP Address

### Command

```bash
hostname -I
```

### Purpose

The `hostname -I` command displays the IP addresses assigned to the server.

### Explanation

IP addresses allow systems to communicate across a network. Cloud servers normally operate within virtual networks where private IP addresses are assigned to individual instances.

### Example

```text
172.30.1.2 172.17.0.1
```

### Results

| Network Address | Description                     |
| :-------------- | :------------------------------ |
| `172.30.1.2`    | Primary private IP address      |
| `172.17.0.1`    | Internal/Docker network address |

---

## 🎯 Primary IP Address

### Command

```bash
hostname -I | awk '{print $1}'
```

### Purpose

This command extracts the first IP address returned by the system.

### Explanation

`hostname -I` can return multiple addresses. `awk '{print $1}'` selects the first address for use as the primary IP value.

### Example

```text
172.30.1.2
```

### Result

**Primary IP Address:** `172.30.1.2`

---

## 🔌 Internal/Docker IP

### Command

```bash
hostname -I | awk '{print $2}'
```

### Purpose

This command extracts the second IP address returned by the system.

### Explanation

The second address represents another internal or virtual networking environment available to the server.

### Example

```text
172.17.0.1
```

### Result

**Internal/Docker IP:** `172.17.0.1`

---

# 🔴 6. Complete Infrastructure Command

The following is the original combined command used to collect the infrastructure information in one execution.

### Command

```bash
cat <<EOF
\$(hostname)
\$(grep "PRETTY_NAME" /etc/os-release | cut -d'=' -f2 | tr -d '"')
\$(uname -r)
\$(lscpu | grep "Model name" | sed 's/Model name: *//' | head -n 1 | xargs)
\$(nproc) Core
\$(free -h | awk '/Mem:/ {print \$2}')
\$(df -h --total | grep total | awk '{print \$2}')
\$(df -h / | awk 'NR==2 {print \$2}') (/dev/vda1)
\$(lsblk -lo NAME,SIZE,MOUNTPOINT | grep -E 'vda1 |vda15|vda16' | awk '{printf "%-7s %-7s %s\n", \$1, \$2, \$3}')
\$(hostname -I | awk '{print \$1}')
\$(hostname -I | awk '{print \$2}')
EOF
```

### Purpose

The purpose of this command block is to collect the major infrastructure details required for Checkpoint 2 in a single structured output.

### Explanation

The command combines several Linux utilities to gather system information:

| Command / Utility | Purpose                              |
| :---------------- | :----------------------------------- |
| `hostname`        | Identifies the server                |
| `grep`            | Searches for specific information    |
| `cut`             | Extracts fields from text            |
| `tr`              | Removes unwanted characters          |
| `uname`           | Retrieves kernel information         |
| `lscpu`           | Displays CPU information             |
| `sed`             | Cleans and transforms text           |
| `nproc`           | Counts available processing units    |
| `free`            | Displays memory information          |
| `df`              | Displays filesystem disk usage       |
| `lsblk`           | Displays block devices               |
| `awk`             | Extracts and formats specific fields |

### Example Output

```text
ubuntu
Ubuntu 24.04.4 LTS
6.8.0-138-generic
Intel Xeon E312xx (Sandy Bridge, IBRS update)
1 Core
1.9Gi
21G
19G (/dev/vda1)
vda1    19G     /
vda15   106M    /boot/efi
vda16   913M    /boot
172.30.1.2
172.17.0.1
```

---

# 🔵 7. Infrastructure Assessment Summary

| Infrastructure Category  | Resource           | Detected Value     |
| :----------------------- | :----------------- | :----------------- |
| 🖥️ **Operating System** | OS                 | Ubuntu 24.04.4 LTS |
| ⚙️ **Kernel**            | Version            | 6.8.0-138-generic  |
| 🧠 **Compute**           | CPU                | Intel Xeon E312xx  |
| 🔢 **Compute**           | CPU Cores          | 1 Core             |
| 💾 **Memory**            | RAM                | 1.9 GiB            |
| 💽 **Storage**           | Total Disk         | 21 GB              |
| 📦 **Storage**           | Root Partition     | 19 GB              |
| 🌐 **Networking**        | Primary IP         | 172.30.1.2         |
| 🔌 **Networking**        | Internal/Docker IP | 172.17.0.1         |
| 🖥️ **Hostname**         | Server Name        | ubuntu             |
| ☁️ **Virtualization**    | Hypervisor         | KVM                |

---

# 🔴 8. Technical Observations

Based on the investigation, the KillerCoda server is a **virtualized Linux instance running on a KVM hypervisor**.

The server has **1 CPU core and approximately 1.9 GiB of RAM**, making it suitable for lightweight workloads such as basic web services, testing environments, small applications, and development activities.

The storage environment uses virtual block devices such as `vda`, which is common in virtualized and cloud-based Linux environments.

The server also has private networking addresses, including `172.30.1.2` and `172.17.0.1`, demonstrating that the environment uses virtual networking.

---

# 🧭 9. Relationship to Cloud Infrastructure

```text
                    🔴 INTERNET
                         │
                         ▼
                ┌─────────────────┐
                │ 🔵 NETWORK      │
                │ 172.30.1.2      │
                └────────┬────────┘
                         │
                         ▼
                ┌─────────────────┐
                │ 🖥️ COMPUTE      │
                │ Intel Xeon      │
                │ 1 CPU Core      │
                │ 1.9 GiB RAM     │
                └────────┬────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
       ┌──────────────┐      ┌──────────────┐
       │ 🐧 UBUNTU    │      │ 💾 STORAGE   │
       │ 24.04.4 LTS  │      │ 21 GB        │
       └──────────────┘      │ /dev/vda1    │
                             └──────────────┘
```

This demonstrates that cloud infrastructure is not composed of a single resource. Compute, storage, networking, and the operating system work together to provide a functional server environment.

---

# 📸 Evidence

Screenshots were captured from the KillerCoda terminal to verify the investigation results.

### 🖥️ Server Information

```text
screenshots/server-information.png
```

### 🌐 Network Information

```text
screenshots/network-information.png
```

### 💽 Storage Information

```text
screenshots/storage-information.png
```

---

# 🔵 Checkpoint 2 Completion

* [x] Operating System identified
* [x] Kernel Version identified
* [x] CPU Model identified
* [x] CPU Core Count identified
* [x] Total RAM identified
* [x] Disk Capacity identified
* [x] Mounted File Systems identified
* [x] Hostname identified
* [x] IP Address identified
* [x] Linux commands documented
* [x] Purpose of commands explained
* [x] Examples provided
* [x] Technical observations documented
* [x] Evidence screenshots prepared
* [x] Report committed to GitHub

---

<div align="center">

## 🔵 CLOUDNOVA TECHNOLOGIES 🔴

**CCM101 – Cloud Computing**

*Build systems. Document decisions. Engineer the cloud.*

---

[🏠 Mission 2](../README.md)   |  
[🔵 Checkpoint 2](#-checkpoint-2--cloud-server-investigation)   |  
[🔴 Evidence](#-evidence)

</div>
