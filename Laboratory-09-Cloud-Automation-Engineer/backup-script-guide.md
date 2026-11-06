# 🛡️ Backup Script & Automation Technical Guide

### Full Code of `backup.sh`

The following Bash script creates a compressed backup of the `app-data` directory and saves it inside the `backups` directory using a timestamped filename.

```bash
#!/bin/bash

# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

### 📝 Code Explanation

| Code | Description |
|---|---|
| `#!/bin/bash` | Specifies Bash as the script interpreter. |
| `SOURCE_DIR` | Defines the directory containing the files to back up. |
| `BACKUP_DIR` | Specifies where the backup archives will be stored. |
| `TIMESTAMP` | Generates the current date and time for the backup filename. |
| `mkdir -p` | Creates the backup directory if it does not already exist. |
| `tar -czf` | Compresses the source directory into a `.tar.gz` archive. |
| `echo` | Displays messages during script execution. |

---

## ⌨️ Execution Commands

The following commands demonstrate the creation, configuration, and execution of the automated backup script.

### 1. Create the Source Directory

```bash
mkdir app-data
```

### 2. Create a Sample Data File

```bash
echo "This is critical client data." > app-data/data.txt
```

### 3. Create and Edit the Backup Script

```bash
nano backup.sh
```

Paste the Bash script provided in the previous section and save the file.

### 4. Make the Script Executable

```bash
chmod +x backup.sh
```

### 5. Execute the Backup Script

```bash
./backup.sh
```

### 6. Verify the Generated Backup

```bash
ls -l backups/
```

The command displays the generated backup archive inside the `backups` directory.

---

## 🔑 File Permissions

### Explanation of `chmod +x`

Linux uses file permissions to control which operations users can perform on files. By default, a newly created text file may not have executable permission.

The command:

```bash
chmod +x backup.sh
```

modifies the file permissions by adding (`+`) executable (`x`) permission.

This allows the operating system to execute the Bash script directly using:

```bash
./backup.sh
```

### 📌 Permission Breakdown

| Symbol | Meaning |
|---|---|
| `r` | Read permission |
| `w` | Write permission |
| `x` | Execute permission |
| `+` | Adds the specified permission |

---

## ⏰ Cron Scheduling

Cron is a Linux-based job scheduler that automatically executes commands or scripts at specified dates and times.

### 1. Check Existing Cron Jobs

```bash
crontab -l
```

### 2. Open the Cron Configuration Editor

```bash
env EDITOR=nano crontab -e
```

### 3. Add the Automated Backup Schedule

```bash
0 2 * * * /root/backup.sh
```

Save the configuration to activate the scheduled task.

### 📝 Cron Expression Breakdown

The Cron expression consists of five time fields followed by the command to execute.

```bash
0 2 * * * /root/backup.sh
```

| Field | Value | Description |
|---|---|---|
| Minute | `0` | Executes at the 0th minute. |
| Hour | `2` | Executes at 2:00 AM. |
| Day of Month | `*` | Runs every day of the month. |
| Month | `*` | Runs every month of the year. |
| Day of Week | `*` | Runs every day of the week. |

**Target Command:** `/root/backup.sh` specifies the absolute path of the backup script executed by the Cron scheduler.

### 4. Verify the Cron Configuration

```bash
crontab -l
```

This command displays the configured scheduled tasks and allows you to verify that the backup schedule has been saved.

---

---

## 🎯 Key Takeaways

Through this laboratory, the following technical concepts were demonstrated:

- **Bash Scripting:** Automating repetitive tasks using shell commands and variables.
- **File Compression:** Creating compressed backup archives using the `tar` command.
- **Linux Permissions:** Allowing script execution through `chmod +x`.
- **Cron Scheduling:** Configuring automated tasks using a Linux crontab.
- **DevOps Automation:** Improving operational efficiency by reducing repetitive manual administration.

---

<p align="center">
  <b>☁️ CloudNova Technologies</b><br>
  <i>Cloud Automation Engineer | CCM101 – Cloud Computing</i>
</p>
