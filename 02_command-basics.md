# The Prompt
When we open our terminal, we will see our prompt which will likely include user@machine followed by a ~ and a dollar sign.

We will see this propmt whenever the shell is ready to accept new inputs.

All we need to do is type some commands and hit enter.


## Case Sensitive
Commands are case sensitive. For Example, Date is not same as date.

```bash
Date ❌

date ✅
```

> If you are using OS X, some commands are not case sensitive, but others are.

> Its safest to assume all commands are case sensitive.

## Arrow Keys
In the terminal, we can use the arrow keys as follows:

- `Left and Right Arrow`: move through a line of texts, one character at a time
- `Up and Down Arrow`: access previous entered commands


# Command Structure

```bash
command -option aruments
```

## Arguments

 ```bash
 ncal 2023
 ```

 - ncal command accepts values to control the specific month and year it displays.

 - If we specify only year, ncal will print the calender for entire year.

- If we specify a month and a year, ncal will print only that year's month.

```bash
ncal april 2019
```

> The sort command accepts a filename and prints sorted content of the file.

```bash
sort movies.txt
```

