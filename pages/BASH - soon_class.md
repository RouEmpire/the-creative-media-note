Type:: [[Programming Language]]
Language:: [[BASH]]

- # Class 1
- BASH is a dependencies coding language
- We use `echo` to print anything to terminal
- Use command `echo $SHELL` to know what SHell you are using
- Use `nano` to create or edit any `.sh` files
- to make that `.sh` use command `chmod` so it's executable
- `chmod +x mycript.sh` for example, `+x` is to add excutable #permissions
	- Use `cat` to print contents in a text file to the terminal
- use `pwd` to print you current working directory
- Script can be write in multiple line, execute like interpreter
	- ```bash
	  echo "Hello Word"
	  ls
	  pwd
	  ```
	- it will run respectively line-by-line
- in every first line of BASH script, we need to type [[shebang]]
	- ```sh
	  #!/bin/bash
	  
	  echo "Hello World"
	  ls
	  pwd
	  ```
- This will tells the Shell which [[runtime]] or [[intepreter]]  to execute this BASH Scrip
  ---
- we can create a files we `.sh` extension _or even no extension at all_ to run the BASH script, incase the file name is `myscript.sh` we type _path to that file_ in terminal to execute that file, incase we are in the same directory of that file, run `./myscript.sh`
	- `.` means _this directory_, it points the file at the current folder you're in
	- `/` means _then_, we put other directory name or other file name in here, if it's a file, it's execute it
	- `myscript.sh` is the file, so ,  BASH will execute it
- # Class 2
- ## How to declare varible
- This is the syntax to declare the variable, use `var` for Variable name and `val` for its Value. To Access its Value, insert `$` at the begin of the variable name, such as `$var` _Do this after declaretions_
- ```bash
  #!/bin/bash
  
   var="val"
   echo  $var   #correct
   echo "$var"  #also correct
  ```
- Such as...
- ```bash
  USER_NAME="RouEmpire"
  echo "Hello , $USER_NAME"
  ```
- The Output is : <samp> Hello , RouEmpire </samp>
  id:: 6638206c-1929-4f01-a39e-9b7ebc2d61f0
- If we try to `echo` a variable that doesn't exists, it will print **An Empty String**
- ## Why we need to use `$`
- We declare varible for using it later, but some times it has a _conflict_ with other things, if we create a varible name `ls` and use it as `$ls`, the [[intepreter]] will use its value, if its has no `$` the command name `ls` will be run instead
- ```bash
  ls="Hello Again"
  
  echo $ls  # print "Hello Again"
  echo  ls  # run 'ls' command
  ```
- Use `exit` command to exit the terminal and **clear all the declared varible**
- ## Example
-