## metasploit

* ### Auxiliary
  > all files except exploit
  > it contain files for info gathering , scanning etc

* ### NOPS
   > use to evade firewall , detection , antivirus

* ### encoders
	> encoding for bypass , antivirus , firewall etc

* ### Exploit
	> Exploits give you the ability to 'pop a shell/run your payload code

* ### Payloads
	> after exploit use to gain shell or other work on target

---

### staged vs stagless Payload
   1. staged :-
       > work in stages , it has / character in it
	 ex:- 	
`window/meterpreter/reverse_shell`

 2. stagless 
     > work in one stage , have to execute once , it has _ character in it 
      ex: --
	  `window/meterpreter_reverse_shell`

---

## COMMANDS	

### search
```
search <name>
// search anything

search type:exploit <name>
// specific type search

```

### show
```
show <name>
show all thing , like show exploit
```

### info

```
info window/meterpreter_reverse_shell
// info about any module
```