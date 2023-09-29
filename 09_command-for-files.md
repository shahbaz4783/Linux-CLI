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

## wc

This command tells the number of lines, words or bytes in files.

```bash
wc countries.txt
```

By default, it prints out three numbers: lines, words, bytes.

To print line:

```bash
wc -l countries
```

To print words:

```bash
wc -w countries
```

To print bytes:

```bash
wc -c countries
```

To print characters:

```bash
wc -m countries
```


## Sort

This comand outputs the sorted content of a file.

```bash
sort name.txt
```

To print in reverse the sorted:

```bash
sort -r name.txt
```

### Sorting Numbers

```bash
sort -n age.txt
```


### Uniques only

```bash
sort -u age.txt
```

### Sorting by field

We can specify a particular 'column' that we want to sort by, using -k option followed by field number.

```bash
sort -nk2 prices.txt
```

