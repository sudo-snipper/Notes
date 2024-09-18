```bash
#!/bin/bash
cat << EOF
these text are here document texts
$PATH
$variable
"$variable"
'$variable'

EOF
```

## OUTPUT

```text
these text are here document texts
/usr/bin
variable_value
"variable_value"
'variable_value'

```
 <br> <br> 
> it pass all texts written in inside of **EOF** to the command before it  (can use any word replace of EOF)  
> it use quotes as characters  , use to insert quotes

--- 

## ex-2
```bash
#!/bin/bash

# Add three commands inside the heredoc content with the `sudo` command
sudo -s  <<COMMAND
date
pwd
whoami
COMMAND
```

---
## leading TAB
 > to reject tab at start of lines
> use <<-


`cat <<-END`

---

## ouput redirect
```bash
#!/bin/bash
OUT=/tmp/output.txt
 
echo "Starting my script..."
echo "Doing something..."
 
cat <<EOF >$OUT
  Status of backup as on $(date)
  Backing up files $HOME and /etc/
EOF
 
echo "Starting backup using rsync..."
```

OR 
> cat << EOF >> myfile.txt