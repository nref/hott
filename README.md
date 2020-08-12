## hott.sh

```
hott.sh: Hot Online Test Tool: a poor man's hot-reloader.
USAGE: ./hott.sh <command> <args> <file1> [<file2> ... <fileN>]
When any of the files changes, 
any process matching <command> exactly will be killed, 
and "<command> <args>" will be run.
```

## Example

### Shell 1
```
> touch test.txt
> ./hott.sh ls -lah *.txt
ls -lah
total 20K
drwxr-xr-x  3 pi pi 4.0K Aug 12 19:25 .
drwxr-xr-x 13 pi pi 4.0K Aug 12 19:23 ..
drwxr-xr-x  8 pi pi 4.0K Aug 12 19:23 .git
-rwxr-xr-x  1 pi pi  706 Aug 12 19:23 hott.sh
-rw-r--r--  1 pi pi 1.1K Aug 12 19:23 LICENSE
-rw-r--r--  1 pi pi    0 Aug 12 19:25 test.txt
```

### Shell 2
```
> touch test.txt
```

### Shell 1
```
ls -lah
total 20K
drwxr-xr-x  3 pi pi 4.0K Aug 12 19:25 .
drwxr-xr-x 13 pi pi 4.0K Aug 12 19:23 ..
drwxr-xr-x  8 pi pi 4.0K Aug 12 19:23 .git
-rwxr-xr-x  1 pi pi  706 Aug 12 19:23 hott.sh
-rw-r--r--  1 pi pi 1.1K Aug 12 19:23 LICENSE
-rw-r--r--  1 pi pi    0 Aug 12 19:26 test.txt
```

### Shell 2
```
> echo test > test.txt
```

### Shell 1
```
ls -lah
total 24K
drwxr-xr-x  3 pi pi 4.0K Aug 12 19:25 .
drwxr-xr-x 13 pi pi 4.0K Aug 12 19:23 ..
drwxr-xr-x  8 pi pi 4.0K Aug 12 19:23 .git
-rwxr-xr-x  1 pi pi  706 Aug 12 19:23 hott.sh
-rw-r--r--  1 pi pi 1.1K Aug 12 19:23 LICENSE
-rw-r--r--  1 pi pi    5 Aug 12 19:26 test.txt
```

## Projects Using

- https://github.com/slater1/gpio

