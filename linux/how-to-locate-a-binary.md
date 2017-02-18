# How to locate a binary (program)?

Sometimes i am asking myself where a specific binary is located in a linux system.

To find a binary i use `which`:

```
$ which php
/usr/local/bin/php
```

This command returns me the php binary, which will be used when i run `php` on console.

Sometimes there are more than one version of a binary (program).
If i want to know all paths, i simply can run `where` instead of `which`.
That command will tell me all paths of a specific binary.

```
$ where php
/usr/local/bin/php
/usr/local/bin/php
/usr/bin/php
```
