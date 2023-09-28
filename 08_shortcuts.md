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