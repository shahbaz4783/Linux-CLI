```bash
find ./ -name '*closed*' | wc -l
```

```bash
find ./ -name '*CLOSED*'
```

```bash
find ./ -iname '*closed*' | wc -l
```

```bash
find ./ -iname '*[13579]_open*' |wc -l
```

```bash
find ./ -empty
```

```bash
find ./ -size +20k
```

```bash
find ./ -size +150k -and -iname '*closed*'
```

```bash
find ./ -newer yesterday.txt
```