> Exit status is code that command give after run 

## 0 means code run success
## 1 means not success or some error message 

> To find the exit status code

```
#!/bin/bash

sudo apt install this || echo $?

```

---
`echo $?`
 > this command show status of last executed command

example 
```
#!/bin/bash

# last command is 

bash script.sh

# to find status of last command

echo $?
```

---
### To set custom Exit status code

example

```
#!/bin/bash

echo 'this is code'

echo 'setting custom status code'

exit 12


```

> the command  `exit 12`, will set custom code , here it set to 12

> running command `echo $?`, after the above code , it will gave exit status of 12



