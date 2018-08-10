# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
>> pwd
* creating a directory
>> mkdir
* deleting a directory
>> rm -r dirname
* creating a file using `touch` command
>> touch filename.ext
* deleting a file
>> rm -r filename.ext
* renaming a file
>> mv oldname newname
* listing hidden files
>> ls -a
* copying a file from one directory to another
>> cp filename newdir
* change active directory
>> cd newdir
* list files in active directory
>> ls

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

---

### Q2.  List Files in Unix   

What do the following commands do:  
* `ls`:
>> list the files and folders in the current directory  
* `ls -a`:
>> list all hidden files as well
* `ls -l`: 
>> long format
* `ls -lh`: 
>> long format with sizes in human readable format
* `ls -lah`: 
>> long format, human readable sizes also for hidden files
* `ls -t`: 
>> list files fored bz modification time
* `ls -glp`: 
>> Displays the long format listing, but exclude the owner name, with directories with per sign

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

'ls -p':
>> displays directories with per sign

'ls -t':
>> displays newest files first (based on timestamp)

'ls -u':
>> displays files by the file access time

'ls -a':
>> displays hidden files as well

'ls -R':
>> displaysfile subdirectories as well

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

>> The xargs command in UNIX is a command line utility for building an execution pipeline from standard input.
>> Example: create/delete a list of directories in a single line command 

 

