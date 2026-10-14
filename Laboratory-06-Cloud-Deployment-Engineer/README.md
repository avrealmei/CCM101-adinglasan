# 🐳 Docker Compose Guide

<div align="center">

# 🔵 DOCKER COMPOSE DOCUMENTATION

**CCM101 – Cloud Computing**

[![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/Docker%20Compose-Multi--Container-0B5CAD?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![Status](https://img.shields.io/badge/Status-Completed-DC2626?style=for-the-badge)](#)

</div>

---

## 📌 Overview

This document explains how Docker Compose is used to deploy an application with multiple containers. In this laboratory activity, Docker Compose is used to define and manage the Nextcloud application and its MySQL database through a YAML configuration file.

Instead of configuring each container separately, Docker Compose allows the services, environment variables, and other settings to be organized in one file. This makes the deployment easier to manage, understand, and reproduce.

## 🧩 Understanding the Docker Compose YAML File

### 1. What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application. Each service describes how a container should run, including its image, environment variables, ports, and other configuration settings.

For this deployment, the services include:

- **Nextcloud:** The application container that provides the web interface and file-sharing functionality.
- **MySQL:** The database container that stores the application's data.

By defining both services in the same Compose file, Docker Compose can create and manage the containers together.

### 2. How Does Nextcloud Find the Database Container?

Nextcloud finds the database through the `MYSQL_HOST` environment variable.

For example:

```yaml
environment:
  MYSQL_HOST: db
```

In this example, `db` must match the name of the MySQL service in the Docker Compose YAML file.

Docker Compose creates a network for the application by default. Containers connected to that network can communicate using their service names. Therefore, Nextcloud can use `db` as the database hostname instead of requiring the database container's IP address.

This makes communication between containers simpler and more reliable because Docker Compose handles service discovery within the network.

**Important:** The value of `MYSQL_HOST` must match the actual MySQL service name defined in the YAML file. If the service is named `mysql` instead of `db`, the hostname should be updated accordingly.

### 3. Difference Between `docker run` and `docker-compose up -d`

Both commands can be used to start containers, but they serve different purposes.

| Feature | `docker run` | `docker compose up -d` |
|---|---|---|
| Configuration | Uses command-line options | Uses a Compose YAML file |
| Containers | Usually starts one container per command | Can start multiple related services |
| Networking | May require manual network configuration | Creates and manages the default application network |
| Management | Containers are configured individually | Services are managed together |
| Background execution | Requires the `-d` option to run in the background | The `-d` option runs services in the background |
| Best use | Running individual containers | Deploying multi-container applications |

In Mission 4, `docker run` was used to start a container directly through the terminal. In this mission, `docker compose up -d` is used to start the services defined in the Compose file.

The `up` command creates or starts the required services, while `-d` means detached mode. Detached mode allows the containers to continue running in the background while the terminal remains available for other commands.

## 💻 Commands Executed

The following are the main commands used when working with Docker Compose. Execute them from the directory containing the Compose YAML file.

```bash
# Check the installed Docker version
docker --version

# Check Docker Compose availability
docker compose version

# Validate the Compose configuration
docker compose config

# Start the application services in the background
docker compose up -d

# Check the running containers
docker compose ps

# View service logs
docker compose logs

# Stop the application services
docker compose down
```

**Note:** These are standard Docker Compose commands for this workflow. Only report a command as executed if you actually ran it during the laboratory activity.

## 🎯 Conclusion

Through this activity, I learned how Docker Compose simplifies the deployment of applications that depend on multiple containers. I also understood how service names and environment variables allow the Nextcloud application to communicate with its database.

Compared with running containers individually, Docker Compose provides a more organized and manageable way to configure, start, and stop related services. These concepts are useful when deploying applications that require separate application and database components.

---

<div align="center">

**Prepared by:** Avril Mei A. Dinglasan  
**Course:** BS Information Technology – 4th Year  
**Subject:** CCM101 – Cloud Computing

🔵 **LEARN • CONFIGURE • DEPLOY** 🔴

</div>
