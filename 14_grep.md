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


### Counting words

```bash
grep -c "javascript" app.js
```

> This will count javascript word in app.js file


## Grep Other Options

### getting lines below and above of matches.

To get 2 lines after match word
```bash
grep -A2 'javascript' app.js
```

To get 3 lines before match word
```bash
grep -B3 'javascript' app.js
```

To get 2 lines before and after match word
```bash
grep -C2 'javascript' app.js
```

To get line number where result found
```bash
grep -n 'server' app.js
```

> It will provide the line number where results found


To limit the number of matches
```bash
grep -m3 'server' app.js
```
> It will only print first 3 matches


## grep with regex

```bash
grep "c..." cricket.txt
```
> It will find words containing c followed by 4 letters.


```bash
grep "c..." cricket.txt -wo
```
> o option will print matches only, not entire file with those words u between.


```bash
grep "^c" cricket.txt
```
> It will print those words which start with c in a line.


```bash
grep "e$" cricket.txt
```
> It will print those words which ends with e in a line.


```bash
grep "2[4-8]" number.txt -o
```
> It will find and print the numbers fron 24 to 28 from numbers.txt file.


```bash
grep "2[^4-8]" number.txt -o
```
> It will exclude numbers fron 24 to 28 from numbers.txt file and print rest starting from 2.


```bash
grep "s[aeiou]" words.txt -o
```
> It will find and print words with combination of a with a,e,i,o,u



### Extended Regex

Some characters have special meanings, to use that special meaning use -E option or  `egrep` instead if `grep`.

```bash
grep "birds?" -E poem.txt
```
> Now It will find bird and birds, '?' sign knows that s is optional


```bash
grep "[aeiou]{2}" -E poem.txt
```

> It will find words having a,e,i,o,u twice together


```bash
grep "[aeiou]{2,4}" -E poem.txt
```

> It will find words having a,e,i,o,u 2 to 4 together
