type:: [[Programming Language]]
language:: [[BASH]]

- # Class 1 (For Referers)
	- **ls (List)**
	  id:: 66552584-024e-4c23-8619-35be2e3944db
		- `ls` is stand for list, it's list all the files and directory in the user `$pwd`
	- **pwd (Print Working Directory)**
		- `pwd` is the command that will print user current working directory
	- **ImageMagick**
	  id:: 6655333b-517a-48a1-9662-db9c49b30db6
		- `magick` is the ImageMagick command that will convert image file as you wish
		- To convert, use `magick input_files.1extension output_files.2extension`
		- For example
		  ```bash
		  magick input.png output.jpg #convert PNG to JPG
		  magick input.png output.pdf #convert PNG to PDF
		  magick *.png output.pdf #convert all PNG Image in current folder into a single PDF
		  ```
	- **Touch**
		- `touch` is use to create a file, simply put a file name you want to create after the touch command, like `touch main.py`
- # Class 2
- BASH is a dependencies coding language
- We use `echo` to print anything to terminal
- Use command `echo $SHELL` to know what SHell you are using
- Use `nano` to create or edit any `.sh` files
- to make that `.sh` use command `chmod` so it's executable
- `chmod +x mycript.sh` for example, `+x` is to add excutable permissions
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
	- ```bash
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
- # Class 3
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
- In order to declare a varible that contain **Other Commands** we can use `$()` to cover the entier command we want
	- ```bash
	  MyCom=$(ls)
	  
	  echo $MyCom
	  ```
	  see ((66552584-024e-4c23-8619-35be2e3944db))
	- It's called **sub-shell**
	- it's run things in the background
- In the Linux Environment, there are **Defualt Variable**, there are var that has been declare
	- Such as
		- `$USER` contain your User name in your system
	- You should declare a varible with all Lowercase, so it's not replace any other defualt var accidentally
	- Run `env` command to see all the defualt var in your system
	-
- # Class 4
	- **Math Function**
		- use command `expr` in case you want to perform any MAth Expression
			- ```sh
			  expr 30 + 10 - 20
			  ```
			  <samp> 20 </samp>
		- Math Expressions are
			- `+` for plus
			- `-` for minus
			- `\*` for for multiplication
				- is case you just use `*` it will leads to error, cause by a wildcards error (BASH thinks it's a wildcards symbol, not a asterisk)
			- `/` for division
		- We can use it with variable
			- ```bash
			  mynum=100
			  expr $mynum + 50
			  ```
			  <samp>150</samp>
- # class 5
	- **testcase**
	  id:: 66553020-31f7-4674-84b0-ea8d304db766
		- It is a condition that happend in the BASH and it will return either **True** or **False**
	- **If Statement**
		- The systax of if statement is...
		  ```bash
		  if [  testcase ] then
		     #any action here
		  fi
		  ```
			- You need _spaces_ between the `[` and `]`
			- the ((66553020-31f7-4674-84b0-ea8d304db766)) is where you put a condition in by...
				- add two varible for both sides
				- in the middle, use `Math Expression`
					- **Math Expression Flag**
						- `-eq` stands for **Equal**
						- `-ne` stands for **Not Equal**
						- `-gt` stands for **Grater Than**
					-
			- Always End the if statement with `fi`
			- For Example, this will echo **"Hi"**
			  ```bash
			  mynum=100
			  
			  if [ $mynum -eq 100 ] then
			     echo "Hi"
			  fi
			  ```
			  <samp>Hi</samp>
	- **Else Statement**
		- The syntax of else statement is...
			- ```bash
			  if [ testcase ] then
			     #first testcase
			  else
			     #Final testcase if others false
			  fi
			  ```
				- There's no need to type `then` in else statement
			- example
			  ```bash
			  mynum=100
			  othernum=105
			  
			  if [ $mynum -eq $othernum] then
			     echo "There are Equal"
			  else
			     echo "There aren't Equal"
			  fi
			  ```
			  <samp>  There aren't Equal </samp>
	- **Reverse The Check**
		- It is a way to reverse a result in ((66553020-31f7-4674-84b0-ea8d304db766))
		- To do it, put `!` in front of any ((66553020-31f7-4674-84b0-ea8d304db766)) like this
		  ```bash
		  [ 500 -eq 500 ] #result as "True"
		  [ ! 500 -eq 500] #result as "False"
		  ```
	- **Files Existing Check**
		- To Check if file exist, put `-f` in ((66553020-31f7-4674-84b0-ea8d304db766)) and follow by the Path to that files
		- Example
		  ```bash
		  if [ -f /bin/magick ] then #check if ImageMagick exists in bin folder
		     magick input.png output.jpg #convert image using ImageMagick
		  else
		     echo "Sorry, you need to install ImageMagick in order to Convert the image"
		  fi
		  ```
		- See more at about `magick` at ((6655333b-517a-48a1-9662-db9c49b30db6))
		-