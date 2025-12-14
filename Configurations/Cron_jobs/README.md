# Schedule Cron Jobs in your workflow

The schedule event allows you to trigger a workflow at a scheduled time.

For example:

```
 on:
   schedule:
     - cron: "15 4,5 * * *"
```


To run at specific UTC times use POSIX cron syntax - https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07

Scheduled workflows run on the latest commit on the default branch. The shortest interval you can run scheduled workflows is once every 5 minutes.

POSIX cron syntax:

```
┌───────────── minute (0 - 59)
│ ┌───────────── hour (0 - 23)
│ │ ┌───────────── day of the month (1 - 31)
│ │ │ ┌───────────── month (1 - 12 or JAN-DEC)
│ │ │ │ ┌───────────── day of the week (0 - 6 or SUN-SAT)
│ │ │ │ │
* * * * *
```


Operator	Description	Example
```
| Operator | Description | Example | 
| *	| Any value  |	15 * * * * runs at every minute 15 of every hour of every day. |
| ,	| Value list | separator	2,10 4,5 * * * runs at minute 2 and 10 of the 4th and 5th hour of every day. | 
| - |	Range of values | 	30 4-6 * * * runs at minute 30 of the 4th, 5th, and 6th hour. | 
| /	| Step values	| 20/15 * * * * runs every 15 minutes starting from minute 20 through 59 (minutes 20, 35, and 50).|
```

**Reference:** https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#schedule



