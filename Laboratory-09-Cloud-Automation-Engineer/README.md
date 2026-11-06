<p align="center">
  <a href="#mission-overview"><img src="https://img.shields.io/badge/MISSION%20OVERVIEW-1D4ED8?style=for-the-badge" alt="Mission Overview"></a>
  <a href="#objectives"><img src="https://img.shields.io/badge/OBJECTIVES-B91C1C?style=for-the-badge" alt="Objectives"></a>
  <a href="#commands-executed"><img src="https://img.shields.io/badge/COMMANDS%20EXECUTED-1D4ED8?style=for-the-badge" alt="Commands Executed"></a>
  <a href="#skills-learned"><img src="https://img.shields.io/badge/SKILLS%20LEARNED-B91C1C?style=for-the-badge" alt="Skills Learned"></a>
</p>

# 🚀 Laboratory 9: The Cloud Automation Engineer

> *"If you have to do a task more than twice in the cloud, you should automate it."*

---

<a id="mission-overview"></a>

## 📖 Mission Overview

Promoted to the Cloud Automation and DevOps Team at CloudNova Technologies, this mission focuses on replacing repetitive manual administrative tasks with efficient and scalable automation routines.

The laboratory involves developing a Bash backup script that automatically compresses client data into a `.tar.gz` archive and configuring a scheduled backup using the Linux Cron scheduler.

Through this activity, the student demonstrates the application of shell scripting, Linux file permissions, task scheduling, and technical documentation in a simulated cloud infrastructure environment.

---

<a id="objectives"></a>

## 🎯 Objectives

- Understand the fundamental syntax of Bash shell scripting, including variables and basic commands.
- Use a command-line text editor (`nano`) to write and save executable scripts.
- Modify Linux file permissions using the `chmod` command.
- Understand automated task scheduling and the syntax of a Linux crontab.
- Create compressed backup archives using the `tar` command.
- Document automation scripts and Cron job configurations using Markdown.
- Complete the final chapter of the GitHub Cloud Computing Portfolio.

---

<a id="commands-executed"></a>

## ⌨️ Commands Executed

### 1. Create the Application Data Directory

```bash
mkdir app-data
```

### 2. Create a Sample Data File

```bash
echo "This is critical client data." > app-data/data.txt
```

### 3. Create the Backup Script

```bash
nano backup.sh
```

### 4. Modify File Permissions

```bash
chmod +x backup.sh
```

### 5. Execute the Backup Script

```bash
./backup.sh
```

### 6. Verify the Backup Archive

```bash
ls -l backups/
```

### 7. Configure the Cron Scheduler

```bash
crontab -l
env EDITOR=nano crontab -e
```

Add the following Cron expression:

```bash
0 2 * * * /root/backup.sh
```

### 8. Verify the Cron Configuration

```bash
crontab -l
```

---

<a id="skills-learned"></a>

## 💡 Skills Learned

- 🖥️ **Bash Scripting:** Writing automated scripts using variables, commands, and file compression.
- 🔒 **Linux Permissions:** Managing executable file permissions through `chmod +x`.
- ⏰ **Task Scheduling:** Automating routine server operations using Linux Cron syntax.
- 🗜️ **File Compression:** Creating `.tar.gz` backup archives using the `tar` command.
- 🛠️ **DevOps Automation:** Reducing repetitive manual administrative tasks through automation.
- 📝 **Technical Documentation:** Organizing and documenting scripts and configurations using Markdown.
