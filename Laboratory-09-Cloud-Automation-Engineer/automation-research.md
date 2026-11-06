# Automation Research

### 💻 1. Bash Script
A Bash script is a plain-text file containing a series of shell commands that are executed sequentially by the Unix/Linux command-line interpreter[cite: 2]. The `#!/bin/bash` line at the very top of the file is known as the **shebang**, which instructs the operating system kernel which interpreter program should be utilized to parse and execute the subsequent lines of code[cite: 2].

### 📦 2. Variables
Programmers utilize variables (such as `$BACKUP_DIR`) instead of hardcoding exact folder paths to maintain code flexibility, readability, and ease of maintenance[cite: 2]. If a target folder path changes later, developers only need to update the variable declaration once at the top rather than modifying multiple hardcoded paths across complex scripts[cite: 2].

### ⏰ 3. Cron Job
A cron job is a time-based job scheduler built into Linux operating systems that executes scripts or commands automatically at specified intervals, dates, and times[cite: 2]. It is critical for cloud operations because it ensures routine maintenance operations—such as automated backups, security patches, and log rotations—happen autonomously without requiring manual human intervention[cite: 2].
