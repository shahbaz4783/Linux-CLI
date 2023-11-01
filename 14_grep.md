## grep

`grep` command searches for pattern in each file's contents.
Grep will print each line that matches a pattern we provide.

```bash
grep PATTERN <file-name>
```

For Example;

```bash
grep 'lion' animal.txt
```
It will print each line form animal.txt that contain the pattern 'lion'.


### Case Insensitive

To make searches case insensitive, use `i` option.

```bash
grep -i 'Lion' animal.txt
```

### Word Search

```bash
grep -w 'cat' animal.txt
```

> -w option ensure that it will only search for words, not for fragments.
> For example, it will search for 'cat' not 'concat' or ant other.


### Recursive Search

```bash
grep -r 'javascript'
```

> -r option performs a resursive search.
> If we dont specify a starting directory, grep will search the current working directory.

```bash
grep -r 'command' myCommands/
```
> It will search command word under 'myCommand' directory recursively.

```bash
grep -ri "ca[tr]" House/
```

> It will search cat and car in House dir

