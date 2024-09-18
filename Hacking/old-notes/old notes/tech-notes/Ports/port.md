**0 is wild card port if we try to connect to this it automatic connect to port above 1024**

| Ports | Protocols | Protocol used | Used for |
| :---- | :-------- | :------------ | :------- |
| 20| FTP-DATA| TCP| File transfer-Data (ftp **send/recieve on port 20**)|
| 21| FTP|TCP|File transfer-control (ftp **server listen on 21**)
|22|SSH|TCP|
|22|SFTP|TCP|FTP over SSH (**encrypt data and send by SSH**)
|23|TELNET|TCP|
|25|SMTP|TCP|outgoing email message|
|53|DNS|TCP and UDP|
|67|DHCP|UDP|server listen on 67|
|68|DHCP|UDP|client listen on 68|
|69|TFPT|UDP|
|80|HTTP|TCP and UDP|
|88|Kerberos|TCP and UDP|
|110|POP3|TCP|incoming email (download email)|
|123|NTP|UDP|network time sync|
|143|IMAP4|TCP|incoming email (store on server)|
|161|SNMP|TCP and UPD|network device manage|
|389|LDAP|TCP and UPD|access and lookup on network info and devices|
|443|HTTPS|TCP|
|445|SMB|TCP|(server message block)network file sharing|
|636|LDAPS|TCP and UDP| ldap over ssl|
|989|FTPS|TCP|FTP with SSL|
|990|FTPS|TCP|FTCP with SSL|
|1720|H.323|TCP| in multimedia session (like : calls (voip), video ,message)
|3389|RDP|TCP|
|5060|SIP|UDP|unencrypted multimedia session|
|5061|SIP|UDP|encrypted multimedia session\




