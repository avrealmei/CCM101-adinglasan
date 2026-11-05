# 🛡️ Laboratory Activity 8: The Cloud Security Engineer

<div align="center">

| [🏠 Portfolio Home](../README.md) | [📌 Mission Overview](#-mission-overview) | [🎯 Objectives](#-objectives) | [💻 Commands Executed](#-commands-executed) | [🧠 Skills Learned](#-skills-learned) |
| :---: | :---: | :---: | :---: | :---: |

</div>

---

## 📌 Mission Overview

<p align="justify">
Welcome to <b>CloudNova Technologies</b>! As part of the elite Cloud Security Team, this mission addresses a critical real-world vulnerability: a junior developer deployed a new Ubuntu server for a client's web application without configuring network security, leaving it entirely exposed to the public internet.
</p>

<p align="justify">
Using the <b>KillerCoda Playground</b>, this laboratory implements the principle of <b>Defense in Depth</b>. By deploying a web application container (<code>secure-web-app</code>), establishing a security baseline, enforcing a strict <i>Default Deny</i> incoming policy through the Uncomplicated Firewall (UFW), and selectively allowing essential ports (SSH and port 8080), the server is secured against unauthorized network traffic.
</p>

---

## 🎯 Objectives

- 🔍 **Understand Attack Surfaces & PoLP:** Understand the Principle of Least Privilege (PoLP) and analyze potential attack surfaces in a virtual machine environment.

- 🔎 **Perform Security Audits:** Audit active network ports and examine network exposure on a Linux server.

- 🔒 **Configure UFW:** Implement a strict **Default Deny** incoming policy while maintaining safe administrative access.

- 🚦 **Granular Port Management:** Selectively allow TCP ports (SSH and port 8080) for legitimate administrative and web application traffic.

- 📝 **Professional Documentation:** Document security configurations, audit results, and technical reflections in Markdown format within the GitHub Cloud Computing Portfolio repository.

---

## 💻 Commands Executed

The following Linux, Docker, and UFW commands were executed during this laboratory activity:

```bash
# 1. Deploy the Nginx web application container on port 8080
docker run -d --name secure-web-app -p 8080:80 nginx

# 2. Verify application accessibility locally
curl -I http://localhost:8080

# 3. Allow SSH access before enabling the firewall
sudo ufw allow ssh

# 4. Configure default firewall policies
sudo ufw default deny incoming
sudo ufw default allow outgoing

# 5. Enable the Uncomplicated Firewall (UFW)
sudo ufw enable

# 6. Check firewall activation status and detailed rules
sudo ufw status verbose

# 7. Allow incoming TCP traffic on port 8080
sudo ufw allow 8080/tcp

# 8. Verify active firewall rules using numbered listings
sudo ufw status numbered
```

---

## 🧠 Skills Learned

**Host-Based Firewall Configuration:** Developed proficiency in managing UFW rules, configuring default firewall policies, and inspecting active network ports.

**Network Risk Mitigation:** Learned how to minimize a server's attack surface by restricting unnecessary incoming connections and reducing exposure to unauthorized network traffic.

**Defensive Administration Workflows:** Understood the importance of allowing administrative access (SSH) before activating restrictive firewall policies to prevent accidental loss of remote server access.

**Container Deployment and Network Security:** Gained practical experience deploying an Nginx container using Docker and managing network access through host-based firewall configurations.

**Technical Portfolio Development:** Improved technical documentation skills by organizing security configurations, deployment commands, audit results, and laboratory reflections in a GitHub repository.
