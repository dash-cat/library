# Bash Cheat Sheet

This cheat sheet provides a quick reference to common Bash commands and concepts, ideal for everyday use.

## Basic Commands

- `ls`: List directory contents.
- `cd directory`: Change the current directory.
- `pwd`: Print the working directory.
- `cp source destination`: Copy files or directories.
- `mv source destination`: Move/rename files or directories.
- `rm file`: Remove files.
- `mkdir directory`: Create a directory.
- `rmdir directory`: Remove an empty directory.
- `touch file`: Create or update a file.
- `echo "text"`: Display text.

## File Permissions

- `chmod permissions file`: Change file permissions.
- `chown user:group file`: Change file owner and group.

## Redirection

- `command > file`: Redirect output to a file (overwrite).
- `command >> file`: Append output to a file.
- `command < file`: Take input from a file.
- `command1 | command2`: Pipe output to another command.

## Process Management

- `ps`: Display active processes.
- `top`: Display all running processes.
- `kill pid`: Kill a process by PID.
- `killall processname`: Kill processes by name.

## Networking

- `ping host`: Check connectivity to a host.
- `ssh user@host`: Connect to a host.
- `scp source user@host:destination`: Copy files to a remote host.

## Searching and Sorting

- `grep pattern file`: Search for a pattern in a file.
- `find directory -name pattern`: Find files matching a pattern.
- `sort file`: Sort file contents.

## Text Processing

- `cat file`: Display file content.
- `head file`: Display the first 10 lines of a file.
- `tail file`: Display the last 10 lines of a file.
- `awk pattern { action } file`: Process text with AWK.
- `sed 's/pattern/replacement/' file`: Replace text with SED.

## System Information

- `df`: Display disk space.
- `du`: Display directory space usage.
- `free`: Display memory usage.
- `uname -a`: Display system information.

## Bash Scripting

- `#!/bin/bash`: Start a bash script.
- `variable=value`: Assign a value to a variable.
- `$variable`: Access a variable's value.
- `if [ condition ]; then ... fi`: Conditional statement.
- `for var in list; do ... done`: For loop.
- `while [ condition ]; do ... done`: While loop.
- `function name { ... }`: Define a function.

## Miscellaneous

- `man command`: Display a command's manual.
- `history`: Display command history.
- `alias name='command'`: Create a command alias.
