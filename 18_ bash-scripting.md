## Bash Scripting

- Write a script in a file and save it
- Make the script executable using chmod
- Verify that shell can find the script


### Shebang
The first line of script should read:

```bash
#!/user/bash
```

It is not necessary to use bash only, we can also use python, nodeJS etc in shebang, then we can write script in python

```bash
#!/user/python3
```

```bash
#!/user/node
```


### Executing the script
We can execute the script manually like this:

```bash
bash pathToFile
```

For example:

```bash
bash ~/script/greet
```


> To run python, node or other files, use their name, like:

```bash
node hello
```


### Locating Command

When we run any command like `pwd, ls, echo`, the shell starts looking for the executable programs in the list of directories stored in the PATH variable.

```bash
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

> It will look for the command in those above dorectories


If we want the shell to find our own programs, we need to make sure we put them in a folder that is in the `PATH` variable

> A common place to put user defined programs is bin folder in home directory. like:

```bash
~/bin

/Users/shahbaz/bin
```

To add this this directory in PATH, save the below line in `.bashrc` file:

```bash
PATH="$HOME/bin:$PATH"
```

and then run the .bashrc file:

```bash
source ~/.bashrc
```

After that directory will be added in the path

We can see it by running `$PATH` command

```bash
/Users/shahbaz/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```