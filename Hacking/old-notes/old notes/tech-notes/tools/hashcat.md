## hashcat

ex: `hashcat -m 0 -a 0 hash.txt wordlisttxt`

---

## force
`--force `
  
  > use when opencl error

---

## brute-force
`hashcat -m <number> -a 3 hash.txt`
> it don't require wordlist
> crack hash without wordlist

---

## Rules
 > if wordlist has lower case it will try with lower word as well as 
 > rule specified lets we specify upper case , it will use both case
### rule file create
`file.rule`

### rule file content

```
:
// stating of file
l
// use wordlist with lowercase
u
// use wordlist with upper case
c
// use wordlist with first capital letter
si!
// use for replace, here :-- replace i with !
```


#### syntax
```
hashcat -m 0 -a 0 hash.txt wordlist.txt -r file.rule
```