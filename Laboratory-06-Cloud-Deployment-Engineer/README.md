 <div align="center">

# ☁️ CLOUDNOVA TECHNOLOGIES

### 🔵 CLOUD DEPLOYMENT ENGINEER 🔴

**CCM101 – Cloud Computing Laboratory**

[![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Docker_Compose-Multi--Container-DC2626?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![Laboratory](https://img.shields.io/badge/Laboratory-06-123B78?style=for-the-badge)](#-mission-overview)

---

[🏠 HOME](./README.md)　|　[🎯 OBJECTIVES](./README.md#-objectives)　|　[💻 COMMANDS](./README.md#-commands-executed)　|　[📘 DOCUMENTATION](./docker-compose-guide.md)

---

</div>

## 📌 Mission Overview

The purpose of this laboratory activity is to understand how Docker Compose simplifies the deployment and management of applications that use multiple containers.

In this mission, I studied how a Nextcloud application and a MySQL database can be configured as separate services in a Docker Compose YAML file. I also documented the configuration, explained how the application connects to the database, and reviewed the commands used to manage the deployment.

This activity helped me understand how containerization makes application deployment more organized, repeatable, and manageable.

## 🎯 Objectives

- Understand the purpose of the `services:` block in a Docker Compose YAML file.
- Explain how Nextcloud finds the database through the `MYSQL_HOST` environment variable.
- Differentiate `docker run` from `docker compose up -d`.
- Learn how to validate a Docker Compose configuration.
- Understand how to start, inspect, and stop containerized services.
- Practice writing technical documentation using Markdown.

## 💻 Commands Executed

The following commands are commonly used when working with Docker Compose.

| Command | Description |
|---|---|
| `docker --version` | Checks the installed Docker version. |
| `docker compose version` | Checks the Docker Compose version. |
| `docker compose config` | Validates and displays the resolved configuration. |
| `docker compose up -d` | Creates or starts the configured services in the background. |
| `docker compose ps` | Displays the status of the Compose containers. |
| `docker compose logs` | Displays service logs for troubleshooting. |
| `docker compose down` | Stops and removes the Compose containers and network. |

**Note:** This section lists the commands relevant to the deployment workflow. I will mark these as executed only after running them in the laboratory environment.

## 🧠 Skills Learned

### 🐳 Docker Compose

I learned how Docker Compose uses a YAML file to define and manage multiple related application services. This makes it easier to configure and deploy an application without manually starting every container separately.

### 🌐 Container Networking

I learned that Docker Compose provides a network where services can communicate using their service names. For example, Nextcloud can connect to MySQL through the hostname specified in `MYSQL_HOST`, as long as it matches the database service name.

### 🗄️ Application and Database Integration

I gained a better understanding of how an application communicates with a database to store and retrieve information. Both containers must have the correct configuration and network connectivity to work together.

### ⌨️ Command-Line Operations

I learned how to validate configurations, start services in detached mode, inspect container status, view logs, and stop a deployment using Docker Compose commands.

### 📝 Technical Documentation

I practiced documenting technical concepts and commands using Markdown. Clear documentation helps other developers understand, troubleshoot, and reproduce an application deployment.

## 📘 Technical Documentation

Read the complete guide for the Docker Compose configuration, including explanations of the `services:` block, the `MYSQL_HOST` environment variable, and the difference between `docker run` and `docker compose up -d`.

**➡️ [Open the Docker Compose Guide](./docker-compose-guide.md)**

## 📝 Reflection

As a fourth-year BSIT student, this activity helped me understand how Docker Compose can simplify the deployment of applications that require multiple services. I learned that the application and database can run in separate containers while communicating through a shared Docker network.

I also realized that proper configuration and technical documentation are important when managing cloud infrastructure. These skills will be useful in future cloud computing activities and real-world IT projects.

---

<div align="center">

🔵 **LEARN**　•　**CONFIGURE**　•　🔴 **DEPLOY**

**CCM101 – Cloud Computing Laboratory**

*Prepared by: Avril Mei A. Dinglasan*

</div>
