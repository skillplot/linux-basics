---
id: basics-linux-commands
title: Basic Linux Commands
description: Basic Linux Commands
---

Linux CLI (Command Line Interface) is robust and powerful interface to interact with the Linux operating system. We use linux `terminal` application to interact with the CLI. We need to know basic commands to use the command line.


* `man` - Displays the user manual of any command that we can run on the terminal
    ```bash
    ## displays the manual of ls command along with all its options
    man ls 
    ## displays the manual of cat command etc.
    man cat
    ```
* `pwd` - Displays the path of the current working directory
* `ls` - Lists the content of a directory. Can be executed with various options like -a, -l, etc.
    ```bash
    ## Displays content of the current directory
    ls      
    ## Displays the contents of the current directory along with hidden files
    ls -a   
    ## Displays the contents of the current directory along with various other details such as the owner of this file, the read/write permissions of the file, the date and time stamp when the file was last updated, etc.
    ls -l   
    ## Same as ls -l but now displays details for hidden files as well
    ls -al  
    ```
* `cd` - Changes the current directory of the shell
    ```bash
    ## Takes you to the root directory 
    cd /      
    ## Takes you to the parent of the current directory
    cd ..     
    ## Takes you to the parent of the parent of the current directory
    cd ../..  
    ## Takes you to the previous directory you were working in
    cd -      
    ## Takes you to your home directory
    cd ~      
    ```
* `mkdir` - Making a new directory
    ```bash
    ## creates a directory named n_dir
    mkdir n_dir  
    ##  create nested directories.
    ## e.g.  mkdir -p  m_dir/hello/world    //creates a world directory inside a hello directory which itself is inside m_dir directory
    mkdir -p  m_dir/hello/world
    ```
* `rmdir` - Removing a directory
    ```bash
    ## removes directory dir, provided it is empty
    rmdir m_dir
    ## deletes a directory recursively along with its content.
    rm -r m_dir
    ```
* `rm` - Removing file or directory
    ```bash
    ## deletes a directory recursively along with its content.
    rm -r m_dir
    ```
* `touch` - it is used to create an empty file.
    ```bash
    ## Create empty file with file1.txt
    touch file1.txt
    ```
* `cat` - Displays the content of a file 
    ```bash
    ##  Displays the content of the file1
    cat file1       
    ##  Opens file1 for writing into it, if file1 already exists. Otherwise, creates file1 and opens it for writing into it. 
    cat > file1     
    ##  Displays the content of file1 followed by the content of file2
    cat file1 file2 
    ```
* `cp` - Copying the content of a file
    ```bash
    ## copies the content of file1 in file2. Overwrites file2’s content
    cp file1 file2
    ## copies all files (file1 to filen) into the dest directory
    cp file1 file2 …. filen dest
    ## copies file1 into your home directory
    cp file1 ~
    ## Whe suffix  into dest directory
    ## copies all files that have their file names with ".txt” a"
    cp *.txt dest
    ```
* `mv` - Used to move one or more files or directories from one place to another and also for renaming a file or a directory
    ```bash
    ## rename f1.txt to f2.txt 
    mv f1.txt f2.txt
    ## move f1.txt to the directory dir
    mv f1.txt dir/
    ## move f1.txt to the directory dir/new/name/
    mv f1.txt dir/new/name/
    ```
* `wc` - Counting words or lines
    ```bash
    ## counts the number of lines in file1.txt
    wc -l file1.txt
    ## counts the number of words in file1.txt
    wc -w file1.txt
    ## counts the number of bytes in file1.txt
    wc -c file1.txt
    ## counts the number of characters in file1.txt
    wc -m file1.txt
    ```
* `head` - print the top N number of data of the given input. 
    ```bash
    ## prints the first 10 lines of file1.txt
    head file1.txt
    ## Prints the first 5 lines of file1.txt
    head -n 5 file1.txt
    ## Prints the first 5 lines of file1.txt
    head -5 file1.txt
    ## prints the first 2 bytes of file1.txt
    head -c 2 file1.txt
    ```
* `tail` - print the last N number of data of the given input. 
    ```bash
    ## Prints the last 10 lines of file1.txt
    tail file1.txt
    ## Prints the last 5 lines of file1.txt
    tail -n 5 file1.txt
    ## Prints the last 5 lines of file1.txt
    tail -5 file1.txt
    ## Prints the last 2 bytes of file1.txt
    tail -c 2 file1.txt
    ```
* `echo` - used to display lines of text/string that are passed as an argument 
    ```bash
    ## Will display hello world on the terminal
    echo "Hello world"
    ```
* `date` -  Displays the current date and time, day, month name, day of the month, the time zone name, and the year.
* `whoami` - Displays the user name of the current user 
* `who` - Displays information about all users currently logged in. 
* `clear` - Clears the screen
* `cal` - Displays the calendar of a specific month or a whole year.
* `hostname`- Print the host name of the current system.
* `hostnamectl` - Displays OS name and version 
* `uname -r` - Displays kernel version
* `type` - This command is used to know the type of any command. It has some options for  various purposes
    ```bash
    ## command- It will tell us whether the command is alias, keyword or a function, and also tell the path of the executable file.
    type -a
    ## command- It will print whether the command is alias, keyword, builtin, function or a file
    type -t
    ## - It will print the name of the disc file which would be executed
    type -p
    ```
