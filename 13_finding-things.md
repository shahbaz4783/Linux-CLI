## locate

This comand performs a search of pathnames across our machine that match a given substring and then prints out any matching names.

```bash
locate movie
```

### Locate options

- `-e`: It will only print entries that actually exist at the time locate is run.
- `-i`: It tells locate to ignore casing.
- `-l or --limit`: It will limit the number of entries that locate retrives.


## find

This command prints out files and directory we specify

```bash
find ~/Document/projects
```

### Finding by type

We can pass option to only find and print files, directories, symbolic links, etc

To find directories:
```bash
find ~/Document -type d
```

To find files:
```bash
find ~/Desktop -type f
```

### Finding by name

```bash
find ~/Desktop -name "*.txt"
```
> -name is case sensitive, to remove case sensitive, use -iname instead of -name

```bash
find ~/Desktop -iname "*.txt"
```


### Finding by size

To find the files more than 1 gigabyte
```bash
find ~/Desktop -size +1G
```

To find the files less than 20 kilobyte
```bash
find ~/Desktop -size -20k
```

To find the files exact 2 megabyte
```bash
find ~/Desktop -size 2M
```

### Finding by owner

```bash
find -user shahbaz
```

## Timestamps

`mtime`: when last modified (content was changed)

```bash
ls -l
```
> This will show the modified time of file listed

`ctime`: when a file was last changed. This occurs anytime mtime changes but also when we rename a file, move it, or alter its permission.

> We can view ctime by this command
```bash
ls -lc
```

`atime`: when a file was last read (open)
```bash
ls -lu
```