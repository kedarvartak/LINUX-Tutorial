
# The Shell: Getting Started

## Table of Contents

* [Introduction](#introduction)
* [What is the Shell?](#what-is-the-shell)
* [The Bash Shell](#the-bash-shell)
* [Understanding the Shell Prompt](#understanding-the-shell-prompt)
* [Running Your First Command](#running-your-first-command)

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

## Running Your First Command

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