* `grep` - This command is used for searching any file for a particular pattern or a word.
* `find` - This is used to search for a file with particular keywords
* `locate` - This command is used for locating any  file by name.
* `chown`
* `chmod`
* `ln`
* `alias`
* `ifconfig` - This command will give the network configuration of the system.
* `wget`
* `tee`
* `sudo`
* `tree` - List contents of directories in a tree-like format.
    ```bash
    ## To use tree command it has to be installed if it is not installed already.
    ## To install first, update apt repository
    sudo apt update
    ## then install `tree` command from apt repository
    sudo apt install tree
    ```


## Pattern matching using 'grep' command

This command is used for searching any file for a particular pattern or a word.

```bash
man grep
-i, --ignore-case
       Ignore case distinctions, so that characters that differ only in case match each other.
-v, --invert-match
      Invert the sense of matching, to select non-matching lines.
-c, --count
     Suppress normal output; instead print a count of matching lines for  each  input  file.   With  the  -v,
     --invert-match option (see below), count non-matching lines.
-o, --only-matching
    Print only the matched (non-empty) parts of a matching line, with each such part on a separate output line.
```

## Chaining commands using pipe `|`

The Pipe is a command in Linux that lets you use two or more commands such that the output of one command serves as input to the next. In short, the output of each is processed directly as input to the next one like a pipeline. The symbol `|` denotes a pipe.

```bash
## chaining commands using pip `|`
ls -ltr | grep data/*.txt
ls -l | grep *.md
```

## Redirection operators `<, <<` and `> && >>`

* default input (standard input) is from keyboard
* default output (standard output) is to the terminal
* default streams can be changed by using input/output redirection so that the input is taken from a file, and the output goes to a file, for instance.
* output redirection - The output from a command normally intended for standard output can be easily diverted to a file instead. This capability is known as output redirection.
    * If the notation `>` f1 is appended to any command that normally writes its output to standard output, the output of that command will be written to file f1 instead of your terminal.
* The input of a command be redirected from a file
* input redirection - The greater-than character `>` is used for output redirection, the less-than character < is used to redirect the input of a command. This is input redirection.

```bash
who -u > data/userdtls-$(date -d now +'%d%m%y_%H%M%S').txt
```

## File Permissions in Linux

### Changing Ownership (chown)

This command is used to change the owner of the file

* Suppose the current owner of a file named `linux-essentials.txt` is `livesmart` and we want to make "**avenger**" the new owner, use the following command:
    ```bash
    chown avenger linux-essentials.txt
    ```
And if we want to change the owner to and from root, we need to use sudo before the above command.
* `sudo chown root linux-essentials.txt`
* If we want to change the group just put ": " before the name of group in place of file name in the above command.
    ```bash
    chown :group1 linux-essentials.txt
    ```


### Changing Mode (chmod)

It is used for changing the mode of opening the file by a particular user, whether it be the owner, user from the group.

Let's see how we can know that what permissions are given to any user:

* `ls -l`
* After running this command you will get a list, one of which looks like this:
    ```bash
    drwxr-xr-x  5  livesmart   livesmart   4096  Jun 10  16:39   Desktop
    ```
* Here, the first part shows the permissions, lets see how
    * first letter shows whether it is a file or a directory, "d" for a directory, and "-" for a file.
    * next three letters show the permission for the owner of the file, rwx means the owner has permission to read, write as well as execute.
    * next three shows permission for user in the group, whichever letter is missing, that permission is not allowed.
    * next three show for any other user who tries to access it
* To change the permission, say , for the owner
    ```bash
    chmod u=rx file.txt
    ```
    * Now the owner will not be able to modify the file. 
    * we can use "o" and "g" in place of "u" to define for others and users in group respectively.


## Linking in Linux

In Linux we can create a link to a file, which can be used to open the file, which is similar to shortcuts in Windows.Both files will have the same content, and a change in any of the fie will be visible in the other one too.

* To know whether there is any link or not run the command:
    ```bash
    ls -li
    ```
* There are two types of links:
    * Hard link
    * Soft link

### Hard Link

In this link, the Inode value of both the source and the link is same, and thus even when when the source is deleted or shifted.  We cannot link directories via hardlink, only files are allowed. The method to create hard link:
```bash
ln [source path] [new path]
```

### Soft Link

In this link we can also link directories and if we remove the source , the link will be like hanging and not point to anything. The method to create soft link 

```bash
ln -s [source path] [new path]
```


### Shell Aliases

These are shortcuts to reference commands. These are created to avoid typing long commands and thus can be used in place of the reference commands.

```bash
alias l="ls -lrt"
alias home="cd ${HOME}"
```
