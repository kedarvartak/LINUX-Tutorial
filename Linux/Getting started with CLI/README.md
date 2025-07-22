
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

---

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
