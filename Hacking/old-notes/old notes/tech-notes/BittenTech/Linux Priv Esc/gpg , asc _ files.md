#### crack hash of asc / gpg files with gpg2john

### example

```
gpg2john tryhackme.asc > hash
john --wordlist=/usr/share/wordlists/rockyou.txt hash
pgp --import tryhackme.asc   //provide cracked password
gpg --decrypt credentials.pgp // provide cracked password
```
