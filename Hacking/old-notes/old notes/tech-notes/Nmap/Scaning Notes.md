## Host / Network scan
`nmap <ip/FQDN>`
`nmap <192.168.1.0/24>`
 * ### Multiple  scan
    `nmap 192.168.1.1-10`  >>> scan ip from 1 to 10
    `nmap 192.168.1.0/24 10.10.1.0/24`
	
---
## Port scan
`nmap -p 22`
`nmap -p 22,23,21,80`
`nmap -p 2-200` 
`nmap -p-`   >>>> all ports

>==this make full connection SYN,ACK,SYN,RST==
>==form LOGS==

### Without full connection
* SYN Stleath scan
   `nmap -sS -p80 192.168.1.1`
   > we make ==SYN,RST== request no ACK
   > many time ==no LOGS== for this
    
	`wireshark` :  **tcp header**
	> ==window : 1024== 
	> this value state send only 1024 bytes at once
	> window : 1024  means it is packet by Nmap
	> ==so it SYN scan can be found easily==
   
ACK scan
   `nmap -sA 192.168.1.1`
   * ACK flag scanning is useful to verify whether the server is blocked with firewalls, IPS, or other
network security controls. As in the FIN scan, we will send an TCP ACK packet. No response or an
ICMP error indicates the presence of a stateful firewall, as the port is filtered, and if we get back an
RST-ACK, then the stateful firewall is absent:
   > we make ==ACK== only
   > it show ==unfiltered ports==ff

### make tcp header realstic
`nmap -sT 192.168.1.1`
> in this nmap don't send it tell OS tcp stack to send 
> so TCP header value in real in this 
> it make FULL Connection


* #### nmap use ==TCP default== to use ==UDP==
   `nmap -sU -p- 192.168.1.1`

* #### For Fast Scan
   `nmap -F 192.168.1.1`
   > -F ::  scan 100 common ports

* #### Top ports
   `nmap --top-ports 20 192.168.1.1`
   
   > scan top common 20 ports



----

## Ping scan
`nmap -sn 192.168.1.0/24`
> show active devices on network


* Without ==Sudo== it don't use ==ICMP==
   `sudo nmap -sn 192.168.1.0/24`
  > use sudo to see device hostnames and ICMP request



----

## Full scan [==warning==]
`nmap -A 192.168.1.1`
> scan all things ::: OS , Ports , Version , Trace, Banner etc.
> full noise , IDS IPS get activate 
> it activate firewall 

---

## OS version
`nmap -O 192.168.1.1`
> scan OS , OS version
> Use TCP STACK

## Bypass Firewall OR TCP loophole

#### ==If target not responde to packets of theses it state port open==
**with out doing SYN, ACK , RST  if found port open**
> FYN flag mean good bye 
*  **NULL SCAN**
   `nmap -sN 192.168.1.2`
   >it ==set all flags to None==
 * **CHRIMAS SCAN**
    `nmap -sX 192.168.1.2`
    >it ==set flags FYN, PSH, URG==
 
 * FIN SCAN
    `nmap -sF 192.1681.1`
    > it ==set flag FYN==

* NO PING SCAN
  `nmap -Pn 192.168.1.0/24`
  > it tell Nmap for not to ping device
  > treat all host alive
----
## UDP SCAN
`nmap -sU 192.168.1.1`

---

## OUTPUT
* `-oN file.txt`
   >to  text files
 * `-oA filename`
    > save to 3 different types of file
 
 ---
 
 ## FASTER SCAN
 * `-T<number>`
   > number :- 1 to 5
   > T3 in normal default
   > more fast more traffic to get notice

---

## SCRIPTS
* `nmap -sC <ip>`
  > default scripts to check ports, fingerprint , version etc,
* `nmap --scritps script.nse <ip>`
  > ex:- nmap --script banner.nse 192.168.1.1
* `nmap --script http-enum <ip>`
  >list hidden directory
* `--script=safe`
  > use all scripts of safe category
  > many other categories are there check theme
  
* `cat /usr/share/nmap/scripts/script.db1`
  > contain details of all scripts
  > there categories  
 ---
 
 ## FIREWALL  /   IDS, IPS
  ### **Packet Fragment**
 *  `nmap -f <ip>`
   
    >use size is 8 bytes
   
	   * `nmap --mtu <size_of_packet> ip`
	     > mtu size will be ==multiple of 8==

* **CheckSum**
  `nmap --badsum <ip>`
  > if no firewall then NO REPLY
  > if firewall then REPLY
  > many cases this work
  
  `nmap --data-lenght <num>`
  >append random data to last of packet 

* **IP SPOOF**
  `nmap -S <spoof_ip> -e <interface> -p- <ip>`
  > nmap don't listen for spoof ip , so packet don't come back
  > use bettercap to listen for spoof ip

* **decoy scan**
  > use multiple IP to scan target
  > use last IP original your
   `nmap -D <spoof_ip>,<spoof_ip>,<your_ip> -e <interface> -p- <ip`
   
* **decoy with random IP**
  `nmap -D RND:20 -e <interface> <ip>`
  > it use 20 random IP to scan
  
* **zombie host**
   >https://nmap.org/book/idlescan.html
   >use other machine to scan for you and your machine guess and see the result
   > using -Pn in best with it
   >  `nmap -p- -Pn -sI <zombie_machine> <target_machine>`
   > `nmap -p- -Pn -sI zombie.com target.com`
   > `nmap -p- -Pn -sI 130.123.42.4 109.13.1.2`
   > 
 
  

   