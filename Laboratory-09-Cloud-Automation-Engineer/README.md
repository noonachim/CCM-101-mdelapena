# Laboratory 09: The Cloud Automation Engineer

## Mission Overview
This laboratory activity focuses on automating a repetitive cloud administration task with a Bash shell script. The script creates a compressed backup of a sample application-data directory, and a Linux cron job is configured to run the script every day at 2:00 AM.

## Objectives
- Explain Bash scripts, variables, and cron jobs.
- Create and save a Bash backup script.
- Use `chmod +x` to make a script executable.
- Run the script and verify that a `.tar.gz` backup is created.
- Configure and verify a cron schedule.
- Document the work using Markdown.

## Commands Executed
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

## Skills Learned
- Writing basic Bash scripts and using variables.
- Creating directories and compressed archives with `mkdir` and `tar`.
- Setting executable file permissions with `chmod`.
- Reading and configuring cron expressions.
- Documenting technical work in Markdown.
- Testing a script and collecting terminal evidence.
