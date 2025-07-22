
# touch Command: Creating Files and Updating Timestamps

## Table of Contents

* [Introduction](#introduction)
* [Creating Files with touch](#creating-files-with-touch)
* [Updating Timestamps](#updating-timestamps)
* [Example: Comparing Timestamps](#example-comparing-timestamps)

## Introduction to touch

The `touch` command in Linux is commonly used to **create new empty files**. It can also be used to **update the access and modification timestamps** of existing files and directories.


## Creating Files with touch

To create an empty file, simply use:

```bash
$ touch README.md
```

This will instantly create a file named `README.md` in the current directory if it doesn't already exist.


## Updating Timestamps

If the file already exists, `touch` **does not change its content**, but it **updates the file's access and modification times** to the current time.

This is useful for:

* Marking a file as recently modified
* Forcing triggers in build tools or cron jobs that rely on timestamps


## Example: Comparing Timestamps

1. First, check the timestamp of a file using `ls -l`:

```bash
$ ls -l README.md
-rw-r--r-- 1 user group 0 Jul 22 15:03 README.md
```

2. Now run `touch` on the same file:

```bash
$ touch README.md
```

3. Check the timestamp again:

```bash
$ ls -l README.md
-rw-r--r-- 1 user group 0 Jul 22 15:17 README.md
```

As you can see, the file's **modification time** has been updated.
