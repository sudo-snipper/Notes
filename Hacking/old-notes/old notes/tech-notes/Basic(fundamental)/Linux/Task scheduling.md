## ==systemd==

```
 create a service : 
                                   ex : sudo vim /etc/systemd/system/mytimer.service 
```

**![2023-07-12_08-40.png](../../../_resources/2023-07-12_08-40.png)**

**`with times`** 

![2023-07-12_08-40_1.png](../../../_resources/2023-07-12_08-40_1.png)

After creating service file reload system-deamon(systemd)  / enable created system

**Reload deamon**

sudo systemctl deamon-reload

**Service start/enable**

sudo systemctl enable/start my.service

**==CRON==**

- **crontab -e : **to edit crontab
- **crontab -l : **to list crontab

                      **COMPONETS **

**![2023-07-12_08-46.png](../../../_resources/2023-07-12_08-46.png)** 

**![Cron cheatsheet for Linux.jpg](../../../_resources/Cron%20cheatsheet%20for%20Linux.jpg)**

==**EXAMPLES**==

                      ![2023-07-12_08-58.png](../../../_resources/2023-07-12_08-58.png)

                         ![2023-07-12_08-59.png](../../../_resources/2023-07-12_08-59.png)

                        ![2023-07-12_08-59_1.png](../../../_resources/2023-07-12_08-59_1.png)

                       ![2023-07-12_09-01.png](../../../_resources/2023-07-12_09-01.png)                     

                       ![2023-07-12_08-59_2.png](../../../_resources/2023-07-12_08-59_2.png)

## ==**To check type of service**==

                                   can use : --      **   systemctl show name.service -p Type**

esle : ----            **check for Type filed entry on name.service file **