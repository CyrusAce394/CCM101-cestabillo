
# Laboratory 09 - Backup Script Guide

## Mission 9: The Cloud Automation Engineer

### Introduction

This laboratory activity focuses on creating an automated backup system using Bash scripting and Linux Cron. The purpose is to reduce manual tasks, prevent data loss, and improve the efficiency of cloud operations.

## 1. Creating the Application Data

The following commands were used to create a sample directory and test file:

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
```

The `app-data` directory represents the client's application data, while `data.txt` contains the sample information that needs to be backed up.

## 2. Creating the Backup Script

The backup script was created using the nano text editor:

```bash
nano backup.sh
```

### Full Bash Script

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

## 3. Explanation of the Bash Script

- `#!/bin/bash` specifies that the script uses the Bash interpreter.
- `SOURCE_DIR` identifies the source directory containing the application data.
- `BACKUP_DIR` identifies the destination directory for backup files.
- `TIMESTAMP` generates the current date and time to create a unique backup filename.
- `echo` displays messages in the terminal.
- `mkdir -p` creates the backup directory if it does not already exist.
- `tar -czf` compresses the source directory into a `.tar.gz` file.

## 4. File Permissions and Execution

Initially, the Bash script could not be executed because it did not have executable permission.

The following command was used to grant executable permission:

```bash
chmod +x backup.sh
```

The `chmod` command changes file permissions in Linux, while `+x` adds executable permission. This allows the script to be executed directly from the terminal.

After modifying the permissions, the script was executed using:

```bash
./backup.sh
```

The terminal displayed the following messages:

```text
Initiating automated backup...
Backup completed successfully at 20261015_140403!
```

The generated backup file was verified using:

```bash
ls -l backups/
```

The backup was successfully created as a compressed `.tar.gz` file.

## 5. Scheduling the Cron Job

Linux Cron was used to schedule the Bash script to run automatically every day at 2:00 AM.

First, the existing Cron jobs were checked using:

```bash
crontab -l
```

Next, the Cron editor was opened using:

```bash
env EDITOR=nano crontab -e
```

The following Cron expression was added:

```cron
0 2 * * * /root/backup.sh
```

### Explanation of the Cron Expression

| Field | Value | Description |
|---|---|---|
| Minute | 0 | Executes at minute 0 |
| Hour | 2 | Executes at 2:00 AM |
| Day of Month | * | Executes every day of the month |
| Month | * | Executes every month |
| Day of Week | * | Executes every day of the week |

The Cron expression schedules the backup script to execute daily at 2:00 AM according to the Linux system's timezone.

The installed Cron job was verified using:

```bash
crontab -l
```

The output confirmed that the schedule had been installed successfully.
