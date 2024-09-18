## server message block

* use on Netbios 
* used for  shared resources
* linux need samba server to run it
* port :-- 139   (netbios is old so work on netbios port)
* port :--- 445

----
Tools :--- **smbclient**
* `smbclient -L 192.168.1.3`
* `nmap -p445 -A 192.168.1.3`
* `nmap -p445 --script=search_scripts 192.168.1.3`
 
 ---
 
## connect to smb share 
```
smbclient //<ip>/user
ex:--  smbclient //10.17.57.101/anonymous
```

---

## Download SMB files
```
smbget -R smb://10.10.16.228/anonymous
```
> provide username and password as nothing

## enumerate
```
enum4linux -a <ip>
```