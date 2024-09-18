>## SecLists from github cotain wordlists , password and many more 
>https://github.com/danielmiessler/SecLists
---
`gobuster dir -u <site> -w wordlist.txt`
>To bruteforce directory
---

### to do subdomain bruteforce first add
### dns in /etc/resolv.conf   (1.1.1.1)
`gobuster dns -d <site> -w /dnsnamelist.txt`
