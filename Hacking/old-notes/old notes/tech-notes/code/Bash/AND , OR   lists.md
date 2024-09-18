> to understand AND  statement

```
#!/bin/bash

echo "this is message"

# for AND && , first statement have to be true , or its 
# exit status have to zero

echo "this is message" && echo "first command is success"
```

---
> to understand OR statement

```
#!/bin/bash

# for OR || , first message exit status have to be none zero

error_command || echo "first is none zero status"
```

---

> to find the status code 

```
#!/bin/bash

echo "command" || echo $?

# or

echo "command" && echo $?

# also can use other method like if statement
```