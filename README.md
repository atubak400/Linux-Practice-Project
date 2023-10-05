# Introduction to linux
Linux is an open-source, Unix-like operating system kernel that serves as the core component of various Linux distributions. It provides a stable and customizable platform for running computer systems, from servers and desktops to embedded devices.

## What is Linux Command
Linux commands are text-based instructions that allow users to interact with the Linux operating system. They are used to perform tasks such as file manipulation, system administration, and program execution, providing a powerful and flexible way to manage and control Linux systems. All linux commands are case sensitive.

An example of linux command is `ls`
The "ls" command is used to list the files and directories in the current directory, providing a basic overview of the contents of the folder you are in.

## File Manipulation
### The `sudo` Command
The "sudo" command in Linux is used to execute a command with superuser privileges or as another user, typically the root user. It is often used to perform administrative tasks that require elevated permissions. If you want to update the package list on a Debian-based system using the "apt" package manager, you can use "sudo" like this: `sudo apt update`

You will be prompted to enter your password to confirm your identity before the command is executed with superuser privileges. This helps enhance system security by restricting elevated access only to authorized users.

![sudo Command](./img/1.png)

### The `pwd` Command
The pwd command in Linux stands for "print working directory." When you run this command, it displays the current directory or folder you are in within the Linux file system. This can be useful to determine your current location in the directory structure. Here's how you use it: `pwd`

Upon running this command, it will provide the full path to the current directory, helping you understand your file system context.

![pwd Command](./img/2.png)

### The `cd` Command
The cd command in Linux stands for "change directory." It is used to navigate through the directory structure of the Linux file system by changing your current working directory. You specify the directory you want to move to as an argument to the cd command

* `cd /path/to/directory`       #move to a specific directory:
* `cd ~`                        #move to your home directory
* `cd ..`                       #move up one directory (to the parent directory)
* `cd - `                       #move to the previous directory you were in (if you've recently changed directories)

The cd command is a fundamental tool for navigating and working with files and directories in the Linux command line. 

![cd Command](./img/3.png)

### The `ls` Command 
The ls command in Linux is used to list the files and directories in the current directory or a specified directory. It provides a basic overview of the contents of a folder.

* `ls`                          #List files and directories in the current directory
* `ls /path/to/directory`       #List files and directories in a specific directory
* `ls -l`                       #List files and directories with additional information
* `ls -la`                      #List files and directories in a long format, including hidden files
* `ls -lh`                      #List files and directories in a human-readable format

![ls Command](./img/4.png)
![ls Command](./img/5.png)
![ls Command](./img/6.png)

### The `echo` Command

The echo command in Linux is used to print text or messages to the terminal or standard output. It is often used in shell scripts or command-line operations to display information or create simple outputs.

* `echo "Hello, World!"`                                  #Display a message or text on the terminal
* `variable="Value"`, `echo $variable`                    #Print the value of a variable
* `echo "Some text" > output.txt`                         #Redirect the output of echo to a file
* `echo "Additional text" >> existingfile.txt`            #Append text to an existing file
* `echo "The current date is $(date)"`                    #Display the result of a command or command substitution

![echo Command](./img/7.png)

### The `cat` Command
The cat command in Linux is used to display the contents of one or more text files on the terminal. 

* `cat filename.txt`                              #Display the contents of a single file
* `cat file1.txt file2.txt`                       #Concatenate and display the contents of multiple files
* `cat -n filename.txt`                           #Display the contents of a file with line numbers
* `cat file1.txt file2.txt > combined.txt`        #Create a new file or overwrite an existing file by combining the contents of multiple files
* `cat file1.txt file2.txt >> existingfile.txt`   #Append the contents of one or more files to an existing file

![cat Command](./img/8.png)

### The `mv` Command
The mv command in Linux is used to move or rename files and directories. It allows you to change the location of a file or directory within the file system or simply rename it. 

* `mv sourcefile.txt destination/`            #Move a file to another location
* `mv oldname.txt newname.txt`                #Rename a file
* `mv sourcedirectory/ destination/`          #Move a directory and its contents to another location 
* `mv oldname/ newname/`                      #Rename a directory
* `mv file1.txt file2.txt destination/`       #Move multiple files into a directory
* `mv -f sourcefile.txt destination/`         #Forcefully overwrite an existing file at the destination

![mv Command](./img/10.png)

### The `cp` Command
The cp command in Linux is used to copy files and directories from one location to another. It allows you to duplicate files and directories while preserving their attributes and content.

* `cp sourcefile.txt destination/`            #Copy a file to another location
* `cp file1.txt file2.txt destination/`       #Copy multiple files to a directory
* `cp -r sourcedirectory/ destination/`       #Copy a directory and its contents recursively to another location
* `cp -a sourcefile.txt destination/`         #Preserve file attributes (such as permissions, timestamps, and ownership) when copying
* `cp -i sourcefile.txt destination/`         #Prompt for confirmation before overwriting an existing file
* `cp -s sourcefile.txt symlinkname`          #Create a symbolic link (symlink) to a file or directory instead of copying its contents

![cp Command](./img/9.png)

### The `mkdir` Command
The mkdir command in Linux is used to create new directories or folders within the file system. It allows you to organize and structure your files and data by creating directories to contain them.

