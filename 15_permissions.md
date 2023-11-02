## Multiple Users

Unix and unix-like systems are multiuser os. More than one person can be using the same computer at the same time.

Additionally, users can belong to groups which are given access to particluar file and folder by their owners.

> A regular user do not have permission to write or even read every file on the machine.


### User and Group ID

When a new user account is made, it is assigned a user id. The user is also assigned a group id.

> We can use `id` command to view it.


## File Attribute

The weird looking 10 characters printed out are file attribute.

```bash
-rw-r--r--
```

> These characters tell us the type of file, the read, write and execute permission for the file owner


## File Type

The first character indicates the type of the file.

Some of the most common types and their corresponding attributes are:

- `-`: regular file
- `d`: directory
- `c`: character special file
- `l`: symbolic link


### Permission
- `r`: file can be read
- `w`: file can be modified
- `x`: file can be executed
- `-`: files cant be read, modified or executed



```bash
rwx
```

```bash
r-x
```

```bash
rw-
```

```bash
r--
```

```bash
---
```



### Owner
First 3 characters after file type specifies permission of owner.

### Group
After first 3 characters, next 3 characters specifies permission of group.

### Word
Last 3 characters specifies permission of rest of the world.

```bash
-rwxrw-r-x
```
