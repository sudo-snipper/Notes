## zone transfer

* get zone  file for info
* To get zone_file :-- **pretend to be secondary DNS**
*  query primary dns for file
*  it use **name servers**

---

1.  ### by HOST command
    *  get nameservers `host -t ns test.com`
     *  get zonefile ` host -l test.com name_server_name`
  ----
  
2. ### by NSLOOKUP command
	* `nslookup`
	* it bring shell of nslookup, then query there to use
	* `set type=mx`  use to set type , it set mx record
	* `google.com`
	* ![26af573106676a13f01c744969357265.png](../../../_resources/26af573106676a13f01c744969357265.png)
	* ### for zone file
	 ```
	 nslookup
	 server name_server_name
	 set type=any
	 ls -d test.com 
	 # -d specifiy the domain 
	 # ls command not work in linux 
	```

----

3. ### by DIG command
  ```
  dig google.com -t ns
  # use +short to get minimal point to point answer
  dig axfr @name_server_name test.com
  # axfr state full zone file
 ```
