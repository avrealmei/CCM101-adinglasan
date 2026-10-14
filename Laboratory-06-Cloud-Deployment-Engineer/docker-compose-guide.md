 <div align="center">

# 🐳 DOCKER COMPOSE GUIDE

### 🔵 CLOUD DEPLOYMENT ENGINEER 🔴

**CCM101 – Cloud Computing Laboratory**


[🎯 OVERVIEW](./README.md#-objectives)　|　[💻 COMMANDS](./README.md#-commands-executed)　|　[📘 DOCUMENTATION](./docker-compose-guide.md)

---

</div>

## 📌 Overview

In this checkpoint, I documented the Docker Compose configuration used to deploy Nextcloud and its database. The purpose of this documentation is to explain how the services are configured, how they communicate with each other, and how Docker Compose makes deployment easier.

## 🧩 1. What Does the `services:` Block Do?

The `services:` block defines the different services that make up an application. In a Docker Compose YAML file, each service specifies how its container should run, including the Docker image, environment variables, ports, and other settings.

For this deployment, the services include:

- **Nextcloud:** The application container that provides the web interface and cloud storage functionality.
- **MySQL:** The database container that stores information required by the application.

By placing both services in the same Compose file, I can manage them together instead of manually configuring each container separately. This makes the deployment more organized and easier to maintain.

## 🌐 2. How Does Nextcloud Find the Database Container?

Nextcloud uses the `MYSQL_HOST` environment variable to identify the hostname of the database service.

For example, the configuration may contain:

```yaml
environment:
  MYSQL_HOST: db
```

In this example, `db` must match the name of the database service defined in the Compose file.

Docker Compose creates a default network for the application. Containers connected to this network can communicate with each other using their service names. Because of this, Nextcloud can connect to the database using `db` as the hostname without needing to manually find the database container's IP address.

This makes communication between containers easier and more manageable. If the database service has a different name, the `MYSQL_HOST` value must be updated to match it.

## ⚙️ 3. Difference Between `docker run` and `docker compose up -d`

Both commands are used to start containers, but they differ in how containers are configured and managed.

| Feature | `docker run` | `docker compose up -d` |
|---|---|---|
| Configuration | Uses command-line options | Uses a YAML configuration file |
| Containers | Usually starts one container per command | Can start multiple related services |
| Networking | May require additional network configuration | Creates and manages the default Compose network |
| Management | Containers are configured individually | Services are managed together |
| Background execution | Uses `-d` to run in the background | Uses `-d` to run in the background |

In Mission 4, I used `docker run` to start a container directly through the terminal. For this mission, `docker compose up -d` allows Docker Compose to create or start all the services defined in the YAML file.

The `up` command creates or starts the configured services, while `-d` means detached mode. This allows the containers to run in the background while I continue using the terminal for other tasks.

## 💻 4. Common Docker Compose Commands

The following commands can be used when working with the deployment. Run them from the directory containing the Compose file.

```bash
# Check the Docker version
docker --version

# Check the Docker Compose version
docker compose version

# Validate the Compose configuration
docker compose config

# Start the services in the background
docker compose up -d

# Check running containers
docker compose ps

# View service logs
docker compose logs

# Stop and remove the containers and network
docker compose down
```

**Note:** These are standard commands for this workflow. Only describe them as executed if they were actually run during the laboratory activity.

## 🎯 Conclusion

Through this checkpoint, I learned how Docker Compose organizes multiple application services in one YAML file. I also understood how the `MYSQL_HOST` environment variable helps Nextcloud locate its database through Docker's service discovery.

Compared with using `docker run` for individual containers, Docker Compose provides a more convenient way to deploy and manage related services. These concepts helped me understand how containerization can simplify application deployment and improve cloud infrastructure management.

---

<div align="center">

🔵 **LEARN**　•　**CONFIGURE**　•　🔴 **DEPLOY**

**CCM101 – Cloud Computing Laboratory**

*Prepared by: Avril Mei A. Dinglasan*

[⬅ Back to Laboratory README](./README.md)

</div>
