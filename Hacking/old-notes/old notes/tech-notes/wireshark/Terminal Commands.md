### 1. For  Add Wireshark in terminal in Windows
 > add wireshark folder in PATH variables

---
### Commands
* `dumpcap -D` 
> to list Interfaces

* `dumpcap -i 1 -w /usr/share/pcap.pcapng`
> -i , specify number of interface
> -w , specify write file for pcap

* `dumpcap -i 1 -w file.pcapng -b filesize:500000 -b files:5`
> filesize:500000 , take size in kilobytes
> files:5 , ring buffer values , total number of files 