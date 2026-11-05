### 📄 File 3: `README.md`
> **Location on GitHub:** `CCM101-adinglasan/Laboratory-08-Cloud-Security-Engineer/README.md`

```markdown
# 🛡️ Laboratory Activity 8: The Cloud Security Engineer

<div align="center">

| [🏠 Portfolio Home](../README.md) | [📌 Mission Overview](#-mission-overview) | [🎯 Objectives](#-objectives) | [💻 Commands Executed](#-commands-executed) | [🧠 Skills Learned](#-skills-learned) |
| :---: | :---: | :---: | :---: | :---: |

</div>

---

## 📌 Mission Overview

<p align="justify">
Welcome to <b>CloudNova Technologies</b>! As part of the elite Cloud Security Team, this mission addresses a critical real-world vulnerability: a junior developer deployed a new Ubuntu server for a client's web application without configuring network security, leaving it entirely exposed to the public internet[cite: 1, 2]. 
</p>

<p align="justify">
Using the <b>KillerCoda Playground</b>, this laboratory implements the principle of <b>defense in depth</b>[cite: 1]. By deploying a vulnerable web application container (`secure-web-app`), establishing a security baseline, enforcing a strict <i>Default Deny</i> incoming policy via the Uncomplicated Firewall (UFW), and carefully allowing selective ports (SSH and port 8080), the server is successfully locked down against malicious traffic[cite: 1, 2, 3].
</p>

---

## 🎯 Objectives

* 🔍 **Understand Attack Surfaces & PoLP:** Master the Principle of Least Privilege (PoLP) and analyze virtual machine attack surfaces[cite: 1].
* 🔎 **Perform Security Audits:** Audit active network ports on a live Linux server environment[cite: 1].
* 🔒 **Configure UFW:** Implement a strict **Default Deny** incoming policy while maintaining safe administrative access[cite: 1, 3].
* 🚦 **Granular Port Management:** Selectively open TCP ports (SSH and port 8080) for legitimate user and administrative traffic[cite: 1, 3].
* 📝 **Professional Documentation:** Document security configurations, audits, and reflections cleanly in Markdown format inside your GitHub Cloud Computing Portfolio repository[cite: 1, 3, 4].

---

## 💻 Commands Executed

The essential Linux, Docker, and UFW commands executed during this laboratory activity include:

```bash
# 1. Deploy the vulnerable Nginx web application container on port 8080
docker run -d --name secure-web-app -p 8080:80 nginx

# 2. Verify application accessibility locally
curl -I http://localhost:8080

# 3. Permanently allow SSH access BEFORE enabling the firewall (crucial safety step)
sudo ufw allow ssh

# 4. Set foundational default firewall policies (Deny incoming, Allow outgoing)
sudo ufw default deny incoming
sudo ufw default allow outgoing

# 5. Enable the Uncomplicated Firewall (UFW)
sudo ufw enable

# 6. Check detailed firewall activation status and verbose rules
sudo ufw status verbose

# 7. Create a precise rule for granular TCP web traffic management on port 8080
sudo ufw allow 8080/tcp

# 8. Verify active firewall rules with numbered listings
sudo ufw status numbered

---

🧠 Skills Learned
Host-Based Firewall Configuration: Proficiency in managing ufw rules, default policies, and inspecting active network ports.

Network Risk Mitigation: Understanding how to minimize a server's attack surface by blocking unnecessary open ports and preventing automated brute-force attacks.

Defensive Administration Workflows: Recognizing the critical operational sequence of permitting administrative access (SSH) prior to activating strict firewall blocks.

Technical Portfolio Development: Structuring comprehensive security audit logs, deployment configurations, and critical thinking reflections within a GitHub repository.
