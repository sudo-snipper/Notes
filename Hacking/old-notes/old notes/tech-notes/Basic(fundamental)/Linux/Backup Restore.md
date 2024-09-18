# **BACKUP PROGRAMS**

- **RSYNC**
- **DEJA DUP**
- **DUPLICITY**
- **TIMESHIFT**

## ==**RSYNC**==

                 **-a : used to preserve the original file attributes, such as permissions, timestamps, etc.**

**                 -v : verbose**

**                 -z : compression**

                  **to backup** :-   rsync -av /backup/files server@ip:/backup/directory

                  **backup with compression** :\-    rsync -azv /backup/files server@ip:/backup/directory

                 **to restore : -    **rsync -av user@remote_host:/path/to/backup/directory /path/to/mydirectory

                  **encryption :-  **rsync -e ssh ........

```
overlordchest@htb[/htb]$ rsync -avz --backup --backup-dir=/path/to/backup/folder --delete /path/t
```

With this, we back up the `mydirectory` to the remote `backup_server`, preserving the original file attributes, timestamps, and permissions, and enabled compression (`-z`) for faster transfers. The `--backup` option creates incremental backups in the directory `/path/to/backup/folder`, and the `--delete` option removes files from the remote host that is no longer present in the source directory.