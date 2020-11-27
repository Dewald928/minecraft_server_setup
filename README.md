# Minecraft server setup notes

## Create world
Download and install [mscs](https://minecraftservercontrol.github.io/docs/mscs)

Follow the instructions

Create backups using crontab

## Backup to google drive
1. Use ```rclone``` to create a [remote](https://rclone.org/drive/) to your google drive (```google-drive```).
2. Use the ```backup_mc_gdrive.sh``` bash file, to set the rclone locations.
3. Another ```crontab -e``` entry is made to run the script every monday/sunday night at 12.

Add this line to the crontab -e
```0 1 * * 1 /home/fuzzyserver/backup_mc_gdrive.sh```

Now it should save the world every week to gdrive
