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



