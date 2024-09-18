## hping3 

**for scannig , custom packet generator**

* `hping3 --scan 0-1023 192.168.1.1`
   > basic scan , no Flags sets

* `hping3 --scan 0-1023 -S 192.168.1.1`
   > Only SYN Flag set

* `hping3 --scan 0-1023 -F 192.168.1.1`
   > Fin flag

* `hping3 --scan 0-1023 -R 192.168.1.1`
  > RST flag

* `hping3 --scan 0-1023 -U 192.168.1.1`
  > Urgent flag

* `hping3 --scan 0-1023 -FUP 192.168.1.1`
  > **many Flags**
  > FIN, Urgetn , push 
  > XMas scan

* `hping3 --scan 0-1023,2000-3000 192.168.1.1`
  > **custom port**