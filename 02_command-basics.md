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

## Options

Options are prefix by a dash like -j, -3 etc

```bash
command -option
```

> We can turn off highlight current date by passing -h option to ncal command

```bash
ncal -h
```

### Case Matters
Lower case and upper case options works differentely. 

For example, `ncal -H` is not a valid option, but `ncal -M` is.

ncal -J is not a valid option, but ncal -j is valid and it prints julian date of calender.

> Options can also be numeric, as `ncal -3` prints previous, current and next month calender

### Combining Options

We can provide multiple option at once.

For example, this command will print previous, current and upcoming month's calender in julien form.

```bash
ncal -j -3
```

We can add more options like this:

```bash
ncal -j -3 -h
```

Another syntex

```bash
ncal -3jh
```

```bash
ncal -jhM
```

```bash
ncal -Mh3j
```

### Long Form Options

Some option supports long full word format options, which are prefixed with two dashes instead of one.

```bash
node -v

node --version
```

More examples:

```bash
sort -r movies.txt

sort --reverse movies.txt
```

```bash
sort -ru names.txt

sort --reverse --unique names.txt
```

### Options with Parameters

Some options require us to pass additonal value.

For example,  `ncal -A` requies additional value for which it will display the number of months.

```bash
ncal -A 4
```

> It will print out current month and 4 more months afterwards.

It can also be written as `-A4`

```bash
ncal -A4
```
> -B2 will print current month and preious 2 months.

```bash
ncal -B2
```

They can be written at same time too

```bash
ncal -B3 -A1
```


## Argument and Option Together

We can write options and arguments in one command together

For example:

```bash
ncal -B4 -A3 -hj august 2012
```

> We can write option first and then argument, or argument first and then option.

```bash
ncal august 2012 -B4 -A3 -hj
```

> But generally option is written before argument.