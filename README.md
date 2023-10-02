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

`cd /path/to/directory`       #move to a specific directory:
`cd ~`                        #move to your home directory
`cd ..`                       #move up one directory (to the parent directory)
`cd - `                       #move to the previous directory you were in (if you've recently changed directories)

The cd command is a fundamental tool for navigating and working with files and directories in the Linux command line. 

![pwd Command](./Img/3.png)

### The `ls` Command 
The ls command in Linux is used to list the files and directories in the current directory or a specified directory. It provides a basic overview of the contents of a folder.

`ls`                          #List files and directories in the current directory
`ls /path/to/directory`       #List files and directories in a specific directory
`ls -l`                       #List files and directories with additional information
`ls -la`                      #List files and directories in a long format, including hidden files
`ls -lh`                      #List files and directories in a human-readable format

![pwd Command](./img/4.png)
![pwd Command](./img/5.png)
![pwd Command](./img/6.png)

### The `echo` Command

The echo command in Linux is used to print text or messages to the terminal or standard output. It is often used in shell scripts or command-line operations to display information or create simple outputs.

`echo "Hello, World!"`                                  #Display a message or text on the terminal
`variable="Value"`, `echo $variable`                    #Print the value of a variable
`echo "Some text" > output.txt`                         #Redirect the output of echo to a file
`echo "Additional text" >> existingfile.txt`            #Append text to an existing file
`echo "The current date is $(date)"`                    #Display the result of a command or command substitution


### The `cat` Command
The cat command in Linux is used to display the contents of one or more text files on the terminal. 

`cat filename.txt`                              #Display the contents of a single file
`cat file1.txt file2.txt`                       #Concatenate and display the contents of multiple files
`cat -n filename.txt`                           #Display the contents of a file with line numbers
`cat file1.txt file2.txt > combined.txt`        #Create a new file or overwrite an existing file by combining the contents of multiple files
`cat file1.txt file2.txt >> existingfile.txt`   #Append the contents of one or more files to an existing file

![pwd Command](./img/7.png)

### The `cp` Command
The cp command in Linux is used to copy files and directories from one location to another. It allows you to duplicate files and directories while preserving their attributes and content.

`cp sourcefile.txt destination/`            #Copy a file to another location
`cp file1.txt file2.txt destination/`       #Copy multiple files to a directory
`cp -r sourcedirectory/ destination/`       #Copy a directory and its contents recursively to another location
`cp -a sourcefile.txt destination/`         #Preserve file attributes (such as permissions, timestamps, and ownership) when copying
`cp -i sourcefile.txt destination/`         #Prompt for confirmation before overwriting an existing file
`cp -s sourcefile.txt symlinkname`          #Create a symbolic link (symlink) to a file or directory instead of copying its contents
