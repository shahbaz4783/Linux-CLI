## Delete

### Deleting Files

To delete files, use:

```bash
rm <filename>
```

To delete `myProject.txt` file, run:

```bash
rm myProject.txt
```

> We can delete multiple files like this:

```bash
rm note.txt script.js index.html style.css
```

### Deleting Folders

To delete empty directory, run:

```bash
rm -d Movies
```

To delete folder which are not empty, run:

```bash
rm -r WebSeries
```

> Deleting files and folder cant be undo, and doesnt stores in bin to retrive.


## Moving Stuffs

To move files and folder, use:

```bash
mv <source> <destination>
```

To move `app.css` to `styles` directory, use:

```bash
mv app.css styles/
```

> We can move multiple files as well


### Renaming

We can rename files and folder by move command.

```bash
mv <current> <newname>
```

To rename app.css to style.css, run:

```bash
mv app.css style.css
```


## Copying

To copy files and folder, use:

```bash
cp <source> <destination>
```

To copy todo.txt called mytodo.txt, run:

```bash
cp todo.txt mytodo.txt
```


To copy multiple files into another directory, use:

```bash
cp file1 file2 directory_name
```
