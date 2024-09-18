---
`nmap <ip>`
> Nmap default use TCP scan
> filtered port mean Firewall only allow specific address
---
`nmap --open <ip>`
>show open ports only

---
`nmap --open -oA file_to_save <ip>`
>save in output in 3 types of file 
>useful for report writing 

---
`nmap -sC -sV -p- <ip>`
>-sC : nmap scripts
>-sV : version , protocol versions
>-p- : scan all 65535 tcp ports

---
`nmap --script=<script-name -p <port> <host>`
> to use scripts

---
`nmap --script=banner -p <port> <host>`
> to get banner (version) of service

---

`nmap -A <host>`
#### all in one
>-A: Enables OS detection and Version detection, Script scanning and Traceroute.
>alternative use ( -O -sV -sC --traceroute)
---

## for fast scan 
`nmap -T5 --min-rate <number> `
>-T<0-5>  : high is faster
>--min-rate < number>  : minimum < number> packet in second
---

 


