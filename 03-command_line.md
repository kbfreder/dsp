# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands

Here's a list of items with which you should be familiar:
* pwd: show current working directory path
* mkdir: creating a directory
* rmdir: deleting a directory
* touch <filename>: creating a file using `touch` command
* rm: deleting a file
* mv <old name> <new name>: renaming a file
* ls -a: listing hidden files
* cp: copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)
>>
* rm -r <dir>: deletes a non-empty directory
* cd: change directory

---

### Q2.  List Files in Unix

What do the following commands do:
`ls`
`ls -a`
`ls -l`
`ls -lh`
`ls -lah`
`ls -t`
`ls -Glp`
'''
>> 
- ls: list of files in current dir
- ls -a: includes hidden files
- ls -l: long list
- ls -lh: as above, but includes file size unit
- ls -lah: long list, including hidden files, showing file size unit
- ls -t: sort by time modified
- ls -Glp: colorized output, in long form, with slash after filename if it is a directory

'''
---

### Q3.  More List Files in Unix

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

>>
- -d: display only directories
- -r: display in reverse order
- -R: display subdirectories as well (!!)
- -u: display by access time
- -1: new line for each entry

---

### Q4.  Xargs

What does `xargs` do? Give an example of how to use it.

>> 
It builds and executes commands from standard input\
ex: remove files in 'tmp' folder older than 2 weeks: 
`find /tmp -mtime +14 | xargs rm
