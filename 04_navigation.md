## Root Directory

The starting point of the file system is the root folder.

It is called root, but actual directory name is '/'.


### Home or User Folder

/home for ubuntu /Users for OS X, contains a home folder for each user on the system.

For example:

```bash
/Users/Alex

/home/Alex
```

### Shortcut for navigating root and home

- root: /
- user: ~


## Print Working Directory (pwd)

It will print the current working directory, strating from the root /

```bash
pwd
```

For example, if pwd command is ran on Desktop, it will print `/Users/Alex/Desktop`.


## Lists (ls)

This will list down the contents of a directory.

```bash
ls
```

We can also list the content of specific directory using the `ls path` command.

```bash
ls /home/Alex/Documents/Movies
```

### List options

This commands accepts many options. Some most commonly used are:

```bash
ls -l
```
> This will list the content in detailed form.


```bash
ls -a
```
> This will also list the hidden files.


```bash
ls -la
```
> This will also list the hidden files in detailed form.


## Change Directory (cd)

It is used to change the current working directory, 'moving' into another directory.

```bash
cd Documents/images
```

## Going Back in Directories

In UNIX-like OS, 

- a single dot is used to represent the current directory.
- two dots (..) represents the parent directory.

So we can use `cd ..` to back up one level into the parent folder.

We can also go back more level by specifying the directory name. 

```bash
cd ../Document/Alex
```


## Relative and Absolute Paths

When providing paths to commands like cd or ls, we have the option of using realtive and absolute paths.

### Relative Paths

These paths specifies a directory/file relative to current directory.

For example, if the current directory is `/Users/Alex` and we want to cd into Documents. We simply runs:

```bash
cd Documents
```

### Absolute Paths

These Paths start from root directory (/).

We can use absolute paths to specify a location no matter our current location.

For example, if we are in `/bin` directory and want to go to Documents, we simply run:

```bash
cd /Users/Alex/Documents
```