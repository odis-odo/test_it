
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Use the next level login:
~~~

~~~

password: 
```

```

  <br>

To get the password first we cat the `/etc/bandit_pass/bandit14` copy and paste it but another way is to pipe into the command `nc` (netcat) or using nc first then copying the password as follows:

```
nc localhost 30000
```

This will show a blank field which would be where you paste the password itself.

<br>

This is piping the file which would pipe the password directly:

```
cat /etc/bandit_pass/bandit14 |  nc localhost 30000
```

Which then gives us the password for the next level.

`Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo`


<br>


The password for the next level (level 15) is :

```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```






