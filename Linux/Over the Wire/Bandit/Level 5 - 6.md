
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties: human-readable 1033 bytes in size not executable.

So we’re looking for a file that is:

- Human readable
- 1033 bytes in size
- Non-executable


Use the next level login:
~~~
ssh -p 2220 bandit5@bandit.labs.overthewire.org
~~~

password: `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`

Using the `find` command with `/!` means it will not search a particular argument and `c` right beside the specified size looks for the size in bytes and is as follows:

```
find . \! -executable -size 1033c
```

<br>

Which will show the result `./maybehere07/.file2` and  then cat the file:

```
cat ./maybehere07/.file2
```



The password for the next level (level 6) is :

```
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```






