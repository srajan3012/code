## DISK QUOTA EXCEEDED ISSUE:

> Error while saving file: Unable to open database file

> sqlite3.OperationalError: unable to open database file
  * `rm ~/.local/share/Trash/files/core.*`

> No space left in home directory (~ or /home/srgarg)
  * Delete or move unnecessary large files. Such files can be found with this command: 
  * `find /home/srgarg/ -xdev -type f -size +50M -exec ls -alh {} \; | sort -rk 5 -n | awk '{print $5 " - " $9}'`
