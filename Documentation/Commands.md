# Terminal

`clear`: Clears the terminal

# System
`sudo shutdown`: Shuts down the system

`sudo reboot`: Reboots the system

## Updates

`sudo apt update`: Fetches the latest version of the package list from your distro's software repository

`sudo apt upgrade`: Downloads and installs the updates for each outdated package and dependency on your system

`apt list --upgradable`: Shows a list of upgradable packages

`sudo apt autoremove`: Removes packages no longer required

# Installation

To find out exactly where the diff program resides on the filesystem:

`which diff`: To find out exactly where the diff program resides on the filesystem

`whereis diff`: Good alternative because it looks for packages in a broader range of system directories

For example, to find out where firefox is installed:

`which firefox`

`whereis firefox`

# Navigating the filesystem
Commands useful for directory navigation:

`pwd`: Displays the present working directory

`cd ~` or `cd`: Change to your home directory; shortcut name is ~ (tilde)

`cd ..`: Change to parent directory (..)

`cd -`: Change to previous working directory; - (minus)

`tree -d`: To view just the directories and to suppress listing file names

# Working with files

## Directories

`mkdir sampdir`: Creates a sample directory named sampdir under the current directory

`mkdir /usr/sampdir`: Creates a sample directory called sampdir under /usr

`rmdir sampdir`: Removes the sampdir directory in the current folder, the directory must be empty or it will raise an error

`rm -rf sampdir`: Removes the sampdir directory in the current folder and all of its contents

## Files

`mv original_name.txt new_name.txt`: Renames a file in the current directory with the name original_name.txt to new_name.txt

`rm filename.txt`: Removes a file in the current directory called filename.txt. -f:Forcefully remove a filerm -i:Interactively remove a file

`touch file1.txt`: Creates a file called file1.txt on the current directory

`ls`: List all the files in the current directory

`ls -l file1.txt`: Check the existence of file1.txt in the current directory

### Find

`find`: Recurses down the filesystem tree from any particular directory (or set of directories) and locates files that match specified conditions

`find /usr -name gcc`: Searching for files and directories named gcc

`find /usr -type d -name gcc`: Searching only for directories named gcc

`find /usr -type f -name gcc`: Searching only for regular files named gcc

`find -name "*.swp" -exec rm {} ';'`: -exec is used to run commands on the files found. This example finds and removes all files that end with .swp

## Searching for files

`updatedb`: Updates the database created by updatedb utility.

`locate filename.txt`: Locates the directory of filename.txt by searching in the database created by the updatedb utility

# Manual pages

## Man pages

For the example of the man pages the sysctl command will be used.

`man -f sysctl`: List all pages on the topic

`man -k sysctl`: List all pages that discuss a specific topic (even if the specified subject is not present in the name)

`man -a sysctl`: Display all pages with the given name in all chapters, one after the other

`man 2 sysctl`: Displays the pages in the 2nd chapter

## GNU Info

`info`: Displays an index of available topics. You can browse through the topic list using the regular movement keys: arrows, Page Up, and Page Down. q to quit, h for help, and Enter to select a menu item. You can view help for a particular topic by typing info topic name.

## Command help

`sysctl --help`: To display a short description of the command.

# Processes

`w`: The load average 

`jobs -l`: Processes launched from the current terminal windos session

`ps`: Provides information about currently running processes keyed by PID. Use the -u option to display information of processes for a specified username. The command ps -ef displays all the processes in the system in full detail. The command ps -eLf goes one step further and displays one line of information for every thread (remember, a process can contain multiple threads).

`pstree`: Displays the processes running on the system in the form of a tree diagram showing the relationship between a process and its parent process and any other processes that it created.

`top`: Static view of what the system is doing is useful, monitoring the system performance live over time is also valuable.
