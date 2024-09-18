`gobuster dir -u test.com -w big.txt -x php,html,txt`

> **-x** : specifies to add given extension on wordlist end

---
### Vhost
```

sudo gobuster vhost -u http://thetoppers.htb/ -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt --no-error --append-domain

```

> used when to discover subdomain of ip we added in hosts file in machine