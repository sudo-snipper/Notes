## simple mail transfer protocol
* ![3b9eedbcd28eb3d4e759c4b78f1eb8e2.png](../../../_resources/3b9eedbcd28eb3d4e759c4b78f1eb8e2.png)

* connect to smtp port
  `telnet <ip> <port>`
* then specify sender mail
   `MAIL FROM:mymail@email.com`
* then , mannual bureforce user accounts 
   	`VRFY user`
	`VRFY root`
	* code for **valid user is 252**
	* code for **invalid user is 550**
	* ![583cb33dbb4ad6e72001ed8364a178e5.png](../../../_resources/583cb33dbb4ad6e72001ed8364a178e5.png)
* use NMAP scripts
* use MsfConsole 
* 