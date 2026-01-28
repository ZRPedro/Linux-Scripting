# Linux-Scripting
A bunch of self made scripts to automate tasks on linux based operating systems. In addition some documentation is also available for how to use them.

# Some basic utilities
There are some basic command line utilities that are used constantly, and it would be impossible to proceed further without using some of them in simple form before we discuss them in more detail. A short list has to include:
- cat: used to type out a file (or combine files).
- head: used to show the first few lines of a file.
- tail: used to show the last few lines of a file.
- man: used to view documentation.

# The Command Line
Most input lines entered at the shell prompt have three basic elements:
- Command
- Options
- Arguments

The command is the name of the program or script you are executing. It may be followed by one or more options (or switches) that modify what the command may do. Options usually start with one or two dashes, for example, -p or --print, in order to differentiate them from arguments, which represent what the command operates on.

However, plenty of commands have no options, no arguments, or neither. In addition, other elements (such as setting environment variables) can also appear on the command line when launching a task.

# Absolute and Relative paths
An absolute pathname begins with the root directory (/) and follows the tree, branch by branch, until it reaches the desired directory or file. Absolute paths always start with /.

A relative pathname starts from the present working directory. Relative paths never start with /.

Most of the time, it is most convenient to use relative paths, which require less typing. Usually, you take advantage of the shortcuts provided by: . (present directory), .. (parent directory) and ~ (your home directory).

# Viewing Files

- cat: Used for viewing files that are not very long; it does not provide any scroll-back.
- tac: Used to look at a file backwards, starting with the last line.
- less: Used to view larger files because it is a paging program. It pauses at each screen full of text, provides scroll-back capabilities, and lets you search and navigate within the file.
  - NOTE: Use / to search for a pattern in the forward direction and ? for a pattern in the backward direction. An older program named more is still used, but has fewer capabilities: "less is more".
- tail: Used to print the last 10 lines of a file by default. You can change the number of lines by doing -n 15 or just -15 if you wanted to look at the last 15 lines instead of the default.
- head: The opposite of tail; by default, it prints the first 10 lines of a file.

# I/O Redirection

Through the command shell, we can redirect the three standard file streams so that we can get input from either a file or another command, instead of from our keyboard, and we can write output and errors to files or use them to provide input for subsequent commands.

For example, if we have a program called do_something that reads from stdin and writes to stdout and stderr, we can change its input source by using the less-than sign (<) followed by the name of the file to be consumed for input data:

`do_something < input-file`

If you want to send the output to a file, use the greater-than sign (>) as in:

`do_something > output-file`

In fact, you can do both at the same time as in:

`do_something < input-file > output-file`

Because stderr is not the same as stdout, error messages will still be seen on the terminal windows in the above example.

If you want to redirect stderr to a separate file, you use stderr’s file descriptor number (2), the greater-than sign (>), followed by the name of the file you want to receive everything the running command writes to stderr:

`do_something 2> error-file`

NOTE: By the same logic, do_something 1> output-file is the same as do_something > output-file.

A special shorthand notation can send anything written to file descriptor 2 (stderr) to the same place as file descriptor 1 (stdout): 2>&1.

`do_something > all-output-file 2>&1`

bash permits an easier syntax for the above:

`do_something >& all-output-file`

# Useful terminal commands
To find out some common useful commands for Linux go to:
[Terminal Commands](Documentation/Commands.md)
