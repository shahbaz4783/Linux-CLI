## Touch

To create a new file, use:

```bash
touch <filename>
```

For example, to create 'todo.txt' file, use:

```bash
touch todo.txt
```

We can also create files from other location.

For example, if we are in `Desktop` directory we can still create file in `Document` directory by relative or absolute paths like this:

```bash
touch ../Document/todo.txt
```

If we are in Document directory and this directory has another directory in it, eg myProjects, we can create a file in 'myProjects' from Document directory like this:

```bash
touch ./myProject/project1.txt
```


Create file on Users directory
```bash 
touch ~/todo.txt
```

We can create multiple files in one line as well by leaving a space. 

For eg:

```bash
touch file1 file2 file3 file4
```

> To give space in file name, we can do like this:

```bash
touch 'tech stacks.txt'
```

```bash
touch tech\ stacks.txt
```


### File Command

This command used to determine the file type of a specific file.

```bash
file tree.png
```


### mkdir

This command is used for creating new directories.

```bash
mkdir <foldername>
```

> We can create multiple directories, create directory form another location too. Same as touch command.

