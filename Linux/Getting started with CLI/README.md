
# The Shell: Getting Started

## Table of Contents

* [Introduction](#introduction)
* [What is the Shell?](#what-is-the-shell)
* [The Bash Shell](#the-bash-shell)
* [Understanding the Shell Prompt](#understanding-the-shell-prompt)
* [Running Your First Command](#running-your-first-command)
* [pwd - Print Working Directory](#pwd---print-working-directory)

## Introduction

The shell is a powerful tool used to interact with the operating system through text-based commands. While graphical user interfaces (GUIs) like Terminal or Console offer a visual wrapper, it's the shell underneath that actually interprets and executes your commands.

## What is the Shell?

The shell is a program that:

1. Accepts commands typed by the user
2. Sends those commands to the operating system
3. Displays the result back to the user

It acts as an intermediary between the user and the core system.

## The Bash Shell

In this guide, we focus on the **Bash** shell (short for **Bourne Again SHell**), which is the default shell in most Linux distributions.

Other common shell programs include ->

* `sh` (Bourne Shell)
* `ksh` (Korn Shell)
* `zsh` (Z Shell)

## Understanding the Shell Prompt 

When you open a terminal, you're greeted with a **shell prompt**, which looks something like this:

```
username@hostname:current_directory $
```

Example:

```
pete@icebox:/home/pete $
```

Here’s what each part means:

* `pete`: Your username
* `icebox`: The hostname (name of the machine)
* `/home/pete`: The current working directory
* `$`: Indicates a regular user (it changes to `#` for the root user)

**Note:** You don’t type the `$` symbol — it’s just a prompt indicating that the shell is ready to receive a command.

## Running Your First Command - Echo , date, whoami

One of the simplest commands in the shell is `echo`. It prints the text you provide as an argument.

Example:

```bash
$ echo Hello World
```

Output:

```
Hello World
```

This verifies that the shell is working and accepting commands correctly.

$ date -> tells you the exact date and time
on the basis of what? suppose i have a remote desktop in a US Timezone, what would be the output then?

- It uses the systems local timezone setting. This timezone is usually set during the system installation or can be configured later using system tools or configuration files.

$ whoami -> tells you your desktop name

Here is the updated and properly structured continuation of your `README.md`, integrating the `pwd` section into your current style and format:

## pwd - Print Working Directory

In Linux, everything is treated as a file, and all files are organized into a **hierarchical directory structure**. This structure starts from a single root directory, represented by `/`.

Here’s a simplified example of the Linux file system:

```
/

|-- bin

|   |-- file1

|   |-- file2

|-- etc

|   |-- file3

|   `-- directory1

|       |-- file4

|       `-- file5

|-- home

|-- var
```

Each file or folder in this tree can be accessed by its **path**, which traces its location starting from the root (`/`). For instance, if you have a folder named `home`, with a subfolder `pete`, and inside that, a folder `Movies`, the complete path to the `Movies` directory would be:

```
/home/pete/Movies
```

To **know where you currently are** in this directory tree, you can use the `pwd` command.

```bash
$ pwd
```

This stands for **print working directory**, and it displays the absolute path of your current location in the filesystem.

Example:

```bash
$ pwd
/home/pete/Movies
```
The output tells you where exactly you stand within the system

Here is the structured version of the `cd - Change Directory` section in line with your current `README.md` style:

## cd - Change Directory

The `cd` command is used to **navigate between directories** in the Linux filesystem. Understanding how paths work is essential to use this command effectively.

There are two ways to specify a path:

### Absolute Path

An **absolute path** starts from the **root directory**, represented by `/`. It specifies the complete location of a directory in the filesystem.

Example:

```
/home/pete/Desktop
```

This path starts at the root and moves down through `home`, then `pete`, and finally to the `Desktop` directory.

### Relative Path

A **relative path** is based on your **current location** in the filesystem. You don’t need to start from the root. If you’re currently in `/home/pete/Documents` and want to navigate to a folder named `taxes` inside it, you can simply run:

```bash
$ cd taxes
```

This avoids the need to type the full path `/home/pete/Documents/taxes`.

### Useful `cd` Shortcuts and Flags

* `.` refers to the **current directory** (no movement).
* `..` moves to the **parent directory** (one level up).
* `~` takes you to your **home directory** (e.g., `/home/pete`).
* `-` takes you to the **previous directory** you were in.

Examples:

```bash
$ cd .      # Stay in the current directory

$ cd ..     # Move one level up

$ cd ~      # Go to home directory

$ cd -      # Switch to previous directory
```

Here is your `ls - List Directory` section, rewritten in the same clean and structured format as the rest of your `README.md`:


## ls - List Directory

The `ls` command is used to **list the contents of a directory**. By default, it lists the files and directories in your **current location**, but you can also specify a different path.

Examples:

```bash
$ ls
$ ls /home/pete
```

This will show the files and directories in the specified location.


### Hidden Files

In Linux, any file or directory that starts with a `.` is considered **hidden**. These are not shown by default with the `ls` command.

To see **all files**, including hidden ones, use the `-a` flag (stands for "all"):

```bash
$ ls -a
```


### Long Listing Format

The `-l` flag (stands for "long") shows a more **detailed view** of each file, including:

* File permissions
* Number of links
* Owner name
* Owner group
* File size
* Last modified timestamp
* File or directory name

Example:

```bash
$ ls -l
```

Sample output:

```
pete@icebox:~$ ls -l

total 80
drwxr-x--- 7 pete penguingroup 4096 Nov 20 16:37 Desktop
drwxr-x--- 2 pete penguingroup 4096 Oct 19 10:46 Documents
drwxr-x--- 4 pete penguingroup 4096 Nov 20 09:30 Downloads
drwxr-x--- 2 pete penguingroup 4096 Oct  7 13:13 Music
drwxr-x--- 2 pete penguingroup 4096 Sep 21 14:02 Pictures
drwxr-x--- 2 pete penguingroup 4096 Jul 27 12:41 Public
drwxr-x--- 2 pete penguingroup 4096 Jul 27 12:41 Templates
drwxr-x--- 2 pete penguingroup 4096 Jul 27 12:41 Videos
```


### Combining Flags

Commands in Linux often accept **multiple flags** to combine functionalities. You can combine `-l` and `-a` like this:

```bash
$ ls -la
```

This shows all files, including hidden ones, in a detailed long format.

> The order of flags (`-la` vs `-al`) doesn't matter; both will work the same.
