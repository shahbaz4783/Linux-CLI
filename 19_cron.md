## Cron

The cron service allow us to schedule commands to run at a regular interval like:

- every 30 mins
- every day at midnight
- every 1st of month
- every 8th of June


### Editing crontab

```bash
crontab -e
```

### cron syntax

```bash
a b c d e command
```

- a : minutes     (0-59)
- b : hours       (0-23)
- c : day         (1-31)
- d : month       (1-12)
- e : day of week (0-6)


### cron characters

- *    : any value
- 3,4  : list of values   (3 and 4)
- 6-18 : range of values  (6 to 18)
- */4  : step value       (every 4)


### Examples

1. Run a job at every 30 minutes, every hour
   (every time the clock shows XX:30)

   ```bash
   30 * * * * command
   ```

   Demo:

   ```bash
   30 * * * * date >> ~/date.log
   ```


2. Run a job everyday at midnight
   (every time the clock shows 00:00)

   ```bash
   0 0 * * * command
   ```

3. Run a job every day at 8:45am

   ```bash
   45 8 * * * command
   ```

4. Run a job every monday at 2pm

   ```bash
   0 14 * * 1 command
   ```

5. Run a job every wednesday  in Febuary at 8:30pm

   ```bash
   30 20 * 2 3 command
   ```

6. Run a job at midnight every 1st day of every month

   ```bash
   0 0 1 * * command
   ```

7. Run a job at midnight every weekday (Mon-Fri)

   ```bash
   0 0 * * 1-5 command
   ```

8. Run a job at every 4 minutes

   ```bash
   */4 * * * * command
   ```


### Error Handling

Sometime we might run incorrect commands, which will result in errors. It will not be printed to find the error. But we can pint errors by passing standard errors

```bash
 */4 * * * * dateo >> ~/time.log 2>&1 
```

> dateo is not correct command, this error will now be printed out in time.log file.

