## cat

The cat command concatenates and prints the content of files.

```bash
cat <filename>
```

If we provide multiple files, it will concatenate their contents and output them.

```bash
cat <file1> <file2> <file3>
```

## less

This command displays the contents of a file, one page at a time. 

```bash
less <filename>
```

> We can navigate in it same as we navigate in manual pages.


## tac

This command is same as cat command, but is prints the content from last line to first.

```bash
tac <filename>
```

## rev

This command also prints the content but it reverses each word, like 'childeren' to 'renedlihc'

```bash
rev <filename>
```


## head

This command prints a portion of file from beginning. By default it prints 10 line of a file.

```bash
head countries.txt
```

To print specific number of line, use -n option.

For example, to print 25 lines, run:

```bash
head -n25 countries.txt
```

We can also only write number, like this:

```bash
head -25 countries.txt
```

## tails

This is same as head, but it print from end.

```bash
tail countries.txt
```