* `mkdir new_directory`                       #Create a new directory in the current location
* `mkdir /path/to/new_directory`              #Create a new directory with a specified path
* `mkdir dir1 dir2 dir3`                      #Create multiple directories with a single command
* `mkdir -p /path/to/nested/directory`        #Create parent directories along with a new directory if they don't already exist
* `mkdir -m 755 new_directory`                #Create directories with specific permissions (e.g., read, write, and execute permissions)

![mkdir Command](./img/11.png)
![mkdir Command](./img/12.png)


### The `touch` Command
The touch command in Linux is used to create new empty files or update the access and modification timestamps of existing files. Here are some common usages of the touch command:

* `touch filename.txt`                                  #Create a new empty file
* `touch file1.txt file2.txt file3.txt`                 #Create multiple empty files with a single command
* `touch existingfile.txt`                              #Update the access and modification timestamps of an existing file
* `touch -d "2023-10-02 15:30:00" filename.txt`         #Create a new file with a specific timestamp

![touch Command](./img/13.png)


### The `locate` Command
The locate command in Linux is used to quickly locate files and directories on your system based on a pre-built database of file names and paths. It provides a fast way to search for files without the need to traverse the entire file system.

* `locate example`                                       #to find all files with the word "example" in their name or path
* `locate -i school*note`                                #to search for files that contain the words school and note, whether they use uppercase or lowercase

![locate Command](./img/14.png)
![locate Command](./img/15.png)

### The `grep` Command
The grep command in Linux is a powerful tool used for searching and pattern matching within text files or the output of other commands. It allows you to find and display lines in files or text streams that match a specified pattern or regular expression. 

* `grep "search_string" filename.txt`                    #Search for a specific string in a file
* `grep "search_string" file1.txt file2.txt`             #Search for a string in multiple files
* `grep -i "pattern" filename.txte`                      #Perform a case-insensitive search
* `grep -n "pattern" filename.txt`                       #Display line numbers with matching lines
* `grep -r "pattern" /path/to/directory/`                #Search recursively in directories and subdirectories
* `grep "^start.*end$" filename.txt`                     #Use regular expressions for more complex pattern matching

![grep Command](./img/16.png)


### The `find` Command
The find command in Linux is a powerful tool for searching and locating files and directories within a file system. It allows you to search for files and directories based on various criteria, including their names, types, sizes, and modification times.

* `find . -name filename.txt`                              #Find a file by name in the current directory and its subdirectories
* `find /path/to/search -type f -name "*.pdf"`             #Search for files by a specific type (e.g., find all PDF files)
* `find /path/to/search -type d -name "dirname"`           #Find directories by name
* `find /path/to/search -type f -size +10M`                #Search for files by size (e.g., find all files larger than 10MB)

![find Command](./img/17.png)

### The `which` Command
The which command in Linux is used to locate and display the full path of an executable program or script in your system's directories. It helps you identify the location of a specific command that you intend to run

* `which command_name`                                     #basic syntax of the which command
* `which ls`                                               #to find the location of the ls command

![which Command](./img/18.png)

### The `df` Command
The df command in Linux is used to display information about disk space usage on mounted file systems. It provides details about the total disk space, used space, available space, and other relevant information for each mounted file system.

* `df [options] [filesystem...]`                        #basic syntax of the df command
* `df`                                                  #Display disk space usage for all mounted file systems
* `df -h`                                               #Display disk space usage in a human-readable forma
* `df /path/to/directory`                               #Show disk space usage for a specific file system or directory

![df Command](./img/19.png)

### The `du` Command
The du (disk usage) command in Linux is used to estimate and display the disk space usage of files and directories. 
It provides information about the size of files and directories, helping you identify which parts of your file system consume the most storage space.

* `du /path/to/directory`                                   #Display the disk space usage of a specific directory
* `du [-shx][directory or file path]`                       #basic syntax of du command
* `du -s .`                                                 #total disk space used in current directory
* `du -hs * | sort -rh | head -50`                          #sort and display top 50 largest folders in MB
* `du -sh /path/to/directory`                               #Display the total disk space usage for a directory and its subdirectories

![du Command](./img/20.png)
![du Command](./img/21.png)

### The `head` Command
The head command in Linux is used to display the beginning (the "head") of a text file or the output of a command. By default, it shows the first 10 lines of a file or the first 10 lines of the output from a command

* `head [options...] [file ...]`                         #display first few lines from each FILE to standard output
* `head filename`                                        #display first few lines from text files (default is ten, can be changed with `-n`)
* `head -n 5 filename.txt`                               #Display a specific number of lines (e.g., 5 lines) from the beginning of a file
* `head file1.txt file2.txt`                             #Display the first few lines of multiple files

![head Command](./img/22.png)

### The `tail` Command
The tail command in Linux is used to display the end (the "tail") of a text file or the output of a command. By default, it shows the last 10 lines of a file or the last 10 lines of the output from a command

* `tail filename`                                         #display last n number of line from given textfile, default is ten
* `tail file1.txt file2.txt`                              #Display last few lines of multiple files

![tail Command](./img/23.png)

### The `diff` Command
### The `tar` Command

## File Permission and Ownership
### The `chmod` Command
### The `chown` Command
### The `jobs` Command
### The `kill` Command
### The `ping` Command
### The `wget` Command
### The `uname` Command
### The `top` Command
### The `history` Command
### The `man` Command
### The `echo` Command
### The `zip`, `unzip` Commands
### The `useradd`, `userdel` Commands
### The `apt-get` Command
### The `nano`, `vi`, `jed` Commands
### The `alias`, `unalias` Commands
### The `su` Command
### The `htop` Command
### The `ps` Command
