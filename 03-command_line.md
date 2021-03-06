# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

Action | Command
--- | ---
Show current working directory | pwd
creating a directory | mkdir [dir]
deleting a directory | rm -r [dir]
creating a file using 'touch' command | touch [file]
deleting a file | rm [file]
renaming a file | mv [file] [newname]
listing hidden files | ls -a
copying a file from one dir to another | cp [file] [dir]
long list of all items sorted by time | ls -alt
view contents of file | cat [file]


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

Command | Action
--- | ---
`ls` | short list of files in current directory
`ls -a` | list including hidden files
`ls -l` | long list of files
`ls -lh` | long list with human readable file sizes
`ls -lah` | long list with human readable sizes and hidden files
`ls -t` | list sorted by mod date
`ls -Glp` | long list with highlighted directory names with closed root

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -1 makes things easy to see, ls -R is useful for a full overview, ls -d is useful to only see directories, ls -m might be useful to iterate over files, ls -xm would make iterations easier

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs allows you to create an execution pipeline using tools like echo, rm, and mkdir. These wouldnt be able to accept standard input without xargs

> > xargs reads the items separated by blanks and executes a command for each. Ex:

> > creating multiple folders:
> > echo 'one two three' | xargs mkdir

 

