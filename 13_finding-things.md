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

To find in current directory
```bash
find ./
```

To find empty files/folders
```bash
find ./ -empty
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

### Finding by time

> +n for greater than n minutes, -n for less than n minutes, n for exact n minutes, 
> where n is a number

#### 'min' is minutes

```bash
find ~/Documents -mmin -n
```

```bash
find ~/Documents -cmin +n
```

```bash
find ~/Documents -amin n
```

#### 'time' multiples number with 24 and outputs the findings

```bash
find ~/Documents -mtime -n
```

```bash
find ~/Documents -ctime n
```

```bash
find ~/Documents -atime +n
```

### Finding by Logical Operators (and, or, not)

To find files whose name should not end by '.jpg':

```bash
find ~/Pictures -not -name "*.jpg"
```

To find files whose name should end by '.jpg' or '.png':

```bash
find ~/Pictures -name "*.jpg" -or -name "*.png"
```


To find files whose name should contain 'will' and 'pexels':

```bash
find ~/Pictures -name "*will*" -and -name "*pexels*"
```

> we can also pass additional options in it like mtime, mmin, etc



### User Defined Actions

We can provide find with our own action to perform using each matching pathnames.

The syntax is:

```bash
find -exec command {} ;
```

> The `{}` are  placeholder for the current pathname (each matches)
> The semicolon `;` is required to indicate the end of the command


To delete every file that contains 'broken' in its filename:

```bash
find ~ -name "*broken*" -exec rm '{}' ';'
```

> We need to wrap {} and ; in quotes because they have special meanings

To find all the files that are owned by user 'shahabaz' and then list out the full detail or each matching:

```bash
find ~ -type f -user shahbaz -exec ls -l '{}' ';'
```

To find all the files end with .html and copy them and create '{filename}_COPY'

```bash
find ./ -type f -name '*.css*' -exec cp '{}' '{}_COPY' ';'
```


## xargs command

When we provide a command via -exec, that command is executed separately for every single element. 

We can instead use a special command called `xargs` to build up the input into a bundle that will provide as an argument list to the next command.

```bash
find ./ -name '*.css*' | xargs ls -l
```

By using `exec` it will be like:

```bash
find ./ -name '*.css*' -exec ls '{}' ';'
```

> With xargs command, we can also pass arugent to next command form previus command through pipeline which doesnt takes it.

```bash
find ./ -name "chapter[1-5].txt" | xargs cat > fullbook.txt
```

```bash
echo hello world | xargs mkdir
```

