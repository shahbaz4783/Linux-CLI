# Expansion and Substitution


## WildCard Characters

We can use multiple wildcard characters to build patterns that can match multiple filenames at once.


### The asterisk (*)

It represents 0 or more characters in a filename.

```bash
ls -l *.txt
```

>It will match any file that will end with `.txt`


```bash
echo *.html
```

>It will match any file that will end with `.html`


```bash
echo *p
```

>It will match any file that will start with `p`


```bash
ls -l *at*
```

>It will match any file that includes `at`. Like cat.txt, data.txt so on


### The Question Mark (?)

It represents any single character.

```bash
ls style.???
```

> It will match any file name `style` that will end by 3 character file extension. Eg, style.css, style.txt etc

```bash
ls style?.css
```

> It will match any fil name `style` which have 1 character before extension. Eg, style1.css, style2.css, styleA.css, stylex.css etc


```bash
ls index?.??
```

> It will match any fil name `style` which have 1 character before extension and two character inextensio. Eg, index1.js, index2.py, indexA.js, indexy.js etc


```bash
mv style?.??? ./styles
```

> This will move all the files starting with `styles` which have 1 character before extension and 3 at extension. Like style1.css, style2.css


### The Square Bracket ([])

Inside square brackets, we can specify a range of characters to match.

```bash
ls pic[153].jpg
```

> It will only match pic1.jpg, pic3.jpg, pic5.jpg

```bash
ls [A-G]* 
```

> It will match any file that will begin with a capital letter from A to G

```bash
ls file[1-9]
```

> It will match file1 to file9


### Negating Ranges

Inside square brackets, we can specify a range of characters to not match, using a caret (^)

```bash
ls [^a]*
```
> It will match those files which will not start with a

```bash
ls [^0-9]*
```

> It will match those files which will not start with a numeric digit 0-9


### Character Classes
We can also use predefined named charactered classes

```bash
echo [[:upper:]]
```
> Any file that start with an uppercase letter

```bash
echo [[:lower:]]
```
> Any file that start with a lowercase letter

```bash
echo [[:digit:]]
```
> Any file that start with a digit (0-9)


## Brace Expansion

It will generate multiple string based on a pattern

```bash
touch page{1..10}.txt
```

> It will generate 10 new files, page1.txt, page2.txt to page10.txt


```bash
mkdir feb{1..28}
```

> It will create 28 folders, named feb1, feb2 to feb28

```bash
echo {7..50..4}
```

> It will print numbers with interval of 4, like 7, 11, 15...47


```bash
echo plan-{a..d}
```

> It will print plan-a plan-b plan-c plan-d


```bash
echo {a,b,c}{1,2,3}
```

> It will print a1 a2 a3 b1 b2 b3 c1 c2 c3


### Nested Brace Expansion

```bash
echo {x,y{1,2,3},z}
```

> It will print x y1 y2 y3 z


## Arithmetic Expansion

```bash
echo $((2+4))
```

```bash
echo $((2*4))
```

```bash
echo $((10/4))
```

```bash
echo $((10%4))
```

```bash
echo $((3**4))
```

> It only outputs whole numbers, it will not give decimals.



## Quoting

```bash
echo hello my name is         Linux
```

> This will ignore space and print it without whitespace.

To get whitespaces, use quotes.

### Double Quotes ("...")

```bash
echo "my name is      Linux"
```

> This will add whitespace

```bash
echo "today is...    $(date)"
```

> This will also run date command. To not run commmands in quotes, use single Quotes


### Single Quote

```bash
echo 'today is...    $(date)'
```

> It will add whitespaces and also not run date commmand