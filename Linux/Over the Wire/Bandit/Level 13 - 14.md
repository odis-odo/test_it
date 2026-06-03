
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

Use the next level login:
~~~
ssh -p 2220 bandit13@bandit.labs.overthewire.org
~~~

password: 
```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

  <br>

Using the `ls -l`  we get the output of:

`-rw-r----- 1 bandit14 bandit13 1679 Sep 19  2024 sshkey.private`

As part of the group bandit13 we can read the file so we can ssh with the option `-i` for identifier for the ssh  key and using the username as bandit14 to the local host:

```
ssh -p 2220 -i sshkey.private bandit14@localhost
```

Then you are connected to bandit 14 which did not require a password.



<br>


The password for the next level (level 14) is :

```
Signed in with ssh key
```






