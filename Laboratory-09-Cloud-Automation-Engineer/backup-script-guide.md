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

## Commands Used
```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

## Testing and Verification
After running `./backup.sh`, use `ls -l backups/` to confirm that a file with a name similar to `backup_YYYYMMDD_HHMMSS.tar.gz` exists. The actual timestamp will depend on when the script runs.

**Important environment note:** The cron entry in the laboratory handout uses `/root/backup.sh`. This absolute path works only if the script is actually saved at `/root/backup.sh`. If your script is in a different directory, use its real absolute path in the cron entry. The script's relative paths (`app-data` and `backups`) also depend on the working directory, so for a more reliable production script, use absolute paths.

## Screenshot Evidence
Add your own screenshots to `screenshots/`:
1. `script-execution.png` showing `./backup.sh` and `ls -l backups/`.
2. `cron-schedule.png` showing the installed cron line from `crontab -l`.
