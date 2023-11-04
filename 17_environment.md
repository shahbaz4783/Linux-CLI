## Viewing Environment

```bash
printenv
```

## Parameter Expansion

```bash
echo $USER
```

```bash
echo $PWD
```

```bash
echo $OLDPWD
```

## Defining Variables

```bash
variable=value
```

This will define variable for current shell session.


To define environment variable:

```bash
export variable=value
```

For example:

```bash
export country=India
```

```bash
export city="New Delhi"
```


## Customise Prompt

Write this command is .bashrc file.
It can be found at `~/user/.bashrc`

```bash
PS1='/u/@'
```
Then run the file by:

```bash
source ~/.bashrc
```

> It will show username and time in prompt
> We can customise it more by looking at PS1 man page or google.


## Aliases

We can define our own command by using `alias` keyword.

```bash
alias 'your-command-name'='actual-command'
```

```bash
alias ll='ls -la'
```

This will run ls `-la` command by running `ll` command

> We have to keep them in `.bashrc` file

We can also create another file by name .bash_aliases and put these lines in .bashcnfile

```bash
if [ -f ~/.bash_aliases ] ; then
    . ~/.bash_aliases
fi
```