# Shell Scripting Cheat Sheet

This cheat sheet provides a quick reference guide for common shell scripting commands and practices.

## Basic Shell Commands

- `echo "text"`: Print text to the terminal.
- `read var`: Read input from the user and store it in `var`.
- `if [ condition ]; then ... fi`: Conditional statement.
- `for var in list; do ... done`: For loop.
- `while [ condition ]; do ... done`: While loop.
- `case word in pattern) commands ;; esac`: Case statement.

## File Operations

- `touch file`: Create a new file or update an existing file's timestamp.
- `cp source destination`: Copy files or directories.
- `mv source destination`: Move/rename files or directories.
- `rm file`: Delete files.
- `mkdir directory`: Create a directory.
- `rmdir directory`: Remove a directory (if empty).
- `grep pattern file`: Search for a pattern in a file.

## Text Processing

- `cat file`: Display file content.
- `head file`: Display the first lines of a file.
- `tail file`: Display the last lines of a file.
- `sort file`: Sort lines in a file.
- `uniq file`: Report or omit repeated lines in a file.
- `awk '{ action }' file`: Pattern scanning and processing language.
- `sed 's/pattern/replacement/' file`: Stream editor for filtering and transforming text.

## Permissions and Ownership

- `chmod permissions file`: Change file permissions.
- `chown user:group file`: Change file owner and group.

## Environment and Variables

- `export VAR=value`: Set environment variable `VAR`.
- `$VAR`: Access the value of an environment variable.
- `printenv`: Print environment variables.

## Networking

- `ping host`: Check the reachability of a host.
- `curl url`: Transfer data from or to a server.
- `wget url`: Retrieve files from the web.

## System Information and Management

- `df`: Report file system disk space usage.
- `du`: Estimate file space usage.
- `top`: Display Linux processes.
- `ps`: Report a snapshot of current processes.

## Shell Script Structure

- Shebang: `#!/bin/bash` or `#!/bin/sh` at the start of a script.
- Comments: Use `#` to add comments.
- Executable: Make the script executable with `chmod +x script.sh`.

## Best Practices

- **Quote Variables**: Always quote your variables (`"$var"`) to prevent word splitting and globbing issues.
- **Check for Command Success**: Use `$?` to check the success of the last executed command.
- **Use Functions**: Group code into reusable functions.
- **Error Handling**: Use `set -e` to stop the script on errors.

This cheat sheet is designed to provide a quick overview and reference. For more detailed information, consult the man pages or detailed shell scripting guides.
