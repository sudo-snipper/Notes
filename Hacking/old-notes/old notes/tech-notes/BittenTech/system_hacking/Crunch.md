## charcter sets
`/usr/share/crunch/charset.lst`
> can write own character set file

```
crunch 3 4 -f /usr/share/crunch/charset.lst hex-lower -o wordlist.txt
```

---

## pattern
 ```
 crunch 8 8 -t @@@admin -o wordlist.txt
 ```
 > replace characters to that symbol
 > @ **lower case**
 > ,    **upper case**
 > % **numbers**
 > ^  **symbols**

---

## start word
```
crunch 8 8 -t @@@admin -s bbbadmin -o wordlist.txt
```
> -s options , specify to start wordlist form bbbadmin not from aaaadmin

---

## words
```
crunch 8 8 -p this pass 
```
> it will use only these words

