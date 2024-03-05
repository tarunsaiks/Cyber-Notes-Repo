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
- Prints arguments to the STDOUT ()

# Navigating Directories

## cd
## mkdir
## rmdir
## Wildcards
# Intermediate Commands
## grep
## less
## pwd
## diff
## file
## find and locate
## head and tail
## sort
