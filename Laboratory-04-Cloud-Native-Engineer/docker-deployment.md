<div align="center">

[![Cloud Computing Lab](https://img.shields.io/badge/CCM101-Cloud%20Computing-blue?style=flat-square&logo=cloud&logoColor=white)](./README.md)
[![Theme](https://img.shields.io/badge/Theme-Blue%20%2F%20Red-red?style=flat-square&logo=docker&logoColor=white)](./docker-deployment.md)

</div>

---

### 🌐 Navigation Bar
<div align="center">

[🏠 **Home**](./README.md) &nbsp;&nbsp;|&nbsp;&nbsp; [🔵 **VMs vs Containers**] [📝 **Reflection**](./reflection.md)

</div>

---

# 🔴 Docker Deployment & Operations

This document records the complete lifecycle operations performed in the KillerCoda playground for CloudNova Technologies, ranging from environment verification to container deployment, management, and cleanup.

---

## 1. Checkpoint 3: Environment Verification

To verify that Docker was installed, configured, and active on the cloud host, the following CLI commands were executed:

```bash
# Check the installed version of the Docker client and build tools
root@ubuntu:~$ docker --version

# Display system-wide diagnostic information regarding the Docker daemon, storage drivers, and resource limits
root@ubuntu:~$ docker info
