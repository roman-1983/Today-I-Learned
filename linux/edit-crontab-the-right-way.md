# Edit crontab the right way

Today i learned, that there is more than one way to edit the crontab of a linux-system.
If you have root-access to a system, it is better to edit the system-wide crontab instead
of editing the user-specific crontab.

## Difference between `crontab -e` and `/etc/crontab`

- Via `crontab -e` you edit the users crontab.
- Via `vi /etc/crontab` you edit the system-wide crontab. 
- Via `crontab -e -u root` you edit the crontab for the user `root`. You won't edit `/etc/crontab` with that command.
- The user-related crontabs are stored in `/var/spool/cron/crontabs/<username>`

## Better use `vi /etc/crontab`
If you have root-access to a system it is better to edit the crontab with `vi /etc/crontab` instead of using `crontab -e` because you have a central point where you can check all crons.

The advantage is, that you can **set the user for execution** of every cron-command in `/etc/crontab`.


## Resources
- [Thread "Difference between /etc/crontab and “crontab -e”" at Superuser.com][1]

[1]: http://superuser.com/questions/290093/difference-between-etc-crontab-and-crontab-e