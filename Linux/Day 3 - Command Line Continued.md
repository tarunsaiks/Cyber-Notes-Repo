# Beginner's Guide to Basic Commands and Shell Customization in Linux

Welcome to the world of Linux! Whether you're diving into the command line for the first time or looking to enhance your skills, understanding basic commands and customizing your shell environment is essential. Let's embark on this journey together and explore some fundamental concepts step by step.

## Changing Your Password and Shell

Feeling like it's time for a password update? 

No worries! Linux makes it easy with the `passwd` command. Simply type `passwd`, follow the prompts, and voilà, your new password is set. Remember, the longer and more complex, the better!

```bash
$ passwd
```

As for your shell, if you're curious about exploring alternatives like zsh, fish or ksh, you can use the `chsh` command. Just keep in mind that examples in this guide assume you're using bash. 

> I recently setup fish and it looks clean and aesthetic, Thanks Michael Taggart!!

# Hidden Files

Ever wondered why some files start with a dot? Those are called dot files or directories, and they typically hold configuration settings. To view them, try running `ls -a` in your home directory. You might be surprised by what's hidden!

```bash
$ ls -a
```

## Environment and Shell Variables

Shell variables are like post-it notes for your shell, handy for storing temporary values. Want to set one? Easy peasy! Just remember, no spaces around the equals sign.

```bash
$ STUFF=blah
```

To transform a shell variable into an environment variable, use `export`.

```bash
$ export STUFF
```

## The Command Path

Ever wondered how your shell finds commands? It's all thanks to the `PATH` environment variable, which lists directories to search. Need to add a custom directory? Just tweak your `PATH` variable!

```bash
$ PATH=dir:$PATH
```

## Special Characters

Linux is full of characters with special powers! From the star symbol to the tilde, each has its own role. Here's a cheat sheet to help you decode them.

```markdown
| Character | Name(s)        | Uses                                     |
|-----------|----------------|------------------------------------------|
| *         | star, asterisk | Regular expression, glob character       |
| .         | dot            | Current directory, file/hostname delimiter|
| !         | bang           | Negation, command history                |
| |         | pipe           | Command pipes                            |
| /         | forward slash  | Directory delimiter, search command      |
| \         | backslash      | Literals, macros                         |
| $         | dollar         | Variables, end of line                   |
| '         | tick, quote    | Literal strings                          |
| `         | backtick       | Command substitution                     |
| "         | double quote   | Semi-literal strings                     |
| ^         | caret          | Negation, beginning of line              |
| ~         | tilde          | Negation, directory shortcut             |
| #         | hash, pound    | Comments, preprocessor, substitutions    |
| [ ]       | square brackets| Ranges                                   |
| { }       | braces         | Statement blocks, ranges                 |
| _         | underscore     | Cheap substitute for a space             |
```

## Command-Line Editing

Tired of reaching for the mouse? Master these control key combinations for lightning-fast command-line editing!

```markdown
| Keystroke | Action                          |
|-----------|---------------------------------|
| CTRL-B    | Move the cursor left            |
| CTRL-F    | Move the cursor right           |
| CTRL-P    | View the previous command       |
| CTRL-N    | View the next command           |
| CTRL-A    | Move the cursor to the beginning of the line |
| CTRL-E    | Move the cursor to the end of the line       |
| CTRL-W    | Erase the preceding word        |
| CTRL-U    | Erase from cursor to beginning of line        |
| CTRL-K    | Erase from cursor to end of line              |
| CTRL-Y    | Paste erased text               |
```

## Text Editors

Ready to dive into editing text files? Meet vi and Emacs, the powerhouses of Unix text editing. Choose your weapon wisely!

## Getting Online Help

Feeling lost? Don't worry, Linux has your back with extensive documentation. Whether it's the trusty `man` pages or searching for help online, there's always a solution at your fingertips.

---

And there you have it, a beginner-friendly guide to basic commands and shell customization in Linux. Armed with this knowledge, you're well on your way to becoming a command line guru!
```