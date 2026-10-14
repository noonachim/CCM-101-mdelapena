# Research: The Language of Automation

## 1. Bash Script
A Bash script is a text file containing shell commands that Linux can run in sequence to perform a task. The line `#!/bin/bash` is called the shebang; it tells the operating system to use Bash to interpret the commands in the file.

## 2. Variables
Variables store values, such as folder paths, under short names that can be reused in a script. For example, using `$BACKUP_DIR` means the path can be changed in one place instead of editing every command that uses it, which makes the script easier to maintain and less likely to contain inconsistent paths.

## 3. Cron Job
A cron job is a scheduled task managed by the Linux cron service. It is useful in cloud operations because routine jobs, such as backups and maintenance tasks, can run at set times without someone needing to start them manually.
