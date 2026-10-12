cat > automation-research.md <<'EOF'
# Automation Research

## Bash Script
A Bash script is a text file with a list of terminal commands that run one after another. Instead of typing them every time, I save them once and run the file. The first line, `#!/bin/bash`, tells Linux to use Bash to read the file.

## Variables
A variable holds a value under a name, like `BACKUP_DIR="backups"`. If the folder name changes later, I only fix it on one line and not everywhere in the script. It also cuts down on typing mistakes.

## Cron Job
Cron is the Linux scheduler. A cron job is a command that cron runs by itself at a time I set, for example every night at 2 AM. In cloud work this matters because things like backups keep happening even when nobody is around to do them.
EOF