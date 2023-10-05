## Standard Streams

Standard streams are comminication channels between a computer program and its environment.

They are:

- Standard Input
- Standard Output
- Standard Error

1. `Standard Output`:
It is a place to which a program or command send information.

2. `Standard Input`:
   It is where a program or command gets its input. By default a shell directs standard input from keyboard. The input infomation could come from a keyboard, a file, or even from another command.

3. `Standard Error`:
   Command and program also have destination to send error, which is standard error. By default, the shell directs standard error information to the screen for us to read, but we can change that destination if needed.


## Redirecting Standard Output

The Symbol '>' tells the shell to redirect the output of a command to a specific file instead of the screen.

```bash
command > filename
```

For eg:

```bash
ls -l > list.txt
```

This will create a file named 'list.txt' and redirect ls command ouptut in it.

> Previous data in file will lost if it had any after redirecting.


### Appending

To keep the existing contents of the file and add new content to the end of the file, use `>>` when redirecting.

```bash
command >> filename
```

For example:

```bash
ncal -3 >> ./folder/calender.txt
```


## Redirecting Staandard Input

`<` Symbol is used to pass the content of a file to standard input. 

```bash
command < filename
```

For example, we can pass the content of movies.txt to cat command using :

```bash
cat < movies.txt
```

## Redirecing Standard Input & Output Together

We can redirect standard input and output at the same time like this:

```bash
ls < mylist.txt > yourlist.txt
```

## Standard Error

By default, the error messages are outputed to the screen, but we can change this by redirecting standard error.

```bash
ls -error 2> errorlog.txt
```

> `>2` Symbol used for error, although for std output we can also use `1>` symbol instead of just `>`



## Redirecing Standard Output & Error Together

```bash
command file.txt > output.txt 2> error.txt
```

To concat 2 files and output on another file as well output error if any, use:

```bash
cat ./folder/calender.txt ./folder/mylist.txt > mylistNcal.txt 2> ./folder/errorlog.txt
```

> Standard Output always should be written first and then standard error.

### Shorter Syntax

If we want to redirect standard output and error in same file, we can use sorter stntax.

```bash
command file.txt > output.txt 2>&1
```

### Another Shorter Syntax

```bash
command file.txt &> output.txt
```