## dash file in linux
 * create
    > `touch -- -file`
    > `touch -- -`
* read
   > `cat > -`
   > `cat > -file`
   
* delete
   >`rm -rf -- -`
   >`rm -rf -- -file`
---
## print uniq lines only
> `sort file.txt | uniq -u`

---
## print only ASCII text of file
`strings file.txt`
  