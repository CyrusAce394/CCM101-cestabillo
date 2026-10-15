
# Laboratory 09 - Cloud Automation Engineer

## Mission Overview

This laboratory activity focused on automating application data backups using Bash scripting and Linux Cron. A Bash script was created to compress sample application files into a backup archive, and a Cron job was configured to execute the script automatically every day at 2:00 AM.

## Objectives

- Understand the fundamentals of Bash scripting.
- Create and edit Bash scripts using nano.
- Use variables and Linux commands for automation.
- Modify file permissions using chmod.
- Create compressed backups using tar.
- Configure scheduled tasks using Linux Cron.
- Document automation procedures using Markdown.

## Commands Executed

```bash
cd /root
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
tar -tzf backups/*.tar.gz
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

### Cron Expression

```cron
0 2 * * * /root/backup.sh
```

## Skills Learned

- Bash shell scripting
- Linux terminal commands
- Variables and timestamps
- File permission management
- Automated backup creation
- File compression using tar
- Cron job scheduling
- Linux task automation
