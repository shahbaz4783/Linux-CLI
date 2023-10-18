## Question 1

```bash
touch {morning,afternoon}-day-{1..60}.txt
```

```bash
touch todos-`date +"%d-%m-%y"`.txt
```


## Question 2

```bash
ls *9.txt
```

```bash
ls *1?.txt
```

```bash
ls afternoon*7.txt
```


## Question 3

```bash
mkdir -p Year/{Summer,Winter,Spring,Monsoon}/{House,Office}
```

```bash
mkdir -p Year/{Summer,Winter,Spring,Monsoon}/{House,Office}/{todos,done}.txt
```