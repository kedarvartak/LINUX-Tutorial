
# Linux Command Line Cheatsheet

## Index
1. Filename vs File Type
2. file Command
3. less Command
4. history Command
5. clear Command
6. Tab Autocomplete
7. cp (Copy) Command


## 1. Filename vs File Type

You can name a file anything. For example, you can name a file banana.jpeg and it may not actually be a JPEG.
To see what it actually is, use the `file` command.


## 2. file Command

```bash
$ file file1
````

## 3. less Command

```bash
$ less file1
```

Use `Space` to go down a page
Use `b` to go up
Press `q` to quit
Use `/` to search for text inside the file


## 4. history Command

```bash
$ history
```

Press the **up arrow** to go through past commands.

```bash
$ cat file1
$ !!
# runs the last command again
```


## 5. clear Command

```bash
$ clear
```

## 6. Tab Autocomplete

Start typing the beginning of a command or file, then press `Tab`.
If there are multiple matches, press `Tab` twice to see all.

## 7. cp (Copy) Command

```bash
$ cp file1 /home/pete/Documents
```

```bash
$ cp mycoolfile /home/pete/Documents/cooldocs
```

```bash
$ cp file1 file2 file3 /home/pete/Documents
```

Wildcards:

* `*` matches anything
* `?` matches a single character
* `[abc]` matches any character in the set

```bash
$ cp *.jpg /home/pete/Pictures
```

```bash
$ cp -r myfolder /home/pete/Documents
```


