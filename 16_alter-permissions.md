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
  chmod g+r secreat.txt
  ```

- To grant only read permisson to all
  ```bash
  chmod a=r secreat.txt
  ```

- To remove write permisson to owner
  ```bash
  chmod u-r secreat.txt
  ```

