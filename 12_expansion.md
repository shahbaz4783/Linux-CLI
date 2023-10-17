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
