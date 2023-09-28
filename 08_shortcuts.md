## Shortcuts

- `Clear Terminal`: Ctrl + l
- `Line Jump to start`: Ctrl + a
- `Line Jump to end`: Ctrl + e
- `Jumping words to left`: Option + left arrow
- `Jumping words to right`: Option + right arrow
- `Swapping Words`: Ctrl + t

### Killing the lines

- `Ctrl + k`: kills the line from current cursor to end of line.
- `Ctrl + u`: kills the line from current cursor to beginning of line.

### Killing words

- `Option + del`: kills the word from current cursor to begginning of line. 

### Reviving Killed Text

When we kill texts, it stored in a memory in an area known as the `kill-ring`.

We can retrive the most recently killed text by:

```bash
ctrl + y
```


## History

We can see all the recent commands in one place by history command.

```bash
history
```

### History Expansion

We can easily run an earlier command by using line number from history.

For example, to run 793rd command, run:

```bash
!793
```


### Seaching Histoy

Type `ctrl + r` to enter `reverse-i-search`. As we start typing, shell will search for history and show the best match.

Hit `ctrl + r` again and again for best matches.