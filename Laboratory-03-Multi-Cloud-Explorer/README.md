cat << 'EOF' > README.md
<div align="center">

# ☁️ CCM101 Laboratory 03: Multi-Cloud Explorer 🚀

<p align="center">
  <a href="#student-information"><b>👤 Student Info</b></a> &nbsp;&bull;&nbsp;
  <a href="#checkpoint-7-linux-server-investigation--cloud-migration-mapping"><b>💻 System Specs</b></a> &nbsp;&bull;&nbsp;
  <a href="#cloud-hosting-equivalence-mapping"><b>🌐 Cloud Mapping</b></a> &nbsp;&bull;&nbsp;
  <a href="https://github.com/avrealmei/CCM101-adinglasan" target="_blank"><b>📂 Repository</b></a>
</p>

</div>

---

## 👤 Student Information
* **Name:** Avril Mei Agaoid Dinglasan
* **Course & Section:** BSIT - University of Eastern Pangasinan
* **Repository:** `CCM101-adinglasan`

---

## 💻 Checkpoint 7: Linux Server Investigation & Cloud Migration Mapping

### 📊 System Information Collected via Terminal
* **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)
* **CPU Information:** Intel Xeon E312xx (Sandy Bridge) @ 2.0GHz (1 Core, x86_64 architecture, KVM Virtualization)
* **Memory (RAM):** 1.9 GiB total (~1.4 GiB available)
* **Disk Space:** 19 GB root filesystem (`/dev/vda1`), with 5.4 GB used and 13 GB available (30% usage)

### ☁️ Cloud Hosting Equivalence Mapping
If this specific Linux server environment were migrated to the public cloud, it could be hosted on the following infrastructure-as-a-service (IaaS) virtual machine offerings:

| Cloud Provider | Hosting Service | Description / Application |
| :--- | :--- | :--- |
| **Amazon Web Services (AWS)** | Amazon EC2 (Elastic Compute Cloud) | Provides scalable virtual server instances (such as `t3.micro` or `t3.small` types) running standard Ubuntu 24.04 AMIs. |
| **Microsoft Azure** | Azure Virtual Machines | Offers scalable Linux virtual machines configured with Ubuntu Server images and enterprise-grade networking. |
| **Google Cloud Platform (GCP)** | Google Compute Engine (GCE) | Delivers customizable virtual machine instances running Linux with high-performance networking and storage. |

---

<div align="center">
  <p><i>"The cloud is not a destination, it's a different way of doing computing." — Peter Levine</i></p>
</div>
EOF
