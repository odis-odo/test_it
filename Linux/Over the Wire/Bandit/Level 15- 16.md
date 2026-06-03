
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.

Use the next level login:
~~~
ssh -p 2220 bandit15@bandit.labs.overthewire.org
~~~

password: n
```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

  <br>

First we can cat the current password for level 15 `cat /etc/bandit_pass/bandit15`

Then we pipe it into the `openssl s_client`  command:

```
cat /etc/bandit_pass/bandit15 | openssl s_client -connect localhost:30001
```

<br>

Also add `-ign_eof` at the end if you are getting **Renegotiating** as follows:

```
cat /etc/bandit_pass/bandit15 | openssl s_client -connect localhost:30001 -ign_eof
```


Which will then give the password for the next level .

`read R BLOCKCorrect! kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx`




<br>


The password for the next level (level 16) is :

```
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```






