<p align="center">
  <a href="#student-profile"><img src="https://img.shields.io/badge/👤%20STUDENT%20PROFILE-1D4ED8?style=for-the-badge&logoColor=white" alt="Student Profile"></a>
  <a href="#mission-overview"><img src="https://img.shields.io/badge/📖%20OVERVIEW-B91C1C?style=for-the-badge&logoColor=white" alt="Overview"></a>
  <a href="#repository-structure"><img src="https://img.shields.io/badge/📁%20REPOSITORY-1D4ED8?style=for-the-badge&logoColor=white" alt="Repository"></a>
  <a href="#laboratory-objectives"><img src="https://img.shields.io/badge/🎯%20OBJECTIVES-B91C1C?style=for-the-badge&logoColor=white" alt="Objectives"></a>
  <a href="#commands-executed"><img src="https://img.shields.io/badge/⌨️%20COMMANDS-1D4ED8?style=for-the-badge&logoColor=white" alt="Commands"></a>
  <a href="#skills-learned"><img src="https://img.shields.io/badge/💡%20SKILLS-B91C1C?style=for-the-badge&logoColor=white" alt="Skills"></a>
</p>

# 🚀 Laboratory 9: The Cloud Automation Engineer

> *"If you have to do a task more than twice in the cloud, you should automate it."*

---

## 👤 Student Profile

| Information | Details |
|---|---|
| Student Name | Avril Mei A. Dinglasan |
| Institution | University of Eastern Pangasinan |
| College | College of Information Technology |
| Course | CCM101 – Cloud Computing |
| Laboratory | Laboratory 9 |
| Role | Cloud Automation Engineer Trainee |
| Organization | CloudNova Technologies |

---

## 📖 Mission Overview

Promoted to the Cloud Automation and DevOps Team at CloudNova Technologies, this mission focuses on replacing repetitive manual administrative tasks with efficient and scalable automation routines.

The laboratory involves developing a Bash backup script that automatically compresses client data into a `.tar.gz` archive and configuring a scheduled backup using the Linux Cron scheduler.

Through this activity, the student demonstrates the application of shell scripting, Linux file permissions, task scheduling, and technical documentation in a simulated cloud infrastructure environment.

---

## 🎯 Laboratory Objectives

- Understand the fundamental syntax of Bash shell scripting, including variables and basic commands.
- Use a command-line text editor (`nano`) to write and save executable scripts.
- Modify Linux file permissions using the `chmod` command.
- Understand automated task scheduling and the syntax of a Linux crontab.
- Create compressed backup archives using the `tar` command.
- Document automation scripts and Cron job configurations using Markdown.
- Complete the final chapter of the GitHub Cloud Computing Portfolio.

---

## 📁 Repository Structure

```text
Laboratory-09/
│
├── README.md
├── backup-script--code.md
│
├── backup.sh
│
├── app-data/
│   └── data.txt
│
└── backups/
    └── backup_YYYYMMDD_HHMMSS.tar.gz
```

### 📄 Documentation Files

| File | Description |
|---|---|
| `README.md` | Laboratory overview, objectives, commands, and skills learned. |
| `backup-script--code.md` | Complete technical guide containing the Bash script, command explanations, file permissions, and Cron configuration. |
| `backup.sh` | Executable Bash backup script. |

---

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

## 💡 Skills Learned

- 🖥️ **Bash Scripting:** Writing automated scripts using variables, commands, and file compression.
- 🔒 **Linux Permissions:** Managing executable file permissions through `chmod +x`.
- ⏰ **Task Scheduling:** Automating routine server operations using Linux Cron syntax.
- 🗜️ **File Compression:** Creating `.tar.gz` backup archives using the `tar` command.
- 🛠️ **DevOps Automation:** Reducing repetitive manual administrative tasks through automation.
- 📝 **Technical Documentation:** Organizing and documenting scripts and configurations using Markdown.

---

## 📚 Technical Documentation

For the complete Bash backup script, execution instructions, permission explanations, and Cron scheduling breakdown, see the technical guide below.

<p align="center">
  <a href="backup-script--code.md">
    <img src="https://img.shields.io/badge/🛡️%20VIEW%20BACKUP%20SCRIPT%20%26%20AUTOMATION%20GUIDE-1D4ED8?style=for-the-badge&logoColor=white" alt="View Backup Script and Automation Guide">
  </a>
</p>

---

## ✅ Laboratory Completion

**Laboratory 9: The Cloud Automation Engineer**

The laboratory demonstrates the successful development and execution of a Bash backup script, creation of compressed backup archives, modification of executable file permissions, and configuration of an automated backup schedule using Linux Cron.

---

<p align="center">
  <b>☁️ CloudNova Technologies</b><br>
  <i>Cloud Computing Laboratory Portfolio</i><br>
  <sub>University of Eastern Pangasinan | College of Information Technology</sub>
</p>
