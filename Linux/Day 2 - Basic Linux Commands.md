Date - 03/04/2024
# Bourne Shell: /bin/sh
The shell is one of the most important parts of a Unix system. A shell is a program that runs commands, like the ones that users enter into a terminal window.

Many important parts of the linux systems are actually shell scripts that contain sequence of shell commands that will be executed. In MS-DOS it is similar to .BAT files.

There are many different Unix shells, but all derive features from the **Bourne shell (/bin/sh)**, a standard shell developed at Bell Labs.

Linux uses an enhanced version of the Bourne shell called `bash` or the “Bourne-again” shell. The `bash` shell is the default shell on most Linux distributions, and /bin/sh is normally a link to `bash` on a Linux system.
# Using the Shell
# Basic Commands
## ls
- List directory contents.
- When executed without any arguments, it lists the contents of the current directory. Optionally, you can specify a directory path to list its contents.
- For example, use `ls -l` for a detailed (long) listing and` ls -F `to display file type information.
## cp
- cp copies files. 
- For example, to copy file1 to file2 - `cp file1 file2`
- You can also copy a file to another directory, keeping the same file name in that directory: `cp file dir`.
- To copy more than one file to a directory (folder) named dir - `cp file1 file2 file3 dir`
## mv
- Renames file, works similar to `cp`
- `mv file1 file2`
- can also be used to move files from one directory to another similar to `cp`
## touch
- Used to create a file.
- if target file already exists, touch updates the file modification timestamp
- `touch newFile`
- `touch oldFile` - timestamp will be modified to time at which the command was run.
## rm
- Deletes or removes a file.
- After you remove a file, it’s usually gone from your system and generally cannot be undeleted unless you restore it from a backup.
- `rm fileToDelete`
## echo
- Prints arguments to the STDOUT (standard output).
```bash
echo Hello Again
Hello Again
```
- The echo command is very useful for finding expansions of shell globs (“wildcards” such as *) and variables (such as $HOME)

# Navigating Directories
- **/** - root directory
- */* is used as directory separator.
- **.** is used to represent current working directory
- **..** is used to represent parent directory.
- if you’re in `/usr/lib`, the path` . `is still `/usr/lib`, and `./X11` is `/usr/lib/X11`.
- multiple sub-directories under root directory.
![](Screenshots/1.4%20Linux%20File%20System.png)
## cd
- the change directory command
- To change to `/etc/`, use `cd /etc`

>[!info]
>The cd command is a shell built-in. It wouldn’t work as a separate program because
if it were to run as a subprocess, it could not (normally) change its parent’s current working directory. This may not seem a particularly important distinction at the moment, but there are times when knowing this fact can clear up confusion.
## mkdir
- Creates a directory
## rmdir
- Removes a directory.
- It will not remove directories with contents unless you specify the `-r` option (recursive), which removes directories and their contents.
## Wildcards
- Wildcards are characters used to match filenames or strings in commands. 
- The shell can match simple patterns to file and directory names, a process known as **globbing**
- Common wildcards include `*` (matches zero or more characters) and `?` (matches any single character).
- The substitution is called expansion because the shell substitutes all matching filenames for a simplified expression. Here are some ways to use * to expand filenames:
	• at* expands to all filenames that start with at.
	
	• *at expands to all filenames that end with at.
	
	• *at* expands to all filenames that contain at.

>[!info]
>If you’re used to the Windows command prompt, you might instinctively type *.* to match all files. Break this habit now. In Linux and other versions of Unix, you must use * to match all files. In the Unix shell, *.* matches only files and directories that contain the dot (.) character in their names. Unix filenames do not need extensions and often do not carry them.

If you don’t want the shell to expand a glob in a command, enclose the glob in single quotes (''). For example, the command echo '*' prints a star

# Intermediate Commands
# grep
- The `grep` command is used to search for patterns within files. It prints lines that match the specified pattern.
- to print the lines in the /etc/passwd file that contain the text root, `grep root /etc/passwd`
- if you want to check every file in /etc that contains the word root, `grep root /etc/*`
- grep understands regular expressions, patterns that are grounded in computer science theory and are very common in Unix utilities. 
- Regular expressions are more powerful than wildcard-style patterns, and they have a different syntax. 
- There are three important things to remember about regular expressions:
	.* matches any number of characters, including none (like the * in globs and wildcards).
	.+ matches any one or more characters.
	. matches exactly one arbitrary character.
## less
## pwd
## diff
## file
## find and locate
## head and tail
## sort
