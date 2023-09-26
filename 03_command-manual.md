## Manual Pages

The man pages are a built-in form of documentation available on nearly all UNIX like OS.

> To read specific piece of documentation associated with a given command, run `man command`

For example, to know about ncal command, run:

```bash
man ncal
```

> To exit the manual page, enter `q`


### Navigating Manual Page

- `Up and Down Arrow`: Navigates Previous and Next one line.
  
- `Space Bar or F`: Navigates entire next viewport.

- `B`: Navigates entire previous viewport.


### Searching in Document

We can search for patterns in documentation. For example, to search about -w in ncal documentation, write `/-w` and hit enter.

###  Manual Pages Content

In general, each man pages follow this pattern:

- `Name or Title`: Short explanation of that command purpose.
- `Synopsis`: Synopsis of the commad syntax.
- `Description`: Description of all the command options.

#### Synopsis

```bash
  ncal [-3hjJpwy] [-A number] [-B number] [-s country_code] [[month] year]
```

> Anything listed inside square brackets are optional.

```bash
echo [-n] [string ...]
```

An ellipsis(...) indicates that one or more of the proceeding operands are allowed

[string ...] indicates that we can pass multiple strings to echo.

For example:

```bash
echo this will print as it is
```

```bash
cp [-R [-H | -L | -P]] [-fi | -n] [-alpsvXx] source_file target_file
```

In the above synopsis, `source_file` and `target_file` are two arguments which are required.

Command will not work if those arguments havent been passed.


## Manual Sections

The sections of the manual are:

1. General Commands Manual
2. System Calls Manual
3. Library Functions Manual
4. Kernel Interfaces Manual
5. File Formats Manual
6. Games Manual
7. Miscellaneous Information Manual
8. System Manager's Manual
9. Kernel Developer's Manual

### Seaching the Manual

We can search for a term within the manual using -k option

```bash
man -k term
```

To Search the for passwd:

```bash
man -k passwd
```
This will list down all the available manual section realted to passwd.

To navigate to sections, write like this:

```bash
man section_no term
```

To navigate to 5th section of passwd, write this:

```bash
man 5 passwd
```

> By default we navigate to first section. For example, `man passwd` will navigate us to first section of manual.

> For other sections, we have to sepecify the section number. 