## Nano Text Editor

Nano is a simple text editor that can be access from the terminal. 

It inclides all the basic text editing functionality like search, spellcheck, syntax highlighting etc.


### Opening Nano

To open a file in nano, use:

```bash
nano filename
```

For example: Open myProjects.txt file

```bash
nano myProject.txt
```

> If the specified file doesnt exists, it will create that file after saving it.


### Editing Specific Line

We can provide specific line to nano to posotion the cursor on that line.

```bash
nano +LINE FILE
```

To open myProject.txt at line number 120, run:

```bash
nano +120 myProject.txt
```


## Editing with Nano

We can movie the cursor with arrow keys. 

At the bottom, there are list of shortcuts that can used inside nano.

### Some important Shortcuts

- `Control + O`: Save File
- `Control + X`: Exit Nano
- `Control + W`: Searching
- `Control + /`: Replace