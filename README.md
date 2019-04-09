# Simple websites backup script

## Introduction
Simple backup script for the Apache web root directory.

## Installation

### Step 1: Setup

Create a directory to store the backup script. I suggest using /scripts:
```bash
sudo mkdir /scripts
```

Clone this repository in the /scripts directory:
```bash
git clone https://github.com/markwierda/websites-backup-script.git
```

Make the script executable:
```bash
sudo chmod +x backup.sh
```

Now you can test the backup script by running:
```bash
sudo ./backup.sh
```

### Step 2: Create a scheduled task

Open the root crontab file:
```bash
sudo crontab -e
```

Add this line at the end of the file:
```bash
@daily sh /scripts/websites-backup-script/backup.sh
```
