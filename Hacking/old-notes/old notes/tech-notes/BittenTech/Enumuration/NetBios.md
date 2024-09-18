## Network basic input output system
* use netbios protocol
*  used assing names (identifiers) in local network
* session managment in local network
* help in sharing resources (files ,printers etcc)
* 16 ASCII character long
* first 15 :---  name of device or user
* last 1:--- service or name types
* not for ipv6
* ![9c2555cc88744aa14212641630a441f7.png](../../../_resources/9c2555cc88744aa14212641630a441f7.png)

* use udp to access netbios names over port 137
* netbios session on port 139 :--  CALL command to start session
* Hang-UP :--- command to stop session
* use broadcasting to ask if name is assisgened or not

----

Tool Use :--- **nbtstat**
`nbtstat -A 192.168.1.3`