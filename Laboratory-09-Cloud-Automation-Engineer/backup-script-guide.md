# Backup Script and Cron Job Guide

## Purpose
This guide documents a Bash script that compresses the sample `app-data` directory into a timestamped `.tar.gz` archive in a `backups` directory.

## Full `backup.sh` Code
```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## What `chmod +x` Does
The command `chmod +x backup.sh` adds executable permission to `backup.sh`. After this permission is added, the script can be started directly with `./backup.sh`, provided the current directory and script contents are correct.

## Cron Schedule
The configured cron line is:

```cron
0 2 * * * /root/backup.sh
```

The five time fields are:

| Field | Value | Meaning |
|---|---:|---|
| Minute | `0` | At minute 0 |
| Hour | `2` | At 2 AM |
| Day of Month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

Therefore, this expression schedules `/root/backup.sh` to run every day at 2:00 AM according to the machine's local time.
