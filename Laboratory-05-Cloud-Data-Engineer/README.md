<div align="center">

# ☁️ Laboratory Activity 5: Mission 5 - The Cloud Data Engineer

[![Cloud Computing](https://img.shields.io/badge/Course-CCM101%20Cloud%20Computing-blue?style=for-the-badge&logo=cloud&logoColor=white)](https://github.com/)
[![Mission Status](https://img.shields.io/badge/Status-Completed-red?style=for-the-badge&logo=docker&logoColor=white)](https://github.com/)

[📁 **Back to Portfolio Root**](../../README.md) &nbsp;&bull;&nbsp; [📂 **Laboratory 4**](../Laboratory-04-Web-Server-Deployment/README.md) &nbsp;&bull;&nbsp; [🚀 **MinIO Documentation**](./minio-deployment.md)

</div>

---

## 🚀 Mission Overview
Congratulations! Your seamless deployment of containerized web servers has caught the attention of the senior architects. You have now been temporarily reassigned to the Cloud Data Engineering Team at CloudNova Technologies. 

In the cloud, data is everything. However, not all data is stored the same way. While traditional computers use hard drives (Block Storage) and shared network drives (File Storage), modern cloud applications rely heavily on Object Storage to store massive amounts of unstructured data like images, videos, and backups. The industry standard for this is Amazon S3, but in this activity, we deployed an S3-compatible cloud storage server using an open-source tool called MinIO. Using a containerized environment, we combined Docker skills with cloud storage knowledge to launch a live object storage server, create a storage "bucket," and upload data over the web.

---

## 🎯 Mission Objectives
* 🔹 **Differentiate** between Block, File, and Object Storage architectures.
* 🔹 **Deploy** an S3-compatible Object Storage server (MinIO) using Docker CLI.
* 🔹 **Access** a cloud service via a web interface using port forwarding and network binding.
* 🔹 **Create** a storage bucket and upload objects (files) to the cloud console.
* 🔹 **Document** cloud storage operations and deployment steps using Markdown.
* 🔹 **Expand** a professional GitHub Cloud Computing Portfolio.

---

## 🛠️ Tools Used
* 🐳 **Docker Engine:** Container platform used to pull and run the MinIO server image.
* 🗄️ **MinIO (`pgsty/minio`):** High-performance, S3-compatible object storage server.
* 💻 **KillerCoda / Ubuntu 24.04 Environment:** Virtualized Linux playground for running terminal commands and configuring port forwarding.
* 🐙 **Git & GitHub:** Version control system used to track files and publish portfolio documentation.

---

## 💡 Skills Learned
* 🔸 Implementing cloud storage principles and evaluating the differences between Block, File, and Object Storage architectures.
* 🔸 Deploying containerized enterprise services via Docker CLI with explicit port mappings (`-p`) and network bindings (`0.0.0.0`).
* 🔸 Utilizing environment variables (`-e`) to pass runtime root credentials (`MINIO_ROOT_USER` and `MINIO_ROOT_PASSWORD`) into container instances securely.
* 🔸 Managing S3 storage buckets and uploading digital assets via a live web management console.
* 🔸 Structuring professional technical documentation and maintaining a clean GitHub repository layout.
