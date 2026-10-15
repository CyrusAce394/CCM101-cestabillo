
# Automated Backup Script Guide

## Mission 9: The Cloud Automation Engineer

### Introduction

This activity demonstrates how to automate file backups using a Bash script and schedule the process using Linux Cron. The purpose is to reduce manual work and prevent data loss by creating compressed backup files.

## 1. Creating the Application Data

The following commands were used to create a sample application folder and a test file:

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
```

The `app-data` directory represents the client's application data, while `data.txt` contains sample information that needs to be backed up.

## 2. Creating the Backup Script

The following Bash script creates a compressed backup of the application data and includes a timestamp in the backup filename.

### Full Bash Script

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

cd /root || exit 1

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

mkdir -p "$BACKUP_DIR"

if tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"; then
    echo "Backup completed successfully at $TIMESTAMP!"
else
    echo "Backup failed!"
    exit 1
fi
```

## 3. Explanation of the Script

- `#!/bin/bash` tells the system to execute the script using Bash.
- `cd /root || exit 1` sets the working directory and stops execution if the directory cannot be accessed.
- `SOURCE_DIR` identifies the folder containing the application data.
- `BACKUP_DIR` identifies where backup files will be stored.
- `TIMESTAMP` generates a unique date and time value.
- `echo` displays status messages in the terminal.
- `mkdir -p` creates the backup directory if it does not exist.
- `tar -czf` compresses the source directory into a `.tar.gz` archive.
- The `if` statement checks whether the backup command succeeded.

## 4. File Permissions and Execution

Initially, the script did not have executable permission.

The following command was used to grant execution permission:

```bash
chmod +x backup.sh
```

The `chmod` command modifies file permissions, while `+x` adds executable permission. This allows Linux to run the script directly as a program.

After granting permission, the script was executed using:

```bash
./backup.sh
```

The backup directory and compressed file were verified using:

```bash
ls -l backups/
```

## 5. Scheduling the Cron Job

Linux Cron was used to schedule the backup process automatically.

The Cron editor was opened using:

```bash
env EDITOR=nano crontab -e
```

The following schedule was added:

```cron
0 2 * * * /root/backup.sh
```

### Explanation of the Cron Expression

| Field | Value | Explanation |
|---|---|---|
| Minute | 0 | Run at minute 0 |
| Hour | 2 | Run at 2 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

This schedule runs the backup script every day at 2:00 AM based on the Linux system's timezone.

The installed Cron job was verified using:

```bash
crontab -l
