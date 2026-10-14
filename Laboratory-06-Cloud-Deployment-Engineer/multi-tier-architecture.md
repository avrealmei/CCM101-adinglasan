<!-- Blue and Red Navbar Banner -->
<div align="center">

| 🔵 **ARCHITECTURE OVERVIEW** | 🔴 **DATABASE TIER** | 🟢 **STATUS: SECURE** |
| :---: | :---: | :---: |
| *Web & App Logic* | *Persistent Storage* | *System Healthy* |

</div>

---

# 🏗️ Two-Tier Architecture Overview

> A robust software design pattern separating application logic and data storage for enhanced security, scalability, and maintainability.

---

## 📌 Definition
A **Two-Tier Architecture** splits an application into two distinct, independently running logical tiers:
1. **The Presentation/Application Tier:** Where user requests and business logic are handled.
2. **The Data Storage Tier:** Where persistent data, records, and databases reside.

---

## 🧩 The Tiers

### 💻 1. The Web/Application Tier
* **Role:** Serves the user interface, manages incoming HTTP requests from users, runs core application logic (such as Nextcloud file management), and communicates with the database to fetch or store data.
* **Key Technologies:** Nginx, Apache, Node.js, PHP, Docker containers.

### 🗄️ 2. The Database Tier
* **Role:** Dedicated exclusively to storing, managing, and retrieving persistent data, including user credentials, configuration settings, file metadata, and system logs.
* **Key Technologies:** PostgreSQL, MySQL, MariaDB, Redis.

---

## 🛡️ Why Separate Them?

Separating the web server and the database into two independent containers or environments provides critical advantages:

* 🔒 **Enhanced Security:** If the web application crashes or is compromised, the database remains isolated and protected in its own container tier.
* 📈 **Independent Scalability:** Scale up your web nodes or database instances independently based on traffic demands without over-allocating resources.
* 🛠️ **Seamless Maintenance:** Back up, update, or patch the database or application tier individually without bringing down the entire system.
