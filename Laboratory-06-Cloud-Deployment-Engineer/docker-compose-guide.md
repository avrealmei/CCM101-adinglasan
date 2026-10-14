 <div align="center">

# 🐳 DOCKER COMPOSE GUIDE

[![Docker](https://img.shields.io/badge/DOCKER-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Docker Compose](https://img.shields.io/badge/DOCKER_COMPOSE-DC2626?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![Mission](https://img.shields.io/badge/MISSION-06-123B78?style=for-the-badge)](#overview)

</div>

---

<div align="center">

[🔵 OVERVIEW](#overview)　|　[🔴 COMMANDS](#docker-compose-commands)　|　[🔵 DOCUMENTATION](#technical-explanation)

</div>

---

## Overview

In this checkpoint, I documented the Docker Compose configuration used to deploy Nextcloud and its database. The purpose of this documentation is to explain how the services are configured, how they communicate with each other, and how Docker Compose makes application deployment easier.

Docker Compose allows developers to define multiple application services in one YAML file. Instead of manually configuring every container, the services can be managed together using a single command.

## Technical Explanation

### 🔵 1. What Does the `services:` Block Do?

The `services:` block defines the different services that make up an application. Each service describes how its container should run, including its Docker image, environment variables, ports, volumes, and other configuration settings.

For this deployment, the services include:

- 🔵 **Nextcloud:** The application container that provides the web interface and cloud storage functionality.
- 🔴 **MySQL:** The database container that stores information required by the application.

By placing both services in the same Compose file, I can manage them together instead of manually configuring each container separately. This makes deployment more organized and easier to maintain.

### 🔴 2. How Does Nextcloud Find the Database Container?

Nextcloud uses the `MYSQL_HOST` environment variable to identify the hostname of the database service.

For example, the configuration may contain:

```yaml
environment:
  MYSQL_HOST: db
```

In this example, `db` must match the name of the database service defined in the Compose file.

Docker Compose creates a default network for the application. Containers connected to this network can communicate using their service names. Because of this, Nextcloud can use `db` as the database hostname without needing to find the database container's IP address manually.

**Important:** The value of `MYSQL_HOST` must match the actual database service name in the YAML file. If the database service is named `mysql`, for example, the hostname should be changed to `mysql`.

### 🔵 3. Difference Between `docker run` and `docker compose up -d`

Both commands can start containers, but they differ in how containers are configured and managed.

| Feature | 🔵 `docker run` | 🔴 `docker compose up -d` |
|---|---|---|
| Configuration | Uses command-line options | Uses a YAML configuration file |
| Containers | Usually starts one container per command | Can start multiple related services |
| Networking | May require additional network configuration | Creates and manages the default Compose network |
| Management | Containers are configured individually | Related services are managed together |
| Background mode | Uses `-d` to run in the background | Uses `-d` to run in the background |

In Mission 4, I used `docker run` to start a container directly through the terminal. In this mission, `docker compose up -d` allows Docker Compose to create or start the services defined in the YAML file.

The `up` command creates or starts the configured services, while `-d` means detached mode. This allows the containers to run in the background while I continue using the terminal for other tasks.

## Docker Compose Commands

The following commands can be used when working with the deployment. Run them from the directory containing your Docker Compose YAML file.

```bash
# Check the Docker version
docker --version

# Check the Docker Compose version
docker compose version

# Validate the Compose configuration
docker compose config

# Start the application services in the background
docker compose up -d

# Check the status of the containers
docker compose ps

# View the service logs
docker compose logs

# Stop and remove the containers and network
docker compose down
```

> 🔴 **Reminder:** These are standard commands for this workflow. Only report them as executed if you actually ran them in your laboratory environment.

## What I Learned

Through this checkpoint, I learned how Docker Compose organizes multiple application services in a single YAML file. I also understood how the `MYSQL_HOST` environment variable helps Nextcloud locate the database through Docker's service discovery.

I realized that Docker Compose is useful because it reduces repetitive commands and makes deployments easier to manage. As a fourth-year BSIT student, this activity helped me better understand how containers, networks, and databases work together when deploying a cloud application.

## Conclusion

This activity improved my understanding of multi-container deployment and technical documentation. I learned that a properly configured Compose file can simplify application deployment, but YAML indentation, service names, and environment variables must be correct for the services to work properly.

These concepts will be useful in future cloud computing activities and real-world IT infrastructure projects.

---

<div align="center">

[🔵 BACK TO LABORATORY README](./README.md)

---

🔵 **LEARN**　•　**CONFIGURE**　•　🔴 **DEPLOY**

**CCM101 – Cloud Computing Laboratory**

*Prepared by: Avril Mei A. Dinglasan*

</div>
