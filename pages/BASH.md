# Class 1
- BASH is a dependencies coding language
- We use `echo` to print anything to terminal
- Use command `echo $SHELL` to know what SHell you are using
- Use `nano` to create or edit any `.sh` files
- to make that `.sh` use command `chmod` so it's executable
- `chmod +x mycript.sh` for example, `+x` is to add excutable permissions
- Use `cat` to print contents in a text file to the terminal
- use `pwd` to print you current working directory
- Script can be write in multiple line, execute like interpreter
	- ```sh
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
- This will tells the Shell which [[runtime]] or [[intepreter]]  to execute this BASH Script
- {{Can we do Multiple Output And print A VArible}}