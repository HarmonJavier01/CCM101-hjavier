cat > backup-script-guide.md <<'EOF'
# Backup Script Guide

This is how the backup for the client's `app-data` folder was set up.

## backup.sh
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

The script makes a `backups` folder if it is missing, then packs `app-data` into a `.tar.gz` file. The timestamp is in the filename, so each run saves a new file and never overwrites an older backup.

## chmod +x
When I first ran `./backup.sh`, I got "Permission denied" because a new file is not executable. `chmod +x backup.sh` added the execute permission, so Linux now treats the file as a program I can run.

## Cron expression
```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|-------|-------|---------|
| Minute | 0 | minute 0 (on the hour) |
| Hour | 2 | 2 AM |
| Day of Month | * | any day |
| Month | * | any month |
| Day of Week | * | any weekday |

So the script runs every night at 2:00 AM.

## Screenshots
![Script execution](screenshots/script-execution.png)

![Cron schedule](screenshots/cron-schedule.png)
EOF