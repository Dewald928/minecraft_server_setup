# Minecraft server setup notes

## Create world
Download and install [mscs](https://minecraftservercontrol.github.io/docs/mscs)

Follow the instructions

Create backups using crontab

## Backup to google drive
1. We use ```rclone``` to create a remote to our google drive.
2. We create a ```backup_mc_gdrive.sh``` bash file with the rclone command
3. Another ```crontab -e``` entry is made to run the script every monday/sunday night at 12
Add this line to the crontab -e
```0 1 * * 1 /home/fuzzyserver/backup_mc_gdrive.sh```
