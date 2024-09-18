# use : fdisk , gpart , gparted

## ==**fdisk**==

            **to view all disks : -** sudo fdisk -l

             **to mount disks :-**sudo mount /dev/name /mount/directory

             **to unmount       :-          **umount /mount/directory

             all mounted disk and their information is in :--        **/etc/fstab**

**             to list all mounted filesystem use :--       mount**

  can't umount when device is running or open to see opened or not use **:--    lsof**