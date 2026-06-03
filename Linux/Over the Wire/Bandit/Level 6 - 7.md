
The password for the next level is stored **somewhere on the server** and has all of the following properties:


- owned by user bandit7
- owned by group bandit6
- 33 bytes in size


Use the next level login:
~~~
ssh -p 2220 bandit6@bandit.labs.overthewire.org
~~~

password: `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`  

  <br>
  
Using the find command and the options -user and specifying the user name bandit7 and the  -group and specifying bandit6 as the group. Also using  -size for  the bytes and adding `2>dev/null` to filter out permission errors.    

```
find / -size 33c -user bandit7 -group bandit6 2>/dev/null
```

<br>

Which will give us the output of `/var/lib/dpkg/info/bandit7.password` and then just cat that output:

```
cat /var/lib/dpkg/info/bandit7.password
```

The password for the next level (level 7) is :

```
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```






