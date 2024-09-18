* `variable_name = value`
* `echo variable_name`
  > to print varible 

---

* `var1 = file.txt`
  `var2 = target.txt`
  `cp $var1 $var2`
  > copy file.txt content to target.txt

---

* `declare -r Var = value`
  > set varible to read only

---

* `var="this is \n new line"`
   `echo -e $var`
   > pass escape sequence
   > use -e to make escape sequence execute

* `var="$(ls -la )"`
  > pass commands

---

* `mv "$myfile" "${myfile}_bak"`
   > if **myfile =  filename**
   > then , output file will be :-- **filename_bak**
   > use **{ }** to pass command 