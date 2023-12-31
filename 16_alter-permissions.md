## Change Mod (chmod)

When specifying permission with chmod, we use special syntax:

### For whom we are changing permission

- `u`: user (owner of the file)
- `g`: group (member of the group)
- `o`: others (rest of peoples)
- `a`: all of the above

### What we are doing (adding and removing permission)

- `-`: remove
- `+`: grant
- `=`: set one, remove all

### Which values we want to alter

- `r`: read permission
- `w`: write permission
- `x`: execute permission


### Examples

- To grant read permisson of group
  ```bash
  chmod g+r secret.txt
  ```

- To grant only read permisson to all
  ```bash
  chmod a=r secret.txt
  ```

- To remove write permisson to owner
  ```bash
  chmod u-r secret.txt
  ```

### chmod with octal notation

| Octal | Binary | File mod |
|-------|--------|----------|
|   0   |   000  |    ---   |
|   1   |   001  |    --x   |
|   2   |   010  |    -w-   |
|   3   |   011  |    -wx   |
|   4   |   100  |    r--   |
|   5   |   101  |    r-x   |
|   6   |   110  |    rw-   |
|   7   |   111  |    rwx   |

> It takes 3 values, one for user, one for owner, one for rest of peoples.

For example:

```bash
chmod 700 secret.txt
```
> It will give all permisson to user, and remove all permisson from group and rest of peoples

```bash
chmod 516 secret.txt
```
> read and execute to user, only execute to group, read and write to rest of peoples


## Substitute User (su)

We can use `su` command to change user from within our own shell session.

```bash
su - alex
```

> It will change the environment too.

```bash
su alex
```

> It will not change the environment.

> To leave the session, type `exit`



## sudo

Some command are not allowed. To run them, use `sudo` before that command.

```bash
sudo command
```

> It will ask to enter user password.


## Change Ownership (chown)

```bash
chown alex songs.txt
```

> It will make alex the owner of songs.txt file


```bash
chown alex:singer songs.txt
```

> It will make alex the owner of songs.txt and also change the file group owner to the group named 'singer'.

```bash
chown :singer songs.txt
```

> It will only change the file group owner.
