## Piping

Pipes are used to transfer a stream from one program to another program.

We can take the output of one command and redirect it to the input of another command.


```bash
command1 | command2
```

For example, to reverse date output:

```bash
date | rev
```
This will print reversed date


### Piping ls command

```bash
ls /usr/bin | less
```

This will print all the lists and pass it to less command


## Difference between redirecting and piping

- `Redirect >`: Connects a command to some file
- `Piping |`: Connects a command to another command

> We can use redirect and piping in same command

```bash
ls -l /usr/bin | wc -m > ./folder/programs.txt
```

```bash
ls -l /usr/bin > ./folder/programs.txt | wc -m > ./folder/programs.txt
```