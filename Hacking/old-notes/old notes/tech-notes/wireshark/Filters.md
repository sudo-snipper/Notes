## Tcp Flags
`tcp.flag.syn==1`
> show packets with syn flag only

`tcp.flag.ack==0`
>don't show ack flag packets

ETC.

---
`tcp.port==24`
>show packet of port 24 only

---

## TOP 10 FILTERS

### 1. ip filters
```
ip.addr==<ip>
ip.src==<source_ip>
ip.dst==<destination_ip>
ip.addr==192.168.1.0/24
# all packets from subnet

```

### all ip, mac , endpoints, to which we communicate
go to
`Statistics > Endpoint`

> give all ip info , size to data sents , packets, Tx , Rx bytes , TCP , UDP

---


### 2.  Make filter Button

Apply Filter then 
> click ''+'' button  front of filter bar 
> this make filter button

* nested / multiple filter button in one
> example :- 1st filter button :- TCP
> to add another in this :- name will be :- TCP//SYN
> this make SYN button in TCP button

---
### 3. Multiple Ports
```
tcp.port in {80,443,22,53,8000..9000}
```

---
### 4. Conversation between two ip

* `Statistics > Conversation > Tcp > apply filter > A <-> B`
 > it make filter for both ip and their port , theri     session

* `RightClick on packet > Conversation Fileter > Tcp`
> 2nd way to do that

## Conversation 

* `RightClick on packet > Conversation Fileter > Tcp`
> 2nd way to do that
 
 > ==can use instead of Folow Tcp Stream==

---

### 5. Search String in Packets

*
```
tcp contains "String"
# extact word String 
# can use any protocol in place of tcp
```

*
```
tcp matches "String"
# case insensitive search
```

*
```
etc matches "String"
frame mathches "String"
# any protocl any packet , matches string (case insensitive)
```

---

### 6. Not Include
```
!(arp or dns or lldp or eth.addr==ff:ff:ff:ff:ff:ff or tcp.port in {8080,22})
```
> remove all this stup for pcap , not include these

---

### 7. Make pcap small

> make pcap small , remove unnessary stuff

```
1. apply filters , to remove unnessary

2. File > Export Specified Packets
```

### 8. ONLY Tcp Flags
```
tcp.analysis.flags
```

### 9. Slow DNS
```
dns.time > 0.2
```
> dns response greater than 200 milisecond

---

### iRTT (round trip time)
* in TCP details , 
* make IRTT as column
* packets from single conversation gave same iRtt time

---
